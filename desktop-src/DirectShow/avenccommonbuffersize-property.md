---
description: Gibt die Größe des Puffers an, der während der Codierung verwendet wird. Diese Eigenschaft gilt nur für die Konstante Bitrate (CBR) und die Variablen Bitrate (VBR)-Codierungs Modi.
ms.assetid: 3315785e-306f-44d6-ac39-796025a2da3a
title: Avenccommonbuffersize-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c677c483c320c9dceef391f45c5d8bf163eece0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125251"
---
# <a name="avenccommonbuffersize-property"></a><span data-ttu-id="6b686-104">Avenccommonbuffersize (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6b686-104">AVEncCommonBufferSize property</span></span>

<span data-ttu-id="6b686-105">Gibt die Größe des Puffers an, der während der Codierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6b686-105">Specifies the size of the buffer used during encoding.</span></span> <span data-ttu-id="6b686-106">Diese Eigenschaft gilt nur für die Konstante Bitrate (CBR) und die Variablen Bitrate (VBR)-Codierungs Modi.</span><span class="sxs-lookup"><span data-stu-id="6b686-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="6b686-107">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="6b686-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="6b686-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="6b686-108">Data type</span></span>

<span data-ttu-id="6b686-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="6b686-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="6b686-110">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="6b686-110">Property GUID</span></span>

<span data-ttu-id="6b686-111">**Codecapi \_ avenccommonbuffersize**</span><span class="sxs-lookup"><span data-stu-id="6b686-111">**CODECAPI\_AVEncCommonBufferSize**</span></span>

## <a name="property-value"></a><span data-ttu-id="6b686-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6b686-112">Property value</span></span>

<span data-ttu-id="6b686-113">Diese Eigenschaft verfügt über einen linearen Wertebereich.</span><span class="sxs-lookup"><span data-stu-id="6b686-113">This property has a linear range of values.</span></span> <span data-ttu-id="6b686-114">Um den unterstützten Bereich abzurufen, nennen Sie [**icodecapi:: getparameterrange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="6b686-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span> <span data-ttu-id="6b686-115">Parameter Bereiche werden für H. 264 UVC 1,5-Kamera Encoder nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6b686-115">Parameter ranges are not supported for H.264 UVC 1.5 camera encoders.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b686-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b686-116">Remarks</span></span>

<span data-ttu-id="6b686-117">Bei einigen Videoformaten wird die Puffergröße in Bits und für andere in Bytes angegeben.</span><span class="sxs-lookup"><span data-stu-id="6b686-117">For some video formats the buffer size is specified in bits and for others it is specified in bytes.</span></span> <span data-ttu-id="6b686-118">Informationen zu bestimmten Informationen finden Sie in den nachfolgenden hinweisen.</span><span class="sxs-lookup"><span data-stu-id="6b686-118">See the remarks below for specific information.</span></span>

<span data-ttu-id="6b686-119">Bei MPEG-Videos definiert diese Eigenschaft die vbv-Puffergröße (Video Buffer Verifier).</span><span class="sxs-lookup"><span data-stu-id="6b686-119">For MPEG video, this property defines the video buffer verifier (VBV) buffer size.</span></span> <span data-ttu-id="6b686-120">Die Größe des Puffers ist in Bits.</span><span class="sxs-lookup"><span data-stu-id="6b686-120">The size of the buffer is in bits.</span></span>

<span data-ttu-id="6b686-121">Bei H. 264-Videos und-Windows Media Video definiert die-Eigenschaft die Größe des hypothetischen Verweis Decoders (HRD).</span><span class="sxs-lookup"><span data-stu-id="6b686-121">For H.264 video and Windows Media Video, the property defines the hypothetical reference decoder (HRD) size.</span></span> <span data-ttu-id="6b686-122">Die Größe des Puffers beträgt Byte.</span><span class="sxs-lookup"><span data-stu-id="6b686-122">The size of the buffer is in bytes.</span></span>

<span data-ttu-id="6b686-123">Für UVC 1,5 H264 Encoding-Kameras muss der an den Kamera Encoder gesendete CPB-Wert 16-Bit-ausgerichtet sein.</span><span class="sxs-lookup"><span data-stu-id="6b686-123">For UVC 1.5 H264 encoding cameras, the CPB value sent to the camera encoder must be 16-bit aligned.</span></span> <span data-ttu-id="6b686-124">Die Größe des Puffers beträgt Byte.</span><span class="sxs-lookup"><span data-stu-id="6b686-124">The size of the buffer is in bytes.</span></span>

<span data-ttu-id="6b686-125">Diese Eigenschaft wird auch mit [H. 264 UVC 1,5-Kamera Codierern](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5)verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b686-125">This property is also used with [H.264 UVC 1.5 camera encoders](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span></span>

## <a name="requirements"></a><span data-ttu-id="6b686-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b686-126">Requirements</span></span>



| <span data-ttu-id="6b686-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b686-127">Requirement</span></span> | <span data-ttu-id="6b686-128">Wert</span><span class="sxs-lookup"><span data-stu-id="6b686-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b686-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b686-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6b686-130">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="6b686-130">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="6b686-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b686-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6b686-132">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="6b686-132">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="6b686-133">Header</span><span class="sxs-lookup"><span data-stu-id="6b686-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b686-134"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b686-134"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b686-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b686-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b686-136">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="6b686-136">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="6b686-137">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="6b686-137">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

