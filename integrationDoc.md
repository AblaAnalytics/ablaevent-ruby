# Setup Ruby

Follow the instructions below to send custom events from your Ruby backend.

## Install

````
gem "ablaevent-ruby"

````
## Configure

````

posthog = PostHog::Client.new({
    api_key: "PHC",
    host: "https://e.abla.io",
    on_error: Proc.new { |status, msg| print msg }
})

````
            
## Send an Event

````
posthog.capture({
    distinct_id: 'test-id',
    event: 'test-event'})

````
