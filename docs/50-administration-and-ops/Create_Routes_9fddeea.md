<!-- loio9fddeea396b34b528bc8d286f3d5d9cf -->

# Create Routes

You can configure the URLs through which end users can reach your applications.



## Context

Routes belong to a space but they’re globally unique, regardless of the organization that controls a space. If a route with a URL exists, you can’t create a route with the same URL.

The following steps guide you through the procedure of creating routes by using the SAP BTP cockpit, but you can also create routes by using the CF CLI. For more information, see [https://cli.cloudfoundry.org/en-US/cf/create-route.html](https://cli.cloudfoundry.org/en-US/cf/create-route.html).



## Procedure

1.  Navigate to your Cloud Foundry space.

2.  Choose *Routes* from the left hand-side navigation.

3.  Choose *New Route* to create a route.

4.  In the dialog, enter the following parameters:


    <table>
    <tr>
    <th>

    Parameter


    
    </th>
    <th>

    Details


    
    </th>
    </tr>
    <tr>
    <td>

    ****Domain****


    
    </td>
    <td>

    From the dropdown menu, you can choose either a shared domain \(for example, the default `**cfapps.<region\>.hana.ondemand.com**`\) or a private domain that you've previously created using the CF CLI.

    From the dropdown menu, you can choose either a shared domain or a private domain that you've previously created using the CF CLI.

    For more information on private domains, see [https://docs.cloudfoundry.org/devguide/deploy-apps/routes-domains.html\#private-domains](https://docs.cloudfoundry.org/devguide/deploy-apps/routes-domains.html#private-domains).


    
    </td>
    </tr>
    <tr>
    <td>

    ****Host Name** **


    
    </td>
    <td>

    The host name is your desired subdomain. In the URL, it’s added before the selected domain, as follows:

    `https://**<host name\>**.<domain>`

    The host name can include no more than 63 characters.


    
    </td>
    </tr>
    <tr>
    <td>

    ****Path****


    
    </td>
    <td>

    In addition to the domain and subdomain, you can also add a path. You can use paths if you want to create routes for multiple applications available for the same host name and domain. The path becomes part of the URL as follows:

    `https://<host name>.<domain>**/<path\>**`


    
    </td>
    </tr>
    </table>
    
    You can see the preview of your route at the bottom of the dialog.

5.  When you're happy with your route, choose *Save*.




<a name="loio9fddeea396b34b528bc8d286f3d5d9cf__postreq_ckl_gbq_43b"/>

## Next Steps

Once you’ve created a route, you must map it to your application. Additionally, you also have the option to bind it to a route service instance, by choosing     \(Bind Route Service\) from the *Actions* column.

**Related Information**  


[Map Routes to Applications Using the Cockpit](Map_Routes_to_Applications_Using_the_Cockpit_b25cf8a.md "Once a route has been created, you can map it to an application to make this application reachable for end users.")

[Create Space Quota Plans](Create_Space_Quota_Plans_b13c4a2.md "You can use the cockpit to create space quota plans.")
