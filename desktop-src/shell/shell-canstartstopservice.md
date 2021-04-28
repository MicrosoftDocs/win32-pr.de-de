---
description: 'Shell.CanStartStopService-Methode: Bestimmt, ob der aktuelle Benutzer den benannten Dienst starten und beenden kann.'
ms.assetid: 1428F529-61F6-4113-A553-2C0D617FD859
title: Shell.CanStartStopService-Methode (Shldisp.h)
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
ms.openlocfilehash: 29561519b95329093ef1f7bfc64023fd1ac4533d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083688"
---
# <a name="shellcanstartstopservice-method"></a><span data-ttu-id="6a8b4-103">Shell.CanStartStopService-Methode</span><span class="sxs-lookup"><span data-stu-id="6a8b4-103">Shell.CanStartStopService method</span></span>

<span data-ttu-id="6a8b4-104">Bestimmt, ob der aktuelle Benutzer den benannten Dienst starten und beenden kann.</span><span class="sxs-lookup"><span data-stu-id="6a8b4-104">Determines if the current user can start and stop the named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a8b4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a8b4-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="6a8b4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a8b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a8b4-107">*sServiceName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6a8b4-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a8b4-108">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6a8b4-108">Type: **String**</span></span>

<span data-ttu-id="6a8b4-109">Eine **Zeichenfolge,** die den Namen des Diensts enthält.</span><span class="sxs-lookup"><span data-stu-id="6a8b4-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a8b4-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6a8b4-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="6a8b4-111">JScript</span><span class="sxs-lookup"><span data-stu-id="6a8b4-111">JScript</span></span>

<span data-ttu-id="6a8b4-112">Typ: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="6a8b4-112">Type: **Variant\***</span></span>

<span data-ttu-id="6a8b4-113">Gibt **TRUE** zurück, wenn der Benutzer den Dienst starten und beenden kann. andernfalls **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="6a8b4-113">Returns **true** if the user can start and stop the service; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="6a8b4-114">VB</span><span class="sxs-lookup"><span data-stu-id="6a8b4-114">VB</span></span>

<span data-ttu-id="6a8b4-115">Typ: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="6a8b4-115">Type: **Variant\***</span></span>

<span data-ttu-id="6a8b4-116">Gibt **TRUE** zurück, wenn der Benutzer den Dienst starten und beenden kann. andernfalls **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="6a8b4-116">Returns **true** if the user can start and stop the service; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a8b4-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6a8b4-117">Remarks</span></span>

<span data-ttu-id="6a8b4-118">Diese Methode ist derzeit in Microsoft Visual Basic nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6a8b4-118">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="6a8b4-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6a8b4-119">Examples</span></span>

<span data-ttu-id="6a8b4-120">Die folgenden Beispiele zeigen die Verwendung von **CanStartStopService** für JScript und VBScript.</span><span class="sxs-lookup"><span data-stu-id="6a8b4-120">The following examples show the usage of **CanStartStopService** for JScript and VBScript.</span></span>

<span data-ttu-id="6a8b4-121">Jscript:</span><span class="sxs-lookup"><span data-stu-id="6a8b4-121">JScript:</span></span>


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



<span data-ttu-id="6a8b4-122">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="6a8b4-122">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="6a8b4-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6a8b4-123">Requirements</span></span>



| <span data-ttu-id="6a8b4-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6a8b4-124">Requirement</span></span> | <span data-ttu-id="6a8b4-125">Wert</span><span class="sxs-lookup"><span data-stu-id="6a8b4-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a8b4-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6a8b4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6a8b4-127">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6a8b4-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6a8b4-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6a8b4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6a8b4-129">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6a8b4-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6a8b4-130">Header</span><span class="sxs-lookup"><span data-stu-id="6a8b4-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a8b4-131"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="6a8b4-131"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="6a8b4-132">Idl</span><span class="sxs-lookup"><span data-stu-id="6a8b4-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6a8b4-133"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="6a8b4-133"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="6a8b4-134">DLL</span><span class="sxs-lookup"><span data-stu-id="6a8b4-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a8b4-135"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="6a8b4-135"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




