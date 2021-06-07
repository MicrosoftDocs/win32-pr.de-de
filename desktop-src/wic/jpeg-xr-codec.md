---
description: Der native JPEG XR-Codec ist über den Windows-Bilderstellungskomponente (WIC) verfügbar. Das JPEG-XR-Format, das vom Codec unterstützt wird, ist für digitale Consumer und professionelle digitale Komprimierung konzipiert.
ms.assetid: CB8D1A5F-B544-462E-8927-F45512CED873
title: ÜBERSICHT ÜBER DEN JPEG XR-Codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0d39608535f9be09821d8db3615641a84fd95a6
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444462"
---
# <a name="jpeg-xr-codec-overview"></a><span data-ttu-id="61ddb-104">ÜBERSICHT ÜBER DEN JPEG XR-Codec</span><span class="sxs-lookup"><span data-stu-id="61ddb-104">JPEG XR Codec Overview</span></span>

<span data-ttu-id="61ddb-105">Der native JPEG XR-Codec ist über den Windows-Bilderstellungskomponente (WIC) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="61ddb-105">The native JPEG XR codec is available through the Windows Imaging Component (WIC).</span></span> <span data-ttu-id="61ddb-106">Das JPEG-XR-Format, das vom Codec unterstützt wird, ist für digitale Consumer und professionelle digitale Komprimierung konzipiert.</span><span class="sxs-lookup"><span data-stu-id="61ddb-106">The JPEG XR format, which the codec supports, is designed for consumer and professional digital photography.</span></span>

<span data-ttu-id="61ddb-107">Das JPEG-XR-Format kann bis zu doppelt so viele Komprimierungseffizienzen wie das ursprüngliche JPEG-Format erreichen, mit weniger spürbaren Komprimierungsartefakten.</span><span class="sxs-lookup"><span data-stu-id="61ddb-107">The JPEG XR format can achieve up to twice the compression efficiency of the original JPEG format, with less noticeable compression artifacts.</span></span> <span data-ttu-id="61ddb-108">Zu den Features von JPEG XR gehören:</span><span class="sxs-lookup"><span data-stu-id="61ddb-108">Features of JPEG XR include:</span></span>

-   <span data-ttu-id="61ddb-109">Unterstützung für monofarbige, RGB-, CGAM- und n-kanalbasierte Bilder</span><span class="sxs-lookup"><span data-stu-id="61ddb-109">Support for monochrome, RGB, CMYK, and n-channel images</span></span>
-   <span data-ttu-id="61ddb-110">8-, 16- und 32-Bit-Ganzzahlformate</span><span class="sxs-lookup"><span data-stu-id="61ddb-110">8-, 16-, and 32-bit integer formats</span></span>
-   <span data-ttu-id="61ddb-111">Hoher dynamischer Bereich, Breitformatformat mit Festkomma- oder Gleitkommafarbwerten</span><span class="sxs-lookup"><span data-stu-id="61ddb-111">High dynamic range, wide-gamut formats, using fixed point or floating point color values</span></span>
-   <span data-ttu-id="61ddb-112">Progressive Decodierung</span><span class="sxs-lookup"><span data-stu-id="61ddb-112">Progressive decoding</span></span>
-   <span data-ttu-id="61ddb-113">Verlustfreie oder verlustfreie Codierung mit demselben Komprimierungsalgorithmus</span><span class="sxs-lookup"><span data-stu-id="61ddb-113">Lossy or lossless encoding using the same compression algorithm</span></span>
-   <span data-ttu-id="61ddb-114">Unterstützung für die Decodierung von für große Bilder von Interesseden Regionen</span><span class="sxs-lookup"><span data-stu-id="61ddb-114">Support for decoding of regions of interest in large images</span></span>

<span data-ttu-id="61ddb-115">Das JPEG-XR-Format wird in den folgenden Standarddokumenten definiert:</span><span class="sxs-lookup"><span data-stu-id="61ddb-115">The JPEG XR format is defined in the following standards documents:</span></span>

-   <span data-ttu-id="61ddb-116">ITU-T T.832: *Informationstechnologie – JPEG XR-Bildcodierungssystem – Spezifikation der Bildcodierung*</span><span class="sxs-lookup"><span data-stu-id="61ddb-116">ITU-T T.832: *Information technology – JPEG XR image coding system – Image coding specification*</span></span>
-   <span data-ttu-id="61ddb-117">ISO/IEC 29199-2:2010: *Informationstechnologie – JPEG XR-Bildcodierungssystem – Teil 2: Spezifikation* der Bildcodierung</span><span class="sxs-lookup"><span data-stu-id="61ddb-117">ISO/IEC 29199-2:2010: *Information technology — JPEG XR image coding system — Part 2: Image coding specification*</span></span>

<span data-ttu-id="61ddb-118">Der JPEG-XR-Standard basiert größtenteils auf dem [HD-Fotoformat,](hdphoto-format-overview.md) es gibt jedoch einige Unterschiede zwischen den beiden Formaten.</span><span class="sxs-lookup"><span data-stu-id="61ddb-118">The JPEG XR standard is largely based on the [HD Photo](hdphoto-format-overview.md) format, but there are some differences between the two formats.</span></span> <span data-ttu-id="61ddb-119">In Windows 8 wurde der HD-Fotocodec aktualisiert, um JPEG XR zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="61ddb-119">In Windows 8, the HD Photo codec has been updated to support JPEG XR.</span></span> <span data-ttu-id="61ddb-120">Der Encoder gibt jetzt immer einen JPEG XR-kompatiblen Bitstream aus.</span><span class="sxs-lookup"><span data-stu-id="61ddb-120">The encoder now always outputs a JPEG XR–compliant bit stream.</span></span> <span data-ttu-id="61ddb-121">Der Decoder kann sowohl JPEG-XR- als auch HD-Fotobilder decodieren.</span><span class="sxs-lookup"><span data-stu-id="61ddb-121">The decoder can decode both JPEG XR and HD Photo images.</span></span>

<span data-ttu-id="61ddb-122">Im Zusammenhang mit dem HD-Fotocodec wurden erhebliche Leistungsverbesserungen am JPEG-XR-Codec vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="61ddb-122">Substantial performance improvements, in relation to the HD Photo codec, have been made to the JPEG XR codec.</span></span> <span data-ttu-id="61ddb-123">Beispielsweise wurde die Bilddecodierung mit unterer Auflösung, z. B. die Miniaturansichtsgenerierung, sowie die Bilddecodierung mit niedriger Auflösung verbessert.</span><span class="sxs-lookup"><span data-stu-id="61ddb-123">For example, sub-resolution image decoding, such as thumbnail generation, has been improved, as well as low-resolution image decoding.</span></span> <span data-ttu-id="61ddb-124">Es wird empfohlen, anstelle des HD-Fotoformats das JPEG-XR-Format zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="61ddb-124">It is recommended that you use the JPEG XR format instead of the HD Photo format.</span></span>

## <a name="codec-information"></a><span data-ttu-id="61ddb-125">Codec-Informationen</span><span class="sxs-lookup"><span data-stu-id="61ddb-125">Codec Information</span></span>



|      <span data-ttu-id="61ddb-126">Komponente</span><span class="sxs-lookup"><span data-stu-id="61ddb-126">Component</span></span>      |    <span data-ttu-id="61ddb-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="61ddb-127">Description</span></span>                                                          |
|---------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="61ddb-128">Dateinamenerweiterung</span><span class="sxs-lookup"><span data-stu-id="61ddb-128">File name extension</span></span> | <span data-ttu-id="61ddb-129">"jxr" und "wdp"</span><span class="sxs-lookup"><span data-stu-id="61ddb-129">"jxr" and "wdp"</span></span>                                                         |
| <span data-ttu-id="61ddb-130">Container-GUID</span><span class="sxs-lookup"><span data-stu-id="61ddb-130">Container GUID</span></span>      | <span data-ttu-id="61ddb-131">**GUID \_ ContainerFormatWmp**</span><span class="sxs-lookup"><span data-stu-id="61ddb-131">**GUID\_ContainerFormatWmp**</span></span>                                            |
| <span data-ttu-id="61ddb-132">Decoder-GUID</span><span class="sxs-lookup"><span data-stu-id="61ddb-132">Decoder GUID</span></span>        | <span data-ttu-id="61ddb-133">**CLSID \_ WICWmpDecoder**</span><span class="sxs-lookup"><span data-stu-id="61ddb-133">**CLSID\_WICWmpDecoder**</span></span>                                                |
| <span data-ttu-id="61ddb-134">Encoder-GUID</span><span class="sxs-lookup"><span data-stu-id="61ddb-134">Encoder GUID</span></span>        | <span data-ttu-id="61ddb-135">**CLSID \_ WICWmpEncoder**</span><span class="sxs-lookup"><span data-stu-id="61ddb-135">**CLSID\_WICWmpEncoder**</span></span>                                                |
| <span data-ttu-id="61ddb-136">Profilunterstützung</span><span class="sxs-lookup"><span data-stu-id="61ddb-136">Profile Support</span></span>     | <span data-ttu-id="61ddb-137">Encoder und Decoder unterstützen bis zu Hauptprofil und bis Ebene 128.</span><span class="sxs-lookup"><span data-stu-id="61ddb-137">The encoder and decoder support up to Main Profile and up to level 128.</span></span> |



 

## <a name="codec-features"></a><span data-ttu-id="61ddb-138">Codecfunktionen</span><span class="sxs-lookup"><span data-stu-id="61ddb-138">Codec Features</span></span>

### <a name="high-dynamic-range"></a><span data-ttu-id="61ddb-139">High Dynamic Range</span><span class="sxs-lookup"><span data-stu-id="61ddb-139">High Dynamic Range</span></span>

<span data-ttu-id="61ddb-140">JPEG XR unterstützt Bilder mit hohem dynamischem Bereich, die Gleitkomma- oder Festkommafarben verwenden.</span><span class="sxs-lookup"><span data-stu-id="61ddb-140">JPEG XR supports high-dynamic range images, using floating-point or fixed-point colors.</span></span> <span data-ttu-id="61ddb-141">In diesen Farbformaten ist der numerische Bereich eines Pixels größer als der sichtbare Bereich, sodass Sie Farben über oder unterhalb des sichtbaren Bereichs während zwischengeschalteter Verarbeitungsphasen anpassen können.</span><span class="sxs-lookup"><span data-stu-id="61ddb-141">In these color formats, the numerical range of a pixel is larger than the visible range, so you can adjust colors above or below the visible range during intermediate processing stages.</span></span>

-   <span data-ttu-id="61ddb-142">Fester Punkt: In einer Festpunktdarstellung steht 0 für Schwarz und 1,0 für die maximale Sättigung.</span><span class="sxs-lookup"><span data-stu-id="61ddb-142">Fixed-point: In a fixed-point representation, 0 represents black and 1.0 represents maximum saturation.</span></span> <span data-ttu-id="61ddb-143">Der JPEG XR-Codec unterstützt sowohl 16-Bit- als auch 32-Bit-Festpunktformate.</span><span class="sxs-lookup"><span data-stu-id="61ddb-143">The JPEG XR codec supports both 16-bit and 32-bit fixed-point formats.</span></span> <span data-ttu-id="61ddb-144">Für 16-Bit, 1,0 = 0x2000h, was 13 Bits für den sichtbaren Bereich \[ 0...1 \] ergibt.</span><span class="sxs-lookup"><span data-stu-id="61ddb-144">For 16-bit, 1.0 = 0x2000h, which gives 13 bits for the visible range \[0...1\].</span></span> <span data-ttu-id="61ddb-145">Der Gesamtbereich ist –4,0 bis +3,999 und wird linear zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="61ddb-145">The total range is –4.0 to +3.999, and is mapped linearly.</span></span> <span data-ttu-id="61ddb-146">Für 32-Bit, 1,0 = 0x01000000h beträgt der sichtbare Bereich 24 Bits und der Gesamtbereich –128 bis +127,999.</span><span class="sxs-lookup"><span data-stu-id="61ddb-146">For 32-bit, 1.0 = 0x01000000h, the visible range is 24 bits, and the total range is –128 to +127.999.</span></span>
-   <span data-ttu-id="61ddb-147">Gleitkomma: In einer Gleitkommadarstellung steht 0 für Schwarz und 1,0 für die maximale Sättigung.</span><span class="sxs-lookup"><span data-stu-id="61ddb-147">Floating-point: In a floating-point representation, 0 represents black and 1.0 represents maximum saturation.</span></span> <span data-ttu-id="61ddb-148">Der JPEG XR-Codec unterstützt sowohl 16-Bit- als auch 32-Bit-Gleitkommaformate.</span><span class="sxs-lookup"><span data-stu-id="61ddb-148">The JPEG XR codec supports both 16-bit and 32-bit floating-point formats.</span></span>

### <a name="tiles"></a><span data-ttu-id="61ddb-149">Kacheln</span><span class="sxs-lookup"><span data-stu-id="61ddb-149">Tiles</span></span>

