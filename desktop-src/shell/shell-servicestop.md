---
description: Beendet einen benannten Dienst.
ms.assetid: AC22C91E-BBC6-4a2e-8D39-F9D7C0AC0947
title: Shell. servicestop-Methode (Shldisp. h)
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
ms.openlocfilehash: 31388078fe1c0e15c2e54efc86f0ff76bcfb7ed2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216600"
---
# <a name="shellservicestop-method"></a><span data-ttu-id="cf97b-103">Shell. servicestop-Methode</span><span class="sxs-lookup"><span data-stu-id="cf97b-103">Shell.ServiceStop method</span></span>

<span data-ttu-id="cf97b-104">Beendet einen benannten Dienst.</span><span class="sxs-lookup"><span data-stu-id="cf97b-104">Stops a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf97b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf97b-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="cf97b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf97b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf97b-107">*sservicename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf97b-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf97b-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="cf97b-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="cf97b-109">Eine **Zeichenfolge** , die den Namen des Dienstanbieter enthält.</span><span class="sxs-lookup"><span data-stu-id="cf97b-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="cf97b-110">*vpersistent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf97b-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf97b-111">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="cf97b-111">Type: **Variant**</span></span>

<span data-ttu-id="cf97b-112">Legen Sie diese Einstellung auf **true** fest, damit der Dienst vom Dienststeuerungs-Manager gestartet wird, wenn [**Servicestart**](./shell-servicestart.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="cf97b-112">Set to **true** to have the service started by the service control manager when [**ServiceStart**](./shell-servicestart.md) is called.</span></span> <span data-ttu-id="cf97b-113">Legen Sie *vpersistenz* auf **false** fest, um die Dienst Konfiguration unverändert zu lassen.</span><span class="sxs-lookup"><span data-stu-id="cf97b-113">To leave the service configuration unchanged, set *vPersistent* to **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf97b-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf97b-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="cf97b-115">JScript</span><span class="sxs-lookup"><span data-stu-id="cf97b-115">JScript</span></span>

<span data-ttu-id="cf97b-116">Typ: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="cf97b-116">Type: \**Variant\** _</span></span>

<span data-ttu-id="cf97b-117">Gibt _ *true*\* zurück, wenn erfolgreich; andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="cf97b-117">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="cf97b-118">VB</span><span class="sxs-lookup"><span data-stu-id="cf97b-118">VB</span></span>

<span data-ttu-id="cf97b-119">Typ: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="cf97b-119">Type: \**Variant\** _</span></span>

<span data-ttu-id="cf97b-120">Gibt _ *true*\* zurück, wenn erfolgreich; andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="cf97b-120">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf97b-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf97b-121">Remarks</span></span>

<span data-ttu-id="cf97b-122">Die Methode gibt **false** zurück, wenn der Dienst bereits beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="cf97b-122">The method returns **false** if the service has already been stopped.</span></span> <span data-ttu-id="cf97b-123">Bevor Sie diese Methode aufrufen, können Sie [**Shell. isservicerunning**](./shell-isservicerunning.md) aufrufen, um den Status des Dienstanbieter zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="cf97b-123">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="cf97b-124">Diese Methode ist zurzeit nicht in Microsoft Visual Basic verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cf97b-124">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="cf97b-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cf97b-125">Examples</span></span>

<span data-ttu-id="cf97b-126">In den folgenden Beispielen wird gezeigt, wie **servicestop** verwendet wird, um den Messenger-Dienst zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="cf97b-126">The following examples show the use of **ServiceStop** to stop the Messenger service.</span></span> <span data-ttu-id="cf97b-127">Die Verwendung wird für JScript und VBScript angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cf97b-127">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="cf97b-128">JScript</span><span class="sxs-lookup"><span data-stu-id="cf97b-128">JScript:</span></span>


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



<span data-ttu-id="cf97b-129">VBScript</span><span class="sxs-lookup"><span data-stu-id="cf97b-129">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="cf97b-130">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="cf97b-130">Requirements</span></span>



| <span data-ttu-id="cf97b-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf97b-131">Requirement</span></span> | <span data-ttu-id="cf97b-132">Wert</span><span class="sxs-lookup"><span data-stu-id="cf97b-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf97b-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cf97b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="cf97b-134">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf97b-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cf97b-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cf97b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="cf97b-136">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf97b-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="cf97b-137">Header</span><span class="sxs-lookup"><span data-stu-id="cf97b-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf97b-138"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf97b-138"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="cf97b-139">IDL</span><span class="sxs-lookup"><span data-stu-id="cf97b-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cf97b-140"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cf97b-140"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="cf97b-141">DLL</span><span class="sxs-lookup"><span data-stu-id="cf97b-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf97b-142"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="cf97b-142"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
