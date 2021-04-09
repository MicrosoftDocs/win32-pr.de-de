---
description: Der Video Encoder Media Foundation H. 265 ist eine Media Foundation Transformation, die das Codieren von Inhalten in das H. 265/hevc-Format unterstützt.
ms.assetid: 790CFB39-6FC0-432D-A434-5262C30EABF4
title: H. 265/hevc-Video Encoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015295792a72f3250c47389192586dbc00566858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959193"
---
# <a name="h265--hevc-video-encoder"></a><span data-ttu-id="f834f-103">H. 265/hevc-Video Encoder</span><span class="sxs-lookup"><span data-stu-id="f834f-103">H.265 / HEVC Video Encoder</span></span>

<span data-ttu-id="f834f-104">Der Video Encoder Media Foundation H. 265 ist eine [Media Foundation Transformation](media-foundation-transforms.md) , die das Codieren von Inhalten in das H. 265/hevc-Format unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f834f-104">The Media Foundation H.265 video encoder is a [Media Foundation Transform](media-foundation-transforms.md) that supports encoding content into the H.265/HEVC format.</span></span> <span data-ttu-id="f834f-105">Der Encoder unterstützt die folgenden Profile:</span><span class="sxs-lookup"><span data-stu-id="f834f-105">The encoder supports the following profiles:</span></span>

-   <span data-ttu-id="f834f-106">Profil: Main</span><span class="sxs-lookup"><span data-stu-id="f834f-106">Main Profile</span></span>

<span data-ttu-id="f834f-107">Der H. 265-Video Encoder macht die folgenden Schnittstellen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="f834f-107">The H.265 video encoder exposes the following interfaces:</span></span>

