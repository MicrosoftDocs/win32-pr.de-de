---
description: Der Windows Media Video 9-Bildschirm Decoder decodiert Datenströme, die vom Windows Media Video 9-Bildschirm Encoder codiert wurden.
ms.assetid: 6688a830-7a54-4f58-947e-26013e191b5f
title: Windows Media Video 9-Bildschirm Decoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd9dcdce920fa39437edb769fd575a7d7a0d68fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359364"
---
# <a name="windows-media-video-9-screen-decoder"></a><span data-ttu-id="da9b0-103">Windows Media Video 9-Bildschirm Decoder</span><span class="sxs-lookup"><span data-stu-id="da9b0-103">Windows Media Video 9 Screen Decoder</span></span>

<span data-ttu-id="da9b0-104">Der Windows Media Video 9-Bildschirm Decoder decodiert Datenströme, die vom [**Windows Media Video 9-Bildschirm Encoder**](windowsmediavideo9screenencoder.md)codiert wurden.</span><span class="sxs-lookup"><span data-stu-id="da9b0-104">The Windows Media Video 9 Screen decoder decodes streams that were encoded by the [**Windows Media Video 9 Screen Encoder**](windowsmediavideo9screenencoder.md).</span></span>

## <a name="class-identifier"></a><span data-ttu-id="da9b0-105">Klassen Bezeichner</span><span class="sxs-lookup"><span data-stu-id="da9b0-105">Class Identifier</span></span>

<span data-ttu-id="da9b0-106">Der Klassen Bezeichner (CLSID) für den Windows Media Video 9-Bildschirm Decoder wird durch die Konstante **CLSID \_ cmsscdecmediaobject** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="da9b0-106">The class identifier (CLSID) for the Windows Media Video 9 Screen decoder is represented by the constant **CLSID\_CMSSCDecMediaObject**.</span></span> <span data-ttu-id="da9b0-107">Sie können eine Instanz des Decoders erstellen, indem Sie **CoCreateInstance** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="da9b0-107">You can create an instance of the decoder by calling **CoCreateInstance**.</span></span>

## <a name="input-types"></a><span data-ttu-id="da9b0-108">Eingabetypen</span><span class="sxs-lookup"><span data-stu-id="da9b0-108">Input Types</span></span>

<span data-ttu-id="da9b0-109">Der aus vier Zeichen bestehende Code (FourCC) für Windows Media Video Bildschirm codierten Inhalt der Version 9 ist "MSS2".</span><span class="sxs-lookup"><span data-stu-id="da9b0-109">The four-character code (FOURCC) for Windows Media Video Screen Version 9 encoded content is "MSS2".</span></span>

<span data-ttu-id="da9b0-110">Die folgenden Eingabetypen werden vom Bildschirm Decoder der Version 9 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="da9b0-110">The following input types are supported by the Version 9 Screen decoder.</span></span>

-   <span data-ttu-id="da9b0-111">Mediasubtype \_ MSS2</span><span class="sxs-lookup"><span data-stu-id="da9b0-111">MEDIASUBTYPE\_MSS2</span></span>

## <a name="output-types"></a><span data-ttu-id="da9b0-112">Ausgabetypen</span><span class="sxs-lookup"><span data-stu-id="da9b0-112">Output Types</span></span>

<span data-ttu-id="da9b0-113">Die folgenden Ausgabetypen werden vom Bildschirm Decoder der Version 9 unterstützt, wenn Sie als DirectX-Medienobjekt (DMO) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="da9b0-113">The following output types are supported by the Version 9 Screen decoder when it is being used as a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="da9b0-114">Mediasubtype \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="da9b0-114">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="da9b0-115">Mediasubtype \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="da9b0-115">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="da9b0-116">Mediasubtype \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="da9b0-116">MEDIASUBTYPE\_ARGB32</span></span>
-   <span data-ttu-id="da9b0-117">Mediasubtype \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="da9b0-117">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="da9b0-118">Mediasubtype \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="da9b0-118">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="da9b0-119">Mediasubtype \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="da9b0-119">MEDIASUBTYPE\_RGB8</span></span>

<span data-ttu-id="da9b0-120">Die folgenden Ausgabetypen werden vom Bildschirm Decoder der Version 9 unterstützt, wenn Sie als Media Foundation Transformation (MFT) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="da9b0-120">The following output types are supported by the Version 9 Screen decoder when it is being used as a Media Foundation Transform (MFT).</span></span>

-   <span data-ttu-id="da9b0-121">MF-Format \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="da9b0-121">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="da9b0-122">MF-Format \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="da9b0-122">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="da9b0-123">MF-Format \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="da9b0-123">MFVideoFormat\_ARGB32</span></span>
-   <span data-ttu-id="da9b0-124">MF-Format \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="da9b0-124">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="da9b0-125">MF-Format \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="da9b0-125">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="da9b0-126">MF-Format \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="da9b0-126">MFVideoFormat\_RGB8</span></span>

## <a name="remarks"></a><span data-ttu-id="da9b0-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da9b0-127">Remarks</span></span>

