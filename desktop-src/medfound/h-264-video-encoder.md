---
description: 'Der Video Encoder Microsoft Media Foundation H. 264 ist eine Media Foundation Transformation, die die folgenden H. 264-Profile unterstützt:'
ms.assetid: 4d4c768f-b76a-40ca-8736-2f592a4f4cc4
title: H. 264-Video Encoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5631239e9db0ddf078848bc3c4a04282e7e79990
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348478"
---
# <a name="h264-video-encoder"></a><span data-ttu-id="1f2e8-103">H. 264-Video Encoder</span><span class="sxs-lookup"><span data-stu-id="1f2e8-103">H.264 Video Encoder</span></span>

<span data-ttu-id="1f2e8-104">Der Video Encoder Microsoft Media Foundation H. 264 ist eine [Media Foundation Transformation](media-foundation-transforms.md) , die die folgenden H. 264-Profile unterstützt:</span><span class="sxs-lookup"><span data-stu-id="1f2e8-104">The Microsoft Media Foundation H.264 video encoder is a [Media Foundation transform](media-foundation-transforms.md) that supports the following H.264 profiles:</span></span>

-   <span data-ttu-id="1f2e8-105">Basis Linien Profil</span><span class="sxs-lookup"><span data-stu-id="1f2e8-105">Baseline Profile</span></span>
-   <span data-ttu-id="1f2e8-106">Profil: Main</span><span class="sxs-lookup"><span data-stu-id="1f2e8-106">Main Profile</span></span>
-   <span data-ttu-id="1f2e8-107">Hohes Profil (erfordert Windows 8)</span><span class="sxs-lookup"><span data-stu-id="1f2e8-107">High profile (requires Windows 8)</span></span>

<span data-ttu-id="1f2e8-108">Der H. 264-Video Encoder macht die folgenden Schnittstellen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="1f2e8-108">The H.264 video encoder exposes the following interfaces:</span></span>

