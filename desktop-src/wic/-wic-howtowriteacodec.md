---
description: In diesem Abschnitt der Themen finden Entwickler Anleitungen zum Implementieren von Bild Dateiformaten-Codecs, die innerhalb des WIC-Frameworks (Windows Imaging Component) funktionieren.
ms.assetid: 58f03dc2-cc31-4d76-b75a-f332da1f900f
title: Schreiben eines WIC-Enabled Codecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee694d9a857781e97a31cb37f5ef18c518dae964
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865551"
---
# <a name="how-to-write-a-wic-enabled-codec"></a><span data-ttu-id="b0b17-103">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="b0b17-103">How to Write a WIC-Enabled Codec</span></span>

<span data-ttu-id="b0b17-104">In diesem Abschnitt der Themen finden Entwickler Anleitungen zum Implementieren von Bild Dateiformaten-Codecs, die innerhalb des WIC-Frameworks (Windows Imaging Component) funktionieren.</span><span class="sxs-lookup"><span data-stu-id="b0b17-104">This section of topics provide developers with guidance on how to implement image file format codecs that will function within the Windows Imaging Component (WIC) framework.</span></span>

<dl>

[<span data-ttu-id="b0b17-105">Introduction (Einführung)</span><span class="sxs-lookup"><span data-stu-id="b0b17-105">Introduction</span></span>](-wic-howtowriteacodec-intro.md)  
[<span data-ttu-id="b0b17-106">Funktionsweise der Windows Imaging Component (WIC)</span><span class="sxs-lookup"><span data-stu-id="b0b17-106">How The Windows Imaging Component (WIC) Works</span></span>](-wic-howwicworks.md)  
<dl>

[<span data-ttu-id="b0b17-107">Ermittlung und Schiedsgerichtsbarkeit</span><span class="sxs-lookup"><span data-stu-id="b0b17-107">Discovery and Arbitration</span></span>](-wic-howwicworks.md)  
[<span data-ttu-id="b0b17-108">Decodierung</span><span class="sxs-lookup"><span data-stu-id="b0b17-108">Decoding</span></span>](-wic-howwicworks.md)  
[<span data-ttu-id="b0b17-109">Codieren</span><span class="sxs-lookup"><span data-stu-id="b0b17-109">Encoding</span></span>](-wic-howwicworks.md)  
[<span data-ttu-id="b0b17-110">Die Lebensdauer eines Codecs.</span><span class="sxs-lookup"><span data-stu-id="b0b17-110">The Lifetime of a Codec</span></span>](-wic-howwicworks.md)  
[<span data-ttu-id="b0b17-111">Gewusst wie: WIC-Aktivieren eines Codecs</span><span class="sxs-lookup"><span data-stu-id="b0b17-111">How to WIC-enable a Codec</span></span>](-wic-howwicworks.md)  
[<span data-ttu-id="b0b17-112">Multithread-Apartment Unterstützung in WIC</span><span class="sxs-lookup"><span data-stu-id="b0b17-112">Multi-Threaded Apartment Support in WIC</span></span>](-wic-howwicworks.md)  
<span data-ttu-id="b0b17-113"></dl> </dd> <a href="-wic-implementingwicdecoder.md">Implementieren eines WIC-Enabled Decoders</a></span><span class="sxs-lookup"><span data-stu-id="b0b17-113"></dl> </dd> <a href="-wic-implementingwicdecoder.md">Implementing a WIC-Enabled Decoder</a></span></span><dl>

[<span data-ttu-id="b0b17-114">Decoder-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="b0b17-114">Decoder Interfaces</span></span>](-wic-decoderinterfaces.md)<dl>

[<span data-ttu-id="b0b17-115">IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="b0b17-115">IWICBitmapDecoder</span></span>](-wic-imp-iwicbitmapdecoder.md)  
[<span data-ttu-id="b0b17-116">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="b0b17-116">IWICBitmapCodecProgressNotification</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)  
[<span data-ttu-id="b0b17-117">IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="b0b17-117">IWICBitmapSource</span></span>](-wic-imp-iwicbitmapsource.md)  
[<span data-ttu-id="b0b17-118">IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="b0b17-118">IWICBitmapFrameDecode</span></span>](-wic-imp-iwicbitmapframedecode.md)  
[<span data-ttu-id="b0b17-119">IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="b0b17-119">IWICMetadataBlockReader</span></span>](-wic-imp-iwicmetadatablockreader.md)  
[<span data-ttu-id="b0b17-120">IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="b0b17-120">IWICBitmapSourceTransform</span></span>](-wic-imp-iwicbitmapsourcetransform.md)  
[<span data-ttu-id="b0b17-121">IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="b0b17-121">IWICDevelopRaw</span></span>](-wic-imp-iwicdevelopraw.md)  
<span data-ttu-id="b0b17-122"></dl> </dd> </dl> </dd> <a href="-wic-implementingwicencoder.md">Implementieren eines WIC-Enabled Encoders</a>  
</span><span class="sxs-lookup"><span data-stu-id="b0b17-122"></dl> </dd> </dl> </dd> <a href="-wic-implementingwicencoder.md">Implementing a WIC-Enabled Encoder</a>  
</span></span><dl>

