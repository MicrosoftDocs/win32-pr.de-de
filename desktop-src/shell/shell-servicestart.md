---
description: 'Shell.ServiceStart-Methode: Startet einen benannten Dienst.'
ms.assetid: 72214E80-38A2-4a57-B555-942902BAFC3D
title: Shell.ServiceStart-Methode (Shldisp.h)
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
ms.openlocfilehash: 9c88b1980d215ad088a4a24362f17147b5d6e432
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083748"
---
# <a name="shellservicestart-method"></a><span data-ttu-id="424e7-103">Shell.ServiceStart-Methode</span><span class="sxs-lookup"><span data-stu-id="424e7-103">Shell.ServiceStart method</span></span>

<span data-ttu-id="424e7-104">Startet einen benannten Dienst.</span><span class="sxs-lookup"><span data-stu-id="424e7-104">Starts a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="424e7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="424e7-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="424e7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="424e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="424e7-107">*sServiceName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="424e7-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="424e7-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="424e7-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="424e7-109">Eine **Zeichenfolge,** die den Namen des Diensts enthält.</span><span class="sxs-lookup"><span data-stu-id="424e7-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="424e7-110">*vPersistent* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="424e7-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="424e7-111">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="424e7-111">Type: **Variant**</span></span>

<span data-ttu-id="424e7-112">Legen Sie diese Einstellung auf **TRUE** fest, damit der Dienst während des Systemstarts automatisch vom Dienststeuerungs-Manager gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="424e7-112">Set to **true** to have the service started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="424e7-113">Legen Sie diese Einstellung auf **FALSE** fest, um die Dienstkonfiguration unverändert zu lassen.</span><span class="sxs-lookup"><span data-stu-id="424e7-113">Set to **false** to leave the service configuration unchanged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="424e7-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="424e7-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="424e7-115">JScript</span><span class="sxs-lookup"><span data-stu-id="424e7-115">JScript</span></span>

<span data-ttu-id="424e7-116">Typ: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="424e7-116">Type: **Variant\***</span></span>

<span data-ttu-id="424e7-117">Gibt **true** zurück, wenn erfolgreich. andernfalls **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="424e7-117">Returns **true** if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="424e7-118">VB</span><span class="sxs-lookup"><span data-stu-id="424e7-118">VB</span></span>

<span data-ttu-id="424e7-119">Typ: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="424e7-119">Type: **Variant\***</span></span>

<span data-ttu-id="424e7-120">Gibt **true** zurück, wenn erfolgreich. andernfalls **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="424e7-120">Returns **true** if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="424e7-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="424e7-121">Remarks</span></span>

<span data-ttu-id="424e7-122">Die Methode gibt **FALSE** zurück, wenn der Dienst bereits gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="424e7-122">The method returns **false** if the service has already been started.</span></span> <span data-ttu-id="424e7-123">Vor dem Aufrufen dieser Methode können Sie [**Shell.IsServiceRunning**](./shell-isservicerunning.md) aufrufen, um den Status des Diensts zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="424e7-123">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="424e7-124">Diese Methode ist derzeit in Microsoft Visual Basic nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="424e7-124">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="424e7-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="424e7-125">Examples</span></span>

<span data-ttu-id="424e7-126">In den folgenden Beispielen wird die Verwendung von **ServiceStart** zum Starten des Messenger-Diensts gezeigt.</span><span class="sxs-lookup"><span data-stu-id="424e7-126">The following examples show the use of **ServiceStart** to start the Messenger service.</span></span> <span data-ttu-id="424e7-127">Die Verwendung wird für JScript und VBScript angezeigt.</span><span class="sxs-lookup"><span data-stu-id="424e7-127">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="424e7-128">Jscript:</span><span class="sxs-lookup"><span data-stu-id="424e7-128">JScript:</span></span>


```JScript
<script language="JScript">
    function fnServiceStartJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStart("Messenger", true);
    }
```



<span data-ttu-id="424e7-129">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="424e7-129">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="424e7-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="424e7-130">Requirements</span></span>



| <span data-ttu-id="424e7-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="424e7-131">Requirement</span></span> | <span data-ttu-id="424e7-132">Wert</span><span class="sxs-lookup"><span data-stu-id="424e7-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="424e7-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="424e7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="424e7-134">Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="424e7-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="424e7-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="424e7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="424e7-136">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="424e7-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="424e7-137">Header</span><span class="sxs-lookup"><span data-stu-id="424e7-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="424e7-138"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="424e7-138"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="424e7-139">Idl</span><span class="sxs-lookup"><span data-stu-id="424e7-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="424e7-140"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="424e7-140"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="424e7-141">DLL</span><span class="sxs-lookup"><span data-stu-id="424e7-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="424e7-142"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="424e7-142"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
