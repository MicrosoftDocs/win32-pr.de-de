---
description: Der MPEG4 Part 2-Video Decoder decodiert Videostreams, die entsprechend dem MPEG4-Teil 2-Standard codiert wurden.
ms.assetid: 56e32d3c-9bd0-41fe-bb22-e4ff37b7cc5c
title: MPEG-4 Part 2-Video Decoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 777e6144684c799eb58f75afd4811ccc8871a46b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215031"
---
# <a name="mpeg-4-part-2-video-decoder"></a><span data-ttu-id="1dcb5-103">MPEG-4 Part 2-Video Decoder</span><span class="sxs-lookup"><span data-stu-id="1dcb5-103">MPEG-4 Part 2 Video Decoder</span></span>

<span data-ttu-id="1dcb5-104">Der MPEG4 Part 2-Video Decoder decodiert Videostreams, die entsprechend dem MPEG4-Teil 2-Standard codiert wurden.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-104">The MPEG4 Part 2 Video decoder decodes video streams that were encoded according to the MPEG4 Part 2 standard.</span></span>

<span data-ttu-id="1dcb5-105">Sie können eine Instanz des Video-Decoders von MPEG4 Part 2 erstellen, indem Sie **CoCreateInstance** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-105">You can create an instance of the MPEG4 Part 2 Video decoder by calling **CoCreateInstance**.</span></span> <span data-ttu-id="1dcb5-106">Verwenden Sie die Klassen-ID **CLSID \_ CMpeg4sDecMediaObject**, um eine Instanz des Decoders zu erstellen, der sich als DirectX Media Object (DMO) verhält.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-106">To create an instance of the decoder that behaves as a DirectX Media Object (DMO), use the class identifier **CLSID\_CMpeg4sDecMediaObject**.</span></span> <span data-ttu-id="1dcb5-107">Verwenden Sie die Klassen-ID **CLSID \_ CMpeg4sDecMFT**, um eine istance des Decoders zu erstellen, der sich als Media Foundation Transformation (MFT) verhält.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-107">To create an istance of the decoder that behaves as a Media Foundation Transform (MFT), use the class identifier **CLSID\_CMpeg4sDecMFT**.</span></span>

## <a name="input-types"></a><span data-ttu-id="1dcb5-108">Eingabetypen</span><span class="sxs-lookup"><span data-stu-id="1dcb5-108">Input Types</span></span>

<span data-ttu-id="1dcb5-109">Der MPEG4 Part 2-Video Decoder unterstützt die folgenden Eingabemedien Typen.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-109">The MPEG4 Part 2 Video decoder supports the following input media types.</span></span>

-   <span data-ttu-id="1dcb5-110">Mediasubtype \_ M4S2</span><span class="sxs-lookup"><span data-stu-id="1dcb5-110">MEDIASUBTYPE\_M4S2</span></span>
-   <span data-ttu-id="1dcb5-111">Mediasubtype \_ m4s2</span><span class="sxs-lookup"><span data-stu-id="1dcb5-111">MEDIASUBTYPE\_m4s2</span></span>
-   <span data-ttu-id="1dcb5-112">Mediasubtype \_ MP4V</span><span class="sxs-lookup"><span data-stu-id="1dcb5-112">MEDIASUBTYPE\_MP4V</span></span>
-   <span data-ttu-id="1dcb5-113">Mediasubtype \_ MP4V</span><span class="sxs-lookup"><span data-stu-id="1dcb5-113">MEDIASUBTYPE\_mp4v</span></span>
-   <span data-ttu-id="1dcb5-114">Mediasubtype \_ MP4 Bitrate (veraltet)</span><span class="sxs-lookup"><span data-stu-id="1dcb5-114">MEDIASUBTYPE\_MP4S (deprecated)</span></span>
-   <span data-ttu-id="1dcb5-115">Mediasubtype \_ MP4 Bitrate (veraltet)</span><span class="sxs-lookup"><span data-stu-id="1dcb5-115">MEDIASUBTYPE\_mp4s (deprecated)</span></span>

