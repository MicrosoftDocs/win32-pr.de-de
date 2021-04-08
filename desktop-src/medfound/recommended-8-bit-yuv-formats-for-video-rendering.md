---
description: Empfohlene 8-Bit-YUV-Formate für Video Rendering
ms.assetid: 675d4c60-4c58-4f15-9bae-ffb0c389c608
title: Empfohlene 8-Bit-YUV-Formate für Video Rendering
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4505eb17f833040e0148ac98912f16af860b55b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753889"
---
# <a name="recommended-8-bit-yuv-formats-for-video-rendering"></a><span data-ttu-id="1cc01-103">Empfohlene 8-Bit-YUV-Formate für Video Rendering</span><span class="sxs-lookup"><span data-stu-id="1cc01-103">Recommended 8-Bit YUV Formats for Video Rendering</span></span>

<span data-ttu-id="1cc01-104">Gary Sullivan und Stephen estrop</span><span class="sxs-lookup"><span data-stu-id="1cc01-104">Gary Sullivan and Stephen Estrop</span></span>

<span data-ttu-id="1cc01-105">Microsoft Corporation</span><span class="sxs-lookup"><span data-stu-id="1cc01-105">Microsoft Corporation</span></span>

<span data-ttu-id="1cc01-106">2002. April, aktualisiert: 2008. November</span><span class="sxs-lookup"><span data-stu-id="1cc01-106">April 2002, updated November 2008</span></span>

<span data-ttu-id="1cc01-107">In diesem Thema werden die 8-Bit-YUV-Farb Formate beschrieben, die für Video Rendering im Windows-Betriebssystem empfohlen werden.</span><span class="sxs-lookup"><span data-stu-id="1cc01-107">This topic describes the 8-bit YUV color formats that are recommended for video rendering in the Windows operating system.</span></span> <span data-ttu-id="1cc01-108">In diesem Artikel werden die Verfahren für die Typumwandlung zwischen YUV-und RGB-Formaten und Techniken zum Upsampling von YUV-Formaten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1cc01-108">This article presents techniques for converting between YUV and RGB formats, and also provides techniques for upsampling YUV formats.</span></span> <span data-ttu-id="1cc01-109">Dieser Artikel richtet sich an jeden Benutzer, der mit dem Entschlüsseln oder Rendern von YUV-Videos in Windows arbeitet.</span><span class="sxs-lookup"><span data-stu-id="1cc01-109">This article is intended for anyone working with YUV video decoding or rendering in Windows.</span></span>

## <a name="introduction"></a><span data-ttu-id="1cc01-110">Einführung</span><span class="sxs-lookup"><span data-stu-id="1cc01-110">Introduction</span></span>

<span data-ttu-id="1cc01-111">Viele YUV-Formate werden in der gesamten Videobranche definiert.</span><span class="sxs-lookup"><span data-stu-id="1cc01-111">Numerous YUV formats are defined throughout the video industry.</span></span> <span data-ttu-id="1cc01-112">In diesem Artikel werden die 8-Bit-YUV-Formate beschrieben, die für Video Rendering in Windows empfohlen werden.</span><span class="sxs-lookup"><span data-stu-id="1cc01-112">This article identifies the 8-bit YUV formats that are recommended for video rendering in Windows.</span></span> <span data-ttu-id="1cc01-113">Decoder-und Anzeige Hersteller werden empfohlen, die in diesem Artikel beschriebenen Formate zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="1cc01-113">Decoder vendors and display vendors are encouraged to support the formats described in this article.</span></span> <span data-ttu-id="1cc01-114">In diesem Artikel werden keine anderen Verwendungsmöglichkeiten von YUV-Farben behandelt, wie z. b. immer noch Fotos.</span><span class="sxs-lookup"><span data-stu-id="1cc01-114">This article does not address other uses of YUV color, such as still photography.</span></span>

<span data-ttu-id="1cc01-115">Die in diesem Artikel beschriebenen Formate verwenden alle 8 Bits pro Pixel-Speicherort, um den Y-Kanal (auch als "Luma Channel" bezeichnet) zu codieren, und verwenden 8 Bits pro Stichprobe, um jedes U-oder V Chroma-Beispiel zu codieren.</span><span class="sxs-lookup"><span data-stu-id="1cc01-115">The formats described in this article all use 8 bits per pixel location to encode the Y channel (also called the luma channel), and use 8 bits per sample to encode each U or V chroma sample.</span></span> <span data-ttu-id="1cc01-116">In den meisten YUV-Formaten werden im Durchschnitt weniger als 24 Bits pro Pixel verwendet, da Sie weniger Stichproben von Ihnen und V als von Y enthalten. In diesem Artikel werden keine YUV-Formate mit 10-Bit-oder höheren Y-Kanälen behandelt.</span><span class="sxs-lookup"><span data-stu-id="1cc01-116">However, most YUV formats use fewer than 24 bits per pixel on average, because they contain fewer samples of U and V than of Y. This article does not cover YUV formats with 10-bit or higher Y channels.</span></span>

> [!Note]  
> <span data-ttu-id="1cc01-117">Für den Zweck dieses Artikels entspricht der Begriff "U" dem Wert von "CB", und der Begriff "V" entspricht CR.</span><span class="sxs-lookup"><span data-stu-id="1cc01-117">For the purposes of this article, the term U is equivalent to Cb, and the term V is equivalent to Cr.</span></span>

 

<span data-ttu-id="1cc01-118">In diesem Artikel werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="1cc01-118">This article covers the following topics:</span></span>

