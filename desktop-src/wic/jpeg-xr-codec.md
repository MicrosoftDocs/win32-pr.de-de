---
description: Der Native JPEG-XR-Codec ist über die Windows Imaging Component (WIC) verfügbar. Das JPEG-XR-Format, das der Codec unterstützt, ist für die digitale Fotografie von Consumer und Professional konzipiert.
ms.assetid: CB8D1A5F-B544-462E-8927-F45512CED873
title: JPEG-XR-Codec-Übersicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f32ffa397667b325d4e49eadf4d8ce42d49e8a88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353877"
---
# <a name="jpeg-xr-codec-overview"></a><span data-ttu-id="5848b-104">JPEG-XR-Codec-Übersicht</span><span class="sxs-lookup"><span data-stu-id="5848b-104">JPEG XR Codec Overview</span></span>

<span data-ttu-id="5848b-105">Der Native JPEG-XR-Codec ist über die Windows Imaging Component (WIC) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5848b-105">The native JPEG XR codec is available through the Windows Imaging Component (WIC).</span></span> <span data-ttu-id="5848b-106">Das JPEG-XR-Format, das der Codec unterstützt, ist für die digitale Fotografie von Consumer und Professional konzipiert.</span><span class="sxs-lookup"><span data-stu-id="5848b-106">The JPEG XR format, which the codec supports, is designed for consumer and professional digital photography.</span></span>

<span data-ttu-id="5848b-107">Das JPEG-XR-Format kann bis zu einer doppelten Komprimierungs Effizienz des ursprünglichen JPEG-Formats mit weniger merklichen Komprimierungs Artefakten erzielen.</span><span class="sxs-lookup"><span data-stu-id="5848b-107">The JPEG XR format can achieve up to twice the compression efficiency of the original JPEG format, with less noticeable compression artifacts.</span></span> <span data-ttu-id="5848b-108">Zu den Features von JPEG XR gehören:</span><span class="sxs-lookup"><span data-stu-id="5848b-108">Features of JPEG XR include:</span></span>

-   <span data-ttu-id="5848b-109">Unterstützung für Chrome-, RGB-, CMYK-und n-Channel-Images</span><span class="sxs-lookup"><span data-stu-id="5848b-109">Support for monochrome, RGB, CMYK, and n-channel images</span></span>
-   <span data-ttu-id="5848b-110">ganzzahlige Formate der Länge 8, 16 und 32 Bit</span><span class="sxs-lookup"><span data-stu-id="5848b-110">8-, 16-, and 32-bit integer formats</span></span>
-   <span data-ttu-id="5848b-111">High Dynamic Range, Wide-Gamut-Formate, verwenden von Fixed-Punkt-oder Gleit Komma Farbwerten</span><span class="sxs-lookup"><span data-stu-id="5848b-111">High dynamic range, wide-gamut formats, using fixed point or floating point color values</span></span>
-   <span data-ttu-id="5848b-112">Progressive Decodierung</span><span class="sxs-lookup"><span data-stu-id="5848b-112">Progressive decoding</span></span>
-   <span data-ttu-id="5848b-113">Verlust oder Verlust lose Codierung mithilfe desselben Komprimierungs Algorithmus</span><span class="sxs-lookup"><span data-stu-id="5848b-113">Lossy or lossless encoding using the same compression algorithm</span></span>
-   <span data-ttu-id="5848b-114">Unterstützung für das Decodieren von Interessenbereichen in großen Bildern</span><span class="sxs-lookup"><span data-stu-id="5848b-114">Support for decoding of regions of interest in large images</span></span>

<span data-ttu-id="5848b-115">Das JPEG-XR-Format wird in den folgenden Standarddokumenten definiert:</span><span class="sxs-lookup"><span data-stu-id="5848b-115">The JPEG XR format is defined in the following standards documents:</span></span>

-   <span data-ttu-id="5848b-116">ITU-T t. 832: *Information Technology – JPEG XR Bild Codierungssystem – Bild Codierungs Spezifikation*</span><span class="sxs-lookup"><span data-stu-id="5848b-116">ITU-T T.832: *Information technology – JPEG XR image coding system – Image coding specification*</span></span>
-   <span data-ttu-id="5848b-117">ISO/IEC 29199-2:2010: *Information Technology – JPEG XR Bild Codierungssystem – Teil 2: Bild Codierungs Spezifikation*</span><span class="sxs-lookup"><span data-stu-id="5848b-117">ISO/IEC 29199-2:2010: *Information technology — JPEG XR image coding system — Part 2: Image coding specification*</span></span>

<span data-ttu-id="5848b-118">Der JPEG-XR-Standard basiert größtenteils auf dem [HD-Foto](hdphoto-format-overview.md) Format, es gibt jedoch einige Unterschiede zwischen den beiden Formaten.</span><span class="sxs-lookup"><span data-stu-id="5848b-118">The JPEG XR standard is largely based on the [HD Photo](hdphoto-format-overview.md) format, but there are some differences between the two formats.</span></span> <span data-ttu-id="5848b-119">In Windows 8 wurde der HD-fotocodec aktualisiert, um JPEG XR zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5848b-119">In Windows 8, the HD Photo codec has been updated to support JPEG XR.</span></span> <span data-ttu-id="5848b-120">Der Encoder gibt jetzt immer einen mit JPEG XR – kompatiblen Bitstream aus.</span><span class="sxs-lookup"><span data-stu-id="5848b-120">The encoder now always outputs a JPEG XR–compliant bit stream.</span></span> <span data-ttu-id="5848b-121">Der Decoder kann sowohl JPEG XR-als auch HD-Foto Bilder decodieren.</span><span class="sxs-lookup"><span data-stu-id="5848b-121">The decoder can decode both JPEG XR and HD Photo images.</span></span>

<span data-ttu-id="5848b-122">Im Zusammenhang mit dem HD-fotocodec wurden erhebliche Leistungsverbesserungen für den JPEG-XR-Codec vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="5848b-122">Substantial performance improvements, in relation to the HD Photo codec, have been made to the JPEG XR codec.</span></span> <span data-ttu-id="5848b-123">Beispielsweise wurde die Bild Decodierung untergeordneter Auflösung, wie z. b. die Generierung von Miniaturansichten, verbessert, ebenso wie das Decodieren von Bildern mit geringer Auflösung.</span><span class="sxs-lookup"><span data-stu-id="5848b-123">For example, sub-resolution image decoding, such as thumbnail generation, has been improved, as well as low-resolution image decoding.</span></span> <span data-ttu-id="5848b-124">Es wird empfohlen, dass Sie das JPEG-XR-Format anstelle des HD-Foto Formats verwenden.</span><span class="sxs-lookup"><span data-stu-id="5848b-124">It is recommended that you use the JPEG XR format instead of the HD Photo format.</span></span>

## <a name="codec-information"></a><span data-ttu-id="5848b-125">Codec-Informationen</span><span class="sxs-lookup"><span data-stu-id="5848b-125">Codec Information</span></span>



|                     |                                                                         |
|---------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="5848b-126">Dateinamenerweiterung</span><span class="sxs-lookup"><span data-stu-id="5848b-126">File name extension</span></span> | <span data-ttu-id="5848b-127">"jxr" und "WDP"</span><span class="sxs-lookup"><span data-stu-id="5848b-127">"jxr" and "wdp"</span></span>                                                         |
| <span data-ttu-id="5848b-128">Container-GUID</span><span class="sxs-lookup"><span data-stu-id="5848b-128">Container GUID</span></span>      | <span data-ttu-id="5848b-129">**GUID \_ containerformatwmp**</span><span class="sxs-lookup"><span data-stu-id="5848b-129">**GUID\_ContainerFormatWmp**</span></span>                                            |
| <span data-ttu-id="5848b-130">Decoderguid</span><span class="sxs-lookup"><span data-stu-id="5848b-130">Decoder GUID</span></span>        | <span data-ttu-id="5848b-131">**CLSID \_ wicwmpdecoder**</span><span class="sxs-lookup"><span data-stu-id="5848b-131">**CLSID\_WICWmpDecoder**</span></span>                                                |
| <span data-ttu-id="5848b-132">Encoder-GUID</span><span class="sxs-lookup"><span data-stu-id="5848b-132">Encoder GUID</span></span>        | <span data-ttu-id="5848b-133">**CLSID \_ wicwmpencoder**</span><span class="sxs-lookup"><span data-stu-id="5848b-133">**CLSID\_WICWmpEncoder**</span></span>                                                |
| <span data-ttu-id="5848b-134">Profil Unterstützung</span><span class="sxs-lookup"><span data-stu-id="5848b-134">Profile Support</span></span>     | <span data-ttu-id="5848b-135">Der Encoder und der Decoder unterstützen bis zu Hauptprofil und bis zu Ebene 128.</span><span class="sxs-lookup"><span data-stu-id="5848b-135">The encoder and decoder support up to Main Profile and up to level 128.</span></span> |



 

## <a name="codec-features"></a><span data-ttu-id="5848b-136">Codec-Features</span><span class="sxs-lookup"><span data-stu-id="5848b-136">Codec Features</span></span>

### <a name="high-dynamic-range"></a><span data-ttu-id="5848b-137">Hoher dynamischer Bereich</span><span class="sxs-lookup"><span data-stu-id="5848b-137">High Dynamic Range</span></span>

<span data-ttu-id="5848b-138">JPEG XR unterstützt Bilder mit hohem dynamischen Bereich unter Verwendung von Gleit Komma-oder fester Punktfarben.</span><span class="sxs-lookup"><span data-stu-id="5848b-138">JPEG XR supports high-dynamic range images, using floating-point or fixed-point colors.</span></span> <span data-ttu-id="5848b-139">In diesen Farbformaten ist der numerische Bereich eines Pixels größer als der sichtbare Bereich, sodass Sie die Farben während der zwischen Verarbeitungsphasen oberhalb oder unterhalb des sichtbaren Bereichs anpassen können.</span><span class="sxs-lookup"><span data-stu-id="5848b-139">In these color formats, the numerical range of a pixel is larger than the visible range, so you can adjust colors above or below the visible range during intermediate processing stages.</span></span>

-   <span data-ttu-id="5848b-140">Fester Punkt: in einer Darstellung mit einem bestimmten Punkt steht 0 für schwarz und 1,0 für die maximale Sättigung.</span><span class="sxs-lookup"><span data-stu-id="5848b-140">Fixed-point: In a fixed-point representation, 0 represents black and 1.0 represents maximum saturation.</span></span> <span data-ttu-id="5848b-141">Der JPEG-XR-Codec unterstützt sowohl das 16-Bit-als auch das 32-Bit-Format mit fester Punkt</span><span class="sxs-lookup"><span data-stu-id="5848b-141">The JPEG XR codec supports both 16-bit and 32-bit fixed-point formats.</span></span> <span data-ttu-id="5848b-142">Für 16-Bit, 1,0 = 0x2000h, das 13 Bits für den sichtbaren Bereich \[ 0... 1 ergibt \] .</span><span class="sxs-lookup"><span data-stu-id="5848b-142">For 16-bit, 1.0 = 0x2000h, which gives 13 bits for the visible range \[0...1\].</span></span> <span data-ttu-id="5848b-143">Der Gesamtbereich liegt zwischen – 4,0 und + 3,999 und wird linear zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="5848b-143">The total range is –4.0 to +3.999, and is mapped linearly.</span></span> <span data-ttu-id="5848b-144">Bei 32-Bit, 1,0 = 0x01000000h beträgt der sichtbare Bereich 24 Bits, und der Gesamtbereich ist – 128 bis + 127,999.</span><span class="sxs-lookup"><span data-stu-id="5848b-144">For 32-bit, 1.0 = 0x01000000h, the visible range is 24 bits, and the total range is –128 to +127.999.</span></span>
-   <span data-ttu-id="5848b-145">Gleit Komma: in einer Gleit Komma Darstellung steht 0 für schwarz und 1,0 für die maximale Sättigung.</span><span class="sxs-lookup"><span data-stu-id="5848b-145">Floating-point: In a floating-point representation, 0 represents black and 1.0 represents maximum saturation.</span></span> <span data-ttu-id="5848b-146">Der JPEG-XR-Codec unterstützt sowohl das 16-Bit-als auch das 32-Bit-Gleit Komma Format.</span><span class="sxs-lookup"><span data-stu-id="5848b-146">The JPEG XR codec supports both 16-bit and 32-bit floating-point formats.</span></span>

### <a name="tiles"></a><span data-ttu-id="5848b-147">Kacheln</span><span class="sxs-lookup"><span data-stu-id="5848b-147">Tiles</span></span>