## <a name="output-types"></a><span data-ttu-id="1dcb5-116">Ausgabetypen</span><span class="sxs-lookup"><span data-stu-id="1dcb5-116">Output Types</span></span>

<span data-ttu-id="1dcb5-117">Der MPEG4 Part 2-Video Decoder unterstützt die folgenden Ausgabemedien-Untertypen, wenn er als DMO fungiert.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-117">The MPEG4 Part 2 Video decoder supports the following output media subtypes when it is acting as a DMO.</span></span>

-   <span data-ttu-id="1dcb5-118">Mediasubtype \_ YV12</span><span class="sxs-lookup"><span data-stu-id="1dcb5-118">MEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="1dcb5-119">Mediasubtype \_ NV12</span><span class="sxs-lookup"><span data-stu-id="1dcb5-119">MEDIASUBTYPE\_NV12</span></span>
-   <span data-ttu-id="1dcb5-120">Mediasubtype \_ im YUY2</span><span class="sxs-lookup"><span data-stu-id="1dcb5-120">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="1dcb5-121">mediasubtype \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="1dcb5-121">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="1dcb5-122">mediasubtype \_ yvyu</span><span class="sxs-lookup"><span data-stu-id="1dcb5-122">MEDIASUBTYPE\_YVYU</span></span>
-   <span data-ttu-id="1dcb5-123">Mediasubtype \_ NV11</span><span class="sxs-lookup"><span data-stu-id="1dcb5-123">MEDIASUBTYPE\_NV11</span></span>
-   <span data-ttu-id="1dcb5-124">Mediasubtype \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="1dcb5-124">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="1dcb5-125">Mediasubtype \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="1dcb5-125">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="1dcb5-126">Mediasubtype \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="1dcb5-126">MEDIASUBTYPE\_ RGB565</span></span>
-   <span data-ttu-id="1dcb5-127">Mediasubtype \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="1dcb5-127">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="1dcb5-128">Mediasubtype \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="1dcb5-128">MEDIASUBTYPE\_RGB8</span></span>

<span data-ttu-id="1dcb5-129">Der MPEG4 Part 2-Video Decoder unterstützt die folgenden Ausgabemedien-Untertypen, wenn er als MFT fungiert.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-129">The MPEG4 Part 2 Video decoder supports the following output media subtypes when it is acting as an MFT.</span></span>

-   <span data-ttu-id="1dcb5-130">Mediasubtype \_ NV12</span><span class="sxs-lookup"><span data-stu-id="1dcb5-130">MEDIASUBTYPE\_NV12</span></span>
-   <span data-ttu-id="1dcb5-131">Mediasubtype \_ YV12</span><span class="sxs-lookup"><span data-stu-id="1dcb5-131">MEDIASUBTYPE\_YV12</span></span>

## <a name="formats"></a><span data-ttu-id="1dcb5-132">Formate</span><span class="sxs-lookup"><span data-stu-id="1dcb5-132">Formats</span></span>

<span data-ttu-id="1dcb5-133">Der MPEG4 Part 2-Video Decoder akzeptiert die folgenden Formate.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-133">The MPEG4 Part 2 Video decoder accepts the following formats.</span></span>

