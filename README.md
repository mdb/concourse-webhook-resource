# concourse-webhook-resource

A [ConcourseCI](http://concourse.ci) resource to issue an HTTP request to some URL from Concourse.

This is largely a simple reference implementation illustrating how to make and test a custom Concourse resource.

[View the Docker image on DockerHub &raquo;](https://hub.docker.com/r/clapclapexcitement/concourse-webhook-resource/)

## Source Configuration

* `url`: *Required*. The webhook URL to which an HTTP request should be issued.

Example:

```
resource_types:

- name: webhook
  type: docker-image
  source:
    repository: clapclapexcitement/concourse-webhook-resource

resources:

- name: ping-some-url
  type: webhook
  source:
    url: "http://some.url"
```

## Behavior

### `out`: Issues an HTTP request

Issues and HTTP request to the configured `url` with the configured params.

#### Parameters

* `http_method`: *Optional*. The HTTP method with which to issue the webhook request. For example: "POST". Defaults to "GET."
* `body`: *Optional*. The HTTP body to send in the request. For example: '{"foo": "bar"}'.
