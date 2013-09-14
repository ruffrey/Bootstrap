# Bootstrap

Orchard CMS Theme based on Twitter Bootstrap

### Compatibility
Orchard 1.6 or higher
Tested with Orchard 1.7
Bootstrap 2.3.2

### Installation
Package available for download in the [Orchard Gallery](http://gallery.orchardproject.net/List/Themes/Orchard.Theme.Bootstrap)

### Usage

Includes Admin panel selectable options for:

* Centered or Fluid Layout
* Fixed Top Navigation or Floating Navigation
* Primary or Inverse Navigation Bar Color
* Navigation Bar Search Field
* Sticky or Normal Footer
* Select a [Bootswatch Theme](http://bootswatch.com/2/) or Default Bootstrap Style

### Included dependencies

* Twitter Bootstrap 2.3.2 (with responsive.min.css) & HTML5 Boilerplate 4.2.0
* Font Awesome 3.2.1
* Custom shapes for LatestTwitter and AddThis widgets
* **[Bootswatch 2.x templates](http://bootswatch.com/2/)** for easy theme changes

### Adding a custom Bootstrap CSS file

1) Add the css file to `Themes\Bootstrap\Styles\`

`newtheme.min.css`

2) Create an entry for the new css file in `Themes\Bootstrap\Bootstrap.csproj`

```
<ItemGroup>
  . . .
  <Content Include="Styles\newtheme.min.css" />
</ItemGroup>
```

3) Define the style in `Themes\Bootstrap\ResourceManifes.cs` `BuildManifests( . . .)`

```
manifest.DefineStyle("newtheme.min.css").SetUrl("newtheme.min.css", "newtheme.min.css");
```

4) Add an option to the admin screen in `Themes\Bootstrap\Views\Admin\Index.cshtml`

```
<option value="newtheme.min.css" @if (Model.Swatch.EndsWith("newtheme.min.css")) { 
  <text>selected="selected"</text> 
}>@T("New Theme Display Title")</option>
```

### Bugs
Please submit issues via Github.
