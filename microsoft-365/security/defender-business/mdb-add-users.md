---
title: Add users and assign licenses in Microsoft Defender for Business
description: Add users and assign Defender for Business licenses to protect their devices
search.appverid: MET150
author: siosulli
ms.author: siosulli
manager: deniseb 
audience: Admin
ms.topic: conceptual
ms.service: defender-business
ms.localizationpriority: medium
ms.date: 05/01/2023
ms.collection: 
- m365-security
- tier1
ms.reviewer: efratka
f1.keywords: NOCSH 
---

# Add users and assign licenses in Microsoft Defender for Business

As soon as you have signed up for Defender for Business, your first step is to add users and assign licenses. This article describes how to add users and assign licenses, and how to make sure multifactor authentication (MFA) is enabled. 

:::image type="content" source="media/mdb-setup-step2.png" alt-text="Visual depicting step 2 - add users and assign licenses in Defender for Business.":::

## Add users and assign licenses

> [!IMPORTANT]
> You must be a global administrator to perform this task.  The person who signed up your company for Microsoft 365 or for Defender for Business is a global administrator by default.

1. Go to the Microsoft 365 admin center at [https://admin.microsoft.com](https://admin.microsoft.com) and sign in.

2. Go to **Users** > **Active users**, and then select **Add a user**.

3. In the **Set up the basics** pane, fill in the basic user information, and then select **Next**.

   - **Name**: Fill in the first and last name, display name, and username.
   - **Domain** Choose the domain for the user's account. For example, if the user's username is `Pat`, and the domain is `contoso.com`, they'll sign in by using `pat@contoso.com`.
   - **Password settings**: Choose whether to use the autogenerated password or to create your own strong password for the user. The user must change their password after 90 days. Or you can choose the option to **Require this user to change their password when they first sign in**. You can also choose whether you want to send the user's password in email when the user is added.

4. On the **Assign product licenses** page, select Defender for Business (or Microsoft 365 Business Premium). Then choose **Next**. 

   If you don't have any licenses available, you can still add a user and buy additional licenses. For more information about adding users, see [Add users and assign licenses at the same time](../../admin/add-users/add-users.md).

5. On the **Optional settings** page, you can expand **Profile info** and fill in details, such as the user's job title, department, location, and so forth. Then choose **Next**.

6. On the **Review and finish** page, review the details, and then select **Finish adding** to add the user. If you need to make any changes, choose **Back** to go back to a previous page.

## Make sure MFA is enabled

One good way to make sure MFA is enabled for all users is by using [security defaults](/azure/active-directory/fundamentals/concept-fundamentals-security-defaults). If your tenant was created on or after October 22, 2019, security defaults might be enabled automatically in your tenant. Use the following procedure to confirm or enable security defaults.

> [!IMPORTANT]
> You must be a security administrator, Conditional Access administrator, or Global Administrator to perform this task.

1. Go to the Azure portal ([https://portal.azure.com/](https://portal.azure.com/)) and sign in.

2. Under **Manage Microsoft Entra ID**, select **View**.

   :::image type="content" source="media/mdb-manage-azuread.png" alt-text="Screenshot showing the View button under the heading Manage Microsoft Entra ID." lightbox="media/mdb-manage-azuread.png":::

3. In the navigation pane, select **Properties**, and then select **Manage security defaults**.

   :::image type="content" source="media/mdb-azuread-properties.png" alt-text="Screenshot showing Properties and Manage Security Defaults for Microsoft Entra ID." lightbox="media/mdb-azuread-properties.png":::

4. On the right side of the screen, in the **Security defaults** pane, see whether security defaults are turned on (**Enabled**) or off (**Disabled**). To turn security defaults on, use the drop-down menu to select **Enabled**. 

   > [!CAUTION]
   > If your organization is using Conditional Access policies, you won't be able to enable security defaults. You'll see a message that indicates you're using classic policies instead. You can use *either* security defaults *or* Conditional Access, but not both. For most organizations, security defaults offer a good level of sign-in security. But if your organization must meet more stringent requirements, you can use Conditional Access policies instead. To learn more, see the following articles:
   > - [Multi-factor authentication](../../business-premium/m365bp-turn-on-mfa.md) (in the Microsoft 365 Business Premium documentation)
   > - [Security defaults in Microsoft Entra ID](/azure/active-directory/fundamentals/concept-fundamentals-security-defaults)

5. Save your changes.

## Next steps

- [Step 3: Assign security roles and permissions in Microsoft Defender for Business](mdb-roles-permissions.md).
- [Step 4: Set up email notifications for your security team](mdb-email-notifications.md).

