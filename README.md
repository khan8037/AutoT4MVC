# What's this for?

There used to be [a really sweet macro](http://stackoverflow.com/questions/2341717/can-you-do-a-runcustomtool-with-envdte-as-a-pre-build-event) for Visual Studio that would automatically run [T4MVC](http://t4mvc.codeplex.com) templates on build. Unfortunately, macro support has been removed from Visual Studio 2012+, so this is an extension that will do the same thing (and more).

T4MVC templates are run under the following conditions (all string comparisons are case-insensitive):

* a project or solution containing the template is built
* a file in a "Controllers" folder is saved (in the same project)
* the settings file "T4MVC.tt.settings.xml" (or "T4MVC.tt.settings.t4") is saved (in the same project)
* a file is added/removed/renamed in a folder named  "Assets", "Content", "Controllers", "CSS", "Images", "JS", "Scripts", "Styles" or "Views" (in the same project)

Note: Drag/drop in the Solution Explorer will not trigger the templates to re-run, as the added/removed events are not fired.

[Chirpy](http://chirpy.codeplex.com/) and [AutoTT](https://github.com/MartinF/Dynamo.AutoTT) do similar things, but Chirpy is overkill if all you want is your T4MVC templates built and I think AutoTT requires configuration.

Just build and install the template using the VSIX file, [grab it from the Visual Studio gallery](http://visualstudiogallery.msdn.microsoft.com/8d820b76-9fc4-429f-a95f-e68ed7d3111a) or **do it the easy way** and use the 'Extension & Updates' manager in Visual Studio 2012, 2013, 2015, 2017, 2019 or 2022.