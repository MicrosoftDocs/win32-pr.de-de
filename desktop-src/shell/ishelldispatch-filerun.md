---
description: Zeigt das Dialogfeld "ausführen" für den Benutzer an.
ms.assetid: BC7C4C26-593D-4467-A2AA-4F2DF835C989
title: Ishelldispatch. filerun-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.FileRun
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 56806edf06d334d90ad038886d955c00876f8f0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753096"
---
# <a name="ishelldispatchfilerun-method"></a><span data-ttu-id="67d0d-103">Ishelldispatch. filerun-Methode</span><span class="sxs-lookup"><span data-stu-id="67d0d-103">IShellDispatch.FileRun method</span></span>

<span data-ttu-id="67d0d-104">Zeigt das Dialogfeld " **Ausführen** " für den Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="67d0d-104">Displays the **Run** dialog to the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="67d0d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="67d0d-105">Syntax</span></span>


```JScript
IShellDispatch.FileRun()
```


```VB

IShellDispatch.FileRun()
```





## <a name="parameters"></a><span data-ttu-id="67d0d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="67d0d-106">Parameters</span></span>

<span data-ttu-id="67d0d-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="67d0d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="67d0d-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="67d0d-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="67d0d-109">JScript</span><span class="sxs-lookup"><span data-stu-id="67d0d-109">JScript</span></span>

<span data-ttu-id="67d0d-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="67d0d-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="67d0d-111">VB</span><span class="sxs-lookup"><span data-stu-id="67d0d-111">VB</span></span>

<span data-ttu-id="67d0d-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="67d0d-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="67d0d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67d0d-113">Remarks</span></span>

<span data-ttu-id="67d0d-114">Diese Methode wird implementiert und über die [**Shell. filerun-**](shell-filerun.md) Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="67d0d-114">This method is implemented and accessed through the [**Shell.FileRun**](shell-filerun.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="67d0d-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="67d0d-115">Examples</span></span>

<span data-ttu-id="67d0d-116">In den folgenden Beispielen wird die Verwendung von **filerun** in JScript, VBScript und Visual Basic veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="67d0d-116">The following examples show the use of **FileRun** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="67d0d-117">JScript</span><span class="sxs-lookup"><span data-stu-id="67d0d-117">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFileRunJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.FileRun();
    }
</script>
```



<span data-ttu-id="67d0d-118">VBScript</span><span class="sxs-lookup"><span data-stu-id="67d0d-118">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellFileRunVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.FileRun

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="67d0d-119">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="67d0d-119">Visual Basic:</span></span>


```VB
Private Sub fnShellFileRunVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.FileRun

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="67d0d-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="67d0d-120">Requirements</span></span>



| <span data-ttu-id="67d0d-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67d0d-121">Requirement</span></span> | <span data-ttu-id="67d0d-122">Wert</span><span class="sxs-lookup"><span data-stu-id="67d0d-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67d0d-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="67d0d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="67d0d-124">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67d0d-124">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="67d0d-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="67d0d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="67d0d-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67d0d-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="67d0d-127">Header</span><span class="sxs-lookup"><span data-stu-id="67d0d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="67d0d-128"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="67d0d-128"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="67d0d-129">IDL</span><span class="sxs-lookup"><span data-stu-id="67d0d-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="67d0d-130"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="67d0d-130"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="67d0d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="67d0d-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67d0d-132"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="67d0d-132"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




