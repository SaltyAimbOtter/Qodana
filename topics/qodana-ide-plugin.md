[//]: # (title: IDE integration)

Starting from version 2022.3, you can use %product% functionality in JetBrains IDEs for binding Qodana 
reports, both stored locally or in Qodana Cloud, with your project opened in an IDE. This means that you can:

* Study [Qodana reports](#Open+report+from+Qodana+UI) including reports [stored locally](#Open+report+from+a+local+storage) 
* Link your projects with [Qodana Cloud](#Link+project+with+Qodana+Cloud) and overview Qodana Cloud-based reports

<note>Prior to 2022.3, this functionality was available as a plugin published 
on <a href="https://plugins.jetbrains.com/plugin/16938-qodana">JetBrains Marketplace</a>.</note>

This functionality is supported by IntelliJ IDEA, PhpStorm, WebStorm, Rider, GoLand, PyCharm, and Rider.

## Before you start

1. Make sure that your preferred IDE is installed via [JetBrains Toolbox App](https://www.jetbrains.com/toolbox-app/).
2. To open Qodana reports from your local storage, make sure that you previously opened the project by the IDE at least 
   one time. This action establishes the link between the %product% report and your IDE.

## UI overview

%product% is available in the **Qodana** tab of the **Problems** window of your IDE. This window is 
located in the lower-left part of the IDE user interface, and becomes visible once you open a report. 

After opening, the **Qodana** tab shows the list of problems that were detected by Qodana.

<img src="ide-plugin-tab-overview-1.png" dark-src="ide-plugin-tab-overview-1_dark.png" width="706" alt="Overview of the Qodana tab" border-effect="line"/>

If you click an item in this list, you can navigate to the highlighted code fragments that contain a problem.

<img src="ide-plugin-code-highlighting.png" dark-src="ide-plugin-code-highlighting_dark.png" width="706" alt="Code highlighting from the Qodana IDE plugin" animated="true" border-effect="line"/>

<anchor name="tab-overview-buttons"/>

In the upper-left corner of this tab, you can find the buttons listed in this table:

<!-- This needs to be rewritten -->

<table>
   <tr>
      <td>Button</td>
      <td>Description</td>
   </tr>
   <tr>
      <td><menupath>Log in to Qodana</menupath></td>
      <td>Logging in to Qodana Cloud. This action is a prerequisite for linking your project with Qodana Cloud-based reports. Alternatively, you can do it using the
<menupath>Tools | Qodana | Log in to Qodana</menupath> menu of your IDE as <a anchor="Log+in+to+Qodana+Cloud">described here</a>.</td>
   </tr>
   <tr>
      <td><menupath>Link project with Cloud</menupath></td>
      <td>link your project with a specific report uploaded to Qodana Cloud. After linking, you can study the report using your IDE.Alternatively, 
you can link your project using the <menupath>Tools | Qodana | Link Project with Cloud</menupath> menu of your IDE as <a anchor="Link+project+with+Qodana+Cloud">described here</a>.</td>
   </tr>
</table>

<img src="ide-plugin-tab-overview-2.png" dark-src="ide-plugin-tab-overview-2_dark.png" width="706" alt="The Qodana tab buttons" border-effect="line"/>

## Open report from Qodana UI

In a Qodana HTML report, choose a problem and click **Open file in \<IDE\>**.

<img src="qd-report-open-in-ide.png" dark-src="qd-report-open-in-ide_dark.png" alt="The Open in IDE button" width="706" border-effect="line"/>

<anchor name="open-report-in-ide"/>

## Open report from Qodana Cloud

Using your IDE, you can:

* [Log in to Qodana Cloud](#Log+in+to+Qodana+Cloud)
* [Link your project with Qodana Cloud](#Link+project+with+Qodana+Cloud)
* [Update the linked reports](#Update+report)

### Log in to Qodana Cloud

Logging in to Qodana Cloud is required before linking your project with reports from Qodana Cloud.

<procedure>
<step>
In your IDE, navigate to <menupath>Tools | Qodana | Log in to Qodana</menupath>. 

<img src="ide-plugin-login-1.png" dark-src="ide-plugin-login-1_dark.png" width="594" alt="Logging into Qodana Cloud" border-effect="line"/>

Alternatively, you can click the **Log in to Qodana** button of the **[Qodana](#tab-overview-buttons)** tab.

</step>
<step>
On the <menupath>Settings | Tools | Qodana </menupath> window, click <menupath>Log in</menupath>. This will redirect you 
to the authentication page.

<img src="ide-plugin-login-2.png" dark-src="ide-plugin-login-2_dark.png" width="594" alt="The log in button" border-effect="line"/>

</step>
<step>On the authentication page, complete the <a href="cloud-get-access.xml">authentication step</a>.</step>
</procedure>

### Link project with Qodana Cloud

You can synchronize your local project with reports uploaded to Qodana Cloud and related to a specific 
<a href="cloud-projects.xml">project</a>. This lets you overview the detected problems using the 
<menupath>Problems</menupath> tool window of your IDE. To link a project, you first need to 
[log in to Qodana Cloud](#Log+in+to+Qodana+Cloud).

<tip>For successful linking, you should have your local project already inspected by Qodana at least once with the report 
uploaded to Qodana Cloud.</tip>

<procedure>
<step>In your IDE, navigate to <menupath>Tools | Qodana </menupath>, and then click 
<menupath>Link Project with Cloud</menupath>. 

<img src="ide-plugin-linking-1.png" dark-src="ide-plugin-linking-1_dark.png" width="594" alt="Linking the project with Qodana Cloud" border-effect="line"/>

Alternatively, you can click the **Link project with Cloud** button of the **[Qodana](#tab-overview-buttons)** tab.

</step>
<step>
On the <menupath>Link Project with Qodana Cloud</menupath> window, select the Qodana Cloud project you would like to
link your local project with, and then click <menupath>Apply</menupath>.

<img src="ide-plugin-linking-2.png" dark-src="ide-plugin-linking-2_dark.png" width="594" alt="The link project with Qodana Cloud window" border-effect="line"/>

</step>

</procedure>

After linking, you can overview the report using the <menupath>Qodana</menupath> tab of the <menupath>Problems</menupath>
window, see the [UI overview](#UI+overview) section.

### Update report

To update the report, you should first have it [linked](#Link+project+with+Qodana+Cloud) with Qodana Cloud. 

In your IDE, navigate to <menupath>Tools | Qodana</menupath>, uncheck
**Cloud Project &lt;project-name&gt;**, and then check it back.

<img src="ide-plugin-update-report-1.png" dark-src="ide-plugin-update-report-1_dark.png" width="706" alt="Updating the report using the Tools menu" border-effect="line"/>

Alternatively, in the <menupath>Qodana</menupath> tab of the <menupath>Problems</menupath> window, you can uncheck 
<menupath>Cloud Project &lt;project-name&gt;</menupath>, and then check it back.

<img src="ide-plugin-update-report-2.png" dark-src="ide-plugin-update-report-2_dark.png" width="706" alt="Updating the report using the Qodana tab" border-effect="line"/>

## Open report from a local storage

In the IDE, go to <menupath>Tools | Qodana | Open Qodana Analysis report</menupath> and select the
<code>qodana.sarif.json</code> report file you would like to open.

<img src="ide-plugin-local-file-1.png" dark-src="ide-plugin-local-file-1_dark.png" width="706" alt="Opening a local Qodana report" border-effect="line"/>

In the <menupath>Qodana</menupath> tab, you can [overview the detected problems](#UI+overview) and jump to the corresponding line in
the code editor. In case a problem was fixed before opening the <code>qodana.sarif.json</code> file, it is marked as
<code>[Not present]</code>.