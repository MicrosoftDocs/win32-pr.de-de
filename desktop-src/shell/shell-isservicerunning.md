---
description: 'Shell.IsServiceRunning-Methode: Gibt einen Wert zurück, der angibt, ob ein bestimmter Dienst ausgeführt wird.'
ms.assetid: FDC41C2D-7462-458f-BBE6-D97260C26B6C
title: Shell.IsServiceRunning-Methode (Shldisp.h)
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
ms.openlocfilehash: 01af900bb7930ec7b6dde0b0700c83f211733dc3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083718"
---
# <a name="shellisservicerunning-method"></a><span data-ttu-id="578a2-103">Shell.IsServiceRunning-Methode</span><span class="sxs-lookup"><span data-stu-id="578a2-103">Shell.IsServiceRunning method</span></span>

<span data-ttu-id="578a2-104">Gibt einen Wert zurück, der angibt, ob ein bestimmter Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="578a2-104">Returns a value that indicates whether a particular service is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="578a2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="578a2-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="578a2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="578a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="578a2-107">*sServiceName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="578a2-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="578a2-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="578a2-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="578a2-109">Eine **Zeichenfolge,** die den Namen des Diensts enthält.</span><span class="sxs-lookup"><span data-stu-id="578a2-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="578a2-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="578a2-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="578a2-111">JScript</span><span class="sxs-lookup"><span data-stu-id="578a2-111">JScript</span></span>

<span data-ttu-id="578a2-112">Typ: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="578a2-112">Type: **Variant\***</span></span>

<span data-ttu-id="578a2-113">Gibt **TRUE zurück,** wenn der von *sServiceName angegebene Dienst* ausgeführt wird. andernfalls **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="578a2-113">Returns **true** if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="578a2-114">VB</span><span class="sxs-lookup"><span data-stu-id="578a2-114">VB</span></span>

<span data-ttu-id="578a2-115">Typ: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="578a2-115">Type: **Variant\***</span></span>

<span data-ttu-id="578a2-116">Gibt **TRUE zurück,** wenn der von *sServiceName angegebene Dienst* ausgeführt wird. andernfalls **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="578a2-116">Returns **true** if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="578a2-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="578a2-117">Remarks</span></span>

<span data-ttu-id="578a2-118">Diese Methode ist derzeit in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="578a2-118">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="578a2-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="578a2-119">Examples</span></span>

<span data-ttu-id="578a2-120">Die folgenden Beispiele zeigen die Verwendung von **IsServiceRunning,** um zu bestimmen, ob der Themes-Dienst für eine Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="578a2-120">The following examples show the use of **IsServiceRunning** to determine whether the Themes service is running for an application.</span></span> <span data-ttu-id="578a2-121">Die Verwendung wird für JScript und VBScript angezeigt.</span><span class="sxs-lookup"><span data-stu-id="578a2-121">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="578a2-122">Jscript:</span><span class="sxs-lookup"><span data-stu-id="578a2-122">JScript:</span></span>


```JScript
function fnIsServiceRunningJ()
{
    var objShell = new ActiveXObject("shell.application");
    var bReturn;

    bReturn = objShell.IsServiceRunning("Themes");
}
```



<span data-ttu-id="578a2-123">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="578a2-123">VBScript:</span></span>


```VB
function fnIsServiceRunningVB()
    dim objShell
    dim bReturn

    set objShell = CreateObject("shell.application")

    bReturn = objShell.IsServiceRunning("Themes")

    set objShell = nothing
end function
```



## <a name="requirements"></a><span data-ttu-id="578a2-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="578a2-124">Requirements</span></span>



| <span data-ttu-id="578a2-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="578a2-125">Requirement</span></span> | <span data-ttu-id="578a2-126">Wert</span><span class="sxs-lookup"><span data-stu-id="578a2-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="578a2-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="578a2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="578a2-128">Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="578a2-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="578a2-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="578a2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="578a2-130">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="578a2-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="578a2-131">Header</span><span class="sxs-lookup"><span data-stu-id="578a2-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="578a2-132"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="578a2-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="578a2-133">Idl</span><span class="sxs-lookup"><span data-stu-id="578a2-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="578a2-134"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="578a2-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="578a2-135">DLL</span><span class="sxs-lookup"><span data-stu-id="578a2-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="578a2-136"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="578a2-136"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
