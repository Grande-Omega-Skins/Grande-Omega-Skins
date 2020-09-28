<!-- @format -->

# Grande Omega Skins

This is a collection of unofficial skins for Grande Omega. It modifies and adds some files to make Grande Omega appear in your prefered skin.

**Use at your own risk, we're not responsible for any errors, bugs, or other stuff you might run into.**

### You're not allowed to use any of the skins during exams / tests, make sure you have a clean copy!

---

## Unofficial Official Skins

These skins are maintained by the Grande Omega Skins project and receive regular updates.

-   [Fox Dark - Foxxite](https://github.com/Grande-Omega-Skins/Fox-Dark)

-   [Wumpus Dark - VAC Efron](https://github.com/Grande-Omega-Skins/Wumpus-Dark)

-   [Midnight Jam - HoroChan](https://github.com/Grande-Omega-Skins/Midnight-Jam)

-   [Wumpus White - Stijn](https://github.com/Grande-Omega-Skins/Wumpus-White)

---

## Resource folder locations

**Normal Version**: `Grande_Omega/resources/app/desktop/Student`

**Auto Updater Version**: `Grande_Omega/bin`

---

## Requirements Installation

1. Download this repo with the "**↓** Code" button and select the ZIP file.

2. Make a **copy** of the [resource](#resource-folder-locations) folder so that you can restore it if needed.

3. Place the contents of the `dist` folder inside the [resource](#resource-folder-locations) folder.

---

## Skin Installation

Before continuing, make sure you've completed all the steps in [Requirements Installation](#requirements-installation).

**Note:** Your skin might have a different installation process. Please check the README.md of the skin before continuing.  

1. Find a skin you want to use, see the skins supported by us above.

2. Download the latest release for that skin, see the release section on the right on the repo of that skin.

3. Extract the contents of `skin-name/dist` of your chosen skin **on top** of your [resource](#resource-folder-locations) folder.

4. Replace the files you're asked to replace. Next time you start Grande Omega it should appear in your chosen skin.

To change skin, restore the [resource](#resource-folder-locations) folder from the copy you made and repeat the installation steps.

You can restore Grande Omega's original files by extracting the contents of the [Template](https://github.com/Grande-Omega-Skins/template-skin/tree/master/dist) repo to your [resource](#resource-folder-locations) folder.

---

## Contributing

1. Create a new repo based on the [Skin Template Repo](https://github.com/Grande-Omega-Skins/template-skin). See the green **Use this template** button.

2. Setup signed commits. These make sure that the commits you make come from a trusted source.

3. Make sure your Skin uses the MIT license.

4. Create your own skin by modifying the files;

    - index.html
    - wwwroot/css/style.css
    - main.js

5. Modify the script at the bottom of index.html to use the code editor theme you want to use.

    Default Script:

    ```HTML
    <script type="text/javascript" src="https://unpkg.com/monaco-themes/dist/monaco-themes.js"></script>
    <script type="text/javascript">
    	fetch("./wwwroot/themes/Eiffel.json")
    	.then((data) => data.json())
    	.then((data) => {
    		monaco.editor.defineTheme("theme", data);
    		monaco.editor.setTheme("theme");
    	});
    </script>
    ```

6. Remove all unused themes from `wwwroot/themes`.

7. Add a **README.md** file that;

    1. Links back to this repo for instructions.
    2. Include a description for your skin.
    3. Include screenshots of your skin.
    4. Include detailed installation instructions.

8. Change the skin.json file with he correct information, or the installer and/or update checker might fail (see the file structure below).

### **NOTE:** Any skins that modify the internal workings of Grande Omega will not be listed here.

---

## Skin.JSON structure

Make sure to remove the arrow comments or the JSON will not work

```JSON
{
	"name": "", <-- skin name
	"author": "", <-- skin author
	"version": 1, <-- skin version

	"resourceDir": "dist", <-- location of modified files, should always be this
	"screenshotsDir": "screenshots", <-- location of screenshots

	"modifiedFiles": ["index.html", "wwwroot/css/style.css"], <-- modified files as seen from resourceDir
	"addedFiles": ["wwwroot/css/bootstrap-dark-min.css",], <-- added files as seen from resourceDir

	"screenShots": ["1.png", "2.png", "3.png"] <-- screenshot files as seen from screenshotsDir
}
```

---

## Dev Tools

To get access to the dev tools, replace the `[resource folder]/main.js` file with the one found in the root of the repo.
