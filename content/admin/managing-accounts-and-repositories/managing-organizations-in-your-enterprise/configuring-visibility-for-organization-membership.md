---
title: Configuring visibility for organization membership
intro: You can set visibility for new organization members across your enterprise to public or private. You can also prevent members from changing their visibility from the default.
redirect_from:
  - /enterprise/admin/user-management/configuring-visibility-for-organization-membership
  - /admin/user-management/configuring-visibility-for-organization-membership
  - /admin/user-management/managing-organizations-in-your-enterprise/configuring-visibility-for-organization-membership
versions:
  ghes: '*'
type: how_to
topics:
  - Enterprise
  - Organizations
  - User account
shortTitle: Set membership visibility
---
You can also enforce your default setting on all current organization members in your instance using a command-line utility. For example, if you'd like to require every organization member's visibility to be public, you can set the default to public and enforce the default for all new members in the admin settings, and then use the command-line utility to enforce the public setting on existing members.

{% data reusables.enterprise-accounts.access-enterprise %}
{% data reusables.enterprise-accounts.policies-tab %}
{% data reusables.enterprise-accounts.options-tab %}
1. Under "Default organization membership visibility", select the drop-down menu, and click **Private** or **Public**.
1. Optionally, to prevent members from changing their membership visibility from the default, select **Enforce for all enterprise members**.
   ![Screenshot of the "Default organization membership visibility" section. The "Enforce for all enterprise members" checkbox is outlined.](/assets/images/enterprise/site-admin-settings/enforce-default-org-membership-visibility-setting.png)
1. If you'd like to enforce your new visibility setting on all existing members, use the `ghe-org-membership-update` command-line utility. For more information, see [AUTOTITLE](/admin/configuration/configuring-your-enterprise/command-line-utilities#ghe-org-membership-update).
