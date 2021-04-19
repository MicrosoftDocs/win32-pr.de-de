---
description: Zwingt den Encoder, den nächsten Frame als Keyframe zu codieren.
ms.assetid: 1E252967-6C28-4DA3-9E64-BD276E475753
title: CODECAPI_AVEncVideoForceKeyFrame-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d72c555d5680e822e9a8308b3e143a754eb22b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346883"
---
# <a name="codecapi_avencvideoforcekeyframe-property"></a><span data-ttu-id="90f17-103">Codecapi \_ avencvideoforcekeyframe (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="90f17-103">CODECAPI\_AVEncVideoForceKeyFrame property</span></span>

<span data-ttu-id="90f17-104">Zwingt den Encoder, den nächsten Frame als Keyframe zu codieren.</span><span class="sxs-lookup"><span data-stu-id="90f17-104">Forces the encoder to code the next frame as a key frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="90f17-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="90f17-105">Data type</span></span>

<span data-ttu-id="90f17-106">**Ulong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="90f17-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="90f17-107">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="90f17-107">Property GUID</span></span>

<span data-ttu-id="90f17-108">**Codecapi \_ avencvideoforcekeyframe**</span><span class="sxs-lookup"><span data-stu-id="90f17-108">**CODECAPI\_AVEncVideoForceKeyFrame**</span></span>

## <a name="property-value"></a><span data-ttu-id="90f17-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="90f17-109">Property value</span></span>

<span data-ttu-id="90f17-110">Wenn der Wert ungleich 0 (null) ist, codiert der Encoder den nächsten Frame als Keyframe.</span><span class="sxs-lookup"><span data-stu-id="90f17-110">If the value is nonzero, the encoder will code the next frame as a key frame.</span></span> <span data-ttu-id="90f17-111">Wenn der Wert 0 (null) ist, wählt der Encoder aus, ob der nächste Frame als Keyframe codiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="90f17-111">If the value is zero, the encoder selects whether to encode the next frame as a key frame.</span></span>

<span data-ttu-id="90f17-112">Diese Eigenschaft gilt für den nächsten Frame, den der Encoder als Eingabe empfängt.</span><span class="sxs-lookup"><span data-stu-id="90f17-112">This property applies to the next frame that the encoder receives as input.</span></span> <span data-ttu-id="90f17-113">Bei einer Media Foundation Transformation (MFT) ist dies der nächste Frame, der an die [**imftransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) -Methode weitergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="90f17-113">For a Media Foundation transform (MFT), this is the next frame that is passed to the [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) method.</span></span> <span data-ttu-id="90f17-114">Die Einstellung wird nach dem nächsten Frame auf 0 (null) zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="90f17-114">The setting resets to zero after the next frame.</span></span>

## <a name="remarks"></a><span data-ttu-id="90f17-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90f17-115">Remarks</span></span>

<span data-ttu-id="90f17-116">Diese Eigenschaft wird auch mit [H. 264 UVC 1,5-Kamera Codierern](camera-encoder-h264-uvc-1-5.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="90f17-116">This property is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="90f17-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90f17-117">Requirements</span></span>



| <span data-ttu-id="90f17-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="90f17-118">Requirement</span></span> | <span data-ttu-id="90f17-119">Wert</span><span class="sxs-lookup"><span data-stu-id="90f17-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90f17-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="90f17-120">Minimum supported client</span></span><br/> | <span data-ttu-id="90f17-121">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="90f17-121">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="90f17-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="90f17-122">Minimum supported server</span></span><br/> | <span data-ttu-id="90f17-123">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="90f17-123">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="90f17-124">Header</span><span class="sxs-lookup"><span data-stu-id="90f17-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="90f17-125"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="90f17-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90f17-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90f17-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90f17-127">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="90f17-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="90f17-128">**Icodecapi**</span><span class="sxs-lookup"><span data-stu-id="90f17-128">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

