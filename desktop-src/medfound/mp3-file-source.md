---
description: Die MP3-Datei Quelle analysiert MP3-Dateien.
ms.assetid: 37362642-1b8a-4fb3-950d-ed1afe3696e5
title: MP3-Datei Quelle
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2241e3b99d5a1918be8ff0182a9eca8939c12ce2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130497"
---
# <a name="mp3-file-source"></a><span data-ttu-id="b086c-103">MP3-Datei Quelle</span><span class="sxs-lookup"><span data-stu-id="b086c-103">MP3 File Source</span></span>

<span data-ttu-id="b086c-104">Die MP3-Datei Quelle analysiert MP3-Dateien.</span><span class="sxs-lookup"><span data-stu-id="b086c-104">The MP3 file source parses MP3 files.</span></span>

<span data-ttu-id="b086c-105">Die MP3-Datei Quelle gibt Puffer aus, die MPEG-1-Audioframes enthalten.</span><span class="sxs-lookup"><span data-stu-id="b086c-105">The MP3 file source outputs buffers that contain MPEG-1 audio frames.</span></span> <span data-ttu-id="b086c-106">Die Audiocodierung wird nicht decodiert.</span><span class="sxs-lookup"><span data-stu-id="b086c-106">It does not decode the audio.</span></span>

## <a name="file-extensions-and-mime-types"></a><span data-ttu-id="b086c-107">Dateierweiterungen und MIME-Typen</span><span class="sxs-lookup"><span data-stu-id="b086c-107">File Extensions and MIME Types</span></span>

<span data-ttu-id="b086c-108">Die MP3-Datei Quelle ist die Standard Medienquelle für die folgende Dateinamenerweiterung:</span><span class="sxs-lookup"><span data-stu-id="b086c-108">The MP3 file source is the default media source for the following file name extension:</span></span>

-   <span data-ttu-id="b086c-109">.mp3</span><span class="sxs-lookup"><span data-stu-id="b086c-109">.mp3</span></span>

<span data-ttu-id="b086c-110">Es ist auch die Standard Medienquelle für die folgenden MIME-Typen.</span><span class="sxs-lookup"><span data-stu-id="b086c-110">It is also the default media source for the following MIME types.</span></span>

-   <span data-ttu-id="b086c-111">Audiodatei/MPEG</span><span class="sxs-lookup"><span data-stu-id="b086c-111">audio/mpeg</span></span>
-   <span data-ttu-id="b086c-112">Audiodatei/x-MP3</span><span class="sxs-lookup"><span data-stu-id="b086c-112">audio/x-mp3</span></span>
-   <span data-ttu-id="b086c-113">Audiodatei/x-MPEG</span><span class="sxs-lookup"><span data-stu-id="b086c-113">audio/x-mpeg</span></span>

## <a name="media-types"></a><span data-ttu-id="b086c-114">Medientypen</span><span class="sxs-lookup"><span data-stu-id="b086c-114">Media Types</span></span>

<span data-ttu-id="b086c-115">Der von der MP3-Datei Quelle angebotene Medientyp enthält die folgenden Attribute.</span><span class="sxs-lookup"><span data-stu-id="b086c-115">The media type offered by the MP3 file source contains the following attributes.</span></span>



