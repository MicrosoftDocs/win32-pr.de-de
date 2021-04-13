---
description: Ermöglicht die erweiterte Videoverarbeitung durch den Quell Leser, einschließlich der Farb Raum Konvertierung, der Deinterlacing, der Videogröße und der Konvertierung von Frameraten.
ms.assetid: 1055CD55-4B25-4EEC-AF1B-C84C52287F8F
title: MF_SOURCE_READER_ENABLE_ADVANCED_VIDEO_PROCESSING-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6978239c5c1c466c78a310b38b5d10bd41f9e004
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525997"
---
# <a name="mf_source_reader_enable_advanced_video_processing-attribute"></a><span data-ttu-id="b2046-103">MF- \_ Quell \_ Leser Aktivieren des \_ \_ erweiterten \_ Video \_ Verarbeitungs Attributs</span><span class="sxs-lookup"><span data-stu-id="b2046-103">MF\_SOURCE\_READER\_ENABLE\_ADVANCED\_VIDEO\_PROCESSING attribute</span></span>

<span data-ttu-id="b2046-104">Ermöglicht die erweiterte Videoverarbeitung durch den [Quell Leser](source-reader.md), einschließlich der Farb Raum Konvertierung, der Deinterlacing, der Videogröße und der Konvertierung von Frameraten.</span><span class="sxs-lookup"><span data-stu-id="b2046-104">Enables advanced video processing by the [Source Reader](source-reader.md), including color space conversion, deinterlacing, video resizing, and frame-rate conversion.</span></span>

## <a name="data-type"></a><span data-ttu-id="b2046-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b2046-105">Data type</span></span>

<span data-ttu-id="b2046-106">**Bool** gespeichert als **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b2046-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="b2046-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2046-107">Remarks</span></span>

<span data-ttu-id="b2046-108">Wenn dieses Attribut **true** ist, kann der Quell Leser einen Videoprozessor in die Verarbeitungs Pipeline einfügen, wodurch die folgenden Typen von Formatkonvertierungen aktiviert werden:</span><span class="sxs-lookup"><span data-stu-id="b2046-108">If this attribute is **TRUE**, the Source Reader can insert a video processor into the processing pipeline, which enables the following types of format conversion:</span></span>

-   <span data-ttu-id="b2046-109">Farb Raum Konvertierung (YUV in RGB-32)</span><span class="sxs-lookup"><span data-stu-id="b2046-109">Color space conversion (YUV to RGB-32)</span></span>
-   <span data-ttu-id="b2046-110">Deinterlacing</span><span class="sxs-lookup"><span data-stu-id="b2046-110">Deinterlacing</span></span>
-   <span data-ttu-id="b2046-111">Ändern der Größe von Videos</span><span class="sxs-lookup"><span data-stu-id="b2046-111">Video resizing</span></span>
-   <span data-ttu-id="b2046-112">Umwandlung von Frame Raten</span><span class="sxs-lookup"><span data-stu-id="b2046-112">Frame-rate conversion</span></span>

<span data-ttu-id="b2046-113">Wenn dieses Attribut **true** ist, muss das MF-Attribut "read [ \_ Write \_ deaktivierte \_ Konverter](mf-readwrite-disable-converters.md) " den Wert **false** aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b2046-113">If this attribute is **TRUE**, the [MF\_READWRITE\_DISABLE\_CONVERTERS](mf-readwrite-disable-converters.md) attribute must be **FALSE**.</span></span>

<span data-ttu-id="b2046-114">Der Quell Leser sucht nach Video Prozessoren, die in der Kategorie **\_ \_ Video \_ Prozessor Kategorie der Kategorie MFT** registriert sind, einschließlich der für den lokalen Prozess registrierten MFTs.</span><span class="sxs-lookup"><span data-stu-id="b2046-114">The Source Reader looks for video processors that are registered in the **MFT\_CATEGORY\_VIDEO\_PROCESSOR** category, including MFTs that are registered for the local process.</span></span> <span data-ttu-id="b2046-115">(Weitere Informationen zur lokalen Registrierung von MFTs finden Sie unter [**MF tregisterlocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) .) Der Quell Leser verwendet den Transcode-Videoprozessor (xvp), wenn kein anderer geeigneter Videoprozessor gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="b2046-115">(See [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) for more information about local registration of MFTs.) The Source Reader uses the Transcode Video Processor (XVP) if no other suitable video processor is found.</span></span>

