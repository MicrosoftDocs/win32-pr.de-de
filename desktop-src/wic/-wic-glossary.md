---
description: Definiert Begriffe, die in WIC verwendet werden.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: b066757a-8841-4976-b20b-989ebba5eb3b
title: Glossar der Windows Imaging-Komponente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee6812024571727c8f769df88f8233119eed13ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368859"
---
# <a name="windows-imaging-component-glossary"></a><span data-ttu-id="6863f-103">Glossar der Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="6863f-103">Windows Imaging Component Glossary</span></span>

## <a name="b"></a><span data-ttu-id="6863f-104">B</span><span class="sxs-lookup"><span data-stu-id="6863f-104">B</span></span>

<dl> <dt>

<span data-ttu-id="6863f-105">**Bittiefe**</span><span class="sxs-lookup"><span data-stu-id="6863f-105">**bit depth**</span></span>
</dt> <dd>

<span data-ttu-id="6863f-106">Die Anzahl der Farbwerte, die einem einzelnen Pixel in einem Bild zugewiesen werden können.</span><span class="sxs-lookup"><span data-stu-id="6863f-106">The number of color values that can be assigned to a single pixel in an image.</span></span> <span data-ttu-id="6863f-107">Die Farbtiefe kann zwischen 1 Bit (schwarz und weiß) und 32 Bits (über 16,7 Millionen Farben) liegen.</span><span class="sxs-lookup"><span data-stu-id="6863f-107">Color depth can range from 1 bit (black and white) to 32 bits (over 16.7 million colors).</span></span> <span data-ttu-id="6863f-108">Siehe auch: Farbtiefe</span><span class="sxs-lookup"><span data-stu-id="6863f-108">See also: Color Depth</span></span>

</dd> <dt>

<span data-ttu-id="6863f-109">**Bits pro Pixel (BPP)**</span><span class="sxs-lookup"><span data-stu-id="6863f-109">**bits per pixel (bpp)**</span></span>
</dt> <dd>

<span data-ttu-id="6863f-110">Die Anzahl der Bits, die den Farbwert der einzelnen Pixel in einem digitalisierten Bild darstellen.</span><span class="sxs-lookup"><span data-stu-id="6863f-110">The number of bits that represent the color value of each pixel in a digitized image.</span></span> <span data-ttu-id="6863f-111">Siehe auch: BPP</span><span class="sxs-lookup"><span data-stu-id="6863f-111">See also:BPP</span></span>

</dd> </dl>

## <a name="c"></a><span data-ttu-id="6863f-112">C</span><span class="sxs-lookup"><span data-stu-id="6863f-112">C</span></span>

<dl> <dt>

<span data-ttu-id="6863f-113">**Clipper**</span><span class="sxs-lookup"><span data-stu-id="6863f-113">**clipper**</span></span>
</dt> <dd>

<span data-ttu-id="6863f-114">Ein iwicbitmapclipperobjekt.</span><span class="sxs-lookup"><span data-stu-id="6863f-114">An IWICBitmapClipper object.</span></span>

</dd> <dt>

<span data-ttu-id="6863f-115">**Codec**</span><span class="sxs-lookup"><span data-stu-id="6863f-115">**codec**</span></span>
</dt> <dd>

<span data-ttu-id="6863f-116">Ein Filter, der einen Datenstrom komprimiert (codiert) oder dekomprimiert (decodiert).</span><span class="sxs-lookup"><span data-stu-id="6863f-116">A filter that compresses (encodes) or decompresses (decodes) a data stream.</span></span>

</dd> <dt>

<span data-ttu-id="6863f-117">**Farb Kontext**</span><span class="sxs-lookup"><span data-stu-id="6863f-117">**color context**</span></span>
</dt> <dd>