| <span data-ttu-id="b086c-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="b086c-116">Attribute</span></span>                                                                                    | <span data-ttu-id="b086c-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b086c-117">Description</span></span>                                                                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b086c-118">**Haupt-Typ des MF- \_ MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b086c-118">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="b086c-119">Gleich **mfmediatype \_ -Audiodatei**.</span><span class="sxs-lookup"><span data-stu-id="b086c-119">Equal to **MFMediaType\_Audio**.</span></span>                                                                                                                   |
| [<span data-ttu-id="b086c-120">**MF- \_ MT- \_ Untertyp**</span><span class="sxs-lookup"><span data-stu-id="b086c-120">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="b086c-121">Entspricht **mfaudioformat \_ MP3** oder **mfaudioformat \_ MPEG**.</span><span class="sxs-lookup"><span data-stu-id="b086c-121">Equal to **MFAudioFormat\_MP3** or **MFAudioFormat\_MPEG**.</span></span>                                                                                        |
| [<span data-ttu-id="b086c-122">**MF \_ \_ -MT-audiodurchschn. \_ \_ Byte \_ pro \_ Sekunde**</span><span class="sxs-lookup"><span data-stu-id="b086c-122">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="b086c-123">Die durchschnittliche Anzahl von Bytes pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="b086c-123">Average number of bytes per second.</span></span>                                                                                                                |
| [<span data-ttu-id="b086c-124">**MF \_ \_ -MT- \_ Audioblock \_ Ausrichtung**</span><span class="sxs-lookup"><span data-stu-id="b086c-124">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="b086c-125">Gleich 1.</span><span class="sxs-lookup"><span data-stu-id="b086c-125">Equal to 1.</span></span>                                                                                                                                        |
| [<span data-ttu-id="b086c-126">**MF \_ \_ -MT- \_ audionum- \_ Kanäle**</span><span class="sxs-lookup"><span data-stu-id="b086c-126">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="b086c-127">Anzahl der Audiokanäle.</span><span class="sxs-lookup"><span data-stu-id="b086c-127">Number of audio channels.</span></span>                                                                                                                          |
| [<span data-ttu-id="b086c-128">**MF \_ \_ -MT- \_ Audiobeispiele \_ pro \_ Sekunde**</span><span class="sxs-lookup"><span data-stu-id="b086c-128">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="b086c-129">Anzahl von Audiobeispielen pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="b086c-129">Number of audio samples per second.</span></span>                                                                                                                |
| [<span data-ttu-id="b086c-130">**\_ \_ Benutzer \_ Daten für MF-MT**</span><span class="sxs-lookup"><span data-stu-id="b086c-130">**MF\_MT\_USER\_DATA**</span></span>](mf-mt-user-data-attribute.md)                                      | <span data-ttu-id="b086c-131">Enthält den Teil einer [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) -Struktur, der nach dem **wfx** -Member der-Struktur angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b086c-131">Contains the portion of a [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) structure that appears after the **wfx** member of the structure.</span></span> |



 

## <a name="interfaces"></a><span data-ttu-id="b086c-132">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="b086c-132">Interfaces</span></span>

<span data-ttu-id="b086c-133">Die MP3-Datei Quelle macht die folgenden Schnittstellen über [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))verfügbar:</span><span class="sxs-lookup"><span data-stu-id="b086c-133">The MP3 file source exposes the following interfaces through [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):</span></span>

-   [<span data-ttu-id="b086c-134">**IMF-Dienst**</span><span class="sxs-lookup"><span data-stu-id="b086c-134">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="b086c-135">**IMF Media Event Generator**</span><span class="sxs-lookup"><span data-stu-id="b086c-135">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [<span data-ttu-id="b086c-136">**Imfmediasource**</span><span class="sxs-lookup"><span data-stu-id="b086c-136">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)

<span data-ttu-id="b086c-137">Außerdem werden die folgenden Schnittstellen über [**IMF-Service**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)verfügbar gemacht:</span><span class="sxs-lookup"><span data-stu-id="b086c-137">In addition, it exposes the following interfaces through [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b086c-138">Dienst-GUID</span><span class="sxs-lookup"><span data-stu-id="b086c-138">Service GUID</span></span></th>
<th><span data-ttu-id="b086c-139">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b086c-139">Interface</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b086c-140"><strong>MF_METADATA_PROVIDER_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="b086c-140"><strong>MF_METADATA_PROVIDER_SERVICE</strong></span></span></td>
<td><span data-ttu-id="b086c-141"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider"><strong>IMFMetadataProvider</strong></a></span><span class="sxs-lookup"><span data-stu-id="b086c-141"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider"><strong>IMFMetadataProvider</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b086c-142"><strong>MF_PROPERTY_HANDLER_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="b086c-142"><strong>MF_PROPERTY_HANDLER_SERVICE</strong></span></span></td>
<td><span data-ttu-id="b086c-143"><a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a>
</span><span class="sxs-lookup"><span data-stu-id="b086c-143"><a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a>
</span></span><blockquote>
[!Note]<br />
<span data-ttu-id="b086c-144">Siehe <a href="shell-metadata-providers.md">shellmetadatenanbieter</a>.</span><span class="sxs-lookup"><span data-stu-id="b086c-144">See <a href="shell-metadata-providers.md">Shell Metadata Providers</a>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b086c-145"><strong>MF_RATE_CONTROL_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="b086c-145"><strong>MF_RATE_CONTROL_SERVICE</strong></span></span></td>
<td><span data-ttu-id="b086c-146"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol"><strong>Imfratecontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="b086c-146"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol"><strong>IMFRateControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b086c-147"><strong>MF_RATE_CONTROL_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="b086c-147"><strong>MF_RATE_CONTROL_SERVICE</strong></span></span></td>
<td><span data-ttu-id="b086c-148"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratesupport"><strong>Imfratesupport</strong></a></span><span class="sxs-lookup"><span data-stu-id="b086c-148"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratesupport"><strong>IMFRateSupport</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="b086c-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b086c-149">Requirements</span></span>



| <span data-ttu-id="b086c-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b086c-150">Requirement</span></span> | <span data-ttu-id="b086c-151">Wert</span><span class="sxs-lookup"><span data-stu-id="b086c-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b086c-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b086c-152">Minimum supported client</span></span><br/> | <span data-ttu-id="b086c-153">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b086c-153">Windows 7 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b086c-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b086c-154">Minimum supported server</span></span><br/> | <span data-ttu-id="b086c-155">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b086c-155">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b086c-156">DLL</span><span class="sxs-lookup"><span data-stu-id="b086c-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b086c-157"><dt>Mf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b086c-157"><dt>Mf.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b086c-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b086c-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b086c-159">Medienquellen und senken</span><span class="sxs-lookup"><span data-stu-id="b086c-159">Media Sources and Sinks</span></span>](media-sources-and-sinks.md)
</dt> <dt>

[<span data-ttu-id="b086c-160">Medienquellen</span><span class="sxs-lookup"><span data-stu-id="b086c-160">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="b086c-161">Quellresolver</span><span class="sxs-lookup"><span data-stu-id="b086c-161">Source Resolver</span></span>](source-resolver.md)
</dt> <dt>

[<span data-ttu-id="b086c-162">Unterstützte Medienformate in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b086c-162">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 
