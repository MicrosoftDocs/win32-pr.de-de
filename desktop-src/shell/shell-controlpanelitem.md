---
description: Führt die angegebene System Steuerungs \* Anwendung (. cpl) aus.
title: Shell. controlpanelitem-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ControlPanelItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 54979bbd-b36b-4b5b-a8a0-5f63e9526fa5
ms.openlocfilehash: dec27dab8bd37cc9c15e603c24a54d528cea331a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979913"
---
# <a name="shellcontrolpanelitem-method"></a><span data-ttu-id="b317e-103">Shell. controlpanelitem-Methode</span><span class="sxs-lookup"><span data-stu-id="b317e-103">Shell.ControlPanelItem method</span></span>

<span data-ttu-id="b317e-104">Führt die angegebene System Steuerungs \* Anwendung (. cpl) aus.</span><span class="sxs-lookup"><span data-stu-id="b317e-104">Runs the specified Control Panel (\*.cpl) application.</span></span> <span data-ttu-id="b317e-105">Wenn die Anwendung bereits geöffnet ist, wird die laufende Instanz aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b317e-105">If the application is already open, it will activate the running instance.</span></span>

> [!Note]  
> <span data-ttu-id="b317e-106">Ab Windows Vista sind die meisten System Steuerungsanwendungen shellelemente und können nicht mit dieser Funktion geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="b317e-106">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="b317e-107">Wenn Sie diese System Steuerungsanwendungen öffnen möchten, übergeben Sie den kanonischen Namen an control.exe.</span><span class="sxs-lookup"><span data-stu-id="b317e-107">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="b317e-108">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="b317e-108">For example:</span></span>
>
> ``` syntax
> control.exe /name Microsoft.Personalization
> ```

 

## <a name="syntax"></a><span data-ttu-id="b317e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b317e-109">Syntax</span></span>


```JScript
Shell.ControlPanelItem(
  bstrDir
)
```


```VB

Shell.ControlPanelItem( _
  ByVal bstrDir As BSTR _
)
```





## <a name="parameters"></a><span data-ttu-id="b317e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b317e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b317e-111">*bstrindir* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b317e-111">*bstrDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b317e-112">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="b317e-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="b317e-113">Der Dateiname der System Steuerungsanwendung.</span><span class="sxs-lookup"><span data-stu-id="b317e-113">The Control Panel application's file name.</span></span> <span data-ttu-id="b317e-114">Alle System Steuerungsanwendungen haben die Erweiterung. cpl.</span><span class="sxs-lookup"><span data-stu-id="b317e-114">All Control Panel applications have the .cpl extension.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b317e-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b317e-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="b317e-116">JScript</span><span class="sxs-lookup"><span data-stu-id="b317e-116">JScript</span></span>

<span data-ttu-id="b317e-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b317e-117">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="b317e-118">VB</span><span class="sxs-lookup"><span data-stu-id="b317e-118">VB</span></span>

<span data-ttu-id="b317e-119">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b317e-119">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="b317e-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b317e-120">Examples</span></span>

<span data-ttu-id="b317e-121">Im folgenden Beispiel wird **controlpanelitem** verwendet, um das Element **Anzeigeeigenschaften** der Systemsteuerung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="b317e-121">The following example uses **ControlPanelItem** to run the Control Panel's **Display Properties** item.</span></span> <span data-ttu-id="b317e-122">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b317e-122">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="b317e-123">JScript</span><span class="sxs-lookup"><span data-stu-id="b317e-123">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellControlPanelItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ControlPanelItem("desk.cpl");
    }
</script>
```



<span data-ttu-id="b317e-124">VBScript</span><span class="sxs-lookup"><span data-stu-id="b317e-124">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellControlPanelItemVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.ControlPanelItem("desk.cpl")
       
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="b317e-125">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="b317e-125">Visual Basic:</span></span>


```VB
Private Sub fnShellControlPanelItemVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.ControlPanelItem ("desk.cpl")
    
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="b317e-126">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b317e-126">Requirements</span></span>



| <span data-ttu-id="b317e-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b317e-127">Requirement</span></span> | <span data-ttu-id="b317e-128">Wert</span><span class="sxs-lookup"><span data-stu-id="b317e-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b317e-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b317e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b317e-130">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b317e-130">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b317e-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b317e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b317e-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b317e-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b317e-133">Header</span><span class="sxs-lookup"><span data-stu-id="b317e-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b317e-134"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b317e-134"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b317e-135">IDL</span><span class="sxs-lookup"><span data-stu-id="b317e-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b317e-136"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b317e-136"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b317e-137">DLL</span><span class="sxs-lookup"><span data-stu-id="b317e-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b317e-138"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="b317e-138"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