<span data-ttu-id="6863f-118">Eine Abstraktion für ein Farbprofil.</span><span class="sxs-lookup"><span data-stu-id="6863f-118">An abstraction for a color profile.</span></span> <span data-ttu-id="6863f-119">Das Profil kann aus einer Datei geladen werden (d.h. "sRGB Color Space Profile. ICM") oder aus einem Arbeitsspeicher Puffer, der durchlesen abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6863f-119">The profile can be loaded from a file (ie. "sRGB Color Space Profile.icm") or from a memory buffer obtained by reading.</span></span> <span data-ttu-id="6863f-120">Farb Kontextinformationen werden von der IWICColorContext-Schnittstelle für WIC definiert und mit der GetColorContext-Methode abgerufen.</span><span class="sxs-lookup"><span data-stu-id="6863f-120">Color context information is defined by the IWICColorContext interface for WIC, and is retrieved with the GetColorContext method.</span></span>

</dd> <dt>

<span data-ttu-id="6863f-121">**Farb Transformation**</span><span class="sxs-lookup"><span data-stu-id="6863f-121">**color transform**</span></span>
</dt> <dd>

<span data-ttu-id="6863f-122">Zuordnung von Farben aus dem Quell Farb Kontext zum Ziel Farb Kontext in einem vorgegebenen Ausgabe Pixel Format.</span><span class="sxs-lookup"><span data-stu-id="6863f-122">Mapping colors from the source color context to the destination color context in a given output pixel format.</span></span>

</dd> <dt>

<span data-ttu-id="6863f-123">**CYMK-Farbmodell**</span><span class="sxs-lookup"><span data-stu-id="6863f-123">**CYMK color model**</span></span>
</dt> <dd>

<span data-ttu-id="6863f-124">Mehrdimensionaler farbiger farbiger Bereich, der aus den Intensitäten Cyan, Magenta, gelb und schwarz besteht, die eine bestimmte Farbe bilden.</span><span class="sxs-lookup"><span data-stu-id="6863f-124">Multidimensional color space consisting of the cyan, magenta, yellow, and black intensities that make up a given color.</span></span>

</dd> </dl>

## <a name="d"></a><span data-ttu-id="6863f-125">D</span><span class="sxs-lookup"><span data-stu-id="6863f-125">D</span></span>

<dl> <dt>

<span data-ttu-id="6863f-126">**der**</span><span class="sxs-lookup"><span data-stu-id="6863f-126">**decoder**</span></span>
</dt> <dd>

<span data-ttu-id="6863f-127">Siehe anderen Begriff: Codec</span><span class="sxs-lookup"><span data-stu-id="6863f-127">See Other Term: codec</span></span>

</dd> </dl>

## <a name="e"></a><span data-ttu-id="6863f-128">E</span><span class="sxs-lookup"><span data-stu-id="6863f-128">E</span></span>

<dl> <dt>

<span data-ttu-id="6863f-129">**ASA**</span><span class="sxs-lookup"><span data-stu-id="6863f-129">**encoder**</span></span>
</dt> <dd>

<span data-ttu-id="6863f-130">Siehe anderen Begriff: Codec</span><span class="sxs-lookup"><span data-stu-id="6863f-130">See Other Term: codec</span></span>

</dd> </dl>

## <a name="l"></a><span data-ttu-id="6863f-131">L</span><span class="sxs-lookup"><span data-stu-id="6863f-131">L</span></span>

<dl> <dt>

<span data-ttu-id="6863f-132">**verlustfreie**</span><span class="sxs-lookup"><span data-stu-id="6863f-132">**lossless**</span></span>
</dt> <dd>

<span data-ttu-id="6863f-133">Ein Komprimierungstyp, mit dem sichergestellt wird, dass die ursprünglichen Daten genau wieder hergestellt werden können, ohne dass die Bildqualität verloren geht.</span><span class="sxs-lookup"><span data-stu-id="6863f-133">A type of compression that ensures that the original data can be recovered exactly, with no loss in image quality.</span></span>

</dd> <dt>

