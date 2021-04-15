---
description: Die folgenden GUIDs definieren Nutz Last Erweiterungen für ASF-Streams (Advanced Systems Format).
ms.assetid: db973b41-1e5c-4bc8-921d-5e9312eb21cb
title: Namen der ASF-Nutz Last Erweiterung (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7dbd27212c8f4812360ba22f89a717659307f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524664"
---
# <a name="asf-payload-extension-guids"></a><span data-ttu-id="ebd2a-103">Namen der ASF-Nutz Last Erweiterung</span><span class="sxs-lookup"><span data-stu-id="ebd2a-103">ASF Payload Extension GUIDs</span></span>

<span data-ttu-id="ebd2a-104">Die folgenden GUIDs definieren Nutz Last Erweiterungen für ASF-Streams (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="ebd2a-104">The following GUIDs define payload extensions for Advanced Systems Format (ASF) streams.</span></span>



| <span data-ttu-id="ebd2a-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="ebd2a-105">Constant</span></span>                                                                                                                                                                                                                                                                                      | <span data-ttu-id="ebd2a-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ebd2a-106">Description</span></span>                                                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASFSampleExtension_SampleDuration"></span><span id="mfasfsampleextension_sampleduration"></span><span id="MFASFSAMPLEEXTENSION_SAMPLEDURATION"></span><dl> <span data-ttu-id="ebd2a-107"><dt>**Mfasf Sample Extension \_ sampleduration**</dt></span><span class="sxs-lookup"><span data-stu-id="ebd2a-107"><dt>**MFASFSampleExtension\_SampleDuration**</dt></span></span> </dl>         | <span data-ttu-id="ebd2a-108">Die Daten zeigen die Dauer (in Millisekunden) des im Buffer-Objekt enthaltenen Beispiels an.</span><span class="sxs-lookup"><span data-stu-id="ebd2a-108">The data indicates the duration, in milliseconds, of the sample contained in the buffer object.</span></span><br/>                                                                       |
| <span id="MFASFSampleExtension_OutputCleanPoint"></span><span id="mfasfsampleextension_outputcleanpoint"></span><span id="MFASFSAMPLEEXTENSION_OUTPUTCLEANPOINT"></span><dl> <span data-ttu-id="ebd2a-109"><dt>**Mfasf Sample Extension \_ outputcleanpoint**</dt></span><span class="sxs-lookup"><span data-stu-id="ebd2a-109"><dt>**MFASFSampleExtension\_OutputCleanPoint**</dt></span></span> </dl> | <span data-ttu-id="ebd2a-110">Die Daten zeigen an, ob das Beispiel ein Keyframe ist.</span><span class="sxs-lookup"><span data-stu-id="ebd2a-110">The data indicates whether the sample is a key frame.</span></span> <span data-ttu-id="ebd2a-111">Der Wert 0 (null) gibt an, dass das Beispiel kein Keyframe ist.</span><span class="sxs-lookup"><span data-stu-id="ebd2a-111">A value of zero indicates that the sample is not a key frame.</span></span> <span data-ttu-id="ebd2a-112">Ein Wert ungleich NULL gibt an, dass es sich um einen Keyframe handelt.</span><span class="sxs-lookup"><span data-stu-id="ebd2a-112">A nonzero value indicates that it is a key frame.</span></span><br/> |
| <span id="MFASFSampleExtension_SMPTE"></span><span id="mfasfsampleextension_smpte"></span><span id="MFASFSAMPLEEXTENSION_SMPTE"></span><dl> <span data-ttu-id="ebd2a-113"><dt>**Mfasssampleextension ( \_ SMPTE)**</dt></span><span class="sxs-lookup"><span data-stu-id="ebd2a-113"><dt>**MFASFSampleExtension\_SMPTE**</dt></span></span> </dl>                                             | <span data-ttu-id="ebd2a-114">Bei den Daten handelt es sich um einen SMPTE-Zeit Code.</span><span class="sxs-lookup"><span data-stu-id="ebd2a-114">The data is a SMPTE time code.</span></span><br/>                                                                                                                                        |
| <span id="MFASFSampleExtension_FileName"></span><span id="mfasfsampleextension_filename"></span><span id="MFASFSAMPLEEXTENSION_FILENAME"></span><dl> <span data-ttu-id="ebd2a-115"><dt>**Mfasf Sample Extension- \_ Dateiname**</dt></span><span class="sxs-lookup"><span data-stu-id="ebd2a-115"><dt>**MFASFSampleExtension\_FileName**</dt></span></span> </dl>                                 | <span data-ttu-id="ebd2a-116">Die Daten in der Beispiel Erweiterung geben den Namen der Datei an, aus der der Inhalt in der Stichprobe entnommen wurde.</span><span class="sxs-lookup"><span data-stu-id="ebd2a-116">The data in the sample extension specifies the name of the file from which the content in the sample was taken.</span></span><br/>                                                       |
| <span id="MFASFSampleExtension_ContentType"></span><span id="mfasfsampleextension_contenttype"></span><span id="MFASFSAMPLEEXTENSION_CONTENTTYPE"></span><dl> <span data-ttu-id="ebd2a-117"><dt>**Mfasf Sample Extension- \_ ContentType**</dt></span><span class="sxs-lookup"><span data-stu-id="ebd2a-117"><dt>**MFASFSampleExtension\_ContentType**</dt></span></span> </dl>                     | <span data-ttu-id="ebd2a-118">Die Daten identifizieren den Inhaltstyp, den das Beispiel enthält.</span><span class="sxs-lookup"><span data-stu-id="ebd2a-118">The data identifies the type of content that the sample contains.</span></span><br/>                                                                                                     |
| <span id="MFASFSampleExtension_PixelAspectRatio"></span><span id="mfasfsampleextension_pixelaspectratio"></span><span id="MFASFSAMPLEEXTENSION_PIXELASPECTRATIO"></span><dl> <span data-ttu-id="ebd2a-119"><dt>**Mfasf Sample Extension \_ pixelaspectratio**</dt></span><span class="sxs-lookup"><span data-stu-id="ebd2a-119"><dt>**MFASFSampleExtension\_PixelAspectRatio**</dt></span></span> </dl> | <span data-ttu-id="ebd2a-120">Die Daten zeigen das Pixel Seitenverhältnis des Inhalts in der Stichprobe an.</span><span class="sxs-lookup"><span data-stu-id="ebd2a-120">The data indicates the pixel aspect ratio of the content in the sample.</span></span><br/>                                                                                               |



## <a name="requirements"></a><span data-ttu-id="ebd2a-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ebd2a-121">Requirements</span></span>



| <span data-ttu-id="ebd2a-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ebd2a-122">Requirement</span></span> | <span data-ttu-id="ebd2a-123">Wert</span><span class="sxs-lookup"><span data-stu-id="ebd2a-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebd2a-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ebd2a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ebd2a-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ebd2a-125">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ebd2a-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ebd2a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ebd2a-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ebd2a-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ebd2a-128">Header</span><span class="sxs-lookup"><span data-stu-id="ebd2a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebd2a-129"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebd2a-129"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebd2a-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ebd2a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebd2a-131">**Imfasf streamconfig:: addpayloadextension**</span><span class="sxs-lookup"><span data-stu-id="ebd2a-131">**IMFASFStreamConfig::AddPayloadExtension**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-addpayloadextension)
</dt> <dt>

[<span data-ttu-id="ebd2a-132">**Imfasf streamconfig:: getpayloadextension**</span><span class="sxs-lookup"><span data-stu-id="ebd2a-132">**IMFASFStreamConfig::GetPayloadExtension**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextension)
</dt> <dt>

[<span data-ttu-id="ebd2a-133">Media Foundation Konstanten</span><span class="sxs-lookup"><span data-stu-id="ebd2a-133">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> </dl>

 

 




