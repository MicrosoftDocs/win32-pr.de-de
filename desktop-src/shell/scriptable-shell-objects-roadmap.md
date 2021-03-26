---
description: Die Windows-Shell bietet einen leistungsstarken Satz von Automatisierungs Objekten, mit denen Sie die Shell mit Microsoft-Visual Basic und Skriptsprachen wie Microsoft JScript (kompatibel mit der ECMA 262-Sprachspezifikation) und Microsoft Visual Basic Scripting Edition (VBScript) programmieren können. Sie können diese Objekte verwenden, um auf viele der Funktionen und Dialogfelder der Shell zuzugreifen. Beispielsweise können Sie auf das Dateisystem zugreifen, Programme starten und Systemeinstellungen ändern.
title: Scriptable-Shellobjekte
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 09455fad-a769-42ef-83ba-b745ac819bf3
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4c39e7e58a9715598056fb74aa154ed8a850f523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980465"
---
# <a name="scriptable-shell-objects"></a><span data-ttu-id="f026c-105">Scriptable-Shellobjekte</span><span class="sxs-lookup"><span data-stu-id="f026c-105">Scriptable Shell Objects</span></span>

<span data-ttu-id="f026c-106">Die Windows-Shell bietet einen leistungsstarken Satz von Automatisierungs Objekten, mit denen Sie die Shell mit Microsoft-Visual Basic und Skriptsprachen wie Microsoft JScript (kompatibel mit der ECMA 262-Sprachspezifikation) und Microsoft Visual Basic Scripting Edition (VBScript) programmieren können.</span><span class="sxs-lookup"><span data-stu-id="f026c-106">The Windows Shell provides a powerful set of automation objects that enable you to program the Shell with Microsoft Visual Basic and scripting languages such as Microsoft JScript (compatible with ECMA 262 language specification) and Microsoft Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="f026c-107">Sie können diese Objekte verwenden, um auf viele der Funktionen und Dialogfelder der Shell zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="f026c-107">You can use these objects to access many of the Shell's features and dialog boxes.</span></span> <span data-ttu-id="f026c-108">Beispielsweise können Sie auf das Dateisystem zugreifen, Programme starten und Systemeinstellungen ändern.</span><span class="sxs-lookup"><span data-stu-id="f026c-108">For example, you can access the file system, launch programs, and change system settings.</span></span>

<span data-ttu-id="f026c-109">In diesem Abschnitt werden die Skript fähigen Shellobjekte vorgestellt.</span><span class="sxs-lookup"><span data-stu-id="f026c-109">This section introduces the scriptable Shell objects.</span></span>