-   [<span data-ttu-id="f834f-108">**Icodecapi**</span><span class="sxs-lookup"><span data-stu-id="f834f-108">**ICodecAPI**</span></span>](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [<span data-ttu-id="f834f-109">**IMF-Transformation**</span><span class="sxs-lookup"><span data-stu-id="f834f-109">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a><span data-ttu-id="f834f-110">Eingabetypen</span><span class="sxs-lookup"><span data-stu-id="f834f-110">Input Types</span></span>

<span data-ttu-id="f834f-111">Der Eingabe Medientyp muss einen der folgenden Untertypen aufweisen:</span><span class="sxs-lookup"><span data-stu-id="f834f-111">The input media type must have one of the following subtypes:</span></span>

-   <span data-ttu-id="f834f-112">**MF-Format ( \_ IYUV)**</span><span class="sxs-lookup"><span data-stu-id="f834f-112">**MFVideoFormat\_IYUV**</span></span>
-   <span data-ttu-id="f834f-113">**MF-Format \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="f834f-113">**MFVideoFormat\_NV12**</span></span>
-   <span data-ttu-id="f834f-114">**MF-Format \_ im YUY2**</span><span class="sxs-lookup"><span data-stu-id="f834f-114">**MFVideoFormat\_YUY2**</span></span>
-   <span data-ttu-id="f834f-115">**MF-Format \_ YV12**</span><span class="sxs-lookup"><span data-stu-id="f834f-115">**MFVideoFormat\_YV12**</span></span>

<span data-ttu-id="f834f-116">Weitere Informationen zu diesen Untertypen finden Sie unter [Video Untertyp-GUIDs](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="f834f-116">For more information about these subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

<span data-ttu-id="f834f-117">Der Ausgabetyp muss vor dem Eingabetyp festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f834f-117">The output type must be set before the input type.</span></span> <span data-ttu-id="f834f-118">Bis der Ausgabetyp festgelegt ist, gibt die [**IMF Transform:: setinputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) -Methode des Encoders einen **\_ \_ \_ \_ nicht \_ festgelegten MF E-Transformationstyp** zurück.</span><span class="sxs-lookup"><span data-stu-id="f834f-118">Until the output type is set, the encoder's [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) method returns **MF\_E\_TRANSFORM\_TYPE\_NOT\_SET**.</span></span>

## <a name="output-types"></a><span data-ttu-id="f834f-119">Ausgabetypen</span><span class="sxs-lookup"><span data-stu-id="f834f-119">Output Types</span></span>

<span data-ttu-id="f834f-120">Der Encoder unterstützt einen einzelnen Ausgabe Untertyp:</span><span class="sxs-lookup"><span data-stu-id="f834f-120">The encoder supports a single output subtype:</span></span>

-   <span data-ttu-id="f834f-121">**MF-Format \_ H265**</span><span class="sxs-lookup"><span data-stu-id="f834f-121">**MFVideoFormat\_H265**</span></span>

<span data-ttu-id="f834f-122">Legen Sie die folgenden Attribute für den Ausgabe Medientyp fest.</span><span class="sxs-lookup"><span data-stu-id="f834f-122">Set the following attributes on the output media type.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f834f-123">Attribut</span><span class="sxs-lookup"><span data-stu-id="f834f-123">Attribute</span></span></th>
<th><span data-ttu-id="f834f-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f834f-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f834f-125"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="f834f-125"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="f834f-126">Der Haupttyp.</span><span class="sxs-lookup"><span data-stu-id="f834f-126">Major type.</span></span> <span data-ttu-id="f834f-127">Muss <strong>MFMediaType_Video</strong>werden.</span><span class="sxs-lookup"><span data-stu-id="f834f-127">Must be <strong>MFMediaType_Video</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f834f-128"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="f834f-128"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="f834f-129">Video Untertyp.</span><span class="sxs-lookup"><span data-stu-id="f834f-129">Video subtype.</span></span> <span data-ttu-id="f834f-130">Muss <strong>MFVideoFormat_HEVC</strong>werden.</span><span class="sxs-lookup"><span data-stu-id="f834f-130">Must be <strong>MFVideoFormat_HEVC</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f834f-131"><a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="f834f-131"><a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a></span></span></td>
<td><span data-ttu-id="f834f-132">Die durchschnittliche codierte Bitrate in Bits pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="f834f-132">Average encoded bit rate, in bits per second.</span></span> <span data-ttu-id="f834f-133">Muss größer sein als Null.</span><span class="sxs-lookup"><span data-stu-id="f834f-133">Must be greater than zero.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f834f-134"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="f834f-134"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span></span></td>
<td><span data-ttu-id="f834f-135">Die Framerate.</span><span class="sxs-lookup"><span data-stu-id="f834f-135">Frame rate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f834f-136"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="f834f-136"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span></span></td>
<td><span data-ttu-id="f834f-137">Frame Größe.</span><span class="sxs-lookup"><span data-stu-id="f834f-137">Frame size.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f834f-138"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="f834f-138"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span></span></td>
<td><span data-ttu-id="f834f-139">Interlace-Modus.</span><span class="sxs-lookup"><span data-stu-id="f834f-139">Interlace mode.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f834f-140"><a href="mf-mt-video-profile.md">MF_MT_VIDEO_PROFILE</a></span><span class="sxs-lookup"><span data-stu-id="f834f-140"><a href="mf-mt-video-profile.md">MF_MT_VIDEO_PROFILE</a></span></span></td>
<td><span data-ttu-id="f834f-141">H. 265-Codierungs Profil.</span><span class="sxs-lookup"><span data-stu-id="f834f-141">H.265 encoding profile.</span></span><br/> <span data-ttu-id="f834f-142">Die unterstützten Werte sind:</span><span class="sxs-lookup"><span data-stu-id="f834f-142">The supported values are:</span></span> <br/>
<ul>
<li><span data-ttu-id="f834f-143"><strong>eAVEncH265VProfile_Main_420_8</strong></span><span class="sxs-lookup"><span data-stu-id="f834f-143"><strong>eAVEncH265VProfile_Main_420_8</strong></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f834f-144"><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></span><span class="sxs-lookup"><span data-stu-id="f834f-144"><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></span></span></td>
<td><span data-ttu-id="f834f-145">Gibt die Ebene des codierten Videos an.</span><span class="sxs-lookup"><span data-stu-id="f834f-145">Specifies the level of the coded video.</span></span> <span data-ttu-id="f834f-146">Weitere Informationen zu den Einschränkungen für Profile und Ebenen finden Sie in Anhang A von ITU-T H. 265.</span><span class="sxs-lookup"><span data-stu-id="f834f-146">For more information about profile and level constraints, refer to Annex A of ITU-T H.265.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f834f-147"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span><span class="sxs-lookup"><span data-stu-id="f834f-147"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span></span></td>
<td><span data-ttu-id="f834f-148">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="f834f-148">Optional.</span></span> <span data-ttu-id="f834f-149">Gibt das Pixel Seitenverhältnis an.</span><span class="sxs-lookup"><span data-stu-id="f834f-149">Specifies the pixel aspect ratio.</span></span> <span data-ttu-id="f834f-150">Der Standardwert ist 1:1.</span><span class="sxs-lookup"><span data-stu-id="f834f-150">The default value is 1:1.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f834f-151">Nachdem der Ausgabetyp festgelegt wurde, aktualisiert der Video Encoder den Typ durch Hinzufügen des [**MF \_ MT-MPEG- \_ \_ Sequenz \_ Header**](mf-mt-mpeg-sequence-header-attribute.md) Attributs.</span><span class="sxs-lookup"><span data-stu-id="f834f-151">After the output type is set, the video encoder updates the type by adding the [**MF\_MT\_MPEG\_SEQUENCE\_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) attribute.</span></span> <span data-ttu-id="f834f-152">Dieses Attribut enthält den Sequence-Header.</span><span class="sxs-lookup"><span data-stu-id="f834f-152">This attribute contains the sequence header.</span></span>

## <a name="supported-imftransform-methods"></a><span data-ttu-id="f834f-153">Unterstützte IMF Transform-Methoden</span><span class="sxs-lookup"><span data-stu-id="f834f-153">Supported IMFTransform methods</span></span>

<span data-ttu-id="f834f-154">Die folgenden Methoden der [**IMF Transform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle werden für den H. 265/hevc-Encoder unterstützt:</span><span class="sxs-lookup"><span data-stu-id="f834f-154">The following methods of the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface are supported for the H.265/HEVC encoder:</span></span>

-   [<span data-ttu-id="f834f-155">**GetAttributes**</span><span class="sxs-lookup"><span data-stu-id="f834f-155">**GetAttributes**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)
-   [<span data-ttu-id="f834f-156">**Getinputavailabletype**</span><span class="sxs-lookup"><span data-stu-id="f834f-156">**GetInputAvailableType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype)
-   [<span data-ttu-id="f834f-157">**Getinputcurrenttype**</span><span class="sxs-lookup"><span data-stu-id="f834f-157">**GetInputCurrentType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype)
-   [<span data-ttu-id="f834f-158">**Getinputstatus**</span><span class="sxs-lookup"><span data-stu-id="f834f-158">**GetInputStatus**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstatus)
-   [<span data-ttu-id="f834f-159">**Getinputstreaminfo**</span><span class="sxs-lookup"><span data-stu-id="f834f-159">**GetInputStreamInfo**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)
-   [<span data-ttu-id="f834f-160">**Getoutputavailabletype**</span><span class="sxs-lookup"><span data-stu-id="f834f-160">**GetOutputAvailableType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)
-   [<span data-ttu-id="f834f-161">**Getoutputcurrenttype**</span><span class="sxs-lookup"><span data-stu-id="f834f-161">**GetOutputCurrentType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype)
-   [<span data-ttu-id="f834f-162">**Getoutputstatus**</span><span class="sxs-lookup"><span data-stu-id="f834f-162">**GetOutputStatus**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstatus)
-   [<span data-ttu-id="f834f-163">**Getoutputstreaminfo**</span><span class="sxs-lookup"><span data-stu-id="f834f-163">**GetOutputStreamInfo**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)
-   [<span data-ttu-id="f834f-164">**Getstreamcount**</span><span class="sxs-lookup"><span data-stu-id="f834f-164">**GetStreamCount**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount)
-   [<span data-ttu-id="f834f-165">**Getstreamlimits**</span><span class="sxs-lookup"><span data-stu-id="f834f-165">**GetStreamLimits**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamlimits)
-   [<span data-ttu-id="f834f-166">**ProcessEvent**</span><span class="sxs-lookup"><span data-stu-id="f834f-166">**ProcessEvent**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)
-   [<span data-ttu-id="f834f-167">**ProcessMessage**</span><span class="sxs-lookup"><span data-stu-id="f834f-167">**ProcessMessage**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)
-   [<span data-ttu-id="f834f-168">**ProcessInput**</span><span class="sxs-lookup"><span data-stu-id="f834f-168">**ProcessInput**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)
-   [<span data-ttu-id="f834f-169">**ProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="f834f-169">**ProcessOutput**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
-   [<span data-ttu-id="f834f-170">**"Ttinputtype"**</span><span class="sxs-lookup"><span data-stu-id="f834f-170">**SetInputType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)
-   [<span data-ttu-id="f834f-171">**Setoutputtype**</span><span class="sxs-lookup"><span data-stu-id="f834f-171">**SetOutputType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)
-   [<span data-ttu-id="f834f-172">**Setoutputbounds**</span><span class="sxs-lookup"><span data-stu-id="f834f-172">**SetOutputBounds**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds)

<span data-ttu-id="f834f-173">Alle anderen [**IMF Transform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Methoden geben den Fehler E \_ notimpl zurück.</span><span class="sxs-lookup"><span data-stu-id="f834f-173">All other [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) methods will return the error E\_NOTIMPL.</span></span>

## <a name="supported-icodecapi-methods"></a><span data-ttu-id="f834f-174">Unterstützte icodecapi-Methoden</span><span class="sxs-lookup"><span data-stu-id="f834f-174">Supported ICodecAPI methods</span></span>

<span data-ttu-id="f834f-175">Die folgenden Methoden der [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Schnittstelle werden für den H. 265/hevc-Encoder unterstützt:</span><span class="sxs-lookup"><span data-stu-id="f834f-175">The following methods of the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface are supported for the H.265/HEVC encoder:</span></span>

-   [<span data-ttu-id="f834f-176">**IsSupported**</span><span class="sxs-lookup"><span data-stu-id="f834f-176">**IsSupported**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [<span data-ttu-id="f834f-177">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="f834f-177">**SetValue**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)
-   [<span data-ttu-id="f834f-178">**GetValue**</span><span class="sxs-lookup"><span data-stu-id="f834f-178">**GetValue**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [<span data-ttu-id="f834f-179">**Getparameterrange**</span><span class="sxs-lookup"><span data-stu-id="f834f-179">**GetParameterRange**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [<span data-ttu-id="f834f-180">**GetParameterValues**</span><span class="sxs-lookup"><span data-stu-id="f834f-180">**GetParameterValues**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)

<span data-ttu-id="f834f-181">Alle anderen [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Methoden geben den Fehler E \_ notimpl zurück.</span><span class="sxs-lookup"><span data-stu-id="f834f-181">All other [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) methods will return the error E\_NOTIMPL.</span></span>

## <a name="codec-properties"></a><span data-ttu-id="f834f-182">Codec-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f834f-182">Codec Properties</span></span>

<span data-ttu-id="f834f-183">Der H. 265-Encoder implementiert die [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Schnittstelle zum Festlegen von Codierungs Parametern.</span><span class="sxs-lookup"><span data-stu-id="f834f-183">The H.265 encoder implements the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface for setting encoding parameters.</span></span> <span data-ttu-id="f834f-184">Die folgenden Eigenschaften werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="f834f-184">It supports the following properties.</span></span>

<span data-ttu-id="f834f-185">Die Codec-Anforderungen für die HCK Encoder-Zertifizierung finden Sie weiter unten im Abschnitt **Certified Hardware Encoder** .</span><span class="sxs-lookup"><span data-stu-id="f834f-185">For the codec requirements for HCK encoder certification, see the **Certified Hardware Encoder** section below.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f834f-186">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f834f-186">Property</span></span></th>
<th><span data-ttu-id="f834f-187">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f834f-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f834f-188"><a href="/windows/desktop/DirectShow/avenccommonratecontrolmode-property"><strong>CODECAPI_AVEncCommonRateControlMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="f834f-188"><a href="/windows/desktop/DirectShow/avenccommonratecontrolmode-property"><strong>CODECAPI_AVEncCommonRateControlMode</strong></a></span></span></td>
<td><span data-ttu-id="f834f-189">Legt den Raten Steuerungs Modus fest.</span><span class="sxs-lookup"><span data-stu-id="f834f-189">Sets the rate control mode.</span></span> <span data-ttu-id="f834f-190">Unterstützte Modi:</span><span class="sxs-lookup"><span data-stu-id="f834f-190">The supported modes are:</span></span><br/>
<ul>
<li><span data-ttu-id="f834f-191"><strong>eAVEncCommonRateControlMode_CBR</strong></span><span class="sxs-lookup"><span data-stu-id="f834f-191"><strong>eAVEncCommonRateControlMode_CBR</strong></span></span></li>
<li><span data-ttu-id="f834f-192"><strong>eAVEncCommonRateControlMode_Quality</strong></span><span class="sxs-lookup"><span data-stu-id="f834f-192"><strong>eAVEncCommonRateControlMode_Quality</strong></span></span></li>
</ul>
<span data-ttu-id="f834f-193">Wenn andere Modi angegeben werden, wird die <strong>eAVEncCommonRateControlMode_CBR</strong> Raten Steuerung verwendet.</span><span class="sxs-lookup"><span data-stu-id="f834f-193">If other modes are specified, the <strong>eAVEncCommonRateControlMode_CBR</strong> rate control will be used.</span></span><br/> <span data-ttu-id="f834f-194">Dies ist ein VT_UI4 Wert.</span><span class="sxs-lookup"><span data-stu-id="f834f-194">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f834f-195"><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></span><span class="sxs-lookup"><span data-stu-id="f834f-195"><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></span></span></td>
<td><span data-ttu-id="f834f-196">Legt die durchschnittliche Bitrate für den codierten Bitstream in Bits pro Sekunde fest.</span><span class="sxs-lookup"><span data-stu-id="f834f-196">Sets the average bit rate for the encoded bit stream, in bits per second.</span></span> <br/> <span data-ttu-id="f834f-197">Der gültige Bereich ist [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="f834f-197">The valid range is [1 ... 2³²–1].</span></span> <br/> <span data-ttu-id="f834f-198">Dies ist ein VT_UI4 Wert.</span><span class="sxs-lookup"><span data-stu-id="f834f-198">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f834f-199"><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></span><span class="sxs-lookup"><span data-stu-id="f834f-199"><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></span></span></td>
<td><span data-ttu-id="f834f-200">Legt die Puffergröße in Bytes für die Konstante Bitrate (CBR)-Codierung fest.</span><span class="sxs-lookup"><span data-stu-id="f834f-200">Sets the buffer size, in bytes, for constant bit rate (CBR) encoding.</span></span><br/> <span data-ttu-id="f834f-201">Der gültige Bereich ist [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="f834f-201">The valid range is [1 ... 2³²–1].</span></span> <br/> <span data-ttu-id="f834f-202">Dies ist ein VT_UI4 Wert.</span><span class="sxs-lookup"><span data-stu-id="f834f-202">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f834f-203"><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></span><span class="sxs-lookup"><span data-stu-id="f834f-203"><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></span></span></td>
<td><span data-ttu-id="f834f-204">Legt die maximale Bitrate für Raten Steuerungs Modi fest, die eine Spitzen Bitrate zulassen.</span><span class="sxs-lookup"><span data-stu-id="f834f-204">Sets the maximum bitrate for rate control modes that allow a peak bitrate.</span></span> <br/> <span data-ttu-id="f834f-205">Der gültige Bereich ist [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="f834f-205">The valid range is [1 ... 2³²–1].</span></span> <br/> <span data-ttu-id="f834f-206">Dies ist ein VT_UI4 Wert.</span><span class="sxs-lookup"><span data-stu-id="f834f-206">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f834f-207"><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></span><span class="sxs-lookup"><span data-stu-id="f834f-207"><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></span></span></td>
<td><span data-ttu-id="f834f-208">Legt die Anzahl von Bildern von einem GOP-Header auf den nächsten fest, einschließlich des führenden Ankers, jedoch nicht des folgenden.</span><span class="sxs-lookup"><span data-stu-id="f834f-208">Sets the number of pictures from one GOP header to the next, including the leading anchor but not the following one.</span></span> <br/> <span data-ttu-id="f834f-209">Der gültige Bereich ist [0... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="f834f-209">The valid range is [0 ... 2³²–1].</span></span> <span data-ttu-id="f834f-210">Wenn der Wert NULL ist, wählt der Encoder die GOP-Größe aus.</span><span class="sxs-lookup"><span data-stu-id="f834f-210">If zero, the encoder selects the GOP size.</span></span> <span data-ttu-id="f834f-211">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="f834f-211">The default value is zero.</span></span> <br/> <span data-ttu-id="f834f-212">Dies ist ein VT_UI4 Wert.</span><span class="sxs-lookup"><span data-stu-id="f834f-212">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f834f-213"><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></span><span class="sxs-lookup"><span data-stu-id="f834f-213"><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></span></span></td>
<td><span data-ttu-id="f834f-214">Aktiviert oder deaktiviert den Modus mit niedriger Latenz.</span><span class="sxs-lookup"><span data-stu-id="f834f-214">Enables or disables low-latency mode.</span></span> <br/> <span data-ttu-id="f834f-215">Dies ist ein VT_BOOL Wert.</span><span class="sxs-lookup"><span data-stu-id="f834f-215">This is a VT_BOOL value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f834f-216"><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></span><span class="sxs-lookup"><span data-stu-id="f834f-216"><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></span></span></td>
<td><span data-ttu-id="f834f-217">Legt den Kompromiss der Qualität/Geschwindigkeit fest.</span><span class="sxs-lookup"><span data-stu-id="f834f-217">Sets the quality/speed tradeoff.</span></span> <span data-ttu-id="f834f-218">Dieser Wert wirkt sich darauf aus, wie der Encoder verschiedene Codierungs Vorgänge ausführt, z. b. Motion Compensation.</span><span class="sxs-lookup"><span data-stu-id="f834f-218">This value affects how the encoder performs various encoding operations, such as motion compensation.</span></span> <span data-ttu-id="f834f-219">Bei höheren Komplexitätsstufen führt der Encoder langsamer aus, erzeugt aber eine bessere Qualität mit derselben Bitrate.</span><span class="sxs-lookup"><span data-stu-id="f834f-219">At higher complexity levels, the encoder runs more slowly but produces better quality at the same bit rate.</span></span> <br/> <span data-ttu-id="f834f-220">Der gültige Bereich ist 0 – 100.</span><span class="sxs-lookup"><span data-stu-id="f834f-220">The valid range is 0 – 100.</span></span> <span data-ttu-id="f834f-221">Intern wird dieser Wert einem kleineren Satz von Qualitäts-und Geschwindigkeitsstufen zugeordnet, der vom Encoder unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="f834f-221">Internally, this value is mapped to a smaller set of quality/speed levels supported by the encoder.</span></span><br/> <span data-ttu-id="f834f-222">Dies ist ein VT_UI4 Wert.</span><span class="sxs-lookup"><span data-stu-id="f834f-222">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f834f-223"><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></span><span class="sxs-lookup"><span data-stu-id="f834f-223"><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></span></span></td>
<td><span data-ttu-id="f834f-224">Zwingt den Encoder, den nächsten Frame als Keyframe zu codieren.</span><span class="sxs-lookup"><span data-stu-id="f834f-224">Forces the encoder to code the next frame as a key frame.</span></span><br/> <span data-ttu-id="f834f-225">Dies ist ein VT_UI4 Wert.</span><span class="sxs-lookup"><span data-stu-id="f834f-225">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f834f-226"><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></span><span class="sxs-lookup"><span data-stu-id="f834f-226"><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></span></span></td>
<td><span data-ttu-id="f834f-227">Wenn diese Eigenschaft festgelegt wird, bewirkt dies, dass der Encoder das angegebene QP verwendet, um den nächsten Frame und alle nachfolgenden Frames zu codieren, bis ein neues QP angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f834f-227">When this property is set it will cause the encoder to use the specified QP to encode the next frame and all subsequent frames until a new QP is specified.</span></span> <br/> <span data-ttu-id="f834f-228">Gültiger Bereich: 0 – 51, inklusiv</span><span class="sxs-lookup"><span data-stu-id="f834f-228">Valid range: 0–51, inclusive</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f834f-229"><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></span><span class="sxs-lookup"><span data-stu-id="f834f-229"><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></span></span></td>
<td><span data-ttu-id="f834f-230">Mit dieser Eigenschaft wird ein Grenzwert für den minimalen QP festgelegt, der vom Encoder während der CBR-Ratecontrol verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f834f-230">This property will set a limit on the minimum QP that the encoder can use during CBR ratecontrol.</span></span><br/> <span data-ttu-id="f834f-231">Dies ist ein VT_UI4 Wert.</span><span class="sxs-lookup"><span data-stu-id="f834f-231">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f834f-232"><a href="codecapi-avencvideomaxqp.md">CODECAPI_AVEncVideoMaxQP</a></span><span class="sxs-lookup"><span data-stu-id="f834f-232"><a href="codecapi-avencvideomaxqp.md">CODECAPI_AVEncVideoMaxQP</a></span></span></td>
<td><span data-ttu-id="f834f-233">Mit dieser Eigenschaft wird ein Grenzwert für die maximale Anzahl von QP festgelegt, die der Encoder während der CBR-Ratecontrol verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="f834f-233">This property will set a limit on the maximum QP that the encoder can use during CBR ratecontrol.</span></span><br/> <span data-ttu-id="f834f-234">Dies ist ein VT_UI4 Wert.</span><span class="sxs-lookup"><span data-stu-id="f834f-234">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f834f-235"><a href="codecapi-videoencoderdisplaycontenttype.md">CODECAPI_VideoEncoderDisplayContentType</a></span><span class="sxs-lookup"><span data-stu-id="f834f-235"><a href="codecapi-videoencoderdisplaycontenttype.md">CODECAPI_VideoEncoderDisplayContentType</a></span></span></td>
<td><span data-ttu-id="f834f-236">Legt fest, ob es sich bei dem Inhalt um Vollbildvideos handelt, im Gegensatz zu Bildschirm Inhalten, die möglicherweise ein kleineres Videofenster enthalten oder überhaupt kein Video enthalten.</span><span class="sxs-lookup"><span data-stu-id="f834f-236">Sets whether the content is full-screen video, as opposed to screen content that might have a smaller window of video or have no video at all.</span></span><br/> <span data-ttu-id="f834f-237">Dies ist ein VT_UI4 Wert.</span><span class="sxs-lookup"><span data-stu-id="f834f-237">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f834f-238"><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></span><span class="sxs-lookup"><span data-stu-id="f834f-238"><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></span></span></td>
<td><span data-ttu-id="f834f-239">Legt die Anzahl von Threads fest, die verwendet werden, um den Komprimierungs Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f834f-239">Sets the number of threads used to perform the compression operation.</span></span> <span data-ttu-id="f834f-240">Der Encoder teilt den Frame in Kacheln auf, sodass die Anzahl der Threads der Anzahl der Kacheln gleicht.</span><span class="sxs-lookup"><span data-stu-id="f834f-240">The encoder will divide the frame into tiles such that the number of threads equals the number of tiles.</span></span><br/>
<ul>
<li><span data-ttu-id="f834f-241">Die Anzahl der logischen Prozessoren.</span><span class="sxs-lookup"><span data-stu-id="f834f-241">The number of logical processors.</span></span> <span data-ttu-id="f834f-242">Die Anzahl der Threads muss kleiner oder gleich der Anzahl der logischen Prozessoren sein.</span><span class="sxs-lookup"><span data-stu-id="f834f-242">The number of threads must be less than or equal to the number of logical processors.</span></span></li>
<li><span data-ttu-id="f834f-243">Die Größe des Frames.</span><span class="sxs-lookup"><span data-stu-id="f834f-243">The size of the frame.</span></span> <span data-ttu-id="f834f-244">Die Größe einer Kachel muss größer oder gleich 265x 64 Pixel sein.</span><span class="sxs-lookup"><span data-stu-id="f834f-244">The size of a tile must bigger than or equal to 265x64 pixels.</span></span></li>
<li><span data-ttu-id="f834f-245">Parität:</span><span class="sxs-lookup"><span data-stu-id="f834f-245">Parity.</span></span> <span data-ttu-id="f834f-246">Die Anzahl der Threads muss ein geraden Wert sein.</span><span class="sxs-lookup"><span data-stu-id="f834f-246">The number of threads must be an even value.</span></span> <span data-ttu-id="f834f-247">Wenn der angegebene Wert ungerade ist, wird der nächste niedrigere gleich Wert verwendet.</span><span class="sxs-lookup"><span data-stu-id="f834f-247">If the specified value is odd then the next lower even value will be used.</span></span></li>
</ul>
<span data-ttu-id="f834f-248">Dies ist ein VT_UI4 Wert.</span><span class="sxs-lookup"><span data-stu-id="f834f-248">This is a VT_UI4 value.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="certified-hardware-encoder"></a><span data-ttu-id="f834f-249">Zertifizierter Hardware Encoder</span><span class="sxs-lookup"><span data-stu-id="f834f-249">Certified Hardware Encoder</span></span>

<span data-ttu-id="f834f-250">Wenn ein zertifizierter Hardware Encoder vorhanden ist, wird er in der Regel anstelle des Eingangsbox System Encoders für Media Foundation bezogenen Szenarios verwendet.</span><span class="sxs-lookup"><span data-stu-id="f834f-250">If a certified hardware encoder is present, it will generally be used instead of the inbox system encoder for Media Foundation related scenarios.</span></span> <span data-ttu-id="f834f-251">Zertifizierte Encoder sind erforderlich, um einen bestimmten Satz von **icodecapi** -Eigenschaften zu unterstützen, und können optional einen anderen Satz von Eigenschaften unterstützen.</span><span class="sxs-lookup"><span data-stu-id="f834f-251">Certified encoders are required to support a certain set of **ICodecAPI** properties and can optionally support another set of properties.</span></span> <span data-ttu-id="f834f-252">Der Zertifizierungsprozess sollte sicherstellen, dass die erforderlichen Eigenschaften ordnungsgemäß unterstützt werden, und, wenn eine optionale Eigenschaft unterstützt wird, dass Sie ebenfalls ordnungsgemäß unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="f834f-252">The certification process should guarantee that the required properties are properly supported and, if an optional property is supported, that it is also properly supported.</span></span>

<span data-ttu-id="f834f-253">Im folgenden finden Sie die erforderlichen und optionalen **icodecapi** -Eigenschaften für Encoder zum übergeben der HCK Encoder-Zertifizierung.</span><span class="sxs-lookup"><span data-stu-id="f834f-253">The following is the set of required and optional **ICodecAPI** properties for encoders to pass the HCK encoder certification.</span></span>

-   [<span data-ttu-id="f834f-254">Codecapi \_ avenccommonratecontrolmode</span><span class="sxs-lookup"><span data-stu-id="f834f-254">CODECAPI\_AVEncCommonRateControlMode</span></span>](../directshow/avenccommonratecontrolmode-property.md)
-   [<span data-ttu-id="f834f-255">Codecapi \_ avenccommonquality</span><span class="sxs-lookup"><span data-stu-id="f834f-255">CODECAPI\_AVEncCommonQuality</span></span>](../directshow/avenccommonquality-property.md)
-   [<span data-ttu-id="f834f-256">Codecapi \_ avenccommonmeanbitrate</span><span class="sxs-lookup"><span data-stu-id="f834f-256">CODECAPI\_AVEncCommonMeanBitRate</span></span>](../directshow/avenccommonmeanbitrate-property.md)
-   [<span data-ttu-id="f834f-257">Codecapi \_ avenccommonbuffersize</span><span class="sxs-lookup"><span data-stu-id="f834f-257">CODECAPI\_AVEncCommonBufferSize</span></span>](../directshow/avenccommonbuffersize-property.md)
-   [<span data-ttu-id="f834f-258">Codecapi \_ avencmpvgopsize</span><span class="sxs-lookup"><span data-stu-id="f834f-258">CODECAPI\_AVEncMPVGOPSize</span></span>](../directshow/avencmpvgopsize-property.md)
-   [<span data-ttu-id="f834f-259">Codecapi \_ avencvideoencodeqp</span><span class="sxs-lookup"><span data-stu-id="f834f-259">CODECAPI\_AVEncVideoEncodeQP</span></span>](codecapi-avencvideoencodeqp.md)
-   [<span data-ttu-id="f834f-260">Codecapi \_ avencvideoforcekeyframe</span><span class="sxs-lookup"><span data-stu-id="f834f-260">CODECAPI\_AVEncVideoForceKeyFrame</span></span>](codecapi-avencvideoforcekeyframe.md)

## <a name="requirements"></a><span data-ttu-id="f834f-261">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f834f-261">Requirements</span></span>



| <span data-ttu-id="f834f-262">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f834f-262">Requirement</span></span> | <span data-ttu-id="f834f-263">Wert</span><span class="sxs-lookup"><span data-stu-id="f834f-263">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f834f-264">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f834f-264">Minimum supported client</span></span><br/> | <span data-ttu-id="f834f-265">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f834f-265">Windows 10 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="f834f-266">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f834f-266">Minimum supported server</span></span><br/> | <span data-ttu-id="f834f-267">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f834f-267">None supported</span></span><br/>                                                                |
| <span data-ttu-id="f834f-268">DLL</span><span class="sxs-lookup"><span data-stu-id="f834f-268">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f834f-269"><dt>Mfh265enc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f834f-269"><dt>Mfh265enc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f834f-270">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f834f-270">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f834f-271">Codec-Objekte</span><span class="sxs-lookup"><span data-stu-id="f834f-271">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