[<span data-ttu-id="b0b17-123">Encoder-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="b0b17-123">Encoder Interfaces</span></span>](-wic-encoderinterfaces.md)  
<dl>

[<span data-ttu-id="b0b17-124">Iwicbitmapcoder</span><span class="sxs-lookup"><span data-stu-id="b0b17-124">IWICBitmapEncoder</span></span>](-wic-imp-iwicbitmapencoder.md)  
[<span data-ttu-id="b0b17-125">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="b0b17-125">IWICBitmapCodecProgressNotification</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)  
[<span data-ttu-id="b0b17-126">IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="b0b17-126">IWICBitmapFrameEncode</span></span>](-wic-imp-iwicbitmapframeencode.md)  
[<span data-ttu-id="b0b17-127">IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="b0b17-127">IWICMetadataBlockWriter</span></span>](-wic-imp-iwicmetadatablockwriter.md)  
<span data-ttu-id="b0b17-128"></dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Codec-Installation und-Registrierung</a>  
</span><span class="sxs-lookup"><span data-stu-id="b0b17-128"></dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Codec Installation and Registration</a>  
</span></span><dl>

[<span data-ttu-id="b0b17-129">Registrieren eines Codecs</span><span class="sxs-lookup"><span data-stu-id="b0b17-129">Registering a Codec</span></span>](-wic-codecinstallandreg.md)  
<dl>

[<span data-ttu-id="b0b17-130">Allgemeine Register Einträge</span><span class="sxs-lookup"><span data-stu-id="b0b17-130">General Register Entries</span></span>](-wic-generalregentries.md)  
[<span data-ttu-id="b0b17-131">Codierungs spezifische Registrierungseinträge</span><span class="sxs-lookup"><span data-stu-id="b0b17-131">Encoder-Specific Registry Entries</span></span>](-wic-encoderregentries.md)  
<dl>

[<span data-ttu-id="b0b17-132">Registrieren eines Container Formats mit metadatenwritern</span><span class="sxs-lookup"><span data-stu-id="b0b17-132">Registering a Container Format with Metadata Writers</span></span>](-wic-encoderregentries.md)  
<span data-ttu-id="b0b17-133"></dl> </dd> <a href="-wic-decoderregentries.md">Codierungs spezifische Registrierungseinträge</a>  
</span><span class="sxs-lookup"><span data-stu-id="b0b17-133"></dl> </dd> <a href="-wic-decoderregentries.md">Encoder-Specific Registry Entries</a>  
</span></span><dl>

[<span data-ttu-id="b0b17-134">Registrieren eines neuen Container Formats mit metadatenlesern</span><span class="sxs-lookup"><span data-stu-id="b0b17-134">Registering a New Container Format with Metadata Readers</span></span>](-wic-decoderregentries.md)  
<span data-ttu-id="b0b17-135"></dl> </dd> <a href="-wic-integrationregentries.md">Integration in Windows Vista Photogallery und Explorer</a>  
</span><span class="sxs-lookup"><span data-stu-id="b0b17-135"></dl> </dd> <a href="-wic-integrationregentries.md">Integration with Windows Vista PhotoGallery and Explorer</a>  
</span></span><dl>

[<span data-ttu-id="b0b17-136">Windows-Eigenschaften Speicher</span><span class="sxs-lookup"><span data-stu-id="b0b17-136">Windows Property Store</span></span>](-wic-integrationregentries.md)  
[<span data-ttu-id="b0b17-137">Windows Vista-Fotogalerie</span><span class="sxs-lookup"><span data-stu-id="b0b17-137">Windows Vista Photo Gallery</span></span>](-wic-integrationregentries.md)  
[<span data-ttu-id="b0b17-138">Windows Vista-Miniaturansicht-Cache</span><span class="sxs-lookup"><span data-stu-id="b0b17-138">Windows Vista Thumbnail Cache</span></span>](-wic-integrationregentries.md)  
<span data-ttu-id="b0b17-139"></dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Aktualisieren des Miniatur Ansichts Caches bei der Installation eines Codecs</a> [, der Ihren WIC-Enabled Codec für Benutzer zur Verfügung stellt](-wic-codecinstallandreg.md) </dl> </dd> <a href="-wic-howtowriteacodec-conclusion.md"></a>  
</span><span class="sxs-lookup"><span data-stu-id="b0b17-139"></dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Updating the Thumbnail Cache when Installing a Codec</a> [Making Your WIC-Enabled Codec Available to Users](-wic-codecinstallandreg.md) </dl> </dd> <a href="-wic-howtowriteacodec-conclusion.md">Conclusion</a>  
</span></span></dl>

## <a name="related-topics"></a><span data-ttu-id="b0b17-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b0b17-140">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b0b17-141">**Licher**</span><span class="sxs-lookup"><span data-stu-id="b0b17-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b0b17-142">Einführung (Schreiben eines WIC-Enabled Codecs)</span><span class="sxs-lookup"><span data-stu-id="b0b17-142">Introduction (How to Write a WIC-Enabled CODEC)</span></span>](-wic-howtowriteacodec-intro.md)
</dt> <dt>

[<span data-ttu-id="b0b17-143">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="b0b17-143">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