-   [<span data-ttu-id="f026c-110">Shell-Versionen</span><span class="sxs-lookup"><span data-stu-id="f026c-110">Shell Versions</span></span>](#shell-versions)
-   [<span data-ttu-id="f026c-111">Instanziieren von shellobjekten</span><span class="sxs-lookup"><span data-stu-id="f026c-111">Instantiating Shell Objects</span></span>](#instantiating-shell-objects)
    -   [<span data-ttu-id="f026c-112">Späte Bindung</span><span class="sxs-lookup"><span data-stu-id="f026c-112">Late Binding</span></span>](#late-binding)
    -   [<span data-ttu-id="f026c-113">HTML-Objekt Element</span><span class="sxs-lookup"><span data-stu-id="f026c-113">HTML OBJECT Element</span></span>](#html-object-element)
-   [<span data-ttu-id="f026c-114">Shellobjekt</span><span class="sxs-lookup"><span data-stu-id="f026c-114">Shell Object</span></span>](#shell-object)
    -   [<span data-ttu-id="f026c-115">Security</span><span class="sxs-lookup"><span data-stu-id="f026c-115">Security</span></span>](#security)
-   [<span data-ttu-id="f026c-116">Ordner Objekte</span><span class="sxs-lookup"><span data-stu-id="f026c-116">Folder Objects</span></span>](#folder-objects)

## <a name="shell-versions"></a><span data-ttu-id="f026c-117">Shell-Versionen</span><span class="sxs-lookup"><span data-stu-id="f026c-117">Shell Versions</span></span>

<span data-ttu-id="f026c-118">Viele der Shellobjekte wurden in [Version 4,71](versions.md) der Shell verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f026c-118">Many of the Shell objects became available in [version 4.71](versions.md) of the Shell.</span></span> <span data-ttu-id="f026c-119">Andere sind in Version 5,00 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f026c-119">Others are available in version 5.00 and later.</span></span> <span data-ttu-id="f026c-120">Version 5,00 wurde mit Windows 2000 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f026c-120">Version 5.00 became available with Windows 2000.</span></span> <span data-ttu-id="f026c-121">In der folgenden Tabelle werden die einzelnen Shellobjekte unter der-Version der Shell aufgelistet, in der das Objekt verfügbar wurde.</span><span class="sxs-lookup"><span data-stu-id="f026c-121">The following table lists each Shell object under the version of the Shell in which the object became available.</span></span>



| <span data-ttu-id="f026c-122">Version 4,71</span><span class="sxs-lookup"><span data-stu-id="f026c-122">Version 4.71</span></span>                                            | <span data-ttu-id="f026c-123">Version 5,00</span><span class="sxs-lookup"><span data-stu-id="f026c-123">Version 5.00</span></span>                                          |
|---------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="f026c-124">**Ordner**</span><span class="sxs-lookup"><span data-stu-id="f026c-124">**Folder**</span></span>](folder.md)                                | [<span data-ttu-id="f026c-125">**Didiskquotauser**</span><span class="sxs-lookup"><span data-stu-id="f026c-125">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)     |
| [<span data-ttu-id="f026c-126">**Folderitemverb**</span><span class="sxs-lookup"><span data-stu-id="f026c-126">**FolderItemVerb**</span></span>](folderitemverb.md)                | [<span data-ttu-id="f026c-127">**Diskquotacontrol**</span><span class="sxs-lookup"><span data-stu-id="f026c-127">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)   |
| [<span data-ttu-id="f026c-128">**Folderitemverbs**</span><span class="sxs-lookup"><span data-stu-id="f026c-128">**FolderItemVerbs**</span></span>](folderitemverbs.md)              | [<span data-ttu-id="f026c-129">**Folder2**</span><span class="sxs-lookup"><span data-stu-id="f026c-129">**Folder2**</span></span>](folder2-object.md)                     |
| [<span data-ttu-id="f026c-130">**Shell**</span><span class="sxs-lookup"><span data-stu-id="f026c-130">**Shell**</span></span>](shell.md)                                  | [<span data-ttu-id="f026c-131">**Von folderItem**</span><span class="sxs-lookup"><span data-stu-id="f026c-131">**FolderItem**</span></span>](folderitem.md)                      |
| [<span data-ttu-id="f026c-132">**Shellfolderview**</span><span class="sxs-lookup"><span data-stu-id="f026c-132">**ShellFolderView**</span></span>](shellfolderview.md)              | [<span data-ttu-id="f026c-133">**Folderitems**</span><span class="sxs-lookup"><span data-stu-id="f026c-133">**FolderItems**</span></span>](folderitems.md)                    |
| [<span data-ttu-id="f026c-134">**Shelluihelper**</span><span class="sxs-lookup"><span data-stu-id="f026c-134">**ShellUIHelper**</span></span>](shelluihelper.md)                  | [<span data-ttu-id="f026c-135">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="f026c-135">**FolderItems2**</span></span>](folderitems2-object.md)           |
| [<span data-ttu-id="f026c-136">**Shellwindows**</span><span class="sxs-lookup"><span data-stu-id="f026c-136">**ShellWindows**</span></span>](shellwindows.md)                    | [<span data-ttu-id="f026c-137">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="f026c-137">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)     |
| [<span data-ttu-id="f026c-138">**Webviewfoldercontents**</span><span class="sxs-lookup"><span data-stu-id="f026c-138">**WebViewFolderContents**</span></span>](../lwef/webviewfoldercontents.md) | [<span data-ttu-id="f026c-139">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="f026c-139">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)     |
|                                                         | [<span data-ttu-id="f026c-140">**Shellfolderitem**</span><span class="sxs-lookup"><span data-stu-id="f026c-140">**ShellFolderItem**</span></span>](shellfolderitem-object.md)     |
|                                                         | [<span data-ttu-id="f026c-141">**Shellfolderviewoc**</span><span class="sxs-lookup"><span data-stu-id="f026c-141">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md) |
|                                                         | [<span data-ttu-id="f026c-142">**Shelllinkobject**</span><span class="sxs-lookup"><span data-stu-id="f026c-142">**ShellLinkObject**</span></span>](shelllinkobject-object.md)     |



 

## <a name="instantiating-shell-objects"></a><span data-ttu-id="f026c-143">Instanziieren von shellobjekten</span><span class="sxs-lookup"><span data-stu-id="f026c-143">Instantiating Shell Objects</span></span>

<span data-ttu-id="f026c-144">Fügen Sie Verweise auf die folgenden Bibliotheken in Ihrem Projekt hinzu, um die Shellobjekte in Visual Basic Anwendungen mit einer frühen Bindung zu instanziieren:</span><span class="sxs-lookup"><span data-stu-id="f026c-144">To instantiate the Shell objects in Visual Basic applications with early binding, add references to the following libraries in your project:</span></span>

-   <span data-ttu-id="f026c-145">Microsoft Internet Controls (shdocvw)</span><span class="sxs-lookup"><span data-stu-id="f026c-145">Microsoft Internet Controls (SHDocVw)</span></span>
-   <span data-ttu-id="f026c-146">Microsoft Shell-Steuerelemente und Automatisierung (shell32)</span><span class="sxs-lookup"><span data-stu-id="f026c-146">Microsoft Shell Controls and Automation (Shell32)</span></span>

### <a name="late-binding"></a><span data-ttu-id="f026c-147">Späte Bindung</span><span class="sxs-lookup"><span data-stu-id="f026c-147">Late Binding</span></span>

<span data-ttu-id="f026c-148">Sie können auch viele der Shellobjekte mit späterer Bindung instanziieren.</span><span class="sxs-lookup"><span data-stu-id="f026c-148">You can also instantiate many of the Shell objects with late binding.</span></span> <span data-ttu-id="f026c-149">Diese Vorgehensweise funktioniert in Visual Basic Anwendungen und in Skripts.</span><span class="sxs-lookup"><span data-stu-id="f026c-149">This approach works in Visual Basic applications and in script.</span></span> <span data-ttu-id="f026c-150">Im folgenden Beispiel wird gezeigt, wie das [**Shellobjekt**](shell.md) in JScript instanziiert wird.</span><span class="sxs-lookup"><span data-stu-id="f026c-150">The following example shows how to instantiate the [**Shell**](shell.md) object in JScript.</span></span>


```
<SCRIPT LANGUAGE="JScript">
<!--
    function fnCreateShell()    
    {
        // Instantiate the Shell object and invoke its FileRun method.
        var oShell = new ActiveXObject("shell.application");
        oshell.FileRun;
    }
-->
</SCRIPT>
```



<span data-ttu-id="f026c-151">Im folgenden Beispiel wird gezeigt, wie das [**Folder**](folder.md) -Objekt in VBScript instanziiert wird.</span><span class="sxs-lookup"><span data-stu-id="f026c-151">The following example shows how to instantiate the [**Folder**](folder.md) object in VBScript.</span></span>


```
<SCRIPT LANGUAGE="VBScript">
<!--
    function fnCreateFolder()
        dim oShell    
        dim oFolder
        dim sDir

        sDir = "C:\SomePath" 
        set oShell = CreateObject("shell.application")
        set oFolder = oShell.NameSpace(sDir)  
    end function
-->  
</SCRIPT>
```



<span data-ttu-id="f026c-152">Im vorherigen Beispiel ist *sDir* der Pfad zum [**Ordner**](folder.md) Objekt.</span><span class="sxs-lookup"><span data-stu-id="f026c-152">In the preceding example, *sDir* is the path to the [**Folder**](folder.md) object.</span></span> <span data-ttu-id="f026c-153">Beachten Sie, dass die [**shellspecialfolderconstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) -Enumerationswerte im Skript nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="f026c-153">Note that the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) enumeration values are not available in script.</span></span>

<span data-ttu-id="f026c-154">Die ProgID für die einzelnen Shellobjekte ist in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="f026c-154">The ProgID for each of the Shell objects is shown in the following table.</span></span>



| <span data-ttu-id="f026c-155">Object</span><span class="sxs-lookup"><span data-stu-id="f026c-155">Object</span></span>                                                  | <span data-ttu-id="f026c-156">ProgID</span><span class="sxs-lookup"><span data-stu-id="f026c-156">ProgID</span></span>                                                                                  |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="f026c-157">**Didiskquotauser**</span><span class="sxs-lookup"><span data-stu-id="f026c-157">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)       | <span data-ttu-id="f026c-158">Microsoft. Diskquota. 1</span><span class="sxs-lookup"><span data-stu-id="f026c-158">Microsoft.DiskQuota.1</span></span>                                                                   |
| [<span data-ttu-id="f026c-159">**Diskquotacontrol**</span><span class="sxs-lookup"><span data-stu-id="f026c-159">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)     | <span data-ttu-id="f026c-160">Die Bindung kann nicht spät</span><span class="sxs-lookup"><span data-stu-id="f026c-160">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="f026c-161">**Ordner**</span><span class="sxs-lookup"><span data-stu-id="f026c-161">**Folder**</span></span>](folder.md)                                | <span data-ttu-id="f026c-162">schel. Shell \_ Application. Namespace ("...")</span><span class="sxs-lookup"><span data-stu-id="f026c-162">shell.Shell\_Application.NameSpace("...")</span></span>                                               |
| [<span data-ttu-id="f026c-163">**Folder2**</span><span class="sxs-lookup"><span data-stu-id="f026c-163">**Folder2**</span></span>](folder2-object.md)                       | <span data-ttu-id="f026c-164">schel. Shell \_ Application. Namespace ("...")</span><span class="sxs-lookup"><span data-stu-id="f026c-164">shell.Shell\_Application.NameSpace("...")</span></span>                                               |
| [<span data-ttu-id="f026c-165">**Von folderItem**</span><span class="sxs-lookup"><span data-stu-id="f026c-165">**FolderItem**</span></span>](folderitem.md)                        | <span data-ttu-id="f026c-166">schel. Shell \_ Application. Namespace ("..."). Self oder Folder. Items. Item oder Folder. Parser Name</span><span class="sxs-lookup"><span data-stu-id="f026c-166">shell.Shell\_Application.NameSpace("...").Self or Folder.Items.Item or Folder.ParseName</span></span> |
| [<span data-ttu-id="f026c-167">**Folderitems**</span><span class="sxs-lookup"><span data-stu-id="f026c-167">**FolderItems**</span></span>](folderitems.md)                      | <span data-ttu-id="f026c-168">Ordner. Items</span><span class="sxs-lookup"><span data-stu-id="f026c-168">Folder.Items</span></span>                                                                            |
| [<span data-ttu-id="f026c-169">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="f026c-169">**FolderItems2**</span></span>](folderitems2-object.md)             | <span data-ttu-id="f026c-170">Ordner. Items</span><span class="sxs-lookup"><span data-stu-id="f026c-170">Folder.Items</span></span>                                                                            |
| [<span data-ttu-id="f026c-171">**Folderitemverb**</span><span class="sxs-lookup"><span data-stu-id="f026c-171">**FolderItemVerb**</span></span>](folderitemverb.md)                | <span data-ttu-id="f026c-172">Shell. Namespace ("..."). Self. Verbs. Item ()</span><span class="sxs-lookup"><span data-stu-id="f026c-172">Shell.NameSpace("...").Self.Verbs.Item()</span></span>                                                |
| [<span data-ttu-id="f026c-173">**Folderitemverbs**</span><span class="sxs-lookup"><span data-stu-id="f026c-173">**FolderItemVerbs**</span></span>](folderitemverbs.md)              | <span data-ttu-id="f026c-174">FolderItem. Verbs oder Shell. Namespace ("..."). Selbst. Verben</span><span class="sxs-lookup"><span data-stu-id="f026c-174">FolderItem.Verbs or Shell.NameSpace("...").Self.Verbs</span></span>                                   |
| [<span data-ttu-id="f026c-175">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="f026c-175">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)       | <span data-ttu-id="f026c-176">schel. \_Shellanwendung</span><span class="sxs-lookup"><span data-stu-id="f026c-176">shell.Shell\_Application</span></span>                                                                |
| [<span data-ttu-id="f026c-177">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="f026c-177">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)       | <span data-ttu-id="f026c-178">Shell. Namespace ("..."). Self. getlink oder Shell. Namespace ("..."). Elemente (). Getlink</span><span class="sxs-lookup"><span data-stu-id="f026c-178">Shell.NameSpace("...").Self.GetLink or Shell.NameSpace("...").Items().GetLink</span></span>           |
| [<span data-ttu-id="f026c-179">**Shell**</span><span class="sxs-lookup"><span data-stu-id="f026c-179">**Shell**</span></span>](shell.md)                                  | <span data-ttu-id="f026c-180">schel. \_Shellanwendung</span><span class="sxs-lookup"><span data-stu-id="f026c-180">shell.Shell\_Application</span></span>                                                                |
| [<span data-ttu-id="f026c-181">**Shellfolderitem**</span><span class="sxs-lookup"><span data-stu-id="f026c-181">**ShellFolderItem**</span></span>](shellfolderitem-object.md)       | <span data-ttu-id="f026c-182">Shell. Namespace ("..."). Self oder Shell. Namespace ("..."). Elemente ()</span><span class="sxs-lookup"><span data-stu-id="f026c-182">Shell.NameSpace("...").Self or Shell.NameSpace("...").Items()</span></span>                           |
| [<span data-ttu-id="f026c-183">**Shellfolderview**</span><span class="sxs-lookup"><span data-stu-id="f026c-183">**ShellFolderView**</span></span>](shellfolderview.md)              | <span data-ttu-id="f026c-184">Die Bindung kann nicht spät</span><span class="sxs-lookup"><span data-stu-id="f026c-184">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="f026c-185">**Shellfolderviewoc**</span><span class="sxs-lookup"><span data-stu-id="f026c-185">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)   | <span data-ttu-id="f026c-186">Die Bindung kann nicht spät</span><span class="sxs-lookup"><span data-stu-id="f026c-186">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="f026c-187">**Shelllinkobject**</span><span class="sxs-lookup"><span data-stu-id="f026c-187">**ShellLinkObject**</span></span>](shelllinkobject-object.md)       | <span data-ttu-id="f026c-188">Shell. Namespace ("..."). Self. getlink oder Shell. Namespace ("..."). Elemente (). Getlink</span><span class="sxs-lookup"><span data-stu-id="f026c-188">Shell.NameSpace("...").Self.GetLink or Shell.NameSpace("...").Items().GetLink</span></span>           |
| [<span data-ttu-id="f026c-189">**Shelluihelper**</span><span class="sxs-lookup"><span data-stu-id="f026c-189">**ShellUIHelper**</span></span>](shelluihelper.md)                  | <span data-ttu-id="f026c-190">Die Bindung kann nicht spät</span><span class="sxs-lookup"><span data-stu-id="f026c-190">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="f026c-191">**Shellwindows**</span><span class="sxs-lookup"><span data-stu-id="f026c-191">**ShellWindows**</span></span>](shellwindows.md)                    | <span data-ttu-id="f026c-192">schel. \_Shellfenster oder shellwindows. \_ "Netwenum"</span><span class="sxs-lookup"><span data-stu-id="f026c-192">shell.Shell\_Windows or ShellWindows.\_NewEnum</span></span>                                          |
| [<span data-ttu-id="f026c-193">**Webviewfoldercontents**</span><span class="sxs-lookup"><span data-stu-id="f026c-193">**WebViewFolderContents**</span></span>](../lwef/webviewfoldercontents.md) | <span data-ttu-id="f026c-194">Die Bindung kann nicht spät</span><span class="sxs-lookup"><span data-stu-id="f026c-194">Cannot late bind</span></span>                                                                        |



 