<span data-ttu-id="b2046-116">Die Anwendung gibt den gewünschten Ausgabetyp an, indem [**imfsourcereader:: setcurrentmediatype**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b2046-116">The application specifies the desired output type by calling [**IMFSourceReader::SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype).</span></span> <span data-ttu-id="b2046-117">Wenn der Quell Leser den Videoprozessor konfiguriert, versucht er, die folgenden Attribute des Ausgabe Typs abzugleichen:</span><span class="sxs-lookup"><span data-stu-id="b2046-117">When the Source Reader configures the video processor, it attempts to match the following attributes of the output type:</span></span>

-   <span data-ttu-id="b2046-118">Frame Rate ([MF- \_ MT-Frame- \_ \_ Rate](mf-mt-frame-rate-attribute.md))</span><span class="sxs-lookup"><span data-stu-id="b2046-118">Frame rate ([MF\_MT\_FRAME\_RATE](mf-mt-frame-rate-attribute.md))</span></span>
-   <span data-ttu-id="b2046-119">Frame Größe ([MF- \_ MT- \_ Rahmen \_ Größe](mf-mt-frame-size-attribute.md))</span><span class="sxs-lookup"><span data-stu-id="b2046-119">Frame size ([MF\_MT\_FRAME\_SIZE](mf-mt-frame-size-attribute.md))</span></span>
-   <span data-ttu-id="b2046-120">Interlace-Modus ([MF- \_ MT- \_ Interlace- \_ Modus](mf-mt-interlace-mode-attribute.md))</span><span class="sxs-lookup"><span data-stu-id="b2046-120">Interlace mode ([MF\_MT\_INTERLACE\_MODE](mf-mt-interlace-mode-attribute.md))</span></span>
-   <span data-ttu-id="b2046-121">Pixel Seitenverhältnis ([MF- \_ MT-Pixel- \_ \_ Seiten \_ Verhältnis](mf-mt-pixel-aspect-ratio-attribute.md))</span><span class="sxs-lookup"><span data-stu-id="b2046-121">Pixel aspect ratio ([MF\_MT\_PIXEL\_ASPECT\_RATIO](mf-mt-pixel-aspect-ratio-attribute.md))</span></span>
-   <span data-ttu-id="b2046-122">Untertyp ([MF- \_ MT- \_ Untertyp](mf-mt-subtype-attribute.md))</span><span class="sxs-lookup"><span data-stu-id="b2046-122">Subtype ([MF\_MT\_SUBTYPE](mf-mt-subtype-attribute.md))</span></span>

<span data-ttu-id="b2046-123">Dieses Attribut ähnelt dem MF- [ \_ Quell \_ Lesegerät zum \_ Aktivieren von \_ Video \_ Verarbeitungs](mf-source-reader-enable-video-processing.md) Attributen, bietet jedoch die folgenden Vorteile:</span><span class="sxs-lookup"><span data-stu-id="b2046-123">This attribute is similar to the [MF\_SOURCE\_READER\_ENABLE\_VIDEO\_PROCESSING](mf-source-reader-enable-video-processing.md) attribute, but offers the following advantages:</span></span>

-   <span data-ttu-id="b2046-124">Es wird ein größerer Bereich von Formatkonvertierungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b2046-124">A greater range of format conversions is supported.</span></span>
-   <span data-ttu-id="b2046-125">Anwendungen können Ihre eigenen Konverter registrieren.</span><span class="sxs-lookup"><span data-stu-id="b2046-125">Applications can register their own converters.</span></span>
-   <span data-ttu-id="b2046-126">Einige Konvertierungen können in Hardware mithilfe der GPU ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b2046-126">Some conversions can be performed in hardware using the GPU.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2046-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2046-127">Requirements</span></span>



| <span data-ttu-id="b2046-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2046-128">Requirement</span></span> | <span data-ttu-id="b2046-129">Wert</span><span class="sxs-lookup"><span data-stu-id="b2046-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2046-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b2046-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b2046-131">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="b2046-131">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="b2046-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b2046-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b2046-133">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="b2046-133">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="b2046-134">Header</span><span class="sxs-lookup"><span data-stu-id="b2046-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2046-135"><dt>"Mfreadwrite. h"</dt></span><span class="sxs-lookup"><span data-stu-id="b2046-135"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2046-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2046-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2046-137">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="b2046-137">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b2046-138">Quell Leser</span><span class="sxs-lookup"><span data-stu-id="b2046-138">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="b2046-139">Attribute des Quell Readers</span><span class="sxs-lookup"><span data-stu-id="b2046-139">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