-   <span data-ttu-id="1cc01-119">[YUV-Stichprobenentnahme](#yuv-sampling).</span><span class="sxs-lookup"><span data-stu-id="1cc01-119">[YUV Sampling](#yuv-sampling).</span></span> <span data-ttu-id="1cc01-120">Beschreibt die gängigsten YUV-Stichproben Techniken.</span><span class="sxs-lookup"><span data-stu-id="1cc01-120">Describes the most common YUV sampling techniques.</span></span>
-   <span data-ttu-id="1cc01-121">[Oberflächen Definitionen](#surface-definitions).</span><span class="sxs-lookup"><span data-stu-id="1cc01-121">[Surface Definitions](#surface-definitions).</span></span> <span data-ttu-id="1cc01-122">Beschreibt die empfohlenen YUV-Formate.</span><span class="sxs-lookup"><span data-stu-id="1cc01-122">Describes the recommended YUV formats.</span></span>
-   <span data-ttu-id="1cc01-123">[Farb Raum-und Chroma-Samplingrate](#color-space-and-chroma-sampling-rate-conversions).</span><span class="sxs-lookup"><span data-stu-id="1cc01-123">[Color Space and Chroma Sampling Rate Conversions](#color-space-and-chroma-sampling-rate-conversions).</span></span> <span data-ttu-id="1cc01-124">Hier finden Sie einige Richtlinien für die Typumwandlung zwischen YUV-und RGB-Formaten sowie für die zwischen unterschiedlichen YUV</span><span class="sxs-lookup"><span data-stu-id="1cc01-124">Provides some guidelines for converting between YUV and RGB formats and for converting between different YUV formats.</span></span>
-   <span data-ttu-id="1cc01-125">[Erkennen von YUV-Formaten in Media Foundation](#identifying-yuv-formats-in-media-foundation).</span><span class="sxs-lookup"><span data-stu-id="1cc01-125">[Identifying YUV Formats in Media Foundation](#identifying-yuv-formats-in-media-foundation).</span></span> <span data-ttu-id="1cc01-126">Erläutert das Beschreiben von YUV-Format Typen in Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="1cc01-126">Explains how to describe YUV format types in Media Foundation.</span></span>

## <a name="yuv-sampling"></a><span data-ttu-id="1cc01-127">YUV-Stichprobe</span><span class="sxs-lookup"><span data-stu-id="1cc01-127">YUV Sampling</span></span>

<span data-ttu-id="1cc01-128">Chroma-Kanäle können eine niedrigere Samplingrate als der Luma-Kanal aufweisen, ohne dass ein dramatischer Verlust der perzeptive Qualität auftritt.</span><span class="sxs-lookup"><span data-stu-id="1cc01-128">Chroma channels can have a lower sampling rate than the luma channel, without any dramatic loss of perceptual quality.</span></span> <span data-ttu-id="1cc01-129">Eine Notation mit der Bezeichnung "a:b: C" wird verwendet, um zu beschreiben, wie oft Sie und V in Relation zu Y als Stichprobe verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="1cc01-129">A notation called the "A:B:C" notation is used to describe how often U and V are sampled relative to Y:</span></span>

-   <span data-ttu-id="1cc01-130">4:4:4 bedeutet, dass die Chroma-Kanäle nicht herabgestuft werden.</span><span class="sxs-lookup"><span data-stu-id="1cc01-130">4:4:4 means no downsampling of the chroma channels.</span></span>
-   <span data-ttu-id="1cc01-131">4:2:2 bedeutet 2:1 horizontale Downsampling ohne vertikale Downsampling.</span><span class="sxs-lookup"><span data-stu-id="1cc01-131">4:2:2 means 2:1 horizontal downsampling, with no vertical downsampling.</span></span> <span data-ttu-id="1cc01-132">Jede Scanzeile enthält vier Y-Beispiele für alle zwei U-oder V-Beispiele.</span><span class="sxs-lookup"><span data-stu-id="1cc01-132">Every scan line contains four Y samples for every two U or V samples.</span></span>
-   <span data-ttu-id="1cc01-133">4:2:0 bedeutet 2:1 horizontale Downsampling mit 2:1 vertikaler Downsampling.</span><span class="sxs-lookup"><span data-stu-id="1cc01-133">4:2:0 means 2:1 horizontal downsampling, with 2:1 vertical downsampling.</span></span>
-   <span data-ttu-id="1cc01-134">4:1:1 bedeutet 4:1 horizontale Downsampling ohne vertikale Downsampling.</span><span class="sxs-lookup"><span data-stu-id="1cc01-134">4:1:1 means 4:1 horizontal downsampling, with no vertical downsampling.</span></span> <span data-ttu-id="1cc01-135">Jede Scanzeile enthält vier Y-Beispiele für jedes Sie und jede V-Stichprobe.</span><span class="sxs-lookup"><span data-stu-id="1cc01-135">Every scan line contains four Y samples for each U and V sample.</span></span> <span data-ttu-id="1cc01-136">4:1:1 die Stichprobenentnahme ist weniger häufig als andere Formate und wird in diesem Artikel nicht ausführlich erläutert.</span><span class="sxs-lookup"><span data-stu-id="1cc01-136">4:1:1 sampling is less common than other formats, and is not discussed in detail in this article.</span></span>

<span data-ttu-id="1cc01-137">Die folgenden Diagramme zeigen, wie Chroma für jede der Verkleinerung-Raten Stichproben erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1cc01-137">The following diagrams shows how chroma is sampled for each of the downsampling rates.</span></span> <span data-ttu-id="1cc01-138">Luma-Beispiele werden durch ein Kreuz dargestellt, und Chroma-Beispiele werden durch einen Kreis dargestellt.</span><span class="sxs-lookup"><span data-stu-id="1cc01-138">Luma samples are represented by a cross, and chroma samples are represented by a circle.</span></span>

![Abbildung 1.](images/yuv-sampling-grids.png)

<span data-ttu-id="1cc01-141">Die vorherrschende Form der 4:2:2-Stichprobenentnahme wird in der ITU-R-Empfehlung BT BT. 601.</span><span class="sxs-lookup"><span data-stu-id="1cc01-141">The dominant form of 4:2:2 sampling is defined in ITU-R Recommendation BT.601.</span></span> <span data-ttu-id="1cc01-142">Es gibt zwei häufige Varianten der 4:2:0-Stichprobenentnahme.</span><span class="sxs-lookup"><span data-stu-id="1cc01-142">There are two common variants of 4:2:0 sampling.</span></span> <span data-ttu-id="1cc01-143">Eines dieser werden in MPEG-2-Video und das andere in MPEG-1 und in den ITU-T-Empfehlungen H. 261 und h. 263 verwendet.</span><span class="sxs-lookup"><span data-stu-id="1cc01-143">One of these is used in MPEG-2 video, and the other is used in MPEG-1 and in ITU-T Recommendations H.261 and H.263.</span></span>

<span data-ttu-id="1cc01-144">Im Vergleich zum MPEG-1-Schema ist es einfacher, zwischen dem MPEG-2-Schema und den für 4:2:2-und 4:4:4-Formaten definierten Samplings zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="1cc01-144">Compared with the MPEG-1 scheme, it is simpler to convert between the MPEG-2 scheme and the sampling grids defined for 4:2:2 and 4:4:4 formats.</span></span> <span data-ttu-id="1cc01-145">Aus diesem Grund wird das MPEG-2-Schema in Windows bevorzugt und sollte als Standardinterpretation von 4:2:0-Formaten angesehen werden.</span><span class="sxs-lookup"><span data-stu-id="1cc01-145">For this reason, the MPEG-2 scheme is preferred in Windows, and should be considered the default interpretation of 4:2:0 formats.</span></span>

## <a name="surface-definitions"></a><span data-ttu-id="1cc01-146">Oberflächen Definitionen</span><span class="sxs-lookup"><span data-stu-id="1cc01-146">Surface Definitions</span></span>

<span data-ttu-id="1cc01-147">In diesem Abschnitt werden die 8-Bit-YUV-Formate beschrieben, die für Video Rendering empfohlen werden.</span><span class="sxs-lookup"><span data-stu-id="1cc01-147">This section describes the 8-bit YUV formats that are recommended for video rendering.</span></span> <span data-ttu-id="1cc01-148">Diese sind in verschiedene Kategorien unterteilt:</span><span class="sxs-lookup"><span data-stu-id="1cc01-148">These fall into several categories:</span></span>

-   [<span data-ttu-id="1cc01-149">4:4:4 Formate, 32 Bits pro Pixel</span><span class="sxs-lookup"><span data-stu-id="1cc01-149">4:4:4 Formats, 32 Bits per Pixel</span></span>](#444-formats-32-bits-per-pixel)
-   [<span data-ttu-id="1cc01-150">4:2:2 Formate, 16 Bits pro Pixel</span><span class="sxs-lookup"><span data-stu-id="1cc01-150">4:2:2 Formats, 16 Bits per Pixel</span></span>](#422-formats-16-bits-per-pixel)
-   [<span data-ttu-id="1cc01-151">4:2:0 Formate, 16 Bits pro Pixel</span><span class="sxs-lookup"><span data-stu-id="1cc01-151">4:2:0 Formats, 16 Bits per Pixel</span></span>](#420-formats-16-bits-per-pixel)
-   [<span data-ttu-id="1cc01-152">4:2:0 Formate, 12 Bits pro Pixel</span><span class="sxs-lookup"><span data-stu-id="1cc01-152">4:2:0 Formats, 12 Bits per Pixel</span></span>](#420-formats-12-bits-per-pixel)

<span data-ttu-id="1cc01-153">Zuerst sollten Sie die folgenden Konzepte kennen, um zu verstehen, was folgt:</span><span class="sxs-lookup"><span data-stu-id="1cc01-153">First, you should be aware of the following concepts in order to understand what follows:</span></span>

-   <span data-ttu-id="1cc01-154">*Oberflächen Ursprung*.</span><span class="sxs-lookup"><span data-stu-id="1cc01-154">*Surface origin*.</span></span> <span data-ttu-id="1cc01-155">Bei den in diesem Artikel beschriebenen YUV-Formaten steht der Ursprung (0,0) immer in der oberen linken Ecke der Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="1cc01-155">For the YUV formats described in this article, the origin (0,0) is always the top left corner of the surface.</span></span>
-   <span data-ttu-id="1cc01-156">*Stride*.</span><span class="sxs-lookup"><span data-stu-id="1cc01-156">*Stride*.</span></span> <span data-ttu-id="1cc01-157">Der Stride einer Oberfläche (manchmal auch als "Tonhöhe" bezeichnet) ist die Breite der Oberfläche (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="1cc01-157">The stride of a surface, sometimes called the pitch, is the width of the surface in bytes.</span></span> <span data-ttu-id="1cc01-158">Wenn ein Oberflächen Ursprung in der oberen linken Ecke liegt, ist der Stride immer positiv.</span><span class="sxs-lookup"><span data-stu-id="1cc01-158">Given a surface origin at the top left corner, the stride is always positive.</span></span>
-   <span data-ttu-id="1cc01-159">*Ausrichtung*.</span><span class="sxs-lookup"><span data-stu-id="1cc01-159">*Alignment*.</span></span> <span data-ttu-id="1cc01-160">Die Ausrichtung einer Oberfläche liegt im Ermessen des Grafik Anzeige Treibers.</span><span class="sxs-lookup"><span data-stu-id="1cc01-160">The alignment of a surface is at the discretion of the graphics display driver.</span></span> <span data-ttu-id="1cc01-161">Die Oberfläche muss immer DWORD-bündig sein. Das heißt, dass einzelne Zeilen innerhalb der Oberfläche von einer 32-Bit-Grenze (DWORD) ausgehen.</span><span class="sxs-lookup"><span data-stu-id="1cc01-161">The surface must always be DWORD aligned; that is, individual lines within the surface are guaranteed to originate on a 32-bit (DWORD) boundary.</span></span> <span data-ttu-id="1cc01-162">Die Ausrichtung kann jedoch je nach den Anforderungen der Hardware größer als 32 Bits sein.</span><span class="sxs-lookup"><span data-stu-id="1cc01-162">The alignment can be larger than 32 bits, however, depending on the needs of the hardware.</span></span>
-   <span data-ttu-id="1cc01-163">Gepacktes Format im Vergleich zum planaren Format.</span><span class="sxs-lookup"><span data-stu-id="1cc01-163">Packed format versus planar format.</span></span> <span data-ttu-id="1cc01-164">YUV-Formate sind in *gepackte* Formate und *planare* Formate unterteilt.</span><span class="sxs-lookup"><span data-stu-id="1cc01-164">YUV formats are divided into *packed* formats and *planar* formats.</span></span> <span data-ttu-id="1cc01-165">In einem gepackten Format werden die Y-, U-und V-Komponenten in einem einzelnen Array gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1cc01-165">In a packed format, the Y, U, and V components are stored in a single array.</span></span> <span data-ttu-id="1cc01-166">Pixel sind in Gruppen von macropixels organisiert, deren Layout vom Format abhängt.</span><span class="sxs-lookup"><span data-stu-id="1cc01-166">Pixels are organized into groups of macropixels, whose layout depends on the format.</span></span> <span data-ttu-id="1cc01-167">In einem planaren Format werden die Y-, U-und V-Komponenten als drei separate Ebenen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1cc01-167">In a planar format, the Y, U, and V components are stored as three separate planes.</span></span>

<span data-ttu-id="1cc01-168">Jedes in diesem Artikel beschriebene YUV-Format verfügt über einen zugewiesenen FourCC-Code.</span><span class="sxs-lookup"><span data-stu-id="1cc01-168">Each of the YUV formats described in this article has an assigned FOURCC code.</span></span> <span data-ttu-id="1cc01-169">Bei einem FourCC-Code handelt es sich um eine 32-Bit-Ganzzahl ohne Vorzeichen, die durch Verkettung von vier ASCII-Zeichen erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1cc01-169">A FOURCC code is a 32-bit unsigned integer that is created by concatenating four ASCII characters.</span></span>

-   <span data-ttu-id="1cc01-170">4:4:4 (32 bpp)</span><span class="sxs-lookup"><span data-stu-id="1cc01-170">4:4:4 (32 bpp)</span></span>
    -   [<span data-ttu-id="1cc01-171">Ayuv</span><span class="sxs-lookup"><span data-stu-id="1cc01-171">AYUV</span></span>](#ayuv)
-   <span data-ttu-id="1cc01-172">4:2:2 (16 bpp)</span><span class="sxs-lookup"><span data-stu-id="1cc01-172">4:2:2 (16 bpp)</span></span>
    -   [<span data-ttu-id="1cc01-173">Im YUY2</span><span class="sxs-lookup"><span data-stu-id="1cc01-173">YUY2</span></span>](#yuy2)
    -   [<span data-ttu-id="1cc01-174">UYVY</span><span class="sxs-lookup"><span data-stu-id="1cc01-174">UYVY</span></span>](#uyvy)
-   <span data-ttu-id="1cc01-175">4:2:0 (16 bpp)</span><span class="sxs-lookup"><span data-stu-id="1cc01-175">4:2:0 (16 bpp)</span></span>
    -   [<span data-ttu-id="1cc01-176">IMC1</span><span class="sxs-lookup"><span data-stu-id="1cc01-176">IMC1</span></span>](#imc1)
    -   [<span data-ttu-id="1cc01-177">IMC3</span><span class="sxs-lookup"><span data-stu-id="1cc01-177">IMC3</span></span>](#imc3)
-   <span data-ttu-id="1cc01-178">4:2:0 (12 BPP)</span><span class="sxs-lookup"><span data-stu-id="1cc01-178">4:2:0 (12 bpp)</span></span>
    -   [<span data-ttu-id="1cc01-179">IMC2</span><span class="sxs-lookup"><span data-stu-id="1cc01-179">IMC2</span></span>](#imc2)
    -   [<span data-ttu-id="1cc01-180">IMC4</span><span class="sxs-lookup"><span data-stu-id="1cc01-180">IMC4</span></span>](#imc4)
    -   [<span data-ttu-id="1cc01-181">YV12</span><span class="sxs-lookup"><span data-stu-id="1cc01-181">YV12</span></span>](#yv12)
    -   [<span data-ttu-id="1cc01-182">NV12</span><span class="sxs-lookup"><span data-stu-id="1cc01-182">NV12</span></span>](#nv12)

## <a name="444-formats-32-bits-per-pixel"></a><span data-ttu-id="1cc01-183">4:4:4 Formate, 32 Bits pro Pixel</span><span class="sxs-lookup"><span data-stu-id="1cc01-183">4:4:4 Formats, 32 Bits per Pixel</span></span>

### <a name="ayuv"></a><span data-ttu-id="1cc01-184">Ayuv</span><span class="sxs-lookup"><span data-stu-id="1cc01-184">AYUV</span></span>

<span data-ttu-id="1cc01-185">Ein einzelnes 4:4:4-Format wird mit dem FourCC-Code ayuv empfohlen.</span><span class="sxs-lookup"><span data-stu-id="1cc01-185">A single 4:4:4 format is recommended, with the FOURCC code AYUV.</span></span> <span data-ttu-id="1cc01-186">Dabei handelt es sich um ein gepacktes Format, bei dem jedes Pixel in der in der folgenden Abbildung gezeigten Reihenfolge als vier aufeinanderfolgende Bytes codiert wird.</span><span class="sxs-lookup"><span data-stu-id="1cc01-186">This is a packed format, where each pixel is encoded as four consecutive bytes, arranged in the sequence shown in the following illustration.</span></span>

![Abbildung 2.](images/yuvformats01.gif)

<span data-ttu-id="1cc01-189">Die markierten Bytes enthalten Werte für Alpha.</span><span class="sxs-lookup"><span data-stu-id="1cc01-189">The bytes marked A contain values for alpha.</span></span>

## <a name="422-formats-16-bits-per-pixel"></a><span data-ttu-id="1cc01-190">4:2:2 Formate, 16 Bits pro Pixel</span><span class="sxs-lookup"><span data-stu-id="1cc01-190">4:2:2 Formats, 16 Bits per Pixel</span></span>

<span data-ttu-id="1cc01-191">Es werden zwei 4:2:2-Formate mit den folgenden FOURCC-Codes empfohlen:</span><span class="sxs-lookup"><span data-stu-id="1cc01-191">Two 4:2:2 formats are recommended, with the following FOURCC codes:</span></span>

-   <span data-ttu-id="1cc01-192">Im YUY2</span><span class="sxs-lookup"><span data-stu-id="1cc01-192">YUY2</span></span>
-   <span data-ttu-id="1cc01-193">UYVY</span><span class="sxs-lookup"><span data-stu-id="1cc01-193">UYVY</span></span>

<span data-ttu-id="1cc01-194">Beide sind gepackte Formate, wobei jedes Makro Pixel zwei Pixel als vier aufeinanderfolgende Bytes codiert ist.</span><span class="sxs-lookup"><span data-stu-id="1cc01-194">Both are packed formats, where each macropixel is two pixels encoded as four consecutive bytes.</span></span> <span data-ttu-id="1cc01-195">Dies führt zu einem horizontalen Verkleinerung des Chroma mit einem Faktor von zwei.</span><span class="sxs-lookup"><span data-stu-id="1cc01-195">This results in horizontal downsampling of the chroma by a factor of two.</span></span>

### <a name="yuy2"></a><span data-ttu-id="1cc01-196">Im YUY2</span><span class="sxs-lookup"><span data-stu-id="1cc01-196">YUY2</span></span>

<span data-ttu-id="1cc01-197">Im im YUY2-Format können die Daten als Array nicht signierter **char** -Werte behandelt werden, wobei das erste Byte das erste y-Beispiel enthält, das zweite Byte das erste U (CB)-Beispiel, das dritte Byte das zweite y-Beispiel und das vierte Byte das erste V-Beispiel (CR), wie im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="1cc01-197">In YUY2 format, the data can be treated as an array of unsigned **char** values, where the first byte contains the first Y sample, the second byte contains the first U (Cb) sample, the third byte contains the second Y sample, and the fourth byte contains the first V (Cr) sample, as shown in the following diagram.</span></span>

![Abbildung 3.](images/yuvformats02.gif)

<span data-ttu-id="1cc01-200">Wenn das Bild als Array von Little-enumdian- **Wort** Werten adressiert wird, enthält das erste **Wort** das erste Y-Beispiel in der unwichtigsten Bits (LSB) und das erste U (CB)-Beispiel in den signifikantesten Bits (MSB).</span><span class="sxs-lookup"><span data-stu-id="1cc01-200">If the image is addressed as an array of little-endian **WORD** values, the first **WORD** contains the first Y sample in the least significant bits (LSBs) and the first U (Cb) sample in the most significant bits (MSBs).</span></span> <span data-ttu-id="1cc01-201">Das zweite **Wort** enthält das zweite Y-Beispiel im lssb und das erste V (CR)-Beispiel in MSSB.</span><span class="sxs-lookup"><span data-stu-id="1cc01-201">The second **WORD** contains the second Y sample in the LSBs and the first V (Cr) sample in the MSBs.</span></span>

<span data-ttu-id="1cc01-202">Im YUY2 ist das bevorzugte 4:2:2-Pixel-Format für die Microsoft DirectX-Video Beschleunigung (DirectX VA).</span><span class="sxs-lookup"><span data-stu-id="1cc01-202">YUY2 is the preferred 4:2:2 pixel format for Microsoft DirectX Video Acceleration (DirectX VA).</span></span> <span data-ttu-id="1cc01-203">Es wird erwartet, dass es sich um eine langfristige Anforderung für DirectX VA Accelerators handelt, die 4:2:2-Video unterstützen.</span><span class="sxs-lookup"><span data-stu-id="1cc01-203">It is expected to be an intermediate-term requirement for DirectX VA accelerators supporting 4:2:2 video.</span></span>

### <a name="uyvy"></a><span data-ttu-id="1cc01-204">UYVY</span><span class="sxs-lookup"><span data-stu-id="1cc01-204">UYVY</span></span>

<span data-ttu-id="1cc01-205">Dieses Format ist mit dem im YUY2-Format identisch, mit dem Unterschied, dass die Byte Reihenfolge umgekehrt ist – d. h., die Chroma-und Luma-Bytes werden gekippt (Abbildung 4).</span><span class="sxs-lookup"><span data-stu-id="1cc01-205">This format is the same as the YUY2 format except the byte order is reversed—that is, the chroma and luma bytes are flipped (Figure 4).</span></span> <span data-ttu-id="1cc01-206">Wenn das Bild als ein Array von zwei Little-enumdian- **Wort** Werten adressiert wird, enthält das erste **Wort** U in den lssb und y0 in den MSSB, und das zweite **Wort** enthält V in den lssb und Y1 in den MSSB.</span><span class="sxs-lookup"><span data-stu-id="1cc01-206">If the image is addressed as an array of two little-endian **WORD** values, the first **WORD** contains U in the LSBs and Y0 in the MSBs, and the second **WORD** contains V in the LSBs and Y1 in the MSBs.</span></span>

![Abbildung 4.](images/yuvformats03.gif)

## <a name="420-formats-16-bits-per-pixel"></a><span data-ttu-id="1cc01-209">4:2:0 Formate, 16 Bits pro Pixel</span><span class="sxs-lookup"><span data-stu-id="1cc01-209">4:2:0 Formats, 16 Bits per Pixel</span></span>

<span data-ttu-id="1cc01-210">Es werden zwei 4:2:0 16-Bits pro Pixel-Format (BPP) mit den folgenden FOURCC-Codes empfohlen:</span><span class="sxs-lookup"><span data-stu-id="1cc01-210">Two 4:2:0 16-bits per pixel (bpp) formats are recommended, with the following FOURCC codes:</span></span>

-   <span data-ttu-id="1cc01-211">IMC1</span><span class="sxs-lookup"><span data-stu-id="1cc01-211">IMC1</span></span>
-   <span data-ttu-id="1cc01-212">IMC3</span><span class="sxs-lookup"><span data-stu-id="1cc01-212">IMC3</span></span>

<span data-ttu-id="1cc01-213">Beide YUV-Formate sind Planare Formate.</span><span class="sxs-lookup"><span data-stu-id="1cc01-213">Both of these YUV formats are planar formats.</span></span> <span data-ttu-id="1cc01-214">Die Chroma-Kanäle werden von einem Faktor von zwei in den horizontalen und vertikalen Dimensionen Subsampling.</span><span class="sxs-lookup"><span data-stu-id="1cc01-214">The chroma channels are subsampled by a factor of two in both the horizontal and vertical dimensions.</span></span>

### <a name="imc1"></a><span data-ttu-id="1cc01-215">IMC1</span><span class="sxs-lookup"><span data-stu-id="1cc01-215">IMC1</span></span>

<span data-ttu-id="1cc01-216">Alle Y-Beispiele werden als erstes im Arbeitsspeicher als Array nicht signierter **char** -Werte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1cc01-216">All of the Y samples appear first in memory as an array of unsigned **char** values.</span></span> <span data-ttu-id="1cc01-217">Anschließend werden alle V-Beispiele (CR) und dann alle U (CB)-Beispiele angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1cc01-217">This is followed by all of the V (Cr) samples, and then all of the U (Cb) samples.</span></span> <span data-ttu-id="1cc01-218">Die Flächen "V" und "U" haben den gleichen Schritt wie die Y-Ebene, was zu nicht verwendeten Speicherbereichen führt, wie in Abbildung 5 dargestellt.</span><span class="sxs-lookup"><span data-stu-id="1cc01-218">The V and U planes have the same stride as the Y plane, resulting in unused areas of memory, as shown in Figure 5.</span></span> <span data-ttu-id="1cc01-219">Die Ebenen "You" und "V" müssen an Speicher Begrenzungen beginnen, die ein Vielfaches von 16 Zeilen sind.</span><span class="sxs-lookup"><span data-stu-id="1cc01-219">The U and V planes must start on memory boundaries that are a multiple of 16 lines.</span></span> <span data-ttu-id="1cc01-220">Abbildung 5 zeigt den Ursprung von Ihnen und V für einen Video Frame mit 352 x 240.</span><span class="sxs-lookup"><span data-stu-id="1cc01-220">Figure 5 shows the origin of U and V for a 352 x 240 video frame.</span></span> <span data-ttu-id="1cc01-221">Die Startadresse der Ebenen "You" und "V" wird wie folgt berechnet:</span><span class="sxs-lookup"><span data-stu-id="1cc01-221">The starting address of the U and V planes are calculated as follows:</span></span>

``` syntax
BYTE* pV = pY + (((Height + 15) & ~15) * Stride);
BYTE* pU = pY + (((((Height * 3) / 2) + 15) & ~15) * Stride);
```

<span data-ttu-id="1cc01-222">Dabei ist *pY* ein Byte Zeiger auf den Anfang des Speicherarrays, wie im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="1cc01-222">where *pY* is a byte pointer to the start of the memory array, as shown in the following diagram.</span></span>

![Abbildung 5.](images/yuvformats04.gif)

### <a name="imc3"></a><span data-ttu-id="1cc01-225">IMC3</span><span class="sxs-lookup"><span data-stu-id="1cc01-225">IMC3</span></span>

<span data-ttu-id="1cc01-226">Dieses Format ist mit IMC1 identisch, mit dem Unterschied, dass Sie und die V-Ebenen ausgetauscht werden, wie im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="1cc01-226">This format is identical to IMC1, except the U and V planes are swapped, as shown in the following diagram.</span></span>

![Abbildung 6.](images/yuvformats05.gif)

## <a name="420-formats-12-bits-per-pixel"></a><span data-ttu-id="1cc01-229">4:2:0 Formate, 12 Bits pro Pixel</span><span class="sxs-lookup"><span data-stu-id="1cc01-229">4:2:0 Formats, 12 Bits per Pixel</span></span>

<span data-ttu-id="1cc01-230">Vier 4:2:0 12-bpp-Formate werden mit den folgenden FOURCC-Codes empfohlen:</span><span class="sxs-lookup"><span data-stu-id="1cc01-230">Four 4:2:0 12-bpp formats are recommended, with the following FOURCC codes:</span></span>

-   <span data-ttu-id="1cc01-231">IMC2</span><span class="sxs-lookup"><span data-stu-id="1cc01-231">IMC2</span></span>
-   <span data-ttu-id="1cc01-232">IMC4</span><span class="sxs-lookup"><span data-stu-id="1cc01-232">IMC4</span></span>
-   <span data-ttu-id="1cc01-233">YV12</span><span class="sxs-lookup"><span data-stu-id="1cc01-233">YV12</span></span>
-   <span data-ttu-id="1cc01-234">NV12</span><span class="sxs-lookup"><span data-stu-id="1cc01-234">NV12</span></span>

<span data-ttu-id="1cc01-235">In allen diesen Formaten werden die Chroma-Kanäle in den horizontalen und vertikalen Dimensionen durch einen Faktor von zwei Subsampling.</span><span class="sxs-lookup"><span data-stu-id="1cc01-235">In all of these formats, the chroma channels are subsampled by a factor of two in both the horizontal and vertical dimensions.</span></span>

### <a name="imc2"></a><span data-ttu-id="1cc01-236">IMC2</span><span class="sxs-lookup"><span data-stu-id="1cc01-236">IMC2</span></span>

<span data-ttu-id="1cc01-237">Dieses Format ist identisch mit IMC1, mit Ausnahme des folgenden Unterschieds: die Zeilen V (CR) und U (CB) sind über Schneidevorgänge mit halber Stride-Grenze.</span><span class="sxs-lookup"><span data-stu-id="1cc01-237">This format is the same as IMC1 except for the following difference: The V (Cr) and U (Cb) lines are interleaved at half-stride boundaries.</span></span> <span data-ttu-id="1cc01-238">Mit anderen Worten, jede vollständige Zeile im Bereich Chroma beginnt mit einer Reihe von V-Beispielen, gefolgt von einer Reihe von U-Beispielen, die an der nächsten Hälfte der nächsten Grenze beginnen (Abbildung 7).</span><span class="sxs-lookup"><span data-stu-id="1cc01-238">In other words, each full-stride line in the chroma area starts with a line of V samples, followed by a line of U samples that begins at the next half-stride boundary (Figure 7).</span></span> <span data-ttu-id="1cc01-239">Mit diesem Layout wird der Adressraum effizienter genutzt als IMC1.</span><span class="sxs-lookup"><span data-stu-id="1cc01-239">This layout makes more efficient use of address space than IMC1.</span></span> <span data-ttu-id="1cc01-240">Er schneidet den Chroma-Adressraum in der Hälfte ab und somit den gesamten Adressraum um 25 Prozent.</span><span class="sxs-lookup"><span data-stu-id="1cc01-240">It cuts the chroma address space in half, and thus the total address space by 25 percent.</span></span> <span data-ttu-id="1cc01-241">Bei 4:2:0-Formaten ist IMC2 das zweitbeliebteste Format nach NV12.</span><span class="sxs-lookup"><span data-stu-id="1cc01-241">Among 4:2:0 formats, IMC2 is the second-most preferred format, after NV12.</span></span> <span data-ttu-id="1cc01-242">Dieses Verfahren wird in der folgenden Abbildung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="1cc01-242">The following image illustrates this process.</span></span>

![Abbildung 7:](images/yuvformats07.gif)

### <a name="imc4"></a><span data-ttu-id="1cc01-245">IMC4</span><span class="sxs-lookup"><span data-stu-id="1cc01-245">IMC4</span></span>

<span data-ttu-id="1cc01-246">Dieses Format ist mit IMC2 identisch, mit der Ausnahme, dass die Zeilen U (CB) und V (CR) ausgetauscht werden, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="1cc01-246">This format is identical to IMC2, except the U (Cb) and V (Cr) lines are swapped, as shown in the following illustration.</span></span>

![Abbildung 8.](images/yuvformats06.gif)

### <a name="yv12"></a><span data-ttu-id="1cc01-249">YV12</span><span class="sxs-lookup"><span data-stu-id="1cc01-249">YV12</span></span>

<span data-ttu-id="1cc01-250">Alle Y-Beispiele werden als erstes im Arbeitsspeicher als Array nicht signierter **char** -Werte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1cc01-250">All of the Y samples appear first in memory as an array of unsigned **char** values.</span></span> <span data-ttu-id="1cc01-251">Auf dieses Array folgt sofort alle V-Beispiele (CR).</span><span class="sxs-lookup"><span data-stu-id="1cc01-251">This array is followed immediately by all of the V (Cr) samples.</span></span> <span data-ttu-id="1cc01-252">Der Schritt der V-Ebene liegt bei der Hälfte des Schrittes der Y-Ebene. und die Ebene "V" enthält die Hälfte der Zeilen in der Y-Ebene.</span><span class="sxs-lookup"><span data-stu-id="1cc01-252">The stride of the V plane is half the stride of the Y plane; and the V plane contains half as many lines as the Y plane.</span></span> <span data-ttu-id="1cc01-253">Auf die v-Ebene folgt sofort alle U (CB)-Beispiele mit dem gleichen Schritt und der Anzahl von Zeilen wie die Ebene "v", wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="1cc01-253">The V plane is followed immediately by all of the U (Cb) samples, with the same stride and number of lines as the V plane, as shown in the following illustration.</span></span>

![Abbildung 9.](images/yuvformats08.gif)

### <a name="nv12"></a><span data-ttu-id="1cc01-256">NV12</span><span class="sxs-lookup"><span data-stu-id="1cc01-256">NV12</span></span>

<span data-ttu-id="1cc01-257">Alle Y-Beispiele werden als erstes im Arbeitsspeicher als Array von **char** -Werten ohne Vorzeichen mit einer geraden Anzahl von Zeilen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1cc01-257">All of the Y samples appear first in memory as an array of unsigned **char** values with an even number of lines.</span></span> <span data-ttu-id="1cc01-258">Auf die Y-Ebene folgt unmittelbar ein Array nicht signierter **char** -Werte, das gepackte U (CB)-und V (CR)-Beispiele enthält.</span><span class="sxs-lookup"><span data-stu-id="1cc01-258">The Y plane is followed immediately by an array of unsigned **char** values that contains packed U (Cb) and V (Cr) samples.</span></span> <span data-ttu-id="1cc01-259">Wenn das kombinierte U-V-Array als Array von Little-enumdian- **Wort** Werten adressiert wird, enthalten die lssb die U-Werte, und die MSSB enthalten die V-Werte.</span><span class="sxs-lookup"><span data-stu-id="1cc01-259">When the combined U-V array is addressed as an array of little-endian **WORD** values, the LSBs contain the U values, and the MSBs contain the V values.</span></span> <span data-ttu-id="1cc01-260">NV12 ist das bevorzugte 4:2:0-Pixel-Format für DirectX VA.</span><span class="sxs-lookup"><span data-stu-id="1cc01-260">NV12 is the preferred 4:2:0 pixel format for DirectX VA.</span></span> <span data-ttu-id="1cc01-261">Es wird erwartet, dass es sich um eine langfristige Anforderung für DirectX VA Accelerators handelt, die 4:2:0-Video unterstützen.</span><span class="sxs-lookup"><span data-stu-id="1cc01-261">It is expected to be an intermediate-term requirement for DirectX VA accelerators supporting 4:2:0 video.</span></span> <span data-ttu-id="1cc01-262">In der folgenden Abbildung sind die Y-Ebene und das-Array dargestellt, das gepackte Sie und V-Beispiele enthält.</span><span class="sxs-lookup"><span data-stu-id="1cc01-262">The following illustration shows the Y plane and the array that contains packed U and V samples.</span></span>

![Abbildung 10.](images/yuvformats09.gif)

## <a name="color-space-and-chroma-sampling-rate-conversions"></a><span data-ttu-id="1cc01-265">Farb Raum-und Chroma-Sampling-Raten Konvertierungen</span><span class="sxs-lookup"><span data-stu-id="1cc01-265">Color Space and Chroma Sampling Rate Conversions</span></span>

<span data-ttu-id="1cc01-266">Dieser Abschnitt enthält Richtlinien für die Typumwandlung zwischen YUV und RGB sowie für die Umstellung zwischen einigen unterschiedlichen YUV-Formaten.</span><span class="sxs-lookup"><span data-stu-id="1cc01-266">This section provides guidelines for converting between YUV and RGB, and for converting between some different YUV formats.</span></span> <span data-ttu-id="1cc01-267">In diesem Abschnitt werden zwei RGB-Codierungs Schemas in Erwägung gezogen: *8-Bit-Computer RGB*, auch als sRGB oder "vollständig skalierbar" (RGB) und *Studio-Video RGB* oder "RGB mit headraum und Zehen Raum" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1cc01-267">We consider two RGB encoding schemes in this section: *8-bit computer RGB*, also known as sRGB or "full-scale" RGB, and *studio video RGB*, or "RGB with head-room and toe-room."</span></span> <span data-ttu-id="1cc01-268">Diese werden wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="1cc01-268">These are defined as follows:</span></span>

-   <span data-ttu-id="1cc01-269">Computer RGB verwendet 8 Bits für jedes rot, grün und blau.</span><span class="sxs-lookup"><span data-stu-id="1cc01-269">Computer RGB uses 8 bits for each sample of red, green, and blue.</span></span> <span data-ttu-id="1cc01-270">Schwarz wird durch r = g = b = 0 und weiß durch r = g = b = 255 dargestellt.</span><span class="sxs-lookup"><span data-stu-id="1cc01-270">Black is represented by R = G = B = 0, and white is represented by R = G = B = 255.</span></span>
-   <span data-ttu-id="1cc01-271">In der Studio-Grafik RGB wird eine beliebige Anzahl von Bits N für jede Stichprobe von rot, grün und Blau verwendet, wobei N 8 oder mehr ist.</span><span class="sxs-lookup"><span data-stu-id="1cc01-271">Studio video RGB uses some number of bits N for each sample of red, green, and blue, where N is 8 or more.</span></span> <span data-ttu-id="1cc01-272">Studio-Video RGB verwendet einen anderen Skalierungsfaktor als Computer RGB und einen Offset.</span><span class="sxs-lookup"><span data-stu-id="1cc01-272">Studio video RGB uses a different scaling factor than computer RGB, and it has an offset.</span></span> <span data-ttu-id="1cc01-273">Schwarz wird durch r = g = b = 16 \* 2 ^ (n-8) und weiß durch r = g = b = 235 \* 2 ^ (n-8) dargestellt.</span><span class="sxs-lookup"><span data-stu-id="1cc01-273">Black is represented by R = G = B = 16\*2^(N-8), and white is represented by R = G = B = 235\*2^(N-8).</span></span> <span data-ttu-id="1cc01-274">Tatsächliche Werte können jedoch außerhalb dieses Bereichs liegen.</span><span class="sxs-lookup"><span data-stu-id="1cc01-274">However, actual values may fall outside this range.</span></span>

<span data-ttu-id="1cc01-275">Studio-Video RGB ist die bevorzugte RGB-Definition für Videos in Windows, während Computer RGB die bevorzugte RGB-Definition für nicht-Video-Anwendungen ist.</span><span class="sxs-lookup"><span data-stu-id="1cc01-275">Studio video RGB is the preferred RGB definition for video in Windows, while computer RGB is the preferred RGB definition for non-video applications.</span></span> <span data-ttu-id="1cc01-276">In beiden Formen von RGB werden die Chromaticity-Koordinaten in "ITU-R BT. 709" für die Definition der RGB-Farb Primärwerte angegeben.</span><span class="sxs-lookup"><span data-stu-id="1cc01-276">In either form of RGB, the chromaticity coordinates are as specified in ITU-R BT.709 for the definition of the RGB color primaries.</span></span> <span data-ttu-id="1cc01-277">Die (x, y)-Koordinaten von R, G und B sind (0,64, 0,33), (0,30, 0,60) und (0,15, 0,06) bzw.</span><span class="sxs-lookup"><span data-stu-id="1cc01-277">The (x,y) coordinates of R, G, and B are (0.64, 0.33), (0.30, 0.60), and (0.15, 0.06), respectively.</span></span> <span data-ttu-id="1cc01-278">Der Verweis weiß ist D65 mit Koordinaten (0,3127, 0,3290).</span><span class="sxs-lookup"><span data-stu-id="1cc01-278">Reference white is D65 with coordinates (0.3127, 0.3290).</span></span> <span data-ttu-id="1cc01-279">Das nominale Gamma ist 1/0.45 (ca. 2,2), wobei präziser Gamma ausführlich in "ITU-R BT. 709" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="1cc01-279">Nominal gamma is 1/0.45 (approximately 2.2), with precise gamma defined in detail in ITU-R BT.709.</span></span>

<span data-ttu-id="1cc01-280">**Konvertierung zwischen RGB und 4:4:4 YUV**</span><span class="sxs-lookup"><span data-stu-id="1cc01-280">**Conversion between RGB and 4:4:4 YUV**</span></span>

<span data-ttu-id="1cc01-281">Zuerst wird die Konvertierung zwischen RGB und 4:4:4 YUV beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1cc01-281">We first describe conversion between RGB and 4:4:4 YUV.</span></span> <span data-ttu-id="1cc01-282">Zum Konvertieren von 4:2:0 oder 4:2:2 YUV in RGB empfiehlt es sich, die YUV-Daten in 4:4:4 YUV zu konvertieren und dann von 4:4:4 YUV in RGB zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="1cc01-282">To convert 4:2:0 or 4:2:2 YUV to RGB, we recommend converting the YUV data to 4:4:4 YUV, and then converting from 4:4:4 YUV to RGB.</span></span> <span data-ttu-id="1cc01-283">Das Format "ayuv", bei dem es sich um ein 4:4:4-Format handelt, verwendet jeweils 8 Bits für die Y-, U-und V-Beispiele.</span><span class="sxs-lookup"><span data-stu-id="1cc01-283">The AYUV format, which is a 4:4:4 format, uses 8 bits each for the Y, U, and V samples.</span></span> <span data-ttu-id="1cc01-284">YUV kann auch mit mehr als 8 Bits pro Stichprobe für einige Anwendungen definiert werden.</span><span class="sxs-lookup"><span data-stu-id="1cc01-284">YUV can also be defined using more than 8 bits per sample for some applications.</span></span>

<span data-ttu-id="1cc01-285">Zwei vorherrschende YUV-Konvertierungen von RGB wurden für digitales Video definiert.</span><span class="sxs-lookup"><span data-stu-id="1cc01-285">Two dominant YUV conversions from RGB have been defined for digital video.</span></span> <span data-ttu-id="1cc01-286">Beide basieren auf der Spezifikation, die als "ITU-R-Empfehlung BT. 709" bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="1cc01-286">Both are based on the specification known as ITU-R Recommendation BT.709.</span></span> <span data-ttu-id="1cc01-287">Die erste Konvertierung ist das ältere YUV-Formular, das für die Verwendung von 50-Hz in BT. 709 definiert ist.</span><span class="sxs-lookup"><span data-stu-id="1cc01-287">The first conversion is the older YUV form defined for 50-Hz use in BT.709.</span></span> <span data-ttu-id="1cc01-288">Sie ist identisch mit der in der ITU-R-Empfehlung "BT. 601" angegebenen Beziehung, die auch mit dem älteren Namen "CCIR 601" bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="1cc01-288">It is the same as the relation specified in ITU-R Recommendation BT.601, also known by its older name, CCIR 601.</span></span> <span data-ttu-id="1cc01-289">Er sollte als bevorzugtes YUV-Format für die Standard-Definition-TV-Auflösung (720 x 576) und ein Video mit niedrigerer Auflösung angesehen werden.</span><span class="sxs-lookup"><span data-stu-id="1cc01-289">It should be considered the preferred YUV format for standard-definition TV resolution (720 x 576) and lower-resolution video.</span></span> <span data-ttu-id="1cc01-290">Dies ist durch die Werte der beiden Konstanten *KR* und *KB* gekennzeichnet:</span><span class="sxs-lookup"><span data-stu-id="1cc01-290">It is characterized by the values of two constants *Kr* and *Kb*:</span></span>

``` syntax
Kr = 0.299
Kb = 0.114
```

<span data-ttu-id="1cc01-291">Die zweite Konvertierung ist das neuere YUV-Formular, das für die Verwendung von 60-Hz in BT. 709 definiert ist, und sollte als bevorzugtes Format für Videoauflösungen oberhalb von SDTV angesehen werden.</span><span class="sxs-lookup"><span data-stu-id="1cc01-291">The second conversion is the newer YUV form defined for 60-Hz use in BT.709, and should be considered the preferred format for video resolutions above SDTV.</span></span> <span data-ttu-id="1cc01-292">Sie ist durch unterschiedliche Werte für diese beiden Konstanten gekennzeichnet:</span><span class="sxs-lookup"><span data-stu-id="1cc01-292">It is characterized by different values for these two constants:</span></span>

``` syntax
Kr = 0.2126
Kb = 0.0722
```

<span data-ttu-id="1cc01-293">Die Konvertierung von RGB in YUV wird wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="1cc01-293">Conversion from RGB to YUV is defined by starting with the following:</span></span>

``` syntax
L = Kr * R + Kb * B + (1 - Kr - Kb) * G
```

<span data-ttu-id="1cc01-294">Die YUV-Werte werden dann wie folgt abgerufen:</span><span class="sxs-lookup"><span data-stu-id="1cc01-294">The YUV values are then obtained as follows:</span></span>

``` syntax
Y =                   floor(2^(M-8) * (219*(L-Z)/S + 16) + 0.5)
U = clip3(0, (2^M)-1, floor(2^(M-8) * (112*(B-L) / ((1-Kb)*S) + 128) + 0.5))
V = clip3(0, (2^M)-1, floor(2^(M-8) * (112*(R-L) / ((1-Kr)*S) + 128) + 0.5))
```

<span data-ttu-id="1cc01-295">where</span><span class="sxs-lookup"><span data-stu-id="1cc01-295">where</span></span>

-   <span data-ttu-id="1cc01-296">M ist die Anzahl von Bits pro YUV-Beispiel (m >= 8).</span><span class="sxs-lookup"><span data-stu-id="1cc01-296">M is the number of bits per YUV sample (M >= 8).</span></span>
-   <span data-ttu-id="1cc01-297">Z ist die Variable auf schwarzer Ebene.</span><span class="sxs-lookup"><span data-stu-id="1cc01-297">Z is the black-level variable.</span></span> <span data-ttu-id="1cc01-298">Für Computer RGB ist Z auf 0 (null).</span><span class="sxs-lookup"><span data-stu-id="1cc01-298">For computer RGB, Z equals 0.</span></span> <span data-ttu-id="1cc01-299">Für Studio-Video RGB entspricht Z dem Wert 16 \* 2 ^ (n-8), wobei N für die Anzahl der Bits pro RGB-Stichprobe (n >= 8) steht.</span><span class="sxs-lookup"><span data-stu-id="1cc01-299">For studio video RGB, Z equals 16\*2^(N-8), where N is the number of bits per RGB sample (N >= 8).</span></span>
-   <span data-ttu-id="1cc01-300">S ist die Skalierungs Variable.</span><span class="sxs-lookup"><span data-stu-id="1cc01-300">S is the scaling variable.</span></span> <span data-ttu-id="1cc01-301">Für Computer RGB ist "S" 255.</span><span class="sxs-lookup"><span data-stu-id="1cc01-301">For computer RGB, S equals 255.</span></span> <span data-ttu-id="1cc01-302">Für Studio-Video RGB ist S auf 219 \* 2 ^ (N-8).</span><span class="sxs-lookup"><span data-stu-id="1cc01-302">For studio video RGB, S equals 219\*2^(N-8).</span></span>

<span data-ttu-id="1cc01-303">Die Funktionsfläche (x) gibt die größte ganze Zahl zurück, die kleiner oder gleich x ist.</span><span class="sxs-lookup"><span data-stu-id="1cc01-303">The function floor(x) returns the largest integer less than or equal to x.</span></span> <span data-ttu-id="1cc01-304">Die Clip3-Funktion (x, y, z) ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="1cc01-304">The function clip3(x, y, z) is defined as follows:</span></span>

``` syntax
clip3(x, y, z) = ((z < x) ? x : ((z > y) ? y : z))
```

> [!Note]  
> <span data-ttu-id="1cc01-305">Clip3 sollte nicht als Präprozessormakro, sondern als Funktion implementiert werden. Andernfalls werden mehrere Auswertungen der Argumente durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="1cc01-305">clip3 should be implemented as a function rather than a preprocessor macro; otherwise multiple evaluations of the arguments will occur.</span></span>

 

<span data-ttu-id="1cc01-306">Das Y-Beispiel stellt die Helligkeit dar, und die Beispiele für Sie und V stellen die Farbabweichungen in Richtung blau bzw. rot dar.</span><span class="sxs-lookup"><span data-stu-id="1cc01-306">The Y sample represents brightness, and the U and V samples represent the color deviations toward blue and red, respectively.</span></span> <span data-ttu-id="1cc01-307">Der nominale Bereich für Y ist 16 \* 2 ^ (m-8) bis 235 \* 2 ^ (m-8).</span><span class="sxs-lookup"><span data-stu-id="1cc01-307">The nominal range for Y is 16\*2^(M-8) to 235\*2^(M-8).</span></span> <span data-ttu-id="1cc01-308">Schwarz wird als 16 \* 2 ^ (m-8) und weiß als 235 \* 2 ^ (m-8) dargestellt.</span><span class="sxs-lookup"><span data-stu-id="1cc01-308">Black is represented as 16\*2^(M-8), and white is represented as 235\*2^(M-8).</span></span> <span data-ttu-id="1cc01-309">Der nominale Bereich für Sie und V beträgt 16 \* 2 ^ (m-8) bis 240 \* 2 ^ (m-8) mit dem Wert 128 \* 2 ^ (m-8), der neutrales Chroma darstellt.</span><span class="sxs-lookup"><span data-stu-id="1cc01-309">The nominal range for U and V are 16\*2^(M-8) to 240\*2^(M-8), with the value 128\*2^(M-8) representing neutral chroma.</span></span> <span data-ttu-id="1cc01-310">Tatsächliche Werte können jedoch außerhalb dieser Bereiche liegen.</span><span class="sxs-lookup"><span data-stu-id="1cc01-310">However, actual values may fall outside these ranges.</span></span>

<span data-ttu-id="1cc01-311">Für Eingabedaten in Form von Studio-Video RGB ist der Clip-Vorgang erforderlich, um die Werte für "You" und "V" im Bereich von 0 bis (2 ^ M)-1 beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="1cc01-311">For input data in the form of studio video RGB, the clip operation is necessary to keep the U and V values within the range 0 to (2^M)-1.</span></span> <span data-ttu-id="1cc01-312">Wenn es sich bei der Eingabe um Computer RGB handelt, ist der Clip Vorgang nicht erforderlich, da die Konvertierungs Formel keine Werte außerhalb dieses Bereichs verursachen kann.</span><span class="sxs-lookup"><span data-stu-id="1cc01-312">If the input is computer RGB, the clip operation is not required, because the conversion formula cannot produce values outside of this range.</span></span>

<span data-ttu-id="1cc01-313">Dabei handelt es sich um die genauen Formeln ohne Näherungs.</span><span class="sxs-lookup"><span data-stu-id="1cc01-313">These are the exact formulas without approximation.</span></span> <span data-ttu-id="1cc01-314">Alles, was in diesem Dokument folgt, wird von diesen Formeln abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="1cc01-314">Everything that follows in this document is derived from these formulas.</span></span> <span data-ttu-id="1cc01-315">In diesem Abschnitt werden die folgenden Konvertierungen beschrieben:</span><span class="sxs-lookup"><span data-stu-id="1cc01-315">This section describes the following conversions:</span></span>

-   [<span data-ttu-id="1cc01-316">Wandeln von RGB888 in YUV 4:4:4</span><span class="sxs-lookup"><span data-stu-id="1cc01-316">Converting RGB888 to YUV 4:4:4</span></span>](#converting-rgb888-to-yuv-444)
-   [<span data-ttu-id="1cc01-317">Umstellen von 8-Bit-YUV in RGB888</span><span class="sxs-lookup"><span data-stu-id="1cc01-317">Converting 8-bit YUV to RGB888</span></span>](#converting-8-bit-yuv-to-rgb888)
-   [<span data-ttu-id="1cc01-318">4:2:0 YUV wird in 4:2:2 YUV umgerechnet</span><span class="sxs-lookup"><span data-stu-id="1cc01-318">Converting 4:2:0 YUV to 4:2:2 YUV</span></span>](#converting-420-yuv-to-422-yuv)
-   [<span data-ttu-id="1cc01-319">4:2:2 YUV wird in 4:4:4 YUV umgerechnet</span><span class="sxs-lookup"><span data-stu-id="1cc01-319">Converting 4:2:2 YUV to 4:4:4 YUV</span></span>](#converting-422-yuv-to-444-yuv)
-   [<span data-ttu-id="1cc01-320">4:2:0 YUV wird in 4:4:4 YUV umgerechnet</span><span class="sxs-lookup"><span data-stu-id="1cc01-320">Converting 4:2:0 YUV to 4:4:4 YUV</span></span>](#converting-420-yuv-to-444-yuv)

## <a name="converting-rgb888-to-yuv-444"></a><span data-ttu-id="1cc01-321">Wandeln von RGB888 in YUV 4:4:4</span><span class="sxs-lookup"><span data-stu-id="1cc01-321">Converting RGB888 to YUV 4:4:4</span></span>

<span data-ttu-id="1cc01-322">Im Fall von "Computer RGB Input" und der 8-Bit-Ausgabe "BT. 601 YUV" sind wir der Meinung, dass die im vorherigen Abschnitt angegebenen Formeln in gewisser Weise den folgenden Werten zugewiesen werden können:</span><span class="sxs-lookup"><span data-stu-id="1cc01-322">In the case of computer RGB input and 8-bit BT.601 YUV output, we believe that the formulas given in the previous section can be reasonably approximated by the following:</span></span>

``` syntax
Y = ( (  66 * R + 129 * G +  25 * B + 128) >> 8) +  16
U = ( ( -38 * R -  74 * G + 112 * B + 128) >> 8) + 128
V = ( ( 112 * R -  94 * G -  18 * B + 128) >> 8) + 128
```

<span data-ttu-id="1cc01-323">Diese Formeln liefern 8-Bit-Ergebnisse mithilfe von Koeffizienten, die nicht mehr als 8 Bits der (unsignierten) Genauigkeit erfordern.</span><span class="sxs-lookup"><span data-stu-id="1cc01-323">These formulas produce 8-bit results using coefficients that require no more than 8 bits of (unsigned) precision.</span></span> <span data-ttu-id="1cc01-324">Zwischenergebnisse erfordern bis zu 16 Bits an Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="1cc01-324">Intermediate results will require up to 16 bits of precision.</span></span>

## <a name="converting-8-bit-yuv-to-rgb888"></a><span data-ttu-id="1cc01-325">Umstellen von 8-Bit-YUV in RGB888</span><span class="sxs-lookup"><span data-stu-id="1cc01-325">Converting 8-bit YUV to RGB888</span></span>

<span data-ttu-id="1cc01-326">Aus den ursprünglichen RGB-zu-YUV-Formeln kann eine der folgenden Beziehungen für BT. 601 abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="1cc01-326">From the original RGB-to-YUV formulas, one can derive the following relationships for BT.601.</span></span>

``` syntax
Y = round( 0.256788 * R + 0.504129 * G + 0.097906 * B) +  16 
U = round(-0.148223 * R - 0.290993 * G + 0.439216 * B) + 128
V = round( 0.439216 * R - 0.367788 * G - 0.071427 * B) + 128
```

<span data-ttu-id="1cc01-327">Daher gilt Folgendes:</span><span class="sxs-lookup"><span data-stu-id="1cc01-327">Therefore, given:</span></span>

``` syntax
C = Y - 16
D = U - 128
E = V - 128
```

<span data-ttu-id="1cc01-328">die Formeln zum Konvertieren von YUV in RGB können wie folgt abgeleitet werden:</span><span class="sxs-lookup"><span data-stu-id="1cc01-328">the formulas to convert YUV to RGB can be derived as follows:</span></span>

``` syntax
R = clip( round( 1.164383 * C                   + 1.596027 * E  ) )
G = clip( round( 1.164383 * C - (0.391762 * D) - (0.812968 * E) ) )
B = clip( round( 1.164383 * C +  2.017232 * D                   ) )
```

<span data-ttu-id="1cc01-329">wobei das `clip()` Clipping auf einen Bereich von \[ 0.. 255 bezeichnet \] .</span><span class="sxs-lookup"><span data-stu-id="1cc01-329">where `clip()` denotes clipping to a range of \[0..255\].</span></span> <span data-ttu-id="1cc01-330">Wir sind der Meinung, dass diese Formeln in gewisser Weise den folgenden folgen:</span><span class="sxs-lookup"><span data-stu-id="1cc01-330">We believe these formulas can be reasonably approximated by the following:</span></span>

``` syntax
R = clip(( 298 * C           + 409 * E + 128) >> 8)
G = clip(( 298 * C - 100 * D - 208 * E + 128) >> 8)
B = clip(( 298 * C + 516 * D           + 128) >> 8)
```

<span data-ttu-id="1cc01-331">Diese Formeln verwenden einige Koeffizienten, bei denen mehr als 8 Bits Genauigkeit erforderlich sind, um jedes 8-Bit-Ergebnis zu erzielen, und Zwischenergebnisse erfordern mehr als 16 Bits an Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="1cc01-331">These formulas use some coefficients that require more than 8 bits of precision to produce each 8-bit result, and intermediate results will require more than 16 bits of precision.</span></span>

<span data-ttu-id="1cc01-332">Zum Konvertieren von 4:2:0 oder 4:2:2 YUV in RGB empfiehlt es sich, die YUV-Daten in 4:4:4 YUV zu konvertieren und dann von 4:4:4 YUV in RGB zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="1cc01-332">To convert 4:2:0 or 4:2:2 YUV to RGB, we recommend converting the YUV data to 4:4:4 YUV, and then converting from 4:4:4 YUV to RGB.</span></span> <span data-ttu-id="1cc01-333">Die folgenden Abschnitte enthalten einige Methoden zum Umrechnen von 4:2:0-und 4:2:2-Formaten in 4:4:4.</span><span class="sxs-lookup"><span data-stu-id="1cc01-333">The sections that follow present some methods for converting 4:2:0 and 4:2:2 formats to 4:4:4.</span></span>

## <a name="converting-420-yuv-to-422-yuv"></a><span data-ttu-id="1cc01-334">4:2:0 YUV wird in 4:2:2 YUV umgerechnet</span><span class="sxs-lookup"><span data-stu-id="1cc01-334">Converting 4:2:0 YUV to 4:2:2 YUV</span></span>

<span data-ttu-id="1cc01-335">Die Konvertierung von 4:2:0 YUV in 4:2:2 YUV erfordert eine vertikale upkonvertierung mit einem Faktor von zwei.</span><span class="sxs-lookup"><span data-stu-id="1cc01-335">Converting 4:2:0 YUV to 4:2:2 YUV requires vertical upconversion by a factor of two.</span></span> <span data-ttu-id="1cc01-336">In diesem Abschnitt wird eine Beispiel Methode zum Ausführen der Upconversion beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1cc01-336">This section describes an example method for performing the upconversion.</span></span> <span data-ttu-id="1cc01-337">Bei der-Methode wird davon ausgegangen, dass die Videobilder Progressive Scan werden.</span><span class="sxs-lookup"><span data-stu-id="1cc01-337">The method assumes that the video pictures are progressive scan.</span></span>

> [!Note]  
> <span data-ttu-id="1cc01-338">Der Konvertierungs Vorgang "4:2:0 bis 4:2:2 Interlacing Scan" stellt atypische Probleme dar und ist schwierig zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="1cc01-338">The 4:2:0 to 4:2:2 interlaced scan conversion process presents atypical problems and is difficult to implement.</span></span> <span data-ttu-id="1cc01-339">In diesem Artikel wird das Problem der Umstellung der Zeilen Sprung Überprüfung von 4:2:0 in 4:2:2 nicht behandelt.</span><span class="sxs-lookup"><span data-stu-id="1cc01-339">This article does not address the issue of converting interlaced scan from 4:2:0 to 4:2:2.</span></span>

 

<span data-ttu-id="1cc01-340">Jede vertikale Zeile von Eingabe-Chroma-Beispielen ist ein Array `Cin[]` , das zwischen 0 und N-1 liegt.</span><span class="sxs-lookup"><span data-stu-id="1cc01-340">Let each vertical line of input chroma samples be an array `Cin[]` that ranges from 0 to N - 1.</span></span> <span data-ttu-id="1cc01-341">Die entsprechende vertikale Linie des Ausgabe Bilds ist ein Array `Cout[]` , das zwischen 0 und 2n-1 liegt.</span><span class="sxs-lookup"><span data-stu-id="1cc01-341">The corresponding vertical line on the output image will be an array `Cout[]` that ranges from 0 to 2N - 1.</span></span> <span data-ttu-id="1cc01-342">Um jede vertikale Linie zu konvertieren, führen Sie den folgenden Prozess aus:</span><span class="sxs-lookup"><span data-stu-id="1cc01-342">To convert each vertical line, perform the following process:</span></span>

``` syntax
Cout[0]     = Cin[0];
Cout[1]     = clip((9 * (Cin[0] + Cin[1]) - (Cin[0] + Cin[2]) + 8) >> 4);
Cout[2]     = Cin[1];
Cout[3]     = clip((9 * (Cin[1] + Cin[2]) - (Cin[0] + Cin[3]) + 8) >> 4);
Cout[4]     = Cin[2]
Cout[5]     = clip((9 * (Cin[2] + Cin[3]) - (Cin[1] + Cin[4]) + 8) >> 4);
...
Cout[2*i]   = Cin[i]
Cout[2*i+1] = clip((9 * (Cin[i] + Cin[i+1]) - (Cin[i-1] + Cin[i+2]) + 8) >> 4);
...
Cout[2*N-3] = clip((9 * (Cin[N-2] + Cin[N-1]) - (Cin[N-3] + Cin[N-1]) + 8) >> 4);
Cout[2*N-2] = Cin[N-1];
Cout[2*N-1] = clip((9 * (Cin[N-1] + Cin[N-1]) - (Cin[N-2] + Cin[N-1]) + 8) >> 4);
```

<span data-ttu-id="1cc01-343">Where Clip () bezeichnet Clipping auf einen Bereich von \[ 0.. 255 \] .</span><span class="sxs-lookup"><span data-stu-id="1cc01-343">where clip() denotes clipping to a range of \[0..255\].</span></span>

> [!Note]  
> <span data-ttu-id="1cc01-344">Die Gleichungen zum Behandeln der Kanten können mathematisch vereinfacht werden.</span><span class="sxs-lookup"><span data-stu-id="1cc01-344">The equations for handling the edges can be mathematically simplified.</span></span> <span data-ttu-id="1cc01-345">Sie werden in dieser Form angezeigt, um den Spann Effekt an den Rändern des Bilds zu veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="1cc01-345">They are shown in this form to illustrate the clamping effect at the edges of the picture.</span></span>

 

<span data-ttu-id="1cc01-346">Tatsächlich berechnet diese Methode jeden fehlenden Wert durch Interpolation der Kurve über die vier angrenzenden Pixel, die auf die Werte der beiden nächsten Pixel gewichtet werden (Abbildung 11).</span><span class="sxs-lookup"><span data-stu-id="1cc01-346">In effect, this method calculates each missing value by interpolating the curve over the four adjacent pixels, weighted toward the values of the two nearest pixels (Figure 11).</span></span> <span data-ttu-id="1cc01-347">Die in diesem Beispiel verwendete spezielle Interpolationsmethode generiert fehlende Stichproben an der Hälfte der ganzzahligen Positionen mithilfe einer bekannten Methode namens Catmull-Rom Interpolationsmethode, die auch als kubische intervolution-Interpolationsmethode bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="1cc01-347">The specific interpolation method used in this example generates missing samples at half-integer positions using a well-known method called Catmull-Rom interpolation, also known as cubic convolution interpolation.</span></span>

![Abbildung 11.](images/yuvformats14.gif)

<span data-ttu-id="1cc01-350">In Signal Verarbeitungs Begriffen sollte die vertikale upkonvertierung idealerweise eine Phasen Verschiebungs Kompensation enthalten, um den vertikalen halb Pixel Offset (relativ zum samplingraster der Ausgabe 4:2:2) zwischen den Speicherorten der 4:2:0-Beispiel Zeilen und dem Speicherort jeder anderen 4:2:2-Beispiel Zeile zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="1cc01-350">In signal processing terms, the vertical upconversion should ideally include a phase shift compensation to account for the half-pixel vertical offset (relative to the output 4:2:2 sampling grid) between the locations of the 4:2:0 sample lines and the location of every other 4:2:2 sample line.</span></span> <span data-ttu-id="1cc01-351">Durch die Einführung dieses Offsets wird jedoch der Verarbeitungsaufwand für das Generieren der Beispiele erhöht, und es ist nicht möglich, die ursprünglichen 4:2:0-Beispiele aus dem Upsampling-Image 4:2:2 zu rekonstruieren.</span><span class="sxs-lookup"><span data-stu-id="1cc01-351">However, introducing this offset would increase the amount of processing required to generate the samples, and make it impossible to reconstruct the original 4:2:0 samples from the upsampled 4:2:2 image.</span></span> <span data-ttu-id="1cc01-352">Außerdem wäre es nicht möglich, Videos direkt in 4:2:2-Oberflächen zu decodieren und diese Oberflächen dann als Referenzbilder für das Decodieren der nachfolgenden Bilder im Stream zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1cc01-352">It would also make it impossible to decode video directly into 4:2:2 surfaces and then use those surfaces as reference pictures for decoding subsequent pictures in the stream.</span></span> <span data-ttu-id="1cc01-353">Daher berücksichtigt die hier angegebene Methode nicht die präzise vertikale Ausrichtung der Beispiele.</span><span class="sxs-lookup"><span data-stu-id="1cc01-353">Therefore, the method provided here does not take into account the precise vertical alignment of the samples.</span></span> <span data-ttu-id="1cc01-354">Dies ist wahrscheinlich nicht visuell schädlich bei einer relativ großen Bildauflösung.</span><span class="sxs-lookup"><span data-stu-id="1cc01-354">Doing so is probably not visually harmful at reasonably high picture resolutions.</span></span>

<span data-ttu-id="1cc01-355">Wenn Sie mit einem 4:2:0-Video beginnen, das das im h. 261-, h. 263-oder MPEG-1-Video definierte Stichproben Raster verwendet, wird auch die Phase der Ausgabe 4:2:2 Chroma-Beispiele in Relation zum Abstand in der Luma-Samplings-Stichproben 4:2:2 Entnahme um einen horizontalen Halbpixel-Offset verschoben.</span><span class="sxs-lookup"><span data-stu-id="1cc01-355">If you start with 4:2:0 video that uses the sampling grid defined in H.261, H.263, or MPEG-1 video, the phase of the output 4:2:2 chroma samples will also be shifted by a half-pixel horizontal offset relative to the spacing on the luma sampling grid (a quarter-pixel offset relative to the spacing of the 4:2:2 chroma sampling grid).</span></span> <span data-ttu-id="1cc01-356">Die MPEG-2-Form von 4:2:0-Video wird jedoch wahrscheinlich häufiger auf PCs verwendet und wird von diesem Problem nicht beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="1cc01-356">However, the MPEG-2 form of 4:2:0 video is probably more commonly used on PCs and does not suffer from this problem.</span></span> <span data-ttu-id="1cc01-357">Außerdem ist die Unterscheidung wahrscheinlich nicht visuell schädlich, wenn es um eine relativ hohe Bildauflösung geht.</span><span class="sxs-lookup"><span data-stu-id="1cc01-357">Moreover, the distinction is probably not visually harmful at reasonably high picture resolutions.</span></span> <span data-ttu-id="1cc01-358">Der Versuch, dieses Problem zu beheben, würde die gleiche Art von Problemen erzeugen, die für den vertikalen Phasen Offset erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="1cc01-358">Trying to correct for this problem would create the same sort of problems discussed for the vertical phase offset.</span></span>

## <a name="converting-422-yuv-to-444-yuv"></a><span data-ttu-id="1cc01-359">4:2:2 YUV wird in 4:4:4 YUV umgerechnet</span><span class="sxs-lookup"><span data-stu-id="1cc01-359">Converting 4:2:2 YUV to 4:4:4 YUV</span></span>

<span data-ttu-id="1cc01-360">Die Konvertierung von 4:2:2 YUV in 4:4:4 YUV erfordert eine horizontale upkonvertierung mit einem Faktor von zwei.</span><span class="sxs-lookup"><span data-stu-id="1cc01-360">Converting 4:2:2 YUV to 4:4:4 YUV requires horizontal upconversion by a factor of two.</span></span> <span data-ttu-id="1cc01-361">Die zuvor beschriebene Methode für die vertikale upkonvertierung kann auch auf die horizontale upkonvertierung angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="1cc01-361">The method described previously for vertical upconversion can also be applied to horizontal upconversion.</span></span> <span data-ttu-id="1cc01-362">Für MPEG-2-und ITU-R BT. 601-Video erstellt diese Methode Beispiele mit der korrekten Phasen Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="1cc01-362">For MPEG-2 and ITU-R BT.601 video, this method will produce samples with the correct phase alignment.</span></span>

## <a name="converting-420-yuv-to-444-yuv"></a><span data-ttu-id="1cc01-363">4:2:0 YUV wird in 4:4:4 YUV umgerechnet</span><span class="sxs-lookup"><span data-stu-id="1cc01-363">Converting 4:2:0 YUV to 4:4:4 YUV</span></span>

<span data-ttu-id="1cc01-364">Wenn Sie 4:2:0 YUV in 4:4:4 YUV konvertieren möchten, können Sie einfach den oben beschriebenen Methoden folgen.</span><span class="sxs-lookup"><span data-stu-id="1cc01-364">To convert 4:2:0 YUV to 4:4:4 YUV, you can simply follow the two methods described previously.</span></span> <span data-ttu-id="1cc01-365">Konvertieren Sie das 4:2:0-Abbild in 4:2:2, und konvertieren Sie dann das 4:2:2-Image in 4:4:4.</span><span class="sxs-lookup"><span data-stu-id="1cc01-365">Convert the 4:2:0 image to 4:2:2, and then convert the 4:2:2 image to 4:4:4.</span></span> <span data-ttu-id="1cc01-366">Sie können auch die Reihenfolge der beiden upkonvertierungsprozesse ändern, da die Reihenfolge der Vorgänge für die visuelle Qualität des Ergebnisses nicht wirklich von Bedeutung ist.</span><span class="sxs-lookup"><span data-stu-id="1cc01-366">You can also switch the order of the two upconversion processes, as the order of operation does not really matter to the visual quality of the result.</span></span>

## <a name="other-yuv-formats"></a><span data-ttu-id="1cc01-367">Andere YUV-Formate</span><span class="sxs-lookup"><span data-stu-id="1cc01-367">Other YUV Formats</span></span>

<span data-ttu-id="1cc01-368">Einige andere, weniger gängige YUV-Formate umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="1cc01-368">Some other, less common YUV formats include the following:</span></span>

-   <span data-ttu-id="1cc01-369">AI44 ist ein im plettisierten YUV-Format mit 8 Bits pro Stichprobe.</span><span class="sxs-lookup"><span data-stu-id="1cc01-369">AI44 is a palettized YUV format with 8 bits per sample.</span></span> <span data-ttu-id="1cc01-370">Jedes Beispiel enthält einen Index in den 4 signifikantesten Bits (MSSB) und einen Alpha-Wert in den 4 geringsten Bits (lssb).</span><span class="sxs-lookup"><span data-stu-id="1cc01-370">Each sample contains an index in the 4 most significant bits (MSBs) and an alpha value in the 4 least significant bits (LSBs).</span></span> <span data-ttu-id="1cc01-371">Der Index verweist auf ein Array von YUV-paletteneinträgen, die im Medientyp für das Format definiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="1cc01-371">The index refers to an array of YUV palette entries, which must be defined in the media type for the format.</span></span> <span data-ttu-id="1cc01-372">Dieses Format wird hauptsächlich für Bild Bilder verwendet.</span><span class="sxs-lookup"><span data-stu-id="1cc01-372">This format is primarily used for subpicture images.</span></span>
-   <span data-ttu-id="1cc01-373">NV11 ist ein 4:1:1-planare-Format mit 12 Bits pro Pixel.</span><span class="sxs-lookup"><span data-stu-id="1cc01-373">NV11 is a 4:1:1 planar format with 12 bits per pixel.</span></span> <span data-ttu-id="1cc01-374">Die Y-Beispiele werden zuerst im Arbeitsspeicher angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1cc01-374">The Y samples appear first in memory.</span></span> <span data-ttu-id="1cc01-375">Auf die Y-Ebene folgt ein Array von gepackten U (CB)-und V-Beispielen (CR).</span><span class="sxs-lookup"><span data-stu-id="1cc01-375">The Y plane is followed by an array of packed U (Cb) and V (Cr) samples.</span></span> <span data-ttu-id="1cc01-376">Wenn das kombinierte u-V-Array als Array von Little-enumdian- **Wort** Werten adressiert wird, sind die U-Beispiele in den lssb der einzelnen **Word** enthalten, und die V-Beispiele sind in den MSSB enthalten.</span><span class="sxs-lookup"><span data-stu-id="1cc01-376">When the combined U-V array is addressed as an array of little-endian **WORD** values, the U samples are contained in the LSBs of each **WORD**, and the V samples are contained in the MSBs.</span></span> <span data-ttu-id="1cc01-377">(Dieses Speicher Layout ähnelt NV12, obwohl die Chroma-Stichprobe anders ist.)</span><span class="sxs-lookup"><span data-stu-id="1cc01-377">(This memory layout is similar to NV12 although the chroma sampling is different.)</span></span>
-   <span data-ttu-id="1cc01-378">Im y41p ist ein 4:1:1-gepacktes Format, bei dem Sie und V jedes vierte Pixel horizontal abgepackt haben.</span><span class="sxs-lookup"><span data-stu-id="1cc01-378">Y41P is a 4:1:1 packed format, with U and V sampled every fourth pixel horizontally.</span></span> <span data-ttu-id="1cc01-379">Jedes Makro Pixel enthält 8 Pixel in drei Bytes mit dem folgenden bytelayout: `U0 Y0 V0 Y1    U4 Y2 V4 Y3    Y4 Y5 Y6 Y7`</span><span class="sxs-lookup"><span data-stu-id="1cc01-379">Each macropixel contains 8 pixels in three bytes, with the following byte layout: `U0 Y0 V0 Y1    U4 Y2 V4 Y3    Y4 Y5 Y6 Y7`</span></span>
-   <span data-ttu-id="1cc01-380">Y41T ist mit im y41p identisch, mit dem Unterschied, dass das unwichtigste Bit jedes Y-Beispiels den Chroma-Schlüssel angibt (0 = transparent, 1 = nicht transparent).</span><span class="sxs-lookup"><span data-stu-id="1cc01-380">Y41T is identical to Y41P, except the least-significant bit of each Y sample specifies the chroma key (0 = transparent, 1 = opaque).</span></span>
-   <span data-ttu-id="1cc01-381">Y42T ist mit UYVY identisch, mit dem Unterschied, dass das unwichtigste Bit jedes Y-Beispiels den Chroma-Schlüssel angibt (0 = transparent, 1 = nicht transparent).</span><span class="sxs-lookup"><span data-stu-id="1cc01-381">Y42T is identical to UYVY, except the least-significant bit of each Y sample specifies the chroma key (0 = transparent, 1 = opaque).</span></span>
-   <span data-ttu-id="1cc01-382">Yvyu entspricht yuyv, mit dem Unterschied, dass die Beispiele für Sie und V ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="1cc01-382">YVYU is equivalent to YUYV except the U and V samples are swapped.</span></span>

## <a name="identifying-yuv-formats-in-media-foundation"></a><span data-ttu-id="1cc01-383">Erkennen von YUV-Formaten in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1cc01-383">Identifying YUV Formats in Media Foundation</span></span>

<span data-ttu-id="1cc01-384">Jedes in diesem Artikel beschriebene YUV-Format verfügt über einen zugewiesenen FourCC-Code.</span><span class="sxs-lookup"><span data-stu-id="1cc01-384">Each of the YUV formats described in this article has an assigned FOURCC code.</span></span> <span data-ttu-id="1cc01-385">Bei einem FourCC-Code handelt es sich um eine 32-Bit-Ganzzahl ohne Vorzeichen, die durch Verkettung von vier ASCII-Zeichen erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1cc01-385">A FOURCC code is a 32-bit unsigned integer that is created by concatenating four ASCII characters.</span></span>

<span data-ttu-id="1cc01-386">Es gibt verschiedene C/C++-Makros, die das Deklarieren von FourCC-Werten im Quellcode vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="1cc01-386">There are various C/C++ macros that make it easier to declare FOURCC values in source code.</span></span> <span data-ttu-id="1cc01-387">Beispielsweise wird das **makefourcc** -Makro in MMSYSTEM. h deklariert, und das **FCC** -Makro wird in aviriff. h deklariert.</span><span class="sxs-lookup"><span data-stu-id="1cc01-387">For example, the **MAKEFOURCC** macro is declared in Mmsystem.h, and the **FCC** macro is declared in Aviriff.h.</span></span> <span data-ttu-id="1cc01-388">Verwenden Sie diese wie folgt:</span><span class="sxs-lookup"><span data-stu-id="1cc01-388">Use them as follows:</span></span>

``` syntax
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
```

<span data-ttu-id="1cc01-389">Sie können einen FourCC-Code auch direkt als Zeichenfolgenliterale deklarieren, indem Sie einfach die Reihenfolge der Zeichen umkehren.</span><span class="sxs-lookup"><span data-stu-id="1cc01-389">You can also declare a FOURCC code directly as a string literal simply by reversing the order of the characters.</span></span> <span data-ttu-id="1cc01-390">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="1cc01-390">For example:</span></span>

``` syntax
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'
```

<span data-ttu-id="1cc01-391">Das Umkehren der Reihenfolge ist erforderlich, da das Windows-Betriebssystem eine Little-Endian-Architektur verwendet.</span><span class="sxs-lookup"><span data-stu-id="1cc01-391">Reversing the order is necessary because the Windows operating system uses a little-endian architecture.</span></span> <span data-ttu-id="1cc01-392">' Y ' = 0x59, ' U ' = 0x55 und ' 2 ' = 0x32, daher ist ' 2yuy ' 0x32595559.</span><span class="sxs-lookup"><span data-stu-id="1cc01-392">'Y' = 0x59, 'U' = 0x55, and '2' = 0x32, so '2YUY' is 0x32595559.</span></span>

<span data-ttu-id="1cc01-393">In Media Foundation werden Formate durch eine GUID des Haupt Typs und eine Untertyp-GUID identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1cc01-393">In Media Foundation, formats are identified by a major type GUID and a subtype GUID.</span></span> <span data-ttu-id="1cc01-394">Der Haupttyp für Computer Videoformate ist immer MF MediaType \_ Video.</span><span class="sxs-lookup"><span data-stu-id="1cc01-394">The major type for computer video formats is always MFMediaType\_Video .</span></span> <span data-ttu-id="1cc01-395">Der Untertyp kann erstellt werden, indem Sie den FourCC-Code einer GUID wie folgt zuordnet:</span><span class="sxs-lookup"><span data-stu-id="1cc01-395">The subtype can be constructed by mapping the FOURCC code to a GUID, as follows:</span></span>

``` syntax
XXXXXXXX-0000-0010-8000-00AA00389B71 
```

<span data-ttu-id="1cc01-396">dabei `XXXXXXXX` ist der FourCC-Code.</span><span class="sxs-lookup"><span data-stu-id="1cc01-396">where `XXXXXXXX` is the FOURCC code.</span></span> <span data-ttu-id="1cc01-397">Folglich lautet die Untertyp-GUID für im YUY2 wie folgt:</span><span class="sxs-lookup"><span data-stu-id="1cc01-397">Thus, the subtype GUID for YUY2 is:</span></span>

``` syntax
32595559-0000-0010-8000-00AA00389B71 
```

<span data-ttu-id="1cc01-398">Konstanten für die gängigsten GUIDs des YUV-Formats werden in der Header Datei "mfapi. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="1cc01-398">Constants for the most common YUV format GUIDs are defined in the header file mfapi.h.</span></span> <span data-ttu-id="1cc01-399">Eine Liste dieser Konstanten finden Sie [unter Video Untertyp-GUIDs](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="1cc01-399">For a list of these constants, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1cc01-400">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1cc01-400">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1cc01-401">Informationen zu YUV-Videos</span><span class="sxs-lookup"><span data-stu-id="1cc01-401">About YUV Video</span></span>](about-yuv-video.md)
</dt> <dt>

[<span data-ttu-id="1cc01-402">Video Medientypen</span><span class="sxs-lookup"><span data-stu-id="1cc01-402">Video Media Types</span></span>](video-media-types.md)
</dt> </dl>

 

 



