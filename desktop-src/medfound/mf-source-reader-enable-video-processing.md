---
description: Ermöglicht die Videoverarbeitung durch den Quell Reader.
ms.assetid: b1ec1c0e-8042-4486-822f-eb106577c0b1
title: MF_SOURCE_READER_ENABLE_VIDEO_PROCESSING-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bfcbb076d5f42e784277dbd78101b473ec33905
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484806"
---
# <a name="mf_source_reader_enable_video_processing-attribute"></a><span data-ttu-id="995ae-103">MF- \_ Quell \_ Leser Aktivieren von \_ \_ Video \_ Verarbeitungs Attributen</span><span class="sxs-lookup"><span data-stu-id="995ae-103">MF\_SOURCE\_READER\_ENABLE\_VIDEO\_PROCESSING attribute</span></span>

<span data-ttu-id="995ae-104">Ermöglicht die Videoverarbeitung durch den [Quell Reader](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="995ae-104">Enables video processing by the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="995ae-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="995ae-105">Data type</span></span>

<span data-ttu-id="995ae-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="995ae-106">**UINT32**</span></span>



| <span data-ttu-id="995ae-107">Wert</span><span class="sxs-lookup"><span data-stu-id="995ae-107">Value</span></span>                                                                                                                                                                | <span data-ttu-id="995ae-108">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="995ae-108">Meaning</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="Nonzero"></span><span id="nonzero"></span><span id="NONZERO"></span><dl> <span data-ttu-id="995ae-109"><dt>**Ungleich NULL**</dt></span><span class="sxs-lookup"><span data-stu-id="995ae-109"><dt>**Nonzero**</dt></span></span> </dl> | <span data-ttu-id="995ae-110">Aktivieren Sie die Videoverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="995ae-110">Enable video processing.</span></span><br/>            |
| <span id="Zero"></span><span id="zero"></span><span id="ZERO"></span><dl> <span data-ttu-id="995ae-111"><dt>**Zins**</dt></span><span class="sxs-lookup"><span data-stu-id="995ae-111"><dt>**Zero**</dt></span></span> </dl>             | <span data-ttu-id="995ae-112">Deaktivieren Sie die Videoverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="995ae-112">Disable video processing.</span></span> <span data-ttu-id="995ae-113">(Standardwert)</span><span class="sxs-lookup"><span data-stu-id="995ae-113">(Default)</span></span><br/> |



 

## <a name="getset"></a><span data-ttu-id="995ae-114">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="995ae-114">Get/set</span></span>

<span data-ttu-id="995ae-115">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="995ae-115">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="995ae-116">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="995ae-116">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="995ae-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="995ae-117">Remarks</span></span>

<span data-ttu-id="995ae-118">Wenn dieses Attribut **true** (ungleich 0 (null)) ist, kann der Quell Leser die folgende eingeschränkte Videoverarbeitung für nicht komprimierte Video Frames ausführen:</span><span class="sxs-lookup"><span data-stu-id="995ae-118">If this attribute is **TRUE** (nonzero), the source reader can perform the following limited video processing on uncompressed video frames:</span></span>

-   <span data-ttu-id="995ae-119">Konvertierung von YUV in RGB-32.</span><span class="sxs-lookup"><span data-stu-id="995ae-119">Conversion from YUV to RGB-32.</span></span>
-   <span data-ttu-id="995ae-120">Deinterlacing.</span><span class="sxs-lookup"><span data-stu-id="995ae-120">Deinterlacing.</span></span>

<span data-ttu-id="995ae-121">Diese Vorgänge werden in Software ausgeführt und sind nicht für die Wiedergabe optimiert.</span><span class="sxs-lookup"><span data-stu-id="995ae-121">These operations are performed in software, and are not optimized for playback.</span></span> <span data-ttu-id="995ae-122">Diese Funktion ist für Anwendungen vorgesehen, die eine kleine Anzahl von Frames verarbeiten, z. –. um eine Video Miniaturansicht zu erstellen – oder Anwendungen, die Frames nicht in Echtzeit decodieren.</span><span class="sxs-lookup"><span data-stu-id="995ae-122">This feature is intended for applications that process a small number of frames—for example, to create a video thumbnail—or applications that do not decode frames in real time.</span></span> <span data-ttu-id="995ae-123">Der Deinterlacing-Vorgang interpoliert Daten aus einem einzelnen Feld und ist daher verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="995ae-123">The deinterlace operation interpolates data from a single field, so it is lossy.</span></span>

<span data-ttu-id="995ae-124">Vermeiden Sie diese Einstellung, wenn Sie Direct3D verwenden, um die Video Frames anzuzeigen, da die GPU in der Regel bessere Video Verarbeitungsfunktionen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="995ae-124">Avoid this setting if you are using Direct3D to display the video frames, because the GPU generally provides better video processing capabilities.</span></span>

<span data-ttu-id="995ae-125">Wenn dieses Attribut " **true**" ist, müssen die folgenden Attribute " **false**" lauten:</span><span class="sxs-lookup"><span data-stu-id="995ae-125">If this attribute is **TRUE**, the following attributes must be **FALSE**:</span></span>

-   [<span data-ttu-id="995ae-126">MF- \_ Quell \_ Leser \_ D3D \_ Manager</span><span class="sxs-lookup"><span data-stu-id="995ae-126">MF\_SOURCE\_READER\_D3D\_MANAGER</span></span>](mf-source-reader-d3d-manager.md)
-   [<span data-ttu-id="995ae-127">MF- \_ Lese Schreibvorgänge \_ Deaktivieren \_</span><span class="sxs-lookup"><span data-stu-id="995ae-127">MF\_READWRITE\_DISABLE\_CONVERTERS</span></span>](mf-readwrite-disable-converters.md)

## <a name="requirements"></a><span data-ttu-id="995ae-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="995ae-128">Requirements</span></span>



| <span data-ttu-id="995ae-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="995ae-129">Requirement</span></span> | <span data-ttu-id="995ae-130">Wert</span><span class="sxs-lookup"><span data-stu-id="995ae-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="995ae-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="995ae-131">Minimum supported client</span></span><br/> | <span data-ttu-id="995ae-132">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="995ae-132">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="995ae-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="995ae-133">Minimum supported server</span></span><br/> | <span data-ttu-id="995ae-134">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="995ae-134">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="995ae-135">Header</span><span class="sxs-lookup"><span data-stu-id="995ae-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="995ae-136"><dt>"Mfreadwrite. h"</dt></span><span class="sxs-lookup"><span data-stu-id="995ae-136"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="995ae-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="995ae-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="995ae-138">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="995ae-138">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="995ae-139">Quell Leser</span><span class="sxs-lookup"><span data-stu-id="995ae-139">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="995ae-140">Attribute des Quell Readers</span><span class="sxs-lookup"><span data-stu-id="995ae-140">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




