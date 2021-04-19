---
description: 'Vollständigkeit der Features: Empfohlene Schnittstellen'
ms.assetid: 759bf253-7450-4895-a550-9f81f3498f79
title: 'Vollständigkeit der Features: Empfohlene Schnittstellen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1dba4bcc029b2205985afb443526376c0eecb16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352232"
---
# <a name="feature-completeness-recommended-interfaces"></a><span data-ttu-id="d5f3f-103">Vollständigkeit der Features: Empfohlene Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="d5f3f-103">Feature Completeness: Recommended Interfaces</span></span>

<span data-ttu-id="d5f3f-104">In der folgenden Tabelle sind die WIC-Schnittstellen (Windows Imaging Component, Windows Imaging Component) aufgelistet, die von den</span><span class="sxs-lookup"><span data-stu-id="d5f3f-104">The following table lists the Windows Imaging Component (WIC) interfaces RAW codecs should implement.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d5f3f-105">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d5f3f-105">Interface</span></span></th>
<th><span data-ttu-id="d5f3f-106">Erforderlich für</span><span class="sxs-lookup"><span data-stu-id="d5f3f-106">Required for</span></span></th>
<th><span data-ttu-id="d5f3f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d5f3f-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d5f3f-108"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a></span><span class="sxs-lookup"><span data-stu-id="d5f3f-108"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a></span></span></td>
<td><span data-ttu-id="d5f3f-109">Decoder</span><span class="sxs-lookup"><span data-stu-id="d5f3f-109">Decoders</span></span></td>
<td><span data-ttu-id="d5f3f-110">Stellt den Startpunkt für das Decodieren einer Bilddatei dar.</span><span class="sxs-lookup"><span data-stu-id="d5f3f-110">Represents the starting point for decoding an image file.</span></span> <span data-ttu-id="d5f3f-111">Bietet Zugriff auf Eigenschaften auf Container Ebene wie Miniaturansichten, Frames und Palette.</span><span class="sxs-lookup"><span data-stu-id="d5f3f-111">Provides access to container-level properties like thumbnails, frames, and palette.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5f3f-112"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a></span><span class="sxs-lookup"><span data-stu-id="d5f3f-112"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a></span></span></td>
<td><span data-ttu-id="d5f3f-113">Decoder</span><span class="sxs-lookup"><span data-stu-id="d5f3f-113">Decoders</span></span></td>
<td><span data-ttu-id="d5f3f-114">Stellt einen bestimmten Bild Rahmen innerhalb des Containers dar, der Zugriff auf Eigenschaften auf Frame-Ebene bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="d5f3f-114">Represents a specific image frame within the container that provides access to frame-level properties.</span></span> <span data-ttu-id="d5f3f-115">Dies ist die Schnittstelle, die die eigentlichen Bildbits decodiert.</span><span class="sxs-lookup"><span data-stu-id="d5f3f-115">This is the interface that decodes the actual image bits.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5f3f-116"><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a></span><span class="sxs-lookup"><span data-stu-id="d5f3f-116"><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a></span></span></td>
<td><span data-ttu-id="d5f3f-117">Decoder</span><span class="sxs-lookup"><span data-stu-id="d5f3f-117">Decoders</span></span></td>
<td><span data-ttu-id="d5f3f-118">Erforderlich für das Auflisten und durchlaufen von metadatenblöcken und das Aufrufen der entsprechenden metadatenleser beim Lesen aus einer Bilddatei.</span><span class="sxs-lookup"><span data-stu-id="d5f3f-118">Required for enumerating and iterating through metadata blocks and invoking the appropriate metadata readers when reading from an image file.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d5f3f-119">Wenn das RAW-Container-Format TIFF-kompatibel ist oder zum Speichern von EXIF-oder XMP-Metadaten Standard-ifds oder-Spalten verwendet, können die Codec-Autoren die integrierten metadatenleser aufrufen, anstatt Sie zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="d5f3f-119">If the RAW container format is TIFF compatible or uses standard IFDs or IRBs to store EXIF or XMP metadata, codec authors can choose to invoke the built-in metadata readers rather than writing their own.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5f3f-120"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform"><strong>IWICBitmapSourceTransform</strong></a></span><span class="sxs-lookup"><span data-stu-id="d5f3f-120"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform"><strong>IWICBitmapSourceTransform</strong></a></span></span></td>
<td><span data-ttu-id="d5f3f-121">Decoder</span><span class="sxs-lookup"><span data-stu-id="d5f3f-121">Decoders</span></span></td>
<td><span data-ttu-id="d5f3f-122">Ermöglicht dem Aufrufer, die gewünschte Skalierung, das Zuschneiden, das Drehen oder das Pixel Format für das decodierte Bild anzugeben, wodurch die decoderleistung erheblich verbessert werden kann.</span><span class="sxs-lookup"><span data-stu-id="d5f3f-122">Allows the caller to specify desired scaling, cropping, rotation, or pixel format for the decoded image, which can significantly improve decoder performance.</span></span> <span data-ttu-id="d5f3f-123">Beispielsweise wird von den Decodern von Microsoft JPEG und Wireless Datagram Protocol (WDP) ein Pyramiden Optimierungs Schema verwendet, um eine schnellere Decodierung zu erreichen, wenn die Zielbitmap kleiner als die Quell Bitmap ist.</span><span class="sxs-lookup"><span data-stu-id="d5f3f-123">For example, Microsoft's JPEG and Wireless Datagram Protocol (WDP) decoders use a pyramid optimization scheme to achieve faster decoding when the target bitmap is smaller than the source bitmap.</span></span> <span data-ttu-id="d5f3f-124">Windows Vista (und höher) versucht, diese Schnittstelle zu verwenden, um eine &quot; schnelle &quot; Vorschau von einem RAW-Image zu extrahieren, wenn die eingebettete Vorschau fehlt oder in der größten Dimension weniger als 1.024 Pixel.</span><span class="sxs-lookup"><span data-stu-id="d5f3f-124">Windows Vista (and later) will attempt to use this interface to extract a &quot;fast&quot; preview from a RAW image whenever the embedded preview is missing or less than 1,024 pixels in its largest dimension.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5f3f-125"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw"><strong>IWICDevelopRaw</strong></a></span><span class="sxs-lookup"><span data-stu-id="d5f3f-125"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw"><strong>IWICDevelopRaw</strong></a></span></span></td>
<td><span data-ttu-id="d5f3f-126">Decoder</span><span class="sxs-lookup"><span data-stu-id="d5f3f-126">Decoders</span></span></td>
<td><span data-ttu-id="d5f3f-127">Erforderlich für Rohdaten Formate.</span><span class="sxs-lookup"><span data-stu-id="d5f3f-127">Required for RAW formats.</span></span> <span data-ttu-id="d5f3f-128">Macht Parameter verfügbar, die für die Rohbild Verarbeitung spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="d5f3f-128">Exposes parameters that are specific to RAW image processing.</span></span> <span data-ttu-id="d5f3f-129">Unformatierte Codecs sollten so viele dieser Parameter unterstützen, wie Sie auf den Codec angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="d5f3f-129">RAW codecs should support as many of these parameters as apply to the codec.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5f3f-130"><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>Iwicbitmapcoder</strong></a></span><span class="sxs-lookup"><span data-stu-id="d5f3f-130"><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a></span></span></td>
<td><span data-ttu-id="d5f3f-131">Encoder</span><span class="sxs-lookup"><span data-stu-id="d5f3f-131">Encoders</span></span></td>
<td><span data-ttu-id="d5f3f-132">Stellt den Startpunkt für das Codieren einer Bilddatei dar.</span><span class="sxs-lookup"><span data-stu-id="d5f3f-132">Represents the starting point for encoding an image file.</span></span> <span data-ttu-id="d5f3f-133">Diese Schnittstelle wird verwendet, um Eigenschaften auf Container Ebene festzulegen, z. b. Miniaturansichten, Frames und Palette.</span><span class="sxs-lookup"><span data-stu-id="d5f3f-133">This interface is used for setting container-level properties, such as thumbnails, frames, and palette.</span></span> <span data-ttu-id="d5f3f-134">Außerdem müssen Sie einen metadatenwriter aufrufen, um die metadatenpersistenz in der Bilddatei zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d5f3f-134">It is also required to invoke a metadata writer to enable metadata persistence to the image file.</span></span> <span data-ttu-id="d5f3f-135">Aus diesen Gründen ist diese Schnittstelle notwendig, auch wenn die Codierung der primären Bitmap in das RAW-Format nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="d5f3f-135">For these reasons, this interface is necessary even if encoding the primary bitmap to the RAW format is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5f3f-136"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a></span><span class="sxs-lookup"><span data-stu-id="d5f3f-136"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a></span></span></td>
<td><span data-ttu-id="d5f3f-137">Encoder</span><span class="sxs-lookup"><span data-stu-id="d5f3f-137">Encoders</span></span></td>
<td><span data-ttu-id="d5f3f-138">Stellt einen bestimmten Bild Rahmen innerhalb des Containers dar.</span><span class="sxs-lookup"><span data-stu-id="d5f3f-138">Represents a specific image frame within the container.</span></span> <span data-ttu-id="d5f3f-139">Diese Schnittstelle wird verwendet, um die eigentlichen Bildbits zu codieren und um die einzelnen Frame-Metadaten und-Eigenschaften festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d5f3f-139">This interface is used to encode the actual image bits and to set per-frame metadata and properties.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5f3f-140"><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a></span><span class="sxs-lookup"><span data-stu-id="d5f3f-140"><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a></span></span></td>
<td><span data-ttu-id="d5f3f-141">Encoder</span><span class="sxs-lookup"><span data-stu-id="d5f3f-141">Encoders</span></span></td>
<td><span data-ttu-id="d5f3f-142">Erforderlich zum Durchlaufen von metadatenblöcken und zum Aufrufen der entsprechenden metadatenschreiber beim Serialisieren einer Bilddatei.</span><span class="sxs-lookup"><span data-stu-id="d5f3f-142">Required for iterating through metadata blocks and invoking the appropriate metadata writers when serializing an image file.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d5f3f-143">Wenn das RAW-Containerformat TIFF-kompatibel ist, können Codec-Autoren die integrierten metadatenwriter aufrufen, anstatt Sie selbst zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="d5f3f-143">If the RAW container format is TIFF-compatible, codec authors can choose to invoke the built-in metadata writers rather than writing their own.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="d5f3f-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d5f3f-144">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d5f3f-145">**Licher**</span><span class="sxs-lookup"><span data-stu-id="d5f3f-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d5f3f-146">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="d5f3f-146">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="d5f3f-147">WIC-Richtlinien für Kamera Rohbild Formate</span><span class="sxs-lookup"><span data-stu-id="d5f3f-147">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="d5f3f-148">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="d5f3f-148">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 




