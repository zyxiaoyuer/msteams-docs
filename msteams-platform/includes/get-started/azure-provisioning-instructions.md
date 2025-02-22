## Deploy your app to Azure

Deployment consists of two steps.  First, necessary cloud resources are created (also known as provisioning). Then, your app's code is copied into the created cloud resources.

# [Visual Studio Code](#tab/vscode)

Select the Teams Toolkit :::image type="icon" source="~/assets/images/teams-toolkit-v2/teams-toolkit-sidebar-icon.png"::: icon in the Visual Studio Code sidebar.

1. Select **Provision in the Cloud**.

   :::image type="content" source="~/assets/images/teams-toolkit-v2/deploy-azure/deploy-provision.png" alt-text="Screenshot showing the provisioning commands" border="false":::

1. Select a subscription to use for the Azure resources, if prompted.

   > [!NOTE]
   > There are always some Azure resources used for hosting your app.

    A dialog warns you that costs may be incurred when running resources in Azure.

1. Select **Provision**.

   :::image type="content" source="~/assets/images/teams-toolkit-v2/provision-warning.png" alt-text="Screenshot of the provisioning dialog." border="false":::

   The provisioning process creates resources in the Azure cloud. It may take some time. You can monitor the progress by watching the dialogs in the bottom-right corner. After a few minutes, you see the following notice:

   :::image type="content" source="~/assets/images/teams-toolkit-v2/deploy-azure/deploy-provision-success.png" alt-text="Screenshot showing the provisioning complete dialog." border="false":::

1. Select **Deploy to the Cloud** from the **Deployment** panel after provisioning is complete.

   :::image type="content" source="~/assets/images/teams-toolkit-v2/deploy-azure/deploy-cloud.png" alt-text="Screenshot showing the where to click to deploy to cloud." border="false":::

   As with provisioning, deployment takes some time. You can monitor the process by watching the dialogs in the bottom-right corner. After a few minutes, you see a completion notice.

Now, you can use the same process to deploy your Bot and Message Extension apps to Azure. 

# [Command Line](#tab/cli)

In your terminal window:

1. Run `teamsfx provision`.

   ``` bash
   teamsfx provision
   ```

   When prompted, select an Azure subscription to use Azure resources.

   > [!NOTE]
   > There are always some Azure resources used for hosting your app.

1. Run `teamsfx deploy`.

   ``` bash
   teamsfx deploy
   ```

---

> [!NOTE]
> **What's the difference between Provision and Deploy?**
>
> The **Provision** step creates resources in Azure and Microsoft 365 for your app, but no code (HTML, CSS, JavaScript, etc.) is copied to the resources. The **Deploy** step copies the code for your app to the resources you created during the provision step. It is common to deploy multiple times without provisioning new resources. Since the provision step can take some time to complete, it is separate from the deployment step.

Once the provisioning and deployment steps are complete:

1. Open the debug panel (**Ctrl+Shift+D** / **⌘⇧-D** or **View > Run**) from Visual Studio Code.
1. Select **Launch Remote (Edge)** from the launch configuration drop-down.
1. Select the Play button to launch your app - now running remotely from Azure!

   :::image type="content" source="~/assets/images/teams-toolkit-v2/deploy-azure/launch-remote.png" alt-text="Screenshot showing the launch app remotely." border="false":::

   Now the app running on Azure will be installed to your client!

   :::image type="content" source="~/assets/images/teams-toolkit-v2/deploy-azure/remote-app-client.png" alt-text="Screenshot showing the app being installed." border="false":::