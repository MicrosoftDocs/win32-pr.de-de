---
description: Die Windows Shell bietet einen leistungsstarken Satz von Automatisierungsobjekten, mit denen Sie die Shell mit Microsoft Visual Basic und Skriptsprachen wie Microsoft JScript (kompatibel mit der ECMA 262-Sprachspezifikation) und Microsoft Visual Basic Scripting Edition (VBScript) programmieren können. Sie können diese Objekte verwenden, um auf viele der Funktionen und Dialogfelder der Shell zu zugreifen. Beispielsweise können Sie auf das Dateisystem zugreifen, Programme starten und Systemeinstellungen ändern.
title: Skriptfähige Shellobjekte
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 09455fad-a769-42ef-83ba-b745ac819bf3
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e8685b44d00d3f48e8de2a567218ef08c1cb5070
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581778"
---
# <a name="scriptable-shell-objects"></a><span data-ttu-id="a41c8-105">Skriptfähige Shellobjekte</span><span class="sxs-lookup"><span data-stu-id="a41c8-105">Scriptable Shell Objects</span></span>

<span data-ttu-id="a41c8-106">Die Windows Shell bietet einen leistungsstarken Satz von Automatisierungsobjekten, mit denen Sie die Shell mit Microsoft Visual Basic und Skriptsprachen wie Microsoft JScript (kompatibel mit der ECMA 262-Sprachspezifikation) und Microsoft Visual Basic Scripting Edition (VBScript) programmieren können.</span><span class="sxs-lookup"><span data-stu-id="a41c8-106">The Windows Shell provides a powerful set of automation objects that enable you to program the Shell with Microsoft Visual Basic and scripting languages such as Microsoft JScript (compatible with ECMA 262 language specification) and Microsoft Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="a41c8-107">Sie können diese Objekte verwenden, um auf viele der Funktionen und Dialogfelder der Shell zu zugreifen.</span><span class="sxs-lookup"><span data-stu-id="a41c8-107">You can use these objects to access many of the Shell's features and dialog boxes.</span></span> <span data-ttu-id="a41c8-108">Beispielsweise können Sie auf das Dateisystem zugreifen, Programme starten und Systemeinstellungen ändern.</span><span class="sxs-lookup"><span data-stu-id="a41c8-108">For example, you can access the file system, launch programs, and change system settings.</span></span>

<span data-ttu-id="a41c8-109">In diesem Abschnitt werden die skriptierbaren Shellobjekte erläutert.</span><span class="sxs-lookup"><span data-stu-id="a41c8-109">This section introduces the scriptable Shell objects.</span></span>

