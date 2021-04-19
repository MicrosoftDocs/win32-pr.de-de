---
description: 'Windows Imaging Component (WIC)-Proxy Funktion für IEnumString:: Reset.'
ms.assetid: 084a3de0-c6de-4ce2-ba78-5d1bacb56cb0
title: IEnumString_Reset_WIC_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumString_Reset_WIC_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 64057e0f49b105232f980ac3d73014156e2da732
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348985"
---
# <a name="ienumstring_reset_wic_proxy-function"></a><span data-ttu-id="e2f7c-103">IEnumString-zurück setzung der \_ \_ WIC- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="e2f7c-103">IEnumString\_Reset\_WIC\_Proxy function</span></span>

<span data-ttu-id="e2f7c-104">Windows Imaging Component (WIC)-Proxy Funktion für IEnumString:: Reset.</span><span class="sxs-lookup"><span data-stu-id="e2f7c-104">Windows Imaging Component (WIC) proxy function for IEnumString::Reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2f7c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2f7c-105">Syntax</span></span>


```C++
HRESULT IEnumString_Reset_WIC_Proxy(
  _In_  IEnumString *THIS_PTR,
  _In_  ULONG       celt,
  _Out_ LPOLESTR    *rgelt,
  _Out_ ULONG       *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="e2f7c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2f7c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2f7c-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2f7c-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2f7c-108">Typ: \**IEnumString \** _</span><span class="sxs-lookup"><span data-stu-id="e2f7c-108">Type: \**IEnumString\** _</span></span>

<span data-ttu-id="e2f7c-109">Paramde</span><span class="sxs-lookup"><span data-stu-id="e2f7c-109">PARAMDESC</span></span>

</dd> <dt>

<span data-ttu-id="e2f7c-110">_celt \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2f7c-110">_celt\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2f7c-111">Typ: **ulong**</span><span class="sxs-lookup"><span data-stu-id="e2f7c-111">Type: **ULONG**</span></span>

</dd> <dt>

<span data-ttu-id="e2f7c-112">*rgelt* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e2f7c-112">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2f7c-113">Typ: \**lpolestr \** _</span><span class="sxs-lookup"><span data-stu-id="e2f7c-113">Type: \**LPOLESTR\** _</span></span>

</dd> <dt>

<span data-ttu-id="e2f7c-114">_pceltFetched \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e2f7c-114">_pceltFetched\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2f7c-115">Typ: \**ulong \** _</span><span class="sxs-lookup"><span data-stu-id="e2f7c-115">Type: \**ULONG\** _</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2f7c-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2f7c-116">Return value</span></span>

<span data-ttu-id="e2f7c-117">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="e2f7c-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="e2f7c-118">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="e2f7c-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e2f7c-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e2f7c-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2f7c-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2f7c-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="e2f7c-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="e2f7c-121">Requirements</span></span>



| <span data-ttu-id="e2f7c-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2f7c-122">Requirement</span></span> | <span data-ttu-id="e2f7c-123">Wert</span><span class="sxs-lookup"><span data-stu-id="e2f7c-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2f7c-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e2f7c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e2f7c-125">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2f7c-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="e2f7c-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e2f7c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e2f7c-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2f7c-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="e2f7c-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e2f7c-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2f7c-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2f7c-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




