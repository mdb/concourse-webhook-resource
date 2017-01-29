# concourse-webhook-resource

A [ConcourseCI](http://concourse.ci) resource to issue an HTTP request to some URL from Concourse.

## Source Configuration

* `url`: *Required*. The webhook URL to which an HTTP request should be issued.

## Behavior

### `out`: Issues an HTTP request

Issues and HTTP request to the configured `url` with the configured params.

#### Parameters

* `http_method`: *Optional*. The HTTP method with which to issue the webhook request. For example: "POST". Defaults to "GET."
* `body`: *Optional*. The HTTP body to send in the request. For example: '{"foo": "bar"}'.
