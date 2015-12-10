# `/proxy/` API

The proxy API contains many utilities, generally returning content likely to be modified frequently.

## [`/proxy/users`](id:proxy-users)

### `GET /proxy/users/<name>/activity`

Gets activity events that appear in the user's activity feed. Returns an array of [activity event objects](definitions/activity_event_object.md).

### `GET /proxy/users/<name>/activity/count`

Gets the number of messages the user has, in this format:

```
{
    "msg_count": /* Messages the user currently has */
}
```

### `GET /proxy/users/<id>/featured`

Gets projects on the homepage that are featured to user personally. Returns an object of which each of its properties' values are arrays of [project objects](definitions/project_object.md):

```
{
    "custom_projects_by_following": /* Projects created by users the user is following */
    "custom_projects_loved_by_following": /* Projects loved by users the user is following */
}
```