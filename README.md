# AutoWindscreen
The Autowindscreens website - https://autowindscreens.co.uk/.

Brochure site with an additional bookflow process that allows customers to book in repairs or replacements for broken vehicle windows.

More info on the internal [Wiki page](https://damdigital.sharepoint.com/Wiki/_layouts/15/WopiFrame.aspx?sourcedoc={c3e155cb-66c3-4966-9450-b433ef6b21a7}&action=edit&wdLOR=&wd=target%28%2F%2FProject%20Overview%20Sheets.one%7C31ee33c2-90db-47d6-9408-80c8bfb3d8ef%2FAuto%20Windscreens%7C5476cc87-2031-45b5-9140-76f3c772b09e%2F%29&wdorigin=703)

### Architecture and Tech
It’s a standard MVC web project that uses Umbraco (v7.7.4)

The bookflow integrates with AW's backend system called Metrix. This is a standard soap webservice that is included in the project.

The Umbraco Models are built via Umbraco API rather than the DLLs.
[More info on the models builder api here](https://24days.in/umbraco-cms/2016/getting-started-with-modelsbuilder/) Scroll down to the API Models section.

### Adding and update database using migration
add-migration "XXX" -StartupProject AutoWindscreenWeb -Project AutoWindscreens.Repositories

update-database -StartupProject AutoWindscreenWeb -Project AutoWindscreens.Repositories
