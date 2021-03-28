---
description: Gibt an, ob das Element Teil des Dateisystems ist.
ms.assetid: 321a2109-88b5-4a41-9a67-dab3e82e95d8
title: FolderItem. IsFile-Eigenschaft (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.IsFileSystem
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 852f022e1c24fa24c158ee4eb68dca44e6f010a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977057"
---
# <a name="folderitemisfilesystem-property"></a><span data-ttu-id="017f4-103">FolderItem. IsFile-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="017f4-103">FolderItem.IsFileSystem property</span></span>

<span data-ttu-id="017f4-104">Gibt an, ob das Element Teil des Dateisystems ist.</span><span class="sxs-lookup"><span data-stu-id="017f4-104">Indicates if the item is part of the file system.</span></span>

<span data-ttu-id="017f4-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="017f4-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="017f4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="017f4-106">Syntax</span></span>


```JScript
bIsFileSystem = FolderItem.IsFileSystem
```



## <a name="property-value"></a><span data-ttu-id="017f4-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="017f4-107">Property value</span></span>

<span data-ttu-id="017f4-108">Ein **boolescher** Wert, der **true** empfängt, wenn das Element Teil des Dateisystems ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="017f4-108">A **Boolean** that receives **true** if the item is part of the file system or **false** if not.</span></span>

## <a name="examples"></a><span data-ttu-id="017f4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="017f4-109">Examples</span></span>

<span data-ttu-id="017f4-110">Im folgenden Beispiel wird die Verwendung von **IsFile** System verwendet, um zu bestimmen, ob der Windows-Ordner Teil des Dateisystems ist.</span><span class="sxs-lookup"><span data-stu-id="017f4-110">The following example uses **IsFileSystem** to determine whether the Windows folder is a part of the file system.</span></span> <span data-ttu-id="017f4-111">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="017f4-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="017f4-112">JScript</span><span class="sxs-lookup"><span data-stu-id="017f4-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIsFileSystemJ()
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
                
                bReturn = objFolderItem.IsFileSystem;
            }
        }
    }
</script>
```



<span data-ttu-id="017f4-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="017f4-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIsFileSystemVB()
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
                                
                    bReturn = objFolderItem.IsFileSystem
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="017f4-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="017f4-114">Visual Basic:</span></span>


```VB
Private Sub fnIsFileSystemVB()
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
                    
                    bReturn = objFolderItem.IsFileSystem
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



## <a name="requirements"></a><span data-ttu-id="017f4-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="017f4-115">Requirements</span></span>



| <span data-ttu-id="017f4-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="017f4-116">Requirement</span></span> | <span data-ttu-id="017f4-117">Wert</span><span class="sxs-lookup"><span data-stu-id="017f4-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="017f4-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="017f4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="017f4-119">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="017f4-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="017f4-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="017f4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="017f4-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="017f4-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="017f4-122">Header</span><span class="sxs-lookup"><span data-stu-id="017f4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="017f4-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="017f4-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="017f4-124">IDL</span><span class="sxs-lookup"><span data-stu-id="017f4-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="017f4-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="017f4-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="017f4-126">DLL</span><span class="sxs-lookup"><span data-stu-id="017f4-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="017f4-127"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="017f4-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




