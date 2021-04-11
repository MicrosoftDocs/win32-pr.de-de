---
description: Die Windows Imaging Component (WIC) stellt ein erweiterbares Framework zum Arbeiten mit Bildern und Bild Metadaten bereit.
ms.assetid: a05b496a-bd4c-4065-8060-df0f8930cde7
title: Übersicht über die Windows Imaging-Komponente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 764260dd9375f1372c1936c7dbd776295eb34433
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216396"
---
# <a name="windows-imaging-component-overview"></a><span data-ttu-id="3a34e-103">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="3a34e-103">Windows Imaging Component Overview</span></span>

<span data-ttu-id="3a34e-104">Die Windows Imaging Component (WIC) stellt ein erweiterbares Framework zum Arbeiten mit Bildern und Bild Metadaten bereit.</span><span class="sxs-lookup"><span data-stu-id="3a34e-104">The Windows Imaging Component (WIC) provides an extensible framework for working with images and image metadata.</span></span> <span data-ttu-id="3a34e-105">Mit WIC können unabhängige Softwarehersteller (ISVs) und unabhängige Hardwarehersteller (IHVs) ihre eigenen Bild Codecs entwickeln und die gleiche Platt Form Unterstützung wie Standard Image Formate (z. b. TIFF, JPEG, PNG, GIF, BMP und HDPhoto) erhalten.</span><span class="sxs-lookup"><span data-stu-id="3a34e-105">WIC makes it possible for independent software vendors (ISVs) and independent hardware vendors (IHVs) to develop their own image codecs and get the same platform support as standard image formats (for example, TIFF, JPEG, PNG, GIF, BMP, and HDPhoto).</span></span> <span data-ttu-id="3a34e-106">Ein einzelner, konsistentes Satz von Schnittstellen wird unabhängig vom Bildformat für die gesamte Bildverarbeitung verwendet, sodass jede Anwendung, die WIC verwendet, automatisch Unterstützung für neue Bildformate erhält, sobald der Codec installiert ist.</span><span class="sxs-lookup"><span data-stu-id="3a34e-106">A single, consistent set of interfaces is used for all image processing, regardless of image format, so any application using the WIC gets automatic support for new image formats as soon as the codec is installed.</span></span> <span data-ttu-id="3a34e-107">Das erweiterbare metadatenframework ermöglicht es Anwendungen, eigene proprietäre Metadaten direkt in Bilddateien zu lesen und zu schreiben, sodass die Metadaten niemals verloren gehen oder von dem Image getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="3a34e-107">The extensible metadata framework makes it possible for applications to read and write their own proprietary metadata directly to image files, so the metadata never gets lost or separated from the image.</span></span>

<span data-ttu-id="3a34e-108">Das Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="3a34e-108">This topic includes the following sections.</span></span>

