---
description: Bestimmt, ob der aktuelle Benutzer den benannten Dienst starten und Abbrechen kann.
ms.assetid: 1428F529-61F6-4113-A553-2C0D617FD859
title: Shell. canstartstopservice-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.CanStartStopService
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1d92fa076141bdebc8a2f24059a65e842e5a3d6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959994"
---
# <a name="shellcanstartstopservice-method"></a><span data-ttu-id="c7902-103">Shell. canstartstopservice-Methode</span><span class="sxs-lookup"><span data-stu-id="c7902-103">Shell.CanStartStopService method</span></span>

<span data-ttu-id="c7902-104">Bestimmt, ob der aktuelle Benutzer den benannten Dienst starten und Abbrechen kann.</span><span class="sxs-lookup"><span data-stu-id="c7902-104">Determines if the current user can start and stop the named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7902-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7902-105">Syntax</span></span>


```JScript
retVal = Shell.CanStartStopService(
  sServiceName
)
```


```VB

Shell.CanStartStopService( _
  ByVal sServiceName As String _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="c7902-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7902-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7902-107">*sservicename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7902-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7902-108">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c7902-108">Type: **String**</span></span>

<span data-ttu-id="c7902-109">Eine **Zeichenfolge** , die den Namen des Dienstanbieter enthält.</span><span class="sxs-lookup"><span data-stu-id="c7902-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7902-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c7902-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="c7902-111">JScript</span><span class="sxs-lookup"><span data-stu-id="c7902-111">JScript</span></span>

<span data-ttu-id="c7902-112">Typ: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="c7902-112">Type: \**Variant\** _</span></span>

<span data-ttu-id="c7902-113">Gibt _ *true*\* zurück, wenn der Benutzer den Dienst starten und Abbrechen kann. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="c7902-113">Returns _ *true*\* if the user can start and stop the service; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="c7902-114">VB</span><span class="sxs-lookup"><span data-stu-id="c7902-114">VB</span></span>

<span data-ttu-id="c7902-115">Typ: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="c7902-115">Type: \**Variant\** _</span></span>

<span data-ttu-id="c7902-116">Gibt _ *true*\* zurück, wenn der Benutzer den Dienst starten und Abbrechen kann. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="c7902-116">Returns _ *true*\* if the user can start and stop the service; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7902-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7902-117">Remarks</span></span>

<span data-ttu-id="c7902-118">Diese Methode ist zurzeit nicht in Microsoft Visual Basic verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c7902-118">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="c7902-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c7902-119">Examples</span></span>

<span data-ttu-id="c7902-120">In den folgenden Beispielen wird die Verwendung von **canstartstopservice** für JScript und VBScript veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="c7902-120">The following examples show the usage of **CanStartStopService** for JScript and VBScript.</span></span>

<span data-ttu-id="c7902-121">JScript</span><span class="sxs-lookup"><span data-stu-id="c7902-121">JScript:</span></span>


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



<span data-ttu-id="c7902-122">VBScript</span><span class="sxs-lookup"><span data-stu-id="c7902-122">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="c7902-123">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c7902-123">Requirements</span></span>



| <span data-ttu-id="c7902-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7902-124">Requirement</span></span> | <span data-ttu-id="c7902-125">Wert</span><span class="sxs-lookup"><span data-stu-id="c7902-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7902-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c7902-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c7902-127">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7902-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c7902-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c7902-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c7902-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7902-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c7902-130">Header</span><span class="sxs-lookup"><span data-stu-id="c7902-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7902-131"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7902-131"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="c7902-132">IDL</span><span class="sxs-lookup"><span data-stu-id="c7902-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c7902-133"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c7902-133"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="c7902-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c7902-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7902-135"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="c7902-135"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