<span data-ttu-id="61ddb-150">Ein Frame kann in rechteckige Unterregionen partitioniert werden, die als Kacheln *bezeichnet werden.*</span><span class="sxs-lookup"><span data-stu-id="61ddb-150">A frame can be partitioned into rectangular subregions called *tiles*.</span></span> <span data-ttu-id="61ddb-151">Eine Kachel ist ein Bereich eines Bilds, das rechteckige Arrays von Makroblocks enthält.</span><span class="sxs-lookup"><span data-stu-id="61ddb-151">A tile is an area of a image that contains rectangular arrays of macroblocks.</span></span> <span data-ttu-id="61ddb-152">Mit Kacheln können Bereiche des Bilds decodiert werden, ohne das gesamte Bild zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="61ddb-152">Tiles enable regions of the image to be decoded without processing the entire image.</span></span>

<span data-ttu-id="61ddb-153">Wählen Sie während der Codierung die Anzahl der Kacheln aus, indem Sie die **Eigenschaften HorizontalTileSlices** und **VerticalTileSlices** festlegen.</span><span class="sxs-lookup"><span data-stu-id="61ddb-153">During encoding, select the number of tiles by setting the **HorizontalTileSlices** and **VerticalTileSlices** properties.</span></span> <span data-ttu-id="61ddb-154">Die minimale Kachelgröße beträgt 16 × 16 Pixel.</span><span class="sxs-lookup"><span data-stu-id="61ddb-154">The minimum tile size is 16 × 16 pixels.</span></span> <span data-ttu-id="61ddb-155">Der Encoder passt die Anzahl der Kacheln an, um diese Einschränkung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="61ddb-155">The encoder adjusts the number of tiles to maintain this restriction.</span></span> <span data-ttu-id="61ddb-156">Da jeder Kachel Speicher- und Verarbeitungsaufwand zugeordnet ist, sollten Sie die Anzahl der Kacheln berücksichtigen, die für bestimmte Szenarien erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="61ddb-156">There is storage and processing overhead associated with each tile, so you should consider the number of tiles that are needed for particular scenarios.</span></span>

### <a name="image-stream-output"></a><span data-ttu-id="61ddb-157">Imagestreamausgabe</span><span class="sxs-lookup"><span data-stu-id="61ddb-157">Image Stream Output</span></span>

<span data-ttu-id="61ddb-158">Der JPEG-XR-Standard definiert zwei Teile einer JPEG-XR-Datei:</span><span class="sxs-lookup"><span data-stu-id="61ddb-158">The JPEG-XR standard defines two parts of a JPEG-XR file:</span></span>

-   <span data-ttu-id="61ddb-159">Der Bildbitstream, der im Textkörper des Standards definiert ist.</span><span class="sxs-lookup"><span data-stu-id="61ddb-159">The image bit stream, defined in the body of the standard.</span></span>
-   <span data-ttu-id="61ddb-160">Der Imagecontainer.</span><span class="sxs-lookup"><span data-stu-id="61ddb-160">The image container.</span></span> <span data-ttu-id="61ddb-161">Die Datei enthält Exif- und XMP-Metadaten und ist in Anhang A des Standards definiert.</span><span class="sxs-lookup"><span data-stu-id="61ddb-161">The file contains Exif and XMP metadata, and is defined in Annex A of the standard.</span></span>

<span data-ttu-id="61ddb-162">Es ist möglich und wird vom Standard zugelassen, den Imagestream in einen anderen Typ von Dateicontainer einbetten.</span><span class="sxs-lookup"><span data-stu-id="61ddb-162">It is possible, and allowed by the standard, to embed the image stream inside another type of file container.</span></span> <span data-ttu-id="61ddb-163">Der Encoder unterstützt einen Nur-Stream-Modus, der den Unformatiertbild-Bitstream ohne Imagecontainer aus gibt.</span><span class="sxs-lookup"><span data-stu-id="61ddb-163">The encoder supports a stream-only mode, which outputs the raw image bit stream with no image container.</span></span> <span data-ttu-id="61ddb-164">Eine Anwendung kann den Bitstream in einem anderen Containerformat speichern.</span><span class="sxs-lookup"><span data-stu-id="61ddb-164">An application can store the bit stream in some other container format.</span></span>

<span data-ttu-id="61ddb-165">Legen Sie die **StreamOnly-Eigenschaft** fest, um den modus only stream zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="61ddb-165">To enable stream-only mode, set the **StreamOnly** property.</span></span>

### <a name="image-quality-settings"></a><span data-ttu-id="61ddb-166">Einstellungen für die Imagequalität</span><span class="sxs-lookup"><span data-stu-id="61ddb-166">Image Quality Settings</span></span>

<span data-ttu-id="61ddb-167">Mehrere Codeceigenschaften steuern die Qualität des Ausgabebilds vom Encoder.</span><span class="sxs-lookup"><span data-stu-id="61ddb-167">Several codec properties control the quality of the output image from the encoder.</span></span>

