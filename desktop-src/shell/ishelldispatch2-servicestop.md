---
description: Beendet einen benannten Dienst.
ms.assetid: f4cd0e2c-4ecc-4e9f-a0b5-d2a8a739f0e2
title: IShellDispatch2. servicestop-Methode (Shldisp. h)
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
ms.openlocfilehash: 6a4a76c1f53309c14875eeaf6f3f4c0839a511bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978017"
---
# <a name="ishelldispatch2servicestop-method"></a><span data-ttu-id="690fe-103">IShellDispatch2. servicestop-Methode</span><span class="sxs-lookup"><span data-stu-id="690fe-103">IShellDispatch2.ServiceStop method</span></span>

<span data-ttu-id="690fe-104">Beendet einen benannten Dienst.</span><span class="sxs-lookup"><span data-stu-id="690fe-104">Stops a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="690fe-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="690fe-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="690fe-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="690fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="690fe-107">*sservicename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="690fe-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="690fe-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="690fe-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="690fe-109">Eine **Zeichenfolge** , die den Namen des Dienstanbieter enthält.</span><span class="sxs-lookup"><span data-stu-id="690fe-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="690fe-110">*vpersistent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="690fe-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="690fe-111">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="690fe-111">Type: **Variant**</span></span>

<span data-ttu-id="690fe-112">Legen Sie diese Einstellung auf **true** fest, damit der Dienst vom Dienststeuerungs-Manager gestartet wird, wenn [**Servicestart**](ishelldispatch2-servicestart.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="690fe-112">Set to **true** to have the service started by the service control manager when [**ServiceStart**](ishelldispatch2-servicestart.md) is called.</span></span> <span data-ttu-id="690fe-113">Legen Sie *vpersistenz* auf **false** fest, um die Dienst Konfiguration unverändert zu lassen.</span><span class="sxs-lookup"><span data-stu-id="690fe-113">To leave the service configuration unchanged, set *vPersistent* to **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="690fe-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="690fe-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="690fe-115">JScript</span><span class="sxs-lookup"><span data-stu-id="690fe-115">JScript</span></span>

<span data-ttu-id="690fe-116">Typ: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="690fe-116">Type: \**Variant\** _</span></span>

<span data-ttu-id="690fe-117">Gibt _ *true*\* zurück, wenn erfolgreich; andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="690fe-117">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="690fe-118">VB</span><span class="sxs-lookup"><span data-stu-id="690fe-118">VB</span></span>

<span data-ttu-id="690fe-119">Typ: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="690fe-119">Type: \**Variant\** _</span></span>

<span data-ttu-id="690fe-120">Gibt _ *true*\* zurück, wenn erfolgreich; andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="690fe-120">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="690fe-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="690fe-121">Remarks</span></span>

<span data-ttu-id="690fe-122">Diese Methode wird implementiert und über die [**Shell. servicestop**](./shell-servicestop.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="690fe-122">This method is implemented and accessed through the [**Shell.ServiceStop**](./shell-servicestop.md) method.</span></span>

<span data-ttu-id="690fe-123">Die Methode gibt **false** zurück, wenn der Dienst bereits beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="690fe-123">The method returns **false** if the service has already been stopped.</span></span> <span data-ttu-id="690fe-124">Bevor Sie diese Methode aufrufen, können Sie [**Shell. isservicerunning**](./shell-isservicerunning.md) aufrufen, um den Status des Dienstanbieter zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="690fe-124">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="690fe-125">Diese Methode ist zurzeit nicht in Microsoft Visual Basic verfügbar.</span><span class="sxs-lookup"><span data-stu-id="690fe-125">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="690fe-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="690fe-126">Examples</span></span>

<span data-ttu-id="690fe-127">In den folgenden Beispielen wird gezeigt, wie **servicestop** verwendet wird, um den Messenger-Dienst zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="690fe-127">The following examples show the use of **ServiceStop** to stop the Messenger service.</span></span> <span data-ttu-id="690fe-128">Die Verwendung wird für JScript und VBScript angezeigt.</span><span class="sxs-lookup"><span data-stu-id="690fe-128">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="690fe-129">JScript</span><span class="sxs-lookup"><span data-stu-id="690fe-129">JScript:</span></span>


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



<span data-ttu-id="690fe-130">VBScript</span><span class="sxs-lookup"><span data-stu-id="690fe-130">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="690fe-131">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="690fe-131">Requirements</span></span>



| <span data-ttu-id="690fe-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="690fe-132">Requirement</span></span> | <span data-ttu-id="690fe-133">Wert</span><span class="sxs-lookup"><span data-stu-id="690fe-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="690fe-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="690fe-134">Minimum supported client</span></span><br/> | <span data-ttu-id="690fe-135">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="690fe-135">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="690fe-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="690fe-136">Minimum supported server</span></span><br/> | <span data-ttu-id="690fe-137">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="690fe-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="690fe-138">Header</span><span class="sxs-lookup"><span data-stu-id="690fe-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="690fe-139"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="690fe-139"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="690fe-140">IDL</span><span class="sxs-lookup"><span data-stu-id="690fe-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="690fe-141"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="690fe-141"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="690fe-142">DLL</span><span class="sxs-lookup"><span data-stu-id="690fe-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="690fe-143"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="690fe-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
