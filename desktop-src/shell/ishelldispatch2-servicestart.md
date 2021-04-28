---
description: 'IShellDispatch2.ServiceStart-Methode: Startet einen benannten Dienst.'
ms.assetid: 3af57cdc-f449-433d-a9e1-119038045e4c
title: IShellDispatch2.ServiceStart-Methode (Shldisp.h)
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
ms.openlocfilehash: c0f4fa218c4def993025ff18bffd0cc54def9818
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117048"
---
# <a name="ishelldispatch2servicestart-method"></a><span data-ttu-id="104d2-103">IShellDispatch2.ServiceStart-Methode</span><span class="sxs-lookup"><span data-stu-id="104d2-103">IShellDispatch2.ServiceStart method</span></span>

<span data-ttu-id="104d2-104">Startet einen benannten Dienst.</span><span class="sxs-lookup"><span data-stu-id="104d2-104">Starts a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="104d2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="104d2-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="104d2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="104d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="104d2-107">*sServiceName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="104d2-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="104d2-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="104d2-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="104d2-109">Eine **Zeichenfolge,** die den Namen des Diensts enthält.</span><span class="sxs-lookup"><span data-stu-id="104d2-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="104d2-110">*vPersistent* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="104d2-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="104d2-111">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="104d2-111">Type: **Variant**</span></span>

<span data-ttu-id="104d2-112">Legen Sie auf **TRUE** fest, damit der Dienst während des Systemstarts automatisch vom Dienststeuerungs-Manager gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="104d2-112">Set to **true** to have the service started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="104d2-113">Legen Sie auf **FALSE fest,** um die Dienstkonfiguration unverändert zu lassen.</span><span class="sxs-lookup"><span data-stu-id="104d2-113">Set to **false** to leave the service configuration unchanged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="104d2-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="104d2-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="104d2-115">JScript</span><span class="sxs-lookup"><span data-stu-id="104d2-115">JScript</span></span>

<span data-ttu-id="104d2-116">Typ: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="104d2-116">Type: **Variant\***</span></span>

<span data-ttu-id="104d2-117">Gibt **true zurück,** wenn erfolgreich; andernfalls **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="104d2-117">Returns **true** if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="104d2-118">VB</span><span class="sxs-lookup"><span data-stu-id="104d2-118">VB</span></span>

<span data-ttu-id="104d2-119">Typ: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="104d2-119">Type: **Variant\***</span></span>

<span data-ttu-id="104d2-120">Gibt **true zurück,** wenn erfolgreich; andernfalls **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="104d2-120">Returns **true** if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="104d2-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="104d2-121">Remarks</span></span>

<span data-ttu-id="104d2-122">Diese Methode wird implementiert und über die [**Shell.ServiceStart-Methode aufgerufen.**](./shell-servicestart.md)</span><span class="sxs-lookup"><span data-stu-id="104d2-122">This method is implemented and accessed through the [**Shell.ServiceStart**](./shell-servicestart.md) method.</span></span>

<span data-ttu-id="104d2-123">Die -Methode **gibt FALSE** zurück, wenn der Dienst bereits gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="104d2-123">The method returns **false** if the service has already been started.</span></span> <span data-ttu-id="104d2-124">Vor dem Aufrufen dieser Methode können Sie [**Shell.IsServiceRunning**](./shell-isservicerunning.md) aufrufen, um den Status des Diensts zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="104d2-124">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="104d2-125">Diese Methode ist derzeit in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="104d2-125">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="104d2-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="104d2-126">Examples</span></span>

<span data-ttu-id="104d2-127">Die folgenden Beispiele zeigen die Verwendung von **ServiceStart zum** Starten des Messenger-Diensts.</span><span class="sxs-lookup"><span data-stu-id="104d2-127">The following examples show the use of **ServiceStart** to start the Messenger service.</span></span> <span data-ttu-id="104d2-128">Die Verwendung wird für JScript und VBScript angezeigt.</span><span class="sxs-lookup"><span data-stu-id="104d2-128">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="104d2-129">Jscript:</span><span class="sxs-lookup"><span data-stu-id="104d2-129">JScript:</span></span>


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



<span data-ttu-id="104d2-130">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="104d2-130">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="104d2-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="104d2-131">Requirements</span></span>



| <span data-ttu-id="104d2-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="104d2-132">Requirement</span></span> | <span data-ttu-id="104d2-133">Wert</span><span class="sxs-lookup"><span data-stu-id="104d2-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="104d2-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="104d2-134">Minimum supported client</span></span><br/> | <span data-ttu-id="104d2-135">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="104d2-135">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="104d2-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="104d2-136">Minimum supported server</span></span><br/> | <span data-ttu-id="104d2-137">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="104d2-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="104d2-138">Header</span><span class="sxs-lookup"><span data-stu-id="104d2-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="104d2-139"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="104d2-139"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="104d2-140">Idl</span><span class="sxs-lookup"><span data-stu-id="104d2-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="104d2-141"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="104d2-141"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="104d2-142">DLL</span><span class="sxs-lookup"><span data-stu-id="104d2-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="104d2-143"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="104d2-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