-   <span data-ttu-id="61ddb-168">[ImageQuality ist](#imagequality) eine Eigenschaft, die von WIC-Codecs gemeinsam verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="61ddb-168">[ImageQuality](#imagequality) is a property common across WIC codecs.</span></span> <span data-ttu-id="61ddb-169">Sie gibt die Bildqualität als einzelnen Gleitkommawert von 0,0 bis 1,0 an.</span><span class="sxs-lookup"><span data-stu-id="61ddb-169">It specifies image quality as a single floating-point value from 0.0–1.0,</span></span>
-   <span data-ttu-id="61ddb-170">Die [Eigenschaften Quality](#image-quality-settings), [Overlap](#overlap)und [Subsampling](#subsampling) bieten mehr Kontrolle über die Qualitätseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="61ddb-170">The [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties give more control over the quality settings.</span></span>

<span data-ttu-id="61ddb-171">Um die [Eigenschaften Quality](#image-quality-settings), [Overlap](#overlap)und [Subsampling](#subsampling) zu verwenden, legen Sie die [UseCodecOptions-Eigenschaft](#usecodecoptions) auf **VARIANT TRUE \_ fest.**</span><span class="sxs-lookup"><span data-stu-id="61ddb-171">To use the [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties, set the [UseCodecOptions](#usecodecoptions) property to **VARIANT\_TRUE**.</span></span>

<span data-ttu-id="61ddb-172">Wenn [UseCodecOptions](#usecodecoptions) auf **VARIANT \_ FALSE** festgelegt ist **(standardmäßig VARIANT \_ FALSE),** verwendet der Encoder die [ImageQuality-Eigenschaft.](#imagequality)</span><span class="sxs-lookup"><span data-stu-id="61ddb-172">If [UseCodecOptions](#usecodecoptions) is **VARIANT\_FALSE** (**VARIANT\_FALSE** is the default) the encoder uses the [ImageQuality](#imagequality) property.</span></span> <span data-ttu-id="61ddb-173">Der Encoder ordnet den Wert von ImageQuality [quality](#image-quality-settings), [Overlap](#overlap)und [Subsampling](#subsampling) über eine Nachschlagetabelle zu.</span><span class="sxs-lookup"><span data-stu-id="61ddb-173">The encoder maps the value of ImageQuality to [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) through a lookup table.</span></span>

<span data-ttu-id="61ddb-174">Der Encoder unterstützt die **CompressionQuality-Eigenschaft** nicht.</span><span class="sxs-lookup"><span data-stu-id="61ddb-174">The encoder does not support the **CompressionQuality** property.</span></span>

### <a name="compressed-domain-transcode"></a><span data-ttu-id="61ddb-175">Transcodierung komprimierter Domänen</span><span class="sxs-lookup"><span data-stu-id="61ddb-175">Compressed Domain Transcode</span></span>

<span data-ttu-id="61ddb-176">Der JPEG XR-Codec kann bestimmte Bildtransformationen durchführen, ohne die komprimierten Daten tatsächlich zu decodieren und neu zu codieren.</span><span class="sxs-lookup"><span data-stu-id="61ddb-176">The JPEG XR codec can perform certain image transformations without actually decoding the compressed data and re-encoding it.</span></span> <span data-ttu-id="61ddb-177">Vorgänge für komprimierte Domänen sind sehr effizient und vermeiden zusätzliche Qualitätsverluste, die typisch sind, wenn Sie ein verlustverknrücktes Bild decodieren und erneut codieren.</span><span class="sxs-lookup"><span data-stu-id="61ddb-177">Compressed domain operations are very efficient and avoid any additional quality loss that is typical when you decode and re-encode a lossy-compressed image.</span></span>

<span data-ttu-id="61ddb-178">Die folgenden Vorgänge für komprimierte Domänen werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="61ddb-178">The following compressed domain operations are supported:</span></span>

-   <span data-ttu-id="61ddb-179">Zuschneiden eines Bildbereichs.</span><span class="sxs-lookup"><span data-stu-id="61ddb-179">Crop a region of the image.</span></span>
-   <span data-ttu-id="61ddb-180">Drehen oder kippen Sie das Bild.</span><span class="sxs-lookup"><span data-stu-id="61ddb-180">Rotate or flip the image.</span></span>
-   <span data-ttu-id="61ddb-181">Verwerfen Sie Häufigkeitsdaten, um eine kleinere Bilddatei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="61ddb-181">Discard frequency data to create a smaller image file.</span></span>
-   <span data-ttu-id="61ddb-182">Organisieren Sie das Bild zwischen räumlicher reihenfolge und Häufigkeits reihenfolge neu.</span><span class="sxs-lookup"><span data-stu-id="61ddb-182">Reorganize the image between spatial and frequency order.</span></span>

<span data-ttu-id="61ddb-183">Der JPEG XR-Encoder verwendet nach Möglichkeit eine komprimierte Domänentranscodierung, wenn das Quellbild ein JPEG XR-Bild ist.</span><span class="sxs-lookup"><span data-stu-id="61ddb-183">The JPEG XR encoder uses compressed domain transcoding, if possible, when the source image is a JPEG XR image.</span></span> <span data-ttu-id="61ddb-184">Wenn der Encoder einen komprimierten Domänenvorgang ausführt, ignoriert er die folgenden Codeceigenschaften: [AlphaQuality,](#alphaquality) [ImageQuality,](#imagequality) [InterleavedAlpha,](#interleavedalpha) [Lossless](#lossless)[Overlap](#overlap)und [Quality](#image-quality-settings).</span><span class="sxs-lookup"><span data-stu-id="61ddb-184">When the encoder performs a compressed domain operation, it ignores the following codec properties: [AlphaQuality](#alphaquality), [ImageQuality](#imagequality), [InterleavedAlpha](#interleavedalpha), [Lossless](#lossless)[Overlap](#overlap), and [Quality](#image-quality-settings).</span></span> <span data-ttu-id="61ddb-185">Wenn die [Eigenschaften HorizontalTileSlices](/windows) und [VerticalTileSlices](/windows) vorhanden sind, müssen Sie sie auf 0 (null) festlegen.</span><span class="sxs-lookup"><span data-stu-id="61ddb-185">If the [HorizontalTileSlices](/windows) and [VerticalTileSlices](/windows) properties are present, you must set them to zero.</span></span> <span data-ttu-id="61ddb-186">Sie können die Kachelgröße eines Bilds nicht im Rahmen einer komprimierten Domänentranscodierung ändern.</span><span class="sxs-lookup"><span data-stu-id="61ddb-186">You cannot change the tile size of an image as part of a compressed domain transcode.</span></span>

<span data-ttu-id="61ddb-187">In der folgenden Liste wird beschrieben, wie die Bildtransformationen durchzuführen sind.</span><span class="sxs-lookup"><span data-stu-id="61ddb-187">The follow list describes how to perform the image transformations.</span></span>

-   <span data-ttu-id="61ddb-188">Legen Sie zum Zuschneiden des Bilds den gewünschten Bereich im [**WICRect-Parameter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) der **WriteSource-Methode** fest.</span><span class="sxs-lookup"><span data-stu-id="61ddb-188">To crop the image, set the desired region in the [**WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) parameter of the **WriteSource** method.</span></span>
-   <span data-ttu-id="61ddb-189">Legen Sie die [BitmapTransform-Eigenschaft](#bitmaptransform) fest, um das Bild zu drehen oder zu kippen.</span><span class="sxs-lookup"><span data-stu-id="61ddb-189">To rotate or flip the image, set the [BitmapTransform](#bitmaptransform) property.</span></span>
-   <span data-ttu-id="61ddb-190">Legen Sie die [ImageDataDiscard-Eigenschaft](#imagedatadiscard) fest, um Häufigkeitsdaten im Bild zu verwerfen.</span><span class="sxs-lookup"><span data-stu-id="61ddb-190">To discard frequency data in the image, set the [ImageDataDiscard](#imagedatadiscard) property.</span></span> <span data-ttu-id="61ddb-191">Legen Sie die AlphaDataDiscard-Eigenschaft fest, um Häufigkeitsdaten im [Alphakanal zu verwerfen.](#alphadatadiscard)</span><span class="sxs-lookup"><span data-stu-id="61ddb-191">To discard frequency data in the alpha channel, set the [AlphaDataDiscard](#alphadatadiscard) property.</span></span> <span data-ttu-id="61ddb-192">Durch das Verwerfen von Häufigkeitsdaten wird die codierte Dateigröße reduziert, und die Auflösung kann reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="61ddb-192">Discarding frequency data reduces the encoded file size and can reduce the resolution.</span></span>
-   <span data-ttu-id="61ddb-193">Um die Bildorganisation zwischen Häufigkeit und räumlicher Reihenfolge zu ändern, legen Sie die [FrequencyOrdering-Eigenschaft](/windows) fest.</span><span class="sxs-lookup"><span data-stu-id="61ddb-193">To change the image organization between frequency and spatial ordering, set the [FrequencyOrdering](/windows) property.</span></span>

<span data-ttu-id="61ddb-194">Legen Sie [UseCodecOptions](#usecodecoptions) auf **VARIANT \_ TRUE** und [CompressedDomainTranscode](#compresseddomaintranscode) auf VARIANT FALSE fest, um die Transcodierung komprimierter Domänen zu deaktivieren und die erneute Codierung des Bilds durch den Encoder zu **\_ erzwingen.**</span><span class="sxs-lookup"><span data-stu-id="61ddb-194">To disable compressed domain transcode and force the encoder to re-encode the image, set the [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE** and set [CompressedDomainTranscode](#compresseddomaintranscode) to **VARIANT\_FALSE**.</span></span>

## <a name="encoder-options"></a><span data-ttu-id="61ddb-195">Encoderoptionen</span><span class="sxs-lookup"><span data-stu-id="61ddb-195">Encoder Options</span></span>

<span data-ttu-id="61ddb-196">Verwenden Sie zum Festlegen von Codierungseigenschaften die [**IPropertyBag2-Schnittstelle.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="61ddb-196">To set encoding properties, use the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface.</span></span> <span data-ttu-id="61ddb-197">Weitere Informationen finden Sie unter Übersicht über [die Codierung.](-wic-creating-encoder.md)</span><span class="sxs-lookup"><span data-stu-id="61ddb-197">For more information, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="61ddb-198">In der folgenden Liste sind die Encoderoptionen angegeben.</span><span class="sxs-lookup"><span data-stu-id="61ddb-198">The following list specifies the encoder options.</span></span>

-   [<span data-ttu-id="61ddb-199">AlphaDataDiscard</span><span class="sxs-lookup"><span data-stu-id="61ddb-199">AlphaDataDiscard</span></span>](#alphadatadiscard)
-   [<span data-ttu-id="61ddb-200">AlphaQuality</span><span class="sxs-lookup"><span data-stu-id="61ddb-200">AlphaQuality</span></span>](#alphaquality)
-   [<span data-ttu-id="61ddb-201">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="61ddb-201">BitmapTransform</span></span>](#bitmaptransform)
-   [<span data-ttu-id="61ddb-202">CompressedDomainTranscode</span><span class="sxs-lookup"><span data-stu-id="61ddb-202">CompressedDomainTranscode</span></span>](#compresseddomaintranscode)
-   [<span data-ttu-id="61ddb-203">FrequencyOrder</span><span class="sxs-lookup"><span data-stu-id="61ddb-203">FrequencyOrder</span></span>](#frequencyorder)
-   [<span data-ttu-id="61ddb-204">HorizontalTileSlices</span><span class="sxs-lookup"><span data-stu-id="61ddb-204">HorizontalTileSlices</span></span>](#horizontaltileslices)
-   [<span data-ttu-id="61ddb-205">IgnoreOverlap</span><span class="sxs-lookup"><span data-stu-id="61ddb-205">IgnoreOverlap</span></span>](#ignoreoverlap)
-   [<span data-ttu-id="61ddb-206">ImageDataDiscard</span><span class="sxs-lookup"><span data-stu-id="61ddb-206">ImageDataDiscard</span></span>](#imagedatadiscard)
-   [<span data-ttu-id="61ddb-207">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="61ddb-207">ImageQuality</span></span>](#imagequality)
-   [<span data-ttu-id="61ddb-208">InterleavedAlpha</span><span class="sxs-lookup"><span data-stu-id="61ddb-208">InterleavedAlpha</span></span>](#interleavedalpha)
-   [<span data-ttu-id="61ddb-209">Lossless</span><span class="sxs-lookup"><span data-stu-id="61ddb-209">Lossless</span></span>](#lossless)
-   [<span data-ttu-id="61ddb-210">Überlappen</span><span class="sxs-lookup"><span data-stu-id="61ddb-210">Overlap</span></span>](#overlap)
-   [<span data-ttu-id="61ddb-211">ProgressiveMode</span><span class="sxs-lookup"><span data-stu-id="61ddb-211">ProgressiveMode</span></span>](#progressivemode)
-   [<span data-ttu-id="61ddb-212">Qualität</span><span class="sxs-lookup"><span data-stu-id="61ddb-212">Quality</span></span>](#image-quality-settings)
-   [<span data-ttu-id="61ddb-213">StreamOnly</span><span class="sxs-lookup"><span data-stu-id="61ddb-213">StreamOnly</span></span>](#streamonly)
-   [<span data-ttu-id="61ddb-214">Untersampling</span><span class="sxs-lookup"><span data-stu-id="61ddb-214">Subsampling</span></span>](#subsampling)
-   [<span data-ttu-id="61ddb-215">UseCodecOptions</span><span class="sxs-lookup"><span data-stu-id="61ddb-215">UseCodecOptions</span></span>](#usecodecoptions)
-   [<span data-ttu-id="61ddb-216">VerticalTileSlices</span><span class="sxs-lookup"><span data-stu-id="61ddb-216">VerticalTileSlices</span></span>](#verticaltileslices)

### <a name="alphadatadiscard"></a><span data-ttu-id="61ddb-217">AlphaDataDiscard</span><span class="sxs-lookup"><span data-stu-id="61ddb-217">AlphaDataDiscard</span></span>

<span data-ttu-id="61ddb-218">Legt die Menge der Alphafrequenzdaten fest, die während einer komprimierten Domänentranscodierung verworfen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="61ddb-218">Sets the amount of alpha frequency data to discard during a compressed domain transcode.</span></span>



| <span data-ttu-id="61ddb-219">Datentyp</span><span class="sxs-lookup"><span data-stu-id="61ddb-219">Data type</span></span> | <span data-ttu-id="61ddb-220">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61ddb-220">VARTYPE</span></span>     | <span data-ttu-id="61ddb-221">Range</span><span class="sxs-lookup"><span data-stu-id="61ddb-221">Range</span></span> | <span data-ttu-id="61ddb-222">Standard</span><span class="sxs-lookup"><span data-stu-id="61ddb-222">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="61ddb-223">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="61ddb-223">**UCHAR**</span></span> | <span data-ttu-id="61ddb-224">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="61ddb-224">**VT\_UI1**</span></span> | <span data-ttu-id="61ddb-225">0–4</span><span class="sxs-lookup"><span data-stu-id="61ddb-225">0–4</span></span>   | <span data-ttu-id="61ddb-226">Keine</span><span class="sxs-lookup"><span data-stu-id="61ddb-226">None</span></span>    |



 

<span data-ttu-id="61ddb-227">Diese Eigenschaft gilt nur, wenn die [CompressedDomainTranscode-Eigenschaft](#compresseddomaintranscode) auf **VARIANT \_ TRUE** festgelegt ist und das Bild entweder einen planaren Alphakanal oder einen verschachtelten Alphakanal enthält. Andernfalls wird sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="61ddb-227">This property applies only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE** and the image contains either a planar alpha channel or interleaved alpha channel; otherwise it is ignored.</span></span>

<span data-ttu-id="61ddb-228">Für Bilder, die einen planaren Alphakanal enthalten, sind die folgenden Werte gültig.</span><span class="sxs-lookup"><span data-stu-id="61ddb-228">For images that contain a planar alpha channel, the following values are valid.</span></span>



| <span data-ttu-id="61ddb-229">Wert</span><span class="sxs-lookup"><span data-stu-id="61ddb-229">Value</span></span> | <span data-ttu-id="61ddb-230">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="61ddb-230">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61ddb-231">0</span><span class="sxs-lookup"><span data-stu-id="61ddb-231">0</span></span>     | <span data-ttu-id="61ddb-232">Es werden keine Bildfrequenzdaten verworfen.</span><span class="sxs-lookup"><span data-stu-id="61ddb-232">No image frequency data is discarded.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="61ddb-233">1</span><span class="sxs-lookup"><span data-stu-id="61ddb-233">1</span></span>     | <span data-ttu-id="61ddb-234">Die Flexbits werden verworfen.</span><span class="sxs-lookup"><span data-stu-id="61ddb-234">The flexbits are discarded.</span></span> <span data-ttu-id="61ddb-235">Dadurch wird die Qualität des planaren Alphakanals für das transcodierte Bild willkürlich reduziert.</span><span class="sxs-lookup"><span data-stu-id="61ddb-235">This arbitrarily reduces the quality of the planar alpha channel for the transcoded image.</span></span> <span data-ttu-id="61ddb-236">, ohne eine Änderung der effektiven Auflösung.</span><span class="sxs-lookup"><span data-stu-id="61ddb-236">, without a change in the effective resolution.</span></span> <span data-ttu-id="61ddb-237">Die genaue Verringerung der Dateigröße und -qualität hängt von zahlreichen Faktoren ab und kann nicht genau angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="61ddb-237">The exact reduction in file size and quality depends on numerous factors and cannot be exactly specified.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="61ddb-238">2</span><span class="sxs-lookup"><span data-stu-id="61ddb-238">2</span></span>     | <span data-ttu-id="61ddb-239">Das Datenband mit hoher Durchlauffrequenz wird verworfen, einschließlich der Flexbits.</span><span class="sxs-lookup"><span data-stu-id="61ddb-239">The high-pass frequency data band is discarded, including the flexbits.</span></span> <span data-ttu-id="61ddb-240">Dadurch wird die Auflösung des planaren Alphakanals in beiden Dimensionen um den Faktor 4 reduziert.</span><span class="sxs-lookup"><span data-stu-id="61ddb-240">This effectively reduces the resolution of the planar alpha channel by a factor of 4 in both dimensions.</span></span> <span data-ttu-id="61ddb-241">Die tatsächlichen Abmessungen des transcodierten Bilds bleiben gleich, aber das Bild verliert alle Details in jedem 4x4-Block von Alphakanalpixeln.</span><span class="sxs-lookup"><span data-stu-id="61ddb-241">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 4x4 block of alpha-channel pixels.</span></span> <span data-ttu-id="61ddb-242">In der Regel sollten Sie diesen Wert nur festlegen, wenn die [ImageDataDiscard-Eigenschaft](#imagedatadiscard) denselben Wert hat.</span><span class="sxs-lookup"><span data-stu-id="61ddb-242">Typically, you should set this value only when the [ImageDataDiscard](#imagedatadiscard) property has the same value.</span></span>                            |
| <span data-ttu-id="61ddb-243">3</span><span class="sxs-lookup"><span data-stu-id="61ddb-243">3</span></span>     | <span data-ttu-id="61ddb-244">Sowohl die Datenbänder mit hoher als auch der niedriger Durchlauffrequenz werden verworfen, einschließlich der Flexbits.</span><span class="sxs-lookup"><span data-stu-id="61ddb-244">Both the high-pass and low-pass frequency data bands are discarded, including the flexbits.</span></span> <span data-ttu-id="61ddb-245">Dadurch wird die Auflösung des planaren Alphakanals in beiden Dimensionen um den Faktor 16 reduziert.</span><span class="sxs-lookup"><span data-stu-id="61ddb-245">This ffectively reduces the resolution of the planar alpha channel by a factor of 16 in both dimensions.</span></span> <span data-ttu-id="61ddb-246">Die tatsächlichen Abmessungen des transcodierten Bilds bleiben gleich, aber das Bild verliert alle Details in jedem 16x16-Makroblock von Alphakanalpixeln.</span><span class="sxs-lookup"><span data-stu-id="61ddb-246">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 16x16 macroblock of alpha-channel pixels.</span></span> <span data-ttu-id="61ddb-247">In der Regel sollten Sie diesen Wert nur festlegen, wenn die [ImageDataDiscard-Eigenschaft](#imagedatadiscard) denselben Wert hat.</span><span class="sxs-lookup"><span data-stu-id="61ddb-247">Typically, you should set this value only when the [ImageDataDiscard](#imagedatadiscard) property has the same value.</span></span> |
| <span data-ttu-id="61ddb-248">4</span><span class="sxs-lookup"><span data-stu-id="61ddb-248">4</span></span>     | <span data-ttu-id="61ddb-249">Der Alphakanal wird vollständig verworfen.</span><span class="sxs-lookup"><span data-stu-id="61ddb-249">The alpha channel is completely discarded.</span></span> <span data-ttu-id="61ddb-250">Das Pixelformat des transcodierten Bilds wird geändert, um das Entfernen des Alphakanals widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="61ddb-250">The pixel format of the transcoded image is changed to reflect the removal of the alpha channel.</span></span>                                                                                                                                                                                                                                                                                                                                |



 

<span data-ttu-id="61ddb-251">Für Bilder, die einen verschachtelten Alphakanal enthalten, ist der folgende Wert gültig.</span><span class="sxs-lookup"><span data-stu-id="61ddb-251">For images that contain an interleaved alpha channel, the following value is valid.</span></span>



| <span data-ttu-id="61ddb-252">Wert</span><span class="sxs-lookup"><span data-stu-id="61ddb-252">Value</span></span> | <span data-ttu-id="61ddb-253">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="61ddb-253">Description</span></span>                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61ddb-254">4</span><span class="sxs-lookup"><span data-stu-id="61ddb-254">4</span></span>     | <span data-ttu-id="61ddb-255">Der Alphakanal wird vollständig verworfen.</span><span class="sxs-lookup"><span data-stu-id="61ddb-255">The alpha channel is completely discarded.</span></span> <span data-ttu-id="61ddb-256">Das Pixelformat des transcodierten Bilds wird geändert, um das Entfernen des Alphakanals widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="61ddb-256">The pixel format of the transcoded image is changed to reflect the removal of the alpha channel.</span></span> |



 

<span data-ttu-id="61ddb-257">Wenn diese Eigenschaft für verschachtelte Alphas nicht auf 4 festgelegt ist, wird der Alphakanal gemäß dem Wert der [ImageDataDiscard-Eigenschaft](#imagedatadiscard) mit den Bilddaten verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="61ddb-257">For interleaved alpha, unless this property is set to 4, the alpha channel is processed the same as the image data, according to the value of the [ImageDataDiscard](#imagedatadiscard) property.</span></span>

### <a name="alphaquality"></a><span data-ttu-id="61ddb-258">AlphaQuality</span><span class="sxs-lookup"><span data-stu-id="61ddb-258">AlphaQuality</span></span>

<span data-ttu-id="61ddb-259">Legt die Komprimierungsqualität für das planare Alphakanalbild fest.</span><span class="sxs-lookup"><span data-stu-id="61ddb-259">Sets the compression quality for the planar alpha channel image.</span></span>



| <span data-ttu-id="61ddb-260">Datentyp</span><span class="sxs-lookup"><span data-stu-id="61ddb-260">Data type</span></span> | <span data-ttu-id="61ddb-261">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61ddb-261">VARTYPE</span></span>     | <span data-ttu-id="61ddb-262">Range</span><span class="sxs-lookup"><span data-stu-id="61ddb-262">Range</span></span> | <span data-ttu-id="61ddb-263">Standard</span><span class="sxs-lookup"><span data-stu-id="61ddb-263">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="61ddb-264">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="61ddb-264">**UCHAR**</span></span> | <span data-ttu-id="61ddb-265">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="61ddb-265">**VT\_UI1**</span></span> | <span data-ttu-id="61ddb-266">1–255</span><span class="sxs-lookup"><span data-stu-id="61ddb-266">1–255</span></span> | <span data-ttu-id="61ddb-267">1</span><span class="sxs-lookup"><span data-stu-id="61ddb-267">1</span></span>       |



 

<span data-ttu-id="61ddb-268">Diese Eigenschaft gilt, wenn das Bild über einen Alphakanal verfügt und die [InterleavedAlpha-Eigenschaft](#interleavedalpha) **VARIANT \_ FALSE** ist.</span><span class="sxs-lookup"><span data-stu-id="61ddb-268">This property applies when the image has an alpha channel and the [InterleavedAlpha](#interleavedalpha) property is **VARIANT\_FALSE**.</span></span> <span data-ttu-id="61ddb-269">Der Wert 1 gibt den verlustfreien Modus an.</span><span class="sxs-lookup"><span data-stu-id="61ddb-269">The value 1 indicates lossless mode.</span></span> <span data-ttu-id="61ddb-270">Steigende Werte führen zu höheren Komprimierungsverhältnissen und einer niedrigeren Imagequalität.</span><span class="sxs-lookup"><span data-stu-id="61ddb-270">Increasing values result in higher compression ratios and lower image quality.</span></span>

### <a name="bitmaptransform"></a><span data-ttu-id="61ddb-271">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="61ddb-271">BitmapTransform</span></span>

<span data-ttu-id="61ddb-272">Gibt an, ob das Bild beim Decodieren gedreht oder gekippt wird.</span><span class="sxs-lookup"><span data-stu-id="61ddb-272">Specifies whether the image is rotated or flipped when decoded.</span></span>



| <span data-ttu-id="61ddb-273">Datentyp</span><span class="sxs-lookup"><span data-stu-id="61ddb-273">Data type</span></span> | <span data-ttu-id="61ddb-274">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61ddb-274">VARTYPE</span></span>     | <span data-ttu-id="61ddb-275">Range</span><span class="sxs-lookup"><span data-stu-id="61ddb-275">Range</span></span>                                                                     | <span data-ttu-id="61ddb-276">Standard</span><span class="sxs-lookup"><span data-stu-id="61ddb-276">Default</span></span>                       |
|-----------|-------------|---------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="61ddb-277">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="61ddb-277">**UCHAR**</span></span> | <span data-ttu-id="61ddb-278">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="61ddb-278">**VT\_UI1**</span></span> | [<span data-ttu-id="61ddb-279">**WICBitmapTransformOptions**</span><span class="sxs-lookup"><span data-stu-id="61ddb-279">**WICBitmapTransformOptions**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | <span data-ttu-id="61ddb-280">**WICBitmapTransformRotate0**</span><span class="sxs-lookup"><span data-stu-id="61ddb-280">**WICBitmapTransformRotate0**</span></span> |



 

### <a name="compresseddomaintranscode"></a><span data-ttu-id="61ddb-281">CompressedDomainTranscode</span><span class="sxs-lookup"><span data-stu-id="61ddb-281">CompressedDomainTranscode</span></span>

<span data-ttu-id="61ddb-282">Aktiviert oder deaktiviert die komprimierte Domänentranscodierung.</span><span class="sxs-lookup"><span data-stu-id="61ddb-282">Enables or disables compressed domain transcoding.</span></span>



| <span data-ttu-id="61ddb-283">Datentyp</span><span class="sxs-lookup"><span data-stu-id="61ddb-283">Data type</span></span>         | <span data-ttu-id="61ddb-284">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61ddb-284">VARTYPE</span></span>      | <span data-ttu-id="61ddb-285">Standard</span><span class="sxs-lookup"><span data-stu-id="61ddb-285">Default</span></span>           |
|-------------------|--------------|-------------------|
| <span data-ttu-id="61ddb-286">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="61ddb-286">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="61ddb-287">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="61ddb-287">**VT\_BOOL**</span></span> | <span data-ttu-id="61ddb-288">**VARIANT \_ TRUE**</span><span class="sxs-lookup"><span data-stu-id="61ddb-288">**VARIANT\_TRUE**</span></span> |



 

<span data-ttu-id="61ddb-289">Legen Sie diese Eigenschaft auf **VARIANT \_ FALSE** fest, um komprimierte Domänenvorgänge zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="61ddb-289">To disable compressed domain operations, set this property to **VARIANT\_FALSE**.</span></span>

### <a name="frequencyorder"></a><span data-ttu-id="61ddb-290">FrequencyOrder</span><span class="sxs-lookup"><span data-stu-id="61ddb-290">FrequencyOrder</span></span>

<span data-ttu-id="61ddb-291">Aktiviert die Codierung in der Häufigkeitsreihenfolge.</span><span class="sxs-lookup"><span data-stu-id="61ddb-291">Enables encoding in frequency order.</span></span> <span data-ttu-id="61ddb-292">Geräteimplementierungen von JPEG XR-Encodern können eine Datei in räumlicher Reihenfolge organisieren, um den während der Codierung erforderlichen Arbeitsspeicher zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="61ddb-292">Device implementations of JPEG XR encoders can organize a file in spatial order to reduce the memory required during encoding.</span></span>



| <span data-ttu-id="61ddb-293">Datentyp</span><span class="sxs-lookup"><span data-stu-id="61ddb-293">Data type</span></span>         | <span data-ttu-id="61ddb-294">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61ddb-294">VARTYPE</span></span>      | <span data-ttu-id="61ddb-295">Standard</span><span class="sxs-lookup"><span data-stu-id="61ddb-295">Default</span></span>           |
|-------------------|--------------|-------------------|
| <span data-ttu-id="61ddb-296">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="61ddb-296">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="61ddb-297">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="61ddb-297">**VT\_BOOL**</span></span> | <span data-ttu-id="61ddb-298">**VARIANT \_ TRUE**</span><span class="sxs-lookup"><span data-stu-id="61ddb-298">**VARIANT\_TRUE**</span></span> |



 

-   <span data-ttu-id="61ddb-299">**VARIANT \_ TRUE:** Häufigkeitsreihenfolge.</span><span class="sxs-lookup"><span data-stu-id="61ddb-299">**VARIANT\_TRUE**: Frequency order.</span></span> <span data-ttu-id="61ddb-300">Die Daten mit der niedrigsten Häufigkeit werden zuerst in der Datei angezeigt, und der Bildinhalt wird nach der Häufigkeit und nicht nach der räumlichen Ausrichtung gruppiert.</span><span class="sxs-lookup"><span data-stu-id="61ddb-300">The lowest frequency data appears first in the file, and image content is grouped by its frequency rather than its spatial orientation.</span></span> <span data-ttu-id="61ddb-301">Das Organisieren einer Datei nach Häufigkeits reihenfolge bietet die beste Leistung für jede häufigkeitsbasierte Decodierung.</span><span class="sxs-lookup"><span data-stu-id="61ddb-301">Organizing a file by frequency order provides the best performance for any frequency-based decoding.</span></span>
-   <span data-ttu-id="61ddb-302">**VARIANT \_ FALSE:** Räumliche Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="61ddb-302">**VARIANT\_FALSE**: Spatial order.</span></span> <span data-ttu-id="61ddb-303">Die räumliche Reihenfolge reduziert den während der Codierung erforderlichen Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="61ddb-303">Spatial order reduces the memory required during encoding</span></span>

<span data-ttu-id="61ddb-304">Die Häufigkeits reihenfolge wird empfohlen, es sei denn, Sie haben leistungs- oder anwendungsspezifische Gründe für die Verwendung der räumlichen Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="61ddb-304">Frequency order is recommended unless you have performance or application-specific reasons to use spatial order.</span></span>

### <a name="horizontaltileslices"></a><span data-ttu-id="61ddb-305">HorizontalTileSlices</span><span class="sxs-lookup"><span data-stu-id="61ddb-305">HorizontalTileSlices</span></span>

<span data-ttu-id="61ddb-306">Legt die Anzahl horizontaler Kacheln fest.</span><span class="sxs-lookup"><span data-stu-id="61ddb-306">Sets the number of horizontal tiles.</span></span>



| <span data-ttu-id="61ddb-307">Datentyp</span><span class="sxs-lookup"><span data-stu-id="61ddb-307">Data type</span></span>  | <span data-ttu-id="61ddb-308">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61ddb-308">VARTYPE</span></span>     | <span data-ttu-id="61ddb-309">Range</span><span class="sxs-lookup"><span data-stu-id="61ddb-309">Range</span></span>  | <span data-ttu-id="61ddb-310">Standard</span><span class="sxs-lookup"><span data-stu-id="61ddb-310">Default</span></span>                      |
|------------|-------------|--------|------------------------------|
| <span data-ttu-id="61ddb-311">**Ushort**</span><span class="sxs-lookup"><span data-stu-id="61ddb-311">**USHORT**</span></span> | <span data-ttu-id="61ddb-312">**VT \_ UI2**</span><span class="sxs-lookup"><span data-stu-id="61ddb-312">**VT\_UI2**</span></span> | <span data-ttu-id="61ddb-313">0–4095</span><span class="sxs-lookup"><span data-stu-id="61ddb-313">0–4095</span></span> | <span data-ttu-id="61ddb-314">(Bildbreite – 1) >> 8</span><span class="sxs-lookup"><span data-stu-id="61ddb-314">(image width – 1) >> 8</span></span> |



 

<span data-ttu-id="61ddb-315">Der Wert ist die Anzahl horizontaler Unterteilungen. das heißt, die Anzahl der horizontalen Kacheln – 1.</span><span class="sxs-lookup"><span data-stu-id="61ddb-315">The value is the number of horizontal subdivisions; that is, the number of horizontal tiles – 1.</span></span>

### <a name="ignoreoverlap"></a><span data-ttu-id="61ddb-316">IgnoreOverlap</span><span class="sxs-lookup"><span data-stu-id="61ddb-316">IgnoreOverlap</span></span>

<span data-ttu-id="61ddb-317">Gibt an, wie der Encoder Kachelgrenzen während einer komprimierten Domänentranscodierung behandelt.</span><span class="sxs-lookup"><span data-stu-id="61ddb-317">Specifies how the encoder handles tile boundaries during a compressed domain transcode.</span></span>



| <span data-ttu-id="61ddb-318">Datentyp</span><span class="sxs-lookup"><span data-stu-id="61ddb-318">Data type</span></span>         | <span data-ttu-id="61ddb-319">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61ddb-319">VARTYPE</span></span>      | <span data-ttu-id="61ddb-320">Standard</span><span class="sxs-lookup"><span data-stu-id="61ddb-320">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="61ddb-321">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="61ddb-321">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="61ddb-322">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="61ddb-322">**VT\_BOOL**</span></span> | <span data-ttu-id="61ddb-323">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="61ddb-323">**VARIANT\_FALSE**</span></span> |



 

<span data-ttu-id="61ddb-324">Diese Eigenschaft wird nur angewendet, wenn die [CompressedDomainTranscode-Eigenschaft](#compresseddomaintranscode) auf **VARIANT \_ TRUE** festgelegt ist und eine Unterbereichstranscodierung mit genau einer oder mehreren Kacheln ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="61ddb-324">This property is applied only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE** and a sub-region transcode of exactly one or more tiles is performed.</span></span>

<span data-ttu-id="61ddb-325">Der Standardvorgang für eine Region-Transcodierung besteht im Erweitern des angeforderten Bereich um die umgebenden Pixel, die für die Überlappung der Bereichsränder erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="61ddb-325">The default operation for a region transcode is to expand the requested region to include the surrounding pixels that are required for overlap decoding of the region edges.</span></span> <span data-ttu-id="61ddb-326">Wenn diese Eigenschaft auf **VARIANT \_ TRUE festgelegt** ist, ignoriert der Codec die umgebenden Pixel, und nur die ausgewählten Kacheln werden extrahiert.</span><span class="sxs-lookup"><span data-stu-id="61ddb-326">If this property is set to **VARIANT\_TRUE**, the codec ignores the surrounding pixels, and only the selected tile or tiles are extracted.</span></span> <span data-ttu-id="61ddb-327">Wenn das Quellbild nicht gekachelt ist oder der angeforderte Bereich Teilkacheln enthält, wird dieser Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="61ddb-327">If the source image is not tiled or if the requested region includes partial tiles, this parameter is ignored.</span></span>

### <a name="imagedatadiscard"></a><span data-ttu-id="61ddb-328">ImageDataDiscard</span><span class="sxs-lookup"><span data-stu-id="61ddb-328">ImageDataDiscard</span></span>

<span data-ttu-id="61ddb-329">Legt die Menge der Bildfrequenzdaten fest, die während einer komprimierten Domänentranscodierung verworfen werden.</span><span class="sxs-lookup"><span data-stu-id="61ddb-329">Sets the amount of image frequency data to discard during a compressed domain transcode.</span></span>



| <span data-ttu-id="61ddb-330">Datentyp</span><span class="sxs-lookup"><span data-stu-id="61ddb-330">Data type</span></span> | <span data-ttu-id="61ddb-331">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61ddb-331">VARTYPE</span></span>     | <span data-ttu-id="61ddb-332">Range</span><span class="sxs-lookup"><span data-stu-id="61ddb-332">Range</span></span> | <span data-ttu-id="61ddb-333">Standard</span><span class="sxs-lookup"><span data-stu-id="61ddb-333">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="61ddb-334">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="61ddb-334">**UCHAR**</span></span> | <span data-ttu-id="61ddb-335">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="61ddb-335">**VT\_UI1**</span></span> | <span data-ttu-id="61ddb-336">0–3</span><span class="sxs-lookup"><span data-stu-id="61ddb-336">0–3</span></span>   | <span data-ttu-id="61ddb-337">0</span><span class="sxs-lookup"><span data-stu-id="61ddb-337">0</span></span>       |



 

<span data-ttu-id="61ddb-338">Diese Eigenschaft gilt nur, wenn [die CompressedDomainTranscode-Eigenschaft](#compresseddomaintranscode) auf **VARIANT \_ TRUE** festgelegt ist. Andernfalls wird sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="61ddb-338">This property applies only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE**; otherwise it is ignored.</span></span>



| <span data-ttu-id="61ddb-339">Wert</span><span class="sxs-lookup"><span data-stu-id="61ddb-339">Value</span></span> | <span data-ttu-id="61ddb-340">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="61ddb-340">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61ddb-341">0</span><span class="sxs-lookup"><span data-stu-id="61ddb-341">0</span></span>     | <span data-ttu-id="61ddb-342">Es werden keine Bildfrequenzdaten verworfen.</span><span class="sxs-lookup"><span data-stu-id="61ddb-342">No image frequency data is discarded.</span></span>                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="61ddb-343">1</span><span class="sxs-lookup"><span data-stu-id="61ddb-343">1</span></span>     | <span data-ttu-id="61ddb-344">Die Flexbits werden verworfen.</span><span class="sxs-lookup"><span data-stu-id="61ddb-344">The flexbits are discarded.</span></span> <span data-ttu-id="61ddb-345">Dadurch wird die Qualität des transcodierten Bilds willkürlich reduziert, ohne die effektive Auflösung des Bilds zu ändern.</span><span class="sxs-lookup"><span data-stu-id="61ddb-345">This arbitrarily reduces the quality of the transcoded image without changing the effective resolution of the image.</span></span> <span data-ttu-id="61ddb-346">Die genaue Verringerung der Dateigröße und -qualität hängt von zahlreichen Faktoren ab und kann nicht genau angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="61ddb-346">The exact reduction in file size and quality depends on numerous factors and cannot be exactly specified.</span></span> <span data-ttu-id="61ddb-347">Dieser Wert gibt einen Fehler zurück, der für einen überlappten Alphakanal angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="61ddb-347">This value returns an error specified for an interleaved alpha channel.</span></span>                                                                                |
| <span data-ttu-id="61ddb-348">2</span><span class="sxs-lookup"><span data-stu-id="61ddb-348">2</span></span>     | <span data-ttu-id="61ddb-349">Das Datenband mit hoher Durchgangshäufigkeit wird verworfen, einschließlich der Flexbits.</span><span class="sxs-lookup"><span data-stu-id="61ddb-349">The high-pass frequency data band is discarded, including the flexbits.</span></span> <span data-ttu-id="61ddb-350">Dadurch wird die Auflösung des transcodierten Bilds in beiden Dimensionen um den Faktor 4 reduziert.</span><span class="sxs-lookup"><span data-stu-id="61ddb-350">This reduces the resolution of the transcoded image by a factor of 4 in both dimensions.</span></span> <span data-ttu-id="61ddb-351">Die tatsächlichen Abmessungen des transcodierten Bilds bleiben unverändert, aber das Bild verliert alle Details in jedem 4x4-Pixelblock.</span><span class="sxs-lookup"><span data-stu-id="61ddb-351">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 4x4 block of pixels.</span></span> <span data-ttu-id="61ddb-352">Daher sollte das transcodierte Bild bei jeder Decodierung entsprechend herabsampelt werden.</span><span class="sxs-lookup"><span data-stu-id="61ddb-352">Therefore, the transcoded image should be downsampled accordingly whenever it is decoded.</span></span>                             |
| <span data-ttu-id="61ddb-353">3</span><span class="sxs-lookup"><span data-stu-id="61ddb-353">3</span></span>     | <span data-ttu-id="61ddb-354">Sowohl die Datenbänder mit hoher als auch niedriger Durchgangshäufigkeit werden verworfen, einschließlich der Flexbits.</span><span class="sxs-lookup"><span data-stu-id="61ddb-354">Both the high-pass and low-pass frequency data bands are discarded, including the flexbits.</span></span> <span data-ttu-id="61ddb-355">Dadurch wird die Auflösung des transcodierten Bilds in beiden Dimensionen um den Faktor 16 reduziert.</span><span class="sxs-lookup"><span data-stu-id="61ddb-355">This reduces the resolution of the transcoded image by a factor of 16 in both dimensions.</span></span> <span data-ttu-id="61ddb-356">Die tatsächlichen Abmessungen des transcodierten Bilds bleiben unverändert, aber das Bild verliert alle Details in jedem 16 x 16-Makroblock von Pixeln.</span><span class="sxs-lookup"><span data-stu-id="61ddb-356">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 16x16 macroblock of pixels.</span></span> <span data-ttu-id="61ddb-357">Daher sollte das transcodierte Bild bei jeder Decodierung entsprechend herabsampelt werden.</span><span class="sxs-lookup"><span data-stu-id="61ddb-357">Therefore, the transcoded image should be downsampled accordingly whenever it is decoded.</span></span> |



 

<span data-ttu-id="61ddb-358">Wenn das Bild einen überlappten Alphakanal enthält, wird der Wert von [ImageDataDiscard](#imagedatadiscard) auf den Alphakanal angewendet, es sei denn, die [AlphaDataDiscard-Eigenschaft](#alphadatadiscard) ist auf 4 festgelegt. In diesem Fall wird der Alphakanal verworfen.</span><span class="sxs-lookup"><span data-stu-id="61ddb-358">If the image contains an interleaved alpha channel, the value of [ImageDataDiscard](#imagedatadiscard) is applied to the alpha channel unless the [AlphaDataDiscard](#alphadatadiscard) property is set to 4, in which case the alpha channel is discarded.</span></span>

<span data-ttu-id="61ddb-359">Bei planaren Alphas werden die verworfenen Häufigkeitsdaten durch die [AlphaDataDiscard-Eigenschaft](#alphadatadiscard) gesteuert.</span><span class="sxs-lookup"><span data-stu-id="61ddb-359">For planar alpha, the frequency data that is discarded is controlled by the [AlphaDataDiscard](#alphadatadiscard) property.</span></span>

### <a name="imagequality"></a><span data-ttu-id="61ddb-360">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="61ddb-360">ImageQuality</span></span>

<span data-ttu-id="61ddb-361">Legt die Imagequalität fest.</span><span class="sxs-lookup"><span data-stu-id="61ddb-361">Sets the image quality.</span></span>



| <span data-ttu-id="61ddb-362">Datentyp</span><span class="sxs-lookup"><span data-stu-id="61ddb-362">Data type</span></span> | <span data-ttu-id="61ddb-363">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61ddb-363">VARTYPE</span></span>    | <span data-ttu-id="61ddb-364">Range</span><span class="sxs-lookup"><span data-stu-id="61ddb-364">Range</span></span> | <span data-ttu-id="61ddb-365">Standard</span><span class="sxs-lookup"><span data-stu-id="61ddb-365">Default</span></span> |
|-----------|------------|-------|---------|
| <span data-ttu-id="61ddb-366">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="61ddb-366">**FLOAT**</span></span> | <span data-ttu-id="61ddb-367">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="61ddb-367">**VT\_R4**</span></span> | <span data-ttu-id="61ddb-368">0–1.0</span><span class="sxs-lookup"><span data-stu-id="61ddb-368">0–1.0</span></span> | <span data-ttu-id="61ddb-369">0.9</span><span class="sxs-lookup"><span data-stu-id="61ddb-369">0.9</span></span>     |



 

<span data-ttu-id="61ddb-370">Ebene 1.0 bietet eine mathematische verlustfreie Komprimierung.</span><span class="sxs-lookup"><span data-stu-id="61ddb-370">Level 1.0 gives mathematically lossless compression.</span></span>

<span data-ttu-id="61ddb-371">Ebene 0.0 ist die Einstellung mit der niedrigsten Qualität.</span><span class="sxs-lookup"><span data-stu-id="61ddb-371">Level 0.0 is the lowest quality setting.</span></span>

### <a name="interleavedalpha"></a><span data-ttu-id="61ddb-372">InterleavedAlpha</span><span class="sxs-lookup"><span data-stu-id="61ddb-372">InterleavedAlpha</span></span>

<span data-ttu-id="61ddb-373">Gibt an, ob verleerte alpha- oder planare Alphas codiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="61ddb-373">Specifies whether to encode interleaved alpha or planar alpha.</span></span>



| <span data-ttu-id="61ddb-374">Datentyp</span><span class="sxs-lookup"><span data-stu-id="61ddb-374">Data type</span></span>         | <span data-ttu-id="61ddb-375">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61ddb-375">VARTYPE</span></span>      | <span data-ttu-id="61ddb-376">Standard</span><span class="sxs-lookup"><span data-stu-id="61ddb-376">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="61ddb-377">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="61ddb-377">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="61ddb-378">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="61ddb-378">**VT\_BOOL**</span></span> | <span data-ttu-id="61ddb-379">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="61ddb-379">**VARIANT\_FALSE**</span></span> |



 

-   <span data-ttu-id="61ddb-380">**VARIANT \_ TRUE:** Überlappter Alphawert.</span><span class="sxs-lookup"><span data-stu-id="61ddb-380">**VARIANT\_TRUE**: Interleaved alpha.</span></span> <span data-ttu-id="61ddb-381">Alphakanalinformationen werden als zusätzlicher verwebter Kanal ohne Korrelation mit den Bildinhaltskanälen codiert.</span><span class="sxs-lookup"><span data-stu-id="61ddb-381">Alpha channel information is encoded as an additional interleaved channel, with no correlation to the image content channels.</span></span> <span data-ttu-id="61ddb-382">Dieser Modus ist nützlich, um alpha gleichzeitig mit dem Bild zu decodieren, wenn das Bild gestreamt wird.</span><span class="sxs-lookup"><span data-stu-id="61ddb-382">This mode is useful for decoding alpha simultaneously with the image when the image is streaming.</span></span>
-   <span data-ttu-id="61ddb-383">VARIANT \_ FALSE: Planares Alpha.</span><span class="sxs-lookup"><span data-stu-id="61ddb-383">VARIANT\_FALSE: Planar alpha.</span></span> <span data-ttu-id="61ddb-384">Ein planarer Alphakanal wird als separates Bild codiert.</span><span class="sxs-lookup"><span data-stu-id="61ddb-384">A planar alpha channel is encoded as a separate image.</span></span> <span data-ttu-id="61ddb-385">Die Bilddaten und der Alphakanal werden unabhängig decodiert.</span><span class="sxs-lookup"><span data-stu-id="61ddb-385">The image data and the alpha channel are decoded independently.</span></span> <span data-ttu-id="61ddb-386">Optional können Sie die Qualitätsstufe des Alphakanals festlegen, indem Sie die [AlphaQuality-Eigenschaft](#alphaquality) festlegen.</span><span class="sxs-lookup"><span data-stu-id="61ddb-386">Optionally, you can set the quality level of the alpha channel by setting the [AlphaQuality](#alphaquality) property.</span></span>

<span data-ttu-id="61ddb-387">Überlappte Alphas werden nur für bestimmte RGB-Pixelformate unterstützt.</span><span class="sxs-lookup"><span data-stu-id="61ddb-387">Interleaved alpha is supported only for certain RGB pixel formats.</span></span> <span data-ttu-id="61ddb-388">Planares Alpha wird für jedes Bildformat unterstützt, das einen Alphakanal definiert.</span><span class="sxs-lookup"><span data-stu-id="61ddb-388">Planar alpha is supported for any image format that defines an alpha channel.</span></span>

### <a name="lossless"></a><span data-ttu-id="61ddb-389">Lossless</span><span class="sxs-lookup"><span data-stu-id="61ddb-389">Lossless</span></span>

<span data-ttu-id="61ddb-390">Aktiviert die Verlustkomprimierung.</span><span class="sxs-lookup"><span data-stu-id="61ddb-390">Enables losses compression.</span></span>



| <span data-ttu-id="61ddb-391">Datentyp</span><span class="sxs-lookup"><span data-stu-id="61ddb-391">Data type</span></span>         | <span data-ttu-id="61ddb-392">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61ddb-392">VARTYPE</span></span>      | <span data-ttu-id="61ddb-393">Standard</span><span class="sxs-lookup"><span data-stu-id="61ddb-393">Default</span></span>        |
|-------------------|--------------|----------------|
| <span data-ttu-id="61ddb-394">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="61ddb-394">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="61ddb-395">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="61ddb-395">**VT\_BOOL**</span></span> | <span data-ttu-id="61ddb-396">VARIANT \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="61ddb-396">VARIANT\_FALSE</span></span> |



 

<span data-ttu-id="61ddb-397">Wenn der Wert **VARIANT \_ TRUE ist,** verwendet der Encoder eine verlustfreie Komprimierung.</span><span class="sxs-lookup"><span data-stu-id="61ddb-397">If the value is **VARIANT\_TRUE**, the encoder uses lossless compression.</span></span> <span data-ttu-id="61ddb-398">Wenn diese Eigenschaft **auf VARIANT \_ TRUE festgelegt** ist, überschreibt diese Eigenschaft die [ImageQuality-Eigenschaft.](#imagequality)</span><span class="sxs-lookup"><span data-stu-id="61ddb-398">When set to **VARIANT\_TRUE**, this property overrides the [ImageQuality](#imagequality) property.</span></span>

### <a name="overlap"></a><span data-ttu-id="61ddb-399">Überlappung</span><span class="sxs-lookup"><span data-stu-id="61ddb-399">Overlap</span></span>

<span data-ttu-id="61ddb-400">Legt die Ebene der Überlappungsfilterung fest.</span><span class="sxs-lookup"><span data-stu-id="61ddb-400">Sets the level of overlap filtering.</span></span> <span data-ttu-id="61ddb-401">Bei der Überlappungsfilterung werden Transformationskoeffizienten über Block- und Makroblockgrenzen hinweg angewendet.</span><span class="sxs-lookup"><span data-stu-id="61ddb-401">With overlap filtering, transform coefficients are applied across block and macroblock boundaries.</span></span> <span data-ttu-id="61ddb-402">Dadurch können blockierende Artefakte reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="61ddb-402">This can reduce blocking artifacts.</span></span>



| <span data-ttu-id="61ddb-403">Datentyp</span><span class="sxs-lookup"><span data-stu-id="61ddb-403">Data type</span></span> | <span data-ttu-id="61ddb-404">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61ddb-404">VARTYPE</span></span>     | <span data-ttu-id="61ddb-405">Range</span><span class="sxs-lookup"><span data-stu-id="61ddb-405">Range</span></span> | <span data-ttu-id="61ddb-406">Standard</span><span class="sxs-lookup"><span data-stu-id="61ddb-406">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="61ddb-407">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="61ddb-407">**UCHAR**</span></span> | <span data-ttu-id="61ddb-408">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="61ddb-408">**VT\_UI1**</span></span> | <span data-ttu-id="61ddb-409">0–4</span><span class="sxs-lookup"><span data-stu-id="61ddb-409">0–4</span></span>   | <span data-ttu-id="61ddb-410">1</span><span class="sxs-lookup"><span data-stu-id="61ddb-410">1</span></span>       |



 



| <span data-ttu-id="61ddb-411">Wert</span><span class="sxs-lookup"><span data-stu-id="61ddb-411">Value</span></span> | <span data-ttu-id="61ddb-412">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="61ddb-412">Description</span></span>                                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="61ddb-413">0</span><span class="sxs-lookup"><span data-stu-id="61ddb-413">0</span></span>     | <span data-ttu-id="61ddb-414">Keine Überlappung.</span><span class="sxs-lookup"><span data-stu-id="61ddb-414">No overlap.</span></span>                                   |
| <span data-ttu-id="61ddb-415">1</span><span class="sxs-lookup"><span data-stu-id="61ddb-415">1</span></span>     | <span data-ttu-id="61ddb-416">Eine Ebene der Überlappung, soft tiling.</span><span class="sxs-lookup"><span data-stu-id="61ddb-416">One level of overlap, soft tiling.</span></span> <span data-ttu-id="61ddb-417">(Standardeinstellung)</span><span class="sxs-lookup"><span data-stu-id="61ddb-417">(Default.)</span></span> |
| <span data-ttu-id="61ddb-418">2</span><span class="sxs-lookup"><span data-stu-id="61ddb-418">2</span></span>     | <span data-ttu-id="61ddb-419">Zwei Ebenen der Überlappung, soft tiling.</span><span class="sxs-lookup"><span data-stu-id="61ddb-419">Two levels of overlap, soft tiling.</span></span>           |
| <span data-ttu-id="61ddb-420">3</span><span class="sxs-lookup"><span data-stu-id="61ddb-420">3</span></span>     | <span data-ttu-id="61ddb-421">Eine Ebene der Überlappung, harter Tiling</span><span class="sxs-lookup"><span data-stu-id="61ddb-421">One level of overlap, hard tiling</span></span>             |
| <span data-ttu-id="61ddb-422">4</span><span class="sxs-lookup"><span data-stu-id="61ddb-422">4</span></span>     | <span data-ttu-id="61ddb-423">Zwei Ebenen von Überlappungen, harte Kacheln.</span><span class="sxs-lookup"><span data-stu-id="61ddb-423">Two levels of overlap, hard tiling.</span></span>           |



 

<span data-ttu-id="61ddb-424">Definitionen:</span><span class="sxs-lookup"><span data-stu-id="61ddb-424">Definitions:</span></span>

-   <span data-ttu-id="61ddb-425">Eine Überlappungsebene: Die codierten Werte von 4x4-Blöcken werden basierend auf benachbarten Blöcken geändert.</span><span class="sxs-lookup"><span data-stu-id="61ddb-425">One level of overlap: The encoded values of 4x4 blocks are modified based on neighboring blocks.</span></span>
-   <span data-ttu-id="61ddb-426">Zwei Überlappungsebenen: Die erste Überlappungsebene wird angewendet.</span><span class="sxs-lookup"><span data-stu-id="61ddb-426">Two levels of overlap: The first level of overlap is applied.</span></span> <span data-ttu-id="61ddb-427">Darüber hinaus werden die codierten Werte von 16 x 16 Makroblocks basierend auf den benachbarten Makroblocks geändert.</span><span class="sxs-lookup"><span data-stu-id="61ddb-427">In addition, the encoded values of 16x16 macroblocks are modified based on the neighboring macroblocks.</span></span>
-   <span data-ttu-id="61ddb-428">Weiche Kacheln: Überlappende Filterung wird über Kachelgrenzen hinweg angewendet.</span><span class="sxs-lookup"><span data-stu-id="61ddb-428">Soft tiling: Overlap filtering is applied across tile boundaries.</span></span>
-   <span data-ttu-id="61ddb-429">Harte Kacheln: Die Filterung von Überlappungen wird nicht über Kachelgrenzen hinweg angewendet.</span><span class="sxs-lookup"><span data-stu-id="61ddb-429">Hard tiling: Overlap filtering is not applied across tile boundaries.</span></span> <span data-ttu-id="61ddb-430">Harte Kacheln können einige visuelle Artefakte entlang der Kachelgrenzen einführen.</span><span class="sxs-lookup"><span data-stu-id="61ddb-430">Hard tiles can introduce some visual artifacts along tile boundaries.</span></span>

<span data-ttu-id="61ddb-431">Wenn Sie diese Eigenschaft festlegen, legen Sie auch [UseCodecOptions](#usecodecoptions) auf **VARIANT \_ TRUE** fest.</span><span class="sxs-lookup"><span data-stu-id="61ddb-431">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="progressivemode"></a><span data-ttu-id="61ddb-432">ProgressiveMode</span><span class="sxs-lookup"><span data-stu-id="61ddb-432">ProgressiveMode</span></span>

<span data-ttu-id="61ddb-433">Aktiviert oder deaktiviert die progressive Codierung.</span><span class="sxs-lookup"><span data-stu-id="61ddb-433">Enables or disables progressive encoding.</span></span>



| <span data-ttu-id="61ddb-434">Datentyp</span><span class="sxs-lookup"><span data-stu-id="61ddb-434">Data type</span></span>         | <span data-ttu-id="61ddb-435">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61ddb-435">VARTYPE</span></span>      | <span data-ttu-id="61ddb-436">Standard</span><span class="sxs-lookup"><span data-stu-id="61ddb-436">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="61ddb-437">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="61ddb-437">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="61ddb-438">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="61ddb-438">**VT\_BOOL**</span></span> | <span data-ttu-id="61ddb-439">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="61ddb-439">**VARIANT\_FALSE**</span></span> |



 



| <span data-ttu-id="61ddb-440">Wert</span><span class="sxs-lookup"><span data-stu-id="61ddb-440">Value</span></span>              | <span data-ttu-id="61ddb-441">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="61ddb-441">Description</span></span>                |
|--------------------|----------------------------|
| <span data-ttu-id="61ddb-442">**VARIANT \_ TRUE**</span><span class="sxs-lookup"><span data-stu-id="61ddb-442">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="61ddb-443">Sequenzieller Modus (Standard).</span><span class="sxs-lookup"><span data-stu-id="61ddb-443">Sequential mode (default).</span></span> |
| <span data-ttu-id="61ddb-444">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="61ddb-444">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="61ddb-445">Progressiver Modus.</span><span class="sxs-lookup"><span data-stu-id="61ddb-445">Progressive mode.</span></span>          |



 

### <a name="quality"></a><span data-ttu-id="61ddb-446">Qualität</span><span class="sxs-lookup"><span data-stu-id="61ddb-446">Quality</span></span>

<span data-ttu-id="61ddb-447">Legt die Komprimierungsqualität fest.</span><span class="sxs-lookup"><span data-stu-id="61ddb-447">Sets the compression quality.</span></span>



| <span data-ttu-id="61ddb-448">Datentyp</span><span class="sxs-lookup"><span data-stu-id="61ddb-448">Data type</span></span> | <span data-ttu-id="61ddb-449">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61ddb-449">VARTYPE</span></span>     | <span data-ttu-id="61ddb-450">Range</span><span class="sxs-lookup"><span data-stu-id="61ddb-450">Range</span></span> | <span data-ttu-id="61ddb-451">Standard</span><span class="sxs-lookup"><span data-stu-id="61ddb-451">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="61ddb-452">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="61ddb-452">**UCHAR**</span></span> | <span data-ttu-id="61ddb-453">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="61ddb-453">**VT\_UI1**</span></span> | <span data-ttu-id="61ddb-454">1–255</span><span class="sxs-lookup"><span data-stu-id="61ddb-454">1–255</span></span> | <span data-ttu-id="61ddb-455">1</span><span class="sxs-lookup"><span data-stu-id="61ddb-455">1</span></span>       |



 

<span data-ttu-id="61ddb-456">Der Wert 1 gibt den verlustfreien Modus an.</span><span class="sxs-lookup"><span data-stu-id="61ddb-456">The value 1 indicates lossless mode.</span></span> <span data-ttu-id="61ddb-457">Steigende Werte führen zu höheren Komprimierungsverhältnissen und einer niedrigeren Imagequalität.</span><span class="sxs-lookup"><span data-stu-id="61ddb-457">Increasing values result in higher compression ratios and lower image quality.</span></span>

<span data-ttu-id="61ddb-458">Wenn Sie diese Eigenschaft festlegen, legen Sie auch [UseCodecOptions](#usecodecoptions) auf **VARIANT \_ TRUE** fest.</span><span class="sxs-lookup"><span data-stu-id="61ddb-458">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="streamonly"></a><span data-ttu-id="61ddb-459">StreamOnly</span><span class="sxs-lookup"><span data-stu-id="61ddb-459">StreamOnly</span></span>

<span data-ttu-id="61ddb-460">Aktiviert oder deaktiviert den reinen Streammodus.</span><span class="sxs-lookup"><span data-stu-id="61ddb-460">Enables or disables stream-only mode.</span></span>



| <span data-ttu-id="61ddb-461">Datentyp</span><span class="sxs-lookup"><span data-stu-id="61ddb-461">Data type</span></span>         | <span data-ttu-id="61ddb-462">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61ddb-462">VARTYPE</span></span>      | <span data-ttu-id="61ddb-463">Standard</span><span class="sxs-lookup"><span data-stu-id="61ddb-463">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="61ddb-464">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="61ddb-464">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="61ddb-465">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="61ddb-465">**VT\_BOOL**</span></span> | <span data-ttu-id="61ddb-466">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="61ddb-466">**VARIANT\_FALSE**</span></span> |



 



| <span data-ttu-id="61ddb-467">Wert</span><span class="sxs-lookup"><span data-stu-id="61ddb-467">Value</span></span>              | <span data-ttu-id="61ddb-468">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="61ddb-468">Description</span></span>                                                            |
|--------------------|------------------------------------------------------------------------|
| <span data-ttu-id="61ddb-469">**VARIANT \_ TRUE**</span><span class="sxs-lookup"><span data-stu-id="61ddb-469">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="61ddb-470">Der Encoder gibt den unformatierten Bilddatenstrom ohne Metadaten aus.</span><span class="sxs-lookup"><span data-stu-id="61ddb-470">The encoder outputs the raw image stream without metadata.</span></span>             |
| <span data-ttu-id="61ddb-471">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="61ddb-471">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="61ddb-472">Der Encoder gibt das Containerformat (Bilddatenstrom plus Metadaten) aus.</span><span class="sxs-lookup"><span data-stu-id="61ddb-472">The encoder outputs the container format (image stream plus metadata).</span></span> |



 

### <a name="subsampling"></a><span data-ttu-id="61ddb-473">Untersampling</span><span class="sxs-lookup"><span data-stu-id="61ddb-473">Subsampling</span></span>

<span data-ttu-id="61ddb-474">Legt die Subsampling für die -Subsampling fest.</span><span class="sxs-lookup"><span data-stu-id="61ddb-474">Sets the chroma subsampling.</span></span> <span data-ttu-id="61ddb-475">Diese Eigenschaft gilt nur für RGB-Bilder.</span><span class="sxs-lookup"><span data-stu-id="61ddb-475">This property applies only to RGB images.</span></span>



| <span data-ttu-id="61ddb-476">Datentyp</span><span class="sxs-lookup"><span data-stu-id="61ddb-476">Data type</span></span> | <span data-ttu-id="61ddb-477">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61ddb-477">VARTYPE</span></span>     | <span data-ttu-id="61ddb-478">Range</span><span class="sxs-lookup"><span data-stu-id="61ddb-478">Range</span></span> | <span data-ttu-id="61ddb-479">Standard</span><span class="sxs-lookup"><span data-stu-id="61ddb-479">Default</span></span>                                                  |
|-----------|-------------|-------|----------------------------------------------------------|
| <span data-ttu-id="61ddb-480">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="61ddb-480">**UCHAR**</span></span> | <span data-ttu-id="61ddb-481">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="61ddb-481">**VT\_UI1**</span></span> | <span data-ttu-id="61ddb-482">0–3</span><span class="sxs-lookup"><span data-stu-id="61ddb-482">0–3</span></span>   | <span data-ttu-id="61ddb-483">3, wenn [ImageQuality](#imagequality) 0.8 >; andernfalls 1</span><span class="sxs-lookup"><span data-stu-id="61ddb-483">3 if [ImageQuality](#imagequality) > 0.8; otherwise 1</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="61ddb-484">Wert</span><span class="sxs-lookup"><span data-stu-id="61ddb-484">Value</span></span></th>
<th><span data-ttu-id="61ddb-485">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="61ddb-485">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="61ddb-486">3</span><span class="sxs-lookup"><span data-stu-id="61ddb-486">3</span></span></td>
<td><span data-ttu-id="61ddb-487">4:4:4-Codierung.</span><span class="sxs-lookup"><span data-stu-id="61ddb-487">4:4:4 encoding.</span></span> <span data-ttu-id="61ddb-488">Behält die vollständige Auflösung bei.</span><span class="sxs-lookup"><span data-stu-id="61ddb-488">Preserves full chroma resolution.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61ddb-489">2</span><span class="sxs-lookup"><span data-stu-id="61ddb-489">2</span></span></td>
<td><span data-ttu-id="61ddb-490">4:2:2-Codierung.</span><span class="sxs-lookup"><span data-stu-id="61ddb-490">4:2:2 encoding.</span></span> <span data-ttu-id="61ddb-491">Die Auflösung von 1/2 der Leuchtdichte beträgt 1/2.</span><span class="sxs-lookup"><span data-stu-id="61ddb-491">Chroma resolution is ½ of luminance resolution.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61ddb-492">1</span><span class="sxs-lookup"><span data-stu-id="61ddb-492">1</span></span></td>
<td><span data-ttu-id="61ddb-493">4:2:0-Codierung.</span><span class="sxs-lookup"><span data-stu-id="61ddb-493">4:2:0 encoding.</span></span> <span data-ttu-id="61ddb-494">Die Auflösung von 1/4 der Leuchtdichte beträgt 1/4.</span><span class="sxs-lookup"><span data-stu-id="61ddb-494">Chroma resolution is ¼ of luminance resolution.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61ddb-495">0</span><span class="sxs-lookup"><span data-stu-id="61ddb-495">0</span></span></td>
<td><span data-ttu-id="61ddb-496">4:0:0-Codierung.</span><span class="sxs-lookup"><span data-stu-id="61ddb-496">4:0:0 encoding.</span></span> <span data-ttu-id="61ddb-497">Verwirft alle Werte und behält nur die Leuchtdichte bei.</span><span class="sxs-lookup"><span data-stu-id="61ddb-497">Discards all chroma values and preserves luminance only.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="61ddb-498">Dieser Modus wird nicht empfohlen, da der Codec eine leicht geänderte Definition der Leuchtdichte verwendet, um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="61ddb-498">This mode is not recommended, because the codec uses a slightly modified definition of luminance to improve performance.</span></span> <span data-ttu-id="61ddb-499">Stattdessen ist es besser, das Bild vor der Codierung in monocolore zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="61ddb-499">Instead, it is better to convert the image to monochrome before encoding.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="61ddb-500">4:2:2 und 4:2:0 behalten die Leuchtdichtedetails auf Kosten der Farbdetails bei.</span><span class="sxs-lookup"><span data-stu-id="61ddb-500">4:2:2 and 4:2:0 preserve luminance detail at the expense of color detail.</span></span>

<span data-ttu-id="61ddb-501">Wenn Sie diese Eigenschaft festlegen, legen Sie auch [UseCodecOptions](#usecodecoptions) auf **VARIANT \_ TRUE** fest.</span><span class="sxs-lookup"><span data-stu-id="61ddb-501">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="usecodecoptions"></a><span data-ttu-id="61ddb-502">UseCodecOptions</span><span class="sxs-lookup"><span data-stu-id="61ddb-502">UseCodecOptions</span></span>

<span data-ttu-id="61ddb-503">Gibt an, ob die Eigenschaften [Quality,](#image-quality-settings) [Overlap](#overlap)und [Subsampling](#subsampling) anstelle der generischen [ImageQuality-Eigenschaft](#imagequality) verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="61ddb-503">Specifies whether to use the [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties instead of the generic [ImageQuality](#imagequality) property.</span></span>



| <span data-ttu-id="61ddb-504">Datentyp</span><span class="sxs-lookup"><span data-stu-id="61ddb-504">Data type</span></span>         | <span data-ttu-id="61ddb-505">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61ddb-505">VARTYPE</span></span>      | <span data-ttu-id="61ddb-506">Standard</span><span class="sxs-lookup"><span data-stu-id="61ddb-506">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="61ddb-507">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="61ddb-507">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="61ddb-508">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="61ddb-508">**VT\_BOOL**</span></span> | <span data-ttu-id="61ddb-509">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="61ddb-509">**VARIANT\_FALSE**</span></span> |



 

### <a name="verticaltileslices"></a><span data-ttu-id="61ddb-510">VerticalTileSlices</span><span class="sxs-lookup"><span data-stu-id="61ddb-510">VerticalTileSlices</span></span>

<span data-ttu-id="61ddb-511">Legt die Anzahl horizontaler Kacheln fest.</span><span class="sxs-lookup"><span data-stu-id="61ddb-511">Sets the number of horizontal tiles.</span></span>



| <span data-ttu-id="61ddb-512">Datentyp</span><span class="sxs-lookup"><span data-stu-id="61ddb-512">Data type</span></span>  | <span data-ttu-id="61ddb-513">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61ddb-513">VARTYPE</span></span>     | <span data-ttu-id="61ddb-514">Range</span><span class="sxs-lookup"><span data-stu-id="61ddb-514">Range</span></span>  | <span data-ttu-id="61ddb-515">Standard</span><span class="sxs-lookup"><span data-stu-id="61ddb-515">Default</span></span>                       |
|------------|-------------|--------|-------------------------------|
| <span data-ttu-id="61ddb-516">**Ushort**</span><span class="sxs-lookup"><span data-stu-id="61ddb-516">**USHORT**</span></span> | <span data-ttu-id="61ddb-517">**VT \_ UI2**</span><span class="sxs-lookup"><span data-stu-id="61ddb-517">**VT\_UI2**</span></span> | <span data-ttu-id="61ddb-518">0–4095</span><span class="sxs-lookup"><span data-stu-id="61ddb-518">0–4095</span></span> | <span data-ttu-id="61ddb-519">(Bildhöhe – 1) >> 8</span><span class="sxs-lookup"><span data-stu-id="61ddb-519">(image height – 1) >> 8</span></span> |



 

<span data-ttu-id="61ddb-520">Der Wert ist die Anzahl der vertikalen Unterteilungen. Das heißt, die Anzahl der vertikalen Kacheln – 1.</span><span class="sxs-lookup"><span data-stu-id="61ddb-520">The value is the number of vertical subdivisions; that is, the number of vertical tiles – 1.</span></span>

## <a name="supported-color-formats"></a><span data-ttu-id="61ddb-521">Unterstützte Farbformate</span><span class="sxs-lookup"><span data-stu-id="61ddb-521">Supported Color Formats</span></span>

<span data-ttu-id="61ddb-522">Weitere Informationen zu diesen Formaten finden Sie unter [Native PixelFormate.](-wic-codec-native-pixel-formats.md)</span><span class="sxs-lookup"><span data-stu-id="61ddb-522">For more information about these formats, see [Native Pixel Formats](-wic-codec-native-pixel-formats.md).</span></span>

-   <span data-ttu-id="61ddb-523">**Ganzzahlige RGB-Formate**</span><span class="sxs-lookup"><span data-stu-id="61ddb-523">**Integer RGB formats**</span></span>
    -   <span data-ttu-id="61ddb-524">GUID \_ WICPixelFormat24bppRGB</span><span class="sxs-lookup"><span data-stu-id="61ddb-524">GUID\_WICPixelFormat24bppRGB</span></span>
    -   <span data-ttu-id="61ddb-525">GUID \_ WICPixelFormat24bppBGR</span><span class="sxs-lookup"><span data-stu-id="61ddb-525">GUID\_WICPixelFormat24bppBGR</span></span>
    -   <span data-ttu-id="61ddb-526">GUID \_ WICPixelFormat32bppBGR</span><span class="sxs-lookup"><span data-stu-id="61ddb-526">GUID\_WICPixelFormat32bppBGR</span></span>
    -   <span data-ttu-id="61ddb-527">GUID \_ WICPixelFormat48bppRGB</span><span class="sxs-lookup"><span data-stu-id="61ddb-527">GUID\_WICPixelFormat48bppRGB</span></span>
    -   <span data-ttu-id="61ddb-528">GUID \_ WICPixelFormat32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="61ddb-528">GUID\_WICPixelFormat32bppBGRA</span></span>
    -   <span data-ttu-id="61ddb-529">GUID \_ WICPixelFormat64bppRGBA</span><span class="sxs-lookup"><span data-stu-id="61ddb-529">GUID\_WICPixelFormat64bppRGBA</span></span>
    -   <span data-ttu-id="61ddb-530">GUID \_ WICPixelFormat32bppPBGRA</span><span class="sxs-lookup"><span data-stu-id="61ddb-530">GUID\_WICPixelFormat32bppPBGRA</span></span>
    -   <span data-ttu-id="61ddb-531">GUID \_ WICPixelFormat64bppPRGBA</span><span class="sxs-lookup"><span data-stu-id="61ddb-531">GUID\_WICPixelFormat64bppPRGBA</span></span>
-   <span data-ttu-id="61ddb-532">**RGB-Formate mit festem Punkt**</span><span class="sxs-lookup"><span data-stu-id="61ddb-532">**Fixed-point RGB formats**</span></span>
    -   <span data-ttu-id="61ddb-533">GUID \_ WICPixelFormat48bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="61ddb-533">GUID\_WICPixelFormat48bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="61ddb-534">GUID \_ WICPixelFormat64bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="61ddb-534">GUID\_WICPixelFormat64bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="61ddb-535">GUID \_ WICPixelFormat96bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="61ddb-535">GUID\_WICPixelFormat96bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="61ddb-536">GUID \_ WICPixelFormat128bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="61ddb-536">GUID\_WICPixelFormat128bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="61ddb-537">GUID \_ WICPixelFormat128bppRGBAFixedPoint</span><span class="sxs-lookup"><span data-stu-id="61ddb-537">GUID\_WICPixelFormat128bppRGBAFixedPoint</span></span>
-   <span data-ttu-id="61ddb-538">**RGB-Gleitkommaformate**</span><span class="sxs-lookup"><span data-stu-id="61ddb-538">**Floating-point RGB formats**</span></span>
    -   <span data-ttu-id="61ddb-539">GUID \_ WICPixelFormat48bppRGBHalf</span><span class="sxs-lookup"><span data-stu-id="61ddb-539">GUID\_WICPixelFormat48bppRGBHalf</span></span>
    -   <span data-ttu-id="61ddb-540">GUID \_ WICPixelFormat64bppRGBHalf</span><span class="sxs-lookup"><span data-stu-id="61ddb-540">GUID\_WICPixelFormat64bppRGBHalf</span></span>
    -   <span data-ttu-id="61ddb-541">GUID \_ WICPixelFormat128bppRGBFloat</span><span class="sxs-lookup"><span data-stu-id="61ddb-541">GUID\_WICPixelFormat128bppRGBFloat</span></span>
    -   <span data-ttu-id="61ddb-542">GUID \_ WICPixelFormat64bppRGBAFixedPoint</span><span class="sxs-lookup"><span data-stu-id="61ddb-542">GUID\_WICPixelFormat64bppRGBAFixedPoint</span></span>
    -   <span data-ttu-id="61ddb-543">GUID \_ WICPixelFormat64bppRGBAHalf</span><span class="sxs-lookup"><span data-stu-id="61ddb-543">GUID\_WICPixelFormat64bppRGBAHalf</span></span>
    -   <span data-ttu-id="61ddb-544">GUID \_ WICPixelFormat128bppRGBAFloat</span><span class="sxs-lookup"><span data-stu-id="61ddb-544">GUID\_WICPixelFormat128bppRGBAFloat</span></span>
    -   <span data-ttu-id="61ddb-545">GUID \_ WICPixelFormat128bppPRGBAFloat</span><span class="sxs-lookup"><span data-stu-id="61ddb-545">GUID\_WICPixelFormat128bppPRGBAFloat</span></span>
-   <span data-ttu-id="61ddb-546">**Graustufenformate**</span><span class="sxs-lookup"><span data-stu-id="61ddb-546">**Grayscale formats**</span></span>
    -   <span data-ttu-id="61ddb-547">GUID \_ WICPixelFormat8bppGray</span><span class="sxs-lookup"><span data-stu-id="61ddb-547">GUID\_WICPixelFormat8bppGray</span></span>
    -   <span data-ttu-id="61ddb-548">GUID \_ WICPixelFormat16bppGray</span><span class="sxs-lookup"><span data-stu-id="61ddb-548">GUID\_WICPixelFormat16bppGray</span></span>
    -   <span data-ttu-id="61ddb-549">GUID \_ WICPixelFormat16bppGrayFixedPoint</span><span class="sxs-lookup"><span data-stu-id="61ddb-549">GUID\_WICPixelFormat16bppGrayFixedPoint</span></span>
    -   <span data-ttu-id="61ddb-550">GUID \_ WICPixelFormat16bppGrayHalf</span><span class="sxs-lookup"><span data-stu-id="61ddb-550">GUID\_WICPixelFormat16bppGrayHalf</span></span>
    -   <span data-ttu-id="61ddb-551">GUID \_ WICPixelFormat32bppGrayFixedPoint</span><span class="sxs-lookup"><span data-stu-id="61ddb-551">GUID\_WICPixelFormat32bppGrayFixedPoint</span></span>
    -   <span data-ttu-id="61ddb-552">GUID \_ WICPixelFormat32bppGrayFloat</span><span class="sxs-lookup"><span data-stu-id="61ddb-552">GUID\_WICPixelFormat32bppGrayFloat</span></span>
-   <span data-ttu-id="61ddb-553">**Gepackte Formate**</span><span class="sxs-lookup"><span data-stu-id="61ddb-553">**Packed formats**</span></span>
    -   <span data-ttu-id="61ddb-554">GUID \_ WICPixelFormat16bppBGR555</span><span class="sxs-lookup"><span data-stu-id="61ddb-554">GUID\_WICPixelFormat16bppBGR555</span></span>
    -   <span data-ttu-id="61ddb-555">GUID \_ WICPixelFormat16bppBGR565</span><span class="sxs-lookup"><span data-stu-id="61ddb-555">GUID\_WICPixelFormat16bppBGR565</span></span>
    -   <span data-ttu-id="61ddb-556">GUID \_ WICPixelFormat32bppBGR101010</span><span class="sxs-lookup"><span data-stu-id="61ddb-556">GUID\_WICPixelFormat32bppBGR101010</span></span>
    -   <span data-ttu-id="61ddb-557">GUID \_ WICPixelFormat32bppRGBE</span><span class="sxs-lookup"><span data-stu-id="61ddb-557">GUID\_WICPixelFormat32bppRGBE</span></span>
-   <span data-ttu-id="61ddb-558">**CMYK-Formate**</span><span class="sxs-lookup"><span data-stu-id="61ddb-558">**CMYK formats**</span></span>
    -   <span data-ttu-id="61ddb-559">GUID \_ WICPixelFormat40bppCMYKAlpha</span><span class="sxs-lookup"><span data-stu-id="61ddb-559">GUID\_WICPixelFormat40bppCMYKAlpha</span></span>
    -   <span data-ttu-id="61ddb-560">GUID \_ WICPixelFormat64bppCMYK</span><span class="sxs-lookup"><span data-stu-id="61ddb-560">GUID\_WICPixelFormat64bppCMYK</span></span>
    -   <span data-ttu-id="61ddb-561">GUID \_ WICPixelFormat80bppCMYKAlpha</span><span class="sxs-lookup"><span data-stu-id="61ddb-561">GUID\_WICPixelFormat80bppCMYKAlpha</span></span>
-   <span data-ttu-id="61ddb-562">**N-Kanal-Formate**</span><span class="sxs-lookup"><span data-stu-id="61ddb-562">**N-channel formats**</span></span>
    -   <span data-ttu-id="61ddb-563">GUID \_ WICPixelFormat32bpp4Channels</span><span class="sxs-lookup"><span data-stu-id="61ddb-563">GUID\_WICPixelFormat32bpp4Channels</span></span>
    -   <span data-ttu-id="61ddb-564">GUID \_ WICPixelFormat40bpp5Channels</span><span class="sxs-lookup"><span data-stu-id="61ddb-564">GUID\_WICPixelFormat40bpp5Channels</span></span>
    -   <span data-ttu-id="61ddb-565">GUID \_ WICPixelFormat48bpp6Channels</span><span class="sxs-lookup"><span data-stu-id="61ddb-565">GUID\_WICPixelFormat48bpp6Channels</span></span>
    -   <span data-ttu-id="61ddb-566">GUID \_ WICPixelFormat56bpp7Channels</span><span class="sxs-lookup"><span data-stu-id="61ddb-566">GUID\_WICPixelFormat56bpp7Channels</span></span>
    -   <span data-ttu-id="61ddb-567">GUID \_ WICPixelFormat64bpp8Channels</span><span class="sxs-lookup"><span data-stu-id="61ddb-567">GUID\_WICPixelFormat64bpp8Channels</span></span>
    -   <span data-ttu-id="61ddb-568">GUID \_ WICPixelFormat32bpp3ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="61ddb-568">GUID\_WICPixelFormat32bpp3ChannelsAlpha</span></span>
    -   <span data-ttu-id="61ddb-569">GUID \_ WICPixelFormat40bpp4ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="61ddb-569">GUID\_WICPixelFormat40bpp4ChannelsAlpha</span></span>
    -   <span data-ttu-id="61ddb-570">GUID \_ WICPixelFormat48bpp5ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="61ddb-570">GUID\_WICPixelFormat48bpp5ChannelsAlpha</span></span>
    -   <span data-ttu-id="61ddb-571">GUID \_ WICPixelFormat56bpp6ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="61ddb-571">GUID\_WICPixelFormat56bpp6ChannelsAlpha</span></span>
    -   <span data-ttu-id="61ddb-572">GUID \_ WICPixelFormat64bpp7ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="61ddb-572">GUID\_WICPixelFormat64bpp7ChannelsAlpha</span></span>
    -   <span data-ttu-id="61ddb-573">GUID \_ WICPixelFormat72bpp8ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="61ddb-573">GUID\_WICPixelFormat72bpp8ChannelsAlpha</span></span>
    -   <span data-ttu-id="61ddb-574">GUID \_ WICPixelFormat48bpp3Channels</span><span class="sxs-lookup"><span data-stu-id="61ddb-574">GUID\_WICPixelFormat48bpp3Channels</span></span>
    -   <span data-ttu-id="61ddb-575">GUID \_ WICPixelFormat64bpp4Channels</span><span class="sxs-lookup"><span data-stu-id="61ddb-575">GUID\_WICPixelFormat64bpp4Channels</span></span>
    -   <span data-ttu-id="61ddb-576">GUID \_ WICPixelFormat80bpp5Channels</span><span class="sxs-lookup"><span data-stu-id="61ddb-576">GUID\_WICPixelFormat80bpp5Channels</span></span>
    -   <span data-ttu-id="61ddb-577">GUID \_ WICPixelFormat96bpp6Channels</span><span class="sxs-lookup"><span data-stu-id="61ddb-577">GUID\_WICPixelFormat96bpp6Channels</span></span>
    -   <span data-ttu-id="61ddb-578">GUID \_ WICPixelFormat128bpp8Channels</span><span class="sxs-lookup"><span data-stu-id="61ddb-578">GUID\_WICPixelFormat128bpp8Channels</span></span>
    -   <span data-ttu-id="61ddb-579">GUID \_ WICPixelFormat64bpp3ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="61ddb-579">GUID\_WICPixelFormat64bpp3ChannelsAlpha</span></span>
    -   <span data-ttu-id="61ddb-580">GUID \_ WICPixelFormat80bpp4ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="61ddb-580">GUID\_WICPixelFormat80bpp4ChannelsAlpha</span></span>
    -   <span data-ttu-id="61ddb-581">GUID \_ WICPixelFormat96bpp5ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="61ddb-581">GUID\_WICPixelFormat96bpp5ChannelsAlpha</span></span>
    -   <span data-ttu-id="61ddb-582">GUID \_ WICPixelFormat112bpp6ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="61ddb-582">GUID\_WICPixelFormat112bpp6ChannelsAlpha</span></span>
    -   <span data-ttu-id="61ddb-583">GUID \_ WICPixelFormat128bpp7ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="61ddb-583">GUID\_WICPixelFormat128bpp7ChannelsAlpha</span></span>
    -   <span data-ttu-id="61ddb-584">GUID \_ WICPixelFormat144bpp8ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="61ddb-584">GUID\_WICPixelFormat144bpp8ChannelsAlpha</span></span>

 

 
