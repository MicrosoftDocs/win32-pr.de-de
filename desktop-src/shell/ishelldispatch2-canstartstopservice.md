---
description: 'IShellDispatch2.CanStartStopService-Methode: Bestimmt, ob der aktuelle Benutzer den benannten Dienst starten und beenden kann.'
ms.assetid: cbb54ae9-02e6-4243-a782-e9f125c21c0d
title: IShellDispatch2.CanStartStopService-Methode (Shldisp.h)
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
ms.openlocfilehash: 600cf7fafd556a9192c4b0de4089516bc6cca2a0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117128"
---
# <a name="ishelldispatch2canstartstopservice-method"></a><span data-ttu-id="aed19-103">IShellDispatch2.CanStartStopService-Methode</span><span class="sxs-lookup"><span data-stu-id="aed19-103">IShellDispatch2.CanStartStopService method</span></span>

<span data-ttu-id="aed19-104">Bestimmt, ob der aktuelle Benutzer den benannten Dienst starten und beenden kann.</span><span class="sxs-lookup"><span data-stu-id="aed19-104">Determines if the current user can start and stop the named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="aed19-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aed19-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="aed19-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aed19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aed19-107">*sServiceName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="aed19-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aed19-108">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="aed19-108">Type: **String**</span></span>

<span data-ttu-id="aed19-109">Eine **Zeichenfolge,** die den Namen des Diensts enthält.</span><span class="sxs-lookup"><span data-stu-id="aed19-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aed19-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aed19-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="aed19-111">JScript</span><span class="sxs-lookup"><span data-stu-id="aed19-111">JScript</span></span>

<span data-ttu-id="aed19-112">Typ: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="aed19-112">Type: **Variant\***</span></span>

<span data-ttu-id="aed19-113">Gibt **TRUE zurück,** wenn der Benutzer den Dienst starten und beenden kann. andernfalls **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="aed19-113">Returns **true** if the user can start and stop the service; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="aed19-114">VB</span><span class="sxs-lookup"><span data-stu-id="aed19-114">VB</span></span>

<span data-ttu-id="aed19-115">Typ: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="aed19-115">Type: **Variant\***</span></span>

<span data-ttu-id="aed19-116">Gibt **TRUE zurück,** wenn der Benutzer den Dienst starten und beenden kann. andernfalls **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="aed19-116">Returns **true** if the user can start and stop the service; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="aed19-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aed19-117">Remarks</span></span>

<span data-ttu-id="aed19-118">Diese Methode wird implementiert und über die [**Shell.CanStartStopService-Methode**](./shell-canstartstopservice.md) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="aed19-118">This method is implemented and accessed through the [**Shell.CanStartStopService**](./shell-canstartstopservice.md) method.</span></span>

<span data-ttu-id="aed19-119">Diese Methode ist derzeit in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="aed19-119">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="aed19-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aed19-120">Examples</span></span>

<span data-ttu-id="aed19-121">Die folgenden Beispiele zeigen die Verwendung von **CanStartStopService** für JScript und VBScript.</span><span class="sxs-lookup"><span data-stu-id="aed19-121">The following examples show the usage of **CanStartStopService** for JScript and VBScript.</span></span>

<span data-ttu-id="aed19-122">Jscript:</span><span class="sxs-lookup"><span data-stu-id="aed19-122">JScript:</span></span>


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



<span data-ttu-id="aed19-123">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="aed19-123">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="aed19-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aed19-124">Requirements</span></span>



| <span data-ttu-id="aed19-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aed19-125">Requirement</span></span> | <span data-ttu-id="aed19-126">Wert</span><span class="sxs-lookup"><span data-stu-id="aed19-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aed19-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aed19-127">Minimum supported client</span></span><br/> | <span data-ttu-id="aed19-128">Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aed19-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aed19-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aed19-129">Minimum supported server</span></span><br/> | <span data-ttu-id="aed19-130">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aed19-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="aed19-131">Header</span><span class="sxs-lookup"><span data-stu-id="aed19-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="aed19-132"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="aed19-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="aed19-133">Idl</span><span class="sxs-lookup"><span data-stu-id="aed19-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="aed19-134"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="aed19-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="aed19-135">DLL</span><span class="sxs-lookup"><span data-stu-id="aed19-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aed19-136"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="aed19-136"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