<span data-ttu-id="da9b0-128">Ein Bildschirm Decoder-Objekt macht die [**imediaobject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) -Schnittstelle verfügbar, sodass das Objekt als DirectX-Medienobjekt (DMO) verwendet werden kann, und stellt die [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle zur Verfügung, sodass das Objekt als Media Foundation Transformation (MFT) verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="da9b0-128">A screen decoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="da9b0-129">Ein Bildschirm Decoder verhält sich als DMO oder MFT, je nachdem, welche Schnittstellen Sie erhalten und welche Version von Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="da9b0-129">A screen decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="da9b0-130">In der folgenden Tabelle sind die Bedingungen aufgeführt, unter denen sich ein Bildschirm Decoder als DMO oder MFT verhält.</span><span class="sxs-lookup"><span data-stu-id="da9b0-130">The following table shows the conditions under which a screen decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="da9b0-131">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="da9b0-131">Operating system</span></span>            | <span data-ttu-id="da9b0-132">Decoderverhalten</span><span class="sxs-lookup"><span data-stu-id="da9b0-132">Decoder behavior</span></span>                                                                                                                                                        |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da9b0-133">Windows XP</span><span class="sxs-lookup"><span data-stu-id="da9b0-133">Windows XP</span></span>                  | <span data-ttu-id="da9b0-134">Ein Windows Media-Bildschirm Decoder verhält sich immer als DMO.</span><span class="sxs-lookup"><span data-stu-id="da9b0-134">A Windows Media Screen decoder always behaves as a DMO.</span></span>                                                                                                                 |
| <span data-ttu-id="da9b0-135">Windows Vista und Windows 7</span><span class="sxs-lookup"><span data-stu-id="da9b0-135">Windows Vista and Windows 7</span></span> | <span data-ttu-id="da9b0-136">Standardmäßig verhält sich ein Windows Media-Bildschirm Decoder als DMO.</span><span class="sxs-lookup"><span data-stu-id="da9b0-136">By default, a Windows Media Screen decoder behaves as a DMO.</span></span> <span data-ttu-id="da9b0-137">Wenn Sie eine [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle auf einem Bildschirm Decoder abrufen, verhält sie sich wie eine MFT.</span><span class="sxs-lookup"><span data-stu-id="da9b0-137">If you obtain an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on a screen decoder, it behaves as an MFT.</span></span> |



 

<span data-ttu-id="da9b0-138">Sie können die gleiche CLSID (CLSID \_ cmsscdecmediaobject) verwenden, um den Bildschirm Decoder der Version 7 und den Bildschirm Decoder der Version 9 zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="da9b0-138">You can use the same CLSID (CLSID\_CMSSCDecMediaObject) to create the Version 7 Screen decoder and the Version 9 Screen decoder.</span></span> <span data-ttu-id="da9b0-139">Der FourCC for Windows Media Video Screen Version 7-codierter Inhalt ist "MSS1".</span><span class="sxs-lookup"><span data-stu-id="da9b0-139">The FOURCC for Windows Media Video Screen Version 7 encoded content is "MSS1".</span></span> <span data-ttu-id="da9b0-140">Der Bildschirm Decoder der Version 7 unterstützt den \_ Eingabetyp mediasubtype MSS1.</span><span class="sxs-lookup"><span data-stu-id="da9b0-140">The Version 7 Screen decoder supports the MEDIASUBTYPE\_MSS1 input type.</span></span>

## <a name="requirements"></a><span data-ttu-id="da9b0-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da9b0-141">Requirements</span></span>



| <span data-ttu-id="da9b0-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da9b0-142">Requirement</span></span> | <span data-ttu-id="da9b0-143">Wert</span><span class="sxs-lookup"><span data-stu-id="da9b0-143">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da9b0-144">Client</span><span class="sxs-lookup"><span data-stu-id="da9b0-144">Client</span></span><br/> | <span data-ttu-id="da9b0-145">Windows XP, Windows Vista oder Windows 7</span><span class="sxs-lookup"><span data-stu-id="da9b0-145">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="da9b0-146">Header</span><span class="sxs-lookup"><span data-stu-id="da9b0-146">Header</span></span><br/> | <dl> <span data-ttu-id="da9b0-147"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="da9b0-147"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="da9b0-148">DLL</span><span class="sxs-lookup"><span data-stu-id="da9b0-148">DLL</span></span><br/>    | <dl> <span data-ttu-id="da9b0-149"><dt>Wmvsdecd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da9b0-149"><dt>Wmvsdecd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da9b0-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da9b0-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da9b0-151">Codec-Objekte</span><span class="sxs-lookup"><span data-stu-id="da9b0-151">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="da9b0-152">Codec-Implementierung</span><span class="sxs-lookup"><span data-stu-id="da9b0-152">Codec Implementation</span></span>](codecimplementation.md)
</dt> <dt>

[<span data-ttu-id="da9b0-153">Verwenden des Windows Media Video 9-Bildschirm Codecs</span><span class="sxs-lookup"><span data-stu-id="da9b0-153">Using the Windows Media Video 9 Screen Codec</span></span>](usingthewindowsmediavideo9screencodec.md)
</dt> <dt>

[<span data-ttu-id="da9b0-154">Windows Media Video 9-Bildschirm Encoder</span><span class="sxs-lookup"><span data-stu-id="da9b0-154">Windows Media Video 9 Screen Encoder</span></span>](windowsmediavideo9screenencoder.md)
</dt> </dl>

 

 
