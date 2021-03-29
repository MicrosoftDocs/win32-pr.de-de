---
description: Startet einen benannten Dienst.
ms.assetid: 3af57cdc-f449-433d-a9e1-119038045e4c
title: IShellDispatch2. Servicestart-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ServiceStart
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 508b4f1c05625acdaed2b5a235ee697cceb544c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978025"
---
# <a name="ishelldispatch2servicestart-method"></a><span data-ttu-id="83762-103">IShellDispatch2. Servicestart-Methode</span><span class="sxs-lookup"><span data-stu-id="83762-103">IShellDispatch2.ServiceStart method</span></span>

<span data-ttu-id="83762-104">Startet einen benannten Dienst.</span><span class="sxs-lookup"><span data-stu-id="83762-104">Starts a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="83762-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="83762-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.ServiceStart(
  sServiceName,
  vPersistent
)
```


```VB

IShellDispatch2.ServiceStart( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="83762-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="83762-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83762-107">*sservicename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83762-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83762-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="83762-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="83762-109">Eine **Zeichenfolge** , die den Namen des Dienstanbieter enthält.</span><span class="sxs-lookup"><span data-stu-id="83762-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="83762-110">*vpersistent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83762-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83762-111">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="83762-111">Type: **Variant**</span></span>

<span data-ttu-id="83762-112">Legen Sie diese Einstellung auf " **true** " fest, damit der Dienst vom Dienststeuerungs-Manager beim Systemstart automatisch gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="83762-112">Set to **true** to have the service started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="83762-113">Legen Sie auf **false** fest, um die Dienst Konfiguration unverändert zu lassen.</span><span class="sxs-lookup"><span data-stu-id="83762-113">Set to **false** to leave the service configuration unchanged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83762-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="83762-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="83762-115">JScript</span><span class="sxs-lookup"><span data-stu-id="83762-115">JScript</span></span>

<span data-ttu-id="83762-116">Typ: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="83762-116">Type: \**Variant\** _</span></span>

<span data-ttu-id="83762-117">Gibt _ *true*\* zurück, wenn erfolgreich; andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="83762-117">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="83762-118">VB</span><span class="sxs-lookup"><span data-stu-id="83762-118">VB</span></span>

<span data-ttu-id="83762-119">Typ: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="83762-119">Type: \**Variant\** _</span></span>

<span data-ttu-id="83762-120">Gibt _ *true*\* zurück, wenn erfolgreich; andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="83762-120">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="83762-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83762-121">Remarks</span></span>

<span data-ttu-id="83762-122">Diese Methode wird implementiert und über die [**Shell. Servicestart**](./shell-servicestart.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="83762-122">This method is implemented and accessed through the [**Shell.ServiceStart**](./shell-servicestart.md) method.</span></span>

<span data-ttu-id="83762-123">Die Methode gibt **false** zurück, wenn der Dienst bereits gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="83762-123">The method returns **false** if the service has already been started.</span></span> <span data-ttu-id="83762-124">Bevor Sie diese Methode aufrufen, können Sie [**Shell. isservicerunning**](./shell-isservicerunning.md) aufrufen, um den Status des Dienstanbieter zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="83762-124">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="83762-125">Diese Methode ist zurzeit nicht in Microsoft Visual Basic verfügbar.</span><span class="sxs-lookup"><span data-stu-id="83762-125">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="83762-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="83762-126">Examples</span></span>

<span data-ttu-id="83762-127">In den folgenden Beispielen wird veranschaulicht, wie **Servicestart** verwendet wird, um den Messenger-Dienst zu starten.</span><span class="sxs-lookup"><span data-stu-id="83762-127">The following examples show the use of **ServiceStart** to start the Messenger service.</span></span> <span data-ttu-id="83762-128">Die Verwendung wird für JScript und VBScript angezeigt.</span><span class="sxs-lookup"><span data-stu-id="83762-128">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="83762-129">JScript</span><span class="sxs-lookup"><span data-stu-id="83762-129">JScript:</span></span>


```JScript
<script language="JScript">
    function fnServiceStartJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStart("Messenger", true);
    }
</script>
```



<span data-ttu-id="83762-130">VBScript</span><span class="sxs-lookup"><span data-stu-id="83762-130">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="83762-131">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="83762-131">Requirements</span></span>



| <span data-ttu-id="83762-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="83762-132">Requirement</span></span> | <span data-ttu-id="83762-133">Wert</span><span class="sxs-lookup"><span data-stu-id="83762-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83762-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="83762-134">Minimum supported client</span></span><br/> | <span data-ttu-id="83762-135">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="83762-135">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="83762-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="83762-136">Minimum supported server</span></span><br/> | <span data-ttu-id="83762-137">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="83762-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="83762-138">Header</span><span class="sxs-lookup"><span data-stu-id="83762-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="83762-139"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="83762-139"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="83762-140">IDL</span><span class="sxs-lookup"><span data-stu-id="83762-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="83762-141"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="83762-141"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="83762-142">DLL</span><span class="sxs-lookup"><span data-stu-id="83762-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83762-143"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="83762-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
