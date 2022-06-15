
![Botpress Custom Module Template](readme-banner.png)

Custom Modules ⚡ supercharges ⚡ your Botpress chatbot building experience by adding in-chat capabilities and by customizing the chatbot editor to your liking.

This Github template is meant as the starting point for building Botpress Custom Modules. You can find a non-exhaustive use-case list [here](#how-do-i-do-xyz?) as well as lots of references below.

## Quick Start 

1. Click "Use this template" at the top of the Github repo or fork this repo.
2. Make your changes in the code. See [How do I do XYZ?](#how-do-i-do-xyz?)
3. To rename the package, change the folder name, the name field in [src/backend/index.ts](src/backend/index.ts) and the name field in [src/backend/index.ts](src/backend/index.ts)
4. Build using ``npm docker build``. The build will be named "YOUR_PACKAGE_NAME.tgz" and be located in the root folder.
5. Open Botpress.
6. Go to the modules page.
7. Click Upload Modules. Select and submit the tgz file. ![](1.png)
8. Click "Restart Server Now" ![](2.png)
9. In the modules page, click unpack now next to your module's name. ![](3.png)
10. Go back up to the list of Stable modules, and activate it by clicking the toggle next to the module's name. ![](4.png)
11. Start editing a chatbot. notice the flag icon for the custom module.
12. When you change your code, restart from from step 7.


## (Advanced) Where's Hot Reload?
Botpress doesn't currently support hot reload for custom module development. If you want to make changes and check them often, we recommend you clone the main repo and follow the instructions found [here](https://botpress.com/docs/building-chatbots/developers/custom-modules#local-development-tips). Changes will be reflected upon restarting the botpress server.

Generally speaking : 
1) Clone the main repo. ``git clone https://github.com/botpress/botpress.git``
2) run ``yarn && yarn build`` in the main repo path.
3) follow ["Module Templates"](https://botpress.com/docs/building-chatbots/developers/custom-modules#module-templates)
4) Follow ["Local Development Tips"](https://botpress.com/docs/building-chatbots/developers/custom-modules#local-development-tips)
5) Use the command ``yarn start`` to start the Botpress server.
6) To see changes, cancel the previous command, and use it again to restart the Botpress server and refresh your browser.

## How do I do XYZ? 

Here is a non-exhaustive list of things you can do with custom modules.

- To add Hooks / middleware : read [this](src/hooks/README.md)
- To add reusible code / actions : read [this](src/actions/README.md)
- To add new skills to the flow editor like a datepicker : inject them [here](src/backend/index.ts) - docs [here](https://botpress.com/docs/building-chatbots/developers/custom-modules#skills)  
- To create bot templates for creating new bots : add them [here](src/bot-templates/) - docs [here](https://botpress.com/docs/building-chatbots/developers/custom-modules#bottemplates)
- To create content types to be sent to your users : add them [here](src/views/lite/)
- To create a navigation page within botpress : add them [here](src/views/full/index.jsx)


## Docs and Reference 

Pro tip : 
The bot making experience is smoother than the custom module building experience. If you can, make your changes in a Botpress Bot, then migrate the changes to your custom module code. 

### Documentation
[Botpress Official Docs](https://botpress.com/docs/building-chatbots/developers/custom-modules)

### Unofficial Video Series
1) [Module Structure](https://share.descript.com/view/F7HWNQVbpEX)
2) [Creating a new module](https://share.descript.com/view/t5iYzfqHrJu)
3) [Backend, API and database](https://share.descript.com/view/C6uaCVLx5wI)
4) [Module Views](https://share.descript.com/view/5FdZBxlzrEe)
5) [Custom Content Types](https://share.descript.com/view/Bz382dj6EFG)
6) [Custom Skills](https://share.descript.com/view/dDOkVlvTaoT)
7) [Bot Templates](https://share.descript.com/view/b6OAuV8C86E)

### Example Custom Modules
[Botpress Solutions Github Repo](https://github.com/botpress/solutions/tree/master/custom%20modules)