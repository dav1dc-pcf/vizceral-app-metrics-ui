![](https://raw.githubusercontent.com/Netflix/vizceral/master/logo.png)

# Vizceral App Metrics UI

This project was forked from [vizceral-example](https://github.com/Netflix/vizceral-example)

# Setup
1. Set the end-point where you have deployed [vz-metrics-adapter](https://github.com/dav1dc-pcf/vz-metrics-adapter) in `src/components/trafficFlow.jsx`:

```
    request.get('http://vz-metrics-adapter.your-pcf.com/index.py')
```

One may also wish to tweak the interval for background refresh of the data in the same file:

```
    intervalHandle = setInterval(() => { self.beginSampleData(self); }, 4000);
```

2. Push this Vizceral NodeJS APP to your PCF/CF Foundation

```
cf login
....
cf target -o your-org -s vz-ui-space
cf push vizceral-app-metrics-ui
```

3. Ensure that at least one instance of [app-metrics-nozzle](https://github.com/dav1dc-pcf/app-metrics-nozzle) and exactly one instance of [vz-metrics-adapter](https://github.com/dav1dc-pcf/vz-metrics-adapter) have also been configured and deployed to your PCF/CF Foundation(s)

4. Open the resulting URL of the **vizceral-app-metrics-ui** application in your browser

5. **Enjoy!**