-   [<span data-ttu-id="a41c8-110">Shellversionen</span><span class="sxs-lookup"><span data-stu-id="a41c8-110">Shell Versions</span></span>](#shell-versions)
-   [<span data-ttu-id="a41c8-111">Instanziieren von Shellobjekten</span><span class="sxs-lookup"><span data-stu-id="a41c8-111">Instantiating Shell Objects</span></span>](#instantiating-shell-objects)
    -   [<span data-ttu-id="a41c8-112">Späte Bindung</span><span class="sxs-lookup"><span data-stu-id="a41c8-112">Late Binding</span></span>](#late-binding)
    -   [<span data-ttu-id="a41c8-113">HTML OBJECT-Element</span><span class="sxs-lookup"><span data-stu-id="a41c8-113">HTML OBJECT Element</span></span>](#html-object-element)
-   [<span data-ttu-id="a41c8-114">Shell-Objekt</span><span class="sxs-lookup"><span data-stu-id="a41c8-114">Shell Object</span></span>](#shell-object)
    -   [<span data-ttu-id="a41c8-115">Security</span><span class="sxs-lookup"><span data-stu-id="a41c8-115">Security</span></span>](#security)
-   [<span data-ttu-id="a41c8-116">Ordnerobjekte</span><span class="sxs-lookup"><span data-stu-id="a41c8-116">Folder Objects</span></span>](#folder-objects)

## <a name="shell-versions"></a><span data-ttu-id="a41c8-117">Shellversionen</span><span class="sxs-lookup"><span data-stu-id="a41c8-117">Shell Versions</span></span>

<span data-ttu-id="a41c8-118">Viele der Shell-Objekte wurden in Version [4.71 der](versions.md) Shell verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a41c8-118">Many of the Shell objects became available in [version 4.71](versions.md) of the Shell.</span></span> <span data-ttu-id="a41c8-119">Andere sind in Version 5.00 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a41c8-119">Others are available in version 5.00 and later.</span></span> <span data-ttu-id="a41c8-120">Version 5.00 ist ab Windows 2000 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a41c8-120">Version 5.00 became available with Windows 2000.</span></span> <span data-ttu-id="a41c8-121">In der folgenden Tabelle sind alle Shell-Objekte unter der Version der Shell aufgeführt, in der das Objekt verfügbar wurde.</span><span class="sxs-lookup"><span data-stu-id="a41c8-121">The following table lists each Shell object under the version of the Shell in which the object became available.</span></span>



| <span data-ttu-id="a41c8-122">Version 4.71</span><span class="sxs-lookup"><span data-stu-id="a41c8-122">Version 4.71</span></span>                                            | <span data-ttu-id="a41c8-123">Version 5.00</span><span class="sxs-lookup"><span data-stu-id="a41c8-123">Version 5.00</span></span>                                          |
|---------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="a41c8-124">**Ordner**</span><span class="sxs-lookup"><span data-stu-id="a41c8-124">**Folder**</span></span>](folder.md)                                | [<span data-ttu-id="a41c8-125">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="a41c8-125">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)     |
| [<span data-ttu-id="a41c8-126">**FolderItemVerb**</span><span class="sxs-lookup"><span data-stu-id="a41c8-126">**FolderItemVerb**</span></span>](folderitemverb.md)                | [<span data-ttu-id="a41c8-127">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="a41c8-127">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)   |
| [<span data-ttu-id="a41c8-128">**FolderItemVerbs**</span><span class="sxs-lookup"><span data-stu-id="a41c8-128">**FolderItemVerbs**</span></span>](folderitemverbs.md)              | [<span data-ttu-id="a41c8-129">**Ordner2**</span><span class="sxs-lookup"><span data-stu-id="a41c8-129">**Folder2**</span></span>](folder2-object.md)                     |
| [<span data-ttu-id="a41c8-130">**Shell**</span><span class="sxs-lookup"><span data-stu-id="a41c8-130">**Shell**</span></span>](shell.md)                                  | [<span data-ttu-id="a41c8-131">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="a41c8-131">**FolderItem**</span></span>](folderitem.md)                      |
| [<span data-ttu-id="a41c8-132">**ShellFolderView**</span><span class="sxs-lookup"><span data-stu-id="a41c8-132">**ShellFolderView**</span></span>](shellfolderview.md)              | [<span data-ttu-id="a41c8-133">**FolderItems**</span><span class="sxs-lookup"><span data-stu-id="a41c8-133">**FolderItems**</span></span>](folderitems.md)                    |
| [<span data-ttu-id="a41c8-134">**ShellUIHelper**</span><span class="sxs-lookup"><span data-stu-id="a41c8-134">**ShellUIHelper**</span></span>](shelluihelper.md)                  | [<span data-ttu-id="a41c8-135">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="a41c8-135">**FolderItems2**</span></span>](folderitems2-object.md)           |
| [<span data-ttu-id="a41c8-136">**ShellWindows**</span><span class="sxs-lookup"><span data-stu-id="a41c8-136">**ShellWindows**</span></span>](shellwindows.md)                    | [<span data-ttu-id="a41c8-137">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="a41c8-137">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)     |
| [<span data-ttu-id="a41c8-138">**WebViewFolderContents**</span><span class="sxs-lookup"><span data-stu-id="a41c8-138">**WebViewFolderContents**</span></span>](../lwef/webviewfoldercontents.md) | [<span data-ttu-id="a41c8-139">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="a41c8-139">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)     |
|                                                         | [<span data-ttu-id="a41c8-140">**ShellFolderItem**</span><span class="sxs-lookup"><span data-stu-id="a41c8-140">**ShellFolderItem**</span></span>](shellfolderitem-object.md)     |
|                                                         | [<span data-ttu-id="a41c8-141">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="a41c8-141">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md) |
|                                                         | [<span data-ttu-id="a41c8-142">**ShellLinkObject**</span><span class="sxs-lookup"><span data-stu-id="a41c8-142">**ShellLinkObject**</span></span>](shelllinkobject-object.md)     |



 

## <a name="instantiating-shell-objects"></a><span data-ttu-id="a41c8-143">Instanziieren von Shellobjekten</span><span class="sxs-lookup"><span data-stu-id="a41c8-143">Instantiating Shell Objects</span></span>

<span data-ttu-id="a41c8-144">Fügen Sie Verweise auf die folgenden Bibliotheken in Ihrem Projekt hinzu, um die Shellobjekte in Visual Basic Anwendungen mit früher Bindung zu instanziieren:</span><span class="sxs-lookup"><span data-stu-id="a41c8-144">To instantiate the Shell objects in Visual Basic applications with early binding, add references to the following libraries in your project:</span></span>

-   <span data-ttu-id="a41c8-145">Microsoft-Internetsteuerelemente (SHDocVw)</span><span class="sxs-lookup"><span data-stu-id="a41c8-145">Microsoft Internet Controls (SHDocVw)</span></span>
-   <span data-ttu-id="a41c8-146">Microsoft Shell-Steuerelemente und -Automatisierung (Shell32)</span><span class="sxs-lookup"><span data-stu-id="a41c8-146">Microsoft Shell Controls and Automation (Shell32)</span></span>

### <a name="late-binding"></a><span data-ttu-id="a41c8-147">Späte Bindung</span><span class="sxs-lookup"><span data-stu-id="a41c8-147">Late Binding</span></span>

<span data-ttu-id="a41c8-148">Sie können auch viele der Shell-Objekte mit später Bindung instanziieren.</span><span class="sxs-lookup"><span data-stu-id="a41c8-148">You can also instantiate many of the Shell objects with late binding.</span></span> <span data-ttu-id="a41c8-149">Dieser Ansatz funktioniert in Visual Basic Anwendungen und Skripts.</span><span class="sxs-lookup"><span data-stu-id="a41c8-149">This approach works in Visual Basic applications and in script.</span></span> <span data-ttu-id="a41c8-150">Das folgende Beispiel zeigt, wie sie das [**Shell-Objekt**](shell.md) in der JScript.</span><span class="sxs-lookup"><span data-stu-id="a41c8-150">The following example shows how to instantiate the [**Shell**](shell.md) object in JScript.</span></span>


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



<span data-ttu-id="a41c8-151">Das folgende Beispiel zeigt, wie das [**Folder-Objekt**](folder.md) in VBScript instanziiert wird.</span><span class="sxs-lookup"><span data-stu-id="a41c8-151">The following example shows how to instantiate the [**Folder**](folder.md) object in VBScript.</span></span>


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



<span data-ttu-id="a41c8-152">Im vorherigen Beispiel ist *sDir* der Pfad zum [**Folder-Objekt.**](folder.md)</span><span class="sxs-lookup"><span data-stu-id="a41c8-152">In the preceding example, *sDir* is the path to the [**Folder**](folder.md) object.</span></span> <span data-ttu-id="a41c8-153">Beachten Sie, [**dass die ShellSpecialFolderConstants-Enumerationswerte**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) im Skript nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="a41c8-153">Note that the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) enumeration values are not available in script.</span></span>

<span data-ttu-id="a41c8-154">Die ProgID für jedes der Shell-Objekte ist in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a41c8-154">The ProgID for each of the Shell objects is shown in the following table.</span></span>



| <span data-ttu-id="a41c8-155">Object</span><span class="sxs-lookup"><span data-stu-id="a41c8-155">Object</span></span>                                                  | <span data-ttu-id="a41c8-156">ProgID</span><span class="sxs-lookup"><span data-stu-id="a41c8-156">ProgID</span></span>                                                                                  |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="a41c8-157">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="a41c8-157">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)       | <span data-ttu-id="a41c8-158">Microsoft.DiskQuota.1</span><span class="sxs-lookup"><span data-stu-id="a41c8-158">Microsoft.DiskQuota.1</span></span>                                                                   |
| [<span data-ttu-id="a41c8-159">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="a41c8-159">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)     | <span data-ttu-id="a41c8-160">Späte Bindung nicht möglich</span><span class="sxs-lookup"><span data-stu-id="a41c8-160">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="a41c8-161">**Ordner**</span><span class="sxs-lookup"><span data-stu-id="a41c8-161">**Folder**</span></span>](folder.md)                                | <span data-ttu-id="a41c8-162">Muschel. Shell \_ Application.NameSpace("...")</span><span class="sxs-lookup"><span data-stu-id="a41c8-162">shell.Shell\_Application.NameSpace("...")</span></span>                                               |
| [<span data-ttu-id="a41c8-163">**Ordner2**</span><span class="sxs-lookup"><span data-stu-id="a41c8-163">**Folder2**</span></span>](folder2-object.md)                       | <span data-ttu-id="a41c8-164">Muschel. Shell \_ Application.NameSpace("...")</span><span class="sxs-lookup"><span data-stu-id="a41c8-164">shell.Shell\_Application.NameSpace("...")</span></span>                                               |
| [<span data-ttu-id="a41c8-165">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="a41c8-165">**FolderItem**</span></span>](folderitem.md)                        | <span data-ttu-id="a41c8-166">Muschel. Shell \_ Application.NameSpace("..."). Self oder Folder.Items.Item oder Folder.ParseName</span><span class="sxs-lookup"><span data-stu-id="a41c8-166">shell.Shell\_Application.NameSpace("...").Self or Folder.Items.Item or Folder.ParseName</span></span> |
| [<span data-ttu-id="a41c8-167">**FolderItems**</span><span class="sxs-lookup"><span data-stu-id="a41c8-167">**FolderItems**</span></span>](folderitems.md)                      | <span data-ttu-id="a41c8-168">Folder.Items</span><span class="sxs-lookup"><span data-stu-id="a41c8-168">Folder.Items</span></span>                                                                            |
| [<span data-ttu-id="a41c8-169">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="a41c8-169">**FolderItems2**</span></span>](folderitems2-object.md)             | <span data-ttu-id="a41c8-170">Folder.Items</span><span class="sxs-lookup"><span data-stu-id="a41c8-170">Folder.Items</span></span>                                                                            |
| [<span data-ttu-id="a41c8-171">**FolderItemVerb**</span><span class="sxs-lookup"><span data-stu-id="a41c8-171">**FolderItemVerb**</span></span>](folderitemverb.md)                | <span data-ttu-id="a41c8-172">Shell.NameSpace("..."). Self.Verbs.Item()</span><span class="sxs-lookup"><span data-stu-id="a41c8-172">Shell.NameSpace("...").Self.Verbs.Item()</span></span>                                                |
| [<span data-ttu-id="a41c8-173">**FolderItemVerbs**</span><span class="sxs-lookup"><span data-stu-id="a41c8-173">**FolderItemVerbs**</span></span>](folderitemverbs.md)              | <span data-ttu-id="a41c8-174">FolderItem.Verbs oder Shell.NameSpace("..."). Self.Verbs</span><span class="sxs-lookup"><span data-stu-id="a41c8-174">FolderItem.Verbs or Shell.NameSpace("...").Self.Verbs</span></span>                                   |
| [<span data-ttu-id="a41c8-175">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="a41c8-175">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)       | <span data-ttu-id="a41c8-176">Muschel. \_Shellanwendung</span><span class="sxs-lookup"><span data-stu-id="a41c8-176">shell.Shell\_Application</span></span>                                                                |
| [<span data-ttu-id="a41c8-177">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="a41c8-177">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)       | <span data-ttu-id="a41c8-178">Shell.NameSpace("..."). Self.GetLink oder Shell.NameSpace("..."). Items(). GetLink</span><span class="sxs-lookup"><span data-stu-id="a41c8-178">Shell.NameSpace("...").Self.GetLink or Shell.NameSpace("...").Items().GetLink</span></span>           |
| [<span data-ttu-id="a41c8-179">**Shell**</span><span class="sxs-lookup"><span data-stu-id="a41c8-179">**Shell**</span></span>](shell.md)                                  | <span data-ttu-id="a41c8-180">Muschel. \_Shellanwendung</span><span class="sxs-lookup"><span data-stu-id="a41c8-180">shell.Shell\_Application</span></span>                                                                |
| [<span data-ttu-id="a41c8-181">**ShellFolderItem**</span><span class="sxs-lookup"><span data-stu-id="a41c8-181">**ShellFolderItem**</span></span>](shellfolderitem-object.md)       | <span data-ttu-id="a41c8-182">Shell.NameSpace("..."). Self oder Shell.NameSpace("..."). Items()</span><span class="sxs-lookup"><span data-stu-id="a41c8-182">Shell.NameSpace("...").Self or Shell.NameSpace("...").Items()</span></span>                           |
| [<span data-ttu-id="a41c8-183">**ShellFolderView**</span><span class="sxs-lookup"><span data-stu-id="a41c8-183">**ShellFolderView**</span></span>](shellfolderview.md)              | <span data-ttu-id="a41c8-184">Späte Bindung nicht möglich</span><span class="sxs-lookup"><span data-stu-id="a41c8-184">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="a41c8-185">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="a41c8-185">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)   | <span data-ttu-id="a41c8-186">Späte Bindung nicht möglich</span><span class="sxs-lookup"><span data-stu-id="a41c8-186">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="a41c8-187">**ShellLinkObject**</span><span class="sxs-lookup"><span data-stu-id="a41c8-187">**ShellLinkObject**</span></span>](shelllinkobject-object.md)       | <span data-ttu-id="a41c8-188">Shell.NameSpace("..."). Self.GetLink oder Shell.NameSpace("..."). Items(). GetLink</span><span class="sxs-lookup"><span data-stu-id="a41c8-188">Shell.NameSpace("...").Self.GetLink or Shell.NameSpace("...").Items().GetLink</span></span>           |
| [<span data-ttu-id="a41c8-189">**ShellUIHelper**</span><span class="sxs-lookup"><span data-stu-id="a41c8-189">**ShellUIHelper**</span></span>](shelluihelper.md)                  | <span data-ttu-id="a41c8-190">Späte Bindung nicht möglich</span><span class="sxs-lookup"><span data-stu-id="a41c8-190">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="a41c8-191">**ShellWindows**</span><span class="sxs-lookup"><span data-stu-id="a41c8-191">**ShellWindows**</span></span>](shellwindows.md)                    | <span data-ttu-id="a41c8-192">Muschel. Shell \_ Windows oder ShellWindows. \_ NewEnum</span><span class="sxs-lookup"><span data-stu-id="a41c8-192">shell.Shell\_Windows or ShellWindows.\_NewEnum</span></span>                                          |
| [<span data-ttu-id="a41c8-193">**WebViewFolderContents**</span><span class="sxs-lookup"><span data-stu-id="a41c8-193">**WebViewFolderContents**</span></span>](../lwef/webviewfoldercontents.md) | <span data-ttu-id="a41c8-194">Späte Bindung nicht möglich</span><span class="sxs-lookup"><span data-stu-id="a41c8-194">Cannot late bind</span></span>                                                                        |



 

