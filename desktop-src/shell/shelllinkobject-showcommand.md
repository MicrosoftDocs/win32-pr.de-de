---
description: Ruft den anfänglichen Anzeige Zustand (Größen, minimiert oder maximiert) des Befehls des links ab oder legt ihn fest.
ms.assetid: 139c6924-f554-4fde-9ed0-bc117bafbb16
title: Shelllinkobject. showcommand-Eigenschaft (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.ShowCommand
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9bacdf98a24d749b5128bc286f06e99299aef437
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995166"
---
# <a name="shelllinkobjectshowcommand-property"></a><span data-ttu-id="78bc2-103">Shelllinkobject. showcommand (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="78bc2-103">ShellLinkObject.ShowCommand property</span></span>

<span data-ttu-id="78bc2-104">Ruft den anfänglichen Anzeige Zustand (Größen, minimiert oder maximiert) des Befehls des links ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="78bc2-104">Gets or sets the initial display state (sized, minimized, or maximized) of the link's command.</span></span>

<span data-ttu-id="78bc2-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="78bc2-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="78bc2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="78bc2-106">Syntax</span></span>


```JScript
iShowCommand = ShellLinkObject.ShowCommand
ShellLinkObject.ShowCommand(intShowCommand) = iShowCommand
```



## <a name="property-value"></a><span data-ttu-id="78bc2-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="78bc2-107">Property value</span></span>

<span data-ttu-id="78bc2-108">der Anzeige Zustand des Links.</span><span class="sxs-lookup"><span data-stu-id="78bc2-108">the link's display state.</span></span> <span data-ttu-id="78bc2-109">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="78bc2-109">This can be one of the following values:</span></span>

<dt>



 <span data-ttu-id="78bc2-110">(1)</span><span class="sxs-lookup"><span data-stu-id="78bc2-110">(1)</span></span>


</dt> <dd>

<span data-ttu-id="78bc2-111">Aktiviert und zeigt ein Fenster an.</span><span class="sxs-lookup"><span data-stu-id="78bc2-111">Activates and displays a window.</span></span> <span data-ttu-id="78bc2-112">Wenn das Fenster minimiert oder maximiert ist, stellt das System die ursprüngliche Größe und Position wieder her.</span><span class="sxs-lookup"><span data-stu-id="78bc2-112">If the window is minimized or maximized, the system restores it to its original size and position.</span></span>

</dd> <dt>



 <span data-ttu-id="78bc2-113">(2)</span><span class="sxs-lookup"><span data-stu-id="78bc2-113">(2)</span></span>


</dt> <dd>

<span data-ttu-id="78bc2-114">Aktiviert das Fenster und zeigt es als minimiertes Fenster an.</span><span class="sxs-lookup"><span data-stu-id="78bc2-114">Activates the window and displays it as a minimized window.</span></span>

</dd> <dt>



 <span data-ttu-id="78bc2-115">(3)</span><span class="sxs-lookup"><span data-stu-id="78bc2-115">(3)</span></span>


</dt> <dd>

<span data-ttu-id="78bc2-116">Aktiviert das Fenster und zeigt es als maximiertes Fenster an.</span><span class="sxs-lookup"><span data-stu-id="78bc2-116">Activates the window and displays it as a maximized window.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="78bc2-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="78bc2-117">Examples</span></span>

<span data-ttu-id="78bc2-118">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Eigenschaft in JScript, VBScript und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="78bc2-118">The following example shows the proper usage of this property in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="78bc2-119">JScript</span><span class="sxs-lookup"><span data-stu-id="78bc2-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShellLinkObjectShowCommandJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.ParseName("Internet Explorer.lnk");
            if (objFolderItem != null)
            {
                var objShellLink;
                
                objShellLink = objFolderItem.GetLink;
                if (objShellLink != null)
                {
                    var nShow;
                    
                    // Get the ShowCommand for the ShellLinkObject.
                    nShow = objShellLink.ShowCommand;
                    alert(nShow);
                    
                    // Set the ShowCommand for the ShellLinkObject.
                    objShellLink.ShowCommand = 1
                }
            }
        }
    }
</script>
```



<span data-ttu-id="78bc2-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="78bc2-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectShowCommandVB()
        dim objShell
        dim objFolder
        dim ssfPROGRAMS
        
        ssfPROGRAMS = 2
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objFolderItem
                
                set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                    if (not objFolderItem is nothing) then
                        dim objShellLink
                        
                        set objShellLink = objFolderItem.GetLink
                            if (not objShellLink is nothing) then
                                dim nShow
                                
                                'Get the ShowCommand for the ShellLinkObject.
                                nShow = objShellLink.ShowCommand
                                alert(nShow)
                                
                                'Set the ShowCommand for the ShellLinkObject.
                                objShellLink.ShowCommand = 1
                            end if
                        set objShellLink = nothing
                    end if
                set objFolderItem = nothing
            end if
        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="78bc2-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="78bc2-121">Visual Basic:</span></span>


```VB
Private Sub fnShellLinkObjectShowCommandVB()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                If (Not objFolderItem Is Nothing) Then
                    Dim objShellLink As ShellLinkObject
                    
                    Set objShellLink = objFolderItem.GetLink
                        If (Not objShellLink Is Nothing) Then
                            Dim nShow As Integer
                            
                            'Get the ShowCommand for the ShellLinkObject.
                            nShow = objShellLink.ShowCommand
                            Debug.Print nShow
                            
                            'Set the ShowCommand for the ShellLinkObject.
                            objShellLink.ShowCommand = 1
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="78bc2-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="78bc2-122">Requirements</span></span>



| <span data-ttu-id="78bc2-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78bc2-123">Requirement</span></span> | <span data-ttu-id="78bc2-124">Wert</span><span class="sxs-lookup"><span data-stu-id="78bc2-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78bc2-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="78bc2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="78bc2-126">Nur Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="78bc2-126">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="78bc2-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="78bc2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="78bc2-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="78bc2-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="78bc2-129">Header</span><span class="sxs-lookup"><span data-stu-id="78bc2-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="78bc2-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="78bc2-130"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="78bc2-131">IDL</span><span class="sxs-lookup"><span data-stu-id="78bc2-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="78bc2-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="78bc2-132"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="78bc2-133">DLL</span><span class="sxs-lookup"><span data-stu-id="78bc2-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78bc2-134"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="78bc2-134"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




