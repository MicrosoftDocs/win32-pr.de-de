---
description: Ruft das im Link angegebene Arbeitsverzeichnis ab oder legt es fest.
ms.assetid: c3820deb-9f00-42a9-ab0e-c0f6389e9f29
title: Shelllinkobject. WorkingDirectory-Eigenschaft (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.WorkingDirectory
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d8788899a06179056cd871b68e4e64566bcd5ee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346128"
---
# <a name="shelllinkobjectworkingdirectory-property"></a><span data-ttu-id="44515-103">Shelllinkobject. WorkingDirectory-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="44515-103">ShellLinkObject.WorkingDirectory property</span></span>

<span data-ttu-id="44515-104">Ruft das im Link angegebene Arbeitsverzeichnis ab oder legt es fest.</span><span class="sxs-lookup"><span data-stu-id="44515-104">Gets or sets the working directory specified in the link.</span></span>

<span data-ttu-id="44515-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="44515-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="44515-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="44515-106">Syntax</span></span>


```JScript
strWorkingDirectory = ShellLinkObject.WorkingDirectory
ShellLinkObject.WorkingDirectory(sWorkingDirectory) = strWorkingDirectory
```



## <a name="property-value"></a><span data-ttu-id="44515-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="44515-107">Property value</span></span>

<span data-ttu-id="44515-108">der voll qualifizierte Pfad des Arbeitsverzeichnisses des Links.</span><span class="sxs-lookup"><span data-stu-id="44515-108">the fully qualified path of the link's working directory.</span></span>

## <a name="examples"></a><span data-ttu-id="44515-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="44515-109">Examples</span></span>

<span data-ttu-id="44515-110">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Eigenschaft in JScript, VBScript und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="44515-110">The following example shows the proper usage of this property in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="44515-111">JScript</span><span class="sxs-lookup"><span data-stu-id="44515-111">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShellLinkObjectWorkingDirectoryJ()
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
                    var szDirectory;
                    
                    // Get the working directory for the ShellLinkObject.
                    szDirectory = objShellLink.WorkingDirectory;
                    alert(szDirectory);
                    
                    // Set the working directory for the ShellLinkObject.
                    objShellLink.WorkingDirectory = "";
                }
            }
        }
    }
</script>
```



<span data-ttu-id="44515-112">VBScript</span><span class="sxs-lookup"><span data-stu-id="44515-112">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectWorkingDirectoryVB()
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
                                dim szDirectory
                                
                                'Get the working directory.
                                szDirectory = objShellLink.WorkingDirectory
                                alert(szDirectory)
                                
                                'Set the working directory.
                                objShellLink.WorkingDirectory = ""
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



<span data-ttu-id="44515-113">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="44515-113">Visual Basic:</span></span>


```VB
Private Sub fnShellLinkObjectWorkingDirectoryVB()
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
                            Dim szDirectory As String
                            
                            'Get the working directory.
                            szDirectory = objShellLink.WorkingDirectory
                            Debug.Print szDirectory
                            
                            'Set the working directory.
                            objShellLink.WorkingDirectory = ""
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
```



## <a name="requirements"></a><span data-ttu-id="44515-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="44515-114">Requirements</span></span>



| <span data-ttu-id="44515-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44515-115">Requirement</span></span> | <span data-ttu-id="44515-116">Wert</span><span class="sxs-lookup"><span data-stu-id="44515-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44515-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="44515-117">Minimum supported client</span></span><br/> | <span data-ttu-id="44515-118">Nur Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44515-118">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="44515-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="44515-119">Minimum supported server</span></span><br/> | <span data-ttu-id="44515-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44515-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="44515-121">Header</span><span class="sxs-lookup"><span data-stu-id="44515-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="44515-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="44515-122"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="44515-123">IDL</span><span class="sxs-lookup"><span data-stu-id="44515-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="44515-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="44515-124"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="44515-125">DLL</span><span class="sxs-lookup"><span data-stu-id="44515-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44515-126"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="44515-126"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




