---
description: Enthält einen Zeiger auf die streamattribute des verbundenen Streams auf einer hardwarebasierten Media Foundation Transformation (MFT).
ms.assetid: 7e14a02e-4cbf-45aa-a6f5-2c53b2437127
title: MFT_CONNECTED_STREAM_ATTRIBUTE-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b182cbed78f5f9851b621de72bf691bf698b70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863963"
---
# <a name="mft_connected_stream_attribute-attribute"></a><span data-ttu-id="fe193-103">Attribut Attribut des MFT- \_ verbundenen \_ Streams \_</span><span class="sxs-lookup"><span data-stu-id="fe193-103">MFT\_CONNECTED\_STREAM\_ATTRIBUTE attribute</span></span>

<span data-ttu-id="fe193-104">Enthält einen Zeiger auf die streamattribute des verbundenen Streams auf einer hardwarebasierten Media Foundation Transformation (MFT).</span><span class="sxs-lookup"><span data-stu-id="fe193-104">Contains a pointer to the stream attributes of the connected stream on a hardware-based Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="fe193-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="fe193-105">Data type</span></span>

<span data-ttu-id="fe193-106">**Imfattributes \** _ als " _*IUnknown \*\* " gespeichert_</span><span class="sxs-lookup"><span data-stu-id="fe193-106">**IMFAttributes\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="fe193-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="fe193-107">Get/set</span></span>

<span data-ttu-id="fe193-108">Um dieses Attribut abzurufen, nennen Sie [_ *imfattributes:: getunknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="fe193-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="fe193-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="fe193-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="fe193-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe193-110">Remarks</span></span>

<span data-ttu-id="fe193-111">Anwendungen verwenden dieses Attribut in der Regel nicht.</span><span class="sxs-lookup"><span data-stu-id="fe193-111">Applications typically do not use this attribute.</span></span>

<span data-ttu-id="fe193-112">Dieses Attribut wird für MFTs verwendet, die als Proxys für ein Hardware Gerät fungieren.</span><span class="sxs-lookup"><span data-stu-id="fe193-112">This attribute is used for MFTs that act as proxies to a hardware device.</span></span> <span data-ttu-id="fe193-113">Weitere Informationen finden Sie unter [Hardware-MFTs](hardware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="fe193-113">For details, see [Hardware MFTs](hardware-mfts.md).</span></span>

<span data-ttu-id="fe193-114">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="fe193-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe193-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe193-115">Requirements</span></span>



| <span data-ttu-id="fe193-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe193-116">Requirement</span></span> | <span data-ttu-id="fe193-117">Wert</span><span class="sxs-lookup"><span data-stu-id="fe193-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe193-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fe193-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fe193-119">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="fe193-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="fe193-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fe193-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fe193-121">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="fe193-121">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="fe193-122">Header</span><span class="sxs-lookup"><span data-stu-id="fe193-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe193-123"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="fe193-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe193-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe193-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe193-125">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="fe193-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fe193-126">mit \_ \_ dem HW- \_ \_ Stream verbundene MFT</span><span class="sxs-lookup"><span data-stu-id="fe193-126">MFT\_CONNECTED\_TO\_HW\_STREAM</span></span>](mft-connected-to-hw-stream.md)
</dt> <dt>

[<span data-ttu-id="fe193-127">Hardware-MFTs</span><span class="sxs-lookup"><span data-stu-id="fe193-127">Hardware MFTs</span></span>](hardware-mfts.md)
</dt> <dt>

[<span data-ttu-id="fe193-128">Transformations Attribute</span><span class="sxs-lookup"><span data-stu-id="fe193-128">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




