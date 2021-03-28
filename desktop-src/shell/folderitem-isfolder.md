---
description: Gibt an, ob das Element ein Ordner ist.
ms.assetid: fb080c8f-04b1-4f9a-9219-0951a2e950ea
title: FolderItem. isFolder-Eigenschaft (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.IsFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9bf0bd4eb9b7964620fe705d6e8f4d10644ca234
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977056"
---
# <a name="folderitemisfolder-property"></a><span data-ttu-id="ee29b-103">FolderItem. isFolder (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ee29b-103">FolderItem.IsFolder property</span></span>

<span data-ttu-id="ee29b-104">Gibt an, ob das Element ein Ordner ist.</span><span class="sxs-lookup"><span data-stu-id="ee29b-104">Indicates if the item is a folder.</span></span>

<span data-ttu-id="ee29b-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="ee29b-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee29b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee29b-106">Syntax</span></span>


```JScript
bIsFolder = FolderItem.IsFolder
```



## <a name="property-value"></a><span data-ttu-id="ee29b-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ee29b-107">Property value</span></span>

<span data-ttu-id="ee29b-108">Ein **boolescher** Wert, der **true** empfängt, wenn es sich bei dem Element um einen Ordner handelt, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="ee29b-108">A **Boolean** that receives **true** if the item is a folder or **false** if not.</span></span>

## <a name="examples"></a><span data-ttu-id="ee29b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ee29b-109">Examples</span></span>

<span data-ttu-id="ee29b-110">Im folgenden Beispiel wird **isFolder** verwendet, um zu bestimmen, ob das Windows-Verzeichnis ein Ordner ist.</span><span class="sxs-lookup"><span data-stu-id="ee29b-110">The following example uses **IsFolder** to determine whether the Windows directory is a folder.</span></span> <span data-ttu-id="ee29b-111">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ee29b-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="ee29b-112">JScript</span><span class="sxs-lookup"><span data-stu-id="ee29b-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIsFolderJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.Self;
            if (objFolderItem != null)
            {
                var bReturn;
                
                bReturn = objFolderItem.IsFolder;
            }
        }
    }
</script>
```



<span data-ttu-id="ee29b-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="ee29b-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIsFolderVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.Self
                if (not objFolderItem is nothing) then
                    dim bReturn
                                
                    bReturn = objFolderItem.IsFolder
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="ee29b-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="ee29b-114">Visual Basic:</span></span>


```VB
Private Sub fnIsFolderVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.Self
                If (Not objFolderItem Is Nothing) Then
                    Dim bReturn As Boolean
                    
                    bReturn = objFolderItem.IsFolder
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="ee29b-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ee29b-115">Requirements</span></span>



| <span data-ttu-id="ee29b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee29b-116">Requirement</span></span> | <span data-ttu-id="ee29b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ee29b-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee29b-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ee29b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ee29b-119">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ee29b-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ee29b-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ee29b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ee29b-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ee29b-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ee29b-122">Header</span><span class="sxs-lookup"><span data-stu-id="ee29b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee29b-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee29b-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="ee29b-124">IDL</span><span class="sxs-lookup"><span data-stu-id="ee29b-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ee29b-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ee29b-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="ee29b-126">DLL</span><span class="sxs-lookup"><span data-stu-id="ee29b-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee29b-127"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="ee29b-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




