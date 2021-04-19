---
description: Der Windows Media Video 7/8-Encoder implementiert frühere Versionen des Windows Media Video Encoders.
ms.assetid: c4165614-b9ec-4216-b36c-f57bc05e3a8e
title: Windows Media Video 7/8-Encoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be5467d02681ef319a508f6f6581e1f3c0191950
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359799"
---
# <a name="windows-media-video-78-encoder"></a><span data-ttu-id="1d5d2-103">Windows Media Video 7/8-Encoder</span><span class="sxs-lookup"><span data-stu-id="1d5d2-103">Windows Media Video 7/8 Encoder</span></span>

<span data-ttu-id="1d5d2-104">Der Windows Media Video 7/8-Encoder implementiert frühere Versionen des Windows Media Video Encoders.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-104">The Windows Media Video 7/8 encoder implements previous versions of the Windows Media Video encoder.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="1d5d2-105">Klassen Bezeichner</span><span class="sxs-lookup"><span data-stu-id="1d5d2-105">Class Identifier</span></span>

<span data-ttu-id="1d5d2-106">Der Klassen Bezeichner (CLSID) für den Windows Media Video 7/8-Encoder ist **CLSID \_ cwmvxencmediaobject**.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-106">The class identifier (CLSID) for the Windows Media Video 7/8 encoder is **CLSID\_CWMVXEncMediaObject**.</span></span> <span data-ttu-id="1d5d2-107">Sie können eine Instanz des Encoders erstellen, indem Sie **CoCreateInstance** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-107">You can create an instance of the encoder by calling **CoCreateInstance**.</span></span>

## <a name="interfaces"></a><span data-ttu-id="1d5d2-108">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="1d5d2-108">Interfaces</span></span>

