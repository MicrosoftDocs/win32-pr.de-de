---
description: 'IShellDispatch2.IsServiceRunning-Methode: Gibt einen Wert zurück, der angibt, ob ein bestimmter Dienst ausgeführt wird.'
ms.assetid: 91f3fba1-7aa5-423a-bc37-49db230c79db
title: IShellDispatch2.IsServiceRunning-Methode (Shldisp.h)
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
ms.openlocfilehash: e8ad792f1669a8ebcfa411c58b34da214ccf69a7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117088"
---
# <a name="ishelldispatch2isservicerunning-method"></a><span data-ttu-id="1d9a5-103">IShellDispatch2.IsServiceRunning-Methode</span><span class="sxs-lookup"><span data-stu-id="1d9a5-103">IShellDispatch2.IsServiceRunning method</span></span>

<span data-ttu-id="1d9a5-104">Gibt einen Wert zurück, der angibt, ob ein bestimmter Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1d9a5-104">Returns a value that indicates whether a particular service is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d9a5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d9a5-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="1d9a5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d9a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d9a5-107">*sServiceName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1d9a5-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d9a5-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="1d9a5-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="1d9a5-109">Eine **Zeichenfolge,** die den Namen des Diensts enthält.</span><span class="sxs-lookup"><span data-stu-id="1d9a5-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d9a5-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1d9a5-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="1d9a5-111">JScript</span><span class="sxs-lookup"><span data-stu-id="1d9a5-111">JScript</span></span>

<span data-ttu-id="1d9a5-112">Typ: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="1d9a5-112">Type: **Variant\***</span></span>

<span data-ttu-id="1d9a5-113">Gibt **TRUE zurück,** wenn der von *sServiceName angegebene Dienst* ausgeführt wird. andernfalls **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="1d9a5-113">Returns **true** if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="1d9a5-114">VB</span><span class="sxs-lookup"><span data-stu-id="1d9a5-114">VB</span></span>

<span data-ttu-id="1d9a5-115">Typ: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="1d9a5-115">Type: **Variant\***</span></span>

<span data-ttu-id="1d9a5-116">Gibt **TRUE zurück,** wenn der von *sServiceName angegebene Dienst* ausgeführt wird. andernfalls **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="1d9a5-116">Returns **true** if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d9a5-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d9a5-117">Remarks</span></span>

<span data-ttu-id="1d9a5-118">Diese Methode wird implementiert und über die [**Shell.IsServiceRunning-Methode aufgerufen.**](./shell-isservicerunning.md)</span><span class="sxs-lookup"><span data-stu-id="1d9a5-118">This method is implemented and accessed through the [**Shell.IsServiceRunning**](./shell-isservicerunning.md) method.</span></span>

<span data-ttu-id="1d9a5-119">Diese Methode ist derzeit in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1d9a5-119">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="1d9a5-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1d9a5-120">Examples</span></span>

<span data-ttu-id="1d9a5-121">Die folgenden Beispiele zeigen die Verwendung von **IsServiceRunning,** um zu bestimmen, ob der Themes-Dienst für eine Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1d9a5-121">The following examples show the use of **IsServiceRunning** to determine whether the Themes service is running for an application.</span></span> <span data-ttu-id="1d9a5-122">Die Verwendung wird für JScript und VBScript angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1d9a5-122">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="1d9a5-123">Jscript:</span><span class="sxs-lookup"><span data-stu-id="1d9a5-123">JScript:</span></span>


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



<span data-ttu-id="1d9a5-124">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="1d9a5-124">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="1d9a5-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d9a5-125">Requirements</span></span>



| <span data-ttu-id="1d9a5-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d9a5-126">Requirement</span></span> | <span data-ttu-id="1d9a5-127">Wert</span><span class="sxs-lookup"><span data-stu-id="1d9a5-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d9a5-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1d9a5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1d9a5-129">Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d9a5-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1d9a5-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1d9a5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1d9a5-131">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d9a5-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1d9a5-132">Header</span><span class="sxs-lookup"><span data-stu-id="1d9a5-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d9a5-133"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="1d9a5-133"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="1d9a5-134">Idl</span><span class="sxs-lookup"><span data-stu-id="1d9a5-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1d9a5-135"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="1d9a5-135"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="1d9a5-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1d9a5-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d9a5-137"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="1d9a5-137"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