<span data-ttu-id="5848b-148">Ein Frame kann in rechteckige Unterbereiche partitioniert werden, die als *Kacheln* bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="5848b-148">A frame can be partitioned into rectangular subregions called *tiles*.</span></span> <span data-ttu-id="5848b-149">Eine Kachel ist ein Bereich eines Bilds, das rechteckige Arrays von Makroblocks enthält.</span><span class="sxs-lookup"><span data-stu-id="5848b-149">A tile is an area of a image that contains rectangular arrays of macroblocks.</span></span> <span data-ttu-id="5848b-150">Durch Kacheln können Bereiche des Bilds decodiert werden, ohne dass das gesamte Bild verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="5848b-150">Tiles enable regions of the image to be decoded without processing the entire image.</span></span>

<span data-ttu-id="5848b-151">Wählen Sie während der Codierung die Anzahl der Kacheln aus, indem Sie die Eigenschaften " **horizontaltileslices** " und " **verticaltileslices** " festlegen.</span><span class="sxs-lookup"><span data-stu-id="5848b-151">During encoding, select the number of tiles by setting the **HorizontalTileSlices** and **VerticalTileSlices** properties.</span></span> <span data-ttu-id="5848b-152">Die minimale Kachel Größe beträgt 16 × 16 Pixel.</span><span class="sxs-lookup"><span data-stu-id="5848b-152">The minimum tile size is 16 × 16 pixels.</span></span> <span data-ttu-id="5848b-153">Der Encoder passt die Anzahl der Kacheln an, um diese Einschränkung aufrechtzuerhalten.</span><span class="sxs-lookup"><span data-stu-id="5848b-153">The encoder adjusts the number of tiles to maintain this restriction.</span></span> <span data-ttu-id="5848b-154">Mit jeder Kachel ist Speicher-und Verarbeitungsaufwand verbunden, sodass Sie die Anzahl der Kacheln berücksichtigen sollten, die für bestimmte Szenarien erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="5848b-154">There is storage and processing overhead associated with each tile, so you should consider the number of tiles that are needed for particular scenarios.</span></span>

### <a name="image-stream-output"></a><span data-ttu-id="5848b-155">Bild Datenstrom Ausgabe</span><span class="sxs-lookup"><span data-stu-id="5848b-155">Image Stream Output</span></span>

<span data-ttu-id="5848b-156">Der JPEG-XR-Standard definiert zwei Teile einer JPEG-XR-Datei:</span><span class="sxs-lookup"><span data-stu-id="5848b-156">The JPEG-XR standard defines two parts of a JPEG-XR file:</span></span>

-   <span data-ttu-id="5848b-157">Der bildbit-Stream, der im Text des Standards definiert ist.</span><span class="sxs-lookup"><span data-stu-id="5848b-157">The image bit stream, defined in the body of the standard.</span></span>
-   <span data-ttu-id="5848b-158">Der Bild Container.</span><span class="sxs-lookup"><span data-stu-id="5848b-158">The image container.</span></span> <span data-ttu-id="5848b-159">Die Datei enthält EXIF-und XMP-Metadaten und ist in Anhang A des Standards definiert.</span><span class="sxs-lookup"><span data-stu-id="5848b-159">The file contains Exif and XMP metadata, and is defined in Annex A of the standard.</span></span>

<span data-ttu-id="5848b-160">Es ist möglich und durch den Standard zulässig, den Bildstream in einen anderen Typ von Datei Container einzubetten.</span><span class="sxs-lookup"><span data-stu-id="5848b-160">It is possible, and allowed by the standard, to embed the image stream inside another type of file container.</span></span> <span data-ttu-id="5848b-161">Der Encoder unterstützt einen reinen Streammodus, der den unformatierten bildbit-Datenstrom ohne Bild Container ausgibt.</span><span class="sxs-lookup"><span data-stu-id="5848b-161">The encoder supports a stream-only mode, which outputs the raw image bit stream with no image container.</span></span> <span data-ttu-id="5848b-162">Eine Anwendung kann den Bitstream in einem anderen Containerformat speichern.</span><span class="sxs-lookup"><span data-stu-id="5848b-162">An application can store the bit stream in some other container format.</span></span>

<span data-ttu-id="5848b-163">Legen Sie die **streamonly** -Eigenschaft fest, um den reinen Streammodus zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5848b-163">To enable stream-only mode, set the **StreamOnly** property.</span></span>

### <a name="image-quality-settings"></a><span data-ttu-id="5848b-164">Bild Qualitätseinstellungen</span><span class="sxs-lookup"><span data-stu-id="5848b-164">Image Quality Settings</span></span>

<span data-ttu-id="5848b-165">Mehrere Codec-Eigenschaften steuern die Qualität des Ausgabe Bilds vom Encoder.</span><span class="sxs-lookup"><span data-stu-id="5848b-165">Several codec properties control the quality of the output image from the encoder.</span></span>

