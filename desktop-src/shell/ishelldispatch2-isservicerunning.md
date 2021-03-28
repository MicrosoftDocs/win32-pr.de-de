---
description: Gibt einen Wert zurück, der angibt, ob ein bestimmter Dienst ausgeführt wird.
ms.assetid: 91f3fba1-7aa5-423a-bc37-49db230c79db
title: IShellDispatch2. isservicerunning-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.IsServiceRunning
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f39cd7da3d9959830208ab971b636e146e549775
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978048"
---
# <a name="ishelldispatch2isservicerunning-method"></a><span data-ttu-id="ca969-103">IShellDispatch2. isservicerunning-Methode</span><span class="sxs-lookup"><span data-stu-id="ca969-103">IShellDispatch2.IsServiceRunning method</span></span>

<span data-ttu-id="ca969-104">Gibt einen Wert zurück, der angibt, ob ein bestimmter Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ca969-104">Returns a value that indicates whether a particular service is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca969-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca969-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.IsServiceRunning(
  sServiceName
)
```


```VB

IShellDispatch2.IsServiceRunning( _
  ByVal sServiceName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="ca969-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca969-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca969-107">*sservicename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca969-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca969-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="ca969-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="ca969-109">Eine **Zeichenfolge** , die den Namen des Dienstanbieter enthält.</span><span class="sxs-lookup"><span data-stu-id="ca969-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca969-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ca969-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="ca969-111">JScript</span><span class="sxs-lookup"><span data-stu-id="ca969-111">JScript</span></span>

<span data-ttu-id="ca969-112">Typ: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="ca969-112">Type: \**Variant\** _</span></span>

<span data-ttu-id="ca969-113">Gibt _ *true*\* zurück, wenn der von *sservicename* angegebene Dienst ausgeführt wird. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="ca969-113">Returns _ *true*\* if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="ca969-114">VB</span><span class="sxs-lookup"><span data-stu-id="ca969-114">VB</span></span>

<span data-ttu-id="ca969-115">Typ: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="ca969-115">Type: \**Variant\** _</span></span>

<span data-ttu-id="ca969-116">Gibt _ *true*\* zurück, wenn der von *sservicename* angegebene Dienst ausgeführt wird. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="ca969-116">Returns _ *true*\* if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca969-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca969-117">Remarks</span></span>

<span data-ttu-id="ca969-118">Diese Methode wird implementiert und über die [**Shell. isservicerunning**](./shell-isservicerunning.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="ca969-118">This method is implemented and accessed through the [**Shell.IsServiceRunning**](./shell-isservicerunning.md) method.</span></span>

<span data-ttu-id="ca969-119">Diese Methode ist zurzeit nicht in Microsoft Visual Basic verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ca969-119">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="ca969-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ca969-120">Examples</span></span>

<span data-ttu-id="ca969-121">In den folgenden Beispielen wird die Verwendung von **isservicerunning** veranschaulicht, um zu bestimmen, ob der Themes-Dienst für eine Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ca969-121">The following examples show the use of **IsServiceRunning** to determine whether the Themes service is running for an application.</span></span> <span data-ttu-id="ca969-122">Die Verwendung wird für JScript und VBScript angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ca969-122">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="ca969-123">JScript</span><span class="sxs-lookup"><span data-stu-id="ca969-123">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIsServiceRunningJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
    
        bReturn = objShell.IsServiceRunning("Themes");
    }
</script>
```



<span data-ttu-id="ca969-124">VBScript</span><span class="sxs-lookup"><span data-stu-id="ca969-124">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIsServiceRunningVB()
        dim objShell
        dim bReturn
    
        set objShell = CreateObject("shell.application")
    
        bReturn = objShell.IsServiceRunning("Themes")
    
        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="ca969-125">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ca969-125">Requirements</span></span>



| <span data-ttu-id="ca969-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca969-126">Requirement</span></span> | <span data-ttu-id="ca969-127">Wert</span><span class="sxs-lookup"><span data-stu-id="ca969-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca969-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ca969-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ca969-129">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ca969-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ca969-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ca969-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ca969-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ca969-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ca969-132">Header</span><span class="sxs-lookup"><span data-stu-id="ca969-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca969-133"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca969-133"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="ca969-134">IDL</span><span class="sxs-lookup"><span data-stu-id="ca969-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ca969-135"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ca969-135"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="ca969-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ca969-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca969-137"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="ca969-137"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
