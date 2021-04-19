---
description: Der Windows Media Video 9-Encoder codiert Videostreams.
ms.assetid: 1d0a41bc-7f7c-4e25-860c-1108ab292951
title: Windows Media Video 9-Encoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c36ee5823c585d60ee74e75f99e8ec9b4d91f5cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370756"
---
# <a name="windows-media-video-9-encoder"></a><span data-ttu-id="a789b-103">Windows Media Video 9-Encoder</span><span class="sxs-lookup"><span data-stu-id="a789b-103">Windows Media Video 9 Encoder</span></span>

<span data-ttu-id="a789b-104">Der Windows Media Video 9-Encoder codiert Videostreams.</span><span class="sxs-lookup"><span data-stu-id="a789b-104">The Windows Media Video 9 encoder encodes video streams.</span></span> <span data-ttu-id="a789b-105">Der Encoder unterstützt die folgenden vier Kategorien codierter Ausgaben.</span><span class="sxs-lookup"><span data-stu-id="a789b-105">The encoder supports the following four categories of encoded output.</span></span>

-   <span data-ttu-id="a789b-106">Windows Media Video 9 einfaches Profil</span><span class="sxs-lookup"><span data-stu-id="a789b-106">Windows Media Video 9 Simple Profile</span></span>
-   <span data-ttu-id="a789b-107">Windows Media Video 9 Hauptprofil</span><span class="sxs-lookup"><span data-stu-id="a789b-107">Windows Media Video 9 Main Profile</span></span>
-   <span data-ttu-id="a789b-108">Erweiterte profile Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="a789b-108">Windows Media Video 9 Advanced Profile</span></span>
-   <span data-ttu-id="a789b-109">Windows Media Video 9,1-Image</span><span class="sxs-lookup"><span data-stu-id="a789b-109">Windows Media Video 9.1 Image</span></span>

## <a name="class-identifier"></a><span data-ttu-id="a789b-110">Klassen Bezeichner</span><span class="sxs-lookup"><span data-stu-id="a789b-110">Class Identifier</span></span>

<span data-ttu-id="a789b-111">Der Klassen Bezeichner (CLSID) für den Windows Media Video Encoder wird durch die Konstante **CLSID \_ CWMV9EncMediaObject** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a789b-111">The class identifier (CLSID) for the Windows Media Video encoder is represented by the constant **CLSID\_CWMV9EncMediaObject**.</span></span> <span data-ttu-id="a789b-112">Sie können eine Instanz des Video Encoders erstellen, indem Sie **CoCreateInstance** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a789b-112">You can create an instance of the video encoder by calling **CoCreateInstance**.</span></span>

## <a name="interfaces"></a><span data-ttu-id="a789b-113">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="a789b-113">Interfaces</span></span>

