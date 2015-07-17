
# iTunes Loved Alfred Workflow

![iTunes loved](https://cloud.githubusercontent.com/assets/2381/8754447/9af64aca-2c91-11e5-8868-ca12ee60bd3a.png)

Executes the following JavaScript via `osascript`.

```javascript
(function() {
  var track = Application("iTunes").currentTrack();
  var trackLoved = track.loved();
  var notification = (trackLoved ? "UnLoved" : "Loved") + ": " + track.name();
  track.loved = !trackLoved;
  return notification;
})()
```

Then shows a notification.

![iTunes Loved Screenshot](https://cloud.githubusercontent.com/assets/2381/8754422/6f486980-2c91-11e5-8f6a-6f40f3d82e48.png)

