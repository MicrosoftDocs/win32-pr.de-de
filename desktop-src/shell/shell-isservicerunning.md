---
description: Gibt einen Wert zurück, der angibt, ob ein bestimmter Dienst ausgeführt wird.
ms.assetid: FDC41C2D-7462-458f-BBE6-D97260C26B6C
title: Shell. isservicerunning-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.IsServiceRunning
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c3a65be4955c6f49e8e6baa49cd9dedb82fc5cc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865263"
---
# <a name="shellisservicerunning-method"></a><span data-ttu-id="afd76-103">Shell. isservicerunning-Methode</span><span class="sxs-lookup"><span data-stu-id="afd76-103">Shell.IsServiceRunning method</span></span>

<span data-ttu-id="afd76-104">Gibt einen Wert zurück, der angibt, ob ein bestimmter Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="afd76-104">Returns a value that indicates whether a particular service is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="afd76-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="afd76-105">Syntax</span></span>


```JScript
retVal = Shell.IsServiceRunning(
  sServiceName
)
```


```VB

Shell.IsServiceRunning( _
  ByVal sServiceName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="afd76-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="afd76-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afd76-107">*sservicename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="afd76-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afd76-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="afd76-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="afd76-109">Eine **Zeichenfolge** , die den Namen des Dienstanbieter enthält.</span><span class="sxs-lookup"><span data-stu-id="afd76-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afd76-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="afd76-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="afd76-111">JScript</span><span class="sxs-lookup"><span data-stu-id="afd76-111">JScript</span></span>

<span data-ttu-id="afd76-112">Typ: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="afd76-112">Type: \**Variant\** _</span></span>

<span data-ttu-id="afd76-113">Gibt _ *true*\* zurück, wenn der von *sservicename* angegebene Dienst ausgeführt wird. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="afd76-113">Returns _ *true*\* if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="afd76-114">VB</span><span class="sxs-lookup"><span data-stu-id="afd76-114">VB</span></span>

<span data-ttu-id="afd76-115">Typ: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="afd76-115">Type: \**Variant\** _</span></span>

<span data-ttu-id="afd76-116">Gibt _ *true*\* zurück, wenn der von *sservicename* angegebene Dienst ausgeführt wird. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="afd76-116">Returns _ *true*\* if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="afd76-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="afd76-117">Remarks</span></span>

<span data-ttu-id="afd76-118">Diese Methode ist zurzeit nicht in Microsoft Visual Basic verfügbar.</span><span class="sxs-lookup"><span data-stu-id="afd76-118">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="afd76-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="afd76-119">Examples</span></span>

<span data-ttu-id="afd76-120">In den folgenden Beispielen wird die Verwendung von **isservicerunning** veranschaulicht, um zu bestimmen, ob der Themes-Dienst für eine Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="afd76-120">The following examples show the use of **IsServiceRunning** to determine whether the Themes service is running for an application.</span></span> <span data-ttu-id="afd76-121">Die Verwendung wird für JScript und VBScript angezeigt.</span><span class="sxs-lookup"><span data-stu-id="afd76-121">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="afd76-122">JScript</span><span class="sxs-lookup"><span data-stu-id="afd76-122">JScript:</span></span>


```JScript
function fnIsServiceRunningJ()
{
    var objShell = new ActiveXObject("shell.application");
    var bReturn;

    bReturn = objShell.IsServiceRunning("Themes");
}
```



<span data-ttu-id="afd76-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="afd76-123">VBScript:</span></span>


```VB
function fnIsServiceRunningVB()
    dim objShell
    dim bReturn

    set objShell = CreateObject("shell.application")

    bReturn = objShell.IsServiceRunning("Themes")

    set objShell = nothing
end function
```



## <a name="requirements"></a><span data-ttu-id="afd76-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="afd76-124">Requirements</span></span>



| <span data-ttu-id="afd76-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="afd76-125">Requirement</span></span> | <span data-ttu-id="afd76-126">Wert</span><span class="sxs-lookup"><span data-stu-id="afd76-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afd76-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="afd76-127">Minimum supported client</span></span><br/> | <span data-ttu-id="afd76-128">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="afd76-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="afd76-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="afd76-129">Minimum supported server</span></span><br/> | <span data-ttu-id="afd76-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="afd76-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="afd76-131">Header</span><span class="sxs-lookup"><span data-stu-id="afd76-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="afd76-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="afd76-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="afd76-133">IDL</span><span class="sxs-lookup"><span data-stu-id="afd76-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="afd76-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="afd76-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="afd76-135">DLL</span><span class="sxs-lookup"><span data-stu-id="afd76-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afd76-136"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="afd76-136"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
