# hpe-onesphere-js
Javascript bindings to the HPE OneSphere REST API.

## Usage

Install dependency

```
yarn add "https://github.com/HewlettPackard/hpe-onesphere-js.git"
```

Example usage

```
import OneSphere from 'hpe-onesphere-js';

const oneSphere = new OneSphere(host);
oneSphere.postSession({ username: ..., password: ... })
  .then(() => oneSphere.getSession())
  .then(session => console.log('Session:', session));
```

## APIs

```
getStatus()
postSession({ username, password })
getSession()

getUsers()
addUser(...)
getUser(uri)
removeUser(uri)
getRoles()
getRole(uri)

getCatalogs()
getCatalog(uri)
getServiceTypes()
getServices()
getService(uri)
getVirtualMachineProfiles()
getVirtualMachineProfile(uri)
getTagKeys()
getTagKey(uri)
getTags()
getTag(uri)

getProviderTypes()
getProviders()
getProvider(uri)
getRegions()
getRegion(uri)
getZoneTypes()
getZones()
getZone(uri)
getRates()
getRate(uri)

getProjects()
getProject(uri)
getDeployments()
getDeployment(uri)
getMetrics(options)
```

## Development

Install
```
yarn install
```

Test
```
npm test
```

The tests are full integration tests and require the following environment variables:

```
ONESPHERE_URL='https://my.onesphere.com'
ONESPHERE_USERNAME='eric.soderberg@hpe.com'
ONESPHERE_PASSWORD='...'
```