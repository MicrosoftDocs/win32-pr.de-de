---
description: Startet einen benannten Dienst.
ms.assetid: 72214E80-38A2-4a57-B555-942902BAFC3D
title: Shell. Servicestart-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ServiceStart
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8cd3b910306fc995d15e9731823614717450ef55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865260"
---
# <a name="shellservicestart-method"></a><span data-ttu-id="0cdae-103">Shell. Servicestart-Methode</span><span class="sxs-lookup"><span data-stu-id="0cdae-103">Shell.ServiceStart method</span></span>

<span data-ttu-id="0cdae-104">Startet einen benannten Dienst.</span><span class="sxs-lookup"><span data-stu-id="0cdae-104">Starts a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cdae-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0cdae-105">Syntax</span></span>


```JScript
retVal = Shell.ServiceStart(
  sServiceName,
  vPersistent
)
```


```VB

Shell.ServiceStart( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="0cdae-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0cdae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cdae-107">*sservicename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0cdae-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cdae-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="0cdae-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="0cdae-109">Eine **Zeichenfolge** , die den Namen des Dienstanbieter enthält.</span><span class="sxs-lookup"><span data-stu-id="0cdae-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="0cdae-110">*vpersistent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0cdae-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cdae-111">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="0cdae-111">Type: **Variant**</span></span>

<span data-ttu-id="0cdae-112">Legen Sie diese Einstellung auf " **true** " fest, damit der Dienst vom Dienststeuerungs-Manager beim Systemstart automatisch gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="0cdae-112">Set to **true** to have the service started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="0cdae-113">Legen Sie auf **false** fest, um die Dienst Konfiguration unverändert zu lassen.</span><span class="sxs-lookup"><span data-stu-id="0cdae-113">Set to **false** to leave the service configuration unchanged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cdae-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0cdae-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="0cdae-115">JScript</span><span class="sxs-lookup"><span data-stu-id="0cdae-115">JScript</span></span>

<span data-ttu-id="0cdae-116">Typ: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="0cdae-116">Type: \**Variant\** _</span></span>

<span data-ttu-id="0cdae-117">Gibt _ *true*\* zurück, wenn erfolgreich; andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="0cdae-117">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="0cdae-118">VB</span><span class="sxs-lookup"><span data-stu-id="0cdae-118">VB</span></span>

<span data-ttu-id="0cdae-119">Typ: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="0cdae-119">Type: \**Variant\** _</span></span>

<span data-ttu-id="0cdae-120">Gibt _ *true*\* zurück, wenn erfolgreich; andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="0cdae-120">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cdae-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0cdae-121">Remarks</span></span>

<span data-ttu-id="0cdae-122">Die Methode gibt **false** zurück, wenn der Dienst bereits gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="0cdae-122">The method returns **false** if the service has already been started.</span></span> <span data-ttu-id="0cdae-123">Bevor Sie diese Methode aufrufen, können Sie [**Shell. isservicerunning**](./shell-isservicerunning.md) aufrufen, um den Status des Dienstanbieter zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="0cdae-123">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="0cdae-124">Diese Methode ist zurzeit nicht in Microsoft Visual Basic verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0cdae-124">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="0cdae-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0cdae-125">Examples</span></span>

<span data-ttu-id="0cdae-126">In den folgenden Beispielen wird veranschaulicht, wie **Servicestart** verwendet wird, um den Messenger-Dienst zu starten.</span><span class="sxs-lookup"><span data-stu-id="0cdae-126">The following examples show the use of **ServiceStart** to start the Messenger service.</span></span> <span data-ttu-id="0cdae-127">Die Verwendung wird für JScript und VBScript angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0cdae-127">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="0cdae-128">JScript</span><span class="sxs-lookup"><span data-stu-id="0cdae-128">JScript:</span></span>


```JScript
<script language="JScript">
    function fnServiceStartJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStart("Messenger", true);
    }
```



<span data-ttu-id="0cdae-129">VBScript</span><span class="sxs-lookup"><span data-stu-id="0cdae-129">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnServiceStartVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ServiceStart("Messenger", true)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="0cdae-130">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="0cdae-130">Requirements</span></span>



| <span data-ttu-id="0cdae-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0cdae-131">Requirement</span></span> | <span data-ttu-id="0cdae-132">Wert</span><span class="sxs-lookup"><span data-stu-id="0cdae-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cdae-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0cdae-133">Minimum supported client</span></span><br/> | <span data-ttu-id="0cdae-134">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0cdae-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0cdae-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0cdae-135">Minimum supported server</span></span><br/> | <span data-ttu-id="0cdae-136">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0cdae-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="0cdae-137">Header</span><span class="sxs-lookup"><span data-stu-id="0cdae-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cdae-138"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cdae-138"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="0cdae-139">IDL</span><span class="sxs-lookup"><span data-stu-id="0cdae-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0cdae-140"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0cdae-140"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="0cdae-141">DLL</span><span class="sxs-lookup"><span data-stu-id="0cdae-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0cdae-142"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="0cdae-142"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
