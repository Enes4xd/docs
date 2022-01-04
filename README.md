# GitHub Docs <!-- omit in toc --> 

This repository contains the documentation website code and Markdown source files for [docs.github.com](https://docs.github.com).

GitHub's Docs team works on pre-production content in a private repo that regularly syncs with this public repo.

Use the table of contents icon <img src="./assets/images/table-of-contents.png" width="25" height="25" /> on the top left corner of this document to get to a specific section of this guide quickly.

## Contributing

See [the contributing guide](CONTRIBUTING.md) for detailed instructions on how to get started with our project. 

We accept different [types of contributions](https://github.com/github/docs/blob/main/contributing/types-of-contributions.md), including some that don't require you to write a single line of code.

On the GitHub Docs site, you can click the make a contribution button to open a PR(Pull Request) for quick fixes like typos, updates, or link fixes.

<img src="./assets/images/contribution_cta.png" width="400">

For more complex contributions, you can open an issue using the most appropriate [issue template](https://github.com/github/docs/issues/new/choose) to describe the changes you'd like to see. By this way you can also be a part of Open source contributor's community without even writing a single line of code.

If you're looking for a way to contribute, you can scan through our [existing issues](https://github.com/github/docs/issues) for something to work on. When ready, check out [Getting Started with Contributing](/CONTRIBUTING.md) for detailed instructions.

### Join us in discussions

We use GitHub Discussions to talk about all sorts of topics related to documentation and this site. For example: if you'd like help troubleshooting a PR, have a great new idea, or want to share something amazing you've learned in our docs, join us in the [discussions](https://github.com/github/docs/discussions).

### And that's it!

If you're having trouble with your GitHub account, contact [Support](https://support.github.com/contact).

That's how you can easily become a member of the GitHub Documentation community. :sparkles:

## READMEs

In addition to the README you're reading right now, this repo includes other READMEs that describe the purpose of each subdirectory in more detail:
You can go through among them for specified details regarding the topics listed below.

- [content/README.md](content/README.md)
- [content/graphql/README.md](content/graphql/README.md)
- [content/rest/README.md](content/rest/README.md)
- [contributing/README.md](contributing/README.md)
- [data/README.md](data/README.md)
- [data/reusables/README.md](data/reusables/README.md)
- [data/variables/README.md](data/variables/README.md)
- [includes/liquid-tags/README.md](includes/liquid-tags/README.md)
- [includes/README.md](includes/README.md)
- [components/README.md](components/README.md)
- [lib/liquid-tags/README.md](lib/liquid-tags/README.md)
- [middleware/README.md](middleware/README.md)
- [script/README.md](script/README.md)
- [stylesheets/README.md](stylesheets/README.md)
- [tests/README.md](tests/README.md)

## License

The GitHub product documentation in the assets, content, and data folders are licensed under a [CC-BY license](LICENSE).

All other code in this repository is licensed under the [MIT license](LICENSE-CODE).

When you are using the GitHub logos, be sure to follow the [GitHub logo guidelines](https://github.com/logos).

## Thanks :purple_heart:

Thanks for all your contributions and efforts towards improving the GitHub documentation. We thank you being part of our :sparkles: community :sparkles: !
title: Quickstart for Codespaces
intro: 'Try out {% data variables.product.prodname_codespaces %} in 5 minutes.'
allowTitleToDifferFromFilename: true
product: '{% data reusables.gated-features.codespaces %}'
versions:
  fpt: '*'
  ghec: '*'
type: quick_start
topics:
  - Codespaces
redirect_from:
  - /codespaces/codespaces-quickstart
---

## Introduction

In this guide, you'll create a codespace from a [template repository](https://github.com/2percentsilk/haikus-for-codespaces) and explore some of the essential features available to you within the codespace.

From this quickstart, you will learn how to create a codespace, connect to a forwarded port to view your running application, use version control in a codespace, and personalize your setup with extensions.

For more information on exactly how {% data variables.product.prodname_codespaces %} works, see the companion guide "[Deep dive into {% data variables.product.prodname_codespaces %}](/codespaces/getting-started/deep-dive)."

## Creating your codespace

1. Navigate to the [template repository](https://github.com/2percentsilk/haikus-for-codespaces) and select **Use this template**. 

2. Name your repository, select your preferred privacy setting, and click **Create repository from this template**.

3. Navigate to the main page of the newly created repository. Under the repository name, use the **{% octicon "code" aria-label="The code icon" %} Code** drop-down menu, and in the **Codespaces** tab, click {% octicon "plus" aria-label="The plus icon" %} **New codespace**.

  ![New codespace button](/assets/images/help/codespaces/new-codespace-button.png)

## Running the application

Once your codespace is created, your repository will be automatically cloned into it. Now you can run the application and launch it in a browser.

1. Since this example uses a Node.js project, start the application by entering `npm run dev` in the terminal. This command executes the `dev` script in the package.json file and starts up the web application defined in the sample repository.
   
   ![npm run dev in terminal](/assets/images/help/codespaces/codespaces-npm-run-dev.png)

    If you're following along with a different application type, enter the corresponding start command for that project.

2. When your application starts, the codespace recognizes the port the application is running on and displays a prompt to forward that port so you can connect to it. 

  ![Port forwarding toast](/assets/images/help/codespaces/quickstart-port-toast.png)

3. Click **Open in Browser** to view your running application in a new tab.

## Edit the application and view changes

1. Switch back to your codespace and open the `haikus.json` file by double-clicking it in the File Explorer.

2. Edit the `text` field of the first haiku to personalize the application with your own haiku.

3. Go back to the running application tab in your browser and refresh to see your changes.
   
  {% octicon "light-bulb" aria-label="The lightbulb icon" %}  If you've closed the tab, open the Ports panel and click the **Open in browser** icon for the running port.
  ![Port Forwarding Panel](/assets/images/help/codespaces/quickstart-forward-port.png)

## Committing and pushing your changes

Now that you've made a few changes, you can use the integrated terminal or the source view to commit and push the changes back to the remote.

{% data reusables.codespaces.source-control-display-dark %}
1. To stage your changes, click  **+** next to the file you've changed, or next to **Changes** if you've changed multiple files and you want to stage them all.
![Source control side bar with staging button highlighted](/assets/images/help/codespaces/codespaces-commit-stage.png)
1. Type a commit message describing the change you've made.
![Source control side bar with a commit message](/assets/images/help/codespaces/codespaces-commit-commit-message.png)  
1. To commit your staged changes, click the check mark at the top the source control side bar.
![Click the check mark icon](/assets/images/help/codespaces/codespaces-commit-checkmark-icon.png)  
    You can push the changes you've made. This applies those changes to the upstream branch on the remote repository. You might want to do this if you're not yet ready to create a pull request, or if you prefer to create a pull request on {% data variables.product.prodname_dotcom %}.
1. At the top of the side bar, click the ellipsis (**...**).
![Ellipsis button for View and More Actions](/assets/images/help/codespaces/source-control-ellipsis-button-nochanges.png)
1. In the drop-down menu, click **Push**.

## Personalizing with an extension

Within a codespace, you have access to the Visual Studio Code Marketplace. For this example, you'll install an extension that alters the theme, but you can install any extension that is useful for your workflow.

1. In the left sidebar, click the Extensions icon.

2.  In the search bar, enter `fairyfloss` and install the fairyfloss extension.

  ![Add an extension](/assets/images/help/codespaces/add-extension.png)

3. Select the `fairyfloss` theme by selecting it from the list.

  ![Select the fairyfloss theme](/assets/images/help/codespaces/fairyfloss.png)

4. Changes you make to your editor setup in the current codespace, such as theme and keyboard bindings, are synced automatically via [Settings Sync](https://code.visualstudio.com/docs/editor/settings-sync) to any other codespaces you open and any instances of Visual Studio Code that are signed into your GitHub account.

## Next Steps

You've successfully created, personalized, and run your first application within a codespace but there's so much more to explore! Here are some helpful resources for taking your next steps with {% data variables.product.prodname_codespaces %}.
  - [Deep dive](/codespaces/getting-started/deep-dive): This quickstart presented some of the features of {% data variables.product.prodname_codespaces %}. The deep dive looks at these areas from a technical standpoint.
  - [Setting up your project for {% data variables.product.prodname_codespaces %}](/codespaces/getting-started-with-codespaces): These guides provide information on setting up your project to use {% data variables.product.prodname_codespaces %} with specific languages
  - [Configuring {% data variables.product.prodname_codespaces %} for your project](/codespaces/setting-up-your-codespace/configuring-codespaces-for-your-project): This guide provides details on creating a custom configuration for {% data variables.product.prodname_codespaces %} for your project.

## Further reading

- [Enabling {% data variables.product.prodname_codespaces %} for your organization](/codespaces/managing-codespaces-for-your-organization/enabling-codespaces-for-your-organization)
- [Managing billing for {% data variables.product.prodname_codespaces %} in your organization](/codespaces/managing-codespaces-for-your-organization/managing-billing-for-codespaces-in-your-organization)
