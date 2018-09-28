![](https://raw.githubusercontent.com/Netflix/vizceral/master/logo.png)

# Vizceral App Metrics UI

This project was forked from [vizceral-example](https://github.com/Netflix/vizceral-example)

# Setup
1. Set the end-point where you have deployed in `src/components/trafficFlow.jsx`:

```
    request.get('http://vz-metrics-adapter.apps.az.dav3.io/index.py')
```

One may also wish to tweak the interval for background refresh of the data in the same file:

```
    intervalHandle = setInterval(() => { self.beginSampleData(self); }, 4000);
```

2. Push the APP to your PCF/CF Foundation

```
cf login
....
cf target -o yourorg -s vz-ui-space
cf push vizceral-app-metrics-ui
```

3. Ensure that ** and ** have also been configured and deployed to your PCF/CF Foundation

3. Open the resulting URL of the *vizceral-app-metrics-ui* application in your browser
