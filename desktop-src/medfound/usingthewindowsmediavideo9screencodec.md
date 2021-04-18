---
description: Verwenden des Windows Media Video 9-Bildschirm Codecs
ms.assetid: d88d5f5e-0935-4bbe-8abf-72cc536f9b40
title: Verwenden des Windows Media Video 9-Bildschirm Codecs (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b825e053c4c732481c8d1ca5d4dc972f804f262a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106361114"
---
# <a name="using-the-windows-media-video-9-screen-codec-microsoft-media-foundation"></a><span data-ttu-id="8304e-103">Verwenden des Windows Media Video 9-Bildschirm Codecs (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="8304e-103">Using the Windows Media Video 9 Screen Codec (Microsoft Media Foundation)</span></span>

<span data-ttu-id="8304e-104">Der Windows Media Video 9-Bildschirm Codec ist für das Komprimieren von *Anwendungsvideos* optimiert, die aus aufeinander folgenden Bildschirmfotos für die Anzeige eines Computers bestehen.</span><span class="sxs-lookup"><span data-stu-id="8304e-104">The Windows Media Video 9 Screen codec is optimized for compressing *application video*, which consists of consecutive screen shots for a computer display.</span></span> <span data-ttu-id="8304e-105">Der Codec nutzt die typische Einfachheit des Bilds (relativ wenige Farben, viele gerade Linien usw.) und eine relative fehlende Bewegung, um ein sehr hohes Komprimierungs Verhältnis zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="8304e-105">The codec takes advantage of the typical image simplicity (relatively few colors, lots of straight lines, and so on) and relative lack of motion to achieve a very high compression ratio.</span></span> <span data-ttu-id="8304e-106">Der Nachteil dieser Optimierung ist, dass Videos, die nicht den erwarteten Merkmalen von Anwendungsvideos entsprechen, möglicherweise nur schwer mit akzeptabler Qualität komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="8304e-106">The disadvantage of this optimization is that video that doesn't conform to the expected characteristics of application video can be difficult to compress with an acceptable level of quality.</span></span>

<span data-ttu-id="8304e-107">Der Windows Media Video 9-Bildschirm Encoder wird durch den Klassen Bezeichner CLSID \_ CMSSEncMediaObject2 identifiziert, und der Decoder wird als Klassen Bezeichner CLSID \_ cmssdecmediaobject bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8304e-107">The Windows Media Video 9 Screen encoder is identified by the class identifier CLSID\_CMSSEncMediaObject2, and the decoder is identified the class identifier CLSID\_CMSSDecMediaObject.</span></span> <span data-ttu-id="8304e-108">Der FourCC-Wert für Medientypen, die diesen Codec verwenden, ist "MSS2".</span><span class="sxs-lookup"><span data-stu-id="8304e-108">The FOURCC value for media types using this codec is "MSS2".</span></span>

## <a name="configuring-the-encoder"></a><span data-ttu-id="8304e-109">Konfigurieren des Encoders</span><span class="sxs-lookup"><span data-stu-id="8304e-109">Configuring the Encoder</span></span>

<span data-ttu-id="8304e-110">Der Encoder des Windows Media Video 9-Bildschirm Codecs wird auf die gleiche Weise konfiguriert wie der Standard Video Decoder.</span><span class="sxs-lookup"><span data-stu-id="8304e-110">The encoder of the Windows Media Video 9 Screen codec is configured in the same way as the standard video decoder.</span></span>

> [!Note]  
> <span data-ttu-id="8304e-111">Der Bildschirm Encoder unterstützt nur One-Pass-Codierung.</span><span class="sxs-lookup"><span data-stu-id="8304e-111">The screen encoder supports only one-pass encoding.</span></span> <span data-ttu-id="8304e-112">Sie können die Eigenschaft " [ \_ passesused" für "mfpkey](mfpkey-passesusedproperty.md) " auf 2 festlegen und die Eingaben zweimal ohne Fehler verarbeiten. Dies hat jedoch keinen Vorteil.</span><span class="sxs-lookup"><span data-stu-id="8304e-112">You can set the [MFPKEY\_PASSESUSED](mfpkey-passesusedproperty.md) property to 2 and process the inputs twice without error, but there is no benefit to doing so.</span></span> <span data-ttu-id="8304e-113">Dies ist ein bekanntes Problem, das in zukünftigen Versionen möglicherweise korrigiert wird.</span><span class="sxs-lookup"><span data-stu-id="8304e-113">This is a known issue and may be corrected in future releases.</span></span>

 

## <a name="getting-the-best-results"></a><span data-ttu-id="8304e-114">Erzielen der besten Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="8304e-114">Getting the Best Results</span></span>

<span data-ttu-id="8304e-115">Wenn Sie feststellen, dass die Qualität, die Sie in Ihrem Bildschirmaufnahme Inhalt wünschen, eine höhere Bitrate erfordert, als Sie für das Liefer Szenario verwenden können, können Sie die folgenden Techniken ausprobieren, um eine höhere Effizienz vom Codec zu erzielen:</span><span class="sxs-lookup"><span data-stu-id="8304e-115">If you discover that the quality you want in your screen capture content requires a higher bit rate than you can use for your delivery scenario, you can try the following techniques to get more efficiency from the codec:</span></span>

-   <span data-ttu-id="8304e-116">Verwenden Sie eine kleinere Auflösung für die Bildschirmaufnahme.</span><span class="sxs-lookup"><span data-stu-id="8304e-116">Use a smaller resolution for the screen capture.</span></span> <span data-ttu-id="8304e-117">Die Erfassung einer größeren Bildschirmauflösung als erforderlich kann den Viewer durch die Darstellung unnötiger Informationen verwirren.</span><span class="sxs-lookup"><span data-stu-id="8304e-117">Capturing a larger screen resolution than needed can confuse the viewer by presenting unnecessary information.</span></span>
-   <span data-ttu-id="8304e-118">Verwenden Sie eine langsamere Framerate.</span><span class="sxs-lookup"><span data-stu-id="8304e-118">Use a slower frame rate.</span></span> <span data-ttu-id="8304e-119">Bildschirmaufnahmen können häufig zu sehr niedrigen Frameraten (manchmal nur 4 oder 5 Frames pro Sekunde) wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="8304e-119">Screen captures can often be effective at very low frame rates (sometimes as low as 4 or 5 frames per second).</span></span>
-   <span data-ttu-id="8304e-120">Verwenden Sie weniger Grafiken in der Bildschirmaufnahme.</span><span class="sxs-lookup"><span data-stu-id="8304e-120">Use fewer graphics in the screen capture.</span></span> <span data-ttu-id="8304e-121">Der Windows Media Video 9-Bildschirm Codec ist so optimiert, dass Windows-primitive und Text mit hoher Qualität codiert werden.</span><span class="sxs-lookup"><span data-stu-id="8304e-121">The Windows Media Video 9 Screen codec is optimized to encode Windows primitives and text with high quality.</span></span> <span data-ttu-id="8304e-122">In der Regel treten Probleme aufgrund von Bitmapgrafiken auf, die häufig Tausende von einzelnen Farben enthalten.</span><span class="sxs-lookup"><span data-stu-id="8304e-122">Usually problems occur because of bitmapped graphics, which often contain thousands of individual colors.</span></span> <span data-ttu-id="8304e-123">Je weniger Bitmaps bei der Erfassung auf dem Bildschirm angezeigt werden, desto besser sind die Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="8304e-123">The fewer bitmaps that are on the screen when you capture, the better your results will be.</span></span> <span data-ttu-id="8304e-124">Wenn Sie keine Grafiken aus der Bildschirmaufnahme ausschließen können, gibt es mehrere Möglichkeiten, die Auswirkungen einer Bitmap auf die Bildqualität zu minimieren:</span><span class="sxs-lookup"><span data-stu-id="8304e-124">If you cannot eliminate graphics from your screen capture, there are several ways to minimize the impact that a bitmap has on image quality:</span></span>
    -   <span data-ttu-id="8304e-125">Verringern Sie die Größe der Grafik.</span><span class="sxs-lookup"><span data-stu-id="8304e-125">Reduce the size of the graphic.</span></span>
    -   <span data-ttu-id="8304e-126">Reduzieren Sie die Anzahl der einzelnen Grafiken, die gleichzeitig auf dem Bildschirm angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8304e-126">Reduce the number of individual graphics that appear on the screen at the same time.</span></span>
    -   <span data-ttu-id="8304e-127">Reduzieren Sie die Menge der Bewegung der Grafik.</span><span class="sxs-lookup"><span data-stu-id="8304e-127">Reduce the amount of movement of the graphic.</span></span> <span data-ttu-id="8304e-128">Wenn sich die Grafik beispielsweise in einem Fenster befindet, lassen Sie das Fenster so stationär wie möglich.</span><span class="sxs-lookup"><span data-stu-id="8304e-128">For example, if the graphic is in a window, keep the window as stationary as possible.</span></span>
    -   <span data-ttu-id="8304e-129">Bewegen Sie den Mauszeiger nicht über die Grafik, oder ziehen Sie Fenster oder andere Elemente auf die Grafik.</span><span class="sxs-lookup"><span data-stu-id="8304e-129">Avoid moving the mouse pointer over the graphic, or dragging windows or other elements over the graphic.</span></span>

## <a name="decoding"></a><span data-ttu-id="8304e-130">Decodierung</span><span class="sxs-lookup"><span data-stu-id="8304e-130">Decoding</span></span>

<span data-ttu-id="8304e-131">Es gibt keine besonderen Anforderungen für das Decodieren von Bildschirm Erfassungs Videos.</span><span class="sxs-lookup"><span data-stu-id="8304e-131">There are no special requirements for decoding screen capture video.</span></span> <span data-ttu-id="8304e-132">Allerdings kann der Bildschirm Aufzeichnungs Decoder den codierten Inhalt ohne die privaten Codec-Daten nicht ordnungsgemäß decodieren, wie bei allen Windows Media Video 9-Codecs.</span><span class="sxs-lookup"><span data-stu-id="8304e-132">However, as with all Windows Media Video 9 codecs, the screen capture decoder cannot properly decompress the encoded content without the codec private data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8304e-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8304e-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8304e-134">Konfigurieren der Video Codierung</span><span class="sxs-lookup"><span data-stu-id="8304e-134">Configuring Video Encoding</span></span>](configuringvideoencoding.md)
</dt> <dt>

[<span data-ttu-id="8304e-135">Verwenden von privaten Videocodec-Daten</span><span class="sxs-lookup"><span data-stu-id="8304e-135">Using Video Codec Private Data</span></span>](usingvideocodecprivatedata.md)
</dt> <dt>

[<span data-ttu-id="8304e-136">Windows Media Video 9-Bildschirm Encoder</span><span class="sxs-lookup"><span data-stu-id="8304e-136">Windows Media Video 9 Screen Encoder</span></span>](windowsmediavideo9screenencoder.md)
</dt> <dt>

[<span data-ttu-id="8304e-137">Arbeiten mit Videos</span><span class="sxs-lookup"><span data-stu-id="8304e-137">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 



