---
description: Synchronisiert alle Offline Dateien im Ordner.
ms.assetid: b149df96-0c8e-47b9-b71e-2ad5dcfdeb8f
title: Folder2. synchronisieren-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2.Synchronize
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e9c39c37ff0e44e58aa71c69496dec8bee2745bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393250"
---
# <a name="folder2synchronize-method"></a><span data-ttu-id="ebace-103">Folder2. synchronisieren-Methode</span><span class="sxs-lookup"><span data-stu-id="ebace-103">Folder2.Synchronize method</span></span>

<span data-ttu-id="ebace-104">Synchronisiert alle Offline Dateien im Ordner.</span><span class="sxs-lookup"><span data-stu-id="ebace-104">Synchronizes all offline files in the folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebace-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ebace-105">Syntax</span></span>


```JScript
iRetVal = Folder2.Synchronize()
```



## <a name="parameters"></a><span data-ttu-id="ebace-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ebace-106">Parameters</span></span>

<span data-ttu-id="ebace-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ebace-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebace-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ebace-108">Remarks</span></span>

<span data-ttu-id="ebace-109">Um diese Methode verwenden zu können, muss das Offlinedateien Feature aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="ebace-109">To use this method, the Offline Files feature must be enabled.</span></span>

## <a name="examples"></a><span data-ttu-id="ebace-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ebace-110">Examples</span></span>

<span data-ttu-id="ebace-111">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung von **Synchronisierung** für JScript, VBScript und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ebace-111">The following example shows the proper use of **Synchronize** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="ebace-112">JScript</span><span class="sxs-lookup"><span data-stu-id="ebace-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnSynchronizeJ()
    {
        var objShell   = new ActiveXObject("shell.application");
        var objFolder2 = new Object;
        
        objFolder2 = objShell.NameSpace("\\\\server\\share\\folder");
        if (objFolder2 != null)
        {
            objFolder2.Synchronize();
        }
    }
</script>
```



<span data-ttu-id="ebace-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="ebace-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnSynchronizeVB()
        dim objShell
        dim objFolder2
       
        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace("\\server\share\folder")

        if (not objFolder2 is nothing) then
            objFolder2.Synchronize
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="ebace-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="ebace-114">Visual Basic:</span></span>


```VB
Private Sub fnSynchronizeVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("\\server\share\folder")

    If (Not objFolder2 Is Nothing) Then
        objFolder2.Synchronize
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="ebace-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ebace-115">Requirements</span></span>



| <span data-ttu-id="ebace-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ebace-116">Requirement</span></span> | <span data-ttu-id="ebace-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ebace-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebace-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ebace-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ebace-119">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ebace-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ebace-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ebace-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ebace-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ebace-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ebace-122">Header</span><span class="sxs-lookup"><span data-stu-id="ebace-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebace-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebace-123"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="ebace-124">IDL</span><span class="sxs-lookup"><span data-stu-id="ebace-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ebace-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ebace-125"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="ebace-126">DLL</span><span class="sxs-lookup"><span data-stu-id="ebace-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebace-127"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="ebace-127"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebace-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ebace-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebace-129">**Folder2**</span><span class="sxs-lookup"><span data-stu-id="ebace-129">**Folder2**</span></span>](folder2-object.md)
</dt> <dt>

[<span data-ttu-id="ebace-130">**Ordner**</span><span class="sxs-lookup"><span data-stu-id="ebace-130">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




