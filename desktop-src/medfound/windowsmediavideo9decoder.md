---
description: Der Windows Media Video 9-Decoder decodiert Videostreams, die vom Windows Media Video Encoder codiert wurden.
ms.assetid: 08f68d1c-c226-4bf6-abd0-fce0f9ddbc05
title: Windows Media Video 9-Decoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96d89e05f82ce503016a10d5591a23bc673d0db5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371632"
---
# <a name="windows-media-video-9-decoder"></a><span data-ttu-id="b942c-103">Windows Media Video 9-Decoder</span><span class="sxs-lookup"><span data-stu-id="b942c-103">Windows Media Video 9 Decoder</span></span>

<span data-ttu-id="b942c-104">Der Windows Media Video 9-Decoder decodiert Videostreams, die vom [**Windows Media Video Encoder**](windowsmediavideo9encoder.md)codiert wurden.</span><span class="sxs-lookup"><span data-stu-id="b942c-104">The Windows Media Video 9 decoder decodes video streams that were encoded by the [**Windows Media Video Encoder**](windowsmediavideo9encoder.md).</span></span> <span data-ttu-id="b942c-105">Der Encoder und der Decoder unterstützen die folgenden vier Kategorien codierter Videos.</span><span class="sxs-lookup"><span data-stu-id="b942c-105">The encoder and decoder support the following four categories of encoded video.</span></span>

-   <span data-ttu-id="b942c-106">Windows Media Video 9 einfaches Profil</span><span class="sxs-lookup"><span data-stu-id="b942c-106">Windows Media Video 9 Simple Profile</span></span>
-   <span data-ttu-id="b942c-107">Windows Media Video 9 Hauptprofil</span><span class="sxs-lookup"><span data-stu-id="b942c-107">Windows Media Video 9 Main Profile</span></span>
-   <span data-ttu-id="b942c-108">Erweiterte profile Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="b942c-108">Windows Media Video 9 Advanced Profile</span></span>
-   <span data-ttu-id="b942c-109">Windows Media Video 9,1-Image</span><span class="sxs-lookup"><span data-stu-id="b942c-109">Windows Media Video 9.1 Image</span></span>

## <a name="class-identifier"></a><span data-ttu-id="b942c-110">Klassen Bezeichner</span><span class="sxs-lookup"><span data-stu-id="b942c-110">Class Identifier</span></span>

<span data-ttu-id="b942c-111">Der Klassen Bezeichner (CLSID) für den Windows Media Video Decoder wird durch die Konstante **CLSID \_ cwmvdecmediaobject** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b942c-111">The class identifier (CLSID) for the Windows Media Video decoder is represented by the constant **CLSID\_CWMVDecMediaObject**.</span></span> <span data-ttu-id="b942c-112">Sie können eine Instanz des Video-Decoders erstellen, indem Sie **CoCreateInstance** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b942c-112">You can create an instance of the video decoder by calling **CoCreateInstance**.</span></span>

## <a name="interfaces"></a><span data-ttu-id="b942c-113">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="b942c-113">Interfaces</span></span>