<span data-ttu-id="6863f-134">**verlustbehafteten**</span><span class="sxs-lookup"><span data-stu-id="6863f-134">**lossy**</span></span>
</dt> <dd>

<span data-ttu-id="6863f-135">Ein Prozess zum Komprimieren von Daten, bei denen Informationen, die als unnötig erachtet werden, entfernt und bei der Dekomprimierung nicht wieder hergestellt werden können</span><span class="sxs-lookup"><span data-stu-id="6863f-135">A process for compressing data in which information deemed unnecessary is removed and cannot be recovered upon decompression.</span></span> <span data-ttu-id="6863f-136">Wird in der Regel mit Audiodaten und visuellen Daten verwendet, bei denen eine geringfügige Verschlechterung der Qualität akzeptabel ist.</span><span class="sxs-lookup"><span data-stu-id="6863f-136">Typically used with audio and visual data in which a slight degradation of quality is acceptable.</span></span>

</dd> </dl>

## <a name="m"></a><span data-ttu-id="6863f-137">M</span><span class="sxs-lookup"><span data-stu-id="6863f-137">M</span></span>

<dl> <dt>

<span data-ttu-id="6863f-138">**Multithread-Apartment (MTA)**</span><span class="sxs-lookup"><span data-stu-id="6863f-138">**multithreaded apartment (MTA)**</span></span>
</dt> <dd>

<span data-ttu-id="6863f-139">Eine Form von Multithreading, die von Component Object Model (com) unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="6863f-139">A form of multithreading that is supported by Component Object Model (COM).</span></span> <span data-ttu-id="6863f-140">In einem Multithread-Apartment Modell befinden sich alle Threads im Prozess, die als "freigegeben" initialisiert wurden, in einem einzigen Apartment.</span><span class="sxs-lookup"><span data-stu-id="6863f-140">In a multithreaded apartment model, all of the threads in the process that have been initialized as free-threaded reside in a single apartment.</span></span>

</dd> </dl>

## <a name="n"></a><span data-ttu-id="6863f-141">N</span><span class="sxs-lookup"><span data-stu-id="6863f-141">N</span></span>

<dl> <dt>

<span data-ttu-id="6863f-142">**Natives Pixel Format**</span><span class="sxs-lookup"><span data-stu-id="6863f-142">**native pixel format**</span></span>
</dt> <dd>

<span data-ttu-id="6863f-143">Eines der Pixel Formate, die von WIC bereitgestellt werden, wobei das Speicher Layout der einzelnen Pixel in einer Bitmap beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="6863f-143">One of the pixel formats provided by WIC, wherein the memory layout of each pixel in a bitmap is described.</span></span>

</dd> </dl>

## <a name="p"></a><span data-ttu-id="6863f-144">P</span><span class="sxs-lookup"><span data-stu-id="6863f-144">P</span></span>

<dl> <dt>

<span data-ttu-id="6863f-145">**Messer**</span><span class="sxs-lookup"><span data-stu-id="6863f-145">**palette**</span></span>
</dt> <dd>

<span data-ttu-id="6863f-146">Ein Satz von Farben, die von einem Objekt oder einer Anwendung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6863f-146">Set of colors used by an object or application.</span></span>

</dd> <dt>

<span data-ttu-id="6863f-147">**Foto-metadatenrichtlinie**</span><span class="sxs-lookup"><span data-stu-id="6863f-147">**photo metadata policy**</span></span>
</dt> <dd>

<span data-ttu-id="6863f-148">Die Windows-Richtlinie zum Lesen, schreiben und Entfernen von Bild Metadaten.</span><span class="sxs-lookup"><span data-stu-id="6863f-148">The windows policy for reading, writing, and removing image metadata.</span></span>

</dd> <dt>

<span data-ttu-id="6863f-149">**Pixelformat**</span><span class="sxs-lookup"><span data-stu-id="6863f-149">**pixel format**</span></span>
</dt> <dd>