-   <span data-ttu-id="5848b-166">[ImageQuality](#imagequality) ist eine Eigenschaft, die von WIC-Codecs gemeinsam ist.</span><span class="sxs-lookup"><span data-stu-id="5848b-166">[ImageQuality](#imagequality) is a property common across WIC codecs.</span></span> <span data-ttu-id="5848b-167">Sie gibt die Bildqualität als einzelnen Gleit Komma Wert von 0,0 – 1.0 an.</span><span class="sxs-lookup"><span data-stu-id="5848b-167">It specifies image quality as a single floating-point value from 0.0–1.0,</span></span>
-   <span data-ttu-id="5848b-168">Die Eigenschaften [Quality](#image-quality-settings), [Überlappung](#overlap)und [Subsampling](#subsampling) haben mehr Kontrolle über die Qualitätseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="5848b-168">The [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties give more control over the quality settings.</span></span>

<span data-ttu-id="5848b-169">Wenn Sie die Eigenschaften [Qualität](#image-quality-settings), [Überlappung](#overlap)und [Unterstichprobe](#subsampling) verwenden möchten, legen Sie die [usecodecoptions](#usecodecoptions) -Eigenschaft auf **Variant \_ true** fest.</span><span class="sxs-lookup"><span data-stu-id="5848b-169">To use the [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties, set the [UseCodecOptions](#usecodecoptions) property to **VARIANT\_TRUE**.</span></span>

<span data-ttu-id="5848b-170">Wenn [usecodecoptions](#usecodecoptions) **Variant \_ false** ist (**Variant \_ false** ist die Standardeinstellung), verwendet der Encoder die [ImageQuality](#imagequality) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="5848b-170">If [UseCodecOptions](#usecodecoptions) is **VARIANT\_FALSE** (**VARIANT\_FALSE** is the default) the encoder uses the [ImageQuality](#imagequality) property.</span></span> <span data-ttu-id="5848b-171">Der Encoder ordnet den Wert von ImageQuality auf [Qualität](#image-quality-settings), [Überlappung](#overlap)und [Unterstichprobe](#subsampling) über eine Nachschlage Tabelle zu.</span><span class="sxs-lookup"><span data-stu-id="5848b-171">The encoder maps the value of ImageQuality to [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) through a lookup table.</span></span>

<span data-ttu-id="5848b-172">Der Encoder unterstützt die **CompressionQuality** -Eigenschaft nicht.</span><span class="sxs-lookup"><span data-stu-id="5848b-172">The encoder does not support the **CompressionQuality** property.</span></span>

### <a name="compressed-domain-transcode"></a><span data-ttu-id="5848b-173">Komprimierter Domänen-transcode</span><span class="sxs-lookup"><span data-stu-id="5848b-173">Compressed Domain Transcode</span></span>

<span data-ttu-id="5848b-174">Der JPEG-XR-Codec kann bestimmte Bild Transformationen ausführen, ohne die komprimierten Daten tatsächlich zu decodieren und neu zu codieren.</span><span class="sxs-lookup"><span data-stu-id="5848b-174">The JPEG XR codec can perform certain image transformations without actually decoding the compressed data and re-encoding it.</span></span> <span data-ttu-id="5848b-175">Komprimierte Domänen Vorgänge sind sehr effizient und vermeiden jeglichen zusätzlichen Qualitätsverlust, der typisch ist, wenn Sie ein Verlust behaftedes Abbilds decodieren und erneut codieren.</span><span class="sxs-lookup"><span data-stu-id="5848b-175">Compressed domain operations are very efficient and avoid any additional quality loss that is typical when you decode and re-encode a lossy-compressed image.</span></span>

<span data-ttu-id="5848b-176">Folgende komprimierte Domänen Vorgänge werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="5848b-176">The following compressed domain operations are supported:</span></span>

-   <span data-ttu-id="5848b-177">Schneiden Sie einen Bereich des Bilds ab.</span><span class="sxs-lookup"><span data-stu-id="5848b-177">Crop a region of the image.</span></span>
-   <span data-ttu-id="5848b-178">Drehen oder Kippen des Bilds.</span><span class="sxs-lookup"><span data-stu-id="5848b-178">Rotate or flip the image.</span></span>
-   <span data-ttu-id="5848b-179">Verwerfen von Häufigkeits Daten zum Erstellen einer kleineren Bilddatei.</span><span class="sxs-lookup"><span data-stu-id="5848b-179">Discard frequency data to create a smaller image file.</span></span>
-   <span data-ttu-id="5848b-180">Ordnen Sie das Bild zwischen räumlicher und Häufigkeits Reihenfolge neu an.</span><span class="sxs-lookup"><span data-stu-id="5848b-180">Reorganize the image between spatial and frequency order.</span></span>

<span data-ttu-id="5848b-181">Der JPEG-XR-Encoder verwendet nach Möglichkeit eine komprimierte Domänen-Transcodierung, wenn das Quell Image ein JPEG-XR-Image ist.</span><span class="sxs-lookup"><span data-stu-id="5848b-181">The JPEG XR encoder uses compressed domain transcoding, if possible, when the source image is a JPEG XR image.</span></span> <span data-ttu-id="5848b-182">Wenn der Encoder einen komprimierten Domänen Vorgang ausführt, ignoriert er die folgenden Codec-Eigenschaften: [alphaquality](#alphaquality), [ImageQuality](#imagequality), [interleavedalpha](#interleavedalpha), [Verlust lose](#lossless)[Überlappung](#overlap)und [Qualität](#image-quality-settings).</span><span class="sxs-lookup"><span data-stu-id="5848b-182">When the encoder performs a compressed domain operation, it ignores the following codec properties: [AlphaQuality](#alphaquality), [ImageQuality](#imagequality), [InterleavedAlpha](#interleavedalpha), [Lossless](#lossless)[Overlap](#overlap), and [Quality](#image-quality-settings).</span></span> <span data-ttu-id="5848b-183">Wenn die Eigenschaften [horizontaltileslices](/windows) und [verticaltileslices](/windows) vorhanden sind, müssen Sie Sie auf 0 (null) festlegen.</span><span class="sxs-lookup"><span data-stu-id="5848b-183">If the [HorizontalTileSlices](/windows) and [VerticalTileSlices](/windows) properties are present, you must set them to zero.</span></span> <span data-ttu-id="5848b-184">Die Kachel Größe eines Bilds kann nicht als Teil eines komprimierten Domänen-transcodes geändert werden.</span><span class="sxs-lookup"><span data-stu-id="5848b-184">You cannot change the tile size of an image as part of a compressed domain transcode.</span></span>

<span data-ttu-id="5848b-185">In der folgenden Liste wird beschrieben, wie die Bild Transformationen durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5848b-185">The follow list describes how to perform the image transformations.</span></span>

-   <span data-ttu-id="5848b-186">Zum Zuschneiden des Bilds legen Sie die gewünschte Region im [**WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) -Parameter der " **Write tesource** "-Methode fest.</span><span class="sxs-lookup"><span data-stu-id="5848b-186">To crop the image, set the desired region in the [**WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) parameter of the **WriteSource** method.</span></span>
-   <span data-ttu-id="5848b-187">Um das Bild zu drehen oder zu kippen, legen Sie die Eigenschaft [BitmapTransform](#bitmaptransform) fest.</span><span class="sxs-lookup"><span data-stu-id="5848b-187">To rotate or flip the image, set the [BitmapTransform](#bitmaptransform) property.</span></span>
-   <span data-ttu-id="5848b-188">Um Häufigkeits Daten im Bild zu verwerfen, legen Sie die [imagedatadiscard](#imagedatadiscard) -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="5848b-188">To discard frequency data in the image, set the [ImageDataDiscard](#imagedatadiscard) property.</span></span> <span data-ttu-id="5848b-189">Legen Sie die Eigenschaft [alphadatadiscard](#alphadatadiscard) fest, um Häufigkeits Daten im Alphakanal zu verwerfen.</span><span class="sxs-lookup"><span data-stu-id="5848b-189">To discard frequency data in the alpha channel, set the [AlphaDataDiscard](#alphadatadiscard) property.</span></span> <span data-ttu-id="5848b-190">Das Verwerfen von Häufigkeits Daten verringert die codierte Dateigröße und kann die Auflösung verringern.</span><span class="sxs-lookup"><span data-stu-id="5848b-190">Discarding frequency data reduces the encoded file size and can reduce the resolution.</span></span>
-   <span data-ttu-id="5848b-191">Um die Image Organisation zwischen Häufigkeit und räumlicher Reihenfolge zu ändern, legen Sie die Eigenschaft [frequencyorder](/windows) fest.</span><span class="sxs-lookup"><span data-stu-id="5848b-191">To change the image organization between frequency and spatial ordering, set the [FrequencyOrdering](/windows) property.</span></span>

<span data-ttu-id="5848b-192">Wenn Sie den komprimierten Domänen Code deaktivieren und erzwingen möchten, dass der Encoder das Image erneut codieren soll, legen Sie [usecodecoptions](#usecodecoptions) auf **Variant \_ true** fest, und legen Sie [compresseddomaintranscode](#compresseddomaintranscode) auf **Variant \_ false** fest.</span><span class="sxs-lookup"><span data-stu-id="5848b-192">To disable compressed domain transcode and force the encoder to re-encode the image, set the [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE** and set [CompressedDomainTranscode](#compresseddomaintranscode) to **VARIANT\_FALSE**.</span></span>

## <a name="encoder-options"></a><span data-ttu-id="5848b-193">Codierungsoptionen</span><span class="sxs-lookup"><span data-stu-id="5848b-193">Encoder Options</span></span>

<span data-ttu-id="5848b-194">Um Codierungs Eigenschaften festzulegen, verwenden Sie die [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5848b-194">To set encoding properties, use the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface.</span></span> <span data-ttu-id="5848b-195">Weitere Informationen finden Sie in der [Übersicht über die Codierung](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="5848b-195">For more information, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="5848b-196">In der folgenden Liste sind die Codierungsoptionen angegeben.</span><span class="sxs-lookup"><span data-stu-id="5848b-196">The following list specifies the encoder options.</span></span>

-   [<span data-ttu-id="5848b-197">Alphadatadiscard</span><span class="sxs-lookup"><span data-stu-id="5848b-197">AlphaDataDiscard</span></span>](#alphadatadiscard)
-   [<span data-ttu-id="5848b-198">Alphaquality</span><span class="sxs-lookup"><span data-stu-id="5848b-198">AlphaQuality</span></span>](#alphaquality)
-   [<span data-ttu-id="5848b-199">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="5848b-199">BitmapTransform</span></span>](#bitmaptransform)
-   [<span data-ttu-id="5848b-200">Compresseddomaintranscode</span><span class="sxs-lookup"><span data-stu-id="5848b-200">CompressedDomainTranscode</span></span>](#compresseddomaintranscode)
-   [<span data-ttu-id="5848b-201">Frequendcyorder</span><span class="sxs-lookup"><span data-stu-id="5848b-201">FrequencyOrder</span></span>](#frequencyorder)
-   [<span data-ttu-id="5848b-202">Horizontaltileslices</span><span class="sxs-lookup"><span data-stu-id="5848b-202">HorizontalTileSlices</span></span>](#horizontaltileslices)
-   [<span data-ttu-id="5848b-203">Ignoreüberschneidung</span><span class="sxs-lookup"><span data-stu-id="5848b-203">IgnoreOverlap</span></span>](#ignoreoverlap)
-   [<span data-ttu-id="5848b-204">Imagedatadiscard</span><span class="sxs-lookup"><span data-stu-id="5848b-204">ImageDataDiscard</span></span>](#imagedatadiscard)
-   [<span data-ttu-id="5848b-205">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="5848b-205">ImageQuality</span></span>](#imagequality)
-   [<span data-ttu-id="5848b-206">Interleavedalpha</span><span class="sxs-lookup"><span data-stu-id="5848b-206">InterleavedAlpha</span></span>](#interleavedalpha)
-   [<span data-ttu-id="5848b-207">Lossless</span><span class="sxs-lookup"><span data-stu-id="5848b-207">Lossless</span></span>](#lossless)
-   [<span data-ttu-id="5848b-208">Überlappen</span><span class="sxs-lookup"><span data-stu-id="5848b-208">Overlap</span></span>](#overlap)
-   [<span data-ttu-id="5848b-209">Progressivemode</span><span class="sxs-lookup"><span data-stu-id="5848b-209">ProgressiveMode</span></span>](#progressivemode)
-   [<span data-ttu-id="5848b-210">Qualität</span><span class="sxs-lookup"><span data-stu-id="5848b-210">Quality</span></span>](#image-quality-settings)
-   [<span data-ttu-id="5848b-211">Streamonly</span><span class="sxs-lookup"><span data-stu-id="5848b-211">StreamOnly</span></span>](#streamonly)
-   [<span data-ttu-id="5848b-212">Unterstichprobe</span><span class="sxs-lookup"><span data-stu-id="5848b-212">Subsampling</span></span>](#subsampling)
-   [<span data-ttu-id="5848b-213">Usecodecoptions</span><span class="sxs-lookup"><span data-stu-id="5848b-213">UseCodecOptions</span></span>](#usecodecoptions)
-   [<span data-ttu-id="5848b-214">Verticaltileslices</span><span class="sxs-lookup"><span data-stu-id="5848b-214">VerticalTileSlices</span></span>](#verticaltileslices)

### <a name="alphadatadiscard"></a><span data-ttu-id="5848b-215">Alphadatadiscard</span><span class="sxs-lookup"><span data-stu-id="5848b-215">AlphaDataDiscard</span></span>

<span data-ttu-id="5848b-216">Legt die Menge der Alpha Frequenzdaten fest, die während eines komprimierten Domänen-transcodes verworfen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5848b-216">Sets the amount of alpha frequency data to discard during a compressed domain transcode.</span></span>



| <span data-ttu-id="5848b-217">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5848b-217">Data type</span></span> | <span data-ttu-id="5848b-218">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5848b-218">VARTYPE</span></span>     | <span data-ttu-id="5848b-219">Range</span><span class="sxs-lookup"><span data-stu-id="5848b-219">Range</span></span> | <span data-ttu-id="5848b-220">Standard</span><span class="sxs-lookup"><span data-stu-id="5848b-220">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="5848b-221">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="5848b-221">**UCHAR**</span></span> | <span data-ttu-id="5848b-222">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="5848b-222">**VT\_UI1**</span></span> | <span data-ttu-id="5848b-223">0 – 4</span><span class="sxs-lookup"><span data-stu-id="5848b-223">0–4</span></span>   | <span data-ttu-id="5848b-224">Keine</span><span class="sxs-lookup"><span data-stu-id="5848b-224">None</span></span>    |



 

<span data-ttu-id="5848b-225">Diese Eigenschaft gilt nur, wenn die [compresseddomaintranscode](#compresseddomaintranscode) -Eigenschaft auf **Variant \_ true** festgelegt ist und das Bild entweder einen planaren Alphakanal oder einen verschachtelten Alphakanal enthält; andernfalls wird es ignoriert.</span><span class="sxs-lookup"><span data-stu-id="5848b-225">This property applies only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE** and the image contains either a planar alpha channel or interleaved alpha channel; otherwise it is ignored.</span></span>

<span data-ttu-id="5848b-226">Bei Bildern, die einen planaren Alphakanal enthalten, sind die folgenden Werte gültig.</span><span class="sxs-lookup"><span data-stu-id="5848b-226">For images that contain a planar alpha channel, the following values are valid.</span></span>



| <span data-ttu-id="5848b-227">Wert</span><span class="sxs-lookup"><span data-stu-id="5848b-227">Value</span></span> | <span data-ttu-id="5848b-228">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5848b-228">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5848b-229">0</span><span class="sxs-lookup"><span data-stu-id="5848b-229">0</span></span>     | <span data-ttu-id="5848b-230">Es werden keine Bildfrequenzdaten verworfen.</span><span class="sxs-lookup"><span data-stu-id="5848b-230">No image frequency data is discarded.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="5848b-231">1</span><span class="sxs-lookup"><span data-stu-id="5848b-231">1</span></span>     | <span data-ttu-id="5848b-232">Die flexbits werden verworfen.</span><span class="sxs-lookup"><span data-stu-id="5848b-232">The flexbits are discarded.</span></span> <span data-ttu-id="5848b-233">Dadurch wird die Qualität des planaren Alphakanals für das transcodierte Bild willkürlich reduziert.</span><span class="sxs-lookup"><span data-stu-id="5848b-233">This arbitrarily reduces the quality of the planar alpha channel for the transcoded image.</span></span> <span data-ttu-id="5848b-234">ohne Änderung der effektiven Auflösung.</span><span class="sxs-lookup"><span data-stu-id="5848b-234">, without a change in the effective resolution.</span></span> <span data-ttu-id="5848b-235">Die genaue Reduzierung der Dateigröße und-Qualität hängt von zahlreichen Faktoren ab und kann nicht genau angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5848b-235">The exact reduction in file size and quality depends on numerous factors and cannot be exactly specified.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="5848b-236">2</span><span class="sxs-lookup"><span data-stu-id="5848b-236">2</span></span>     | <span data-ttu-id="5848b-237">Das Daten Band der Hochpass Frequenz wird verworfen, einschließlich der flexbits.</span><span class="sxs-lookup"><span data-stu-id="5848b-237">The high-pass frequency data band is discarded, including the flexbits.</span></span> <span data-ttu-id="5848b-238">Dadurch wird die Auflösung des planaren Alphakanals um den Faktor 4 in beiden Dimensionen reduziert.</span><span class="sxs-lookup"><span data-stu-id="5848b-238">This effectively reduces the resolution of the planar alpha channel by a factor of 4 in both dimensions.</span></span> <span data-ttu-id="5848b-239">Die tatsächlichen Dimensionen des transcodierten Bilds bleiben unverändert, aber das Bild verliert alle Details in jedem 4 x 4-Block von Alpha-Channel-Pixeln.</span><span class="sxs-lookup"><span data-stu-id="5848b-239">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 4x4 block of alpha-channel pixels.</span></span> <span data-ttu-id="5848b-240">Normalerweise sollten Sie diesen Wert nur festlegen, wenn die [imagedatadiscard](#imagedatadiscard) -Eigenschaft denselben Wert aufweist.</span><span class="sxs-lookup"><span data-stu-id="5848b-240">Typically, you should set this value only when the [ImageDataDiscard](#imagedatadiscard) property has the same value.</span></span>                            |
| <span data-ttu-id="5848b-241">3</span><span class="sxs-lookup"><span data-stu-id="5848b-241">3</span></span>     | <span data-ttu-id="5848b-242">Die Datenbänder "High-Pass" und "Low-Pass Frequency" werden verworfen, einschließlich der "flexbits".</span><span class="sxs-lookup"><span data-stu-id="5848b-242">Both the high-pass and low-pass frequency data bands are discarded, including the flexbits.</span></span> <span data-ttu-id="5848b-243">Dadurch wird die Auflösung des planaren Alphakanals um den Faktor 16 in beiden Dimensionen reduziert.</span><span class="sxs-lookup"><span data-stu-id="5848b-243">This ffectively reduces the resolution of the planar alpha channel by a factor of 16 in both dimensions.</span></span> <span data-ttu-id="5848b-244">Die tatsächlichen Dimensionen des transcodierten Bilds bleiben unverändert, aber das Bild verliert alle Details in jedem 16x16-Makroblock von Alpha-Channel-Pixeln.</span><span class="sxs-lookup"><span data-stu-id="5848b-244">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 16x16 macroblock of alpha-channel pixels.</span></span> <span data-ttu-id="5848b-245">Normalerweise sollten Sie diesen Wert nur festlegen, wenn die [imagedatadiscard](#imagedatadiscard) -Eigenschaft denselben Wert aufweist.</span><span class="sxs-lookup"><span data-stu-id="5848b-245">Typically, you should set this value only when the [ImageDataDiscard](#imagedatadiscard) property has the same value.</span></span> |
| <span data-ttu-id="5848b-246">4</span><span class="sxs-lookup"><span data-stu-id="5848b-246">4</span></span>     | <span data-ttu-id="5848b-247">Der Alphakanal wird vollständig verworfen.</span><span class="sxs-lookup"><span data-stu-id="5848b-247">The alpha channel is completely discarded.</span></span> <span data-ttu-id="5848b-248">Das Pixel Format des transcodierten Bilds wird geändert, um das Entfernen des Alphakanals widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="5848b-248">The pixel format of the transcoded image is changed to reflect the removal of the alpha channel.</span></span>                                                                                                                                                                                                                                                                                                                                |



 

<span data-ttu-id="5848b-249">Bei Bildern, die einen verschachtelten Alphakanal enthalten, ist der folgende Wert gültig.</span><span class="sxs-lookup"><span data-stu-id="5848b-249">For images that contain an interleaved alpha channel, the following value is valid.</span></span>



| <span data-ttu-id="5848b-250">Wert</span><span class="sxs-lookup"><span data-stu-id="5848b-250">Value</span></span> | <span data-ttu-id="5848b-251">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5848b-251">Description</span></span>                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5848b-252">4</span><span class="sxs-lookup"><span data-stu-id="5848b-252">4</span></span>     | <span data-ttu-id="5848b-253">Der Alphakanal wird vollständig verworfen.</span><span class="sxs-lookup"><span data-stu-id="5848b-253">The alpha channel is completely discarded.</span></span> <span data-ttu-id="5848b-254">Das Pixel Format des transcodierten Bilds wird geändert, um das Entfernen des Alphakanals widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="5848b-254">The pixel format of the transcoded image is changed to reflect the removal of the alpha channel.</span></span> |



 

<span data-ttu-id="5848b-255">Wenn diese Eigenschaft für verschachtelte Alpha Dateien nicht auf 4 festgelegt ist, wird der Alphakanal gemäß dem Wert der [imagedatadiscard](#imagedatadiscard) -Eigenschaft genauso wie die Bilddaten verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="5848b-255">For interleaved alpha, unless this property is set to 4, the alpha channel is processed the same as the image data, according to the value of the [ImageDataDiscard](#imagedatadiscard) property.</span></span>

### <a name="alphaquality"></a><span data-ttu-id="5848b-256">Alphaquality</span><span class="sxs-lookup"><span data-stu-id="5848b-256">AlphaQuality</span></span>

<span data-ttu-id="5848b-257">Legt die Komprimierungs Qualität für das Bild des planaren Alphakanals fest.</span><span class="sxs-lookup"><span data-stu-id="5848b-257">Sets the compression quality for the planar alpha channel image.</span></span>



| <span data-ttu-id="5848b-258">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5848b-258">Data type</span></span> | <span data-ttu-id="5848b-259">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5848b-259">VARTYPE</span></span>     | <span data-ttu-id="5848b-260">Range</span><span class="sxs-lookup"><span data-stu-id="5848b-260">Range</span></span> | <span data-ttu-id="5848b-261">Standard</span><span class="sxs-lookup"><span data-stu-id="5848b-261">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="5848b-262">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="5848b-262">**UCHAR**</span></span> | <span data-ttu-id="5848b-263">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="5848b-263">**VT\_UI1**</span></span> | <span data-ttu-id="5848b-264">1 – 255</span><span class="sxs-lookup"><span data-stu-id="5848b-264">1–255</span></span> | <span data-ttu-id="5848b-265">1</span><span class="sxs-lookup"><span data-stu-id="5848b-265">1</span></span>       |



 

<span data-ttu-id="5848b-266">Diese Eigenschaft wird angewendet, wenn das Image einen Alpha-Kanal aufweist und die [interleavedalpha](#interleavedalpha) -Eigenschaft **Variant \_ false** ist.</span><span class="sxs-lookup"><span data-stu-id="5848b-266">This property applies when the image has an alpha channel and the [InterleavedAlpha](#interleavedalpha) property is **VARIANT\_FALSE**.</span></span> <span data-ttu-id="5848b-267">Der Wert 1 gibt den Modus ohne Verlust an.</span><span class="sxs-lookup"><span data-stu-id="5848b-267">The value 1 indicates lossless mode.</span></span> <span data-ttu-id="5848b-268">Das Erhöhen der Werte führt zu einem höheren Komprimierungs Verhältnis und einer geringeren Bildqualität.</span><span class="sxs-lookup"><span data-stu-id="5848b-268">Increasing values result in higher compression ratios and lower image quality.</span></span>

### <a name="bitmaptransform"></a><span data-ttu-id="5848b-269">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="5848b-269">BitmapTransform</span></span>

<span data-ttu-id="5848b-270">Gibt an, ob das Bild beim decodierten gedreht oder geflippt wird.</span><span class="sxs-lookup"><span data-stu-id="5848b-270">Specifies whether the image is rotated or flipped when decoded.</span></span>



| <span data-ttu-id="5848b-271">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5848b-271">Data type</span></span> | <span data-ttu-id="5848b-272">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5848b-272">VARTYPE</span></span>     | <span data-ttu-id="5848b-273">Range</span><span class="sxs-lookup"><span data-stu-id="5848b-273">Range</span></span>                                                                     | <span data-ttu-id="5848b-274">Standard</span><span class="sxs-lookup"><span data-stu-id="5848b-274">Default</span></span>                       |
|-----------|-------------|---------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="5848b-275">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="5848b-275">**UCHAR**</span></span> | <span data-ttu-id="5848b-276">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="5848b-276">**VT\_UI1**</span></span> | [<span data-ttu-id="5848b-277">**WICBitmapTransformOptions**</span><span class="sxs-lookup"><span data-stu-id="5848b-277">**WICBitmapTransformOptions**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | <span data-ttu-id="5848b-278">**WICBitmapTransformRotate0**</span><span class="sxs-lookup"><span data-stu-id="5848b-278">**WICBitmapTransformRotate0**</span></span> |



 

### <a name="compresseddomaintranscode"></a><span data-ttu-id="5848b-279">Compresseddomaintranscode</span><span class="sxs-lookup"><span data-stu-id="5848b-279">CompressedDomainTranscode</span></span>

<span data-ttu-id="5848b-280">Aktiviert oder deaktiviert die komprimierte Domänen übergreifende Transcodierung.</span><span class="sxs-lookup"><span data-stu-id="5848b-280">Enables or disables compressed domain transcoding.</span></span>



| <span data-ttu-id="5848b-281">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5848b-281">Data type</span></span>         | <span data-ttu-id="5848b-282">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5848b-282">VARTYPE</span></span>      | <span data-ttu-id="5848b-283">Standard</span><span class="sxs-lookup"><span data-stu-id="5848b-283">Default</span></span>           |
|-------------------|--------------|-------------------|
| <span data-ttu-id="5848b-284">**Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="5848b-284">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="5848b-285">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="5848b-285">**VT\_BOOL**</span></span> | <span data-ttu-id="5848b-286">**Variant \_ true**</span><span class="sxs-lookup"><span data-stu-id="5848b-286">**VARIANT\_TRUE**</span></span> |



 

<span data-ttu-id="5848b-287">Wenn Sie komprimierte Domänen Vorgänge deaktivieren möchten, legen Sie diese Eigenschaft auf **Variant \_ false** fest.</span><span class="sxs-lookup"><span data-stu-id="5848b-287">To disable compressed domain operations, set this property to **VARIANT\_FALSE**.</span></span>

### <a name="frequencyorder"></a><span data-ttu-id="5848b-288">Frequendcyorder</span><span class="sxs-lookup"><span data-stu-id="5848b-288">FrequencyOrder</span></span>

<span data-ttu-id="5848b-289">Aktiviert die Codierung in Reihenfolge der Häufigkeit.</span><span class="sxs-lookup"><span data-stu-id="5848b-289">Enables encoding in frequency order.</span></span> <span data-ttu-id="5848b-290">Geräte Implementierungen von JPEG-XR-Encodern können eine Datei in räumlicher Reihenfolge organisieren, um den während der Codierung erforderlichen Speicherplatz zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="5848b-290">Device implementations of JPEG XR encoders can organize a file in spatial order to reduce the memory required during encoding.</span></span>



| <span data-ttu-id="5848b-291">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5848b-291">Data type</span></span>         | <span data-ttu-id="5848b-292">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5848b-292">VARTYPE</span></span>      | <span data-ttu-id="5848b-293">Standard</span><span class="sxs-lookup"><span data-stu-id="5848b-293">Default</span></span>           |
|-------------------|--------------|-------------------|
| <span data-ttu-id="5848b-294">**Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="5848b-294">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="5848b-295">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="5848b-295">**VT\_BOOL**</span></span> | <span data-ttu-id="5848b-296">**Variant \_ true**</span><span class="sxs-lookup"><span data-stu-id="5848b-296">**VARIANT\_TRUE**</span></span> |



 

-   <span data-ttu-id="5848b-297">**Variant \_ TRUE**: Häufigkeit der Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="5848b-297">**VARIANT\_TRUE**: Frequency order.</span></span> <span data-ttu-id="5848b-298">Die niedrigsten Häufigkeits Daten werden zuerst in der Datei angezeigt, und der Bildinhalt wird anhand seiner Häufigkeit und nicht anhand seiner räumlichen Ausrichtung gruppiert.</span><span class="sxs-lookup"><span data-stu-id="5848b-298">The lowest frequency data appears first in the file, and image content is grouped by its frequency rather than its spatial orientation.</span></span> <span data-ttu-id="5848b-299">Das Organisieren einer Datei nach Reihenfolge der Reihenfolge bietet die beste Leistung für jede Häufigkeits basierte Decodierung.</span><span class="sxs-lookup"><span data-stu-id="5848b-299">Organizing a file by frequency order provides the best performance for any frequency-based decoding.</span></span>
-   <span data-ttu-id="5848b-300">**Variant \_ FALSE**: räumliche Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="5848b-300">**VARIANT\_FALSE**: Spatial order.</span></span> <span data-ttu-id="5848b-301">Räumliche Reihenfolge reduziert den während der Codierung erforderlichen Speicherplatz</span><span class="sxs-lookup"><span data-stu-id="5848b-301">Spatial order reduces the memory required during encoding</span></span>

<span data-ttu-id="5848b-302">Die Reihenfolge der Häufigkeit wird empfohlen, es sei denn, Sie haben Leistungs-oder anwendungsspezifische Gründe für die räumliche Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="5848b-302">Frequency order is recommended unless you have performance or application-specific reasons to use spatial order.</span></span>

### <a name="horizontaltileslices"></a><span data-ttu-id="5848b-303">Horizontaltileslices</span><span class="sxs-lookup"><span data-stu-id="5848b-303">HorizontalTileSlices</span></span>

<span data-ttu-id="5848b-304">Legt die Anzahl horizontaler Kacheln fest.</span><span class="sxs-lookup"><span data-stu-id="5848b-304">Sets the number of horizontal tiles.</span></span>



| <span data-ttu-id="5848b-305">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5848b-305">Data type</span></span>  | <span data-ttu-id="5848b-306">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5848b-306">VARTYPE</span></span>     | <span data-ttu-id="5848b-307">Range</span><span class="sxs-lookup"><span data-stu-id="5848b-307">Range</span></span>  | <span data-ttu-id="5848b-308">Standard</span><span class="sxs-lookup"><span data-stu-id="5848b-308">Default</span></span>                      |
|------------|-------------|--------|------------------------------|
| <span data-ttu-id="5848b-309">**USHORT**</span><span class="sxs-lookup"><span data-stu-id="5848b-309">**USHORT**</span></span> | <span data-ttu-id="5848b-310">**VT \_ UI2**</span><span class="sxs-lookup"><span data-stu-id="5848b-310">**VT\_UI2**</span></span> | <span data-ttu-id="5848b-311">0 – 4095</span><span class="sxs-lookup"><span data-stu-id="5848b-311">0–4095</span></span> | <span data-ttu-id="5848b-312">(Bildbreite – 1)  >> 8</span><span class="sxs-lookup"><span data-stu-id="5848b-312">(image width – 1) >> 8</span></span> |



 

<span data-ttu-id="5848b-313">Der Wert ist die Anzahl der horizontalen Unterteilungen. Das heißt, die Anzahl horizontaler Kacheln – 1.</span><span class="sxs-lookup"><span data-stu-id="5848b-313">The value is the number of horizontal subdivisions; that is, the number of horizontal tiles – 1.</span></span>

### <a name="ignoreoverlap"></a><span data-ttu-id="5848b-314">Ignoreüberschneidung</span><span class="sxs-lookup"><span data-stu-id="5848b-314">IgnoreOverlap</span></span>

<span data-ttu-id="5848b-315">Gibt an, wie der Encoder Kachel Grenzen während eines komprimierten Domänen-transcodes behandelt.</span><span class="sxs-lookup"><span data-stu-id="5848b-315">Specifies how the encoder handles tile boundaries during a compressed domain transcode.</span></span>



| <span data-ttu-id="5848b-316">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5848b-316">Data type</span></span>         | <span data-ttu-id="5848b-317">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5848b-317">VARTYPE</span></span>      | <span data-ttu-id="5848b-318">Standard</span><span class="sxs-lookup"><span data-stu-id="5848b-318">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="5848b-319">**Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="5848b-319">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="5848b-320">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="5848b-320">**VT\_BOOL**</span></span> | <span data-ttu-id="5848b-321">**Variant \_ false**</span><span class="sxs-lookup"><span data-stu-id="5848b-321">**VARIANT\_FALSE**</span></span> |



 

<span data-ttu-id="5848b-322">Diese Eigenschaft wird nur angewendet, wenn die [compresseddomaintranscode](#compresseddomaintranscode) -Eigenschaft auf **Variant \_ true** festgelegt ist und ein Teil Regions-transcodieren von genau einer oder mehreren Kacheln ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5848b-322">This property is applied only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE** and a sub-region transcode of exactly one or more tiles is performed.</span></span>

<span data-ttu-id="5848b-323">Der Standard Vorgang für einen Regions-transcodieren besteht darin, den angeforderten Bereich so zu erweitern, dass er die umgebenden Pixel einschließt, die für eine Überlappung der Bereichs Ränder erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="5848b-323">The default operation for a region transcode is to expand the requested region to include the surrounding pixels that are required for overlap decoding of the region edges.</span></span> <span data-ttu-id="5848b-324">Wenn diese Eigenschaft auf **Variant \_ true** festgelegt ist, ignoriert der Codec die umgebenden Pixel, und nur die ausgewählten Kacheln werden extrahiert.</span><span class="sxs-lookup"><span data-stu-id="5848b-324">If this property is set to **VARIANT\_TRUE**, the codec ignores the surrounding pixels, and only the selected tile or tiles are extracted.</span></span> <span data-ttu-id="5848b-325">Wenn das Quellbild nicht gekachelt ist oder die angeforderte Region partielle Kacheln enthält, wird dieser Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="5848b-325">If the source image is not tiled or if the requested region includes partial tiles, this parameter is ignored.</span></span>

### <a name="imagedatadiscard"></a><span data-ttu-id="5848b-326">Imagedatadiscard</span><span class="sxs-lookup"><span data-stu-id="5848b-326">ImageDataDiscard</span></span>

<span data-ttu-id="5848b-327">Legt die Menge der Bildfrequenz Daten fest, die während eines komprimierten Domänen-transcodes verworfen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5848b-327">Sets the amount of image frequency data to discard during a compressed domain transcode.</span></span>



| <span data-ttu-id="5848b-328">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5848b-328">Data type</span></span> | <span data-ttu-id="5848b-329">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5848b-329">VARTYPE</span></span>     | <span data-ttu-id="5848b-330">Range</span><span class="sxs-lookup"><span data-stu-id="5848b-330">Range</span></span> | <span data-ttu-id="5848b-331">Standard</span><span class="sxs-lookup"><span data-stu-id="5848b-331">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="5848b-332">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="5848b-332">**UCHAR**</span></span> | <span data-ttu-id="5848b-333">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="5848b-333">**VT\_UI1**</span></span> | <span data-ttu-id="5848b-334">0 – 3</span><span class="sxs-lookup"><span data-stu-id="5848b-334">0–3</span></span>   | <span data-ttu-id="5848b-335">0</span><span class="sxs-lookup"><span data-stu-id="5848b-335">0</span></span>       |



 

<span data-ttu-id="5848b-336">Diese Eigenschaft gilt nur, wenn die [compresseddomaintranscode](#compresseddomaintranscode) -Eigenschaft auf **Variant \_ true** festgelegt ist; andernfalls wird Sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="5848b-336">This property applies only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE**; otherwise it is ignored.</span></span>



| <span data-ttu-id="5848b-337">Wert</span><span class="sxs-lookup"><span data-stu-id="5848b-337">Value</span></span> | <span data-ttu-id="5848b-338">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5848b-338">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5848b-339">0</span><span class="sxs-lookup"><span data-stu-id="5848b-339">0</span></span>     | <span data-ttu-id="5848b-340">Es werden keine Bildfrequenzdaten verworfen.</span><span class="sxs-lookup"><span data-stu-id="5848b-340">No image frequency data is discarded.</span></span>                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="5848b-341">1</span><span class="sxs-lookup"><span data-stu-id="5848b-341">1</span></span>     | <span data-ttu-id="5848b-342">Die flexbits werden verworfen.</span><span class="sxs-lookup"><span data-stu-id="5848b-342">The flexbits are discarded.</span></span> <span data-ttu-id="5848b-343">Dadurch wird die Qualität des transcodierten Bilds willkürlich reduziert, ohne die effektive Auflösung des Bilds zu ändern.</span><span class="sxs-lookup"><span data-stu-id="5848b-343">This arbitrarily reduces the quality of the transcoded image without changing the effective resolution of the image.</span></span> <span data-ttu-id="5848b-344">Die genaue Reduzierung der Dateigröße und-Qualität hängt von zahlreichen Faktoren ab und kann nicht genau angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5848b-344">The exact reduction in file size and quality depends on numerous factors and cannot be exactly specified.</span></span> <span data-ttu-id="5848b-345">Dieser Wert gibt einen für einen verschachtelten Alphakanal angegebenen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="5848b-345">This value returns an error specified for an interleaved alpha channel.</span></span>                                                                                |
| <span data-ttu-id="5848b-346">2</span><span class="sxs-lookup"><span data-stu-id="5848b-346">2</span></span>     | <span data-ttu-id="5848b-347">Das Daten Band der Hochpass Frequenz wird verworfen, einschließlich der flexbits.</span><span class="sxs-lookup"><span data-stu-id="5848b-347">The high-pass frequency data band is discarded, including the flexbits.</span></span> <span data-ttu-id="5848b-348">Dadurch wird die Auflösung des transcodierten Bilds in beiden Dimensionen um den Faktor 4 reduziert.</span><span class="sxs-lookup"><span data-stu-id="5848b-348">This reduces the resolution of the transcoded image by a factor of 4 in both dimensions.</span></span> <span data-ttu-id="5848b-349">Die tatsächlichen Dimensionen des transcodierten Bilds bleiben unverändert, aber das Bild verliert alle Details in jedem 4 x 4-Block von Pixeln.</span><span class="sxs-lookup"><span data-stu-id="5848b-349">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 4x4 block of pixels.</span></span> <span data-ttu-id="5848b-350">Daher sollte das transcodierte Bild bei jeder decodierte Ausführung entsprechend herabgestuft werden.</span><span class="sxs-lookup"><span data-stu-id="5848b-350">Therefore, the transcoded image should be downsampled accordingly whenever it is decoded.</span></span>                             |
| <span data-ttu-id="5848b-351">3</span><span class="sxs-lookup"><span data-stu-id="5848b-351">3</span></span>     | <span data-ttu-id="5848b-352">Die Datenbänder "High-Pass" und "Low-Pass Frequency" werden verworfen, einschließlich der "flexbits".</span><span class="sxs-lookup"><span data-stu-id="5848b-352">Both the high-pass and low-pass frequency data bands are discarded, including the flexbits.</span></span> <span data-ttu-id="5848b-353">Dadurch wird die Auflösung des transcodierten Bilds mit dem Faktor 16 in beiden Dimensionen reduziert.</span><span class="sxs-lookup"><span data-stu-id="5848b-353">This reduces the resolution of the transcoded image by a factor of 16 in both dimensions.</span></span> <span data-ttu-id="5848b-354">Die tatsächlichen Dimensionen des transcodierten Bilds bleiben unverändert, aber das Bild verliert alle Details in jedem 16x16-Makroblock von Pixeln.</span><span class="sxs-lookup"><span data-stu-id="5848b-354">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 16x16 macroblock of pixels.</span></span> <span data-ttu-id="5848b-355">Daher sollte das transcodierte Bild bei jeder decodierte Ausführung entsprechend herabgestuft werden.</span><span class="sxs-lookup"><span data-stu-id="5848b-355">Therefore, the transcoded image should be downsampled accordingly whenever it is decoded.</span></span> |



 

<span data-ttu-id="5848b-356">Wenn das Image einen verschachtelten Alphakanal enthält, wird der Wert von [imagedatadiscard](#imagedatadiscard) auf den Alphakanal angewendet, es sei denn, die [alphadatadiscard](#alphadatadiscard) -Eigenschaft ist auf 4 festgelegt. in diesem Fall wird der Alphakanal verworfen.</span><span class="sxs-lookup"><span data-stu-id="5848b-356">If the image contains an interleaved alpha channel, the value of [ImageDataDiscard](#imagedatadiscard) is applied to the alpha channel unless the [AlphaDataDiscard](#alphadatadiscard) property is set to 4, in which case the alpha channel is discarded.</span></span>

<span data-ttu-id="5848b-357">Bei planare Alpha werden die verworfenen Häufigkeits Daten durch die [alphadatadiscard](#alphadatadiscard) -Eigenschaft gesteuert.</span><span class="sxs-lookup"><span data-stu-id="5848b-357">For planar alpha, the frequency data that is discarded is controlled by the [AlphaDataDiscard](#alphadatadiscard) property.</span></span>

### <a name="imagequality"></a><span data-ttu-id="5848b-358">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="5848b-358">ImageQuality</span></span>

<span data-ttu-id="5848b-359">Legt die Bildqualität fest.</span><span class="sxs-lookup"><span data-stu-id="5848b-359">Sets the image quality.</span></span>



| <span data-ttu-id="5848b-360">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5848b-360">Data type</span></span> | <span data-ttu-id="5848b-361">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5848b-361">VARTYPE</span></span>    | <span data-ttu-id="5848b-362">Range</span><span class="sxs-lookup"><span data-stu-id="5848b-362">Range</span></span> | <span data-ttu-id="5848b-363">Standard</span><span class="sxs-lookup"><span data-stu-id="5848b-363">Default</span></span> |
|-----------|------------|-------|---------|
| <span data-ttu-id="5848b-364">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="5848b-364">**FLOAT**</span></span> | <span data-ttu-id="5848b-365">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="5848b-365">**VT\_R4**</span></span> | <span data-ttu-id="5848b-366">0 – 1.0</span><span class="sxs-lookup"><span data-stu-id="5848b-366">0–1.0</span></span> | <span data-ttu-id="5848b-367">0.9</span><span class="sxs-lookup"><span data-stu-id="5848b-367">0.9</span></span>     |



 

<span data-ttu-id="5848b-368">Ebene 1,0 bietet eine mathematisch verlustfreie Komprimierung.</span><span class="sxs-lookup"><span data-stu-id="5848b-368">Level 1.0 gives mathematically lossless compression.</span></span>

<span data-ttu-id="5848b-369">Ebene 0,0 ist die Einstellung für die niedrigste Qualität.</span><span class="sxs-lookup"><span data-stu-id="5848b-369">Level 0.0 is the lowest quality setting.</span></span>

### <a name="interleavedalpha"></a><span data-ttu-id="5848b-370">Interleavedalpha</span><span class="sxs-lookup"><span data-stu-id="5848b-370">InterleavedAlpha</span></span>

<span data-ttu-id="5848b-371">Gibt an, ob überlappende Alpha oder planare Alpha codiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5848b-371">Specifies whether to encode interleaved alpha or planar alpha.</span></span>



| <span data-ttu-id="5848b-372">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5848b-372">Data type</span></span>         | <span data-ttu-id="5848b-373">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5848b-373">VARTYPE</span></span>      | <span data-ttu-id="5848b-374">Standard</span><span class="sxs-lookup"><span data-stu-id="5848b-374">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="5848b-375">**Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="5848b-375">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="5848b-376">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="5848b-376">**VT\_BOOL**</span></span> | <span data-ttu-id="5848b-377">**Variant \_ false**</span><span class="sxs-lookup"><span data-stu-id="5848b-377">**VARIANT\_FALSE**</span></span> |



 

-   <span data-ttu-id="5848b-378">**Variant \_ TRUE**: Interleaved alpha.</span><span class="sxs-lookup"><span data-stu-id="5848b-378">**VARIANT\_TRUE**: Interleaved alpha.</span></span> <span data-ttu-id="5848b-379">Alpha Kanalinformationen werden als zusätzlicher überlappenden Kanal codiert, ohne dass eine Korrelation zu den Bildinhalts Kanälen besteht.</span><span class="sxs-lookup"><span data-stu-id="5848b-379">Alpha channel information is encoded as an additional interleaved channel, with no correlation to the image content channels.</span></span> <span data-ttu-id="5848b-380">Dieser Modus ist nützlich für das gleichzeitige Decodieren von Alpha mit dem Bild beim Streaming des Bilds.</span><span class="sxs-lookup"><span data-stu-id="5848b-380">This mode is useful for decoding alpha simultaneously with the image when the image is streaming.</span></span>
-   <span data-ttu-id="5848b-381">Variant \_ false: Planar alpha.</span><span class="sxs-lookup"><span data-stu-id="5848b-381">VARIANT\_FALSE: Planar alpha.</span></span> <span data-ttu-id="5848b-382">Ein planarer Alphakanal wird als separates Bild codiert.</span><span class="sxs-lookup"><span data-stu-id="5848b-382">A planar alpha channel is encoded as a separate image.</span></span> <span data-ttu-id="5848b-383">Die Bilddaten und der Alphakanal werden unabhängig voneinander decodiert.</span><span class="sxs-lookup"><span data-stu-id="5848b-383">The image data and the alpha channel are decoded independently.</span></span> <span data-ttu-id="5848b-384">Optional können Sie die Qualitätsstufe des Alphakanals festlegen, indem Sie die [alphaquality](#alphaquality) -Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="5848b-384">Optionally, you can set the quality level of the alpha channel by setting the [AlphaQuality](#alphaquality) property.</span></span>

<span data-ttu-id="5848b-385">Das verschachtelte Alpha wird nur für bestimmte RGB-Pixel Formate unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5848b-385">Interleaved alpha is supported only for certain RGB pixel formats.</span></span> <span data-ttu-id="5848b-386">Planar Alpha wird für jedes Bildformat unterstützt, das einen Alphakanal definiert.</span><span class="sxs-lookup"><span data-stu-id="5848b-386">Planar alpha is supported for any image format that defines an alpha channel.</span></span>

### <a name="lossless"></a><span data-ttu-id="5848b-387">Lossless</span><span class="sxs-lookup"><span data-stu-id="5848b-387">Lossless</span></span>

<span data-ttu-id="5848b-388">Ermöglicht die Komprimierung von Verlusten.</span><span class="sxs-lookup"><span data-stu-id="5848b-388">Enables losses compression.</span></span>



| <span data-ttu-id="5848b-389">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5848b-389">Data type</span></span>         | <span data-ttu-id="5848b-390">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5848b-390">VARTYPE</span></span>      | <span data-ttu-id="5848b-391">Standard</span><span class="sxs-lookup"><span data-stu-id="5848b-391">Default</span></span>        |
|-------------------|--------------|----------------|
| <span data-ttu-id="5848b-392">**Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="5848b-392">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="5848b-393">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="5848b-393">**VT\_BOOL**</span></span> | <span data-ttu-id="5848b-394">Variant \_ false</span><span class="sxs-lookup"><span data-stu-id="5848b-394">VARIANT\_FALSE</span></span> |



 

<span data-ttu-id="5848b-395">Wenn der Wert **Variant \_ true** ist, verwendet der Encoder die Verlust lose Komprimierung.</span><span class="sxs-lookup"><span data-stu-id="5848b-395">If the value is **VARIANT\_TRUE**, the encoder uses lossless compression.</span></span> <span data-ttu-id="5848b-396">Wenn diese Eigenschaft auf **Variant \_ true** festgelegt ist, überschreibt diese Eigenschaft die [ImageQuality](#imagequality) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="5848b-396">When set to **VARIANT\_TRUE**, this property overrides the [ImageQuality](#imagequality) property.</span></span>

### <a name="overlap"></a><span data-ttu-id="5848b-397">Überlappung</span><span class="sxs-lookup"><span data-stu-id="5848b-397">Overlap</span></span>

<span data-ttu-id="5848b-398">Legt die Ebene der Überlappungs Filterung fest.</span><span class="sxs-lookup"><span data-stu-id="5848b-398">Sets the level of overlap filtering.</span></span> <span data-ttu-id="5848b-399">Mit Überlappungs Filterung werden Transformations Koeffizienten über Block-und Makroblock Grenzen hinweg angewendet.</span><span class="sxs-lookup"><span data-stu-id="5848b-399">With overlap filtering, transform coefficients are applied across block and macroblock boundaries.</span></span> <span data-ttu-id="5848b-400">Dadurch können blockierende Artefakte reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="5848b-400">This can reduce blocking artifacts.</span></span>



| <span data-ttu-id="5848b-401">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5848b-401">Data type</span></span> | <span data-ttu-id="5848b-402">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5848b-402">VARTYPE</span></span>     | <span data-ttu-id="5848b-403">Range</span><span class="sxs-lookup"><span data-stu-id="5848b-403">Range</span></span> | <span data-ttu-id="5848b-404">Standard</span><span class="sxs-lookup"><span data-stu-id="5848b-404">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="5848b-405">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="5848b-405">**UCHAR**</span></span> | <span data-ttu-id="5848b-406">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="5848b-406">**VT\_UI1**</span></span> | <span data-ttu-id="5848b-407">0 – 4</span><span class="sxs-lookup"><span data-stu-id="5848b-407">0–4</span></span>   | <span data-ttu-id="5848b-408">1</span><span class="sxs-lookup"><span data-stu-id="5848b-408">1</span></span>       |



 



| <span data-ttu-id="5848b-409">Wert</span><span class="sxs-lookup"><span data-stu-id="5848b-409">Value</span></span> | <span data-ttu-id="5848b-410">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5848b-410">Description</span></span>                                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="5848b-411">0</span><span class="sxs-lookup"><span data-stu-id="5848b-411">0</span></span>     | <span data-ttu-id="5848b-412">Keine Überlappung.</span><span class="sxs-lookup"><span data-stu-id="5848b-412">No overlap.</span></span>                                   |
| <span data-ttu-id="5848b-413">1</span><span class="sxs-lookup"><span data-stu-id="5848b-413">1</span></span>     | <span data-ttu-id="5848b-414">Eine Überschneidungs Ebene, weiche tiult.</span><span class="sxs-lookup"><span data-stu-id="5848b-414">One level of overlap, soft tiling.</span></span> <span data-ttu-id="5848b-415">(Standardeinstellung)</span><span class="sxs-lookup"><span data-stu-id="5848b-415">(Default.)</span></span> |
| <span data-ttu-id="5848b-416">2</span><span class="sxs-lookup"><span data-stu-id="5848b-416">2</span></span>     | <span data-ttu-id="5848b-417">Zwei überlappende Ebenen, weiche tiult.</span><span class="sxs-lookup"><span data-stu-id="5848b-417">Two levels of overlap, soft tiling.</span></span>           |
| <span data-ttu-id="5848b-418">3</span><span class="sxs-lookup"><span data-stu-id="5848b-418">3</span></span>     | <span data-ttu-id="5848b-419">Eine Überschneidungs Ebene, harte Zeit</span><span class="sxs-lookup"><span data-stu-id="5848b-419">One level of overlap, hard tiling</span></span>             |
| <span data-ttu-id="5848b-420">4</span><span class="sxs-lookup"><span data-stu-id="5848b-420">4</span></span>     | <span data-ttu-id="5848b-421">Zwei Ebenen der Überlappung, Festplatte.</span><span class="sxs-lookup"><span data-stu-id="5848b-421">Two levels of overlap, hard tiling.</span></span>           |



 

<span data-ttu-id="5848b-422">Definitionen:</span><span class="sxs-lookup"><span data-stu-id="5848b-422">Definitions:</span></span>

-   <span data-ttu-id="5848b-423">Eine Überlappungs Ebene: die codierten Werte von 4 x 4-Blöcken werden auf der Grundlage benachbarter Blöcke geändert.</span><span class="sxs-lookup"><span data-stu-id="5848b-423">One level of overlap: The encoded values of 4x4 blocks are modified based on neighboring blocks.</span></span>
-   <span data-ttu-id="5848b-424">Zwei überlappende Ebenen: die erste Überlappungs Ebene wird angewendet.</span><span class="sxs-lookup"><span data-stu-id="5848b-424">Two levels of overlap: The first level of overlap is applied.</span></span> <span data-ttu-id="5848b-425">Außerdem werden die codierten Werte von 16x16-Makro Blöcken basierend auf den benachbarten Macroblocks geändert.</span><span class="sxs-lookup"><span data-stu-id="5848b-425">In addition, the encoded values of 16x16 macroblocks are modified based on the neighboring macroblocks.</span></span>
-   <span data-ttu-id="5848b-426">Soft tiult: überlappende Filterung wird über Kachel Grenzen hinweg angewendet.</span><span class="sxs-lookup"><span data-stu-id="5848b-426">Soft tiling: Overlap filtering is applied across tile boundaries.</span></span>
-   <span data-ttu-id="5848b-427">Harte Zeit: überlappende Filterung wird nicht über Kachel Grenzen hinweg angewendet.</span><span class="sxs-lookup"><span data-stu-id="5848b-427">Hard tiling: Overlap filtering is not applied across tile boundaries.</span></span> <span data-ttu-id="5848b-428">Mit fest Kacheln können einige visuelle Artefakte entlang der Kachel Grenzen eingeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5848b-428">Hard tiles can introduce some visual artifacts along tile boundaries.</span></span>

<span data-ttu-id="5848b-429">Wenn Sie diese Eigenschaft festlegen, legen Sie auch [usecodecoptions](#usecodecoptions) auf **Variant \_ true** fest.</span><span class="sxs-lookup"><span data-stu-id="5848b-429">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="progressivemode"></a><span data-ttu-id="5848b-430">Progressivemode</span><span class="sxs-lookup"><span data-stu-id="5848b-430">ProgressiveMode</span></span>

<span data-ttu-id="5848b-431">Aktiviert oder deaktiviert die Progressive Codierung.</span><span class="sxs-lookup"><span data-stu-id="5848b-431">Enables or disables progressive encoding.</span></span>



| <span data-ttu-id="5848b-432">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5848b-432">Data type</span></span>         | <span data-ttu-id="5848b-433">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5848b-433">VARTYPE</span></span>      | <span data-ttu-id="5848b-434">Standard</span><span class="sxs-lookup"><span data-stu-id="5848b-434">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="5848b-435">**Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="5848b-435">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="5848b-436">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="5848b-436">**VT\_BOOL**</span></span> | <span data-ttu-id="5848b-437">**Variant \_ false**</span><span class="sxs-lookup"><span data-stu-id="5848b-437">**VARIANT\_FALSE**</span></span> |



 



| <span data-ttu-id="5848b-438">Wert</span><span class="sxs-lookup"><span data-stu-id="5848b-438">Value</span></span>              | <span data-ttu-id="5848b-439">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5848b-439">Description</span></span>                |
|--------------------|----------------------------|
| <span data-ttu-id="5848b-440">**Variant \_ true**</span><span class="sxs-lookup"><span data-stu-id="5848b-440">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="5848b-441">Sequenzieller Modus (Standard).</span><span class="sxs-lookup"><span data-stu-id="5848b-441">Sequential mode (default).</span></span> |
| <span data-ttu-id="5848b-442">**Variant \_ false**</span><span class="sxs-lookup"><span data-stu-id="5848b-442">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="5848b-443">Progressiver Modus.</span><span class="sxs-lookup"><span data-stu-id="5848b-443">Progressive mode.</span></span>          |



 

### <a name="quality"></a><span data-ttu-id="5848b-444">Qualität</span><span class="sxs-lookup"><span data-stu-id="5848b-444">Quality</span></span>

<span data-ttu-id="5848b-445">Legt die Komprimierungs Qualität fest.</span><span class="sxs-lookup"><span data-stu-id="5848b-445">Sets the compression quality.</span></span>



| <span data-ttu-id="5848b-446">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5848b-446">Data type</span></span> | <span data-ttu-id="5848b-447">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5848b-447">VARTYPE</span></span>     | <span data-ttu-id="5848b-448">Range</span><span class="sxs-lookup"><span data-stu-id="5848b-448">Range</span></span> | <span data-ttu-id="5848b-449">Standard</span><span class="sxs-lookup"><span data-stu-id="5848b-449">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="5848b-450">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="5848b-450">**UCHAR**</span></span> | <span data-ttu-id="5848b-451">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="5848b-451">**VT\_UI1**</span></span> | <span data-ttu-id="5848b-452">1 – 255</span><span class="sxs-lookup"><span data-stu-id="5848b-452">1–255</span></span> | <span data-ttu-id="5848b-453">1</span><span class="sxs-lookup"><span data-stu-id="5848b-453">1</span></span>       |



 

<span data-ttu-id="5848b-454">Der Wert 1 gibt den Modus ohne Verlust an.</span><span class="sxs-lookup"><span data-stu-id="5848b-454">The value 1 indicates lossless mode.</span></span> <span data-ttu-id="5848b-455">Das Erhöhen der Werte führt zu einem höheren Komprimierungs Verhältnis und einer geringeren Bildqualität.</span><span class="sxs-lookup"><span data-stu-id="5848b-455">Increasing values result in higher compression ratios and lower image quality.</span></span>

<span data-ttu-id="5848b-456">Wenn Sie diese Eigenschaft festlegen, legen Sie auch [usecodecoptions](#usecodecoptions) auf **Variant \_ true** fest.</span><span class="sxs-lookup"><span data-stu-id="5848b-456">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="streamonly"></a><span data-ttu-id="5848b-457">Streamonly</span><span class="sxs-lookup"><span data-stu-id="5848b-457">StreamOnly</span></span>

<span data-ttu-id="5848b-458">Aktiviert oder deaktiviert den reinen Streammodus.</span><span class="sxs-lookup"><span data-stu-id="5848b-458">Enables or disables stream-only mode.</span></span>



| <span data-ttu-id="5848b-459">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5848b-459">Data type</span></span>         | <span data-ttu-id="5848b-460">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5848b-460">VARTYPE</span></span>      | <span data-ttu-id="5848b-461">Standard</span><span class="sxs-lookup"><span data-stu-id="5848b-461">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="5848b-462">**Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="5848b-462">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="5848b-463">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="5848b-463">**VT\_BOOL**</span></span> | <span data-ttu-id="5848b-464">**Variant \_ false**</span><span class="sxs-lookup"><span data-stu-id="5848b-464">**VARIANT\_FALSE**</span></span> |



 



| <span data-ttu-id="5848b-465">Wert</span><span class="sxs-lookup"><span data-stu-id="5848b-465">Value</span></span>              | <span data-ttu-id="5848b-466">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5848b-466">Description</span></span>                                                            |
|--------------------|------------------------------------------------------------------------|
| <span data-ttu-id="5848b-467">**Variant \_ true**</span><span class="sxs-lookup"><span data-stu-id="5848b-467">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="5848b-468">Der Encoder gibt den Rohdaten Strom ohne Metadaten aus.</span><span class="sxs-lookup"><span data-stu-id="5848b-468">The encoder outputs the raw image stream without metadata.</span></span>             |
| <span data-ttu-id="5848b-469">**Variant \_ false**</span><span class="sxs-lookup"><span data-stu-id="5848b-469">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="5848b-470">Der Encoder gibt das Containerformat (Bild Datenstrom und Metadaten) aus.</span><span class="sxs-lookup"><span data-stu-id="5848b-470">The encoder outputs the container format (image stream plus metadata).</span></span> |



 

### <a name="subsampling"></a><span data-ttu-id="5848b-471">Unterstichprobe</span><span class="sxs-lookup"><span data-stu-id="5848b-471">Subsampling</span></span>

<span data-ttu-id="5848b-472">Legt die Chroma-Unterstichprobe fest.</span><span class="sxs-lookup"><span data-stu-id="5848b-472">Sets the chroma subsampling.</span></span> <span data-ttu-id="5848b-473">Diese Eigenschaft gilt nur für RGB-Bilder.</span><span class="sxs-lookup"><span data-stu-id="5848b-473">This property applies only to RGB images.</span></span>



| <span data-ttu-id="5848b-474">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5848b-474">Data type</span></span> | <span data-ttu-id="5848b-475">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5848b-475">VARTYPE</span></span>     | <span data-ttu-id="5848b-476">Range</span><span class="sxs-lookup"><span data-stu-id="5848b-476">Range</span></span> | <span data-ttu-id="5848b-477">Standard</span><span class="sxs-lookup"><span data-stu-id="5848b-477">Default</span></span>                                                  |
|-----------|-------------|-------|----------------------------------------------------------|
| <span data-ttu-id="5848b-478">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="5848b-478">**UCHAR**</span></span> | <span data-ttu-id="5848b-479">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="5848b-479">**VT\_UI1**</span></span> | <span data-ttu-id="5848b-480">0 – 3</span><span class="sxs-lookup"><span data-stu-id="5848b-480">0–3</span></span>   | <span data-ttu-id="5848b-481">3, wenn [ImageQuality](#imagequality) > 0,8; andernfalls 1</span><span class="sxs-lookup"><span data-stu-id="5848b-481">3 if [ImageQuality](#imagequality) > 0.8; otherwise 1</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5848b-482">Wert</span><span class="sxs-lookup"><span data-stu-id="5848b-482">Value</span></span></th>
<th><span data-ttu-id="5848b-483">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5848b-483">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5848b-484">3</span><span class="sxs-lookup"><span data-stu-id="5848b-484">3</span></span></td>
<td><span data-ttu-id="5848b-485">4:4:4-Codierung.</span><span class="sxs-lookup"><span data-stu-id="5848b-485">4:4:4 encoding.</span></span> <span data-ttu-id="5848b-486">Behält die vollständige Chroma-Auflösung bei.</span><span class="sxs-lookup"><span data-stu-id="5848b-486">Preserves full chroma resolution.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5848b-487">2</span><span class="sxs-lookup"><span data-stu-id="5848b-487">2</span></span></td>
<td><span data-ttu-id="5848b-488">4:2:2-Codierung.</span><span class="sxs-lookup"><span data-stu-id="5848b-488">4:2:2 encoding.</span></span> <span data-ttu-id="5848b-489">Die Chroma-Auflösung ist 1/2 der Beleuchtungs Auflösung.</span><span class="sxs-lookup"><span data-stu-id="5848b-489">Chroma resolution is ½ of luminance resolution.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5848b-490">1</span><span class="sxs-lookup"><span data-stu-id="5848b-490">1</span></span></td>
<td><span data-ttu-id="5848b-491">4:2:0-Codierung.</span><span class="sxs-lookup"><span data-stu-id="5848b-491">4:2:0 encoding.</span></span> <span data-ttu-id="5848b-492">Die Chroma-Auflösung ist 1/4 der Beleuchtungs Auflösung.</span><span class="sxs-lookup"><span data-stu-id="5848b-492">Chroma resolution is ¼ of luminance resolution.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5848b-493">0</span><span class="sxs-lookup"><span data-stu-id="5848b-493">0</span></span></td>
<td><span data-ttu-id="5848b-494">4:0:0-Codierung.</span><span class="sxs-lookup"><span data-stu-id="5848b-494">4:0:0 encoding.</span></span> <span data-ttu-id="5848b-495">Verwirft alle Chroma-Werte und behält nur die Leuchtkraft bei.</span><span class="sxs-lookup"><span data-stu-id="5848b-495">Discards all chroma values and preserves luminance only.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="5848b-496">Dieser Modus wird nicht empfohlen, da der Codec eine etwas geänderte Definition der Leuchtkraft verwendet, um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="5848b-496">This mode is not recommended, because the codec uses a slightly modified definition of luminance to improve performance.</span></span> <span data-ttu-id="5848b-497">Stattdessen ist es besser, das Bild vor der Codierung in monochrome zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="5848b-497">Instead, it is better to convert the image to monochrome before encoding.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5848b-498">4:2:2 und 4:2:0 behalten Sie die Details der Leuchtkraft auf der Kosten der Farbdetails bei.</span><span class="sxs-lookup"><span data-stu-id="5848b-498">4:2:2 and 4:2:0 preserve luminance detail at the expense of color detail.</span></span>

<span data-ttu-id="5848b-499">Wenn Sie diese Eigenschaft festlegen, legen Sie auch [usecodecoptions](#usecodecoptions) auf **Variant \_ true** fest.</span><span class="sxs-lookup"><span data-stu-id="5848b-499">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="usecodecoptions"></a><span data-ttu-id="5848b-500">Usecodecoptions</span><span class="sxs-lookup"><span data-stu-id="5848b-500">UseCodecOptions</span></span>

<span data-ttu-id="5848b-501">Gibt an, ob die Eigenschaften [Quality](#image-quality-settings), [Überlappung](#overlap)und [Subsampling](#subsampling) anstelle der generischen [ImageQuality](#imagequality) -Eigenschaft verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5848b-501">Specifies whether to use the [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties instead of the generic [ImageQuality](#imagequality) property.</span></span>



| <span data-ttu-id="5848b-502">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5848b-502">Data type</span></span>         | <span data-ttu-id="5848b-503">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5848b-503">VARTYPE</span></span>      | <span data-ttu-id="5848b-504">Standard</span><span class="sxs-lookup"><span data-stu-id="5848b-504">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="5848b-505">**Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="5848b-505">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="5848b-506">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="5848b-506">**VT\_BOOL**</span></span> | <span data-ttu-id="5848b-507">**Variant \_ false**</span><span class="sxs-lookup"><span data-stu-id="5848b-507">**VARIANT\_FALSE**</span></span> |



 

### <a name="verticaltileslices"></a><span data-ttu-id="5848b-508">Verticaltileslices</span><span class="sxs-lookup"><span data-stu-id="5848b-508">VerticalTileSlices</span></span>

<span data-ttu-id="5848b-509">Legt die Anzahl horizontaler Kacheln fest.</span><span class="sxs-lookup"><span data-stu-id="5848b-509">Sets the number of horizontal tiles.</span></span>



| <span data-ttu-id="5848b-510">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5848b-510">Data type</span></span>  | <span data-ttu-id="5848b-511">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5848b-511">VARTYPE</span></span>     | <span data-ttu-id="5848b-512">Range</span><span class="sxs-lookup"><span data-stu-id="5848b-512">Range</span></span>  | <span data-ttu-id="5848b-513">Standard</span><span class="sxs-lookup"><span data-stu-id="5848b-513">Default</span></span>                       |
|------------|-------------|--------|-------------------------------|
| <span data-ttu-id="5848b-514">**USHORT**</span><span class="sxs-lookup"><span data-stu-id="5848b-514">**USHORT**</span></span> | <span data-ttu-id="5848b-515">**VT \_ UI2**</span><span class="sxs-lookup"><span data-stu-id="5848b-515">**VT\_UI2**</span></span> | <span data-ttu-id="5848b-516">0 – 4095</span><span class="sxs-lookup"><span data-stu-id="5848b-516">0–4095</span></span> | <span data-ttu-id="5848b-517">(Bildhöhe – 1)  >> 8</span><span class="sxs-lookup"><span data-stu-id="5848b-517">(image height – 1) >> 8</span></span> |



 

<span data-ttu-id="5848b-518">Der Wert ist die Anzahl vertikaler Unterteilungen. Das heißt, die Anzahl vertikaler Kacheln – 1.</span><span class="sxs-lookup"><span data-stu-id="5848b-518">The value is the number of vertical subdivisions; that is, the number of vertical tiles – 1.</span></span>

## <a name="supported-color-formats"></a><span data-ttu-id="5848b-519">Unterstützte Farb Formate</span><span class="sxs-lookup"><span data-stu-id="5848b-519">Supported Color Formats</span></span>

<span data-ttu-id="5848b-520">Weitere Informationen zu diesen Formaten finden Sie unter [native Pixel Formats](-wic-codec-native-pixel-formats.md).</span><span class="sxs-lookup"><span data-stu-id="5848b-520">For more information about these formats, see [Native Pixel Formats](-wic-codec-native-pixel-formats.md).</span></span>

-   <span data-ttu-id="5848b-521">**Integer-RGB-Formate**</span><span class="sxs-lookup"><span data-stu-id="5848b-521">**Integer RGB formats**</span></span>
    -   <span data-ttu-id="5848b-522">GUID \_ WICPixelFormat24bppRGB</span><span class="sxs-lookup"><span data-stu-id="5848b-522">GUID\_WICPixelFormat24bppRGB</span></span>
    -   <span data-ttu-id="5848b-523">GUID \_ WICPixelFormat24bppBGR</span><span class="sxs-lookup"><span data-stu-id="5848b-523">GUID\_WICPixelFormat24bppBGR</span></span>
    -   <span data-ttu-id="5848b-524">GUID \_ WICPixelFormat32bppBGR</span><span class="sxs-lookup"><span data-stu-id="5848b-524">GUID\_WICPixelFormat32bppBGR</span></span>
    -   <span data-ttu-id="5848b-525">GUID \_ WICPixelFormat48bppRGB</span><span class="sxs-lookup"><span data-stu-id="5848b-525">GUID\_WICPixelFormat48bppRGB</span></span>
    -   <span data-ttu-id="5848b-526">GUID \_ WICPixelFormat32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="5848b-526">GUID\_WICPixelFormat32bppBGRA</span></span>
    -   <span data-ttu-id="5848b-527">GUID \_ WICPixelFormat64bppRGBA</span><span class="sxs-lookup"><span data-stu-id="5848b-527">GUID\_WICPixelFormat64bppRGBA</span></span>
    -   <span data-ttu-id="5848b-528">GUID \_ WICPixelFormat32bppPBGRA</span><span class="sxs-lookup"><span data-stu-id="5848b-528">GUID\_WICPixelFormat32bppPBGRA</span></span>
    -   <span data-ttu-id="5848b-529">GUID \_ WICPixelFormat64bppPRGBA</span><span class="sxs-lookup"><span data-stu-id="5848b-529">GUID\_WICPixelFormat64bppPRGBA</span></span>
-   <span data-ttu-id="5848b-530">**Einstufige RGB-Formate**</span><span class="sxs-lookup"><span data-stu-id="5848b-530">**Fixed-point RGB formats**</span></span>
    -   <span data-ttu-id="5848b-531">GUID \_ WICPixelFormat48bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="5848b-531">GUID\_WICPixelFormat48bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="5848b-532">GUID \_ WICPixelFormat64bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="5848b-532">GUID\_WICPixelFormat64bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="5848b-533">GUID \_ WICPixelFormat96bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="5848b-533">GUID\_WICPixelFormat96bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="5848b-534">GUID \_ WICPixelFormat128bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="5848b-534">GUID\_WICPixelFormat128bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="5848b-535">GUID \_ WICPixelFormat128bppRGBAFixedPoint</span><span class="sxs-lookup"><span data-stu-id="5848b-535">GUID\_WICPixelFormat128bppRGBAFixedPoint</span></span>
-   <span data-ttu-id="5848b-536">**Gleit Komma-RGB-Formate**</span><span class="sxs-lookup"><span data-stu-id="5848b-536">**Floating-point RGB formats**</span></span>
    -   <span data-ttu-id="5848b-537">GUID \_ WICPixelFormat48bppRGBHalf</span><span class="sxs-lookup"><span data-stu-id="5848b-537">GUID\_WICPixelFormat48bppRGBHalf</span></span>
    -   <span data-ttu-id="5848b-538">GUID \_ WICPixelFormat64bppRGBHalf</span><span class="sxs-lookup"><span data-stu-id="5848b-538">GUID\_WICPixelFormat64bppRGBHalf</span></span>
    -   <span data-ttu-id="5848b-539">GUID \_ WICPixelFormat128bppRGBFloat</span><span class="sxs-lookup"><span data-stu-id="5848b-539">GUID\_WICPixelFormat128bppRGBFloat</span></span>
    -   <span data-ttu-id="5848b-540">GUID \_ WICPixelFormat64bppRGBAFixedPoint</span><span class="sxs-lookup"><span data-stu-id="5848b-540">GUID\_WICPixelFormat64bppRGBAFixedPoint</span></span>
    -   <span data-ttu-id="5848b-541">GUID \_ WICPixelFormat64bppRGBAHalf</span><span class="sxs-lookup"><span data-stu-id="5848b-541">GUID\_WICPixelFormat64bppRGBAHalf</span></span>
    -   <span data-ttu-id="5848b-542">GUID \_ WICPixelFormat128bppRGBAFloat</span><span class="sxs-lookup"><span data-stu-id="5848b-542">GUID\_WICPixelFormat128bppRGBAFloat</span></span>
    -   <span data-ttu-id="5848b-543">GUID \_ WICPixelFormat128bppPRGBAFloat</span><span class="sxs-lookup"><span data-stu-id="5848b-543">GUID\_WICPixelFormat128bppPRGBAFloat</span></span>
-   <span data-ttu-id="5848b-544">**Graustufen Formate**</span><span class="sxs-lookup"><span data-stu-id="5848b-544">**Grayscale formats**</span></span>
    -   <span data-ttu-id="5848b-545">GUID \_ WICPixelFormat8bppGray</span><span class="sxs-lookup"><span data-stu-id="5848b-545">GUID\_WICPixelFormat8bppGray</span></span>
    -   <span data-ttu-id="5848b-546">GUID \_ WICPixelFormat16bppGray</span><span class="sxs-lookup"><span data-stu-id="5848b-546">GUID\_WICPixelFormat16bppGray</span></span>
    -   <span data-ttu-id="5848b-547">GUID \_ WICPixelFormat16bppGrayFixedPoint</span><span class="sxs-lookup"><span data-stu-id="5848b-547">GUID\_WICPixelFormat16bppGrayFixedPoint</span></span>
    -   <span data-ttu-id="5848b-548">GUID \_ WICPixelFormat16bppGrayHalf</span><span class="sxs-lookup"><span data-stu-id="5848b-548">GUID\_WICPixelFormat16bppGrayHalf</span></span>
    -   <span data-ttu-id="5848b-549">GUID \_ WICPixelFormat32bppGrayFixedPoint</span><span class="sxs-lookup"><span data-stu-id="5848b-549">GUID\_WICPixelFormat32bppGrayFixedPoint</span></span>
    -   <span data-ttu-id="5848b-550">GUID \_ WICPixelFormat32bppGrayFloat</span><span class="sxs-lookup"><span data-stu-id="5848b-550">GUID\_WICPixelFormat32bppGrayFloat</span></span>
-   <span data-ttu-id="5848b-551">**Gepackte Formate**</span><span class="sxs-lookup"><span data-stu-id="5848b-551">**Packed formats**</span></span>
    -   <span data-ttu-id="5848b-552">GUID \_ WICPixelFormat16bppBGR555</span><span class="sxs-lookup"><span data-stu-id="5848b-552">GUID\_WICPixelFormat16bppBGR555</span></span>
    -   <span data-ttu-id="5848b-553">GUID \_ WICPixelFormat16bppBGR565</span><span class="sxs-lookup"><span data-stu-id="5848b-553">GUID\_WICPixelFormat16bppBGR565</span></span>
    -   <span data-ttu-id="5848b-554">GUID \_ WICPixelFormat32bppBGR101010</span><span class="sxs-lookup"><span data-stu-id="5848b-554">GUID\_WICPixelFormat32bppBGR101010</span></span>
    -   <span data-ttu-id="5848b-555">GUID \_ WICPixelFormat32bppRGBE</span><span class="sxs-lookup"><span data-stu-id="5848b-555">GUID\_WICPixelFormat32bppRGBE</span></span>
-   <span data-ttu-id="5848b-556">**CMYK-Formate**</span><span class="sxs-lookup"><span data-stu-id="5848b-556">**CMYK formats**</span></span>
    -   <span data-ttu-id="5848b-557">GUID \_ WICPixelFormat40bppCMYKAlpha</span><span class="sxs-lookup"><span data-stu-id="5848b-557">GUID\_WICPixelFormat40bppCMYKAlpha</span></span>
    -   <span data-ttu-id="5848b-558">GUID \_ WICPixelFormat64bppCMYK</span><span class="sxs-lookup"><span data-stu-id="5848b-558">GUID\_WICPixelFormat64bppCMYK</span></span>
    -   <span data-ttu-id="5848b-559">GUID \_ WICPixelFormat80bppCMYKAlpha</span><span class="sxs-lookup"><span data-stu-id="5848b-559">GUID\_WICPixelFormat80bppCMYKAlpha</span></span>
-   <span data-ttu-id="5848b-560">**N-Kanal Formate**</span><span class="sxs-lookup"><span data-stu-id="5848b-560">**N-channel formats**</span></span>
    -   <span data-ttu-id="5848b-561">GUID \_ WICPixelFormat32bpp4Channels</span><span class="sxs-lookup"><span data-stu-id="5848b-561">GUID\_WICPixelFormat32bpp4Channels</span></span>
    -   <span data-ttu-id="5848b-562">GUID \_ WICPixelFormat40bpp5Channels</span><span class="sxs-lookup"><span data-stu-id="5848b-562">GUID\_WICPixelFormat40bpp5Channels</span></span>
    -   <span data-ttu-id="5848b-563">GUID \_ WICPixelFormat48bpp6Channels</span><span class="sxs-lookup"><span data-stu-id="5848b-563">GUID\_WICPixelFormat48bpp6Channels</span></span>
    -   <span data-ttu-id="5848b-564">GUID \_ WICPixelFormat56bpp7Channels</span><span class="sxs-lookup"><span data-stu-id="5848b-564">GUID\_WICPixelFormat56bpp7Channels</span></span>
    -   <span data-ttu-id="5848b-565">GUID \_ WICPixelFormat64bpp8Channels</span><span class="sxs-lookup"><span data-stu-id="5848b-565">GUID\_WICPixelFormat64bpp8Channels</span></span>
    -   <span data-ttu-id="5848b-566">GUID \_ WICPixelFormat32bpp3ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="5848b-566">GUID\_WICPixelFormat32bpp3ChannelsAlpha</span></span>
    -   <span data-ttu-id="5848b-567">GUID \_ WICPixelFormat40bpp4ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="5848b-567">GUID\_WICPixelFormat40bpp4ChannelsAlpha</span></span>
    -   <span data-ttu-id="5848b-568">GUID \_ WICPixelFormat48bpp5ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="5848b-568">GUID\_WICPixelFormat48bpp5ChannelsAlpha</span></span>
    -   <span data-ttu-id="5848b-569">GUID \_ WICPixelFormat56bpp6ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="5848b-569">GUID\_WICPixelFormat56bpp6ChannelsAlpha</span></span>
    -   <span data-ttu-id="5848b-570">GUID \_ WICPixelFormat64bpp7ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="5848b-570">GUID\_WICPixelFormat64bpp7ChannelsAlpha</span></span>
    -   <span data-ttu-id="5848b-571">GUID \_ WICPixelFormat72bpp8ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="5848b-571">GUID\_WICPixelFormat72bpp8ChannelsAlpha</span></span>
    -   <span data-ttu-id="5848b-572">GUID \_ WICPixelFormat48bpp3Channels</span><span class="sxs-lookup"><span data-stu-id="5848b-572">GUID\_WICPixelFormat48bpp3Channels</span></span>
    -   <span data-ttu-id="5848b-573">GUID \_ WICPixelFormat64bpp4Channels</span><span class="sxs-lookup"><span data-stu-id="5848b-573">GUID\_WICPixelFormat64bpp4Channels</span></span>
    -   <span data-ttu-id="5848b-574">GUID \_ WICPixelFormat80bpp5Channels</span><span class="sxs-lookup"><span data-stu-id="5848b-574">GUID\_WICPixelFormat80bpp5Channels</span></span>
    -   <span data-ttu-id="5848b-575">GUID \_ WICPixelFormat96bpp6Channels</span><span class="sxs-lookup"><span data-stu-id="5848b-575">GUID\_WICPixelFormat96bpp6Channels</span></span>
    -   <span data-ttu-id="5848b-576">GUID \_ WICPixelFormat128bpp8Channels</span><span class="sxs-lookup"><span data-stu-id="5848b-576">GUID\_WICPixelFormat128bpp8Channels</span></span>
    -   <span data-ttu-id="5848b-577">GUID \_ WICPixelFormat64bpp3ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="5848b-577">GUID\_WICPixelFormat64bpp3ChannelsAlpha</span></span>
    -   <span data-ttu-id="5848b-578">GUID \_ WICPixelFormat80bpp4ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="5848b-578">GUID\_WICPixelFormat80bpp4ChannelsAlpha</span></span>
    -   <span data-ttu-id="5848b-579">GUID \_ WICPixelFormat96bpp5ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="5848b-579">GUID\_WICPixelFormat96bpp5ChannelsAlpha</span></span>
    -   <span data-ttu-id="5848b-580">GUID \_ WICPixelFormat112bpp6ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="5848b-580">GUID\_WICPixelFormat112bpp6ChannelsAlpha</span></span>
    -   <span data-ttu-id="5848b-581">GUID \_ WICPixelFormat128bpp7ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="5848b-581">GUID\_WICPixelFormat128bpp7ChannelsAlpha</span></span>
    -   <span data-ttu-id="5848b-582">GUID \_ WICPixelFormat144bpp8ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="5848b-582">GUID\_WICPixelFormat144bpp8ChannelsAlpha</span></span>

 

 