-   [<span data-ttu-id="1f2e8-109">**Icodecapi**</span><span class="sxs-lookup"><span data-stu-id="1f2e8-109">**ICodecAPI**</span></span>](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [<span data-ttu-id="1f2e8-110">**IMF-Transformation**</span><span class="sxs-lookup"><span data-stu-id="1f2e8-110">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a><span data-ttu-id="1f2e8-111">Eingabetypen</span><span class="sxs-lookup"><span data-stu-id="1f2e8-111">Input Types</span></span>

<span data-ttu-id="1f2e8-112">Der Eingabe Medientyp muss einen der folgenden Untertypen aufweisen:</span><span class="sxs-lookup"><span data-stu-id="1f2e8-112">The input media type must have one of the following subtypes:</span></span>

-   <span data-ttu-id="1f2e8-113">**MFVideoFormat_I420**</span><span class="sxs-lookup"><span data-stu-id="1f2e8-113">**MFVideoFormat_I420**</span></span>
-   <span data-ttu-id="1f2e8-114">**MFVideoFormat_IYUV**</span><span class="sxs-lookup"><span data-stu-id="1f2e8-114">**MFVideoFormat_IYUV**</span></span>
-   <span data-ttu-id="1f2e8-115">**MFVideoFormat_NV12**</span><span class="sxs-lookup"><span data-stu-id="1f2e8-115">**MFVideoFormat_NV12**</span></span>
-   <span data-ttu-id="1f2e8-116">**MFVideoFormat_YUY2**</span><span class="sxs-lookup"><span data-stu-id="1f2e8-116">**MFVideoFormat_YUY2**</span></span>
-   <span data-ttu-id="1f2e8-117">**MFVideoFormat_YV12**</span><span class="sxs-lookup"><span data-stu-id="1f2e8-117">**MFVideoFormat_YV12**</span></span>

<span data-ttu-id="1f2e8-118">Weitere Informationen zu diesen Untertypen finden Sie unter [Video Untertyp-GUIDs](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="1f2e8-118">For more information about these subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

<span data-ttu-id="1f2e8-119">Der Ausgabetyp muss vor dem Eingabetyp festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-119">The output type must be set before the input type.</span></span> <span data-ttu-id="1f2e8-120">Bis der Ausgabetyp festgelegt ist, gibt die [**IMF Transform:: setinputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) -Methode des Encoders **MF_E_TRANSFORM_TYPE_NOT_SET** zurück.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-120">Until the output type is set, the encoder's [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) method returns **MF_E_TRANSFORM_TYPE_NOT_SET**.</span></span>

## <a name="output-types"></a><span data-ttu-id="1f2e8-121">Ausgabetypen</span><span class="sxs-lookup"><span data-stu-id="1f2e8-121">Output Types</span></span>

<span data-ttu-id="1f2e8-122">Der Encoder unterstützt einen einzelnen Ausgabe Untertyp:</span><span class="sxs-lookup"><span data-stu-id="1f2e8-122">The encoder supports a single output subtype:</span></span>

-   <span data-ttu-id="1f2e8-123">**MFVideoFormat_H264**</span><span class="sxs-lookup"><span data-stu-id="1f2e8-123">**MFVideoFormat_H264**</span></span>

<span data-ttu-id="1f2e8-124">Legen Sie die folgenden Attribute für den Ausgabe Medientyp fest.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-124">Set the following attributes on the output media type.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1f2e8-125">Attribut</span><span class="sxs-lookup"><span data-stu-id="1f2e8-125">Attribute</span></span></th>
<th><span data-ttu-id="1f2e8-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1f2e8-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1f2e8-127"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f2e8-127"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="1f2e8-128">Der Haupttyp.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-128">Major type.</span></span> <span data-ttu-id="1f2e8-129">Muss <strong>MFMediaType_Video</strong>werden.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-129">Must be <strong>MFMediaType_Video</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f2e8-130"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f2e8-130"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="1f2e8-131">Video Untertyp.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-131">Video subtype.</span></span> <span data-ttu-id="1f2e8-132">Muss <strong>MFVideoFormat_H264</strong>werden.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-132">Must be <strong>MFVideoFormat_H264</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f2e8-133"><a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f2e8-133"><a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a></span></span></td>
<td><span data-ttu-id="1f2e8-134">Die durchschnittliche codierte Bitrate in Bits pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-134">Average encoded bit rate, in bits per second.</span></span> <span data-ttu-id="1f2e8-135">Muss größer sein als Null.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-135">Must be greater than zero.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f2e8-136"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f2e8-136"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span></span></td>
<td><span data-ttu-id="1f2e8-137">Die Framerate.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-137">Frame rate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f2e8-138"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f2e8-138"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span></span></td>
<td><span data-ttu-id="1f2e8-139">Frame Größe.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-139">Frame size.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f2e8-140"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f2e8-140"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span></span></td>
<td><span data-ttu-id="1f2e8-141">Interlace-Modus.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-141">Interlace mode.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f2e8-142"><a href="mf-mt-mpeg2-profile-attribute.md"><strong>MF_MT_MPEG2_PROFILE</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f2e8-142"><a href="mf-mt-mpeg2-profile-attribute.md"><strong>MF_MT_MPEG2_PROFILE</strong></a></span></span></td>
<td><span data-ttu-id="1f2e8-143">H. 264-Codierungs Profil.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-143">H.264 encoding profile.</span></span><br/> <span data-ttu-id="1f2e8-144">Die unterstützten Werte sind:</span><span class="sxs-lookup"><span data-stu-id="1f2e8-144">The supported values are:</span></span><br/>
<ul>
<li><span data-ttu-id="1f2e8-145"><strong>eAVEncH264VProfile_Base</strong> (Standard)</span><span class="sxs-lookup"><span data-stu-id="1f2e8-145"><strong>eAVEncH264VProfile_Base</strong> (default)</span></span></li>
<li><span data-ttu-id="1f2e8-146"><strong>eAVEncH264VProfile_Main</strong></span><span class="sxs-lookup"><span data-stu-id="1f2e8-146"><strong>eAVEncH264VProfile_Main</strong></span></span></li>
<li><span data-ttu-id="1f2e8-147"><strong>eAVEncH264VProfile_High</strong> (erfordert Windows 8)</span><span class="sxs-lookup"><span data-stu-id="1f2e8-147"><strong>eAVEncH264VProfile_High</strong> (requires Windows 8)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f2e8-148"><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f2e8-148"><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></span></span></td>
<td><span data-ttu-id="1f2e8-149">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-149">Optional.</span></span> <span data-ttu-id="1f2e8-150">Gibt die H. 264-Codierungs Ebene an.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-150">Specifies the H.264 encoding level.</span></span><br/> <span data-ttu-id="1f2e8-151">Der Standardwert ist – 1 und gibt an, dass der Encoder die Codierungs Ebene auswählt.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-151">The default value is –1, indicating that the encoder will select the encoding level.</span></span><br/> <span data-ttu-id="1f2e8-152">Es wird empfohlen, die Ebene nicht im Medientyp festzulegen, und der Encoder kann die Ebene auswählen.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-152">It is recommended not to set the level in the media type, and allow the encoder to select the level.</span></span> <span data-ttu-id="1f2e8-153">Der Encoder kann die richtige Ebene für einen bestimmten Videostream ableiten, wobei die Format Einschränkungen und die Merkmale des Videos berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-153">The encoder can derive the proper level for a given video stream, taking into account the format constraints and the characteristics of the video.</span></span> <span data-ttu-id="1f2e8-154">Weitere Informationen zu den Einschränkungen für Profile und Ebenen finden Sie in Anhang A von ITU-T H. 264.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-154">For more information about profile and level constraints, refer to Annex A of ITU-T H.264.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f2e8-155"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f2e8-155"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span></span></td>
<td><span data-ttu-id="1f2e8-156">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-156">Optional.</span></span> <span data-ttu-id="1f2e8-157">Gibt das Pixel Seitenverhältnis an.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-157">Specifies the pixel aspect ratio.</span></span> <span data-ttu-id="1f2e8-158">Der Standardwert ist 1:1.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-158">The default value is 1:1.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1f2e8-159">Nachdem der Ausgabetyp festgelegt wurde, aktualisiert der Video Encoder den Typ durch Hinzufügen des [**MF_MT_MPEG_SEQUENCE_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) Attributs.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-159">After the output type is set, the video encoder updates the type by adding the [**MF_MT_MPEG_SEQUENCE_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) attribute.</span></span> <span data-ttu-id="1f2e8-160">Dieses Attribut enthält den Sequence-Header.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-160">This attribute contains the sequence header.</span></span>

## <a name="codec-properties"></a><span data-ttu-id="1f2e8-161">Codec-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1f2e8-161">Codec Properties</span></span>

<span data-ttu-id="1f2e8-162">Der H. 264-Encoder implementiert die [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Schnittstelle zum Festlegen von Codierungs Parametern.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-162">The H.264 encoder implements the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface for setting encoding parameters.</span></span> <span data-ttu-id="1f2e8-163">Die folgenden Eigenschaften werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="1f2e8-163">It supports the following properties.</span></span>

<span data-ttu-id="1f2e8-164">Die Codec-Anforderungen für die HCK Encoder-Zertifizierung finden Sie weiter unten im Abschnitt **Certified Hardware Encoder** .</span><span class="sxs-lookup"><span data-stu-id="1f2e8-164">For the codec requirements for HCK encoder certification, see the **Certified Hardware Encoder** section below.</span></span>

<span data-ttu-id="1f2e8-165">Die folgenden Eigenschaften werden in Windows 7 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-165">The following properties are supported in Windows 7.</span></span>



| <span data-ttu-id="1f2e8-166">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1f2e8-166">Property</span></span>                                                                              | <span data-ttu-id="1f2e8-167">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1f2e8-167">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1f2e8-168">**CODECAPI_AVEncCommonRateControlMode**</span><span class="sxs-lookup"><span data-stu-id="1f2e8-168">**CODECAPI_AVEncCommonRateControlMode**</span></span>](../directshow/avenccommonratecontrolmode-property.md) | <span data-ttu-id="1f2e8-169">Legt den Raten Steuerungs Modus fest.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-169">Sets the rate control mode.</span></span> <span data-ttu-id="1f2e8-170">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-170">See Remarks.</span></span> <span data-ttu-id="1f2e8-171">Der Standardmodus ist die eingeschränkte variablenbitrate (VBR).</span><span class="sxs-lookup"><span data-stu-id="1f2e8-171">The default mode is unconstrained variable bit rate (VBR).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="1f2e8-172">**CODECAPI_AVEncCommonQuality**</span><span class="sxs-lookup"><span data-stu-id="1f2e8-172">**CODECAPI_AVEncCommonQuality**</span></span>](../directshow/avenccommonquality-property.md)                 | <span data-ttu-id="1f2e8-173">Legt die Qualitätsstufe fest.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-173">Sets the quality level.</span></span> <span data-ttu-id="1f2e8-174">Diese Eigenschaft wird angewendet, wenn der Raten Steuerungs Modus Qualitäts basierte VBR (**eAVEncCommonRateControlMode_Quality**) ist.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-174">This property applies when the rate control mode is quality-based VBR (**eAVEncCommonRateControlMode_Quality**).</span></span> <span data-ttu-id="1f2e8-175">Der gültige Bereich ist 1 – 100.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-175">The valid range is 1–100.</span></span> <span data-ttu-id="1f2e8-176">Der Standardwert ist 70.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-176">The default value is 70.</span></span> <br/> <span data-ttu-id="1f2e8-177">Um diesen Parameter festzulegen, legen Sie die-Eigenschaft vor dem Aufrufen von [**imftransform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)fest.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-177">To set this parameter, set the property before calling [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span> <br/> <span data-ttu-id="1f2e8-178">Wenn Sie diesen Parameter in Windows 7 festlegen möchten, legen Sie die-Eigenschaft vor dem Aufrufen von [**imftransform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)fest.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-178">To set this parameter in Windows 7, set the property before calling [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span> <span data-ttu-id="1f2e8-179">Der Encoder ignoriert Änderungen, nachdem der Ausgabetyp festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-179">The encoder ignores changes after the output type is set.</span></span> <br/> <span data-ttu-id="1f2e8-180">In Windows 8 kann diese Eigenschaft während der Codierung jederzeit festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-180">In Windows 8, this property can be set at any time during encoding.</span></span> <span data-ttu-id="1f2e8-181">Änderungen werden ab dem nächsten Eingabe Rahmen angewendet.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-181">Changes are applied starting at the next input frame.</span></span> <br/> <span data-ttu-id="1f2e8-182">Intern konvertiert der Encoder diese Eigenschaft in einen [avencvideoencodeqp](codecapi-avencvideoencodeqp.md) -Wert.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-182">Internally, the encoder converts this property to an [AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md) value.</span></span> <br/> |



 

<span data-ttu-id="1f2e8-183">Die folgenden Eigenschaften erfordern Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-183">The following properties require Windows 8.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1f2e8-184">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1f2e8-184">Property</span></span></th>
<th><span data-ttu-id="1f2e8-185">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1f2e8-185">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1f2e8-186"><a href="codecapi-avencadaptivemode.md">CODECAPI_AVEncAdaptiveMode</a></span><span class="sxs-lookup"><span data-stu-id="1f2e8-186"><a href="codecapi-avencadaptivemode.md">CODECAPI_AVEncAdaptiveMode</a></span></span></td>
<td><span data-ttu-id="1f2e8-187">Legt den adaptiven Codierungs Modus fest.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-187">Sets the adaptive encoding mode.</span></span> <span data-ttu-id="1f2e8-188">Der H. 264-Encoder unterstützt die folgenden Modi in Windows 8:</span><span class="sxs-lookup"><span data-stu-id="1f2e8-188">The H.264 encoder supports the following modes in Windows 8:</span></span>
<ul>
<li><span data-ttu-id="1f2e8-189"><strong>eAVEncAdaptiveMode_None</strong>.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-189"><strong>eAVEncAdaptiveMode_None</strong>.</span></span> <span data-ttu-id="1f2e8-190">Keine adaptive Codierung.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-190">No adaptive encoding.</span></span> <span data-ttu-id="1f2e8-191">(Standardeinstellung)</span><span class="sxs-lookup"><span data-stu-id="1f2e8-191">(Default.)</span></span></li>
<li><span data-ttu-id="1f2e8-192"><strong>eAVEncAdaptiveMode_FrameRate</strong>.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-192"><strong>eAVEncAdaptiveMode_FrameRate</strong>.</span></span> <span data-ttu-id="1f2e8-193">Ändern Sie die Framerate adaptiv.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-193">Adaptively change the frame rate.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f2e8-194"><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></span><span class="sxs-lookup"><span data-stu-id="1f2e8-194"><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></span></span></td>
<td><span data-ttu-id="1f2e8-195">Legt die Puffergröße in Bytes für die Konstante Bitrate (CBR)-Codierung fest.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-195">Sets the buffer size, in bytes, for constant bit rate (CBR) encoding.</span></span><br/> <span data-ttu-id="1f2e8-196">Der gültige Bereich ist [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="1f2e8-196">The valid range is [1 ... 2³²–1].</span></span> <br/> <span data-ttu-id="1f2e8-197">Erfordert Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-197">Requires Windows 8.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f2e8-198"><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></span><span class="sxs-lookup"><span data-stu-id="1f2e8-198"><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></span></span></td>
<td><span data-ttu-id="1f2e8-199">Gibt bei eingeschränkter VBR-Codierung die Rate an, mit der der &quot; Leaky-Bucket &quot; in Bits pro Sekunde entladen wird.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-199">For constrained VBR encoding, specifies the rate at which the &quot;leaky bucket&quot; is drained, in bits per second.</span></span> <span data-ttu-id="1f2e8-200">Diese Eigenschaft wird angewendet, wenn der Raten Steuerungs Modus <strong>eAVEncCommonRateControlMode_PeakConstrainedVBR</strong>ist.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-200">This property applies when the rate control mode is <strong>eAVEncCommonRateControlMode_PeakConstrainedVBR</strong>.</span></span> <br/> <span data-ttu-id="1f2e8-201">Der gültige Bereich ist [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="1f2e8-201">The valid range is [1 ... 2³²–1].</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f2e8-202"><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></span><span class="sxs-lookup"><span data-stu-id="1f2e8-202"><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></span></span></td>
<td><span data-ttu-id="1f2e8-203">Legt die durchschnittliche Bitrate für den codierten Bitstream in Bits pro Sekunde fest.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-203">Sets the average bit rate for the encoded bit stream, in bits per second.</span></span> <span data-ttu-id="1f2e8-204">Diese Eigenschaft wird ignoriert, wenn der Raten Steuerungs Modus <strong>eAVEncCommonRateControlMode_Quality</strong>ist.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-204">This property is ignored if the rate control mode is <strong>eAVEncCommonRateControlMode_Quality</strong>.</span></span> <br/> <span data-ttu-id="1f2e8-205">Der gültige Bereich ist [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="1f2e8-205">The valid range is [1 ... 2³²–1].</span></span> <br/> <span data-ttu-id="1f2e8-206">In CBR und uneingeschränkten VBR-Modi bestimmt die durchschnittliche Bitrate die endgültige Größe der Datei.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-206">In CBR and unconstrained VBR modes, the average bit rate determines the final size of the file.</span></span> <span data-ttu-id="1f2e8-207">Im CBR-Modus ist die durchschnittliche Bitrate auch die Rate, mit der komprimierte Bits aus dem &quot; Leaky-Bucket entladen werden. &quot; (Weitere Informationen finden Sie unter das unkomprimierte <a href="the-leaky-bucket-buffer-model.md">Bucket-Puffer Modell</a>.)</span><span class="sxs-lookup"><span data-stu-id="1f2e8-207">In CBR mode, the average bit rate is also the rate at which compressed bits are drained from the &quot;leaky bucket.&quot; (For more information, see <a href="the-leaky-bucket-buffer-model.md">The Leaky Bucket Buffer Model</a>.)</span></span> <br/> <span data-ttu-id="1f2e8-208">In Windows 7 wird die durchschnittliche Bitrate durch das <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> -Attribut für den Medientyp angegeben.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-208">In Windows 7, the average bit rate is specified by the <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> attribute on the media type.</span></span> <br/> <span data-ttu-id="1f2e8-209">In Windows 8 können Sie die durchschnittliche Bitrate entweder mithilfe des <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> -Attributs oder der <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a> -Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-209">In Windows 8, you can set the average bit rate using either the <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> attribute or the <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a> property.</span></span> <span data-ttu-id="1f2e8-210">Wenn beide festgelegt sind, CODECAPI_AVEncCommonMeanBitRate überschreibt.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-210">If both are set, CODECAPI_AVEncCommonMeanBitRate overrides.</span></span> <span data-ttu-id="1f2e8-211">In Windows 8 können Sie die durchschnittliche Bitrate während der Codierung festlegen.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-211">In Windows 8, you can set the average bit rate during encoding.</span></span> <span data-ttu-id="1f2e8-212">Wenn sich die Bitrate ändert, verwendet der Encoder Adaptive Codierung.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-212">If the bit rate changes, the encoder uses adaptive encoding.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f2e8-213"><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></span><span class="sxs-lookup"><span data-stu-id="1f2e8-213"><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></span></span></td>
<td><span data-ttu-id="1f2e8-214">Legt den Kompromiss der Qualität/Geschwindigkeit fest.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-214">Sets the quality/speed tradeoff.</span></span> <span data-ttu-id="1f2e8-215">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="1f2e8-215">Valid range:</span></span>
<ul>
<li><span data-ttu-id="1f2e8-216">0 – 33: geringe Komplexität</span><span class="sxs-lookup"><span data-stu-id="1f2e8-216">0–33: Low complexity</span></span></li>
<li><span data-ttu-id="1f2e8-217">34 – 66: mittlere Komplexität (Standard)</span><span class="sxs-lookup"><span data-stu-id="1f2e8-217">34–66: Medium complexity (default)</span></span></li>
<li><span data-ttu-id="1f2e8-218">67 – 100: hohe Komplexität</span><span class="sxs-lookup"><span data-stu-id="1f2e8-218">67–100: High complexity</span></span></li>
</ul>
<br/> <span data-ttu-id="1f2e8-219">Dieser Wert wirkt sich darauf aus, wie der Encoder verschiedene Codierungs Vorgänge ausführt, z. b. Motion Compensation.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-219">This value affects how the encoder performs various encoding operations, such as motion compensation.</span></span> <span data-ttu-id="1f2e8-220">Bei höheren Komplexitätsstufen führt der Encoder langsamer aus, erzeugt aber eine bessere Qualität mit derselben Bitrate.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-220">At higher complexity levels, the encoder runs more slowly but produces better quality at the same bit rate.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f2e8-221"><a href="codecapi-avench264cabacenable.md">CODECAPI_AVEncH264CABACEnable</a></span><span class="sxs-lookup"><span data-stu-id="1f2e8-221"><a href="codecapi-avench264cabacenable.md">CODECAPI_AVEncH264CABACEnable</a></span></span></td>
<td><span data-ttu-id="1f2e8-222">Aktiviert oder deaktiviert CABAC (Kontext Adaptive binäre binäre Codierung) für die H. 264-Entropie Codierung.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-222">Enables or disables CABAC (context-adaptive binary arithmetic coding) for H.264 entropy coding.</span></span> <span data-ttu-id="1f2e8-223">Der Standardwert ist <strong>VARIANT_FALSE</strong>.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-223">The default value is <strong>VARIANT_FALSE</strong>.</span></span> <br/> <span data-ttu-id="1f2e8-224">CABAC wird nicht für Basis Linien Profile verwendet.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-224">CABAC is not used for Baseline profile.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f2e8-225"><a href="codecapi-avench264spsid.md">CODECAPI_AVEncH264SPSID</a></span><span class="sxs-lookup"><span data-stu-id="1f2e8-225"><a href="codecapi-avench264spsid.md">CODECAPI_AVEncH264SPSID</a></span></span></td>
<td><span data-ttu-id="1f2e8-226">Legt den Wert <strong>seq_parameter_set_id</strong> in der SPS-nal-Einheit des H. 264-Bitstreams fest.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-226">Sets the value of <strong>seq_parameter_set_id</strong> in the SPS NAL unit of the H.264 bitstream.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f2e8-227"><a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a></span><span class="sxs-lookup"><span data-stu-id="1f2e8-227"><a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a></span></span></td>
<td><span data-ttu-id="1f2e8-228">Legt die maximale Anzahl aufeinander folgender B-Frames im ausgabebitstream fest.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-228">Sets the maximum number of consecutive B frames in the output bitstream.</span></span> <span data-ttu-id="1f2e8-229">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="1f2e8-229">Valid values are:</span></span>
<ul>
<li><span data-ttu-id="1f2e8-230">0: keine Rahmen (Standard) verwenden.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-230">0: Do not use B frames (default).</span></span></li>
<li><span data-ttu-id="1f2e8-231">1: Verwenden Sie einen B-Frame.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-231">1: Use one B frame.</span></span></li>
<li><span data-ttu-id="1f2e8-232">2: Verwenden Sie zwei B-Frames.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-232">2: Use two B frames.</span></span></li>
</ul>
<span data-ttu-id="1f2e8-233">Um diesen Parameter festzulegen, legen Sie die-Eigenschaft vor dem Aufrufen von <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype"><strong>imftransform:: setoutputtype</strong></a>fest.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-233">To set this parameter, set the property before calling <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype"><strong>IMFTransform::SetOutputType</strong></a>.</span></span> <br/> <span data-ttu-id="1f2e8-234">Für das Basis Linien Profil ist die Anzahl der B-Frames immer 0 (null).</span><span class="sxs-lookup"><span data-stu-id="1f2e8-234">For Baseline profile, the number of B frames is always zero.</span></span> <span data-ttu-id="1f2e8-235">Der Encoder überschreibt Werte ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="1f2e8-235">The encoder will override nonzero values.</span></span><br/> <span data-ttu-id="1f2e8-236">Wenn diese Eigenschaft bei anderen H. 264-Profilen ungleich 0 (null) ist, ist das Codierungs Muster ibbpbbp, wobei die maximale Anzahl aufeinander folgender B-Frames gleich <a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a>ist.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-236">For other H.264 profiles, if this property is nonzero, the encoding pattern is IBBPBBP, where the maximum number of consecutive B frames is equal to <a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a>.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f2e8-237"><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></span><span class="sxs-lookup"><span data-stu-id="1f2e8-237"><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></span></span></td>
<td><span data-ttu-id="1f2e8-238">Legt die Anzahl von Bildern von einem GOP-Header auf den nächsten fest, einschließlich des führenden Ankers, jedoch nicht des folgenden.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-238">Sets the number of pictures from one GOP header to the next, including the leading anchor but not the following one.</span></span> <br/> <span data-ttu-id="1f2e8-239">Der gültige Bereich ist [0... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="1f2e8-239">The valid range is [0 ... 2³²–1].</span></span> <span data-ttu-id="1f2e8-240">Wenn der Wert NULL ist, wählt der Encoder die GOP-Größe aus.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-240">If zero, the encoder selects the GOP size.</span></span> <span data-ttu-id="1f2e8-241">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="1f2e8-241">The default value is zero.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f2e8-242"><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></span><span class="sxs-lookup"><span data-stu-id="1f2e8-242"><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></span></span></td>
<td><span data-ttu-id="1f2e8-243">Legt die Anzahl von Arbeitsthreads fest, die von einem Encoder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-243">Sets the number of worker threads used by a encoder.</span></span><br/> <span data-ttu-id="1f2e8-244">Der gültige Bereich ist 0 – 16.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-244">The valid range is 0–16.</span></span> <span data-ttu-id="1f2e8-245">Wenn der Wert NULL ist, wählt der Encoder die Anzahl der Threads aus.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-245">If zero, the encoder selects the number of threads.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f2e8-246"><a href="codecapi-avencvideocontenttype.md">CODECAPI_AVEncVideoContentType</a></span><span class="sxs-lookup"><span data-stu-id="1f2e8-246"><a href="codecapi-avencvideocontenttype.md">CODECAPI_AVEncVideoContentType</a></span></span></td>
<td><span data-ttu-id="1f2e8-247">Gibt den Typ von Videoinhalten an.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-247">Indicates the type of video content.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f2e8-248"><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></span><span class="sxs-lookup"><span data-stu-id="1f2e8-248"><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></span></span></td>
<td><span data-ttu-id="1f2e8-249">Gültiger Bereich: 16 – 51.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-249">Valid range: 16–51.</span></span> <span data-ttu-id="1f2e8-250">Der Standardwert ist 24.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-250">The default value is 24.</span></span> <br/> <span data-ttu-id="1f2e8-251">Diese Eigenschaft wird angewendet, wenn der Raten Steuerungs Modus <strong>eAVEncCommonRateControlMode_Quality</strong>ist.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-251">This property applies when the rate control mode is <strong>eAVEncCommonRateControlMode_Quality</strong>.</span></span> <br/> <span data-ttu-id="1f2e8-252">Diese Eigenschaft konfiguriert die gleiche Codierungs Einstellung wie " <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>rrccommonquality</strong></a>".</span><span class="sxs-lookup"><span data-stu-id="1f2e8-252">This property configures the same encoding setting as <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a>.</span></span> <span data-ttu-id="1f2e8-253">Mithilfe von " <a href="codecapi-avencvideoencodeqp.md">avencvideoencodeqp</a> " kann die Anwendung den Wert von QP jedoch direkt angeben.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-253">However, <a href="codecapi-avencvideoencodeqp.md">AVEncVideoEncodeQP</a> enables the application to specify the value of QP directly.</span></span> <span data-ttu-id="1f2e8-254">Wenn beide Eigenschaften festgelegt sind, überschreibt der Wert von avencvideoencodeqp.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-254">If both properties are set, AVEncVideoEncodeQP overrides.</span></span> <br/> <span data-ttu-id="1f2e8-255">Der Standardwert von 24 entspricht dem Standardwert 70 für die Einstellung " <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>avenccommonquality</strong></a> ".</span><span class="sxs-lookup"><span data-stu-id="1f2e8-255">The default value of 24 corresponds to the default value of 70 for the <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a> setting.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f2e8-256"><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></span><span class="sxs-lookup"><span data-stu-id="1f2e8-256"><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></span></span></td>
<td><span data-ttu-id="1f2e8-257">Zwingt den Encoder, den nächsten Frame als Keyframe zu codieren.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-257">Forces the encoder to code the next frame as a key frame.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f2e8-258"><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></span><span class="sxs-lookup"><span data-stu-id="1f2e8-258"><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></span></span></td>
<td><span data-ttu-id="1f2e8-259">Gültiger Bereich: 0 – 51.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-259">Valid range: 0–51.</span></span> <span data-ttu-id="1f2e8-260">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-260">The default value is 0.</span></span> <br/> <span data-ttu-id="1f2e8-261">Diese Eigenschaft gilt für alle Raten Steuerungs Modi.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-261">This property applies to all rate control modes.</span></span> <span data-ttu-id="1f2e8-262">Der Encoder sollte nicht einen QP-Wert enthalten, der niedriger ist als der Wert, der durch die <a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a> -Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-262">The encoder should not produce a QP value lower than what is specified by the <a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a> property.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f2e8-263"><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></span><span class="sxs-lookup"><span data-stu-id="1f2e8-263"><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></span></span></td>
<td><span data-ttu-id="1f2e8-264">Aktiviert oder deaktiviert den Modus mit niedriger Latenz.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-264">Enables or disables low-latency mode.</span></span> <span data-ttu-id="1f2e8-265">Weitere Informationen finden Sie &quot; im Abschnitt "Hinweise" unter Multithreading &quot; .</span><span class="sxs-lookup"><span data-stu-id="1f2e8-265">See &quot;Multithreading&quot; in the Remarks section.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="1f2e8-266">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f2e8-266">Remarks</span></span>

<span data-ttu-id="1f2e8-267">Der Encoder unterstützt die folgenden Modi für die Raten Steuerung.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-267">The encoder supports the following rate control modes.</span></span>



| <span data-ttu-id="1f2e8-268">Mode</span><span class="sxs-lookup"><span data-stu-id="1f2e8-268">Mode</span></span>                                  | <span data-ttu-id="1f2e8-269">Konstante</span><span class="sxs-lookup"><span data-stu-id="1f2e8-269">Constant</span></span>                                            | <span data-ttu-id="1f2e8-270">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1f2e8-270">Description</span></span>                                                                                                                                                                                                                                         |
|---------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f2e8-271">Konstante Bitrate (CBR)</span><span class="sxs-lookup"><span data-stu-id="1f2e8-271">Constant bit rate (CBR)</span></span>               | <span data-ttu-id="1f2e8-272">**eAVEncCommonRateControlMode_CBR**</span><span class="sxs-lookup"><span data-stu-id="1f2e8-272">**eAVEncCommonRateControlMode_CBR**</span></span>                | <span data-ttu-id="1f2e8-273">Der Encoder versucht, eine Konstante Bitrate mithilfe eines "Leaky Bucket"-Modells zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-273">The encoder tries to achieve a constant bit rate, using a "leaky bucket" model.</span></span> <span data-ttu-id="1f2e8-274">Die Zielbitrate wird durch die [CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-274">The target bit rate is given by the [CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) property.</span></span> <br/> <span data-ttu-id="1f2e8-275">Erfordert Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-275">Requires Windows 8.</span></span> <br/> |
| <span data-ttu-id="1f2e8-276">Bitrate der eingeschränkten Variablen (VBR)</span><span class="sxs-lookup"><span data-stu-id="1f2e8-276">Constrained variable bit rate (VBR)</span></span>   | <span data-ttu-id="1f2e8-277">**eAVEncCommonRateControlMode_PeakConstrainedVBR**</span><span class="sxs-lookup"><span data-stu-id="1f2e8-277">**eAVEncCommonRateControlMode_PeakConstrainedVBR**</span></span> | <span data-ttu-id="1f2e8-278">Der Encoder verwendet ein "Leaky Bucket"-Modell mit einer Spitzen Bitrate.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-278">The encoder uses a "leaky bucket" model with a peak bit rate.</span></span> <span data-ttu-id="1f2e8-279">Die Ausgleichs Rate für den Leaky-Bucket wird durch die [CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-279">The drain rate for the leaky bucket is given by the [CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md) property.</span></span> <br/> <span data-ttu-id="1f2e8-280">Erfordert Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-280">Requires Windows 8.</span></span> <br/>     |
| <span data-ttu-id="1f2e8-281">Qualitäts basierte Variable Bitrate (VBR)</span><span class="sxs-lookup"><span data-stu-id="1f2e8-281">Quality-based variable bit rate (VBR)</span></span> | <span data-ttu-id="1f2e8-282">**eAVEncCommonRateControlMode_Quality**</span><span class="sxs-lookup"><span data-stu-id="1f2e8-282">**eAVEncCommonRateControlMode_Quality**</span></span>            | <span data-ttu-id="1f2e8-283">Der Encoder versucht, eine Konstante Qualitätsstufe zu erreichen, die von der Eigenschaft " [**avenccommonquality**](../directshow/avenccommonquality-property.md) " angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-283">The encoder tries to achieve a constant quality level, given by the [**AVEncCommonQuality**](../directshow/avenccommonquality-property.md) property.</span></span>                                                                                                           |
| <span data-ttu-id="1f2e8-284">Nicht eingeschränkter VBR</span><span class="sxs-lookup"><span data-stu-id="1f2e8-284">Unconstrained VBR</span></span>                     | <span data-ttu-id="1f2e8-285">**eAVEncCommonRateControlMode_UnconstrainedVBR**</span><span class="sxs-lookup"><span data-stu-id="1f2e8-285">**eAVEncCommonRateControlMode_UnconstrainedVBR**</span></span>   | <span data-ttu-id="1f2e8-286">Der Encoder versucht, die Ziel Bitrate zu erreichen, die vom [**MF_MT_AVG_BITRATE**](mf-mt-avg-bitrate-attribute.md) -Attribut im Ausgabe Medientyp angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-286">The encoder tries to achieve the target bitrate given by the [**MF_MT_AVG_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute in the output media type.</span></span> <span data-ttu-id="1f2e8-287">Dies ist der Standardmodus.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-287">This is the default mode.</span></span>                                                              |



 

<span data-ttu-id="1f2e8-288">Für CBR und eingeschränkte VBR-Modi ist Windows 8 erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-288">CBR and constrained VBR modes require Windows 8.</span></span>

<span data-ttu-id="1f2e8-289">In Windows 8 legt der Encoder die folgenden Attribute auf den Ausgabe Beispielen fest:</span><span class="sxs-lookup"><span data-stu-id="1f2e8-289">In Windows 8, the encoder sets the following attributes on the output samples:</span></span>

-   [<span data-ttu-id="1f2e8-290">MFSampleExtension_DecodeTimestamp</span><span class="sxs-lookup"><span data-stu-id="1f2e8-290">MFSampleExtension_DecodeTimestamp</span></span>](mfsampleextension-decodetimestamp.md)
-   [<span data-ttu-id="1f2e8-291">MFSampleExtension_VideoEncodePictureType</span><span class="sxs-lookup"><span data-stu-id="1f2e8-291">MFSampleExtension_VideoEncodePictureType</span></span>](mfsampleextension-videoencodepicturetype.md)
-   [<span data-ttu-id="1f2e8-292">MFSampleExtension_VideoEncodeQP</span><span class="sxs-lookup"><span data-stu-id="1f2e8-292">MFSampleExtension_VideoEncodeQP</span></span>](mfsampleextension-videoencodeqp.md)

> [!Note]  
> <span data-ttu-id="1f2e8-293">In einer früheren Version der Dokumentation wurde fälschlicherweise angegeben, dass der Encoder auf Windows Server 2008 R2 unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-293">A previous version of the documentation incorrectly stated that the encoder is supported on Windows Server 2008 R2.</span></span>

 

### <a name="multithreading"></a><span data-ttu-id="1f2e8-294">Multithreading</span><span class="sxs-lookup"><span data-stu-id="1f2e8-294">Multithreading</span></span>

<span data-ttu-id="1f2e8-295">In Windows 8 unterstützt der Encoder zwei Codierungs Modi:</span><span class="sxs-lookup"><span data-stu-id="1f2e8-295">In Windows 8, the encoder supports two encoding modes:</span></span>

-   <span data-ttu-id="1f2e8-296">**Slice-Codierung.**</span><span class="sxs-lookup"><span data-stu-id="1f2e8-296">**Slice encoding.**</span></span> <span data-ttu-id="1f2e8-297">In diesem Modus werden Slices parallel codiert.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-297">In this mode, slices are encoded in parallel.</span></span> <span data-ttu-id="1f2e8-298">Jeder Slice wird in einem anderen Thread codiert.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-298">Each slice is encoded on a different thread.</span></span> <span data-ttu-id="1f2e8-299">Dieser Modus weist eine geringe Latenzzeit auf, da ein einzelnes Bild parallel codiert wird.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-299">This mode has low latency, because a single picture is encoded in parallel.</span></span> <span data-ttu-id="1f2e8-300">Dieser Ansatz wird jedoch nicht skaliert, wenn die Anzahl der Kerne zunimmt, weil die Anzahl der Slices durch die Anzahl der Makroblock Zeilen im Eingabebild begrenzt ist.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-300">However, this approach does not scale as the number of cores increases, because the number of slices is bounded by the number of macroblock rows in the input picture.</span></span>
-   <span data-ttu-id="1f2e8-301">**Multiframe-Codierung.**</span><span class="sxs-lookup"><span data-stu-id="1f2e8-301">**Multi-frame encoding.**</span></span> <span data-ttu-id="1f2e8-302">In diesem Modus akzeptiert der Encoder mehrere Frames der Eingabe und codiert Sie parallel.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-302">In this mode, the encoder accepts multiple frames of input and encodes them in parallel.</span></span> <span data-ttu-id="1f2e8-303">Dieser Modus wird in einer Umgebung mit mehreren Kernen besser skaliert, führt jedoch zu einer höheren Latenz.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-303">This mode scales better in a multicore environment, but introduces more latency.</span></span>

<span data-ttu-id="1f2e8-304">Der Encoder verwendet standardmäßig die Slice-Codierung, um die Latenz zu minimieren</span><span class="sxs-lookup"><span data-stu-id="1f2e8-304">The encoder defaults to slice encoding, to minimize latency.</span></span> <span data-ttu-id="1f2e8-305">Legen Sie die [CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md) -Eigenschaft auf **VARIANT_FALSE** fest, um die Multi-Frame-Codierung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-305">To enable multi-frame encoding, set the [CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md) property to **VARIANT_FALSE**.</span></span>

<span data-ttu-id="1f2e8-306">Legen Sie die [CODECAPI_AVEncNumWorkerThreads](codecapi-avencnumworkerthreads.md) -Eigenschaft fest, um die Anzahl von Arbeitsthreads festzulegen, die vom Encoder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-306">To set the number of worker threads used by the encoder, set the [CODECAPI_AVEncNumWorkerThreads](codecapi-avencnumworkerthreads.md) property.</span></span>

<span data-ttu-id="1f2e8-307">In Windows 7 verwendet der Encoder immer die Slice-Codierung.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-307">In Windows 7, the encoder always uses slice encoding.</span></span>

### <a name="certified-hardware-encoder"></a><span data-ttu-id="1f2e8-308">Zertifizierter Hardware Encoder</span><span class="sxs-lookup"><span data-stu-id="1f2e8-308">Certified Hardware Encoder</span></span>

<span data-ttu-id="1f2e8-309">Wenn ein zertifizierter Hardware Encoder vorhanden ist, wird er in der Regel anstelle des Eingangsbox System Encoders für Media Foundation bezogenen Szenarios verwendet.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-309">If a certified hardware encoder is present, it will generally be used instead of the inbox system encoder for Media Foundation related scenarios.</span></span> <span data-ttu-id="1f2e8-310">Zertifizierte Encoder sind erforderlich, um einen bestimmten Satz von **icodecapi** -Eigenschaften zu unterstützen, und können optional einen anderen Satz von Eigenschaften unterstützen.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-310">Certified encoders are required to support a certain set of **ICodecAPI** properties and can optionally support another set of properties.</span></span> <span data-ttu-id="1f2e8-311">Der Zertifizierungsprozess sollte sicherstellen, dass die erforderlichen Eigenschaften ordnungsgemäß unterstützt werden, und, wenn eine optionale Eigenschaft unterstützt wird, dass Sie ebenfalls ordnungsgemäß unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-311">The certification process should guarantee that the required properties are properly supported and, if an optional property is supported, that it is also properly supported.</span></span>

<span data-ttu-id="1f2e8-312">Im folgenden finden Sie die erforderlichen und optionalen **icodecapi** -Eigenschaften für Encoder zum übergeben der HCK Encoder-Zertifizierung.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-312">The following is the set of required and optional **ICodecAPI** properties for encoders to pass the HCK encoder certification.</span></span>

<span data-ttu-id="1f2e8-313">Die folgenden Eigenschaften von Windows 8 und Windows 8.1 **icodecapi** sind erforderlich:</span><span class="sxs-lookup"><span data-stu-id="1f2e8-313">The following Windows 8 and Windows 8.1 **ICodecAPI** properties are required:</span></span>

-   [<span data-ttu-id="1f2e8-314">CODECAPI_AVEncCommonRateControlMode</span><span class="sxs-lookup"><span data-stu-id="1f2e8-314">CODECAPI_AVEncCommonRateControlMode</span></span>](../directshow/avenccommonratecontrolmode-property.md)
-   [<span data-ttu-id="1f2e8-315">CODECAPI_AVEncCommonQuality</span><span class="sxs-lookup"><span data-stu-id="1f2e8-315">CODECAPI_AVEncCommonQuality</span></span>](../directshow/avenccommonquality-property.md)
-   [<span data-ttu-id="1f2e8-316">CODECAPI_AVEncCommonQualityVsSpeed</span><span class="sxs-lookup"><span data-stu-id="1f2e8-316">CODECAPI_AVEncCommonQualityVsSpeed</span></span>](../directshow/avenccommonqualityvsspeed-property.md)
-   [<span data-ttu-id="1f2e8-317">CODECAPI_AVEncCommonMeanBitRate</span><span class="sxs-lookup"><span data-stu-id="1f2e8-317">CODECAPI_AVEncCommonMeanBitRate</span></span>](../directshow/avenccommonmeanbitrate-property.md)
-   [<span data-ttu-id="1f2e8-318">CODECAPI_AVEncCommonMaxBitRate</span><span class="sxs-lookup"><span data-stu-id="1f2e8-318">CODECAPI_AVEncCommonMaxBitRate</span></span>](../directshow/avenccommonmaxbitrate-property.md)
-   [<span data-ttu-id="1f2e8-319">CODECAPI_AVEncCommonBufferSize</span><span class="sxs-lookup"><span data-stu-id="1f2e8-319">CODECAPI_AVEncCommonBufferSize</span></span>](../directshow/avenccommonbuffersize-property.md)
-   [<span data-ttu-id="1f2e8-320">CODECAPI_AVEncMPVGOPSize</span><span class="sxs-lookup"><span data-stu-id="1f2e8-320">CODECAPI_AVEncMPVGOPSize</span></span>](../directshow/avencmpvgopsize-property.md)
-   [<span data-ttu-id="1f2e8-321">CODECAPI_AVEncVideoEncodeQP</span><span class="sxs-lookup"><span data-stu-id="1f2e8-321">CODECAPI_AVEncVideoEncodeQP</span></span>](codecapi-avencvideoencodeqp.md)
-   [<span data-ttu-id="1f2e8-322">CODECAPI_AVEncVideoForceKeyFrame</span><span class="sxs-lookup"><span data-stu-id="1f2e8-322">CODECAPI_AVEncVideoForceKeyFrame</span></span>](codecapi-avencvideoforcekeyframe.md)

<span data-ttu-id="1f2e8-323">Die folgenden Windows 8.1 **icodecapi** -Eigenschaften sind optional, werden jedoch in HCK getestet, sofern dies unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-323">The following Windows 8.1 **ICodecAPI** properties are optional, but are tested in HCK if supported.</span></span>

-   [<span data-ttu-id="1f2e8-324">CODECAPI_AVEncVideoMinQP</span><span class="sxs-lookup"><span data-stu-id="1f2e8-324">CODECAPI_AVEncVideoMinQP</span></span>](codecapi-avencvideominqp.md)
-   [<span data-ttu-id="1f2e8-325">CODECAPI_AVEncVideoLTRBufferControl</span><span class="sxs-lookup"><span data-stu-id="1f2e8-325">CODECAPI_AVEncVideoLTRBufferControl</span></span>](codecapi-avencvideoltrbuffercontrol.md)
-   [<span data-ttu-id="1f2e8-326">CODECAPI_AVEncVideoMarkLTRFrame</span><span class="sxs-lookup"><span data-stu-id="1f2e8-326">CODECAPI_AVEncVideoMarkLTRFrame</span></span>](codecapi-avencvideomarkltrframe.md)
-   [<span data-ttu-id="1f2e8-327">CODECAPI_AVEncVideoUseLTRFrame</span><span class="sxs-lookup"><span data-stu-id="1f2e8-327">CODECAPI_AVEncVideoUseLTRFrame</span></span>](codecapi-avencvideouseltrframe.md)
-   [<span data-ttu-id="1f2e8-328">CODECAPI_AVEncVideoEncodeFrameTypeQP</span><span class="sxs-lookup"><span data-stu-id="1f2e8-328">CODECAPI_AVEncVideoEncodeFrameTypeQP</span></span>](codecapi-avencvideoencodeframetypeqp.md)
-   [<span data-ttu-id="1f2e8-329">CODECAPI_AVEncSliceControlMode</span><span class="sxs-lookup"><span data-stu-id="1f2e8-329">CODECAPI_AVEncSliceControlMode</span></span>](codecapi-avencslicecontrolmode.md)
-   [<span data-ttu-id="1f2e8-330">CODECAPI_AVEncSliceControlSize</span><span class="sxs-lookup"><span data-stu-id="1f2e8-330">CODECAPI_AVEncSliceControlSize</span></span>](codecapi-avencslicecontrolsize.md)
-   [<span data-ttu-id="1f2e8-331">CODECAPI_AVEncVideoMaxNumRefFrame</span><span class="sxs-lookup"><span data-stu-id="1f2e8-331">CODECAPI_AVEncVideoMaxNumRefFrame</span></span>](codecapi-avencvideomaxnumrefframe.md)
-   [<span data-ttu-id="1f2e8-332">CODECAPI_AVEncVideoMeanAbsoluteDifference</span><span class="sxs-lookup"><span data-stu-id="1f2e8-332">CODECAPI_AVEncVideoMeanAbsoluteDifference</span></span>](codecapi-avencvideomeanabsolutedifference.md)
-   [<span data-ttu-id="1f2e8-333">CODECAPI_AVEncVideoMaxQP</span><span class="sxs-lookup"><span data-stu-id="1f2e8-333">CODECAPI_AVEncVideoMaxQP</span></span>](codecapi-avencvideomaxqp.md)
-   [<span data-ttu-id="1f2e8-334">CODECAPI_AVEncVideoROIEnabled</span><span class="sxs-lookup"><span data-stu-id="1f2e8-334">CODECAPI_AVEncVideoROIEnabled</span></span>](codecapi-avencvideoroienabled.md)
-   <span data-ttu-id="1f2e8-335">[CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (dynamisch)</span><span class="sxs-lookup"><span data-stu-id="1f2e8-335">[CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (Dynamic)</span></span>
-   [<span data-ttu-id="1f2e8-336">CODECAPI_AVEncH264CABACEnable</span><span class="sxs-lookup"><span data-stu-id="1f2e8-336">CODECAPI_AVEncH264CABACEnable</span></span>](codecapi-avench264cabacenable.md)

<span data-ttu-id="1f2e8-337">Die folgenden Eigenschaften von Windows 8 und Windows 8.1 **icodecapi** sind optional, werden aber in HCK getestet, sofern dies unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-337">The following Windows 8 and Windows 8.1 **ICodecAPI** properties are optional, but are tested in HCK if supported.</span></span>

-   <span data-ttu-id="1f2e8-338">[CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (statisch)</span><span class="sxs-lookup"><span data-stu-id="1f2e8-338">[CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (Static)</span></span>
-   [<span data-ttu-id="1f2e8-339">CODECAPI_AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="1f2e8-339">CODECAPI_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)

<span data-ttu-id="1f2e8-340">Die folgenden **icodecapi** -Eigenschaften sind optional.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-340">The following **ICodecAPI** properties are optional.</span></span> <span data-ttu-id="1f2e8-341">Sie werden nicht in HCK getestet.</span><span class="sxs-lookup"><span data-stu-id="1f2e8-341">They are not tested in HCK.</span></span>

-   [<span data-ttu-id="1f2e8-342">CODECAPI_AVEncMPVDefaultBPictureCount</span><span class="sxs-lookup"><span data-stu-id="1f2e8-342">CODECAPI_AVEncMPVDefaultBPictureCount</span></span>](../directshow/avencmpvdefaultbpicturecount-property.md)

## <a name="requirements"></a><span data-ttu-id="1f2e8-343">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f2e8-343">Requirements</span></span>



| <span data-ttu-id="1f2e8-344">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f2e8-344">Requirement</span></span> | <span data-ttu-id="1f2e8-345">Wert</span><span class="sxs-lookup"><span data-stu-id="1f2e8-345">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f2e8-346">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1f2e8-346">Minimum supported client</span></span><br/> | <span data-ttu-id="1f2e8-347">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f2e8-347">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1f2e8-348">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1f2e8-348">Minimum supported server</span></span><br/> | <span data-ttu-id="1f2e8-349">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1f2e8-349">None supported</span></span><br/>                                                                |
| <span data-ttu-id="1f2e8-350">DLL</span><span class="sxs-lookup"><span data-stu-id="1f2e8-350">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f2e8-351"><dt>Mfh264enc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f2e8-351"><dt>Mfh264enc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f2e8-352">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f2e8-352">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f2e8-353">Codec-Objekte</span><span class="sxs-lookup"><span data-stu-id="1f2e8-353">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="1f2e8-354">MPEG-4-Unterstützung in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1f2e8-354">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="1f2e8-355">Unterstützte Medienformate in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1f2e8-355">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="1f2e8-356">Video Medientypen</span><span class="sxs-lookup"><span data-stu-id="1f2e8-356">Video Media Types</span></span>](video-media-types.md)
</dt> </dl>

 

 