<span data-ttu-id="6863f-150">Größe und Anordnung von Pixel Farbkomponenten im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="6863f-150">Size and arrangement of pixel color components in memory.</span></span> <span data-ttu-id="6863f-151">Sie wird durch die Gesamtzahl der pro Pixel verwendeten Bits und die Anzahl der Bits angegeben, die zum Speichern der roten, grünen, blauen und Alpha Komponenten der Farbe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6863f-151">It is specified by the total number of bits used per pixel and the number of bits used to store the red, green, blue, and alpha components of the color.</span></span> <span data-ttu-id="6863f-152">Beispielsweise verwendet das RGB24-Pixel-Format 24 Bits zum Speichern einer Pixelfarbe mit jeweils acht Bits für Rot, grün und blau.</span><span class="sxs-lookup"><span data-stu-id="6863f-152">For example, the RGB24 pixel format uses 24 bits to store a pixel color, with eight bits each for red, green, and blue.</span></span> <span data-ttu-id="6863f-153">Das ARGB32-Pixel Format verwendet 32 Bits mit 24 Bits an Farbinformationen und 8 Bits von Alphakanal Informationen.</span><span class="sxs-lookup"><span data-stu-id="6863f-153">The ARGB32 pixel format uses 32 bits, with 24 bits of color information and 8 bits of alpha channel information.</span></span>

</dd> <dt>

<span data-ttu-id="6863f-154">**Progressive Decodierung**</span><span class="sxs-lookup"><span data-stu-id="6863f-154">**progressive decoding**</span></span>
</dt> <dd>

<span data-ttu-id="6863f-155">Der Prozess für das Decodieren von Bildern, die mit Informationen über die verschiedenen Decodierungs Ebenen codiert wurden.</span><span class="sxs-lookup"><span data-stu-id="6863f-155">The process for decoding images that have been encoded with information about the different decoding levels.</span></span>

</dd> </dl>

## <a name="s"></a><span data-ttu-id="6863f-156">E</span><span class="sxs-lookup"><span data-stu-id="6863f-156">S</span></span>

<dl> <dt>

<span data-ttu-id="6863f-157">**Streich**</span><span class="sxs-lookup"><span data-stu-id="6863f-157">**stream**</span></span>
</dt> <dd>

<span data-ttu-id="6863f-158">Bezieht sich auf eine IStream-com-Schnittstelle, die zum sequenziellen lesen oder Schreiben von Daten in Dateien, Arbeitsspeicher oder Netzwerkspeicher Orte verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="6863f-158">Refers to an IStream COM interface which can be used to sequentially read or write data to files, memory, or network locations.</span></span>

</dd> </dl>

## <a name="t"></a><span data-ttu-id="6863f-159">T</span><span class="sxs-lookup"><span data-stu-id="6863f-159">T</span></span>

<dl> <dt>

<span data-ttu-id="6863f-160">**Tonkurve**</span><span class="sxs-lookup"><span data-stu-id="6863f-160">**tone curve**</span></span>
</dt> <dd>

<span data-ttu-id="6863f-161">Ein in digitaler Fotografie verwendetes Diagramm, das den klanglichen Bereich des Bilds anzeigt.</span><span class="sxs-lookup"><span data-stu-id="6863f-161">A graph used in digital photography that displays the tonal range of the image.</span></span>

</dd> </dl>

## <a name="w"></a><span data-ttu-id="6863f-162">W</span><span class="sxs-lookup"><span data-stu-id="6863f-162">W</span></span>

<dl> <dt>

<span data-ttu-id="6863f-163">**Windows Imaging-Komponente (WIC)**</span><span class="sxs-lookup"><span data-stu-id="6863f-163">**Windows Imaging Component (WIC)**</span></span>
</dt> <dd>

<span data-ttu-id="6863f-164">Eine erweiterbare Plattform, die eine Low-Level-API für digitale Images bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="6863f-164">An extensible platform that provides low-level API for digital images.</span></span>

</dd> </dl>

 

 



