---
description: Erfahren Sie mehr über die IShellDispatch.RefreshMenu-Methode, die den Inhalt der Startmenü aktualisiert. Wird nur mit Systemen vor Windows XP verwendet.
ms.assetid: D36FA5A0-AF03-4627-86E0-869BF1440958
title: IShellDispatch.RefreshMenu-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.RefreshMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d9e1a3c326cfa79c7b754cc8a364e649cf2c9931
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404673"
---
# <a name="ishelldispatchrefreshmenu-method"></a><span data-ttu-id="e1ba3-104">IShellDispatch.RefreshMenu-Methode</span><span class="sxs-lookup"><span data-stu-id="e1ba3-104">IShellDispatch.RefreshMenu method</span></span>

<span data-ttu-id="e1ba3-105">Aktualisiert den Inhalt  des Startmenüs.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-105">Refreshes the contents of the **Start** menu.</span></span> <span data-ttu-id="e1ba3-106">Wird nur mit Systemen vor Windows XP verwendet.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-106">Used only with systems preceding Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1ba3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1ba3-107">Syntax</span></span>


```JScript
IShellDispatch.RefreshMenu()
```


```VB

IShellDispatch.RefreshMenu()
```





## <a name="parameters"></a><span data-ttu-id="e1ba3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1ba3-108">Parameters</span></span>

<span data-ttu-id="e1ba3-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e1ba3-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e1ba3-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="e1ba3-111">JScript</span><span class="sxs-lookup"><span data-stu-id="e1ba3-111">JScript</span></span>

<span data-ttu-id="e1ba3-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="e1ba3-113">VB</span><span class="sxs-lookup"><span data-stu-id="e1ba3-113">VB</span></span>

<span data-ttu-id="e1ba3-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1ba3-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e1ba3-115">Remarks</span></span>

<span data-ttu-id="e1ba3-116">Diese Methode wird implementiert und über die [**Shell.TrayProperties-Methode**](shell-trayproperties.md) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-116">This method is implemented and accessed through the [**Shell.TrayProperties**](shell-trayproperties.md) method.</span></span>

<span data-ttu-id="e1ba3-117">Die funktionen, die **RefreshMenu** bereitstellt, werden automatisch unter Windows XP oder höher verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-117">The functionality that **RefreshMenu** provides is handled automatically under Windows XP or later.</span></span> <span data-ttu-id="e1ba3-118">Rufen Sie diese Methode nicht unter Windows XP oder höher auf.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-118">Do not call this method on Windows XP or later.</span></span>

## <a name="examples"></a><span data-ttu-id="e1ba3-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e1ba3-119">Examples</span></span>

<span data-ttu-id="e1ba3-120">Die folgenden Beispiele zeigen die Verwendung von **RefreshMenu** in JScript, VBScript und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-120">The following examples show the use of **RefreshMenu** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="e1ba3-121">Jscript:</span><span class="sxs-lookup"><span data-stu-id="e1ba3-121">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellRefreshMenuJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.RefreshMenu();
    }
</script>
```



<span data-ttu-id="e1ba3-122">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="e1ba3-122">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellRefreshMenuVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.RefreshMenu

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="e1ba3-123">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="e1ba3-123">Visual Basic:</span></span>


```VB
Private Sub fnShellRefreshMenuVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.RefreshMenu

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="e1ba3-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="e1ba3-124">Requirements</span></span>



| <span data-ttu-id="e1ba3-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e1ba3-125">Requirement</span></span> | <span data-ttu-id="e1ba3-126">Wert</span><span class="sxs-lookup"><span data-stu-id="e1ba3-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1ba3-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e1ba3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e1ba3-128">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e1ba3-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e1ba3-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e1ba3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e1ba3-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e1ba3-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e1ba3-131">Header</span><span class="sxs-lookup"><span data-stu-id="e1ba3-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1ba3-132"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="e1ba3-132"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="e1ba3-133">Idl</span><span class="sxs-lookup"><span data-stu-id="e1ba3-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e1ba3-134"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="e1ba3-134"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="e1ba3-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e1ba3-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1ba3-136"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="e1ba3-136"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




