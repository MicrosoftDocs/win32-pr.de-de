---
description: 'Windows Imaging Component (WIC)-Proxy Funktion für IPropertyBag2:: Write.'
ms.assetid: b97caba6-298a-4b36-9f39-9b5440b866c3
title: IPropertyBag2_Write_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertyBag2_Write_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c868ee748c3c2894daa63850284ae121f85975fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343249"
---
# <a name="ipropertybag2_write_proxy-function"></a><span data-ttu-id="5a9db-103">IPropertyBag2- \_ Schreib \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="5a9db-103">IPropertyBag2\_Write\_Proxy function</span></span>

<span data-ttu-id="5a9db-104">Windows Imaging Component (WIC)-Proxy Funktion für IPropertyBag2:: Write.</span><span class="sxs-lookup"><span data-stu-id="5a9db-104">Windows Imaging Component (WIC) proxy function for IPropertyBag2::Write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a9db-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a9db-105">Syntax</span></span>


```C++
HRESULT IPropertyBag2_Write_Proxy(
  _In_ IPropertyBag2 *THIS_PTR,
  _In_ ULONG         cProperties,
  _In_ PROPBAG2      *ppropBag,
  _In_ VARIANT       *pvarValue
);
```



## <a name="parameters"></a><span data-ttu-id="5a9db-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a9db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a9db-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a9db-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a9db-108">Typ: \**[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) \** _</span><span class="sxs-lookup"><span data-stu-id="5a9db-108">Type: \**[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\** _</span></span>

<span data-ttu-id="5a9db-109">Paramde</span><span class="sxs-lookup"><span data-stu-id="5a9db-109">PARAMDESC</span></span>

</dd> <dt>

<span data-ttu-id="5a9db-110">_cProperties \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a9db-110">_cProperties\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a9db-111">Typ: **ulong**</span><span class="sxs-lookup"><span data-stu-id="5a9db-111">Type: **ULONG**</span></span>

</dd> <dt>

<span data-ttu-id="5a9db-112">*ppropbag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a9db-112">*ppropBag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a9db-113">Typ: \**[PROPBAG2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768188(v=vs.85)) \** _</span><span class="sxs-lookup"><span data-stu-id="5a9db-113">Type: \**[PROPBAG2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768188(v=vs.85))\** _</span></span>

</dd> <dt>

<span data-ttu-id="5a9db-114">_pvarValue \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a9db-114">_pvarValue\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a9db-115">Typ: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="5a9db-115">Type: \**VARIANT\** _</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a9db-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5a9db-116">Return value</span></span>

<span data-ttu-id="5a9db-117">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="5a9db-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="5a9db-118">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="5a9db-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5a9db-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5a9db-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a9db-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a9db-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="5a9db-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="5a9db-121">Requirements</span></span>



| <span data-ttu-id="5a9db-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5a9db-122">Requirement</span></span> | <span data-ttu-id="5a9db-123">Wert</span><span class="sxs-lookup"><span data-stu-id="5a9db-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a9db-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5a9db-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5a9db-125">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5a9db-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="5a9db-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5a9db-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5a9db-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5a9db-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="5a9db-128">DLL</span><span class="sxs-lookup"><span data-stu-id="5a9db-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a9db-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a9db-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

