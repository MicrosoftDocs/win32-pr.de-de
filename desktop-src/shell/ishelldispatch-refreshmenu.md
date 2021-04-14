---
description: Aktualisiert den Inhalt des Start Menüs. Wird nur mit Systemen vor Windows XP verwendet.
ms.assetid: D36FA5A0-AF03-4627-86E0-869BF1440958
title: Ishelldispatch. erfrischend Menu-Methode (Shldisp. h)
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
ms.openlocfilehash: 98728ef48ffb9ef4383cf9ba567606758b7a015c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978096"
---
# <a name="ishelldispatchrefreshmenu-method"></a><span data-ttu-id="daa81-104">Ishelldispatch. erfrischend Menu-Methode</span><span class="sxs-lookup"><span data-stu-id="daa81-104">IShellDispatch.RefreshMenu method</span></span>

<span data-ttu-id="daa81-105">Aktualisiert den Inhalt des **Start** Menüs.</span><span class="sxs-lookup"><span data-stu-id="daa81-105">Refreshes the contents of the **Start** menu.</span></span> <span data-ttu-id="daa81-106">Wird nur mit Systemen vor Windows XP verwendet.</span><span class="sxs-lookup"><span data-stu-id="daa81-106">Used only with systems preceding Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="daa81-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="daa81-107">Syntax</span></span>


```JScript
IShellDispatch.RefreshMenu()
```


```VB

IShellDispatch.RefreshMenu()
```





## <a name="parameters"></a><span data-ttu-id="daa81-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="daa81-108">Parameters</span></span>

<span data-ttu-id="daa81-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="daa81-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="daa81-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="daa81-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="daa81-111">JScript</span><span class="sxs-lookup"><span data-stu-id="daa81-111">JScript</span></span>

<span data-ttu-id="daa81-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="daa81-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="daa81-113">VB</span><span class="sxs-lookup"><span data-stu-id="daa81-113">VB</span></span>

<span data-ttu-id="daa81-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="daa81-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="daa81-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="daa81-115">Remarks</span></span>

<span data-ttu-id="daa81-116">Diese Methode ist implementiert, und der Zugriff erfolgt über die [**Shell. trayproperties**](shell-trayproperties.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="daa81-116">This method is implemented and accessed through the [**Shell.TrayProperties**](shell-trayproperties.md) method.</span></span>

<span data-ttu-id="daa81-117">Die Funktionalität, die das Aktualitäts **Menü** bereitstellt, wird automatisch unter Windows XP oder höher behandelt.</span><span class="sxs-lookup"><span data-stu-id="daa81-117">The functionality that **RefreshMenu** provides is handled automatically under Windows XP or later.</span></span> <span data-ttu-id="daa81-118">Diese Methode darf nicht unter Windows XP oder höher aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="daa81-118">Do not call this method on Windows XP or later.</span></span>

## <a name="examples"></a><span data-ttu-id="daa81-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="daa81-119">Examples</span></span>

<span data-ttu-id="daa81-120">In den folgenden Beispielen wird die Verwendung des **aktuerfrischenden Menüs** in JScript, VBScript und Visual Basic veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="daa81-120">The following examples show the use of **RefreshMenu** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="daa81-121">JScript</span><span class="sxs-lookup"><span data-stu-id="daa81-121">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellRefreshMenuJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.RefreshMenu();
    }
</script>
```



<span data-ttu-id="daa81-122">VBScript</span><span class="sxs-lookup"><span data-stu-id="daa81-122">VBScript:</span></span>


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



<span data-ttu-id="daa81-123">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="daa81-123">Visual Basic:</span></span>


```VB
Private Sub fnShellRefreshMenuVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.RefreshMenu

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="daa81-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="daa81-124">Requirements</span></span>



| <span data-ttu-id="daa81-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="daa81-125">Requirement</span></span> | <span data-ttu-id="daa81-126">Wert</span><span class="sxs-lookup"><span data-stu-id="daa81-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="daa81-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="daa81-127">Minimum supported client</span></span><br/> | <span data-ttu-id="daa81-128">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="daa81-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="daa81-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="daa81-129">Minimum supported server</span></span><br/> | <span data-ttu-id="daa81-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="daa81-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="daa81-131">Header</span><span class="sxs-lookup"><span data-stu-id="daa81-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="daa81-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="daa81-132"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="daa81-133">IDL</span><span class="sxs-lookup"><span data-stu-id="daa81-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="daa81-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="daa81-134"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="daa81-135">DLL</span><span class="sxs-lookup"><span data-stu-id="daa81-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="daa81-136"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="daa81-136"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




