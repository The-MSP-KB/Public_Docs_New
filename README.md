# Page

Rewst User Setup and GDAP Relationship Guidance

Step by Step

### Introduction <a href="#introduction" id="introduction"></a>

This guide specifically goes over the following:

* Creating the Rewst service account user.
* Creating the Rewst groups that GDAP permissions will be assigned to.
* Adding the Rewst user to the AdminAgents group.
* Creating a new admin relationship with the roles specifically required by Rewst. (Depending on your current GDAP relationship setup(s) this may not be necessary as long as your relationship contains the right roles and groups are available with the necessary permissions for the user)

Other applications/your technicians might need additional roles added to the relationship. Adding new roles after the relationship has been created requires recreating the relationship.

* Adding the Rewst group to the admin relationship.
* Adding the roles for the Rewst group in the admin relationship.

Below are the manual steps for completing this task

### Azure Active Directory (In Partner Tenant) <a href="#azure-active-directory-in-partner-tenant" id="azure-active-directory-in-partner-tenant"></a>

1. 1.**Login** to [Microsoft Entra ID](https://portal.azure.com/#view/Microsoft\_AAD\_IAM/ActiveDirectoryMenuBlade/\~/Overview).
2. 2.**Navigate** to _Users_.

![](https://3676225685-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FAQQ1EHVcEsGKBPVHmiav%2Fuploads%2FvZq7BE4FblhvIB0OM8oB%2Fimage%20\(7\).png?alt=media\&token=b4d021e3-7aee-426a-8eea-cbcec80e8b68)

1. 3.**Click** _New User_ → _Create User_.

![](https://3676225685-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FAQQ1EHVcEsGKBPVHmiav%2Fuploads%2F8ZdK6w1rFxK78dWA6tGO%2Fimage%20\(8\).png?alt=media\&token=54bb1116-bac5-4002-b8f9-1e736382ab5b)

1. 4.**Provide** the user principal name.
   * example: rewst
2. 5.**Provide** a display name.
   * example: Rewst Integration
3. 6.**Provide** a password.
   * document this for later usage
4. 7.**Click** _Next: Properties._

![](https://3676225685-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FAQQ1EHVcEsGKBPVHmiav%2Fuploads%2FpcNy7zZyA7JNhnEpyq9j%2Fimage%20\(8\).png?alt=media\&token=f390d640-1368-4a6a-a1ec-33057176d175)

1. 8.**Click** _Next: Assignments._
2. 9.**Click** _Add Role_ while under the assignments tab.
3. 10.**Search** for _Global Administrator_ in the role selection.
4. 11.**Select** the _Global Administrator role_.

Note: This role is required for installing the Enterprise Applications used when Rewst first authorizes.

1. 12.**Click** _Select._

![](https://3676225685-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FAQQ1EHVcEsGKBPVHmiav%2Fuploads%2FnrrBa4PzgQoLx0c9ibxc%2Fimage%20\(9\).png?alt=media\&token=022652a3-3624-4ee5-bb16-ffaa3365820d)

1. 13.**Verify** the role is now listed in the main pane.
2. 14.**Click** _Next: Review + Create_ If the role is there.
   * Verify the information is correct on the _Review + Create page_.
3. 15.**Click** _Create_.
4. 16.**Navigate** back to _Microsoft Entra ID._
5. 17.**Click** _Groups_.
6. For each of the groups in our recommend roles, create a new group. We recommend calling them "Rewst GDAP Role Name", for example "Rewst GDAP Application Administrator"

![](https://3676225685-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FAQQ1EHVcEsGKBPVHmiav%2Fuploads%2FEuv7SIw9D2hv9dL1yuJw%2Fimage%20\(8\).png?alt=media\&token=03d4912f-713a-4803-a79f-80154ea636e0)

![](https://3676225685-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FAQQ1EHVcEsGKBPVHmiav%2Fuploads%2FKlVyj0iMjp90KwGiNcFz%2Fimage%20\(9\).png?alt=media\&token=fe669854-5f5f-423e-90ce-ac61f7951574)

1. 19.**Select** _Security_ for Group type.
2. 20.**Enter** _Rewst – GDAP  Rolename_ for the group name.
3. 21.**Enter** _Rewst GDAP Permissions Group_ for the group description.
4. 22.**Set** _Microsoft Entra roles can be assigned to the group_ to _Yes._
5. 23.**Click** on _No members selected_.
6. 24.**Select** the Rewst account created in the previous steps in the new pane type in _Rewst_.
7. 25.**Click** _Select._

![](https://3676225685-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FAQQ1EHVcEsGKBPVHmiav%2Fuploads%2FjnfIJQsV5WpJ1gRjRmnO%2Fimage%20\(10\).png?alt=media\&token=6830541a-50fb-49e3-8d54-6623a1e27b28)

1. 26.**Select** _Yes_ when prompted with the following:
   * _"Creating a group to which Microsoft Entra roles can be assigned is a setting that cannot be changed later. Are you sure you want to add this capability?"_

It is also necessary to add the user to the ‘AdminAgents’ group on the group's page as well after the previous steps are done.

### Partner Center <a href="#partner-center" id="partner-center"></a>

1. 1.**Navigate** to the [Microsoft Partner Center](https://partner.microsoft.com/).
2. 2.**Click** on _Customers_ once on the Partner Center home page.

![](https://3676225685-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FAQQ1EHVcEsGKBPVHmiav%2Fuploads%2FaoBjsGAQgsDr2iZVOHCs%2Fimage%20\(11\).png?alt=media\&token=3bc373ce-f558-41a6-92a8-965530c6d557)

1. 3.**Click** on the name of the customer you would like to create the admin relationship for once the customer list loads.

![](https://3676225685-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FAQQ1EHVcEsGKBPVHmiav%2Fuploads%2F37tvZafcuaPeOLDAfgxl%2Fimage%20\(12\).png?alt=media\&token=f0b56753-c20c-46fe-8c24-d15dec60dc76)

1. 4.**Click** on _Admin Relationships_ in the left nav pane once in the customer page.

![](https://3676225685-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FAQQ1EHVcEsGKBPVHmiav%2Fuploads%2Fki6KfzncQnfYOAitfEhV%2Fimage%20\(14\).png?alt=media\&token=b9545a4e-1d18-4d7e-997e-d000683b0036)

1. 5.**Press** _Request for new admin relationship_ once on the relationship page.
2. 6.**Provide** a name for the admin relationship.

Note: This value must be unique per relationship/customer.

1. 7.**Provide** a duration.
   * max is 730 days
2. 8.**Click** _Select Microsoft Entra Roles_.

![](https://3676225685-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FAQQ1EHVcEsGKBPVHmiav%2Fuploads%2F0PI7KTk328GUaQ68F3x8%2Fimage%20\(15\).png?alt=media\&token=30cde685-d767-4c8c-b2a0-f08ec57c1164)

1. 9.**Select** the roles listed in [Recommended Roles for GDAP](https://docs.rewst.help/documentation/integrations/cloud/authorization-best-practices#recommended-roles-for-gdap).

Note: The list is not in alphabetical order and it is recommended that you use CTRL + F to search the page to make finding the roles easier.

1. 10.**Click** the _Save_ button once all roles are selected.
2. 11.**Click** _Finalize Request_ once you've verified all the roles you selected are listed.

![](https://3676225685-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FAQQ1EHVcEsGKBPVHmiav%2Fuploads%2FnnWtzDapoXE7GH2jXdyB%2Fimage%20\(16\).png?alt=media\&token=f9ce4ec5-7f53-47fd-9a7d-6ff55f297b6d)You will be redirected to a page that shows the request.At this point, your customer will need to accept the request or you will need to log in as a global administrator on the tenant to accept the request using the link in the _Click to review and accept_ section.

1. 12.**Click** _Done_.

Once the request has been approved the admin relationship will be established.

1. 13.**Verify** that the relationship is established by returning to the _Admin Relationships_ page and confirming the status is active.
2. 14.**Click** on the relationship name if the status is _Active._

![](https://3676225685-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FAQQ1EHVcEsGKBPVHmiav%2Fuploads%2FrnUR7TxxfHXXSjcW8JNj%2Fimage%20\(17\).png?alt=media\&token=32903c77-b9a3-4782-a68d-6e840d68275b)This will bring you to the page that shows all the available roles in the relationship and the list of available security groups.

1. 15.**Click** _Add security groups._

![](https://3676225685-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FAQQ1EHVcEsGKBPVHmiav%2Fuploads%2FH7PljPBb1PHtD0YCFbbk%2Fimage%20\(18\).png?alt=media\&token=f4848044-6619-45b5-b9a7-8728fde3ecbe)

1. 16.**For each of the groups create a mapping to the relationship. For example "Rewst GDAP Application Administrator" is matched to "Application Administrator"**

![](https://3676225685-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FAQQ1EHVcEsGKBPVHmiav%2Fuploads%2FId2mEYbho2R4Yi6JdUJ6%2FPicture15.png?alt=media\&token=c48ddca2-ddb7-49ad-b902-220b1ae6425a)

1. 17.Click _Next._
2. 18.**Select** the roles required for Rewst in the relationship as per [Recommended Roles for GDAP](https://docs.rewst.help/documentation/integrations/cloud/authorization-best-practices#recommended-roles-for-gdap).

![](https://3676225685-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FAQQ1EHVcEsGKBPVHmiav%2Fuploads%2Fgm23vqmV8VAXpFvdabXp%2FPicture16.png?alt=media\&token=7e6f3c06-ccf0-45b4-b3e4-726ff920da67)

1. 19.**Click** _Save_.
2. 20.**Wait** for the status to change to _Active_ (manual page refresh is needed).

![](https://3676225685-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FAQQ1EHVcEsGKBPVHmiav%2Fuploads%2FdTvMFh8AIqTv3FmrETgd%2Fimage%20\(20\).png?alt=media\&token=3bfee7df-f13e-422d-abff-7dc1b3b36870)These steps will need to be performed for each customer (creating the admin relationship/assigning the group to the relationship/assigning the roles to the group in the relationship)blah blah blah
