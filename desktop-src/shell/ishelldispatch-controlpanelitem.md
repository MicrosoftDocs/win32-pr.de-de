---
description: Führt die angegebene Systemsteuerung aus.
title: IShellDispatch.ControlPanelItem-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.ControlPanelItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9A9B6B3F-FBBC-4e76-8018-8858B6392276
ms.openlocfilehash: 1a1c024b316472be00f119485326b704a4fe8dd0
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842841"
---
# <a name="ishelldispatchcontrolpanelitem-method"></a><span data-ttu-id="2fd02-103">IShellDispatch.ControlPanelItem-Methode</span><span class="sxs-lookup"><span data-stu-id="2fd02-103">IShellDispatch.ControlPanelItem method</span></span>

<span data-ttu-id="2fd02-104">Führt die angegebene Systemsteuerung aus.</span><span class="sxs-lookup"><span data-stu-id="2fd02-104">Runs the specified Control Panel application.</span></span> <span data-ttu-id="2fd02-105">Wenn die Anwendung bereits geöffnet ist, wird die ausgeführte Instanz aktiviert.</span><span class="sxs-lookup"><span data-stu-id="2fd02-105">If the application is already open, it will activate the running instance.</span></span>

> [!Note]  
> <span data-ttu-id="2fd02-106">Ab Windows Vista sind die meisten Systemsteuerung Shell-Elemente und können mit dieser Funktion nicht geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="2fd02-106">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="2fd02-107">Um diese anwendungen Systemsteuerung öffnen, übergeben Sie den kanonischen Namen an control.exe.</span><span class="sxs-lookup"><span data-stu-id="2fd02-107">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="2fd02-108">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="2fd02-108">For example:</span></span>
>
> ``` syntax
> control.exe /name Microsoft.Personalization
> ```

 

## <a name="syntax"></a><span data-ttu-id="2fd02-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2fd02-109">Syntax</span></span>


```JScript
IShellDispatch.ControlPanelItem(
  bstrDir
)
```


```VB

IShellDispatch.ControlPanelItem( _
  ByVal bstrDir As BSTR _
)
```





## <a name="parameters"></a><span data-ttu-id="2fd02-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2fd02-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fd02-111">*bstrDir* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2fd02-111">*bstrDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fd02-112">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="2fd02-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="2fd02-113">Der Systemsteuerung dateiname der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="2fd02-113">The Control Panel application's file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fd02-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2fd02-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="2fd02-115">JScript</span><span class="sxs-lookup"><span data-stu-id="2fd02-115">JScript</span></span>

<span data-ttu-id="2fd02-116">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2fd02-116">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="2fd02-117">VB</span><span class="sxs-lookup"><span data-stu-id="2fd02-117">VB</span></span>

<span data-ttu-id="2fd02-118">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2fd02-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fd02-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2fd02-119">Remarks</span></span>

<span data-ttu-id="2fd02-120">Diese Methode wird implementiert und über die [**Shell.ControlPanelItem-Methode aufgerufen.**](shell-controlpanelitem.md)</span><span class="sxs-lookup"><span data-stu-id="2fd02-120">This method is implemented and accessed through the [**Shell.ControlPanelItem**](shell-controlpanelitem.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="2fd02-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2fd02-121">Examples</span></span>

<span data-ttu-id="2fd02-122">In den folgenden Beispielen [**wird ControlPanelItem**](shell-controlpanelitem.md) verwendet, um das Systemsteuerung **des** Anzeigeeigenschaften ausführen.</span><span class="sxs-lookup"><span data-stu-id="2fd02-122">The following examples use [**ControlPanelItem**](shell-controlpanelitem.md) to run the Control Panel's **Display Properties** item.</span></span> <span data-ttu-id="2fd02-123">Die Verwendung wird für JScript, VBScript und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2fd02-123">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="2fd02-124">Jscript:</span><span class="sxs-lookup"><span data-stu-id="2fd02-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellControlPanelItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Shell_ControlPanelItem("desk.cpl");
    }
</script>
```



<span data-ttu-id="2fd02-125">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="2fd02-125">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellControlPanelItemVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.Shell_ControlPanelItem("desk.cpl")
       
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="2fd02-126">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="2fd02-126">Visual Basic:</span></span>


```VB
Private Sub fnShellControlPanelItemVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.Shell_ControlPanelItem ("desk.cpl")
    
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="2fd02-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2fd02-127">Requirements</span></span>



| <span data-ttu-id="2fd02-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2fd02-128">Requirement</span></span> | <span data-ttu-id="2fd02-129">Wert</span><span class="sxs-lookup"><span data-stu-id="2fd02-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fd02-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2fd02-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2fd02-131">Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2fd02-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2fd02-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2fd02-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2fd02-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2fd02-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2fd02-134">Header</span><span class="sxs-lookup"><span data-stu-id="2fd02-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fd02-135"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="2fd02-135"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="2fd02-136">Idl</span><span class="sxs-lookup"><span data-stu-id="2fd02-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2fd02-137"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="2fd02-137"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="2fd02-138">DLL</span><span class="sxs-lookup"><span data-stu-id="2fd02-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fd02-139"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="2fd02-139"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
