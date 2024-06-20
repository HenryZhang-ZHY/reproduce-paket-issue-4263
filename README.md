# To reproduce

1. run `dotnet tool restore`
2. run `dotnet paket update`

You will see that paket trapped into infinite loop while resolving conflicts.

```log
The process is taking longer than expected.
Paket may still find a valid resolution, but this might take a while.
  Conflict detected:
   - Microsoft.Identity.Client 4.45.0 requested package Microsoft.IdentityModel.Abstractions: >= 6.18
   - Microsoft.IdentityModel.Logging 7.6.2 requested package Microsoft.IdentityModel.Abstractions: >= 7.6.2

The process is taking longer than expected.
Paket may still find a valid resolution, but this might take a while.
  Conflict detected:
   - Microsoft.Identity.Client 4.45.0 requested package Microsoft.IdentityModel.Abstractions: >= 6.18
   - Microsoft.IdentityModel.Logging 7.6.2 requested package Microsoft.IdentityModel.Abstractions: >= 7.6.2

The process is taking longer than expected.
Paket may still find a valid resolution, but this might take a while.
  Conflict detected:
   - Microsoft.Identity.Client 4.45.0 requested package Microsoft.IdentityModel.Abstractions: >= 6.18
   - Microsoft.IdentityModel.Logging 7.6.2 requested package Microsoft.IdentityModel.Abstractions: >= 7.6.2

The process is taking longer than expected.
Paket may still find a valid resolution, but this might take a while.
  Conflict detected:
   - Microsoft.Identity.Client 4.45.0 requested package Microsoft.IdentityModel.Abstractions: >= 6.18
   - Microsoft.IdentityModel.Logging 7.6.2 requested package Microsoft.IdentityModel.Abstractions: >= 7.6.2
```