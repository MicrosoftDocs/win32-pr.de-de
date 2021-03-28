---
description: Bestimmt, ob der aktuelle Benutzer den benannten Dienst starten und Abbrechen kann.
ms.assetid: cbb54ae9-02e6-4243-a782-e9f125c21c0d
title: IShellDispatch2. canstartstopservice-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.CanStartStopService
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 92655c2c561284f00204826e1848a75f00f4a04d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527329"
---
# <a name="ishelldispatch2canstartstopservice-method"></a><span data-ttu-id="c88e5-103">IShellDispatch2. canstartstopservice-Methode</span><span class="sxs-lookup"><span data-stu-id="c88e5-103">IShellDispatch2.CanStartStopService method</span></span>

<span data-ttu-id="c88e5-104">Bestimmt, ob der aktuelle Benutzer den benannten Dienst starten und Abbrechen kann.</span><span class="sxs-lookup"><span data-stu-id="c88e5-104">Determines if the current user can start and stop the named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="c88e5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c88e5-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.CanStartStopService(
  sServiceName
)
```


```VB

IShellDispatch2.CanStartStopService( _
  ByVal sServiceName As String _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="c88e5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c88e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c88e5-107">*sservicename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c88e5-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c88e5-108">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c88e5-108">Type: **String**</span></span>

<span data-ttu-id="c88e5-109">Eine **Zeichenfolge** , die den Namen des Dienstanbieter enthält.</span><span class="sxs-lookup"><span data-stu-id="c88e5-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c88e5-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c88e5-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="c88e5-111">JScript</span><span class="sxs-lookup"><span data-stu-id="c88e5-111">JScript</span></span>

<span data-ttu-id="c88e5-112">Typ: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="c88e5-112">Type: \**Variant\** _</span></span>

<span data-ttu-id="c88e5-113">Gibt _ *true*\* zurück, wenn der Benutzer den Dienst starten und Abbrechen kann. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="c88e5-113">Returns _ *true*\* if the user can start and stop the service; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="c88e5-114">VB</span><span class="sxs-lookup"><span data-stu-id="c88e5-114">VB</span></span>

<span data-ttu-id="c88e5-115">Typ: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="c88e5-115">Type: \**Variant\** _</span></span>

<span data-ttu-id="c88e5-116">Gibt _ *true*\* zurück, wenn der Benutzer den Dienst starten und Abbrechen kann. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="c88e5-116">Returns _ *true*\* if the user can start and stop the service; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c88e5-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c88e5-117">Remarks</span></span>

<span data-ttu-id="c88e5-118">Diese Methode wird implementiert und über die [**Shell. canstartstopservice**](./shell-canstartstopservice.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="c88e5-118">This method is implemented and accessed through the [**Shell.CanStartStopService**](./shell-canstartstopservice.md) method.</span></span>

<span data-ttu-id="c88e5-119">Diese Methode ist zurzeit nicht in Microsoft Visual Basic verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c88e5-119">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="c88e5-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c88e5-120">Examples</span></span>

<span data-ttu-id="c88e5-121">In den folgenden Beispielen wird die Verwendung von **canstartstopservice** für JScript und VBScript veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="c88e5-121">The following examples show the usage of **CanStartStopService** for JScript and VBScript.</span></span>

<span data-ttu-id="c88e5-122">JScript</span><span class="sxs-lookup"><span data-stu-id="c88e5-122">JScript:</span></span>


```JScript
<script language="JScript">
    function fnCanStartStopServiceJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;

        bReturn = objShell.CanStartStopService("service name");
    }
</script>
```



<span data-ttu-id="c88e5-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="c88e5-123">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnCanStartStopServiceVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.CanStartStopService("service name")

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="c88e5-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c88e5-124">Requirements</span></span>



| <span data-ttu-id="c88e5-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c88e5-125">Requirement</span></span> | <span data-ttu-id="c88e5-126">Wert</span><span class="sxs-lookup"><span data-stu-id="c88e5-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c88e5-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c88e5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c88e5-128">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c88e5-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c88e5-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c88e5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c88e5-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c88e5-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c88e5-131">Header</span><span class="sxs-lookup"><span data-stu-id="c88e5-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c88e5-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c88e5-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="c88e5-133">IDL</span><span class="sxs-lookup"><span data-stu-id="c88e5-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c88e5-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c88e5-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="c88e5-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c88e5-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c88e5-136"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="c88e5-136"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