### <a name="html-object-element"></a><span data-ttu-id="f026c-195">HTML-Objekt Element</span><span class="sxs-lookup"><span data-stu-id="f026c-195">HTML OBJECT Element</span></span>

<span data-ttu-id="f026c-196">Sie können auch das [**Object**](https://msdn.microsoft.com/library/ms535859(v=VS.85).aspx) -Element verwenden, um Shellobjekte auf einer HTML-Seite zu instanziieren.</span><span class="sxs-lookup"><span data-stu-id="f026c-196">You can also use the [**OBJECT**](https://msdn.microsoft.com/library/ms535859(v=VS.85).aspx) element to instantiate Shell objects on an HTML page.</span></span> <span data-ttu-id="f026c-197">Legen Sie hierzu das **ID** -Attribut des **Object** -Elements auf den Variablennamen fest, den Sie in Ihren Skripts verwenden möchten, und identifizieren Sie das Objekt mit der registrierten Nummer (ClassID).</span><span class="sxs-lookup"><span data-stu-id="f026c-197">To do this, set the **OBJECT** element's **ID** attribute to the variable name you will use in your scripts, and identify the object using its registered number (CLASSID).</span></span> <span data-ttu-id="f026c-198">Der folgende HTML-Code erstellt mit dem **Object** -Element eine Instanz des [**shellfolderitem**](shellfolderitem-object.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="f026c-198">The following HTML creates an instance of the [**ShellFolderItem**](shellfolderitem-object.md) object using the **OBJECT** element.</span></span>


```
<OBJECT ID="oShFolderItem" 
    NAME="Shell Folder Item Object"
    CLASSID="clsid:2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e">
</OBJECT>
```



<span data-ttu-id="f026c-199">In der folgenden Tabelle werden die einzelnen Shellobjekte und die jeweilige ClassID aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f026c-199">The following table lists each Shell object and its respective CLASSID.</span></span>



|                                                         |                                      |
|---------------------------------------------------------|--------------------------------------|
| [<span data-ttu-id="f026c-200">**Didiskquotauser**</span><span class="sxs-lookup"><span data-stu-id="f026c-200">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)       | <span data-ttu-id="f026c-201">7988b571-ec89-11CF-9c00-00aa00a14f56</span><span class="sxs-lookup"><span data-stu-id="f026c-201">7988B571-EC89-11cf-9C00-00AA00A14F56</span></span> |
| [<span data-ttu-id="f026c-202">**Diskquotacontrol**</span><span class="sxs-lookup"><span data-stu-id="f026c-202">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)     | <span data-ttu-id="f026c-203">7988b571-ec89-11CF-9c00-00aa00a14f56</span><span class="sxs-lookup"><span data-stu-id="f026c-203">7988B571-EC89-11cf-9C00-00AA00A14F56</span></span> |
| [<span data-ttu-id="f026c-204">**Ordner**</span><span class="sxs-lookup"><span data-stu-id="f026c-204">**Folder**</span></span>](folder.md)                                | <span data-ttu-id="f026c-205">BBCBDE60-C3FF-11CE-8350-444553540000</span><span class="sxs-lookup"><span data-stu-id="f026c-205">BBCBDE60-C3FF-11CE-8350-444553540000</span></span> |
| [<span data-ttu-id="f026c-206">**Folder2**</span><span class="sxs-lookup"><span data-stu-id="f026c-206">**Folder2**</span></span>](folder2-object.md)                       | <span data-ttu-id="f026c-207">f0d2d8ef-3890-11d2-bf8b-00c04fb93661</span><span class="sxs-lookup"><span data-stu-id="f026c-207">f0d2d8ef-3890-11d2-bf8b-00c04fb93661</span></span> |
| [<span data-ttu-id="f026c-208">**Von folderItem**</span><span class="sxs-lookup"><span data-stu-id="f026c-208">**FolderItem**</span></span>](folderitem.md)                        | <span data-ttu-id="f026c-209">744129e0-CBE5-11CE-8350-444553540000</span><span class="sxs-lookup"><span data-stu-id="f026c-209">744129E0-CBE5-11CE-8350-444553540000</span></span> |
| [<span data-ttu-id="f026c-210">**Folderitems**</span><span class="sxs-lookup"><span data-stu-id="f026c-210">**FolderItems**</span></span>](folderitems.md)                      | <span data-ttu-id="f026c-211">744129e0-CBE5-11CE-8350-444553540000</span><span class="sxs-lookup"><span data-stu-id="f026c-211">744129E0-CBE5-11CE-8350-444553540000</span></span> |
| [<span data-ttu-id="f026c-212">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="f026c-212">**FolderItems2**</span></span>](folderitems2-object.md)             | <span data-ttu-id="f026c-213">C94F0AD0-F363-11d2-A327-00C04F8EEC7F</span><span class="sxs-lookup"><span data-stu-id="f026c-213">C94F0AD0-F363-11d2-A327-00C04F8EEC7F</span></span> |
| [<span data-ttu-id="f026c-214">**Folderitemverb**</span><span class="sxs-lookup"><span data-stu-id="f026c-214">**FolderItemVerb**</span></span>](folderitemverb.md)                | <span data-ttu-id="f026c-215">08ec3e00-50b0-11CF-960c-0080c7f4ee85</span><span class="sxs-lookup"><span data-stu-id="f026c-215">08EC3E00-50B0-11CF-960C-0080C7F4EE85</span></span> |
| [<span data-ttu-id="f026c-216">**Folderitemverbs**</span><span class="sxs-lookup"><span data-stu-id="f026c-216">**FolderItemVerbs**</span></span>](folderitemverbs.md)              | <span data-ttu-id="f026c-217">1f8352c0-50b0-11CF-960c-0080c7f4ee85</span><span class="sxs-lookup"><span data-stu-id="f026c-217">1F8352C0-50B0-11CF-960C-0080C7F4EE85</span></span> |
| [<span data-ttu-id="f026c-218">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="f026c-218">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)       | <span data-ttu-id="f026c-219">A4C6892C-3BA9-11d2-9DEA-00C04FB16162</span><span class="sxs-lookup"><span data-stu-id="f026c-219">A4C6892C-3BA9-11d2-9DEA-00C04FB16162</span></span> |
| [<span data-ttu-id="f026c-220">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="f026c-220">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)       | <span data-ttu-id="f026c-221">317ee249-b12e-11d2-B1E4-00c04f 8eeb3e</span><span class="sxs-lookup"><span data-stu-id="f026c-221">317EE249-F12E-11d2-B1E4-00C04F8EEB3E</span></span> |
| [<span data-ttu-id="f026c-222">**Shell**</span><span class="sxs-lookup"><span data-stu-id="f026c-222">**Shell**</span></span>](shell.md)                                  | <span data-ttu-id="f026c-223">13709620-C279-11CE-A49E-444553540000</span><span class="sxs-lookup"><span data-stu-id="f026c-223">13709620-C279-11CE-A49E-444553540000</span></span> |
| [<span data-ttu-id="f026c-224">**Shellfolderitem**</span><span class="sxs-lookup"><span data-stu-id="f026c-224">**ShellFolderItem**</span></span>](shellfolderitem-object.md)       | <span data-ttu-id="f026c-225">2fe352ea-fid1fi-11d2-B1F 4-00c04fi8eeb3e</span><span class="sxs-lookup"><span data-stu-id="f026c-225">2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e</span></span> |
| [<span data-ttu-id="f026c-226">**Shellfolderview**</span><span class="sxs-lookup"><span data-stu-id="f026c-226">**ShellFolderView**</span></span>](shellfolderview.md)              | <span data-ttu-id="f026c-227">62112aa1-ebe4-11CF-a5fb-0020afe7292d</span><span class="sxs-lookup"><span data-stu-id="f026c-227">62112AA1-EBE4-11cf-A5FB-0020AFE7292D</span></span> |
| [<span data-ttu-id="f026c-228">**Shellfolderviewoc**</span><span class="sxs-lookup"><span data-stu-id="f026c-228">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)   | <span data-ttu-id="f026c-229">4a3df050-23bd-11d2-939f -00a0c91eedba</span><span class="sxs-lookup"><span data-stu-id="f026c-229">4a3df050-23bd-11d2-939f-00a0c91eedba</span></span> |
| [<span data-ttu-id="f026c-230">**Shelllinkobject**</span><span class="sxs-lookup"><span data-stu-id="f026c-230">**ShellLinkObject**</span></span>](shelllinkobject-object.md)       | <span data-ttu-id="f026c-231">11219420-1768-11d1-95be-00609797ea4f</span><span class="sxs-lookup"><span data-stu-id="f026c-231">11219420-1768-11d1-95BE-00609797EA4F</span></span> |
| [<span data-ttu-id="f026c-232">**Shelluihelper**</span><span class="sxs-lookup"><span data-stu-id="f026c-232">**ShellUIHelper**</span></span>](shelluihelper.md)                  | <span data-ttu-id="f026c-233">64ab4bb7-111E-11d1-8f79-00c04fc2fbe1</span><span class="sxs-lookup"><span data-stu-id="f026c-233">64AB4BB7-111E-11D1-8F79-00C04FC2FBE1</span></span> |
| [<span data-ttu-id="f026c-234">**Shellwindows**</span><span class="sxs-lookup"><span data-stu-id="f026c-234">**ShellWindows**</span></span>](shellwindows.md)                    | <span data-ttu-id="f026c-235">9ba05972-f6a8-11CF-A442-00a0c90a8f39</span><span class="sxs-lookup"><span data-stu-id="f026c-235">9BA05972-F6A8-11CF-A442-00A0C90A8F39</span></span> |
| [<span data-ttu-id="f026c-236">**Webviewfoldercontents**</span><span class="sxs-lookup"><span data-stu-id="f026c-236">**WebViewFolderContents**</span></span>](../lwef/webviewfoldercontents.md) | <span data-ttu-id="f026c-237">1820fed0-473e-11D0-a96c-00c04f d705a2</span><span class="sxs-lookup"><span data-stu-id="f026c-237">1820FED0-473E-11D0-A96C-00C04FD705A2</span></span> |



 

## <a name="shell-object"></a><span data-ttu-id="f026c-238">Shellobjekt</span><span class="sxs-lookup"><span data-stu-id="f026c-238">Shell Object</span></span>

<span data-ttu-id="f026c-239">Das [**Shellobjekt**](shell.md) stellt die Objekte in der Shell dar.</span><span class="sxs-lookup"><span data-stu-id="f026c-239">The [**Shell**](shell.md) object represents the objects in the Shell.</span></span> <span data-ttu-id="f026c-240">Sie können die Methoden, die vom Shell-Objekt verfügbar gemacht werden, für Folgendes verwenden:</span><span class="sxs-lookup"><span data-stu-id="f026c-240">You can use the methods exposed by the Shell object to:</span></span>

-   <span data-ttu-id="f026c-241">Öffnen, untersuchen und suchen Sie nach Ordnern.</span><span class="sxs-lookup"><span data-stu-id="f026c-241">Open, explore, and browse for folders.</span></span>
-   <span data-ttu-id="f026c-242">Minimieren, wiederherstellen, kaskadieren oder Kacheln öffnen.</span><span class="sxs-lookup"><span data-stu-id="f026c-242">Minimize, restore, cascade, or tile open windows.</span></span>
-   <span data-ttu-id="f026c-243">Starten Sie System Steuerungsanwendungen.</span><span class="sxs-lookup"><span data-stu-id="f026c-243">Launch Control Panel applications.</span></span>
-   <span data-ttu-id="f026c-244">Anzeigen von System Dialogfeldern.</span><span class="sxs-lookup"><span data-stu-id="f026c-244">Display system dialog boxes.</span></span>

<span data-ttu-id="f026c-245">Benutzer sind vielleicht am häufigsten mit den Befehlen vertraut, auf die Sie über das **Startmenü** und das Kontextmenü der Taskleiste zugreifen.</span><span class="sxs-lookup"><span data-stu-id="f026c-245">Users are perhaps most familiar with the commands they access from the **Start** menu and the taskbar's shortcut menu.</span></span> <span data-ttu-id="f026c-246">Das Kontextmenü der Taskleiste wird angezeigt, wenn Benutzer mit der rechten Maustaste auf die Taskleiste klicken.</span><span class="sxs-lookup"><span data-stu-id="f026c-246">The taskbar's shortcut menu appears when users right-click the taskbar.</span></span> <span data-ttu-id="f026c-247">Die folgende HTML-Anwendung (HTA) erzeugt eine Startseite mit Schaltflächen, mit denen viele der Methoden des [**shellobjekts**](shell.md) implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="f026c-247">The following HTML Application (HTA) produces a start page with buttons that implement many of the [**Shell**](shell.md) object's methods.</span></span> <span data-ttu-id="f026c-248">Einige dieser Methoden implementieren Features im **Startmenü** und im Kontextmenü der Taskleiste.</span><span class="sxs-lookup"><span data-stu-id="f026c-248">Some of these methods implement features on the **Start** menu and the taskbar's shortcut menu.</span></span>


```
<HTML>
<HEAD>
    <TITLE>Start Page</TITLE>
    
    <OBJECT ID="oShell"
        CLASSID="clsid:13709620-C279-11CE-A49E-444553540000">
    </OBJECT>
    
    <STYLE>
        INPUT {width: 200} 
    </STYLE>  
    
    <SCRIPT LANGUAGE="VBScript">
    <!--
        function fnStart(sMethod)
            select case sMethod
              case 0    
                  'Minimizes all windows on the desktop
                oshell.Shell_MinimizeAll
              case 1  
                  'Displays the Run dialog box
                oshell.FileRun
              case 2  
                  'Displays the Shut Down Windows dialog box
                oshell.Shell_ShutdownWindows
              case 3  
                  'Displays the Find dialog box
                oshell.Shell_FindFilesr
              case 4  
                  'Displays the Date/Time dialog box
                oshell.Shell_SetTime 
              case 5  
                  'Displays the Internet Properties dialog box
                oshell.Shell_ControlPanelItem "INETCPL.cpl"
              case 6  
                  'Explores the My Documents folder
                oshell.Shell_Explore "C:\My Documents"
              case 7  
                  'Enables user to select folder from Program Files
                oshell.Shell_BrowseForFolder 0, "My Programs", 0, "C:\Program Files" 
              case 8  
                  'Opens the Favorites folder
                oshell.Shell_Open "C:\WINDOWS\Favorites"
              case 9  
                  'Displays the Taskbar Properties dialog box
                oshell.Shell_TrayProperties
            end select  
        end function      
    -->
    </SCRIPT>
</HEAD>

<BODY>
    <H1>Start...</H1>
    <INPUT type="button" value="Edit Taskbar Properties" onclick="fnStart(9)"><br>
    <INPUT type="button" value="Open Favorites Folder" onclick="fnStart(8)"><br>
    <INPUT type="button" value="Browse Program Files" onclick="fnStart(7)"><br>
    <INPUT type="button" value="Explore My Documents" onclick="fnStart(6)"><br>
    <INPUT type="button" value="Modify Internet Properties" onclick="fnStart(5)"><br>
    <INPUT type="button" value="Set System Time" onclick="fnStart(4)"><br>
    <INPUT type="button" value="Find a File or Folder" onclick="fnStart(3)"><br>
    <INPUT type="button" value="Shut Down Windows" onclick="fnStart(2)"><br>
    <INPUT type="button" value="Run" onclick="fnStart(1)">     
    <INPUT type="button" value="Minimize All Windows" onclick="fnStart(0)">     
</BODY>
</HTML>
```



### <a name="security"></a><span data-ttu-id="f026c-249">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="f026c-249">Security</span></span>

<span data-ttu-id="f026c-250">Als Anwendung wird eine HTA unter einem anderen Sicherheitsmodell als eine Webseite ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f026c-250">As an application, an HTA runs under a different security model than a webpage.</span></span> <span data-ttu-id="f026c-251">Um mit einer Webseite zu interagieren, die die Funktionalität der Shellobjekte implementiert, müssen Benutzer die **ActiveX-Steuerelemente initialisieren und Skripts, die nicht als sichere Option gekennzeichnet** sind, für die Sicherheitszone aktivieren, in der Sie die Seite anzeigen.</span><span class="sxs-lookup"><span data-stu-id="f026c-251">To interact with a webpage that implements the functionality of the Shell objects, users must enable the **Initialize and script ActiveX Controls not marked as safe** option for the security zone in which they are viewing the page.</span></span>

## <a name="folder-objects"></a><span data-ttu-id="f026c-252">Ordner Objekte</span><span class="sxs-lookup"><span data-stu-id="f026c-252">Folder Objects</span></span>

<span data-ttu-id="f026c-253">Das [**Folder**](folder.md) -Objekt stellt einen Shellordner dar.</span><span class="sxs-lookup"><span data-stu-id="f026c-253">The [**Folder**](folder.md) object represents a Shell folder.</span></span> <span data-ttu-id="f026c-254">Sie können die Methoden, die vom Folder-Objekt verfügbar gemacht werden, für Folgendes verwenden:</span><span class="sxs-lookup"><span data-stu-id="f026c-254">You can use the methods exposed by the Folder object to:</span></span>

-   <span data-ttu-id="f026c-255">Hier erhalten Sie Informationen zu einem Ordner.</span><span class="sxs-lookup"><span data-stu-id="f026c-255">Get information about a folder.</span></span>
-   <span data-ttu-id="f026c-256">Erstellen Sie Unterordner.</span><span class="sxs-lookup"><span data-stu-id="f026c-256">Create subfolders.</span></span>
-   <span data-ttu-id="f026c-257">Kopieren Sie Datei Objekte, und verschieben Sie Sie in den Ordner.</span><span class="sxs-lookup"><span data-stu-id="f026c-257">Copy and move file objects into the folder.</span></span>

<span data-ttu-id="f026c-258">Das [**folderItem**](folderitem.md) -Objekt stellt ein Element in einem Shellordner dar.</span><span class="sxs-lookup"><span data-stu-id="f026c-258">The [**FolderItem**](folderitem.md) object represents an item in a Shell folder.</span></span> <span data-ttu-id="f026c-259">Mit den Eigenschaften können Sie Informationen zum Element abrufen.</span><span class="sxs-lookup"><span data-stu-id="f026c-259">Its properties enable you to retrieve information about the item.</span></span> <span data-ttu-id="f026c-260">Sie können die Methoden, die von diesem-Objekt verfügbar gemacht werden, zum Ausführen der Verben eines Elements oder zum Abrufen von Informationen über das [**folderitemverbs**](folderitemverbs.md) -Objekt eines Elements verwenden.</span><span class="sxs-lookup"><span data-stu-id="f026c-260">You can use the methods exposed by this object to run an item's verbs, or to retrieve information about an item's [**FolderItemVerbs**](folderitemverbs.md) object.</span></span>

<span data-ttu-id="f026c-261">Das [**folderitems**](folderitems.md) -Objekt stellt eine Sammlung von Elementen in einem Shellordner dar.</span><span class="sxs-lookup"><span data-stu-id="f026c-261">The [**FolderItems**](folderitems.md) object represents a collection of items in a Shell folder.</span></span> <span data-ttu-id="f026c-262">Die zugehörigen Methoden und Eigenschaften ermöglichen es Ihnen, Informationen über die Sammlung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f026c-262">Its methods and properties enable you to retrieve information about the collection.</span></span>

<span data-ttu-id="f026c-263">Im folgenden Visual Basic Beispiel wird die Beziehung zwischen mehreren Ordner Objekten und deren Verwendung zusammen gezeigt.</span><span class="sxs-lookup"><span data-stu-id="f026c-263">The following Visual Basic example shows the relationship between several of the folder objects and how they can be used together.</span></span> <span data-ttu-id="f026c-264">Wenn der Benutzer auf die Befehls Schaltfläche **cmdgetpath** klickt, zeigt das Programm ein Dialogfeld an, in dem der Benutzer einen Ordner aus **Arbeitsplatz** auswählen kann, wobei ssfdrives der [**shellspecialfolderconstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) -Enumerationswert für **Arbeitsplatz** ist.</span><span class="sxs-lookup"><span data-stu-id="f026c-264">When the user clicks the command button called **cmdGetPath**, the program displays a dialog box that enables the user to select a folder from **My Computer**, where ssfDRIVES is the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) enumeration value for **My Computer**.</span></span> <span data-ttu-id="f026c-265">Wenn der Benutzer einen Ordner auswählt, wird der Pfad des Ordners im Textfeld mit dem Namen " **txtpath**" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f026c-265">When the user chooses a folder, the folder's path is displayed in the text box called **txtPath**.</span></span>


