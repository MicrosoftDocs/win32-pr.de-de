---
description: Metadatenunterstützung
ms.assetid: f3b4a3d9-a353-4af8-9998-cb7da7a062b7
title: Metadatenunterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32499a88bd9cc12186629476f4d9f32a6e811858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351416"
---
# <a name="metadata-support"></a><span data-ttu-id="dd9fb-103">Metadatenunterstützung</span><span class="sxs-lookup"><span data-stu-id="dd9fb-103">Metadata Support</span></span>

<span data-ttu-id="dd9fb-104">Unformatierte Formate sollten auch allgemeine metadatenlese-und Schreib Szenarien für Images in Windows unterstützen.</span><span class="sxs-lookup"><span data-stu-id="dd9fb-104">RAW formats should also support the common metadata read and write scenarios for images in Windows.</span></span> <span data-ttu-id="dd9fb-105">Microsoft hat eine Reihe von systemeigenen metadatenanbietern für die austauschbare Image Datei (EXIF), den International Press Telecommunications Council (IPTC) und die Extensible Metadata Platform (XMP)-Metadaten entwickelt, die derzeit nur für TIFF-und JPEG-Container aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="dd9fb-105">Microsoft has developed a set of native metadata providers for exchangeable image file (EXIF), International Press Telecommunications Council (IPTC), and Extensible Metadata Platform (XMP) metadata that are currently invoked only for TIFF and JPEG containers.</span></span> <span data-ttu-id="dd9fb-106">Wenn das RAW-Image in einem dieser Containerformate gespeichert wird, wird empfohlen, die integrierten Metadatenanbieter von Windows zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="dd9fb-106">If the RAW image is stored in one of these container formats, it is recommended to use the Windows built-in metadata providers.</span></span> <span data-ttu-id="dd9fb-107">Der Codec-Autor ist jedoch dafür verantwortlich, dies ordnungsgemäß zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="dd9fb-107">However, the codec author is responsible for configuring this properly.</span></span> <span data-ttu-id="dd9fb-108">Bei unformatierten Dateien, die nicht auf einem TIFF-Container basieren, ist es möglicherweise notwendig, EXIF-, IPTC-oder XMP-Writer zu implementieren, da die integrierten Reader und Writer erwarten, dass die Daten mit den Layout-Spezifikationen von EXIF, IPTC und XMP auf dem Datenträger übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="dd9fb-108">For RAW files that are not based on a TIFF container, it might be necessary to implement EXIF, IPTC, or XMP writers because the built-in readers and writers expect the data to conform to EXIF, IPTC, and XMP on-disk layout specifications.</span></span> <span data-ttu-id="dd9fb-109">Codec-Autoren können auch Ihre eigenen Anbieter für benutzerdefinierte Metadaten implementieren.</span><span class="sxs-lookup"><span data-stu-id="dd9fb-109">Codec authors can also implement their own providers for any custom metadata.</span></span>

<span data-ttu-id="dd9fb-110">Aufgrund der Architektur von Windows Imaging Component (WIC) können metadatenwriter nur über eine Instanz eines Bild Encoders aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="dd9fb-110">Because of the architecture of Windows Imaging Component (WIC), metadata writers can be invoked only through an instance of an image encoder.</span></span> <span data-ttu-id="dd9fb-111">Daher sollten Besitzer von rohformaten mindestens einen "Stub" [**wicrawparameterset. wicautoadjustedparameterset**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) -Encoder erstellen, auch wenn die tatsächliche Codierung von Pixeln in ein RAW-Format nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="dd9fb-111">Therefore, RAW format owners should create at least a "stub" [**WICRawParameterSet.WICAutoAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) encoder, even if the actual encoding of pixels into a RAW format is not implemented.</span></span> <span data-ttu-id="dd9fb-112">Der Codec-Autor muss die richtigen Metadatenhandler aufrufen:</span><span class="sxs-lookup"><span data-stu-id="dd9fb-112">The codec author must invoke the proper metadata handlers:</span></span>

-   <span data-ttu-id="dd9fb-113">[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) für den Decoder und den Frame Decoder entsprechend.</span><span class="sxs-lookup"><span data-stu-id="dd9fb-113">[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) on both the decoder and frame decoder as appropriate.</span></span>
-   <span data-ttu-id="dd9fb-114">[**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) sowohl für den Encoder als auch den Frame Encoder.</span><span class="sxs-lookup"><span data-stu-id="dd9fb-114">[**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) on both the encoder and frame encoder as appropriate.</span></span>

<span data-ttu-id="dd9fb-115">Zur Unterstützung aller erwarteten Szenarien bei der Abbild Erstellung von Anwendungen in Windows Vista wird empfohlen, dass Codec-Anbieter mindestens Folgendes unterstützen:</span><span class="sxs-lookup"><span data-stu-id="dd9fb-115">To support all of the anticipated scenarios in imaging applications in Windows Vista, it is recommended that codec vendors support the following at a minimum:</span></span>

-   <span data-ttu-id="dd9fb-116">EXIF-Lesevorgang</span><span class="sxs-lookup"><span data-stu-id="dd9fb-116">EXIF read</span></span>
-   <span data-ttu-id="dd9fb-117">Partieller EXIF-Schreibvorgang (um Updates zum Erfassen von Datum und Uhrzeit zuzulassen)</span><span class="sxs-lookup"><span data-stu-id="dd9fb-117">Partial EXIF write (to permit updates to capture date and time)</span></span>
-   <span data-ttu-id="dd9fb-118">XMP-Lese-und-Schreibvorgänge (einschließlich optional IPTC-Kern für XMP)</span><span class="sxs-lookup"><span data-stu-id="dd9fb-118">XMP read and write (including optionally IPTC Core for XMP)</span></span>
-   <span data-ttu-id="dd9fb-119">IPTC IIMv4 lesen und schreiben</span><span class="sxs-lookup"><span data-stu-id="dd9fb-119">IPTC IIMv4 read and write</span></span>

<span data-ttu-id="dd9fb-120">Der größte Teil des metadatenzugriffs (sowohl Lese-als auch Schreibzugriff) in Windows Vista erfolgt über die [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) -oder [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="dd9fb-120">Most of the metadata access (both read and write) in Windows Vista occurs through the [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) or [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) interface.</span></span> <span data-ttu-id="dd9fb-121">Um an der Windows Vista-metadatenumgebung teilnehmen zu können, müssen unformatierte Codec-Autoren die [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) -Methode und die [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) -Methode implementieren.</span><span class="sxs-lookup"><span data-stu-id="dd9fb-121">Therefore, to participate in the Windows Vista metadata experiences, RAW codec authors must implement the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) and [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd9fb-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dd9fb-122">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="dd9fb-123">**Licher**</span><span class="sxs-lookup"><span data-stu-id="dd9fb-123">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="dd9fb-124">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="dd9fb-124">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="dd9fb-125">WIC-Richtlinien für Kamera Rohbild Formate</span><span class="sxs-lookup"><span data-stu-id="dd9fb-125">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="dd9fb-126">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="dd9fb-126">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



