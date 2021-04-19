---
description: Gibt die Anzahl von nicht komprimierten Puffern an, die von der gesteigerten Video-Renderer (EVR) für Deinterlacing benötigt werden.
ms.assetid: b62bff64-153f-4028-a546-250419dc4152
title: MF_SA_REQUIRED_SAMPLE_COUNT-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbe7d47370cd4877a0f9722d443bc6bb3f7bdeb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351753"
---
# <a name="mf_sa_required_sample_count-attribute"></a><span data-ttu-id="7b34b-103">\_ \_ Anzahl erforderlicher \_ \_ Attribute der MF-SA</span><span class="sxs-lookup"><span data-stu-id="7b34b-103">MF\_SA\_REQUIRED\_SAMPLE\_COUNT attribute</span></span>

<span data-ttu-id="7b34b-104">Gibt die Anzahl von nicht komprimierten Puffern an, die von der gesteigerten Video-Renderer (EVR) für Deinterlacing benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="7b34b-104">Indicates the number of uncompressed buffers that the enhanced video renderer (EVR) media sink requires for deinterlacing.</span></span>

## <a name="data-type"></a><span data-ttu-id="7b34b-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="7b34b-105">Data type</span></span>

<span data-ttu-id="7b34b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7b34b-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="7b34b-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7b34b-107">Remarks</span></span>

<span data-ttu-id="7b34b-108">Dabei handelt es sich um ein Attribut auf Streamebene.</span><span class="sxs-lookup"><span data-stu-id="7b34b-108">This is a stream-level attribute.</span></span> <span data-ttu-id="7b34b-109">Gehen Sie folgendermaßen vor, um das-Attribut aus dem EVR zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="7b34b-109">To get the attribute from the EVR, do the following:</span></span>

1.  <span data-ttu-id="7b34b-110">Aufrufen von [**imfmediasink:: getstreamsinkbyindex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) zum Abrufen der streamsenke.</span><span class="sxs-lookup"><span data-stu-id="7b34b-110">Call [**IMFMediaSink::GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) to get the stream sink.</span></span>
2.  <span data-ttu-id="7b34b-111">Abfragen der streamsenke für die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7b34b-111">Query the stream sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>
3.  <span data-ttu-id="7b34b-112">Rückrufe [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="7b34b-112">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="7b34b-113">Intern wird dieses Attribut vom Mixer dem EVR bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="7b34b-113">Internally, the mixer provides this attribute to the EVR.</span></span> <span data-ttu-id="7b34b-114">Um das Attribut vom Mixer abzurufen, nennen Sie [**imftransform:: getinputstreamattributs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes).</span><span class="sxs-lookup"><span data-stu-id="7b34b-114">To get the attribute from the mixer, call [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes).</span></span>

<span data-ttu-id="7b34b-115">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="7b34b-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b34b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b34b-116">Requirements</span></span>



| <span data-ttu-id="7b34b-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b34b-117">Requirement</span></span> | <span data-ttu-id="7b34b-118">Wert</span><span class="sxs-lookup"><span data-stu-id="7b34b-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b34b-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7b34b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7b34b-120">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="7b34b-120">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                    |
| <span data-ttu-id="7b34b-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7b34b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7b34b-122">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="7b34b-122">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="7b34b-123">Header</span><span class="sxs-lookup"><span data-stu-id="7b34b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b34b-124"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="7b34b-124"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b34b-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b34b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b34b-126">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="7b34b-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7b34b-127">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="7b34b-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="7b34b-128">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="7b34b-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="7b34b-129">Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="7b34b-129">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




