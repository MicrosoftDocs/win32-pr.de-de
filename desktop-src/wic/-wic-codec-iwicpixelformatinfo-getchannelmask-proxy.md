---
description: Proxy Funktion für die getchannelmask-Methode.
ms.assetid: c96e6078-4648-4333-8a25-bcb03a2cd50b
title: IWICPixelFormatInfo_GetChannelMask_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPixelFormatInfo_GetChannelMask_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0db2c14e89aba2b13cb95209b81f6d0da5d9d949
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218039"
---
# <a name="iwicpixelformatinfo_getchannelmask_proxy-function"></a><span data-ttu-id="a15d3-103">Iwicpixelformatinfo- \_ Funktion "getchannelmask" \_</span><span class="sxs-lookup"><span data-stu-id="a15d3-103">IWICPixelFormatInfo\_GetChannelMask\_Proxy function</span></span>

<span data-ttu-id="a15d3-104">Proxy Funktion für die [**getchannelmask**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelmask) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a15d3-104">Proxy function for the [**GetChannelMask**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelmask) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a15d3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a15d3-105">Syntax</span></span>


```C++
HRESULT IWICPixelFormatInfo_GetChannelMask_Proxy(
  _In_    IWICPixelFormatInfo *THIS_PTR,
  _In_    UINT                uiChannelIndex,
  _In_    UINT                cbMaskBuffer,
  _Inout_ BYTE                *pbMaskBuffer,
  _Out_   UINT                *pcbActual
);
```



## <a name="parameters"></a><span data-ttu-id="a15d3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a15d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a15d3-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a15d3-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a15d3-108">Typ: \**[**iwicpixelformatinfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="a15d3-108">Type: \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)\** _</span></span>

<span data-ttu-id="a15d3-109">Zeiger auf dieses [_ *iwicpixelformatinfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="a15d3-109">Pointer to this [_ *IWICPixelFormatInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="a15d3-110">*uichannelindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a15d3-110">*uiChannelIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a15d3-111">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="a15d3-111">Type: **UINT**</span></span>

<span data-ttu-id="a15d3-112">Der Index für die abzurufende Kanalmaske.</span><span class="sxs-lookup"><span data-stu-id="a15d3-112">The index to the channel mask to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="a15d3-113">*cbmaskbuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a15d3-113">*cbMaskBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a15d3-114">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="a15d3-114">Type: **UINT**</span></span>

<span data-ttu-id="a15d3-115">Die Größe des *pbmaskbuffer* -Puffers.</span><span class="sxs-lookup"><span data-stu-id="a15d3-115">The size of the *pbMaskBuffer* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a15d3-116">*pbmaskbuffer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a15d3-116">*pbMaskBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a15d3-117">Typ: \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="a15d3-117">Type: \**BYTE\** _</span></span>

<span data-ttu-id="a15d3-118">Zeiger auf den Masken Puffer.</span><span class="sxs-lookup"><span data-stu-id="a15d3-118">Pointer to the mask buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a15d3-119">_pcbActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a15d3-119">_pcbActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a15d3-120">Typ: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="a15d3-120">Type: \**UINT\** _</span></span>

<span data-ttu-id="a15d3-121">Die tatsächliche Puffergröße, die zum Abrufen der Kanalmaske benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="a15d3-121">The actual buffer size needed to obtain the channel mask.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a15d3-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a15d3-122">Return value</span></span>

<span data-ttu-id="a15d3-123">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="a15d3-123">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="a15d3-124">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="a15d3-124">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a15d3-125">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a15d3-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a15d3-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a15d3-126">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a15d3-127">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a15d3-127">Requirements</span></span>



| <span data-ttu-id="a15d3-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a15d3-128">Requirement</span></span> | <span data-ttu-id="a15d3-129">Wert</span><span class="sxs-lookup"><span data-stu-id="a15d3-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a15d3-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a15d3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a15d3-131">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a15d3-131">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a15d3-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a15d3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a15d3-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a15d3-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a15d3-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a15d3-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a15d3-135"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a15d3-135"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