<span data-ttu-id="b942c-114">Ein Video Decoder-Objekt macht die [**imediaobject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) -Schnittstelle verfügbar, sodass das Objekt als DirectX-Medienobjekt (DMO) verwendet werden kann, und stellt die [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle zur Verfügung, sodass das Objekt als Media Foundation Transformation (MFT) verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b942c-114">A video decoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="b942c-115">Ein Video Decoder verhält sich als DMO oder MFT, je nachdem, welche Schnittstellen Sie erhalten und welche Version von Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b942c-115">A video decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="b942c-116">In der folgenden Tabelle sind die Bedingungen aufgeführt, unter denen sich ein Video Decoder als DMO oder MFT verhält.</span><span class="sxs-lookup"><span data-stu-id="b942c-116">The following table shows the conditions under which a video decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="b942c-117">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="b942c-117">Operating system</span></span>            | <span data-ttu-id="b942c-118">Decoderverhalten</span><span class="sxs-lookup"><span data-stu-id="b942c-118">Decoder behavior</span></span>                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b942c-119">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b942c-119">Windows XP</span></span>                  | <span data-ttu-id="b942c-120">Ein Windows Media-Video Decoder verhält sich immer als DMO.</span><span class="sxs-lookup"><span data-stu-id="b942c-120">A Windows Media video decoder always behaves as a DMO.</span></span>                                                                                                                |
| <span data-ttu-id="b942c-121">Windows Vista und Windows 7</span><span class="sxs-lookup"><span data-stu-id="b942c-121">Windows Vista and Windows 7</span></span> | <span data-ttu-id="b942c-122">Standardmäßig verhält sich ein Windows Media-Video Decoder als DMO.</span><span class="sxs-lookup"><span data-stu-id="b942c-122">By default, a Windows Media video decoder behaves as a DMO.</span></span> <span data-ttu-id="b942c-123">Wenn Sie eine [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle in einem Video Decoder erhalten, verhält sie sich wie eine MFT.</span><span class="sxs-lookup"><span data-stu-id="b942c-123">If you obtain an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on a video decoder, it behaves as an MFT.</span></span> |



 

<span data-ttu-id="b942c-124">Ab Windows 7 implementiert der Windows Media Video Decoder die [**idmuqualitycontrol**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-idmoqualitycontrol) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b942c-124">Beginning with Windows 7, the Windows Media Video decoder implements the [**IDMOQualityControl**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-idmoqualitycontrol) interface.</span></span>

## <a name="input-formats"></a><span data-ttu-id="b942c-125">Eingabeformate</span><span class="sxs-lookup"><span data-stu-id="b942c-125">Input Formats</span></span>

<span data-ttu-id="b942c-126">In der folgenden Tabelle werden die vier Zeichen Codes (fourccs) angezeigt, die den Kategorien codierter Eingaben entsprechen, die vom Windows Media Video Decoder unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b942c-126">The following table shows the four-character codes (FOURCCs) that correspond to the categories of encoded input that are supported by the Windows Media Video decoder.</span></span>



| <span data-ttu-id="b942c-127">Category</span><span class="sxs-lookup"><span data-stu-id="b942c-127">Category</span></span>                               | <span data-ttu-id="b942c-128">FOURCC</span><span class="sxs-lookup"><span data-stu-id="b942c-128">FOURCC</span></span>                                   |
|----------------------------------------|------------------------------------------|
| <span data-ttu-id="b942c-129">Windows Media Video 9 einfaches Profil</span><span class="sxs-lookup"><span data-stu-id="b942c-129">Windows Media Video 9 Simple Profile</span></span>   | <span data-ttu-id="b942c-130">"WMV3"</span><span class="sxs-lookup"><span data-stu-id="b942c-130">"WMV3"</span></span>                                   |
| <span data-ttu-id="b942c-131">Windows Media Video 9 Hauptprofil</span><span class="sxs-lookup"><span data-stu-id="b942c-131">Windows Media Video 9 Main Profile</span></span>     | <span data-ttu-id="b942c-132">"WMV3"</span><span class="sxs-lookup"><span data-stu-id="b942c-132">"WMV3"</span></span>                                   |
| <span data-ttu-id="b942c-133">Erweiterte profile Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="b942c-133">Windows Media Video 9 Advanced Profile</span></span> | <span data-ttu-id="b942c-134">"WVC1"</span><span class="sxs-lookup"><span data-stu-id="b942c-134">"WVC1"</span></span>                                   |
| <span data-ttu-id="b942c-135">Windows Media Video 9,1-Image</span><span class="sxs-lookup"><span data-stu-id="b942c-135">Windows Media Video 9.1 Image</span></span>          | <span data-ttu-id="b942c-136">"Wmvp" für 9,1, "WVP2" für 9,1 Version 2</span><span class="sxs-lookup"><span data-stu-id="b942c-136">"WMVP" for 9.1, "WVP2" for 9.1 version 2</span></span> |



 

## <a name="output-formats"></a><span data-ttu-id="b942c-137">Ausgabeformate</span><span class="sxs-lookup"><span data-stu-id="b942c-137">Output Formats</span></span>

<span data-ttu-id="b942c-138">Der Windows Media Video-Decoder unterstützt die folgenden Ausgabemedien-Untertypen, wenn er als DMO fungiert.</span><span class="sxs-lookup"><span data-stu-id="b942c-138">The Windows Media Video decoder supports the following output media subtypes when it is acting as a DMO.</span></span>

-   <span data-ttu-id="b942c-139">Mediasubtype \_ NV12</span><span class="sxs-lookup"><span data-stu-id="b942c-139">MEDIASUBTYPE\_NV12</span></span>
-   <span data-ttu-id="b942c-140">Mediasubtype \_ YV12</span><span class="sxs-lookup"><span data-stu-id="b942c-140">MEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="b942c-141">Mediasubtype \_ im YUY2</span><span class="sxs-lookup"><span data-stu-id="b942c-141">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="b942c-142">mediasubtype \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="b942c-142">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="b942c-143">mediasubtype \_ yvyu</span><span class="sxs-lookup"><span data-stu-id="b942c-143">MEDIASUBTYPE\_YVYU</span></span>
-   <span data-ttu-id="b942c-144">Mediasubtype \_ NV11</span><span class="sxs-lookup"><span data-stu-id="b942c-144">MEDIASUBTYPE\_NV11</span></span>
-   <span data-ttu-id="b942c-145">Mediasubtype \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="b942c-145">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="b942c-146">Mediasubtype \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="b942c-146">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="b942c-147">Mediasubtype \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="b942c-147">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="b942c-148">Mediasubtype \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="b942c-148">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="b942c-149">Mediasubtype \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="b942c-149">MEDIASUBTYPE\_RGB8</span></span>

<span data-ttu-id="b942c-150">Der Windows Media Video-Decoder unterstützt die folgenden Ausgabemedien-Untertypen, wenn er als MFT fungiert.</span><span class="sxs-lookup"><span data-stu-id="b942c-150">The Windows Media Video decoder supports the following output media subtypes when it is acting as an MFT.</span></span>

-   <span data-ttu-id="b942c-151">MF-Format \_ NV12</span><span class="sxs-lookup"><span data-stu-id="b942c-151">MFVideoFormat\_NV12</span></span>
-   <span data-ttu-id="b942c-152">MF-Format \_ YV12</span><span class="sxs-lookup"><span data-stu-id="b942c-152">MFVideoFormat\_YV12</span></span>
-   <span data-ttu-id="b942c-153">MF-Format \_ im YUY2</span><span class="sxs-lookup"><span data-stu-id="b942c-153">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="b942c-154">MF-Format ( \_ UYVY)</span><span class="sxs-lookup"><span data-stu-id="b942c-154">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="b942c-155">Mfvideoformat \_ yvyu</span><span class="sxs-lookup"><span data-stu-id="b942c-155">MFVideoFormat\_YVYU</span></span>
-   <span data-ttu-id="b942c-156">MF-Format \_ NV11</span><span class="sxs-lookup"><span data-stu-id="b942c-156">MFVideoFormat\_NV11</span></span>
-   <span data-ttu-id="b942c-157">MF-Format \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="b942c-157">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="b942c-158">MF-Format \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="b942c-158">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="b942c-159">MF-Format \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="b942c-159">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="b942c-160">MF-Format \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="b942c-160">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="b942c-161">MF-Format \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="b942c-161">MFVideoFormat\_RGB8</span></span>

## <a name="properties"></a><span data-ttu-id="b942c-162">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b942c-162">Properties</span></span>

<span data-ttu-id="b942c-163">Der Windows Media Video-Decoder unterstützt die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b942c-163">The Windows Media Video decoder supports the following properties.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b942c-164">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b942c-164">Property</span></span></th>
<th><span data-ttu-id="b942c-165">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b942c-165">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b942c-166"><a href="mfpkey-decoder-deinterlacingproperty.md">MFPKEY_DECODER_DEINTERLACING</a></span><span class="sxs-lookup"><span data-stu-id="b942c-166"><a href="mfpkey-decoder-deinterlacingproperty.md">MFPKEY_DECODER_DEINTERLACING</a></span></span></td>
<td><span data-ttu-id="b942c-167">Gibt an, ob der Codec interpackt Video Frames aus dem komprimierten Stream als progressive Frames decodiert.</span><span class="sxs-lookup"><span data-stu-id="b942c-167">Specifies whether the codec decodes interlaced video frames from the compressed stream as progressive frames.</span></span><br/> <dl> <span data-ttu-id="b942c-168">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="b942c-168">Windows XP and later.</span></span><br />
<span data-ttu-id="b942c-169">Einfaches Profil, Hauptprofil, erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="b942c-169">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="b942c-170">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="b942c-170">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b942c-171"><a href="mfpkey-dxva-enabledproperty.md">MFPKEY_DXVA_ENABLED</a></span><span class="sxs-lookup"><span data-stu-id="b942c-171"><a href="mfpkey-dxva-enabledproperty.md">MFPKEY_DXVA_ENABLED</a></span></span></td>
<td><span data-ttu-id="b942c-172">Gibt an, ob der Decoder die DirectX-Video Beschleunigungs Hardware verwendet, falls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b942c-172">Specifies whether the decoder will use DirectX video acceleration hardware, if available.</span></span><br/> <dl> <span data-ttu-id="b942c-173">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="b942c-173">Windows XP and later.</span></span><br />
<span data-ttu-id="b942c-174">Einfaches Profil, Hauptprofil, erweitertes Profil.</span><span class="sxs-lookup"><span data-stu-id="b942c-174">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="b942c-175">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="b942c-175">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b942c-176"><a href="mfpkey-avdecvideoswpowerlevelproperty.md">MFPKEY_AVDecVideoSWPowerLevel</a></span><span class="sxs-lookup"><span data-stu-id="b942c-176"><a href="mfpkey-avdecvideoswpowerlevelproperty.md">MFPKEY_AVDecVideoSWPowerLevel</a></span></span></td>
<td><span data-ttu-id="b942c-177">Gibt die Leistungs Ebene für den Decoder an.</span><span class="sxs-lookup"><span data-stu-id="b942c-177">Specifies the power level for the decoder.</span></span><br/> <dl> <span data-ttu-id="b942c-178">Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b942c-178">Windows 7.</span></span><br />
<span data-ttu-id="b942c-179">Einfaches Profil, Hauptprofil, erweitertes Profil, Image.</span><span class="sxs-lookup"><span data-stu-id="b942c-179">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="b942c-180">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="b942c-180">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b942c-181"><a href="mfpkey-fi-enabledproperty.md">MFPKEY_FI_ENABLED</a></span><span class="sxs-lookup"><span data-stu-id="b942c-181"><a href="mfpkey-fi-enabledproperty.md">MFPKEY_FI_ENABLED</a></span></span></td>
<td><span data-ttu-id="b942c-182">Gibt an, ob der Decoder die Frame Interpolation verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="b942c-182">Specifies whether the decoder should use frame interpolation.</span></span><br/> <dl> <span data-ttu-id="b942c-183">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="b942c-183">Windows XP and later.</span></span><br />
<span data-ttu-id="b942c-184">Einfaches Profil, Hauptprofil, erweitertes Profil, Image.</span><span class="sxs-lookup"><span data-stu-id="b942c-184">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="b942c-185">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="b942c-185">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b942c-186"><a href="mfpkey-fi-supportedproperty.md">MFPKEY_FI_SUPPORTED</a></span><span class="sxs-lookup"><span data-stu-id="b942c-186"><a href="mfpkey-fi-supportedproperty.md">MFPKEY_FI_SUPPORTED</a></span></span></td>
<td><span data-ttu-id="b942c-187">Gibt an, ob der Decoder Frame Interpolation unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b942c-187">Specifies whether the decoder supports frame interpolation.</span></span><br/> <dl> <span data-ttu-id="b942c-188">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="b942c-188">Windows XP and later.</span></span><br />
<span data-ttu-id="b942c-189">Einfaches Profil, Hauptprofil, erweitertes Profil, Bild</span><span class="sxs-lookup"><span data-stu-id="b942c-189">Simple Profile, Main Profile, Advanced Profile, Image</span></span><br />
<span data-ttu-id="b942c-190">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="b942c-190">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b942c-191"><a href="mfpkey-numthreadsdecproperty.md">MFPKEY_NUMTHREADSDEC</a></span><span class="sxs-lookup"><span data-stu-id="b942c-191"><a href="mfpkey-numthreadsdecproperty.md">MFPKEY_NUMTHREADSDEC</a></span></span></td>
<td><span data-ttu-id="b942c-192">Gibt die Anzahl der Threads an, die vom Decoder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b942c-192">Specifies the number of threads that the decoder will use.</span></span><br/> <dl> <span data-ttu-id="b942c-193">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="b942c-193">Windows Vista and later.</span></span><br />
<span data-ttu-id="b942c-194">Einfaches Profil, Hauptprofil, erweitertes Profil, Image.</span><span class="sxs-lookup"><span data-stu-id="b942c-194">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="b942c-195">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="b942c-195">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b942c-196"><a href="mfpkey-postprocessmodeproperty.md">MFPKEY_POSTPROCESSMODE</a></span><span class="sxs-lookup"><span data-stu-id="b942c-196"><a href="mfpkey-postprocessmodeproperty.md">MFPKEY_POSTPROCESSMODE</a></span></span></td>
<td><span data-ttu-id="b942c-197">Gibt den postverarbeitungs Modus für den Decoder an.</span><span class="sxs-lookup"><span data-stu-id="b942c-197">Specifies the post processing mode for the decoder.</span></span><br/> <dl> <span data-ttu-id="b942c-198">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="b942c-198">Windows Vista and later.</span></span><br />
<span data-ttu-id="b942c-199">Einfaches Profil, Hauptprofil, erweitertes Profil, Image.</span><span class="sxs-lookup"><span data-stu-id="b942c-199">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="b942c-200">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="b942c-200">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b942c-201"><strong>g_wszWMVCNeedsDrain</strong></span><span class="sxs-lookup"><span data-stu-id="b942c-201"><strong>g_wszWMVCNeedsDrain</strong></span></span></td>
<td><span data-ttu-id="b942c-202">Gibt an, ob der Decoder entladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b942c-202">Specifies whether the decoder should be drained.</span></span><br/> <dl> <span data-ttu-id="b942c-203">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b942c-203">Windows 8</span></span><br />
<span data-ttu-id="b942c-204">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="b942c-204">Read-only.</span></span><br />
</dl> <span data-ttu-id="b942c-205">Diese Eigenschaft wird von der Windows Media-Format Laufzeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="b942c-205">This property is used by the Windows Media Format runtime.</span></span> <span data-ttu-id="b942c-206">Der Eigenschaftentyp ist <strong>VARIANT_BOOL</strong>.</span><span class="sxs-lookup"><span data-stu-id="b942c-206">The property type is <strong>VARIANT_BOOL</strong>.</span></span> <span data-ttu-id="b942c-207">Wenn der Wert <strong>VARIANT_TRUE</strong>ist, sollte der Decoder nach einer Diskontinuität entladen werden.</span><span class="sxs-lookup"><span data-stu-id="b942c-207">If the value is <strong>VARIANT_TRUE</strong>, the decoder should be drained after a discontinuity.</span></span> <span data-ttu-id="b942c-208">Weitere Informationen zum Entleeren von MFT finden Sie unter <a href="basic-mft-processing-model.md">Grundlegendes MFT-Verarbeitungsmodell</a>.</span><span class="sxs-lookup"><span data-stu-id="b942c-208">For more information about draining an MFT, see <a href="basic-mft-processing-model.md">Basic MFT Processing Model</a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b942c-209">Um diese Eigenschaft abzufragen, verwenden Sie die <a href="/windows/desktop/com/ipropertybag-and-ipersistpropertybag"><strong>IPropertyBag</strong></a> -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b942c-209">To query this property, use the <a href="/windows/desktop/com/ipropertybag-and-ipersistpropertybag"><strong>IPropertyBag</strong></a> interface.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="b942c-210">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b942c-210">Remarks</span></span>

<span data-ttu-id="b942c-211">Die vom Windows Media Video 9-Decoder maximal zulässige Auflösung ist 4096x4096.</span><span class="sxs-lookup"><span data-stu-id="b942c-211">The maximum resolution allowed by the Windows Media Video 9 decoder is 4096x4096.</span></span>

## <a name="requirements"></a><span data-ttu-id="b942c-212">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b942c-212">Requirements</span></span>



| <span data-ttu-id="b942c-213">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b942c-213">Requirement</span></span> | <span data-ttu-id="b942c-214">Wert</span><span class="sxs-lookup"><span data-stu-id="b942c-214">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b942c-215">Client</span><span class="sxs-lookup"><span data-stu-id="b942c-215">Client</span></span><br/> | <span data-ttu-id="b942c-216">Windows XP, Windows Vista oder Windows 7</span><span class="sxs-lookup"><span data-stu-id="b942c-216">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="b942c-217">Header</span><span class="sxs-lookup"><span data-stu-id="b942c-217">Header</span></span><br/> | <dl> <span data-ttu-id="b942c-218"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b942c-218"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="b942c-219">DLL</span><span class="sxs-lookup"><span data-stu-id="b942c-219">DLL</span></span><br/>    | <dl> <span data-ttu-id="b942c-220"><dt>Wmvdecod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b942c-220"><dt>Wmvdecod.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b942c-221">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b942c-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b942c-222">Codec-Objekte</span><span class="sxs-lookup"><span data-stu-id="b942c-222">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="b942c-223">Codec-Implementierung</span><span class="sxs-lookup"><span data-stu-id="b942c-223">Codec Implementation</span></span>](codecimplementation.md)
</dt> </dl>

 

 
