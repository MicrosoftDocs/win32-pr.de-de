---
title: IMsRdpCameraRedirConfigCollection EncodingQuality-Eigenschaft
description: Gibt die Codierungsqualität an (Bitrate).
ms.tgt_platform: multiple
keywords:
- Encodingquality-Eigenschaft Remotedesktopdienste
- Encodingquality-Eigenschaft Remotedesktopdienste, imsrdpcameraredirconfigcollection-Schnittstelle
- Imsrdpcameraredirconfigcollection-Schnittstelle Remotedesktopdienste, encodingquality-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.EncodingQuality
- IMsRdpCameraRedirConfigCollection.put_EncodingQuality
- IMsRdpCameraRedirConfigCollection.get_EncodingQuality
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d8044c2fb70233243a3a74d8dc5faac96873cb48
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "104480539"
---
# <a name="imsrdpcameraredirconfigcollectionencodingquality-property"></a><span data-ttu-id="840ff-106">Imsrdpcameraredirconfigcollection:: encodingquality (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="840ff-106">IMsRdpCameraRedirConfigCollection::EncodingQuality property</span></span>

<span data-ttu-id="840ff-107">Gibt die Codierungsqualität an (Bitrate).</span><span class="sxs-lookup"><span data-stu-id="840ff-107">Specifies the encoding quality (bit rate).</span></span>

<span data-ttu-id="840ff-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="840ff-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="840ff-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="840ff-109">Syntax</span></span>

```C++
HRESULT put_EncodingQuality(
    [in] CameraRedirEncodingQuality encodingQuality
);

HRESULT get_EncodingQuality(
    [out, retval] CameraRedirEncodingQuality* pEncodingQuality
);
```

## <a name="property-value"></a><span data-ttu-id="840ff-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="840ff-110">Property value</span></span>

<span data-ttu-id="840ff-111">Einer der folgenden **cameraredirencodingquality** -Enumerationswerte, der die Codierungsqualität angibt (Bitrate).</span><span class="sxs-lookup"><span data-stu-id="840ff-111">One of the following **CameraRedirEncodingQuality** enum values that specifies the encoding quality (bit rate).</span></span>

| <span data-ttu-id="840ff-112">Enum-Elementname</span><span class="sxs-lookup"><span data-stu-id="840ff-112">Enum member name</span></span> | <span data-ttu-id="840ff-113">Wert</span><span class="sxs-lookup"><span data-stu-id="840ff-113">Value</span></span> |
|-----------------|--------|
| <span data-ttu-id="840ff-114">encodingqualitylow</span><span class="sxs-lookup"><span data-stu-id="840ff-114">encodingQualityLow</span></span> | <span data-ttu-id="840ff-115">0x0000</span><span class="sxs-lookup"><span data-stu-id="840ff-115">0x0000</span></span> |
| <span data-ttu-id="840ff-116">encodingqualitymedium</span><span class="sxs-lookup"><span data-stu-id="840ff-116">encodingQualityMedium</span></span> | <span data-ttu-id="840ff-117">0x0001</span><span class="sxs-lookup"><span data-stu-id="840ff-117">0x0001</span></span> |
| <span data-ttu-id="840ff-118">encodingqualityhigh</span><span class="sxs-lookup"><span data-stu-id="840ff-118">encodingQualityHigh</span></span> | <span data-ttu-id="840ff-119">0x0002</span><span class="sxs-lookup"><span data-stu-id="840ff-119">0x0002</span></span> |

## <a name="requirements"></a><span data-ttu-id="840ff-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="840ff-120">Requirements</span></span>

| <span data-ttu-id="840ff-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="840ff-121">Requirement</span></span> | <span data-ttu-id="840ff-122">Wert</span><span class="sxs-lookup"><span data-stu-id="840ff-122">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="840ff-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="840ff-123">Minimum supported client</span></span>| <span data-ttu-id="840ff-124">Windows 10, Version 1803 (Build 17134)</span><span class="sxs-lookup"><span data-stu-id="840ff-124">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="840ff-125">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="840ff-125">Type library</span></span>            | <span data-ttu-id="840ff-126">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="840ff-126">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="840ff-127">DLL</span><span class="sxs-lookup"><span data-stu-id="840ff-127">DLL</span></span>                  | <span data-ttu-id="840ff-128">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="840ff-128">MsTscAx.dll</span></span>     |
| <span data-ttu-id="840ff-129">IID</span><span class="sxs-lookup"><span data-stu-id="840ff-129">IID</span></span>                      | <span data-ttu-id="840ff-130">IID \_ imsrdpcameraredirconfigcollection ist als AE45252B-aaab-4504-B681-649d6073a37a definiert.</span><span class="sxs-lookup"><span data-stu-id="840ff-130">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="840ff-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="840ff-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="840ff-132">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="840ff-132">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>