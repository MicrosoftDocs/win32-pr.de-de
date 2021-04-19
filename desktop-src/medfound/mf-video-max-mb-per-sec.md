---
description: Gibt an, dass die maximale Makroblock-Verarbeitungsrate in Makroblöcke pro Sekunde von dem Hardware Encoder unterstützt wird.
ms.assetid: 1AA41DE3-C37C-41BA-9549-5F12373DDB3B
title: MF_VIDEO_MAX_MB_PER_SEC-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbee009b50daee074241c11750e9d25240cda153
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347010"
---
# <a name="mf_video_max_mb_per_sec-attribute"></a><span data-ttu-id="2ecda-103">MF- \_ Video \_ Max \_ MB \_ pro Sek \_ .-Attribut</span><span class="sxs-lookup"><span data-stu-id="2ecda-103">MF\_VIDEO\_MAX\_MB\_PER\_SEC attribute</span></span>

<span data-ttu-id="2ecda-104">Gibt an, dass die maximale Makroblock-Verarbeitungsrate in Makroblöcke pro [**Sekunde von dem**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)Hardware Encoder unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="2ecda-104">Specifies, on [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform), the maximum macroblock processing rate, in macroblocks per second, that is supported by the hardware encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="2ecda-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="2ecda-105">Data type</span></span>

<span data-ttu-id="2ecda-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="2ecda-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="2ecda-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ecda-107">Remarks</span></span>

<span data-ttu-id="2ecda-108">Dieses Attribut ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="2ecda-108">This is a read-only attribute.</span></span>

<span data-ttu-id="2ecda-109">**H. 264/AVC-Encoder:**</span><span class="sxs-lookup"><span data-stu-id="2ecda-109">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="2ecda-110">Dieses Attribut wird von den folgenden Eigenschaften beeinflusst:</span><span class="sxs-lookup"><span data-stu-id="2ecda-110">This attribute is affected by the following properties:</span></span>

-   <span data-ttu-id="2ecda-111">[MF \_ MT- \_ Video \_ Ebene](mf-mt-video-level.md) (die ein Alias der [MF-MT- \_ \_ \_ Ebene](mf-mt-mpeg2-level-attribute.md)ist)</span><span class="sxs-lookup"><span data-stu-id="2ecda-111">[MF\_MT\_VIDEO\_LEVEL](mf-mt-video-level.md) (which is an alias of [MF\_MT\_MPEG2\_LEVEL](mf-mt-mpeg2-level-attribute.md))</span></span>
-   [<span data-ttu-id="2ecda-112">Codecapi \_ avenccommonqualityvsspeed</span><span class="sxs-lookup"><span data-stu-id="2ecda-112">CODECAPI\_AVEncCommonQualityVsSpeed</span></span>](../directshow/avenccommonqualityvsspeed-property.md)
-   [<span data-ttu-id="2ecda-113">Codecapi \_ avencmpvdefaultbpicturecount</span><span class="sxs-lookup"><span data-stu-id="2ecda-113">CODECAPI\_AVEncMPVDefaultBPictureCount</span></span>](../directshow/avencmpvdefaultbpicturecount-property.md)

<span data-ttu-id="2ecda-114">Wenn das [MF MT-Attribut auf \_ \_ Video \_ Ebene](mf-mt-video-level.md) vorhanden ist, sollte der Encoder die Verarbeitungsrate für die höchste Bitrate und Auflösung zurückgeben, die auf der angegebenen Ebene unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="2ecda-114">If the [MF\_MT\_VIDEO\_LEVEL](mf-mt-video-level.md) attribute is present, the encoder should return the processing rate for the highest bitrate and resolution supported at the specified level.</span></span> <span data-ttu-id="2ecda-115">Wenn das MF \_ - \_ \_ Attribut auf Video Ebene nicht vorhanden ist, sollte es eine Standard Ebene von 4 verwenden.</span><span class="sxs-lookup"><span data-stu-id="2ecda-115">If the MF\_MT\_VIDEO\_LEVEL attribute is not present then it should use a default level of 4.</span></span>

<span data-ttu-id="2ecda-116">Wenn die Eigenschaft " [codecapi \_ avenccommonqualityvsspeed](../directshow/avenccommonqualityvsspeed-property.md) icodecapi" festgelegt wurde, sollte der Encoder die Verarbeitungsrate zurückgeben, die dem für diese Eigenschaft festgelegten Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="2ecda-116">If the [CODECAPI\_AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md) ICodecAPI property has been set, the encoder should return the processing rate corresponding to the value set for this property.</span></span> <span data-ttu-id="2ecda-117">Wenn das Attribut codecapi \_ avenccommonqualityvsspeed nicht vorhanden ist, sollte es den Standardwert 0 (null) verwenden, der der schnellste Verarbeitungsmodus sein sollte.</span><span class="sxs-lookup"><span data-stu-id="2ecda-117">If the CODECAPI\_AVEncCommonQualityVsSpeed attribute is not present, then it should use a default value of 0 which should be the fastest processing mode.</span></span>

<span data-ttu-id="2ecda-118">Wenn die Eigenschaft " [codecapi \_ avencmpvdefaultbpicturecount](../directshow/avencmpvdefaultbpicturecount-property.md) icodecapi" auf einen gültigen und unterstützten Wert festgelegt wurde, sollte der Encoder die Verarbeitungsrate zurückgeben, die dem für diese Eigenschaft festgelegten Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="2ecda-118">If the [CODECAPI\_AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md) ICodecAPI property has been set to a valid and supported value, the encoder should return the processing rate corresponding the value set for this property.</span></span> <span data-ttu-id="2ecda-119">Wenn das codecapi- \_ Attribut "avencmpvdefaultbpicturecount" nicht "presen" ist, sollte es einen Standardwert von 0 B-Frames verwenden.</span><span class="sxs-lookup"><span data-stu-id="2ecda-119">If the CODECAPI\_AVEncMPVDefaultBPictureCount attribute is not presen,t then it should use a default value of 0 B frames.</span></span>

<span data-ttu-id="2ecda-120">Nur die unteren 28 Bits sollten von einer Anwendung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2ecda-120">Only the lower 28 bits should be used by an application.</span></span> <span data-ttu-id="2ecda-121">Die oberen 4 Bits sind für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="2ecda-121">The upper 4bits are reserved for future use.</span></span> <span data-ttu-id="2ecda-122">Anwendungen sollten die oberen 4 Bits ignorieren, und die oberen 4 Bits sollten von MFTs auf 0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="2ecda-122">Applications should ignore the upper 4 bits and MFTs should set the upper 4 bits to 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ecda-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ecda-123">Requirements</span></span>



| <span data-ttu-id="2ecda-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2ecda-124">Requirement</span></span> | <span data-ttu-id="2ecda-125">Wert</span><span class="sxs-lookup"><span data-stu-id="2ecda-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2ecda-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2ecda-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2ecda-127">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="2ecda-127">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="2ecda-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2ecda-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2ecda-129">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="2ecda-129">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="2ecda-130">Header</span><span class="sxs-lookup"><span data-stu-id="2ecda-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ecda-131"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ecda-131"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ecda-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2ecda-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ecda-133">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="2ecda-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