### <a name="html-object-element"></a><span data-ttu-id="a41c8-195">HTML OBJECT-Element</span><span class="sxs-lookup"><span data-stu-id="a41c8-195">HTML OBJECT Element</span></span>

<span data-ttu-id="a41c8-196">Sie können auch das [**OBJECT-Element**](https://msdn.microsoft.com/library/ms535859(v=VS.85).aspx) verwenden, um Shellobjekte auf einer HTML-Seite zu instanziieren.</span><span class="sxs-lookup"><span data-stu-id="a41c8-196">You can also use the [**OBJECT**](https://msdn.microsoft.com/library/ms535859(v=VS.85).aspx) element to instantiate Shell objects on an HTML page.</span></span> <span data-ttu-id="a41c8-197">Legen Sie hierzu das **ID-Attribut** des **OBJECT-Elements** auf den Variablennamen fest, den Sie in Ihren Skripts verwenden, und identifizieren Sie das Objekt anhand seiner registrierten Nummer (CLASSID).</span><span class="sxs-lookup"><span data-stu-id="a41c8-197">To do this, set the **OBJECT** element's **ID** attribute to the variable name you will use in your scripts, and identify the object using its registered number (CLASSID).</span></span> <span data-ttu-id="a41c8-198">Der folgende HTML-Code erstellt eine Instanz des [**ShellFolderItem-Objekts**](shellfolderitem-object.md) mithilfe des **OBJECT-Elements.**</span><span class="sxs-lookup"><span data-stu-id="a41c8-198">The following HTML creates an instance of the [**ShellFolderItem**](shellfolderitem-object.md) object using the **OBJECT** element.</span></span>


```
<OBJECT ID="oShFolderItem" 
    NAME="Shell Folder Item Object"
    CLASSID="clsid:2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e">
</OBJECT>
```



<span data-ttu-id="a41c8-199">In der folgenden Tabelle sind jedes Shell-Objekt und die entsprechende CLASSID aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="a41c8-199">The following table lists each Shell object and its respective CLASSID.</span></span>



| <span data-ttu-id="a41c8-200">Shellobjekt</span><span class="sxs-lookup"><span data-stu-id="a41c8-200">Shell object</span></span>                                           | <span data-ttu-id="a41c8-201">Classid</span><span class="sxs-lookup"><span data-stu-id="a41c8-201">CLASSID</span></span>                              |
|--------------------------------------------------------|--------------------------------------|
| [<span data-ttu-id="a41c8-202">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="a41c8-202">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)       | <span data-ttu-id="a41c8-203">7988B571-EC89-11cf-9C00-00AA00A14F56</span><span class="sxs-lookup"><span data-stu-id="a41c8-203">7988B571-EC89-11cf-9C00-00AA00A14F56</span></span> |
| [<span data-ttu-id="a41c8-204">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="a41c8-204">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)     | <span data-ttu-id="a41c8-205">7988B571-EC89-11cf-9C00-00AA00A14F56</span><span class="sxs-lookup"><span data-stu-id="a41c8-205">7988B571-EC89-11cf-9C00-00AA00A14F56</span></span> |
| [<span data-ttu-id="a41c8-206">**Ordner**</span><span class="sxs-lookup"><span data-stu-id="a41c8-206">**Folder**</span></span>](folder.md)                                | <span data-ttu-id="a41c8-207">SOLLBDE60-C3FF-11CE-8350-444553540000</span><span class="sxs-lookup"><span data-stu-id="a41c8-207">BBCBDE60-C3FF-11CE-8350-444553540000</span></span> |
| [<span data-ttu-id="a41c8-208">**Folder2**</span><span class="sxs-lookup"><span data-stu-id="a41c8-208">**Folder2**</span></span>](folder2-object.md)                       | <span data-ttu-id="a41c8-209">f0d2d8ef-3890-11d2-bf8b-00c04fb93661</span><span class="sxs-lookup"><span data-stu-id="a41c8-209">f0d2d8ef-3890-11d2-bf8b-00c04fb93661</span></span> |
| [<span data-ttu-id="a41c8-210">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="a41c8-210">**FolderItem**</span></span>](folderitem.md)                        | <span data-ttu-id="a41c8-211">744129E0-CBE5-11CE-8350-444553540000</span><span class="sxs-lookup"><span data-stu-id="a41c8-211">744129E0-CBE5-11CE-8350-444553540000</span></span> |
| [<span data-ttu-id="a41c8-212">**FolderItems**</span><span class="sxs-lookup"><span data-stu-id="a41c8-212">**FolderItems**</span></span>](folderitems.md)                      | <span data-ttu-id="a41c8-213">744129E0-CBE5-11CE-8350-444553540000</span><span class="sxs-lookup"><span data-stu-id="a41c8-213">744129E0-CBE5-11CE-8350-444553540000</span></span> |
| [<span data-ttu-id="a41c8-214">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="a41c8-214">**FolderItems2**</span></span>](folderitems2-object.md)             | <span data-ttu-id="a41c8-215">C94F0AD0-F363-11d2-A327-00C04F8EEC7F</span><span class="sxs-lookup"><span data-stu-id="a41c8-215">C94F0AD0-F363-11d2-A327-00C04F8EEC7F</span></span> |
| [<span data-ttu-id="a41c8-216">**FolderItemVerb**</span><span class="sxs-lookup"><span data-stu-id="a41c8-216">**FolderItemVerb**</span></span>](folderitemverb.md)                | <span data-ttu-id="a41c8-217">08EC3E00-50B0-11CF-960C-0080C7F4EE85</span><span class="sxs-lookup"><span data-stu-id="a41c8-217">08EC3E00-50B0-11CF-960C-0080C7F4EE85</span></span> |
| [<span data-ttu-id="a41c8-218">**FolderItemVerbs**</span><span class="sxs-lookup"><span data-stu-id="a41c8-218">**FolderItemVerbs**</span></span>](folderitemverbs.md)              | <span data-ttu-id="a41c8-219">1F8352C0-50B0-11CF-960C-0080C7F4EE85</span><span class="sxs-lookup"><span data-stu-id="a41c8-219">1F8352C0-50B0-11CF-960C-0080C7F4EE85</span></span> |
| [<span data-ttu-id="a41c8-220">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="a41c8-220">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)       | <span data-ttu-id="a41c8-221">A4C6892C-3BA9-11d2-9DEA-00C04FB16162</span><span class="sxs-lookup"><span data-stu-id="a41c8-221">A4C6892C-3BA9-11d2-9DEA-00C04FB16162</span></span> |
| [<span data-ttu-id="a41c8-222">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="a41c8-222">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)       | <span data-ttu-id="a41c8-223">317EE249-F12E-11d2-B1E4-00C04F8EEB3E</span><span class="sxs-lookup"><span data-stu-id="a41c8-223">317EE249-F12E-11d2-B1E4-00C04F8EEB3E</span></span> |
| [<span data-ttu-id="a41c8-224">**Shell**</span><span class="sxs-lookup"><span data-stu-id="a41c8-224">**Shell**</span></span>](shell.md)                                  | <span data-ttu-id="a41c8-225">13709620-C279-11CE-A49E-444553540000</span><span class="sxs-lookup"><span data-stu-id="a41c8-225">13709620-C279-11CE-A49E-444553540000</span></span> |
| [<span data-ttu-id="a41c8-226">**ShellFolderItem**</span><span class="sxs-lookup"><span data-stu-id="a41c8-226">**ShellFolderItem**</span></span>](shellfolderitem-object.md)       | <span data-ttu-id="a41c8-227">2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e</span><span class="sxs-lookup"><span data-stu-id="a41c8-227">2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e</span></span> |
| [<span data-ttu-id="a41c8-228">**ShellFolderView**</span><span class="sxs-lookup"><span data-stu-id="a41c8-228">**ShellFolderView**</span></span>](shellfolderview.md)              | <span data-ttu-id="a41c8-229">62112AA1-EBE4-11cf-A5FB-0020AFE7292D</span><span class="sxs-lookup"><span data-stu-id="a41c8-229">62112AA1-EBE4-11cf-A5FB-0020AFE7292D</span></span> |
| [<span data-ttu-id="a41c8-230">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="a41c8-230">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)   | <span data-ttu-id="a41c8-231">4a3df050-23bd-11d2-939f-00a0c91eedba</span><span class="sxs-lookup"><span data-stu-id="a41c8-231">4a3df050-23bd-11d2-939f-00a0c91eedba</span></span> |
| [<span data-ttu-id="a41c8-232">**ShellLinkObject**</span><span class="sxs-lookup"><span data-stu-id="a41c8-232">**ShellLinkObject**</span></span>](shelllinkobject-object.md)       | <span data-ttu-id="a41c8-233">11219420-1768-11d1-95BE-00609797EA4F</span><span class="sxs-lookup"><span data-stu-id="a41c8-233">11219420-1768-11d1-95BE-00609797EA4F</span></span> |
| [<span data-ttu-id="a41c8-234">**ShellUIHelper**</span><span class="sxs-lookup"><span data-stu-id="a41c8-234">**ShellUIHelper**</span></span>](shelluihelper.md)                  | <span data-ttu-id="a41c8-235">64AB4BB7-111E-11D1-8F79-00C04FC2FBE1</span><span class="sxs-lookup"><span data-stu-id="a41c8-235">64AB4BB7-111E-11D1-8F79-00C04FC2FBE1</span></span> |
| [<span data-ttu-id="a41c8-236">**ShellWindows**</span><span class="sxs-lookup"><span data-stu-id="a41c8-236">**ShellWindows**</span></span>](shellwindows.md)                    | <span data-ttu-id="a41c8-237">9BA05972-F6A8-11CF-A442-00A0C90A8F39</span><span class="sxs-lookup"><span data-stu-id="a41c8-237">9BA05972-F6A8-11CF-A442-00A0C90A8F39</span></span> |
| [<span data-ttu-id="a41c8-238">**WebViewFolderContents**</span><span class="sxs-lookup"><span data-stu-id="a41c8-238">**WebViewFolderContents**</span></span>](../lwef/webviewfoldercontents.md) | <span data-ttu-id="a41c8-239">1820FED0-473E-11D0-A96C-00C04FD705A2</span><span class="sxs-lookup"><span data-stu-id="a41c8-239">1820FED0-473E-11D0-A96C-00C04FD705A2</span></span> |



 

## <a name="shell-object"></a><span data-ttu-id="a41c8-240">Shell-Objekt</span><span class="sxs-lookup"><span data-stu-id="a41c8-240">Shell Object</span></span>

<span data-ttu-id="a41c8-241">Das [**Shell-Objekt**](shell.md) stellt die Objekte in der Shell dar.</span><span class="sxs-lookup"><span data-stu-id="a41c8-241">The [**Shell**](shell.md) object represents the objects in the Shell.</span></span> <span data-ttu-id="a41c8-242">Sie können die vom Shell-Objekt verfügbar gemachten Methoden für Folgendes verwenden:</span><span class="sxs-lookup"><span data-stu-id="a41c8-242">You can use the methods exposed by the Shell object to:</span></span>

-   <span data-ttu-id="a41c8-243">Öffnen, Durchsuchen und Suchen nach Ordnern.</span><span class="sxs-lookup"><span data-stu-id="a41c8-243">Open, explore, and browse for folders.</span></span>
-   <span data-ttu-id="a41c8-244">Fenster minimieren, wiederherstellen, kaskadieren oder Kachel öffnen.</span><span class="sxs-lookup"><span data-stu-id="a41c8-244">Minimize, restore, cascade, or tile open windows.</span></span>
-   <span data-ttu-id="a41c8-245">Starten Sie Systemsteuerung Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="a41c8-245">Launch Control Panel applications.</span></span>
-   <span data-ttu-id="a41c8-246">Systemdialogfelder anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a41c8-246">Display system dialog boxes.</span></span>

<span data-ttu-id="a41c8-247">Benutzer sind vielleicht am besten mit den Befehlen vertraut, auf die sie über das **Startmenü** und das Kontextmenü der Taskleiste zugreifen.</span><span class="sxs-lookup"><span data-stu-id="a41c8-247">Users are perhaps most familiar with the commands they access from the **Start** menu and the taskbar's shortcut menu.</span></span> <span data-ttu-id="a41c8-248">Das Kontextmenü der Taskleiste wird angezeigt, wenn Benutzer mit der rechten Maustaste auf die Taskleiste klicken.</span><span class="sxs-lookup"><span data-stu-id="a41c8-248">The taskbar's shortcut menu appears when users right-click the taskbar.</span></span> <span data-ttu-id="a41c8-249">Die folgende HTML-Anwendung (HTA) erzeugt eine Startseite mit Schaltflächen, die viele methoden des [**Shell-Objekts**](shell.md) implementieren.</span><span class="sxs-lookup"><span data-stu-id="a41c8-249">The following HTML Application (HTA) produces a start page with buttons that implement many of the [**Shell**](shell.md) object's methods.</span></span> <span data-ttu-id="a41c8-250">Einige dieser Methoden implementieren Features im **Startmenü** und im Kontextmenü der Taskleiste.</span><span class="sxs-lookup"><span data-stu-id="a41c8-250">Some of these methods implement features on the **Start** menu and the taskbar's shortcut menu.</span></span>


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



### <a name="security"></a><span data-ttu-id="a41c8-251">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="a41c8-251">Security</span></span>

<span data-ttu-id="a41c8-252">Als Anwendung wird ein HTA unter einem anderen Sicherheitsmodell als eine Webseite ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a41c8-252">As an application, an HTA runs under a different security model than a webpage.</span></span> <span data-ttu-id="a41c8-253">Um mit einer Webseite zu interagieren, die die Funktionalität der Shell-Objekte implementiert, müssen Benutzer die **Option Initialisieren und Skripts ActiveX Steuerelemente** aktivieren, die nicht als sichere Option für die Sicherheitszone markiert sind, in der sie die Seite anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a41c8-253">To interact with a webpage that implements the functionality of the Shell objects, users must enable the **Initialize and script ActiveX Controls not marked as safe** option for the security zone in which they are viewing the page.</span></span>

## <a name="folder-objects"></a><span data-ttu-id="a41c8-254">Ordnerobjekte</span><span class="sxs-lookup"><span data-stu-id="a41c8-254">Folder Objects</span></span>

<span data-ttu-id="a41c8-255">Das [**Folder-Objekt**](folder.md) stellt einen Shellordner dar.</span><span class="sxs-lookup"><span data-stu-id="a41c8-255">The [**Folder**](folder.md) object represents a Shell folder.</span></span> <span data-ttu-id="a41c8-256">Sie können die vom Folder-Objekt verfügbar gemachten Methoden für Folgendes verwenden:</span><span class="sxs-lookup"><span data-stu-id="a41c8-256">You can use the methods exposed by the Folder object to:</span></span>

-   <span data-ttu-id="a41c8-257">Abrufen von Informationen zu einem Ordner.</span><span class="sxs-lookup"><span data-stu-id="a41c8-257">Get information about a folder.</span></span>
-   <span data-ttu-id="a41c8-258">Erstellen Sie Unterordner.</span><span class="sxs-lookup"><span data-stu-id="a41c8-258">Create subfolders.</span></span>
-   <span data-ttu-id="a41c8-259">Kopieren und Verschieben von Dateiobjekten in den Ordner.</span><span class="sxs-lookup"><span data-stu-id="a41c8-259">Copy and move file objects into the folder.</span></span>

<span data-ttu-id="a41c8-260">Das [**FolderItem-Objekt**](folderitem.md) stellt ein Element in einem Shellordner dar.</span><span class="sxs-lookup"><span data-stu-id="a41c8-260">The [**FolderItem**](folderitem.md) object represents an item in a Shell folder.</span></span> <span data-ttu-id="a41c8-261">Seine Eigenschaften ermöglichen es Ihnen, Informationen über das Element abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a41c8-261">Its properties enable you to retrieve information about the item.</span></span> <span data-ttu-id="a41c8-262">Sie können die von diesem -Objekt verfügbar gemachten Methoden verwenden, um die Verben eines Elements auszuführen oder Informationen zum [**FolderItemVerbs-Objekt**](folderitemverbs.md) eines Elements abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a41c8-262">You can use the methods exposed by this object to run an item's verbs, or to retrieve information about an item's [**FolderItemVerbs**](folderitemverbs.md) object.</span></span>

<span data-ttu-id="a41c8-263">Das [**FolderItems-Objekt**](folderitems.md) stellt eine Auflistung von Elementen in einem Shellordner dar.</span><span class="sxs-lookup"><span data-stu-id="a41c8-263">The [**FolderItems**](folderitems.md) object represents a collection of items in a Shell folder.</span></span> <span data-ttu-id="a41c8-264">Mithilfe der Methoden und Eigenschaften können Sie Informationen über die Auflistung abrufen.</span><span class="sxs-lookup"><span data-stu-id="a41c8-264">Its methods and properties enable you to retrieve information about the collection.</span></span>

<span data-ttu-id="a41c8-265">Das folgende Visual Basic Beispiel zeigt die Beziehung zwischen mehreren Ordnerobjekten und wie sie zusammen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="a41c8-265">The following Visual Basic example shows the relationship between several of the folder objects and how they can be used together.</span></span> <span data-ttu-id="a41c8-266">Wenn der Benutzer auf die Befehlsschaltfläche **cmdGetPath** klickt, zeigt das Programm ein Dialogfeld an, in dem der Benutzer einen Ordner aus **Arbeitsplatz** auswählen kann, wobei ssfDRIVES der [**ShellSpecialFolderConstants-Enumerationswert**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) für **Arbeitsplatz** ist.</span><span class="sxs-lookup"><span data-stu-id="a41c8-266">When the user clicks the command button called **cmdGetPath**, the program displays a dialog box that enables the user to select a folder from **My Computer**, where ssfDRIVES is the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) enumeration value for **My Computer**.</span></span> <span data-ttu-id="a41c8-267">Wenn der Benutzer einen Ordner ausgibt, wird der Pfad des Ordners im Textfeld **txtPath** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a41c8-267">When the user chooses a folder, the folder's path is displayed in the text box called **txtPath**.</span></span>


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



<span data-ttu-id="a41c8-268">In VBScript unterscheidet sich diese Funktion geringfügig, da die [**ShellSpecialFolderConstants-Enumerationswerte**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) im Skript nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="a41c8-268">In VBScript, this function is slightly different because the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) enumeration values are not available in script.</span></span> <span data-ttu-id="a41c8-269">Das folgende Beispiel zeigt die VBScript-Entsprechung des vorherigen Beispiels.</span><span class="sxs-lookup"><span data-stu-id="a41c8-269">The following example shows the VBScript equivalent of the previous example.</span></span>


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



<span data-ttu-id="a41c8-270">Beachten Sie im folgenden JScript Beispiel, bei dem es sich um eine direkte Übersetzung des vorherigen VBScript-Beispiels handelt, wie die leeren Klammern "()" zum Aufrufen der [**Items-**](folder-items.md) und [**Item-Methoden**](folderitems-item.md) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a41c8-270">In the following JScript example, which is a direct translation of the preceding VBScript example, note how the empty parentheses '()' are used to invoke the [**Items**](folder-items.md) and [**Item**](folderitems-item.md) methods.</span></span>


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



 

 
