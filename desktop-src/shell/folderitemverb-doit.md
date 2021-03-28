---
description: Führt ein Verb für das folderItem-Element aus, das dem Verb zugeordnet ist.
ms.assetid: 92400fe9-e4d1-4bc9-b4ee-d2adaf38154f
title: Folderitemverb. doit-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItemVerb.DoIt
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 0703b9403dfe9ff6600de68aaa710cd5a55c225a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977001"
---
# <a name="folderitemverbdoit-method"></a><span data-ttu-id="36950-103">Folderitemverb. doit-Methode</span><span class="sxs-lookup"><span data-stu-id="36950-103">FolderItemVerb.DoIt method</span></span>

<span data-ttu-id="36950-104">Führt ein Verb für das [**folderItem**](folderitem.md) -Element aus, das dem Verb zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="36950-104">Executes a verb on the [**FolderItem**](folderitem.md) associated with the verb.</span></span>

## <a name="syntax"></a><span data-ttu-id="36950-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="36950-105">Syntax</span></span>


```JScript
FolderItemVerb.DoIt()
```



## <a name="parameters"></a><span data-ttu-id="36950-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="36950-106">Parameters</span></span>

<span data-ttu-id="36950-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="36950-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="36950-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="36950-108">Return value</span></span>

<span data-ttu-id="36950-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="36950-109">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="36950-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="36950-110">Examples</span></span>

<span data-ttu-id="36950-111">Im folgenden Beispiel wird **doit** verwendet, um das erste Verb in der Auflistung von Verben auszuführen, auf die der Programmordner des Benutzers antwortet.</span><span class="sxs-lookup"><span data-stu-id="36950-111">The following example uses **DoIt** to execute the first verb in the collection of verbs to which the user's Program folder responds.</span></span> <span data-ttu-id="36950-112">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="36950-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="36950-113">JScript</span><span class="sxs-lookup"><span data-stu-id="36950-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemVerbDoItJ()
    {
        var objShell    = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objVerbs;
            
            objVerbs = objFolder.Self.Verbs();
            if (objVerbs != null)
            {
                objVerbs.Item(0).DoIt();
            }
        }
    }
</script>
```



<span data-ttu-id="36950-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="36950-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemVerbDoItVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfPROGRAMS
            
            ssfPROGRAMS = 2
            set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objVerbs
                
                set objVerbs = objFolder.Self.Verbs
                    if (not objVerbs is nothing) then
                        objVerbs.Item(0).DoIt
                    end if
                set objVerbs = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="36950-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="36950-115">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemVerbDoItVB()
    Dim objShell    As Shell
    Dim objFolder2  As Folder2
    Dim ssfPROGRAMS As Long
            
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfPROGRAMS)
    If (Not objFolder2 Is Nothing) Then
        Dim objVerbs As FolderItemVerbs
        
        Set objVerbs = objFolder2.Self.Verbs
            If (Not objVerbs Is Nothing) Then
                objVerbs.Item(0).DoIt
            End If
        Set objVerbs = Nothing
    End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="36950-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="36950-116">Requirements</span></span>



| <span data-ttu-id="36950-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="36950-117">Requirement</span></span> | <span data-ttu-id="36950-118">Wert</span><span class="sxs-lookup"><span data-stu-id="36950-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36950-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="36950-119">Minimum supported client</span></span><br/> | <span data-ttu-id="36950-120">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36950-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="36950-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="36950-121">Minimum supported server</span></span><br/> | <span data-ttu-id="36950-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36950-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="36950-123">Header</span><span class="sxs-lookup"><span data-stu-id="36950-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="36950-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="36950-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="36950-125">IDL</span><span class="sxs-lookup"><span data-stu-id="36950-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="36950-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="36950-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="36950-127">DLL</span><span class="sxs-lookup"><span data-stu-id="36950-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36950-128"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="36950-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