-   [<span data-ttu-id="1dcb5-134">**Videoinfoheader**</span><span class="sxs-lookup"><span data-stu-id="1dcb5-134">**VIDEOINFOHEADER**</span></span>](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)
-   <span data-ttu-id="1dcb5-135">[**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (VIH2)</span><span class="sxs-lookup"><span data-stu-id="1dcb5-135">[**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (VIH2)</span></span>
-   [<span data-ttu-id="1dcb5-136">**MF-Info**</span><span class="sxs-lookup"><span data-stu-id="1dcb5-136">**MFVideoInfo**</span></span>](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoinfo)
-   <span data-ttu-id="1dcb5-137">[**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) (nur der VIH2-Teil des Headers wird verwendet.)</span><span class="sxs-lookup"><span data-stu-id="1dcb5-137">[**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) (Only the VIH2 portion of the header is used.)</span></span>

## <a name="interfaces-for-the-dmo"></a><span data-ttu-id="1dcb5-138">Schnittstellen für den DMO</span><span class="sxs-lookup"><span data-stu-id="1dcb5-138">Interfaces for the DMO</span></span>

<span data-ttu-id="1dcb5-139">Wenn Sie eine Instanz des Video-Decoders von MPEG4 Part 2 als DMO erstellen, macht der Decoder die folgenden Schnittstellen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-139">If you create an instance of the MPEG4 Part 2 Video decoder as a DMO, the decoder exposes the following interfaces.</span></span>

-   [<span data-ttu-id="1dcb5-140">**Imediaobject**</span><span class="sxs-lookup"><span data-stu-id="1dcb5-140">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [<span data-ttu-id="1dcb5-141">**Icodecapi**</span><span class="sxs-lookup"><span data-stu-id="1dcb5-141">**ICodecAPI**</span></span>](/windows/win32/api/strmif/nn-strmif-icodecapi)

<span data-ttu-id="1dcb5-142">Sie können eine [**imediaobject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) -Schnittstelle abrufen, indem Sie **CoCreateInstance** aufrufen, und Sie können eine [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Schnittstelle abrufen, indem Sie **QueryInterface** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-142">You can obtain an [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface by calling **CoCreateInstance**, and you can obtain an [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface by calling **QueryInterface**.</span></span>

## <a name="interfaces-for-the-mft"></a><span data-ttu-id="1dcb5-143">Schnittstellen für die MFT</span><span class="sxs-lookup"><span data-stu-id="1dcb5-143">Interfaces for the MFT</span></span>

<span data-ttu-id="1dcb5-144">Wenn Sie eine Instanz des Video-Decoders der Komponente "MPEG2 Part 2" als MFT erstellen, macht der Decoder die folgenden Schnittstellen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-144">If you create an instance of the MPEG2 Part 2 Video decoder as an MFT, the decoder exposes the following interfaces.</span></span>

-   [<span data-ttu-id="1dcb5-145">**IMF-Transformation**</span><span class="sxs-lookup"><span data-stu-id="1dcb5-145">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="1dcb5-146">**Imfattributes**</span><span class="sxs-lookup"><span data-stu-id="1dcb5-146">**IMFAttributes**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [<span data-ttu-id="1dcb5-147">**IMF-Empfehlung**</span><span class="sxs-lookup"><span data-stu-id="1dcb5-147">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [<span data-ttu-id="1dcb5-148">**IMFQualityAdvise2**</span><span class="sxs-lookup"><span data-stu-id="1dcb5-148">**IMFQualityAdvise2**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [<span data-ttu-id="1dcb5-149">**Imfratecontrol**</span><span class="sxs-lookup"><span data-stu-id="1dcb5-149">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [<span data-ttu-id="1dcb5-150">**Imfratesupport**</span><span class="sxs-lookup"><span data-stu-id="1dcb5-150">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)

<span data-ttu-id="1dcb5-151">Sie können einen Zeiger auf die [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle abrufen, indem Sie **CoCreateInstance** aufrufen, und Sie können einen Zeiger auf die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle abrufen, indem Sie [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-151">You can obtain a pointer to the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface by calling **CoCreateInstance**, and you can obtain a pointer to the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface by calling [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes).</span></span> <span data-ttu-id="1dcb5-152">Sie können einen Zeiger auf die [**imfqualityempfehlung**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise) -oder [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2) -Schnittstelle abrufen, indem Sie **QueryInterface** auf der MFT aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-152">You can obtain a pointer to the [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise) or [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2) interface by calling **QueryInterface** on the MFT.</span></span> <span data-ttu-id="1dcb5-153">Sie können einen Zeiger auf die [**imfratecontrol**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) -oder [**imfratesupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) -Schnittstelle abrufen, indem Sie [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) aufrufen und den Dienst-ID **MF- \_ Raten \_ Steuerungs \_ Dienst** übergeben.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-153">You can obtain a pointer to the [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) or [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) interface by calling [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) and passing the service identifier **MF\_RATE\_CONTROL\_SERVICE**.</span></span>

## <a name="profiles-and-levels"></a><span data-ttu-id="1dcb5-154">Profile und Ebenen</span><span class="sxs-lookup"><span data-stu-id="1dcb5-154">Profiles and Levels</span></span>

<span data-ttu-id="1dcb5-155">Die MPEG4-Spezifikation definiert mehrere Profile, von denen jede die Tools angibt, mit denen ein Encoder einen codierten Datenstrom generieren kann.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-155">The MPEG4 specification defines several profiles, each of which specifies the tools that an encoder can use to generate an encoded stream.</span></span> <span data-ttu-id="1dcb5-156">Der MPEG4 part2-Video Decoder unterstützt zwei dieser Profile: einfaches visuelles Profil und erweitertes einfaches Profil.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-156">The MPEG4 Part2 Video Decoder supports two of those profiles: Simple Visual Profile and Advanced Simple Profile.</span></span> <span data-ttu-id="1dcb5-157">Das heißt, der MPEG4 Part 2-Video Decoder kann Datenströme decodieren, die entweder entsprechend dem einfachen visuellen Profil oder dem erweiterten einfachen Profil codiert wurden.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-157">In other words, the MPEG4 Part 2 Video decoder can decode streams that were encoded according to either the Simple Visual Profile or the Advanced Simple Profile.</span></span>

<span data-ttu-id="1dcb5-158">Das einfache visuelle Profil unterstützt die grundlegende Übertragung von Video mit niedriger Bitrate im progressiven Modus.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-158">The Simple Visual Profile supports basic transmission of low bit-rate video in progressive mode.</span></span> <span data-ttu-id="1dcb5-159">Es werden nur interne und Vorhersage Bilder unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-159">It supports only Intra and Prediction pictures.</span></span> <span data-ttu-id="1dcb5-160">Außerdem wird der kurzheader Modus unterstützt, der abwärts mit dem H. 263 Baseline-Profil kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-160">It also supports the short header mode, which is backward compatible with the H.263 baseline profile.</span></span> <span data-ttu-id="1dcb5-161">Ab Windows 10 unterstützt der MPEG-4 Part 2-Video Decoder auch h. 263v2 (h. 263 +), der benutzerdefinierte Bildgrößen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-161">Starting with Windows 10, the MPEG-4 Part 2 Video Decoder also supports H.263v2 (H.263+) which supports custom picture sizes.</span></span>

<span data-ttu-id="1dcb5-162">Das erweiterte einfache Profil unterstützt alle Tools des einfachen visuellen Profils und unterstützt zusätzlich Zeilen Sprung Video, B-Frames, Quarter-PEL-Bewegungskompensation, zusätzliche Quantisierungs Tabellen und globale Bewegungs Kompensierung.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-162">The Advanced Simple Profile supports all the tools of the Simple Visual Profile and, in addition, supports interlaced video, B-frames, quarter-pel motion compensation, additional quantization tables, and global motion compensation.</span></span>

<span data-ttu-id="1dcb5-163">Die MPEG4-Spezifikation definiert auch mehrere Ebenen, von denen jede Einschränkungen für den von einem Encoder generierten Ausgabestream angibt.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-163">The MPEG4 specification also defines several levels, each of which specifies constraints on the output stream generated by an encoder.</span></span>

<span data-ttu-id="1dcb5-164">In der folgenden Tabelle sind die Profile und Ebenen zusammen mit den typischen Lösungen aufgeführt, die vom MPEG4 Part 2-Video Decoder unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-164">The following table shows the profiles and levels, along with typical resolutions, supported by the MPEG4 Part 2 Video decoder.</span></span>



| <span data-ttu-id="1dcb5-165">Profil</span><span class="sxs-lookup"><span data-stu-id="1dcb5-165">Profile</span></span>         | <span data-ttu-id="1dcb5-166">Ebene</span><span class="sxs-lookup"><span data-stu-id="1dcb5-166">Level</span></span> | <span data-ttu-id="1dcb5-167">Typische Lösung</span><span class="sxs-lookup"><span data-stu-id="1dcb5-167">Typical Resolution</span></span> |
|-----------------|-------|--------------------|
| <span data-ttu-id="1dcb5-168">Einfaches visuelles Element</span><span class="sxs-lookup"><span data-stu-id="1dcb5-168">Simple Visual</span></span>   | <span data-ttu-id="1dcb5-169">0</span><span class="sxs-lookup"><span data-stu-id="1dcb5-169">0</span></span>     | <span data-ttu-id="1dcb5-170">176 x 144</span><span class="sxs-lookup"><span data-stu-id="1dcb5-170">176 x 144</span></span>          |
| <span data-ttu-id="1dcb5-171">Einfaches visuelles Element</span><span class="sxs-lookup"><span data-stu-id="1dcb5-171">Simple Visual</span></span>   | <span data-ttu-id="1dcb5-172">1</span><span class="sxs-lookup"><span data-stu-id="1dcb5-172">1</span></span>     | <span data-ttu-id="1dcb5-173">176 x 144</span><span class="sxs-lookup"><span data-stu-id="1dcb5-173">176 x 144</span></span>          |
| <span data-ttu-id="1dcb5-174">Einfaches visuelles Element</span><span class="sxs-lookup"><span data-stu-id="1dcb5-174">Simple Visual</span></span>   | <span data-ttu-id="1dcb5-175">2</span><span class="sxs-lookup"><span data-stu-id="1dcb5-175">2</span></span>     | <span data-ttu-id="1dcb5-176">352 x 288</span><span class="sxs-lookup"><span data-stu-id="1dcb5-176">352 x 288</span></span>          |
| <span data-ttu-id="1dcb5-177">Einfaches visuelles Element</span><span class="sxs-lookup"><span data-stu-id="1dcb5-177">Simple Visual</span></span>   | <span data-ttu-id="1dcb5-178">3</span><span class="sxs-lookup"><span data-stu-id="1dcb5-178">3</span></span>     | <span data-ttu-id="1dcb5-179">352 x 288</span><span class="sxs-lookup"><span data-stu-id="1dcb5-179">352 x 288</span></span>          |
| <span data-ttu-id="1dcb5-180">Simplevisual</span><span class="sxs-lookup"><span data-stu-id="1dcb5-180">SimpleVisual</span></span>    | <span data-ttu-id="1dcb5-181">4a</span><span class="sxs-lookup"><span data-stu-id="1dcb5-181">4a</span></span>    | <span data-ttu-id="1dcb5-182">640 x 480</span><span class="sxs-lookup"><span data-stu-id="1dcb5-182">640 x 480</span></span>          |
| <span data-ttu-id="1dcb5-183">Einfaches visuelles Element</span><span class="sxs-lookup"><span data-stu-id="1dcb5-183">Simple Visual</span></span>   | <span data-ttu-id="1dcb5-184">5</span><span class="sxs-lookup"><span data-stu-id="1dcb5-184">5</span></span>     | <span data-ttu-id="1dcb5-185">720 x 576</span><span class="sxs-lookup"><span data-stu-id="1dcb5-185">720 x 576</span></span>          |
| <span data-ttu-id="1dcb5-186">Erweiterte einfache</span><span class="sxs-lookup"><span data-stu-id="1dcb5-186">Advanced Simple</span></span> | <span data-ttu-id="1dcb5-187">0</span><span class="sxs-lookup"><span data-stu-id="1dcb5-187">0</span></span>     | <span data-ttu-id="1dcb5-188">176 x 144</span><span class="sxs-lookup"><span data-stu-id="1dcb5-188">176 x 144</span></span>          |
| <span data-ttu-id="1dcb5-189">Erweiterte einfache</span><span class="sxs-lookup"><span data-stu-id="1dcb5-189">Advanced Simple</span></span> | <span data-ttu-id="1dcb5-190">1</span><span class="sxs-lookup"><span data-stu-id="1dcb5-190">1</span></span>     | <span data-ttu-id="1dcb5-191">176 x 144</span><span class="sxs-lookup"><span data-stu-id="1dcb5-191">176 x 144</span></span>          |
| <span data-ttu-id="1dcb5-192">Erweiterte einfache</span><span class="sxs-lookup"><span data-stu-id="1dcb5-192">Advanced Simple</span></span> | <span data-ttu-id="1dcb5-193">2</span><span class="sxs-lookup"><span data-stu-id="1dcb5-193">2</span></span>     | <span data-ttu-id="1dcb5-194">352 x 288</span><span class="sxs-lookup"><span data-stu-id="1dcb5-194">352 x 288</span></span>          |
| <span data-ttu-id="1dcb5-195">Erweiterte einfache</span><span class="sxs-lookup"><span data-stu-id="1dcb5-195">Advanced Simple</span></span> | <span data-ttu-id="1dcb5-196">3</span><span class="sxs-lookup"><span data-stu-id="1dcb5-196">3</span></span>     | <span data-ttu-id="1dcb5-197">352 x 288</span><span class="sxs-lookup"><span data-stu-id="1dcb5-197">352 x 288</span></span>          |
| <span data-ttu-id="1dcb5-198">Erweiterte einfache</span><span class="sxs-lookup"><span data-stu-id="1dcb5-198">Advanced Simple</span></span> | <span data-ttu-id="1dcb5-199">3b</span><span class="sxs-lookup"><span data-stu-id="1dcb5-199">3b</span></span>    | <span data-ttu-id="1dcb5-200">352 x 288</span><span class="sxs-lookup"><span data-stu-id="1dcb5-200">352 x 288</span></span>          |
| <span data-ttu-id="1dcb5-201">Erweiterte einfache</span><span class="sxs-lookup"><span data-stu-id="1dcb5-201">Advanced Simple</span></span> | <span data-ttu-id="1dcb5-202">4</span><span class="sxs-lookup"><span data-stu-id="1dcb5-202">4</span></span>     | <span data-ttu-id="1dcb5-203">352 x 756</span><span class="sxs-lookup"><span data-stu-id="1dcb5-203">352 x 756</span></span>          |
| <span data-ttu-id="1dcb5-204">Erweiterte einfache</span><span class="sxs-lookup"><span data-stu-id="1dcb5-204">Advanced Simple</span></span> | <span data-ttu-id="1dcb5-205">5</span><span class="sxs-lookup"><span data-stu-id="1dcb5-205">5</span></span>     | <span data-ttu-id="1dcb5-206">720 x 576</span><span class="sxs-lookup"><span data-stu-id="1dcb5-206">720 x 576</span></span>          |



 

<span data-ttu-id="1dcb5-207">Weitere Informationen zu Profilen und Ebenen finden Sie in der "MPEG4 Part 2"-Spezifikation (ISO/IEC 14496-2): Informationstechnologie-Codieren von audiovisuellen Objekten--Teil 2: Visual.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-207">For more information about profiles and levels, see the MPEG4 Part 2 specification (ISO/IEC 14496-2): Information technology -- Coding of audio-visual objects -- Part 2: Visual.</span></span>

## <a name="decoder-properties"></a><span data-ttu-id="1dcb5-208">Decoder-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1dcb5-208">Decoder Properties</span></span>

<span data-ttu-id="1dcb5-209">Verwenden Sie die [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Schnittstelle oder die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle, um die Eigenschaften des Video-Decoders von MPEG4 Part 2 festzulegen.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-209">To set properties on the MPEG4 Part 2 Video decoder, use the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface or the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="1dcb5-210">Der MPEG4 Part 2-Video Decoder unterstützt die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-210">The MPEG4 Part 2 Video decoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1dcb5-211">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1dcb5-211">Property</span></span></th>
<th><span data-ttu-id="1dcb5-212">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1dcb5-212">Description</span></span></th>
<th><span data-ttu-id="1dcb5-213">Standardwert</span><span class="sxs-lookup"><span data-stu-id="1dcb5-213">Default Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1dcb5-214"><a href="/windows/desktop/DirectShow/avdecvideoswpowerlevel-property"><strong>CODECAPI_AVDecVideoSWPowerLevel</strong></a></span><span class="sxs-lookup"><span data-stu-id="1dcb5-214"><a href="/windows/desktop/DirectShow/avdecvideoswpowerlevel-property"><strong>CODECAPI_AVDecVideoSWPowerLevel</strong></a></span></span></td>
<td><span data-ttu-id="1dcb5-215">Gibt den Energie Stand an.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-215">Specifies the power level.</span></span><br/> <dl> <span data-ttu-id="1dcb5-216">Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-216">Windows 7.</span></span><br />
<span data-ttu-id="1dcb5-217">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-217">Write-only.</span></span><br />
</dl></td>
<td><span data-ttu-id="1dcb5-218">100</span><span class="sxs-lookup"><span data-stu-id="1dcb5-218">100</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1dcb5-219"><a href="/windows/desktop/DirectShow/avdecvideothumbnailgenerationmode-property"><strong>CODECAPI_AVDecVideoThumbnailGenerationMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="1dcb5-219"><a href="/windows/desktop/DirectShow/avdecvideothumbnailgenerationmode-property"><strong>CODECAPI_AVDecVideoThumbnailGenerationMode</strong></a></span></span></td>
<td><span data-ttu-id="1dcb5-220">Gibt den Modus für die Miniatur Generierung an.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-220">Specifies the thumbnail generation mode.</span></span><br/> <dl> <span data-ttu-id="1dcb5-221">Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-221">Windows 7.</span></span><br />
<span data-ttu-id="1dcb5-222">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-222">Write-only.</span></span><br />
</dl></td>
<td><span data-ttu-id="1dcb5-223"><strong>VARIANT_FALSE</strong></span><span class="sxs-lookup"><span data-stu-id="1dcb5-223"><strong>VARIANT_FALSE</strong></span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="1dcb5-224">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1dcb5-224">Remarks</span></span>

<span data-ttu-id="1dcb5-225">Die global eindeutigen Bezeichner (GUIDs) für RGB-Medien Untertypen unterscheiden sich abhängig davon, ob ein Decoder als DMO oder MFT fungiert.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-225">The globally unique identifiers (GUIDs) for RGB media subtypes differ depending on whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="1dcb5-226">Die GUIDs für nicht-RGB-Medien Untertypen sind identisch, unabhängig davon, ob ein Decoder als DMO oder MFT fungiert.</span><span class="sxs-lookup"><span data-stu-id="1dcb5-226">The GUIDs for non-RGB media subtypes are the same, regardless of whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="1dcb5-227">Informationen zu den GUIDs, die Medien Untertypen darstellen, finden Sie unter [Medientypen](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="1dcb5-227">For information about the GUIDs that represent media subtypes, see [Media Types](media-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1dcb5-228">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1dcb5-228">Requirements</span></span>



| <span data-ttu-id="1dcb5-229">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1dcb5-229">Requirement</span></span> | <span data-ttu-id="1dcb5-230">Wert</span><span class="sxs-lookup"><span data-stu-id="1dcb5-230">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1dcb5-231">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1dcb5-231">Minimum supported client</span></span><br/> | <span data-ttu-id="1dcb5-232">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1dcb5-232">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="1dcb5-233">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1dcb5-233">Minimum supported server</span></span><br/> | <span data-ttu-id="1dcb5-234">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1dcb5-234">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1dcb5-235">Header</span><span class="sxs-lookup"><span data-stu-id="1dcb5-235">Header</span></span><br/>                   | <dl> <span data-ttu-id="1dcb5-236"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1dcb5-236"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="1dcb5-237">DLL</span><span class="sxs-lookup"><span data-stu-id="1dcb5-237">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1dcb5-238"><dt>MP4SDecd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1dcb5-238"><dt>MP4SDecd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dcb5-239">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1dcb5-239">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dcb5-240">Codec-Objekte</span><span class="sxs-lookup"><span data-stu-id="1dcb5-240">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
