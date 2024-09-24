This .NET and Angular application was generaged in Visual Studio by using template "ASP.NET Core with Angular".

It's based on tutorial:
Create an ASP.NET Core app with Angular in Visual Studio
https://learn.microsoft.com/en-us/visualstudio/javascript/tutorial-asp-net-core-with-angular?view=vs-2022

To compile:
1. In PowerShell I switch folder to Angular client:
cd C:\Repos\AngularNetCore\AngularNetCore\ClientApp\

2. > npm run build

3. Run from Visual Studio as normal by pressing F5 button

Upgrade to Angular v16
1. npm install @angular/cli@16.0.0

2. npm update --all

Build errors after upgrade:
Error: node_modules/@types/node/stream/web.d.ts:458:13 - error TS2502: 'ReadableByteStreamController' is referenced directly or indirectly in its own type annotation.
458         var ReadableByteStreamController: typeof globalThis extends
                ~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Error: node_modules/@types/node/stream/web.d.ts:467:13 - error TS2502: 'ReadableStreamBYOBReader' is referenced directly or indirectly in its own type annotation.
467         var ReadableStreamBYOBReader: typeof globalThis extends { onmessage: any; ReadableStreamBYOBReader: infer T }
                ~~~~~~~~~~~~~~~~~~~~~~~~
3. Upgrade particular library:
ng update  @types/node --allow-dirty

4. RUn

> angularnetcore@0.0.0 prestart
> node aspnetcore-https

> angularnetcore@0.0.0 start
> run-script-os

> angularnetcore@0.0.0 start:windows
> ng serve --port 44470 --ssl --ssl-cert %APPDATA%\ASP.NET\https\%npm_package_name%.pem --ssl-key %APPDATA%\ASP.NET\https\%npm_package_name%.key

Workspace extension with invalid name (defaultProject) found.