-   [<span data-ttu-id="3a34e-109">Windows Imaging-Komponenten Features</span><span class="sxs-lookup"><span data-stu-id="3a34e-109">Windows Imaging Component Features</span></span>](#windows-imaging-component-features)
-   [<span data-ttu-id="3a34e-110">Native Codecs</span><span class="sxs-lookup"><span data-stu-id="3a34e-110">Native Codecs</span></span>](#native-codecs)
-   [<span data-ttu-id="3a34e-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3a34e-111">Related topics</span></span>](#related-topics)

## <a name="windows-imaging-component-features"></a><span data-ttu-id="3a34e-112">Windows Imaging-Komponenten Features</span><span class="sxs-lookup"><span data-stu-id="3a34e-112">Windows Imaging Component Features</span></span>

<span data-ttu-id="3a34e-113">Die wichtigsten Features von WIC sind:</span><span class="sxs-lookup"><span data-stu-id="3a34e-113">The primary features of WIC are:</span></span>

-   <span data-ttu-id="3a34e-114">Ermöglicht es Anwendungsentwicklern, Bild Verarbeitungsvorgänge in beliebigen Bildformaten durch einen einzelnen, konsistenten Satz von allgemeinen Schnittstellen auszuführen, ohne dass vorherige Kenntnisse über bestimmte Bildformate erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="3a34e-114">Enables application developers to perform image processing operations on any image format through a single, consistent set of common interfaces, without requiring prior knowledge of specific image formats.</span></span>
-   <span data-ttu-id="3a34e-115">Bietet eine erweiterbare "Plug & Play"-Architektur für Bild Codecs, Pixel Formate und Metadaten mit automatischer Lauf Zeit Ermittlung neuer Formate.</span><span class="sxs-lookup"><span data-stu-id="3a34e-115">Provides an extensible "plug and play" architecture for image codecs, pixel formats, and metadata, with automatic run-time discovery of new formats.</span></span>
-   <span data-ttu-id="3a34e-116">Unterstützt das Lesen und schreiben beliebiger Metadaten in Bilddateien mit der Möglichkeit, unbekannte Metadaten während der Bearbeitung beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="3a34e-116">Supports reading and writing of arbitrary metadata in image files, with the ability to preserve unrecognized metadata during editing.</span></span>
-   <span data-ttu-id="3a34e-117">Speichert High-Bit-dateibilddaten (bis zu 32 Bits pro Kanal) in der gesamten Bild Verarbeitungs Pipeline.</span><span class="sxs-lookup"><span data-stu-id="3a34e-117">Preserves high bit depth image data, up to 32 bits per channel, throughout the image processing pipeline.</span></span>
-   <span data-ttu-id="3a34e-118">Bietet integrierte Unterstützung für die beliebtesten Bildformate, Pixel Formate und Metadatenschemas.</span><span class="sxs-lookup"><span data-stu-id="3a34e-118">Provides built-in support for most popular image formats, pixel formats, and metadata schemas.</span></span>

## <a name="native-codecs"></a><span data-ttu-id="3a34e-119">Native Codecs</span><span class="sxs-lookup"><span data-stu-id="3a34e-119">Native Codecs</span></span>

<span data-ttu-id="3a34e-120">WIC umfasst mehrere integrierte Codecs.</span><span class="sxs-lookup"><span data-stu-id="3a34e-120">WIC includes several built-in codecs.</span></span> <span data-ttu-id="3a34e-121">Die folgenden Standard-Codecs werden mit der-Plattform bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="3a34e-121">The following standard codecs are provided with the platform.</span></span> 

| <span data-ttu-id="3a34e-122">Codec</span><span class="sxs-lookup"><span data-stu-id="3a34e-122">Codec</span></span>                                                                                             | <span data-ttu-id="3a34e-123">MIME-Typen</span><span class="sxs-lookup"><span data-stu-id="3a34e-123">Mime Types</span></span>                       | <span data-ttu-id="3a34e-124">Decoder</span><span class="sxs-lookup"><span data-stu-id="3a34e-124">Decoders</span></span> | <span data-ttu-id="3a34e-125">Encoder</span><span class="sxs-lookup"><span data-stu-id="3a34e-125">Encoders</span></span> |
|---------------------------------------------------------------------------------------------------|----------------------------------|----------|----------|
| <span data-ttu-id="3a34e-126">BMP (Windows-Bitmap-Format), BMP-Spezifikation V5.</span><span class="sxs-lookup"><span data-stu-id="3a34e-126">BMP (Windows Bitmap Format), BMP Specification v5.</span></span>                                                | <span data-ttu-id="3a34e-127">image/bmp</span><span class="sxs-lookup"><span data-stu-id="3a34e-127">image/bmp</span></span>                        | <span data-ttu-id="3a34e-128">Ja</span><span class="sxs-lookup"><span data-stu-id="3a34e-128">Yes</span></span>      | <span data-ttu-id="3a34e-129">Ja</span><span class="sxs-lookup"><span data-stu-id="3a34e-129">Yes</span></span>      |
| <span data-ttu-id="3a34e-130">GIF (Graphics Interchange Format 89A), GIF-Spezifikation 89A/89m</span><span class="sxs-lookup"><span data-stu-id="3a34e-130">GIF (Graphics Interchange Format 89a), GIF Specification 89a/89m</span></span>                                  | <span data-ttu-id="3a34e-131">image/gif</span><span class="sxs-lookup"><span data-stu-id="3a34e-131">image/gif</span></span>                        | <span data-ttu-id="3a34e-132">Ja</span><span class="sxs-lookup"><span data-stu-id="3a34e-132">Yes</span></span>      | <span data-ttu-id="3a34e-133">Ja</span><span class="sxs-lookup"><span data-stu-id="3a34e-133">Yes</span></span>      |
| <span data-ttu-id="3a34e-134">ICO (Symbol Format)</span><span class="sxs-lookup"><span data-stu-id="3a34e-134">ICO (Icon Format)</span></span>                                                                                 | <span data-ttu-id="3a34e-135">Image/ICO</span><span class="sxs-lookup"><span data-stu-id="3a34e-135">image/ico</span></span>                        | <span data-ttu-id="3a34e-136">Ja</span><span class="sxs-lookup"><span data-stu-id="3a34e-136">Yes</span></span>      | <span data-ttu-id="3a34e-137">Nein</span><span class="sxs-lookup"><span data-stu-id="3a34e-137">No</span></span>       |
| <span data-ttu-id="3a34e-138">JPEG (Joint Photographic Experts Group), JFIF-Spezifikation 1,02</span><span class="sxs-lookup"><span data-stu-id="3a34e-138">JPEG (Joint Photographic Experts Group), JFIF Specification 1.02</span></span>                                  | <span data-ttu-id="3a34e-139">Image/JPEG, Image/jpe, Image/JPG</span><span class="sxs-lookup"><span data-stu-id="3a34e-139">image/jpeg, image/jpe, image/jpg</span></span> | <span data-ttu-id="3a34e-140">Ja</span><span class="sxs-lookup"><span data-stu-id="3a34e-140">Yes</span></span>      | <span data-ttu-id="3a34e-141">Ja</span><span class="sxs-lookup"><span data-stu-id="3a34e-141">Yes</span></span>      |
| <span data-ttu-id="3a34e-142">PNG (Portable Network Graphics), PNG-Spezifikation 1,2</span><span class="sxs-lookup"><span data-stu-id="3a34e-142">PNG (Portable Network Graphics), PNG Specification 1.2</span></span>                                            | <span data-ttu-id="3a34e-143">image/png</span><span class="sxs-lookup"><span data-stu-id="3a34e-143">image/png</span></span>                        | <span data-ttu-id="3a34e-144">Ja</span><span class="sxs-lookup"><span data-stu-id="3a34e-144">Yes</span></span>      | <span data-ttu-id="3a34e-145">Ja</span><span class="sxs-lookup"><span data-stu-id="3a34e-145">Yes</span></span>      |
| <span data-ttu-id="3a34e-146">TIFF (Tagged Image File Format), TIFF-Spezifikation 6,0</span><span class="sxs-lookup"><span data-stu-id="3a34e-146">TIFF (Tagged Image File Format), TIFF Specification 6.0</span></span>                                           | <span data-ttu-id="3a34e-147">Bild/TIFF, Bild/TIF</span><span class="sxs-lookup"><span data-stu-id="3a34e-147">image/tiff, image/tif</span></span>            | <span data-ttu-id="3a34e-148">Ja</span><span class="sxs-lookup"><span data-stu-id="3a34e-148">Yes</span></span>      | <span data-ttu-id="3a34e-149">Ja</span><span class="sxs-lookup"><span data-stu-id="3a34e-149">Yes</span></span>      |
| <span data-ttu-id="3a34e-150">Windows Media Photo, [HD Photo Specification 1,0](https://www.microsoft.com/whdc/xps/wmphoto.mspx)</span><span class="sxs-lookup"><span data-stu-id="3a34e-150">Windows Media Photo, [HD Photo Specification 1.0](https://www.microsoft.com/whdc/xps/wmphoto.mspx)</span></span> | <span data-ttu-id="3a34e-151">Image/vnd. ms-Phot</span><span class="sxs-lookup"><span data-stu-id="3a34e-151">image/vnd.ms-phot</span></span>                | <span data-ttu-id="3a34e-152">Ja</span><span class="sxs-lookup"><span data-stu-id="3a34e-152">Yes</span></span>      | <span data-ttu-id="3a34e-153">Ja</span><span class="sxs-lookup"><span data-stu-id="3a34e-153">Yes</span></span>      |
| <span data-ttu-id="3a34e-154">DDS (DirectDraw-Oberfläche)</span><span class="sxs-lookup"><span data-stu-id="3a34e-154">DDS (DirectDraw Surface)</span></span>                                                                          | <span data-ttu-id="3a34e-155">Image/vnd. ms-DDS</span><span class="sxs-lookup"><span data-stu-id="3a34e-155">image/vnd.ms-dds</span></span>                 | <span data-ttu-id="3a34e-156">Ja</span><span class="sxs-lookup"><span data-stu-id="3a34e-156">Yes</span></span>      | <span data-ttu-id="3a34e-157">Ja</span><span class="sxs-lookup"><span data-stu-id="3a34e-157">Yes</span></span>      |



 

## <a name="related-topics"></a><span data-ttu-id="3a34e-158">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3a34e-158">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="3a34e-159">**Licher**</span><span class="sxs-lookup"><span data-stu-id="3a34e-159">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3a34e-160">Übersicht über WIC-Metadaten</span><span class="sxs-lookup"><span data-stu-id="3a34e-160">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

<span data-ttu-id="3a34e-161">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="3a34e-161">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="3a34e-162">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="3a34e-162">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

<span data-ttu-id="3a34e-163">[AITCodec-Beispielcodec](/previous-versions/dotnet/netframework-3.0/ms771770(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3a34e-163">[AITCodec Sample CODEC](/previous-versions/dotnet/netframework-3.0/ms771770(v=vs.85))</span></span>
</dt> </dl>

 

 