<span data-ttu-id="1d5d2-109">Ein Video Encoder-Objekt macht die [**imediaobject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) -Schnittstelle verfügbar, sodass das Objekt als DirectX-Medienobjekt (DMO) verwendet werden kann, und stellt die [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle zur Verfügung, sodass das Objekt als Media Foundation Transformation (MFT) verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-109">A video encoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="1d5d2-110">Ein Video Encoder verhält sich als DMO oder MFT, je nachdem, welche Schnittstellen Sie erhalten und welche Version von Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-110">A video encoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="1d5d2-111">In der folgenden Tabelle sind die Bedingungen aufgeführt, unter denen sich ein Video Encoder als DMO oder MFT verhält.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-111">The following table shows the conditions under which a video encoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="1d5d2-112">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="1d5d2-112">Operating system</span></span>            | <span data-ttu-id="1d5d2-113">Codierungs Verhalten</span><span class="sxs-lookup"><span data-stu-id="1d5d2-113">Encoder behavior</span></span>                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d5d2-114">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1d5d2-114">Windows XP</span></span>                  | <span data-ttu-id="1d5d2-115">Ein Windows Media-Video Encoder verhält sich immer als DMO.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-115">A Windows Media video encoder always behaves as a DMO.</span></span>                                                                                                                |
| <span data-ttu-id="1d5d2-116">Windows Vista und Windows 7</span><span class="sxs-lookup"><span data-stu-id="1d5d2-116">Windows Vista and Windows 7</span></span> | <span data-ttu-id="1d5d2-117">Standardmäßig verhält sich ein Windows Media-Video Encoder als DMO.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-117">By default, a Windows Media video encoder behaves as a DMO.</span></span> <span data-ttu-id="1d5d2-118">Wenn Sie eine [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle für einen Video Encoder erhalten, verhält sie sich wie eine MFT.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-118">If you obtain an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on a video encoder, it behaves as an MFT.</span></span> |



 

## <a name="input-formats"></a><span data-ttu-id="1d5d2-119">Eingabeformate</span><span class="sxs-lookup"><span data-stu-id="1d5d2-119">Input Formats</span></span>

<span data-ttu-id="1d5d2-120">Der Windows Media Video Encoder unterstützt die folgenden Eingabemedien-Untertypen, wenn er als DMO fungiert.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-120">The Windows Media Video encoder supports the following input media subtypes when it is acting as a DMO.</span></span>

-   <span data-ttu-id="1d5d2-121">mediasubtype \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="1d5d2-121">MEDIASUBTYPE\_IYUV</span></span>
-   <span data-ttu-id="1d5d2-122">Mediasubtype \_ I420</span><span class="sxs-lookup"><span data-stu-id="1d5d2-122">MEDIASUBTYPE\_I420</span></span>
-   <span data-ttu-id="1d5d2-123">Mediasubtype \_ YV12</span><span class="sxs-lookup"><span data-stu-id="1d5d2-123">MEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="1d5d2-124">Mediasubtype \_ NV11</span><span class="sxs-lookup"><span data-stu-id="1d5d2-124">MEDIASUBTYPE\_NV11</span></span>
-   <span data-ttu-id="1d5d2-125">Mediasubtype \_ NV12</span><span class="sxs-lookup"><span data-stu-id="1d5d2-125">MEDIASUBTYPE\_NV12</span></span>
-   <span data-ttu-id="1d5d2-126">Mediasubtype \_ im YUY2</span><span class="sxs-lookup"><span data-stu-id="1d5d2-126">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="1d5d2-127">mediasubtype \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="1d5d2-127">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="1d5d2-128">mediasubtype \_ yvyu</span><span class="sxs-lookup"><span data-stu-id="1d5d2-128">MEDIASUBTYPE\_YVYU</span></span>
-   <span data-ttu-id="1d5d2-129">Mediasubtype \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="1d5d2-129">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="1d5d2-130">Mediasubtype \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="1d5d2-130">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="1d5d2-131">Mediasubtype \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="1d5d2-131">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="1d5d2-132">Mediasubtype \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="1d5d2-132">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="1d5d2-133">Mediasubtype \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="1d5d2-133">MEDIASUBTYPE\_RGB8</span></span>
-   <span data-ttu-id="1d5d2-134">mediasubtype- \_ Foto</span><span class="sxs-lookup"><span data-stu-id="1d5d2-134">MEDIASUBTYPE\_PHOTOMOTION</span></span>

<span data-ttu-id="1d5d2-135">Der Windows Media Video Encoder unterstützt die folgenden Eingabemedien-Untertypen, wenn er als MFT fungiert.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-135">The Windows Media Video encoder supports the following input media subtypes when it is acting as an MFT.</span></span>

-   <span data-ttu-id="1d5d2-136">MF-Format ( \_ IYUV)</span><span class="sxs-lookup"><span data-stu-id="1d5d2-136">MFVideoFormat\_IYUV</span></span>
-   <span data-ttu-id="1d5d2-137">MF-Format \_ I420</span><span class="sxs-lookup"><span data-stu-id="1d5d2-137">MFVideoFormat\_I420</span></span>
-   <span data-ttu-id="1d5d2-138">MF-Format \_ YV12</span><span class="sxs-lookup"><span data-stu-id="1d5d2-138">MFVideoFormat\_YV12</span></span>
-   <span data-ttu-id="1d5d2-139">MF-Format \_ NV11</span><span class="sxs-lookup"><span data-stu-id="1d5d2-139">MFVideoFormat\_NV11</span></span>
-   <span data-ttu-id="1d5d2-140">MF-Format \_ NV12</span><span class="sxs-lookup"><span data-stu-id="1d5d2-140">MFVideoFormat\_NV12</span></span>
-   <span data-ttu-id="1d5d2-141">MF-Format \_ im YUY2</span><span class="sxs-lookup"><span data-stu-id="1d5d2-141">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="1d5d2-142">MF-Format ( \_ UYVY)</span><span class="sxs-lookup"><span data-stu-id="1d5d2-142">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="1d5d2-143">Mfvideoformat \_ yvyu</span><span class="sxs-lookup"><span data-stu-id="1d5d2-143">MFVideoFormat\_YVYU</span></span>
-   <span data-ttu-id="1d5d2-144">MF-Format \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="1d5d2-144">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="1d5d2-145">MF-Format \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="1d5d2-145">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="1d5d2-146">MF-Format \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="1d5d2-146">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="1d5d2-147">MF-Format \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="1d5d2-147">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="1d5d2-148">MF-Format \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="1d5d2-148">MFVideoFormat\_RGB8</span></span>
-   <span data-ttu-id="1d5d2-149">mediasubtype- \_ Foto</span><span class="sxs-lookup"><span data-stu-id="1d5d2-149">MEDIASUBTYPE\_PHOTOMOTION</span></span>

## <a name="output-formats"></a><span data-ttu-id="1d5d2-150">Ausgabeformate</span><span class="sxs-lookup"><span data-stu-id="1d5d2-150">Output Formats</span></span>

<span data-ttu-id="1d5d2-151">In der folgenden Tabelle sind die vier Zeichen Codes (fourccs) für die vom Windows Media Video 7/8-Encoder unterstützten Ausgabetypen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-151">The following table shows the four-character codes (FOURCCs) for the output types supported by the Windows Media Video 7/8 encoder.</span></span>



| <span data-ttu-id="1d5d2-152">Category</span><span class="sxs-lookup"><span data-stu-id="1d5d2-152">Category</span></span>              | <span data-ttu-id="1d5d2-153">FOURCC</span><span class="sxs-lookup"><span data-stu-id="1d5d2-153">FOURCC</span></span> |
|-----------------------|--------|
| <span data-ttu-id="1d5d2-154">Windows Media Video 7</span><span class="sxs-lookup"><span data-stu-id="1d5d2-154">Windows Media Video 7</span></span> | <span data-ttu-id="1d5d2-155">"WMV1"</span><span class="sxs-lookup"><span data-stu-id="1d5d2-155">"WMV1"</span></span> |
| <span data-ttu-id="1d5d2-156">Windows Media Video 8</span><span class="sxs-lookup"><span data-stu-id="1d5d2-156">Windows Media Video 8</span></span> | <span data-ttu-id="1d5d2-157">"WMV2"</span><span class="sxs-lookup"><span data-stu-id="1d5d2-157">"WMV2"</span></span> |



 

## <a name="properties"></a><span data-ttu-id="1d5d2-158">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1d5d2-158">Properties</span></span>

<span data-ttu-id="1d5d2-159">Der Windows Media Video 7/8-Encoder unterstützt die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-159">The Windows Media Video 7/8 encoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1d5d2-160">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1d5d2-160">Property</span></span></th>
<th><span data-ttu-id="1d5d2-161">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1d5d2-161">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1d5d2-162"><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d5d2-162"><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></span></span></td>
<td><span data-ttu-id="1d5d2-163">Gibt den Aufwand in Bytes pro Paket an, der für den Container erforderlich ist, der zum Speichern der komprimierten Inhalte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-163">Specifies the overhead, in bytes per packet, required for the container used to store the compressed content.</span></span><br/> <dl> <span data-ttu-id="1d5d2-164">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-164">Windows XP and later.</span></span><br />
<span data-ttu-id="1d5d2-165">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-165">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1d5d2-166"><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d5d2-166"><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></span></span></td>
<td><span data-ttu-id="1d5d2-167">Gibt die durchschnittliche Frame Rate von Videoinhalten in Frames pro Sekunde an.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-167">Specifies the average frame rate of video content, in frames per second.</span></span><br/> <dl> <span data-ttu-id="1d5d2-168">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-168">Windows XP and later.</span></span><br />
<span data-ttu-id="1d5d2-169">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-169">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1d5d2-170"><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d5d2-170"><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></span></span></td>
<td><span data-ttu-id="1d5d2-171">Gibt das Puffer Fenster eines eingeschränkten VBR (Variable-Bit-Rate)-Streams mit der durchschnittlichen Bitrate (angegeben durch <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>) in Millisekunden an.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-171">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its average bit rate (specified by <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>).</span></span><br/> <dl> <span data-ttu-id="1d5d2-172">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-172">Windows XP and later.</span></span><br />
<span data-ttu-id="1d5d2-173">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-173">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1d5d2-174"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d5d2-174"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span></span></td>
<td><span data-ttu-id="1d5d2-175">Gibt das Puffer Fenster eines eingeschränkten VBR (Variable-Bit-Rate)-Streams mit der maximalen Bitrate (angegeben durch <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>) in Millisekunden an.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-175">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its peak bit rate (specified by <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>).</span></span><br/> <dl> <span data-ttu-id="1d5d2-176">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-176">Windows XP and later.</span></span><br />
<span data-ttu-id="1d5d2-177">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-177">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1d5d2-178"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d5d2-178"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></span></span></td>
<td><span data-ttu-id="1d5d2-179">Gibt an, ob der codierte videobit-Stream einen Puffer Füllwert mit jedem Keyframe enthält.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-179">Specifies whether the encoded video bit stream contains a buffer fullness value with every key frame.</span></span><br/> <dl> <span data-ttu-id="1d5d2-180">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-180">Windows XP and later.</span></span><br />
<span data-ttu-id="1d5d2-181">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-181">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1d5d2-182"><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d5d2-182"><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="1d5d2-183">Gibt die Anzahl der vom Codec codierten Videorahmen an.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-183">Specifies the number of video frames encoded by the codec.</span></span><br/> <dl> <span data-ttu-id="1d5d2-184">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-184">Windows XP and later.</span></span><br />
<span data-ttu-id="1d5d2-185">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-185">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1d5d2-186"><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d5d2-186"><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="1d5d2-187">Gibt die Anzahl der durch den Codec codierten Video Frames an, die tatsächlich Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-187">Specifies the number of video frames encoded by the codec that actually contain data.</span></span><br/> <dl> <span data-ttu-id="1d5d2-188">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-188">Windows XP and later.</span></span><br />
<span data-ttu-id="1d5d2-189">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-189">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1d5d2-190"><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d5d2-190"><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></span></span></td>
<td><span data-ttu-id="1d5d2-191">Diese Eigenschaft wird durch <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>abgelöst.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-191">This property is superseded by <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1d5d2-192"><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d5d2-192"><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></span></span></td>
<td><span data-ttu-id="1d5d2-193">Gibt die Komplexität des Encoder-Algorithmus an.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-193">Specifies the complexity of the encoder algorithm.</span></span><br/> <dl> <span data-ttu-id="1d5d2-194">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-194">Windows Vista and later.</span></span><br />
<span data-ttu-id="1d5d2-195">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-195">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1d5d2-196"><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d5d2-196"><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></span></span></td>
<td><span data-ttu-id="1d5d2-197">Gibt eine numerische Darstellung der Kompromisse zwischen Bewegungs Glätte und Bildqualität in der Codec-Ausgabe an.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-197">Specifies a numeric representation of the tradeoff between motion smoothness and image quality in codec output.</span></span><br/> <dl> <span data-ttu-id="1d5d2-198">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-198">Windows XP and later.</span></span><br />
<span data-ttu-id="1d5d2-199">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-199">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1d5d2-200"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d5d2-200"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span></span></td>
<td><span data-ttu-id="1d5d2-201">Gibt die Geräte Konformitäts Vorlage an, der der codierte Inhalt entspricht.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-201">Specifies the device conformance template to which the encoded content conforms.</span></span><br/> <dl> <span data-ttu-id="1d5d2-202">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-202">Windows XP and later.</span></span><br />
<span data-ttu-id="1d5d2-203">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-203">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1d5d2-204"><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d5d2-204"><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></span></span></td>
<td><span data-ttu-id="1d5d2-205">Gibt die Konformitäts Vorlage für Geräte an, die Sie für die Videocodierung verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-205">Specifies the device conformance template that you want to use for video encoding.</span></span><br/> <dl> <span data-ttu-id="1d5d2-206">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-206">Windows XP and later.</span></span><br />
<span data-ttu-id="1d5d2-207">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-207">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1d5d2-208"><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d5d2-208"><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="1d5d2-209">Gibt die Anzahl der während der Codierung gelöschten Videorahmen an.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-209">Specifies the number of video frames dropped during encoding.</span></span><br/> <dl> <span data-ttu-id="1d5d2-210">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-210">Windows XP and later.</span></span><br />
<span data-ttu-id="1d5d2-211">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-211">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1d5d2-212"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d5d2-212"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span></span></td>
<td><span data-ttu-id="1d5d2-213">Gibt das Ende eines Codierungs Durchlaufs an.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-213">Specifies the end of an encoding pass.</span></span><br/> <dl> <span data-ttu-id="1d5d2-214">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-214">Windows XP and later.</span></span><br />
<span data-ttu-id="1d5d2-215">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-215">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1d5d2-216"><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d5d2-216"><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></span></span></td>
<td><span data-ttu-id="1d5d2-217">Gibt den FourCC-Wert an, der den Encoder identifiziert, den Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-217">Specifies the FOURCC that identifies the encoder you want to use.</span></span><br/> <dl> <span data-ttu-id="1d5d2-218">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-218">Windows XP and later.</span></span><br />
<span data-ttu-id="1d5d2-219">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-219">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1d5d2-220"><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d5d2-220"><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></span></span></td>
<td><span data-ttu-id="1d5d2-221">Gibt an, ob die Codec-Ausgabe mit Zeilen Sprung dargestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-221">Specifies whether the codec output will be interlaced.</span></span><br/> <dl> <span data-ttu-id="1d5d2-222">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-222">Windows XP and later.</span></span><br />
<span data-ttu-id="1d5d2-223">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-223">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1d5d2-224"><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d5d2-224"><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></span></span></td>
<td><span data-ttu-id="1d5d2-225">Gibt die maximale Zeit (in Millisekunden) zwischen Keyframes in der Codec-Ausgabe an.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-225">Specifies the maximum time, in milliseconds, between key frames in the codec output.</span></span><br/> <dl> <span data-ttu-id="1d5d2-226">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-226">Windows XP and later.</span></span><br />
<span data-ttu-id="1d5d2-227">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-227">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1d5d2-228"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d5d2-228"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span></span></td>
<td><span data-ttu-id="1d5d2-229">Gibt die maximale Anzahl von durch den Codec unterstützten Durchläufen an.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-229">Specifies the maximum number of passes supported by the codec.</span></span><br/> <dl> <span data-ttu-id="1d5d2-230">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-230">Windows XP and later.</span></span><br />
<span data-ttu-id="1d5d2-231">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-231">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1d5d2-232"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d5d2-232"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span></span></td>
<td><span data-ttu-id="1d5d2-233">Gibt die Anzahl von Durchläufen an, die vom Codec zum Codieren des Inhalts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-233">Specifies the number of passes that the codec will use to encode the content.</span></span><br/> <dl> <span data-ttu-id="1d5d2-234">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-234">Windows XP and later.</span></span><br />
<span data-ttu-id="1d5d2-235">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-235">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1d5d2-236"><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d5d2-236"><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="1d5d2-237">Gibt an, ob der Encoder für doppelte Frames Dummy-Frame-Einträge im Bitdaten Strom erzeugt.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-237">Specifies whether the encoder produces dummy frame entries in the bit stream for duplicate frames.</span></span><br/> <dl> <span data-ttu-id="1d5d2-238">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-238">Windows XP and later.</span></span><br />
<span data-ttu-id="1d5d2-239">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-239">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1d5d2-240"><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d5d2-240"><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></span></span></td>
<td><span data-ttu-id="1d5d2-241">Gibt QP an.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-241">Specifies QP.</span></span><br/> <dl> <span data-ttu-id="1d5d2-242">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-242">Windows Vista and later.</span></span><br />
<span data-ttu-id="1d5d2-243">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-243">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1d5d2-244"><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d5d2-244"><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></span></span></td>
<td><span data-ttu-id="1d5d2-245">Gibt die durchschnittliche Bitrate in Bits pro Sekunde an, die für die 2-Pass-VBR-Codierung (Variable Bitrate) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-245">Specifies the average bit rate, in bits per second, used for 2-pass variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="1d5d2-246">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-246">Windows XP and later.</span></span><br />
<span data-ttu-id="1d5d2-247">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-247">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1d5d2-248"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d5d2-248"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span></span></td>
<td><span data-ttu-id="1d5d2-249">Gibt die Spitzen Bitrate in Bits pro Sekunde an, die für die eingeschränkte 2-Pass-Variable-Bitrate (VBR) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-249">Specifies the peak bit rate, in bits per second, used for constrained 2-pass variable-bit-rate (VBR).</span></span><br/> <dl> <span data-ttu-id="1d5d2-250">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-250">Windows XP and later.</span></span><br />
<span data-ttu-id="1d5d2-251">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-251">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1d5d2-252"><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d5d2-252"><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="1d5d2-253">Gibt die Anzahl der Videorahmen an, die während des Codierungs Vorgangs an den Encoder übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-253">Specifies the number of video frames passed to the encoder during the encoding process.</span></span><br/> <dl> <span data-ttu-id="1d5d2-254">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-254">Windows XP and later.</span></span><br />
<span data-ttu-id="1d5d2-255">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-255">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1d5d2-256"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d5d2-256"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span></span></td>
<td><span data-ttu-id="1d5d2-257">Gibt an, ob der Codec die VBR-Codierung (Variable-Bit-Rate) verwendet.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-257">Specifies whether the codec will use variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="1d5d2-258">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-258">Windows XP and later.</span></span><br />
<span data-ttu-id="1d5d2-259">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-259">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1d5d2-260"><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d5d2-260"><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="1d5d2-261">Gibt die tatsächliche Qualitätsstufe für die Qualitäts basierte (1-Pass-) VBR-Codierung (Variable-Bitrate) an.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-261">Specifies the actual quality level for quality based (1-pass) variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="1d5d2-262">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-262">Windows XP and later.</span></span><br />
<span data-ttu-id="1d5d2-263">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-263">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1d5d2-264"><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d5d2-264"><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></span></span></td>
<td><span data-ttu-id="1d5d2-265">Gibt den Umfang des Inhalts in Millisekunden an, der in den Modell Puffer passen kann.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-265">Specifies the amount of content, in milliseconds, that can fit into the model buffer.</span></span><br/> <dl> <span data-ttu-id="1d5d2-266">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-266">Windows XP and later.</span></span><br />
<span data-ttu-id="1d5d2-267">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-267">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1d5d2-268"><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d5d2-268"><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="1d5d2-269">Gibt die Anzahl der Videorahmen an, die übersprungen wurden, weil Sie Duplikate vorheriger Frames waren.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-269">Specifies the number of video frames that were skipped because they were duplicates of previous frames.</span></span><br/> <dl> <span data-ttu-id="1d5d2-270">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="1d5d2-270">Windows XP and later.</span></span><br />
<span data-ttu-id="1d5d2-271">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1d5d2-271">Read-only</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="1d5d2-272">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d5d2-272">Requirements</span></span>



| <span data-ttu-id="1d5d2-273">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d5d2-273">Requirement</span></span> | <span data-ttu-id="1d5d2-274">Wert</span><span class="sxs-lookup"><span data-stu-id="1d5d2-274">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d5d2-275">Client</span><span class="sxs-lookup"><span data-stu-id="1d5d2-275">Client</span></span><br/> | <span data-ttu-id="1d5d2-276">Windows XP, Windows Vista oder Windows 7</span><span class="sxs-lookup"><span data-stu-id="1d5d2-276">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="1d5d2-277">Header</span><span class="sxs-lookup"><span data-stu-id="1d5d2-277">Header</span></span><br/> | <dl> <span data-ttu-id="1d5d2-278"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d5d2-278"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="1d5d2-279">DLL</span><span class="sxs-lookup"><span data-stu-id="1d5d2-279">DLL</span></span><br/>    | <dl> <span data-ttu-id="1d5d2-280"><dt>Wmvxencd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d5d2-280"><dt>Wmvxencd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d5d2-281">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d5d2-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d5d2-282">Codec-Objekte</span><span class="sxs-lookup"><span data-stu-id="1d5d2-282">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="1d5d2-283">Codec-Implementierung</span><span class="sxs-lookup"><span data-stu-id="1d5d2-283">Codec Implementation</span></span>](codecimplementation.md)
</dt> <dt>

[<span data-ttu-id="1d5d2-284">Video Untertyp-GUIDs</span><span class="sxs-lookup"><span data-stu-id="1d5d2-284">Video Subtype GUIDs</span></span>](video-subtype-guids.md)
</dt> </dl>

 

 