```
Private Sub cmdGetPath_Click()
    Dim oShell As New Shell
    Dim oFolder As Folder
    Dim oFolderItem As FolderItem
 
    Set oFolder = oshell.Shell_BrowseForFolder(Me.hWnd, "Select a Folder", 0, ssfDrives)
   
    Set oFolderItem = oFolderItems.Item

    txtPath.Text = oFolderItem.Path
End Sub
```



<span data-ttu-id="f026c-266">In VBScript unterscheidet sich diese Funktion etwas, da die Enumerationswerte von [**shellspecialfolderkonstanten**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) nicht im Skript verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="f026c-266">In VBScript, this function is slightly different because the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) enumeration values are not available in script.</span></span> <span data-ttu-id="f026c-267">Das folgende Beispiel zeigt die VBScript-Entsprechung des vorherigen Beispiels.</span><span class="sxs-lookup"><span data-stu-id="f026c-267">The following example shows the VBScript equivalent of the previous example.</span></span>


```
<SCRIPT LANGUAGE="VBScript">
<!--
    function fnGetMyPathVB() 
        dim oShell
        dim oFolder
        dim oFolderItem
        
        set oShell = CreateObject("shell.application")      
        set oFolder = oshell.Shell_BrowseForFolder(0, "Choose a Folder", 0)             
        set oFolderItem = oFolder.Items.Item         
        
        document.all.item("myPath").innerText = oFolderItem.Path                                
    end function
-->
</SCRIPT>
```



<span data-ttu-id="f026c-268">Im folgenden JScript-Beispiel, bei dem es sich um eine direkte Übersetzung des vorangehenden VBScript-Beispiels handelt, beachten Sie, wie die leeren Klammern "()" verwendet werden, um die [**Elemente**](folder-items.md) und [**Element**](folderitems-item.md) Methoden aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="f026c-268">In the following JScript example, which is a direct translation of the preceding VBScript example, note how the empty parentheses '()' are used to invoke the [**Items**](folder-items.md) and [**Item**](folderitems-item.md) methods.</span></span>


```
<SCRIPT LANGUAGE="JavaScript">
<!--
    function fnGetMyPathJ() 
    {       
        var oShell = new ActiveXObject("shell.application");
                    
        var oFolder = new Object;                   
        oFolder = oshell.Shell_BrowseForFolder(0, "Choose a folder", 0);
                                
        var oFolderItem = new Object;       
        oFolderItem = oFolder.Items().Item();                               
        
        document.all.item("myPath").innerText = oFolderItem.Path;
    }    
-->
</SCRIPT>
```



 

 