<span data-ttu-id="a789b-114">Ein Video Encoder-Objekt macht die [**imediaobject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) -Schnittstelle verfügbar, sodass das Objekt als DirectX-Medienobjekt (DMO) verwendet werden kann, und stellt die [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle zur Verfügung, sodass das Objekt als Media Foundation Transformation (MFT) verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a789b-114">A video encoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="a789b-115">Ein Video Encoder verhält sich als DMO oder MFT, je nachdem, welche Schnittstellen Sie erhalten und welche Version von Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a789b-115">A video encoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="a789b-116">In der folgenden Tabelle sind die Bedingungen aufgeführt, unter denen sich ein Video Encoder als DMO oder MFT verhält.</span><span class="sxs-lookup"><span data-stu-id="a789b-116">The following table shows the conditions under which a video encoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="a789b-117">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="a789b-117">Operating system</span></span>            | <span data-ttu-id="a789b-118">Codierungs Verhalten</span><span class="sxs-lookup"><span data-stu-id="a789b-118">Encoder behavior</span></span>                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a789b-119">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a789b-119">Windows XP</span></span>                  | <span data-ttu-id="a789b-120">Ein Windows Media-Video Encoder verhält sich immer als DMO.</span><span class="sxs-lookup"><span data-stu-id="a789b-120">A Windows Media video encoder always behaves as a DMO.</span></span>                                                                                                                |
| <span data-ttu-id="a789b-121">Windows Vista und Windows 7</span><span class="sxs-lookup"><span data-stu-id="a789b-121">Windows Vista and Windows 7</span></span> | <span data-ttu-id="a789b-122">Standardmäßig verhält sich ein Windows Media-Video Encoder als DMO.</span><span class="sxs-lookup"><span data-stu-id="a789b-122">By default, a Windows Media video encoder behaves as a DMO.</span></span> <span data-ttu-id="a789b-123">Wenn Sie eine [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle für einen Video Encoder erhalten, verhält sie sich wie eine MFT.</span><span class="sxs-lookup"><span data-stu-id="a789b-123">If you obtain an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on a video encoder, it behaves as an MFT.</span></span> |



 

## <a name="input-formats"></a><span data-ttu-id="a789b-124">Eingabeformate</span><span class="sxs-lookup"><span data-stu-id="a789b-124">Input Formats</span></span>

<span data-ttu-id="a789b-125">Der Windows Media Video Encoder unterstützt die folgenden Eingabemedien-Untertypen, wenn er als DMO fungiert.</span><span class="sxs-lookup"><span data-stu-id="a789b-125">The Windows Media Video encoder supports the following input media subtypes when it is acting as a DMO.</span></span>

-   <span data-ttu-id="a789b-126">mediasubtype \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="a789b-126">MEDIASUBTYPE\_IYUV</span></span>
-   <span data-ttu-id="a789b-127">Mediasubtype \_ I420</span><span class="sxs-lookup"><span data-stu-id="a789b-127">MEDIASUBTYPE\_I420</span></span>
-   <span data-ttu-id="a789b-128">Mediasubtype \_ YV12</span><span class="sxs-lookup"><span data-stu-id="a789b-128">MEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="a789b-129">Mediasubtype \_ NV11</span><span class="sxs-lookup"><span data-stu-id="a789b-129">MEDIASUBTYPE\_NV11</span></span>
-   <span data-ttu-id="a789b-130">Mediasubtype \_ NV12</span><span class="sxs-lookup"><span data-stu-id="a789b-130">MEDIASUBTYPE\_NV12</span></span>
-   <span data-ttu-id="a789b-131">Mediasubtype \_ im YUY2</span><span class="sxs-lookup"><span data-stu-id="a789b-131">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="a789b-132">mediasubtype \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="a789b-132">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="a789b-133">mediasubtype \_ yvyu</span><span class="sxs-lookup"><span data-stu-id="a789b-133">MEDIASUBTYPE\_YVYU</span></span>
-   <span data-ttu-id="a789b-134">Mediasubtype \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="a789b-134">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="a789b-135">Mediasubtype \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="a789b-135">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="a789b-136">Mediasubtype \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="a789b-136">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="a789b-137">Mediasubtype \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="a789b-137">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="a789b-138">Mediasubtype \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="a789b-138">MEDIASUBTYPE\_RGB8</span></span>
-   <span data-ttu-id="a789b-139">mediasubtype- \_ Foto</span><span class="sxs-lookup"><span data-stu-id="a789b-139">MEDIASUBTYPE\_PHOTOMOTION</span></span>

<span data-ttu-id="a789b-140">Der Windows Media Video Encoder unterstützt die folgenden Eingabemedien-Untertypen, wenn er als MFT fungiert.</span><span class="sxs-lookup"><span data-stu-id="a789b-140">The Windows Media Video encoder supports the following input media subtypes when it is acting as an MFT.</span></span>

-   <span data-ttu-id="a789b-141">MF-Format ( \_ IYUV)</span><span class="sxs-lookup"><span data-stu-id="a789b-141">MFVideoFormat\_IYUV</span></span>
-   <span data-ttu-id="a789b-142">MF-Format \_ I420</span><span class="sxs-lookup"><span data-stu-id="a789b-142">MFVideoFormat\_I420</span></span>
-   <span data-ttu-id="a789b-143">MF-Format \_ YV12</span><span class="sxs-lookup"><span data-stu-id="a789b-143">MFVideoFormat\_YV12</span></span>
-   <span data-ttu-id="a789b-144">MF-Format \_ NV11</span><span class="sxs-lookup"><span data-stu-id="a789b-144">MFVideoFormat\_NV11</span></span>
-   <span data-ttu-id="a789b-145">MF-Format \_ NV12</span><span class="sxs-lookup"><span data-stu-id="a789b-145">MFVideoFormat\_NV12</span></span>
-   <span data-ttu-id="a789b-146">MF-Format \_ im YUY2</span><span class="sxs-lookup"><span data-stu-id="a789b-146">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="a789b-147">MF-Format ( \_ UYVY)</span><span class="sxs-lookup"><span data-stu-id="a789b-147">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="a789b-148">Mfvideoformat \_ yvyu</span><span class="sxs-lookup"><span data-stu-id="a789b-148">MFVideoFormat\_YVYU</span></span>
-   <span data-ttu-id="a789b-149">MF-Format \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="a789b-149">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="a789b-150">MF-Format \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="a789b-150">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="a789b-151">MF-Format \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="a789b-151">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="a789b-152">MF-Format \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="a789b-152">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="a789b-153">MF-Format \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="a789b-153">MFVideoFormat\_RGB8</span></span>
-   <span data-ttu-id="a789b-154">mediasubtype- \_ Foto</span><span class="sxs-lookup"><span data-stu-id="a789b-154">MEDIASUBTYPE\_PHOTOMOTION</span></span>

## <a name="output-formats"></a><span data-ttu-id="a789b-155">Ausgabeformate</span><span class="sxs-lookup"><span data-stu-id="a789b-155">Output Formats</span></span>

<span data-ttu-id="a789b-156">In der folgenden Tabelle werden die vier Zeichen Codes (fourccs) angezeigt, die den Kategorien der codierten Ausgabe entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a789b-156">The following table shows the four-character codes (FOURCCs) that correspond to the categories of encoded output.</span></span>



| <span data-ttu-id="a789b-157">Category</span><span class="sxs-lookup"><span data-stu-id="a789b-157">Category</span></span>                               | <span data-ttu-id="a789b-158">FOURCC</span><span class="sxs-lookup"><span data-stu-id="a789b-158">FOURCC</span></span>                                   |
|----------------------------------------|------------------------------------------|
| <span data-ttu-id="a789b-159">Windows Media Video 9 einfaches Profil</span><span class="sxs-lookup"><span data-stu-id="a789b-159">Windows Media Video 9 Simple Profile</span></span>   | <span data-ttu-id="a789b-160">"WMV3"</span><span class="sxs-lookup"><span data-stu-id="a789b-160">"WMV3"</span></span>                                   |
| <span data-ttu-id="a789b-161">Windows Media Video 9 Hauptprofil</span><span class="sxs-lookup"><span data-stu-id="a789b-161">Windows Media Video 9 Main Profile</span></span>     | <span data-ttu-id="a789b-162">"WMV3"</span><span class="sxs-lookup"><span data-stu-id="a789b-162">"WMV3"</span></span>                                   |
| <span data-ttu-id="a789b-163">Erweiterte profile Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="a789b-163">Windows Media Video 9 Advanced Profile</span></span> | <span data-ttu-id="a789b-164">"WVC1"</span><span class="sxs-lookup"><span data-stu-id="a789b-164">"WVC1"</span></span>                                   |
| <span data-ttu-id="a789b-165">Windows Media Video 9,1-Image</span><span class="sxs-lookup"><span data-stu-id="a789b-165">Windows Media Video 9.1 Image</span></span>          | <span data-ttu-id="a789b-166">"Wmvp" für 9,1, "WVP2" für 9,1 Version 2</span><span class="sxs-lookup"><span data-stu-id="a789b-166">"WMVP" for 9.1, "WVP2" for 9.1 version 2</span></span> |



 

<span data-ttu-id="a789b-167">Um zwischen einfachem Profil und Hauptprofil zu unterscheiden, legen Sie die Eigenschaft [**mfpkey \_ decodercomplexityangeforderten**](mfpkey-decodercomplexityrequestedproperty.md) fest.</span><span class="sxs-lookup"><span data-stu-id="a789b-167">To distinguish between Simple Profile and Main Profile, set the [**MFPKEY\_DECODERCOMPLEXITYREQUESTED**](mfpkey-decodercomplexityrequestedproperty.md) property.</span></span>

## <a name="properties"></a><span data-ttu-id="a789b-168">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a789b-168">Properties</span></span>

<span data-ttu-id="a789b-169">Der Windows Media Video 9-Encoder unterstützt die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a789b-169">The Windows Media Video 9 encoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a789b-170">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a789b-170">Property</span></span></th>
<th><span data-ttu-id="a789b-171">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a789b-171">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a789b-172"><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-172"><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></span></span></td>
<td><span data-ttu-id="a789b-173">Gibt den Aufwand in Bytes pro Paket an, der für den Container erforderlich ist, der zum Speichern der komprimierten Inhalte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a789b-173">Specifies the overhead, in bytes per packet, required for the container used to store the compressed content.</span></span><br/> <dl> <span data-ttu-id="a789b-174">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-174">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-175">Einfaches Profil, Hauptprofil, erweitertes Profil, Image.</span><span class="sxs-lookup"><span data-stu-id="a789b-175">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="a789b-176">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-176">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a789b-177"><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-177"><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></span></span></td>
<td><span data-ttu-id="a789b-178">Gibt die durchschnittliche Frame Rate von Videoinhalten in Frames pro Sekunde an.</span><span class="sxs-lookup"><span data-stu-id="a789b-178">Specifies the average frame rate of video content, in frames per second.</span></span><br/> <dl> <span data-ttu-id="a789b-179">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-179">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-180">Einfaches Profil, Hauptprofil, erweitertes Profil, Image.</span><span class="sxs-lookup"><span data-stu-id="a789b-180">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="a789b-181">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a789b-181">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a789b-182"><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-182"><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></span></span></td>
<td><span data-ttu-id="a789b-183">Gibt das Puffer Fenster eines eingeschränkten VBR (Variable-Bit-Rate)-Streams mit der durchschnittlichen Bitrate (angegeben durch <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>) in Millisekunden an.</span><span class="sxs-lookup"><span data-stu-id="a789b-183">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its average bit rate (specified by <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>).</span></span><br/> <dl> <span data-ttu-id="a789b-184">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-184">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-185">Einfaches Profil, Hauptprofil, erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-185">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-186">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-186">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a789b-187"><a href="mfpkey-bdeltaqpproperty.md"><strong>MFPKEY_BDELTAQP</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-187"><a href="mfpkey-bdeltaqpproperty.md"><strong>MFPKEY_BDELTAQP</strong></a></span></span></td>
<td><span data-ttu-id="a789b-188">Gibt die Delta Vergrößerung zwischen dem Bild quantifizer des Anker Rahmens und dem Bild quantifizer des B-Frames an.</span><span class="sxs-lookup"><span data-stu-id="a789b-188">Specifies the delta increase between the picture quantizer of the anchor frame and the picture quantizer of the B-frame.</span></span><br/> <dl> <span data-ttu-id="a789b-189">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-189">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-190">Hauptprofil, erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-190">Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-191">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-191">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a789b-192"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-192"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span></span></td>
<td><span data-ttu-id="a789b-193">Gibt das Puffer Fenster eines eingeschränkten VBR (Variable-Bit-Rate)-Streams mit der maximalen Bitrate (angegeben durch <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>) in Millisekunden an.</span><span class="sxs-lookup"><span data-stu-id="a789b-193">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its peak bit rate (specified by <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>).</span></span><br/> <dl> <span data-ttu-id="a789b-194">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-194">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-195">Einfaches Profil, Hauptprofil, erweitertes Profil, Image.</span><span class="sxs-lookup"><span data-stu-id="a789b-195">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="a789b-196">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-196">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a789b-197"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-197"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></span></span></td>
<td><span data-ttu-id="a789b-198">Gibt an, ob der codierte videobit-Stream einen Puffer Füllwert mit jedem Keyframe enthält.</span><span class="sxs-lookup"><span data-stu-id="a789b-198">Specifies whether the encoded video bit stream contains a buffer fullness value with every key frame.</span></span><br/> <dl> <span data-ttu-id="a789b-199">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-199">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-200">Einfaches Profil, Hauptprofil, erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-200">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-201">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a789b-201">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a789b-202"><a href="mfpkey-closedentrypointproperty.md"><strong>MFPKEY_CLOSEDENTRYPOINT</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-202"><a href="mfpkey-closedentrypointproperty.md"><strong>MFPKEY_CLOSEDENTRYPOINT</strong></a></span></span></td>
<td><span data-ttu-id="a789b-203">Gibt das Codierungs Muster an, das am Anfang einer Gruppe von Bildern verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a789b-203">Specifies the encoding pattern to use at the beginning of a group of pictures.</span></span><br/> <dl> <span data-ttu-id="a789b-204">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-204">Windows Vista and later.</span></span><br />
<span data-ttu-id="a789b-205">Einfaches Profil, Hauptprofil, erweitertes Profil, Image.</span><span class="sxs-lookup"><span data-stu-id="a789b-205">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="a789b-206">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-206">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a789b-207"><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-207"><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="a789b-208">Gibt die Anzahl der vom Codec codierten Videorahmen an.</span><span class="sxs-lookup"><span data-stu-id="a789b-208">Specifies the number of video frames encoded by the codec.</span></span><br/> <dl> <span data-ttu-id="a789b-209">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-209">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-210">Einfaches Profil, Hauptprofil, erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-210">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-211">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a789b-211">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a789b-212"><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-212"><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="a789b-213">Gibt die Anzahl der durch den Codec codierten Video Frames an, die tatsächlich Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="a789b-213">Specifies the number of video frames encoded by the codec that actually contain data.</span></span><br/> <dl> <span data-ttu-id="a789b-214">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-214">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-215">Einfaches Profil, Hauptprofil, erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-215">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-216">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a789b-216">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a789b-217"><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-217"><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></span></span></td>
<td><span data-ttu-id="a789b-218">Diese Eigenschaft wird durch <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>abgelöst.</span><span class="sxs-lookup"><span data-stu-id="a789b-218">This property is superseded by <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a789b-219"><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-219"><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></span></span></td>
<td><span data-ttu-id="a789b-220">Gibt die Komplexität des Encoder-Algorithmus an.</span><span class="sxs-lookup"><span data-stu-id="a789b-220">Specifies the complexity of the encoder algorithm.</span></span><br/> <dl> <span data-ttu-id="a789b-221">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-221">Windows Vista and later.</span></span><br />
<span data-ttu-id="a789b-222">Einfaches Profil, Hauptprofil.</span><span class="sxs-lookup"><span data-stu-id="a789b-222">Simple Profile, Main Profile.</span></span> <span data-ttu-id="a789b-223">Erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-223">Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-224">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-224">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a789b-225"><a href="mfpkey-compressionoptimizationtypeproperty.md"><strong>MFPKEY_COMPRESSIONOPTIMIZATIONTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-225"><a href="mfpkey-compressionoptimizationtypeproperty.md"><strong>MFPKEY_COMPRESSIONOPTIMIZATIONTYPE</strong></a></span></span></td>
<td><span data-ttu-id="a789b-226">Gibt den Typ der Optimierung an, der für den erweiterten profilcodec von Windows Media Video 9 verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a789b-226">Specifies the type of optimization to use for the Windows Media Video 9 Advanced Profile codec.</span></span><br/> <dl> <span data-ttu-id="a789b-227">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-227">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-228">Einfaches Profil, Hauptprofil, erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-228">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-229">Schreiben.</span><span class="sxs-lookup"><span data-stu-id="a789b-229">Write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a789b-230"><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-230"><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></span></span></td>
<td><span data-ttu-id="a789b-231">Gibt eine numerische Darstellung der Kompromisse zwischen Bewegungs Glätte und Bildqualität in der Codec-Ausgabe an.</span><span class="sxs-lookup"><span data-stu-id="a789b-231">Specifies a numeric representation of the tradeoff between motion smoothness and image quality in codec output.</span></span><br/> <dl> <span data-ttu-id="a789b-232">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-232">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-233">Einfaches Profil, Hauptprofil, erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-233">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-234">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-234">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a789b-235"><a href="mfpkey-datarateproperty.md"><strong>MFPKEY_DATARATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-235"><a href="mfpkey-datarateproperty.md"><strong>MFPKEY_DATARATE</strong></a></span></span></td>
<td><span data-ttu-id="a789b-236">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a789b-236">Not used.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a789b-237"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-237"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span></span></td>
<td><span data-ttu-id="a789b-238">Gibt die Geräte Konformitäts Vorlage an, der der codierte Inhalt entspricht.</span><span class="sxs-lookup"><span data-stu-id="a789b-238">Specifies the device conformance template to which the encoded content conforms.</span></span><br/> <dl> <span data-ttu-id="a789b-239">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-239">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-240">Einfaches Profil, Hauptprofil, erweitertes Profil, Image.</span><span class="sxs-lookup"><span data-stu-id="a789b-240">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="a789b-241">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a789b-241">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a789b-242"><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-242"><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></span></span></td>
<td><span data-ttu-id="a789b-243">Gibt die Konformitäts Vorlage für Geräte an, die Sie für die Videocodierung verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="a789b-243">Specifies the device conformance template that you want to use for video encoding.</span></span><br/> <dl> <span data-ttu-id="a789b-244">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-244">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-245">Einfaches Profil, Hauptprofil, erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-245">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-246">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-246">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a789b-247"><a href="mfpkey-deltamvrangeindexproperty.md"><strong>MFPKEY_DELTAMVRANGEINDEX</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-247"><a href="mfpkey-deltamvrangeindexproperty.md"><strong>MFPKEY_DELTAMVRANGEINDEX</strong></a></span></span></td>
<td><span data-ttu-id="a789b-248">Gibt die Methode an, die zum Codieren der Bewegungsvektor Informationen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a789b-248">Specifies the method used to encode the motion vector information.</span></span><br/> <dl> <span data-ttu-id="a789b-249">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-249">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-250">Einfaches Profil, Hauptprofil, erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-250">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-251">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-251">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a789b-252"><a href="mfpkey-denoiseoptionproperty.md"><strong>MFPKEY_DENOISEOPTION</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-252"><a href="mfpkey-denoiseoptionproperty.md"><strong>MFPKEY_DENOISEOPTION</strong></a></span></span></td>
<td><span data-ttu-id="a789b-253">Gibt an, ob der Codec beim Codieren den Rauschfilter verwendet.</span><span class="sxs-lookup"><span data-stu-id="a789b-253">Specifies whether the codec will use the noise filter when encoding.</span></span><br/> <dl> <span data-ttu-id="a789b-254">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-254">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-255">Einfaches Profil, Hauptprofil, erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-255">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-256">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-256">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a789b-257"><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-257"><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="a789b-258">Gibt die gewünschte Qualitätsstufe für die Qualitäts basierte (1-Pass-) VBR-Codierung (Variable-Bitrate) an.</span><span class="sxs-lookup"><span data-stu-id="a789b-258">Specifies the desired quality level for quality based (1-pass) variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="a789b-259">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-259">Windows Vista and later.</span></span><br />
<span data-ttu-id="a789b-260">Einfaches Profil, Hauptprofil, erweitertes Profil, Image.</span><span class="sxs-lookup"><span data-stu-id="a789b-260">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="a789b-261">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-261">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a789b-262"><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-262"><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="a789b-263">Gibt die Anzahl der während der Codierung gelöschten Videorahmen an.</span><span class="sxs-lookup"><span data-stu-id="a789b-263">Specifies the number of video frames dropped during encoding.</span></span><br/> <dl> <span data-ttu-id="a789b-264">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-264">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-265">Einfaches Profil, Hauptprofil, erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-265">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-266">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a789b-266">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a789b-267"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-267"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span></span></td>
<td><span data-ttu-id="a789b-268">Gibt das Ende eines Codierungs Durchlaufs an.</span><span class="sxs-lookup"><span data-stu-id="a789b-268">Specifies the end of an encoding pass.</span></span><br/> <dl> <span data-ttu-id="a789b-269">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-269">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-270">Einfaches Profil, Hauptprofil, erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-270">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-271">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-271">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a789b-272"><a href="mfpkey-forceframeheightproperty.md"><strong>MFPKEY_FORCEFRAMEHEIGHT</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-272"><a href="mfpkey-forceframeheightproperty.md"><strong>MFPKEY_FORCEFRAMEHEIGHT</strong></a></span></span></td>
<td><span data-ttu-id="a789b-273">Gibt eine Zwischenrahmen Höhe für codiertes Video an.</span><span class="sxs-lookup"><span data-stu-id="a789b-273">Specifies an intermediate frame height for encoded video.</span></span><br/> <dl> <span data-ttu-id="a789b-274">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-274">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-275">Erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-275">Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-276">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-276">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a789b-277"><a href="mfpkey-forceframewidthproperty.md"><strong>MFPKEY_FORCEFRAMEWIDTH</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-277"><a href="mfpkey-forceframewidthproperty.md"><strong>MFPKEY_FORCEFRAMEWIDTH</strong></a></span></span></td>
<td><span data-ttu-id="a789b-278">Gibt eine zwischen Rahmenbreite für codiertes Video an.</span><span class="sxs-lookup"><span data-stu-id="a789b-278">Specifies an intermediate frame width for encoded video.</span></span><br/> <dl> <span data-ttu-id="a789b-279">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-279">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-280">Erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-280">Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-281">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-281">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a789b-282"><a href="mfpkey-forcemediansettingproperty.md"><strong>MFPKEY_FORCEMEDIANSETTING</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-282"><a href="mfpkey-forcemediansettingproperty.md"><strong>MFPKEY_FORCEMEDIANSETTING</strong></a></span></span></td>
<td><span data-ttu-id="a789b-283">Gibt an, ob der Codec die Median Filterung während der Codierung verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="a789b-283">Specifies whether the codec should use median filtering during encoding.</span></span><br/> <dl> <span data-ttu-id="a789b-284">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-284">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-285">Einfaches Profil, Hauptprofil, erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-285">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-286">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-286">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a789b-287"><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-287"><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></span></span></td>
<td><span data-ttu-id="a789b-288">Gibt den FourCC-Wert an, der den Encoder identifiziert, den Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="a789b-288">Specifies the FOURCC that identifies the encoder you want to use.</span></span><br/> <dl> <span data-ttu-id="a789b-289">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-289">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-290">Einfaches Profil, Hauptprofil, erweitertes Profil, Image.</span><span class="sxs-lookup"><span data-stu-id="a789b-290">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="a789b-291">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-291">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a789b-292"><a href="mfpkey-framecountproperty.md"><strong>MFPKEY_FRAMECOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-292"><a href="mfpkey-framecountproperty.md"><strong>MFPKEY_FRAMECOUNT</strong></a></span></span></td>
<td><span data-ttu-id="a789b-293">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="a789b-293">Obsolete.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a789b-294"><a href="mfpkey-fullframerateproperty.md"><strong>MFPKEY_FULLFRAMERATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-294"><a href="mfpkey-fullframerateproperty.md"><strong>MFPKEY_FULLFRAMERATE</strong></a></span></span></td>
<td><span data-ttu-id="a789b-295">Gibt an, ob der Encoder zum Löschen von Frames berechtigt ist.</span><span class="sxs-lookup"><span data-stu-id="a789b-295">Specifies whether the encoder is allowed to drop frames.</span></span><br/> <dl> <span data-ttu-id="a789b-296">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-296">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-297">Einfaches Profil, Hauptprofil, erweitertes Profil, Image.</span><span class="sxs-lookup"><span data-stu-id="a789b-297">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="a789b-298">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-298">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a789b-299"><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-299"><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></span></span></td>
<td><span data-ttu-id="a789b-300">Gibt an, ob die Codec-Ausgabe mit Zeilen Sprung dargestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a789b-300">Specifies whether the codec output will be interlaced.</span></span><br/> <dl> <span data-ttu-id="a789b-301">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-301">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-302">Erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-302">Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-303">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-303">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a789b-304"><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-304"><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></span></span></td>
<td><span data-ttu-id="a789b-305">Gibt die maximale Zeit (in Millisekunden) zwischen Keyframes in der Codec-Ausgabe an.</span><span class="sxs-lookup"><span data-stu-id="a789b-305">Specifies the maximum time, in milliseconds, between key frames in the codec output.</span></span><br/> <dl> <span data-ttu-id="a789b-306">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-306">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-307">Einfaches Profil, Hauptprofil, erweitertes Profil, Image.</span><span class="sxs-lookup"><span data-stu-id="a789b-307">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="a789b-308">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-308">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a789b-309"><a href="mfpkey-liveencodeproperty.md"><strong>MFPKEY_LIVEENCODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-309"><a href="mfpkey-liveencodeproperty.md"><strong>MFPKEY_LIVEENCODE</strong></a></span></span></td>
<td><span data-ttu-id="a789b-310">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a789b-310">Not used.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a789b-311"><a href="mfpkey-lookaheadproperty.md"><strong>MFPKEY_LOOKAHEAD</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-311"><a href="mfpkey-lookaheadproperty.md"><strong>MFPKEY_LOOKAHEAD</strong></a></span></span></td>
<td><span data-ttu-id="a789b-312">Gibt die Anzahl der Frames nach dem aktuellen Frame an, den der Codec vor dem Codieren des aktuellen Frames auswerten soll.</span><span class="sxs-lookup"><span data-stu-id="a789b-312">Specifies the number of frames after the current frame that the codec will evaluate before encoding the current frame.</span></span><br/> <dl> <span data-ttu-id="a789b-313">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-313">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-314">Einfaches Profil, Hauptprofil, erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-314">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-315">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-315">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a789b-316"><a href="mfpkey-loopfilterproperty.md"><strong>MFPKEY_LOOPFILTER</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-316"><a href="mfpkey-loopfilterproperty.md"><strong>MFPKEY_LOOPFILTER</strong></a></span></span></td>
<td><span data-ttu-id="a789b-317">Gibt an, ob der Codec den Schleifen Filter für die Schleife während der Codierung verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="a789b-317">Specifies whether the codec should use the in-loop deblocking filter during encoding.</span></span><br/> <dl> <span data-ttu-id="a789b-318">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-318">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-319">Hauptprofil, erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-319">Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-320">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-320">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a789b-321"><a href="mfpkey-macroblockmodecostmethodproperty.md"><strong>MFPKEY_MACROBLOCKMODECOSTMETHOD</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-321"><a href="mfpkey-macroblockmodecostmethodproperty.md"><strong>MFPKEY_MACROBLOCKMODECOSTMETHOD</strong></a></span></span></td>
<td><span data-ttu-id="a789b-322">Gibt die kostenmethode an, die vom Codec verwendet wird, um zu bestimmen, welcher Makroblock Modus verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a789b-322">Specifies the cost method used by the codec to determine which macroblock mode to use.</span></span><br/> <dl> <span data-ttu-id="a789b-323">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-323">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-324">Einfaches Profil, Hauptprofil, erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-324">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-325">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-325">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a789b-326"><a href="mfpkey-motionmatchmethodproperty.md"><strong>MFPKEY_MOTIONMATCHMETHOD</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-326"><a href="mfpkey-motionmatchmethodproperty.md"><strong>MFPKEY_MOTIONMATCHMETHOD</strong></a></span></span></td>
<td><span data-ttu-id="a789b-327">Gibt die Methode an, die für den Bewegungs Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a789b-327">Specifies the method to use for motion matching.</span></span><br/> <dl> <span data-ttu-id="a789b-328">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-328">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-329">Einfaches Profil, Hauptprofil, erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-329">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-330">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-330">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a789b-331"><a href="mfpkey-motionsearchlevelproperty.md"><strong>MFPKEY_MOTIONSEARCHLEVEL</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-331"><a href="mfpkey-motionsearchlevelproperty.md"><strong>MFPKEY_MOTIONSEARCHLEVEL</strong></a></span></span></td>
<td><span data-ttu-id="a789b-332">Gibt die Typen von Videoinformationen an, die bei Bewegungs Suchvorgängen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a789b-332">Specifies the types of video information that are used in motion search operations.</span></span><br/> <dl> <span data-ttu-id="a789b-333">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-333">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-334">Einfaches Profil, Hauptprofil, erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-334">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-335">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-335">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a789b-336"><a href="mfpkey-motionsearchrangeproperty.md"><strong>MFPKEY_MOTIONSEARCHRANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-336"><a href="mfpkey-motionsearchrangeproperty.md"><strong>MFPKEY_MOTIONSEARCHRANGE</strong></a></span></span></td>
<td><span data-ttu-id="a789b-337">Gibt den in Bewegungs suchen verwendeten Bereich an.</span><span class="sxs-lookup"><span data-stu-id="a789b-337">Specifies the range used in motion searches.</span></span><br/> <dl> <span data-ttu-id="a789b-338">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-338">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-339">Hauptprofil, erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-339">Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-340">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-340">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a789b-341"><a href="mfpkey-noiseedgeremovalproperty.md"><strong>MFPKEY_NOISEEDGEREMOVAL</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-341"><a href="mfpkey-noiseedgeremovalproperty.md"><strong>MFPKEY_NOISEEDGEREMOVAL</strong></a></span></span></td>
<td><span data-ttu-id="a789b-342">Gibt an, ob der Codec versuchen soll, laute Rahmen Ränder zu erkennen und zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="a789b-342">Specifies whether the codec should attempt to detect noisy frame edges and remove them.</span></span><br/> <dl> <span data-ttu-id="a789b-343">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-343">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-344">Einfaches Profil, Hauptprofil, erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-344">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-345">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-345">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a789b-346"><a href="mfpkey-numbframesproperty.md"><strong>MFPKEY_NUMBFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-346"><a href="mfpkey-numbframesproperty.md"><strong>MFPKEY_NUMBFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="a789b-347">Gibt die Anzahl der bidirektionalen Vorhersage Rahmen (B-Frames) an.</span><span class="sxs-lookup"><span data-stu-id="a789b-347">Specifies the number of bidirectional predictive frames (B-frames).</span></span><br/> <dl> <span data-ttu-id="a789b-348">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-348">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-349">Hauptprofil, erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-349">Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-350">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-350">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a789b-351"><a href="mfpkey-numthreadsproperty.md"><strong>MFPKEY_NUMTHREADS</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-351"><a href="mfpkey-numthreadsproperty.md"><strong>MFPKEY_NUMTHREADS</strong></a></span></span></td>
<td><span data-ttu-id="a789b-352">Gibt die Anzahl der Threads an, die der Codec für die Codierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="a789b-352">Specifies the number of threads that the codec will use for encoding.</span></span><br/> <dl> <span data-ttu-id="a789b-353">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-353">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-354">Einfaches Profil, Hauptprofil, erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-354">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-355">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-355">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a789b-356"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-356"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span></span></td>
<td><span data-ttu-id="a789b-357">Gibt die maximale Anzahl von durch den Codec unterstützten Durchläufen an.</span><span class="sxs-lookup"><span data-stu-id="a789b-357">Specifies the maximum number of passes supported by the codec.</span></span><br/> <dl> <span data-ttu-id="a789b-358">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-358">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-359">Einfaches Profil, Hauptprofil, erweitertes Profil, Image.</span><span class="sxs-lookup"><span data-stu-id="a789b-359">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="a789b-360">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a789b-360">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a789b-361"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-361"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span></span></td>
<td><span data-ttu-id="a789b-362">Gibt die Anzahl von Durchläufen an, die vom Codec zum Codieren des Inhalts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a789b-362">Specifies the number of passes that the codec will use to encode the content.</span></span><br/> <dl> <span data-ttu-id="a789b-363">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-363">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-364">Einfaches Profil, Hauptprofil, erweitertes Profil, Image.</span><span class="sxs-lookup"><span data-stu-id="a789b-364">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="a789b-365">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-365">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a789b-366"><a href="mfpkey-perceptualoptlevelproperty.md"><strong>MFPKEY_PERCEPTUALOPTLEVEL</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-366"><a href="mfpkey-perceptualoptlevelproperty.md"><strong>MFPKEY_PERCEPTUALOPTLEVEL</strong></a></span></span></td>
<td><span data-ttu-id="a789b-367">Gibt an, ob der Codec beim Codieren die konservative perzeptive Optimierung verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="a789b-367">Specifies whether the codec should use conservative perceptual optimization when encoding.</span></span><br/> <dl> <span data-ttu-id="a789b-368">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-368">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-369">Hauptprofil, erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-369">Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-370">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-370">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a789b-371"><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-371"><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="a789b-372">Gibt an, ob der Encoder für doppelte Frames Dummy-Frame-Einträge im Bitdaten Strom erzeugt.</span><span class="sxs-lookup"><span data-stu-id="a789b-372">Specifies whether the encoder produces dummy frame entries in the bit stream for duplicate frames.</span></span><br/> <dl> <span data-ttu-id="a789b-373">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-373">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-374">Einfaches Profil, Hauptprofil, erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-374">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-375">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-375">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a789b-376"><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-376"><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></span></span></td>
<td><span data-ttu-id="a789b-377">Gibt QP an.</span><span class="sxs-lookup"><span data-stu-id="a789b-377">Specifies QP.</span></span><br/> <dl> <span data-ttu-id="a789b-378">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-378">Windows Vista and later.</span></span><br />
<span data-ttu-id="a789b-379">Einfaches Profil, Hauptprofil, erweitertes Profil, Image.</span><span class="sxs-lookup"><span data-stu-id="a789b-379">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="a789b-380">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-380">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a789b-381"><a href="mfpkey-rangereduxproperty.md"><strong>MFPKEY_RANGEREDUX</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-381"><a href="mfpkey-rangereduxproperty.md"><strong>MFPKEY_RANGEREDUX</strong></a></span></span></td>
<td><span data-ttu-id="a789b-382">Gibt den Grad an, zu dem der Codec den effektiven Farbbereich des Videos verringern soll.</span><span class="sxs-lookup"><span data-stu-id="a789b-382">Specifies the degree to which the codec should reduce the effective color range of the video.</span></span><br/> <dl> <span data-ttu-id="a789b-383">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-383">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-384">Erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-384">Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-385">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-385">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a789b-386"><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-386"><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></span></span></td>
<td><span data-ttu-id="a789b-387">Gibt die durchschnittliche Bitrate in Bits pro Sekunde an, die für die 2-Pass-VBR-Codierung (Variable Bitrate) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a789b-387">Specifies the average bit rate, in bits per second, used for 2-pass variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="a789b-388">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-388">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-389">Einfaches Profil, Hauptprofil, erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-389">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-390">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-390">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a789b-391"><a href="mfpkey-rdsubpixelsearchproperty.md"><strong>MFPKEY_RDSUBPIXELSEARCH</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-391"><a href="mfpkey-rdsubpixelsearchproperty.md"><strong>MFPKEY_RDSUBPIXELSEARCH</strong></a></span></span></td>
<td><span data-ttu-id="a789b-392">Gibt an, ob der Encoder die RD-basierte unter Pixel-MV-Suche verwendet.</span><span class="sxs-lookup"><span data-stu-id="a789b-392">Specifies whether the encoder uses RD-based sub-pixel MV search.</span></span> <br/> <dl> <span data-ttu-id="a789b-393">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-393">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-394">Einfaches Profil, Hauptprofil, erweitertes Profil, Image.</span><span class="sxs-lookup"><span data-stu-id="a789b-394">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="a789b-395">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-395">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a789b-396"><a href="mfpkey-reencendbuffersizeproperty.md"><strong>MFPKEY_REENCENDBUFFERSIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-396"><a href="mfpkey-reencendbuffersizeproperty.md"><strong>MFPKEY_REENCENDBUFFERSIZE</strong></a></span></span></td>
<td><span data-ttu-id="a789b-397">Gibt für die Neucodierung von Segmenten die Puffergröße an.</span><span class="sxs-lookup"><span data-stu-id="a789b-397">For segment re-encoding, specifies the buffer size.</span></span><br/> <dl> <span data-ttu-id="a789b-398">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-398">Windows Vista and later.</span></span><br />
<span data-ttu-id="a789b-399">Einfaches Profil, Hauptprofil, erweitertes Profil, Image.</span><span class="sxs-lookup"><span data-stu-id="a789b-399">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="a789b-400">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-400">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a789b-401"><a href="mfpkey-reencdurationproperty.md"><strong>MFPKEY_REENCDURATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-401"><a href="mfpkey-reencdurationproperty.md"><strong>MFPKEY_REENCDURATION</strong></a></span></span></td>
<td><span data-ttu-id="a789b-402">Gibt für die Neucodierung von Segmenten die Dauer des zu codierenden Segments an.</span><span class="sxs-lookup"><span data-stu-id="a789b-402">For segment re-encoding, specifies the duration of the segment to be re-encoded.</span></span><br/> <dl> <span data-ttu-id="a789b-403">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-403">Windows Vista and later.</span></span><br />
<span data-ttu-id="a789b-404">Einfaches Profil, Hauptprofil, erweitertes Profil, Image.</span><span class="sxs-lookup"><span data-stu-id="a789b-404">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="a789b-405">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-405">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a789b-406"><a href="mfpkey-reencqprefproperty.md"><strong>MFPKEY_REENCQPREF</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-406"><a href="mfpkey-reencqprefproperty.md"><strong>MFPKEY_REENCQPREF</strong></a></span></span></td>
<td><span data-ttu-id="a789b-407">Gibt für die Neucodierung von Segmenten den quantifizer des Frames vor dem Start Segment an.</span><span class="sxs-lookup"><span data-stu-id="a789b-407">For segment re-encoding, specifies the quantizer of the frame prior to the starting segment.</span></span><br/> <dl> <span data-ttu-id="a789b-408">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-408">Windows Vista and later.</span></span><br />
<span data-ttu-id="a789b-409">Einfaches Profil, Hauptprofil, erweitertes Profil, Image.</span><span class="sxs-lookup"><span data-stu-id="a789b-409">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="a789b-410">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-410">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a789b-411"><a href="mfpkey-reencstartbuffersizeproperty.md"><strong>MFPKEY_REENCSTARTBUFFERSIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-411"><a href="mfpkey-reencstartbuffersizeproperty.md"><strong>MFPKEY_REENCSTARTBUFFERSIZE</strong></a></span></span></td>
<td><span data-ttu-id="a789b-412">Gibt bei der Neucodierung von Segmenten die Größe des Start Puffers an.</span><span class="sxs-lookup"><span data-stu-id="a789b-412">For segment re-encoding, specifies the starting buffer fullness.</span></span><br/> <dl> <span data-ttu-id="a789b-413">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-413">Windows Vista and later.</span></span><br />
<span data-ttu-id="a789b-414">Einfaches Profil, Hauptprofil, erweitertes Profil, Image.</span><span class="sxs-lookup"><span data-stu-id="a789b-414">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="a789b-415">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-415">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a789b-416"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-416"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span></span></td>
<td><span data-ttu-id="a789b-417">Gibt die Spitzen Bitrate in Bits pro Sekunde an, die für die eingeschränkte 2-Pass-Variable-Bitrate (VBR) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a789b-417">Specifies the peak bit rate, in bits per second, used for constrained 2-pass variable-bit-rate (VBR).</span></span><br/> <dl> <span data-ttu-id="a789b-418">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-418">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-419">Einfaches Profil, Hauptprofil, erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-419">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-420">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-420">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a789b-421"><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-421"><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="a789b-422">Gibt die Anzahl der Videorahmen an, die während des Codierungs Vorgangs an den Encoder übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="a789b-422">Specifies the number of video frames passed to the encoder during the encoding process.</span></span><br/> <dl> <span data-ttu-id="a789b-423">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-423">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-424">Einfaches Profil, Hauptprofil, erweitertes Profil, Image.</span><span class="sxs-lookup"><span data-stu-id="a789b-424">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="a789b-425">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a789b-425">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a789b-426"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-426"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span></span></td>
<td><span data-ttu-id="a789b-427">Gibt an, ob der Codec die VBR-Codierung (Variable-Bit-Rate) verwendet.</span><span class="sxs-lookup"><span data-stu-id="a789b-427">Specifies whether the codec will use variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="a789b-428">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-428">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-429">Einfaches Profil, Hauptprofil, erweitertes Profil, Image.</span><span class="sxs-lookup"><span data-stu-id="a789b-429">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="a789b-430">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-430">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a789b-431"><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-431"><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="a789b-432">Gibt die tatsächliche Qualitätsstufe für die Qualitäts basierte (1-Pass-) VBR-Codierung (Variable-Bitrate) an.</span><span class="sxs-lookup"><span data-stu-id="a789b-432">Specifies the actual quality level for quality based (1-pass) variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="a789b-433">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-433">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-434">Einfaches Profil, Hauptprofil, erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-434">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-435">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-435">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a789b-436"><a href="mfpkey-videoscalingproperty.md"><strong>MFPKEY_VIDEOSCALING</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-436"><a href="mfpkey-videoscalingproperty.md"><strong>MFPKEY_VIDEOSCALING</strong></a></span></span></td>
<td><span data-ttu-id="a789b-437">Gibt an, ob der Codec die Optimierung der Video Skalierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="a789b-437">Specifies whether the codec will use video scaling optimization.</span></span><br/> <dl> <span data-ttu-id="a789b-438">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-438">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-439">Einfaches Profil, Hauptprofil, erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-439">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-440">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-440">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a789b-441"><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-441"><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></span></span></td>
<td><span data-ttu-id="a789b-442">Gibt den Umfang des Inhalts in Millisekunden an, der in den Modell Puffer passen kann.</span><span class="sxs-lookup"><span data-stu-id="a789b-442">Specifies the amount of content, in milliseconds, that can fit into the model buffer.</span></span><br/> <dl> <span data-ttu-id="a789b-443">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-443">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-444">Erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-444">Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-445">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-445">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a789b-446"><a href="mfpkey-volheaderforreencodeproperty.md"><strong>MFPKEY_VOLHEADERFORREENCODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-446"><a href="mfpkey-volheaderforreencodeproperty.md"><strong>MFPKEY_VOLHEADERFORREENCODE</strong></a></span></span></td>
<td><span data-ttu-id="a789b-447">Gibt für die Neucodierung von Segmenten die privaten Codec-Daten der Datei an, die erneut codiert wird.</span><span class="sxs-lookup"><span data-stu-id="a789b-447">For segment re-encoding, specifies the codec private data of the file that is being re-encoded.</span></span><br/> <dl> <span data-ttu-id="a789b-448">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-448">Windows Vista and later.</span></span><br />
<span data-ttu-id="a789b-449">Einfaches Profil, Hauptprofil, erweitertes Profil, Image.</span><span class="sxs-lookup"><span data-stu-id="a789b-449">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="a789b-450">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-450">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a789b-451"><a href="mfpkey-vtypeproperty.md"><strong>MFPKEY_VTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-451"><a href="mfpkey-vtypeproperty.md"><strong>MFPKEY_VTYPE</strong></a></span></span></td>
<td><span data-ttu-id="a789b-452">Gibt den Typ der Logik an, die der Codec zum Erkennen von Zeilen Sprung-Quellvideos verwendet.</span><span class="sxs-lookup"><span data-stu-id="a789b-452">Specifies the type of logic that the codec will use to detect interlaced source video.</span></span><br/> <dl> <span data-ttu-id="a789b-453">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-453">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-454">Erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-454">Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-455">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a789b-455">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a789b-456"><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="a789b-456"><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="a789b-457">Gibt die Anzahl der Videorahmen an, die übersprungen wurden, weil Sie Duplikate vorheriger Frames waren.</span><span class="sxs-lookup"><span data-stu-id="a789b-457">Specifies the number of video frames that were skipped because they were duplicates of previous frames.</span></span><br/> <dl> <span data-ttu-id="a789b-458">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="a789b-458">Windows XP and later.</span></span><br />
<span data-ttu-id="a789b-459">Einfaches Profil, Hauptprofil, erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="a789b-459">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="a789b-460">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a789b-460">Read-only</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="a789b-461">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a789b-461">Requirements</span></span>



| <span data-ttu-id="a789b-462">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a789b-462">Requirement</span></span> | <span data-ttu-id="a789b-463">Wert</span><span class="sxs-lookup"><span data-stu-id="a789b-463">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a789b-464">Client</span><span class="sxs-lookup"><span data-stu-id="a789b-464">Client</span></span><br/> | <span data-ttu-id="a789b-465">Windows XP, Windows Vista oder Windows 7</span><span class="sxs-lookup"><span data-stu-id="a789b-465">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="a789b-466">Header</span><span class="sxs-lookup"><span data-stu-id="a789b-466">Header</span></span><br/> | <dl> <span data-ttu-id="a789b-467"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a789b-467"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="a789b-468">DLL</span><span class="sxs-lookup"><span data-stu-id="a789b-468">DLL</span></span><br/>    | <dl> <span data-ttu-id="a789b-469"><dt>Wmvencod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a789b-469"><dt>Wmvencod.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a789b-470">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a789b-470">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a789b-471">Codec-Objekte</span><span class="sxs-lookup"><span data-stu-id="a789b-471">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="a789b-472">Codec-Implementierung</span><span class="sxs-lookup"><span data-stu-id="a789b-472">Codec Implementation</span></span>](codecimplementation.md)
</dt> </dl>

 

 
