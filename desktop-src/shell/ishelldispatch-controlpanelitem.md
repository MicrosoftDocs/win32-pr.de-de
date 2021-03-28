---
description: Führt die angegebene System Steuerungsanwendung aus.
title: Ishelldispatch. controlpanelitem-Methode (Shldisp. h)
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
ms.openlocfilehash: 72164ff76cbcf15703bc91160e6211b38015f989
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527353"
---
# <a name="ishelldispatchcontrolpanelitem-method"></a><span data-ttu-id="fa5dd-103">Ishelldispatch. controlpanelitem-Methode</span><span class="sxs-lookup"><span data-stu-id="fa5dd-103">IShellDispatch.ControlPanelItem method</span></span>

<span data-ttu-id="fa5dd-104">Führt die angegebene System Steuerungsanwendung aus.</span><span class="sxs-lookup"><span data-stu-id="fa5dd-104">Runs the specified Control Panel application.</span></span> <span data-ttu-id="fa5dd-105">Wenn die Anwendung bereits geöffnet ist, wird die laufende Instanz aktiviert.</span><span class="sxs-lookup"><span data-stu-id="fa5dd-105">If the application is already open, it will activate the running instance.</span></span>

> [!Note]  
> <span data-ttu-id="fa5dd-106">Ab Windows Vista sind die meisten System Steuerungsanwendungen shellelemente und können nicht mit dieser Funktion geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="fa5dd-106">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="fa5dd-107">Wenn Sie diese System Steuerungsanwendungen öffnen möchten, übergeben Sie den kanonischen Namen an control.exe.</span><span class="sxs-lookup"><span data-stu-id="fa5dd-107">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="fa5dd-108">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="fa5dd-108">For example:</span></span>
>
> ``` syntax
> control.exe /name Microsoft.Personalization
> ```

 

## <a name="syntax"></a><span data-ttu-id="fa5dd-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa5dd-109">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="fa5dd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa5dd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa5dd-111">*bstrindir* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fa5dd-111">*bstrDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa5dd-112">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="fa5dd-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="fa5dd-113">Der Dateiname der System Steuerungsanwendung.</span><span class="sxs-lookup"><span data-stu-id="fa5dd-113">The Control Panel application's file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa5dd-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fa5dd-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="fa5dd-115">JScript</span><span class="sxs-lookup"><span data-stu-id="fa5dd-115">JScript</span></span>

<span data-ttu-id="fa5dd-116">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fa5dd-116">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="fa5dd-117">VB</span><span class="sxs-lookup"><span data-stu-id="fa5dd-117">VB</span></span>

<span data-ttu-id="fa5dd-118">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fa5dd-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa5dd-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fa5dd-119">Remarks</span></span>

<span data-ttu-id="fa5dd-120">Diese Methode wird implementiert und über die [**Shell. controlpanelitem**](shell-controlpanelitem.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="fa5dd-120">This method is implemented and accessed through the [**Shell.ControlPanelItem**](shell-controlpanelitem.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="fa5dd-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fa5dd-121">Examples</span></span>

<span data-ttu-id="fa5dd-122">In den folgenden Beispielen wird [**controlpanelitem**](shell-controlpanelitem.md) verwendet, um das Element **Anzeigeeigenschaften** der Systemsteuerung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="fa5dd-122">The following examples use [**ControlPanelItem**](shell-controlpanelitem.md) to run the Control Panel's **Display Properties** item.</span></span> <span data-ttu-id="fa5dd-123">Die Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fa5dd-123">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="fa5dd-124">JScript</span><span class="sxs-lookup"><span data-stu-id="fa5dd-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellControlPanelItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Shell_ControlPanelItem("desk.cpl");
    }
</script>
```



<span data-ttu-id="fa5dd-125">VBScript</span><span class="sxs-lookup"><span data-stu-id="fa5dd-125">VBScript:</span></span>


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



<span data-ttu-id="fa5dd-126">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="fa5dd-126">Visual Basic:</span></span>


```VB
Private Sub fnShellControlPanelItemVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.Shell_ControlPanelItem ("desk.cpl")
    
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="fa5dd-127">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="fa5dd-127">Requirements</span></span>



| <span data-ttu-id="fa5dd-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fa5dd-128">Requirement</span></span> | <span data-ttu-id="fa5dd-129">Wert</span><span class="sxs-lookup"><span data-stu-id="fa5dd-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa5dd-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fa5dd-130">Minimum supported client</span></span><br/> | <span data-ttu-id="fa5dd-131">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fa5dd-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fa5dd-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fa5dd-132">Minimum supported server</span></span><br/> | <span data-ttu-id="fa5dd-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fa5dd-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fa5dd-134">Header</span><span class="sxs-lookup"><span data-stu-id="fa5dd-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa5dd-135"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa5dd-135"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="fa5dd-136">IDL</span><span class="sxs-lookup"><span data-stu-id="fa5dd-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fa5dd-137"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fa5dd-137"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="fa5dd-138">DLL</span><span class="sxs-lookup"><span data-stu-id="fa5dd-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa5dd-139"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="fa5dd-139"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
