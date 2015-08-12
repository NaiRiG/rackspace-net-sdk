# Rackspace .NET SDK
The .NET SDK for all things Rackspace.

## Migration
We are in the middle of migrating Rackspace solutions out of [OpenStack.NET](https://github.com/openstacknetsdk/openstack.net).

* [Migration Plan and FAQ](https://github.com/openstacknetsdk/openstack.net/wiki/Rackspace-and-OpenStack.NET)
* [OpenStack.NET 1.5.x Milestones](https://github.com/openstacknetsdk/openstack.net/milestones)
* [Rackspace .NET SDK 0.x Milesones](https://github.com/rackspace/rackspace.net/milestones)

## Building from Source
** Prerequisites **
* Visual Studio 2015

### Build script

Execute `build.cmd` to download all dependencies and build. Use `build.cmd help` or `build.cmd /?` to view the available command line arguments.

```bash
build.cmd [Build|UnitTest|Documentation|Package] [/Configuration Debug|Release]

# Execute Build target in Debug mode
build.cmd

# Execute UnitTest target in Debug mode
build.cmd UnitTest

# Execute Build target in Release mode
build.cmd /Configuration Release

# Execute Package target in Release mode
build.cmd Package /Configuration Release
```

### Integration Tests
You must have a Rackspace cloud account to test against in order to run the integration tests. The tests look for the credentials in environment variables: RACKSPACENET_USER and RACKSPACENET_APIKEY. After you have set the environment variables you will need to log out, then log back in.

```batchfile
setx RACKSPACENET_USER secretusername
setx RACKSPACENET_APIKEY secretpassword
```
