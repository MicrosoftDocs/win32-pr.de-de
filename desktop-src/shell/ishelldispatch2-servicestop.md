---
description: 'IShellDispatch2.ServiceStop-Methode: Beendet einen benannten Dienst.'
ms.assetid: f4cd0e2c-4ecc-4e9f-a0b5-d2a8a739f0e2
title: IShellDispatch2.ServiceStop-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ServiceStop
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 651138eb687cfd83406bc6e1a7fcf520ff001171
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117028"
---
# <a name="ishelldispatch2servicestop-method"></a><span data-ttu-id="5e897-103">IShellDispatch2.ServiceStop-Methode</span><span class="sxs-lookup"><span data-stu-id="5e897-103">IShellDispatch2.ServiceStop method</span></span>

<span data-ttu-id="5e897-104">Beendet einen benannten Dienst.</span><span class="sxs-lookup"><span data-stu-id="5e897-104">Stops a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e897-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e897-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.ServiceStop(
  sServiceName,
  vPersistent
)
```


```VB

IShellDispatch2.ServiceStop( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="5e897-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e897-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e897-107">*sServiceName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5e897-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e897-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="5e897-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="5e897-109">Eine **Zeichenfolge,** die den Namen des Diensts enthält.</span><span class="sxs-lookup"><span data-stu-id="5e897-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="5e897-110">*vPersistent* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5e897-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e897-111">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="5e897-111">Type: **Variant**</span></span>

<span data-ttu-id="5e897-112">Legen Sie auf **TRUE** fest, damit der Dienst vom Dienststeuerungs-Manager gestartet wird, wenn [**ServiceStart**](ishelldispatch2-servicestart.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5e897-112">Set to **true** to have the service started by the service control manager when [**ServiceStart**](ishelldispatch2-servicestart.md) is called.</span></span> <span data-ttu-id="5e897-113">Um die Dienstkonfiguration unverändert zu lassen, legen *Sie vPersistent auf* **false fest.**</span><span class="sxs-lookup"><span data-stu-id="5e897-113">To leave the service configuration unchanged, set *vPersistent* to **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e897-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5e897-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="5e897-115">JScript</span><span class="sxs-lookup"><span data-stu-id="5e897-115">JScript</span></span>

<span data-ttu-id="5e897-116">Typ: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="5e897-116">Type: **Variant\***</span></span>

<span data-ttu-id="5e897-117">Gibt **true zurück,** wenn erfolgreich; andernfalls **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="5e897-117">Returns **true** if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="5e897-118">VB</span><span class="sxs-lookup"><span data-stu-id="5e897-118">VB</span></span>

<span data-ttu-id="5e897-119">Typ: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="5e897-119">Type: **Variant\***</span></span>

<span data-ttu-id="5e897-120">Gibt **true zurück,** wenn erfolgreich; andernfalls **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="5e897-120">Returns **true** if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e897-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5e897-121">Remarks</span></span>

<span data-ttu-id="5e897-122">Diese Methode wird implementiert und über die [**Shell.ServiceStop-Methode**](./shell-servicestop.md) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="5e897-122">This method is implemented and accessed through the [**Shell.ServiceStop**](./shell-servicestop.md) method.</span></span>

<span data-ttu-id="5e897-123">Die Methode gibt **FALSE zurück,** wenn der Dienst bereits beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="5e897-123">The method returns **false** if the service has already been stopped.</span></span> <span data-ttu-id="5e897-124">Vor dem Aufrufen dieser Methode können Sie [**Shell.IsServiceRunning**](./shell-isservicerunning.md) aufrufen, um den Status des Diensts zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="5e897-124">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="5e897-125">Diese Methode ist derzeit in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5e897-125">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="5e897-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e897-126">Examples</span></span>

<span data-ttu-id="5e897-127">In den folgenden Beispielen wird die Verwendung von **ServiceStop zum** Beenden des Messenger-Diensts gezeigt.</span><span class="sxs-lookup"><span data-stu-id="5e897-127">The following examples show the use of **ServiceStop** to stop the Messenger service.</span></span> <span data-ttu-id="5e897-128">Die Verwendung wird für JScript und VBScript angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5e897-128">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="5e897-129">Jscript:</span><span class="sxs-lookup"><span data-stu-id="5e897-129">JScript:</span></span>


```JScript
<script language="JScript">
    function fnServiceStopJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStop("Messenger", true);
    }
</script>
```



<span data-ttu-id="5e897-130">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="5e897-130">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnServiceStopVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ServiceStop("Messenger", true)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="5e897-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e897-131">Requirements</span></span>



| <span data-ttu-id="5e897-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e897-132">Requirement</span></span> | <span data-ttu-id="5e897-133">Wert</span><span class="sxs-lookup"><span data-stu-id="5e897-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e897-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5e897-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5e897-135">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5e897-135">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5e897-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5e897-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5e897-137">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5e897-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="5e897-138">Header</span><span class="sxs-lookup"><span data-stu-id="5e897-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e897-139"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="5e897-139"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="5e897-140">Idl</span><span class="sxs-lookup"><span data-stu-id="5e897-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5e897-141"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="5e897-141"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="5e897-142">DLL</span><span class="sxs-lookup"><span data-stu-id="5e897-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e897-143"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="5e897-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
