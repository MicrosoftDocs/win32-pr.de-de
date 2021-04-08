---
description: Die folgenden GUIDs definieren Kategorien für Media Foundation Transformationen (MFTs). Diese Kategorien werden verwendet, um MFTs zu registrieren und aufzuzählen.
ms.assetid: eca3ae3b-e40a-407d-986c-d0a85b891f52
title: MFT_CATEGORY (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb7bc74054ad9f201b1f2ca53b526826d34c510d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863964"
---
# <a name="mft_category"></a><span data-ttu-id="aa4c5-104">MFT- \_ Kategorie</span><span class="sxs-lookup"><span data-stu-id="aa4c5-104">MFT\_CATEGORY</span></span>

<span data-ttu-id="aa4c5-105">Die folgenden GUIDs definieren Kategorien für Media Foundation Transformationen (MFTs).</span><span class="sxs-lookup"><span data-stu-id="aa4c5-105">The following GUIDs define categories for Media Foundation transforms (MFTs).</span></span> <span data-ttu-id="aa4c5-106">Diese Kategorien werden verwendet, um MFTs zu registrieren und aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="aa4c5-106">These categories are used to register and enumerate MFTs.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="aa4c5-107">Konstante</span><span class="sxs-lookup"><span data-stu-id="aa4c5-107">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="aa4c5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aa4c5-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_AUDIO_DECODER"></span><span id="mft_category_audio_decoder"></span><dl> <span data-ttu-id="aa4c5-109"><dt><strong>MFT_CATEGORY_AUDIO_DECODER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="aa4c5-109"><dt><strong>MFT_CATEGORY_AUDIO_DECODER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="aa4c5-110">Audiodecoder.</span><span class="sxs-lookup"><span data-stu-id="aa4c5-110">Audio decoders.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_AUDIO_EFFECT"></span><span id="mft_category_audio_effect"></span><dl> <span data-ttu-id="aa4c5-111"><dt><strong>MFT_CATEGORY_AUDIO_EFFECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="aa4c5-111"><dt><strong>MFT_CATEGORY_AUDIO_EFFECT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="aa4c5-112">Audioeffekte.</span><span class="sxs-lookup"><span data-stu-id="aa4c5-112">Audio effects.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_AUDIO_ENCODER"></span><span id="mft_category_audio_encoder"></span><dl> <span data-ttu-id="aa4c5-113"><dt><strong>MFT_CATEGORY_AUDIO_ENCODER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="aa4c5-113"><dt><strong>MFT_CATEGORY_AUDIO_ENCODER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="aa4c5-114">Audioencoder.</span><span class="sxs-lookup"><span data-stu-id="aa4c5-114">Audio encoders.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_DEMULTIPLEXER"></span><span id="mft_category_demultiplexer"></span><dl> <span data-ttu-id="aa4c5-115"><dt><strong>MFT_CATEGORY_DEMULTIPLEXER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="aa4c5-115"><dt><strong>MFT_CATEGORY_DEMULTIPLEXER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="aa4c5-116">Demultiplexer.</span><span class="sxs-lookup"><span data-stu-id="aa4c5-116">Demultiplexers.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_MULTIPLEXER"></span><span id="mft_category_multiplexer"></span><dl> <span data-ttu-id="aa4c5-117"><dt><strong>MFT_CATEGORY_MULTIPLEXER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="aa4c5-117"><dt><strong>MFT_CATEGORY_MULTIPLEXER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="aa4c5-118">Multiplexers (.</span><span class="sxs-lookup"><span data-stu-id="aa4c5-118">Multiplexers.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="aa4c5-119">In Windows Vista unterstützt die Media Foundation Pipeline keine MFTs mit mehr als einer Eingabe.</span><span class="sxs-lookup"><span data-stu-id="aa4c5-119">In Windows Vista, the Media Foundation pipeline does not support MFTs with more than one input.</span></span> <span data-ttu-id="aa4c5-120">MFTs mit mehreren Eingaben werden in Windows 7 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="aa4c5-120">Multiple-input MFTs are supported in Windows 7.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_OTHER"></span><span id="mft_category_other"></span><dl> <span data-ttu-id="aa4c5-121"><dt><strong>MFT_CATEGORY_OTHER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="aa4c5-121"><dt><strong>MFT_CATEGORY_OTHER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="aa4c5-122">Verschiedene MFTs.</span><span class="sxs-lookup"><span data-stu-id="aa4c5-122">Miscellaneous MFTs.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_DECODER"></span><span id="mft_category_video_decoder"></span><dl> <span data-ttu-id="aa4c5-123"><dt><strong>MFT_CATEGORY_VIDEO_DECODER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="aa4c5-123"><dt><strong>MFT_CATEGORY_VIDEO_DECODER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="aa4c5-124">Video-Decoders.</span><span class="sxs-lookup"><span data-stu-id="aa4c5-124">Video decoders.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_EFFECT"></span><span id="mft_category_video_effect"></span><dl> <span data-ttu-id="aa4c5-125"><dt><strong>MFT_CATEGORY_VIDEO_EFFECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="aa4c5-125"><dt><strong>MFT_CATEGORY_VIDEO_EFFECT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="aa4c5-126">Video Effekte.</span><span class="sxs-lookup"><span data-stu-id="aa4c5-126">Video effects.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_RENDERER_EFFECT"></span><span id="mft_category_video_renderer_effect"></span><dl> <span data-ttu-id="aa4c5-127"><dt><strong>MFT_CATEGORY_VIDEO_RENDERER_EFFECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="aa4c5-127"><dt><strong>MFT_CATEGORY_VIDEO_RENDERER_EFFECT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="aa4c5-128">Effekte der Videorenderer.</span><span class="sxs-lookup"><span data-stu-id="aa4c5-128">Video renderer effects.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_ENCODER"></span><span id="mft_category_video_encoder"></span><dl> <span data-ttu-id="aa4c5-129"><dt><strong>MFT_CATEGORY_VIDEO_ENCODER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="aa4c5-129"><dt><strong>MFT_CATEGORY_VIDEO_ENCODER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="aa4c5-130">Video Encoder.</span><span class="sxs-lookup"><span data-stu-id="aa4c5-130">Video encoders.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_PROCESSOR"></span><span id="mft_category_video_processor"></span><dl> <span data-ttu-id="aa4c5-131"><dt><strong>MFT_CATEGORY_VIDEO_PROCESSOR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="aa4c5-131"><dt><strong>MFT_CATEGORY_VIDEO_PROCESSOR</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="aa4c5-132">Eingeführt in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="aa4c5-132">Introduced in Windows 7.</span></span>
</blockquote>
<br/> <span data-ttu-id="aa4c5-133">Video Prozessoren.</span><span class="sxs-lookup"><span data-stu-id="aa4c5-133">Video processors.</span></span> <br/> <span data-ttu-id="aa4c5-134">Diese Kategorie ist auf MFTs beschränkt, die Formatkonvertierungen für unkomprimierte Videos ausführen, einschließlich Farb Raum Konvertierungen.</span><span class="sxs-lookup"><span data-stu-id="aa4c5-134">This category is limited to MFTs that perform format conversions on uncompressed video, including color-space conversions.</span></span> <span data-ttu-id="aa4c5-135">Verwenden Sie für Video Effekte, die die Darstellung des Bilds ändern (z. b. einen Weichzeichnereffekt oder eine Farb-zu-Graustufen Transformation) die <strong>MFT_CATEGORY_VIDEO_EFFECT</strong> Kategorie.</span><span class="sxs-lookup"><span data-stu-id="aa4c5-135">For video effects that modify the appearance of the image (such as a blur effect or a color-to-grayscale transform), use the <strong>MFT_CATEGORY_VIDEO_EFFECT</strong> category.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="aa4c5-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa4c5-136">Requirements</span></span>



| <span data-ttu-id="aa4c5-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa4c5-137">Requirement</span></span> | <span data-ttu-id="aa4c5-138">Wert</span><span class="sxs-lookup"><span data-stu-id="aa4c5-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aa4c5-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aa4c5-139">Minimum supported client</span></span><br/> | <span data-ttu-id="aa4c5-140">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa4c5-140">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="aa4c5-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aa4c5-141">Minimum supported server</span></span><br/> | <span data-ttu-id="aa4c5-142">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa4c5-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="aa4c5-143">Header</span><span class="sxs-lookup"><span data-stu-id="aa4c5-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa4c5-144"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa4c5-144"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa4c5-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa4c5-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa4c5-146">Media Foundation Konstanten</span><span class="sxs-lookup"><span data-stu-id="aa4c5-146">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> <dt>

[<span data-ttu-id="aa4c5-147">Media Foundation Transformationen</span><span class="sxs-lookup"><span data-stu-id="aa4c5-147">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="aa4c5-148">**MF-Wert**</span><span class="sxs-lookup"><span data-stu-id="aa4c5-148">**MFTEnum**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mftenum)
</dt> <dt>

[<span data-ttu-id="aa4c5-149">**MF-Datei**</span><span class="sxs-lookup"><span data-stu-id="aa4c5-149">**MFTEnumEx**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
</dt> <dt>

[<span data-ttu-id="aa4c5-150">**MF-tregiester**</span><span class="sxs-lookup"><span data-stu-id="aa4c5-150">**MFTRegister**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mftregister)
</dt> </dl>

 

 




