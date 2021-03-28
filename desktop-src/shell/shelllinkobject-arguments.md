---
description: Enthält die Argumente eines Links.
ms.assetid: 938db958-4b59-4dd6-ac56-f21db05ec989
title: Shelllinkobject. Arguments-Eigenschaft (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.Arguments
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c9b8a32eb4b935b5164ef91bf299777b36d7e53d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217687"
---
# <a name="shelllinkobjectarguments-property"></a><span data-ttu-id="dec2c-103">Shelllinkobject. Arguments (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="dec2c-103">ShellLinkObject.Arguments property</span></span>

<span data-ttu-id="dec2c-104">Enthält die Argumente eines Links.</span><span class="sxs-lookup"><span data-stu-id="dec2c-104">Contains a link's arguments.</span></span>

<span data-ttu-id="dec2c-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="dec2c-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="dec2c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="dec2c-106">Syntax</span></span>


```JScript
strArguments = ShellLinkObject.Arguments
ShellLinkObject.Arguments(sArguments) = strArguments
```



## <a name="property-value"></a><span data-ttu-id="dec2c-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="dec2c-107">Property value</span></span>

<span data-ttu-id="dec2c-108">die Argumente des Links.</span><span class="sxs-lookup"><span data-stu-id="dec2c-108">the link's arguments.</span></span>

## <a name="examples"></a><span data-ttu-id="dec2c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dec2c-109">Examples</span></span>

<span data-ttu-id="dec2c-110">Im folgenden Beispiel werden **Argumente** zum Abrufen der Argumente für einen Link zu Internet Explorer im Startmenü des Benutzers verwendet.</span><span class="sxs-lookup"><span data-stu-id="dec2c-110">The following example uses **Arguments** to retrieve the arguments for a link to Internet Explorer found in the user's Start menu.</span></span> <span data-ttu-id="dec2c-111">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dec2c-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="dec2c-112">JScript</span><span class="sxs-lookup"><span data-stu-id="dec2c-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShellLinkObjectArgumentJ()
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
                    var szArguments;
                    
                    // Get the arguments for the ShellLinkObject
                    szArguments = objShellLink.Arguments;
                    alert(szArguments);
                    
                    // Set the arguments for the ShellLinkObject
                    objShellLink.Arguments = "/s"
                }
            }
        }
    }
</script>
```



<span data-ttu-id="dec2c-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="dec2c-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectArgumentVB()
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
                    dim szArguments
                    
                    'Get the arguments for the ShellLinkObject
                    szArguments = objShellLink.Arguments
                    alert(szArguments)
                    
                    'Set the arguments for the ShellLinkObject
                    objShellLink.Arguments = "/s"
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



<span data-ttu-id="dec2c-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="dec2c-114">Visual Basic:</span></span>


```VB
Private Sub fnShellLinkObjectArgumentsVB()
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
                    Dim szArguments As String
                    
                    'Get the arguments for the ShellLinkObject
                    szArguments = objShellLink.Arguments
                    Debug.Print szArguments
                    
                    'Set the arguments for the ShellLinkObject
                    objShellLink.Arguments = "/s"
                End If

                Set objShellLink = Nothing
            End If

            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="dec2c-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="dec2c-115">Requirements</span></span>



| <span data-ttu-id="dec2c-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dec2c-116">Requirement</span></span> | <span data-ttu-id="dec2c-117">Wert</span><span class="sxs-lookup"><span data-stu-id="dec2c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dec2c-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dec2c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dec2c-119">Nur Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dec2c-119">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="dec2c-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dec2c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dec2c-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dec2c-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="dec2c-122">Header</span><span class="sxs-lookup"><span data-stu-id="dec2c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="dec2c-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="dec2c-123"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="dec2c-124">IDL</span><span class="sxs-lookup"><span data-stu-id="dec2c-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dec2c-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dec2c-125"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="dec2c-126">DLL</span><span class="sxs-lookup"><span data-stu-id="dec2c-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dec2c-127"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="dec2c-127"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




