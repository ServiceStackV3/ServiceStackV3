ServiceStack V3
===============

This is project is an archive containing documentation and content available for the legacy v3 BSD release of ServiceStack.

## See the [wiki for the available documentation on v3](https://github.com/ServiceStackV3/ServiceStackV3/wiki)

## NuGet

### Referencing v3 packages in New Projects

If you want a new project to use ServiceStack's v3 packages then you need to specify the version number 
when installing via NuGet, e.g:                

    PM> Install-Package ServiceStack -Version 3.9.71
    
All v3 packages can be installed the same way, e.g install **ServiceStack.Text** and **ServiceStack.Redis** with:

    PM> Install-Package ServiceStack.Text -Version 3.9.71
    PM> Install-Package ServiceStack.Redis -Version 3.9.71

### Existing Projects

Existing ServiceStack v3 NuGet packages already have a <b>[3,4)</b> version constraint applied to them which should prevent them 
from implicitly upgrading to the latest v4+ packages when installing other dependencies. 

The latest v4 ServiceStack packages requires accepting an end-user license to install the packages, 
this dialog only appears for v4 packages so if this dialog appears when upgrading ServiceStack, decline and 
use the NuGet <b>Package Manager Console</b>:

    PM> Update-Package ServiceStack -Version 3.9.71
    
#### Uninstalling an existing version

If you've mistakingly installed the wrong version of ServiceStack, it can be easily uninstalled with:

    PM> Uninstall-Package ServiceStack -Force

### NuGet package authors with a dependency on ServiceStack

If you maintain a NuGet package that has a dependency on any ServiceStack package,
it can be constrained to use only v3 packages by specifying the <b>version="[3,4)"</b>
version constraint in your ServiceStack dependency, e.g:

    <dependency id="ServiceStack" version="[3,4)" />

More info about [versioning is available on NuGet](http://docs.nuget.org/docs/reference/versioning).


## Support

Whilst there is no official direct or commercial support for the legacy v3 releases, StackOverflow remains the optimal place to ask for support. Please also include the `#servicestack-v3` hashtag when [Asking a new question](http://stackoverflow.com/questions/ask).

[Service Stack](https://servicestack.net) still hosts continuous integration builds and publishes monthly periodic releases of ServiceStack v3 to NuGet. But as there is no manual Q/A process for v3 releases, any new fixes contributed **must** be accompanied by unit or integration tests verifying the fix and **must not** change existing behavior, cause any regressions to the existing test suite or otherwise break backwards compatibility to the existing code-base. 

See the [contributing guide](https://github.com/ServiceStackV3/ServiceStackV3/wiki/Contributing) for more details.

## Source code for V3

The [BSD](https://github.com/ServiceStack/ServiceStack/blob/v3/LICENSE) source code for ServiceStack v3 is available in the **v3 branches**, i.e:

  - [ServiceStack/v3](https://github.com/ServiceStack/ServiceStack/tree/v3)
  - [ServiceStack.Text/v3](https://github.com/ServiceStack/ServiceStack.Text/tree/v3)
  - [ServiceStack.Redis/v3](https://github.com/ServiceStack/ServiceStack.Redis/tree/v3)
  - [ServiceStack.OrmLite/v3](https://github.com/ServiceStack/ServiceStack.OrmLite/tree/v3)
  - [ServiceStack.Logging/v3](https://github.com/ServiceStackV3/ServiceStack.Logging/tree/v3)
  - [ServiceStack.Contrib/v3](https://github.com/ServiceStackV3/ServiceStack.Contrib/tree/v3)

#### Example projects, use-cases, template and demos

  - [RazorRockstars/v3](https://github.com/ServiceStack/RazorRockstars/tree/v3)
  - [ServiceStack.UseCases/v3](https://github.com/ServiceStack/ServiceStack.UseCases/tree/v3)
  - [ServiceStack.Examples/v3](https://github.com/ServiceStack/ServiceStack.Examples/tree/v3)
  - [SocialBootstrapApi/v3](https://github.com/ServiceStack/SocialBootstrapApi/tree/v3)
  - [RedisAdmin UI](https://github.com/ServiceStackV3/ServiceStack.RedisWebServices)

