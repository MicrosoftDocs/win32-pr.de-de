---
description: 'Shell.ServiceStop-Methode: Beendet einen benannten Dienst.'
ms.assetid: AC22C91E-BBC6-4a2e-8D39-F9D7C0AC0947
title: Shell.ServiceStop-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ServiceStop
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5307fabe79ab9e634ca1e2815c0b90d59b13b1f6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104158"
---
# <a name="shellservicestop-method"></a><span data-ttu-id="55221-103">Shell.ServiceStop-Methode</span><span class="sxs-lookup"><span data-stu-id="55221-103">Shell.ServiceStop method</span></span>

<span data-ttu-id="55221-104">Beendet einen benannten Dienst.</span><span class="sxs-lookup"><span data-stu-id="55221-104">Stops a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="55221-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="55221-105">Syntax</span></span>


```JScript
retVal = Shell.ServiceStop(
  sServiceName,
  vPersistent
)
```


```VB

Shell.ServiceStop( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="55221-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="55221-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55221-107">*sServiceName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="55221-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55221-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="55221-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="55221-109">Eine **Zeichenfolge,** die den Namen des Diensts enthält.</span><span class="sxs-lookup"><span data-stu-id="55221-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="55221-110">*vPersistent* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="55221-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55221-111">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="55221-111">Type: **Variant**</span></span>

<span data-ttu-id="55221-112">Legen Sie auf **TRUE** fest, damit der Dienst vom Dienststeuerungs-Manager gestartet wird, wenn [**ServiceStart**](./shell-servicestart.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="55221-112">Set to **true** to have the service started by the service control manager when [**ServiceStart**](./shell-servicestart.md) is called.</span></span> <span data-ttu-id="55221-113">Um die Dienstkonfiguration unverändert zu lassen, legen *Sie vPersistent auf* **false fest.**</span><span class="sxs-lookup"><span data-stu-id="55221-113">To leave the service configuration unchanged, set *vPersistent* to **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55221-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="55221-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="55221-115">JScript</span><span class="sxs-lookup"><span data-stu-id="55221-115">JScript</span></span>

<span data-ttu-id="55221-116">Typ: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="55221-116">Type: **Variant\***</span></span>

<span data-ttu-id="55221-117">Gibt **true zurück,** wenn erfolgreich; andernfalls **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="55221-117">Returns **true** if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="55221-118">VB</span><span class="sxs-lookup"><span data-stu-id="55221-118">VB</span></span>

<span data-ttu-id="55221-119">Typ: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="55221-119">Type: **Variant\***</span></span>

<span data-ttu-id="55221-120">Gibt **true zurück,** wenn erfolgreich; andernfalls **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="55221-120">Returns **true** if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="55221-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55221-121">Remarks</span></span>

<span data-ttu-id="55221-122">Die Methode gibt **FALSE zurück,** wenn der Dienst bereits beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="55221-122">The method returns **false** if the service has already been stopped.</span></span> <span data-ttu-id="55221-123">Vor dem Aufrufen dieser Methode können Sie [**Shell.IsServiceRunning**](./shell-isservicerunning.md) aufrufen, um den Status des Diensts zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="55221-123">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="55221-124">Diese Methode ist derzeit in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="55221-124">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="55221-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="55221-125">Examples</span></span>

<span data-ttu-id="55221-126">In den folgenden Beispielen wird die Verwendung von **ServiceStop zum** Beenden des Messenger-Diensts gezeigt.</span><span class="sxs-lookup"><span data-stu-id="55221-126">The following examples show the use of **ServiceStop** to stop the Messenger service.</span></span> <span data-ttu-id="55221-127">Die Verwendung wird für JScript und VBScript angezeigt.</span><span class="sxs-lookup"><span data-stu-id="55221-127">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="55221-128">Jscript:</span><span class="sxs-lookup"><span data-stu-id="55221-128">JScript:</span></span>


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



<span data-ttu-id="55221-129">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="55221-129">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="55221-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55221-130">Requirements</span></span>



| <span data-ttu-id="55221-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55221-131">Requirement</span></span> | <span data-ttu-id="55221-132">Wert</span><span class="sxs-lookup"><span data-stu-id="55221-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55221-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="55221-133">Minimum supported client</span></span><br/> | <span data-ttu-id="55221-134">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55221-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="55221-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="55221-135">Minimum supported server</span></span><br/> | <span data-ttu-id="55221-136">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55221-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="55221-137">Header</span><span class="sxs-lookup"><span data-stu-id="55221-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="55221-138"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="55221-138"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="55221-139">Idl</span><span class="sxs-lookup"><span data-stu-id="55221-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="55221-140"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="55221-140"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="55221-141">DLL</span><span class="sxs-lookup"><span data-stu-id="55221-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55221-142"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="55221-142"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
