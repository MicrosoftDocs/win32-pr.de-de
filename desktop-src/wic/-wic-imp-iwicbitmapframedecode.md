---
description: Implementieren von IWICBitmapFrameDecode
ms.assetid: 7dc626ad-1158-4b67-8ca7-47b4cf88e278
title: Implementieren von IWICBitmapFrameDecode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 394b5858ec5eee37ef1c7f52b766806c4a0c1a92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758304"
---
# <a name="implementing-iwicbitmapframedecode"></a><span data-ttu-id="1bf12-103">Implementieren von IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="1bf12-103">Implementing IWICBitmapFrameDecode</span></span>

## <a name="iwicbitmapframedecode"></a><span data-ttu-id="1bf12-104">IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="1bf12-104">IWICBitmapFrameDecode</span></span>

<span data-ttu-id="1bf12-105">[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) ist die Schnittstelle auf Frame-Ebene, die den Zugriff auf die eigentlichen Bildbits ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="1bf12-105">[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) is the frame-level interface that provides access to the actual image bits.</span></span> <span data-ttu-id="1bf12-106">Sie implementieren diese Schnittstelle in ihrer Decodierung-Klasse auf Frame-Ebene.</span><span class="sxs-lookup"><span data-stu-id="1bf12-106">You implement this interface on your frame-level decoding class.</span></span> <span data-ttu-id="1bf12-107">Da es von [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)abgeleitet ist, enthält Ihre Implementierung von **IWICBitmapFrameDecode** eine Implementierung der **IWICBitmapSource** -Methoden.</span><span class="sxs-lookup"><span data-stu-id="1bf12-107">Because it’s derived from [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource), your implementation of **IWICBitmapFrameDecode** will include an implementation of the **IWICBitmapSource** methods.</span></span> <span data-ttu-id="1bf12-108">Die zusätzlichen Methoden für **IWICBitmapFrameDecode** ermöglichen den Zugriff auf die Miniaturansicht auf Frame-Ebene, alle Farb Kontexte für das Bild und den metadatenabfragerleser für den Frame.</span><span class="sxs-lookup"><span data-stu-id="1bf12-108">The additional methods on **IWICBitmapFrameDecode** provide access to the frame-level thumbnail, any color contexts for the image, and the metadata query reader for the frame.</span></span>

``` syntax
interface IWICBitmapFrameDecode : IWICBitmapSource
{
// Required methods
HRESULT GetThumbnail ( IWICBitmapSource **ppIThumbnail );
HRESULT GetColorContexts ( UINT cCount, 
IWICColorContext **ppIColorContexts, UINT *pcActualCount );
HRESULT GetMetadataQueryReader ( IWICMetadataQueryReader **ppIMetadataQueryReader );

// Methods inherited from IWICBitmapSource
HRESULT GetSize ( UINT *puiWidth, UINT *puiHeight );
HRESULT GetPixelFormat ( WICPixelFormatGUID *pPixelFormat );
HRESULT GetResolution ( double *pDpiX, double *pDpiY );
HRESULT CopyPixels ( const WICRect *prc, 
   UINT cbStride,
   UINT cbBufferSize, 
   BYTE *pbBuffer );
// Optional method
HRESULT CopyPalette ( IWICPalette *pIPalette );
}
```

-   [<span data-ttu-id="1bf12-109">GetThumbnail</span><span class="sxs-lookup"><span data-stu-id="1bf12-109">GetThumbnail</span></span>](#getthumbnail)
-   [<span data-ttu-id="1bf12-110">Getcolorkontexte</span><span class="sxs-lookup"><span data-stu-id="1bf12-110">GetColorContexts</span></span>](#getcolorcontexts)
-   [<span data-ttu-id="1bf12-111">GetMetadataQueryReader</span><span class="sxs-lookup"><span data-stu-id="1bf12-111">GetMetadataQueryReader</span></span>](#getmetadataqueryreader)
-   [<span data-ttu-id="1bf12-112">GetSize, GetPixelFormat und GetResolution</span><span class="sxs-lookup"><span data-stu-id="1bf12-112">GetSize, GetPixelFormat, and GetResolution</span></span>](#getsize-getpixelformat-and-getresolution)
-   [<span data-ttu-id="1bf12-113">CopyPixels</span><span class="sxs-lookup"><span data-stu-id="1bf12-113">CopyPixels</span></span>](#copypixels)
-   [<span data-ttu-id="1bf12-114">CopyPalette</span><span class="sxs-lookup"><span data-stu-id="1bf12-114">CopyPalette</span></span>](#copypalette)

### <a name="getthumbnail"></a><span data-ttu-id="1bf12-115">GetThumbnail</span><span class="sxs-lookup"><span data-stu-id="1bf12-115">GetThumbnail</span></span>

<span data-ttu-id="1bf12-116">[**Getminiatur**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) gibt die Miniaturansicht für den aktuellen Frame zurück.</span><span class="sxs-lookup"><span data-stu-id="1bf12-116">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) returns the thumbnail for the current frame.</span></span> <span data-ttu-id="1bf12-117">Aus Leistungsgründen werden Miniaturansichten am häufigsten in einem JPEG-Format codiert.</span><span class="sxs-lookup"><span data-stu-id="1bf12-117">For performance reasons, thumbnails are most commonly encoded in a JPEG format.</span></span> <span data-ttu-id="1bf12-118">Ebenso wie bei der Vorschau des Decoders ist es nicht notwendig oder empfehlenswert, ihren eigenen JPEG-Decoder für Miniaturansichten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="1bf12-118">Just as with the Preview on the decoder, it is not necessary or recommended to provide your own JPEG decoder for thumbnails.</span></span> <span data-ttu-id="1bf12-119">Stattdessen sollten Sie an den von der Windows Imaging Component (WIC) bereitgestellten JPEG-Decoder delegieren.</span><span class="sxs-lookup"><span data-stu-id="1bf12-119">Instead, you should delegate to the JPEG decoder provided by Windows Imaging Component (WIC).</span></span>

<span data-ttu-id="1bf12-120">Weitere Informationen zu Miniaturansichten finden Sie unter der [setminiatur](-wic-imp-iwicbitmapframeencode.md) -Methode zum [Implementieren von iwicbitmapframecocode](-wic-imp-iwicbitmapframeencode.md).</span><span class="sxs-lookup"><span data-stu-id="1bf12-120">For more information on thumbnails, see the [SetThumbnail](-wic-imp-iwicbitmapframeencode.md) method on [Implementing IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md).</span></span>

### <a name="getcolorcontexts"></a><span data-ttu-id="1bf12-121">Getcolorkontexte</span><span class="sxs-lookup"><span data-stu-id="1bf12-121">GetColorContexts</span></span>

<span data-ttu-id="1bf12-122">[**Getcolorkontexte**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) gibt die gültigen Farb Kontexte (auch als Farbprofile bezeichnet) zurück, die mit dem Bild in diesem Frame verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="1bf12-122">[**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) returns the valid color contexts (also known as color profiles) associated with the image in this frame.</span></span> <span data-ttu-id="1bf12-123">In den meisten Fällen handelt es sich hierbei nur um einen, aber es gibt Fälle, in denen es zwei oder nur selten gibt.</span><span class="sxs-lookup"><span data-stu-id="1bf12-123">In most cases, this will only be one, but there could be cases where there are two or, rarely, more.</span></span> <span data-ttu-id="1bf12-124">Der Aufrufer übergibt mindestens ein [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) -Objekt, wobei der *ccount* -Parameter festgelegt wird, um anzugeben, wie viele Sie übergeben.</span><span class="sxs-lookup"><span data-stu-id="1bf12-124">The caller will pass in one or more [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) objects, setting the *cCount* parameter to indicate how many they are passing in.</span></span> <span data-ttu-id="1bf12-125">Diese Methode füllt die **IWICColorContext** -Objekte mit den tatsächlichen Farb Kontext Daten für die Farbprofile auf, die dem Bild zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1bf12-125">This method populates the **IWICColorContext** objects with the actual color context data for the color profiles associated with the image.</span></span> <span data-ttu-id="1bf12-126">Legen Sie den Parameter *pcActualCount* auf die tatsächliche Anzahl der Farb Kontexte fest, die dem Bild zugeordnet sind, auch wenn dieser Wert größer ist als die Zahl, die Sie zurückgeben können.</span><span class="sxs-lookup"><span data-stu-id="1bf12-126">Set the *pcActualCount* parameter to the actual number of color contexts associated with the image, even if this is greater than the number you can return.</span></span> <span data-ttu-id="1bf12-127">(Falls mehr Farb Kontexte verfügbar sind, als die Anzahl der **IWICColorContext** -Objekte, die vom Aufrufer übergeben werden, weist dies den Aufrufer an, dass mindestens ein anderer Benutzer verfügbar ist.)</span><span class="sxs-lookup"><span data-stu-id="1bf12-127">(In the case where more color contexts are available than the number of **IWICColorContext** objects passed in by the caller, this tells the caller there are one or more others available.)</span></span>

### <a name="getmetadataqueryreader"></a><span data-ttu-id="1bf12-128">GetMetadataQueryReader</span><span class="sxs-lookup"><span data-stu-id="1bf12-128">GetMetadataQueryReader</span></span>

<span data-ttu-id="1bf12-129">[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) gibt eine [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) zurück, die eine Anwendung verwenden kann, um Metadaten aus dem bildinframe abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1bf12-129">[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) returns an [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) that an application can use to retrieve metadata from the image frame.</span></span> <span data-ttu-id="1bf12-130">Diese Schnittstelle wird von einem Metadatenhandler implementiert und ermöglicht es einer Anwendung, bestimmte Metadateneigenschaften abzufragen, die zu einem bestimmten Metadatenformat gehören.</span><span class="sxs-lookup"><span data-stu-id="1bf12-130">This interface is implemented by a metadata handler, and allows an application to query for specific metadata properties belonging to a particular metadata format.</span></span> <span data-ttu-id="1bf12-131">Weitere Informationen finden Sie unter [Implementieren von IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md).</span><span class="sxs-lookup"><span data-stu-id="1bf12-131">For more information, see [Implementing IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md).</span></span>

<span data-ttu-id="1bf12-132">Um ein [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)zu instanziieren, müssen Sie für [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)den Befehl " [**kreatequeryreaderfromblockreader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createqueryreaderfromblockreader) " aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1bf12-132">To instantiate an [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader), call [**CreateQueryReaderFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createqueryreaderfromblockreader) on the [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory).</span></span>


```C++
IWICMetadataQueryReader* pQueryReader = NULL;
HRESULT hr;

hr = m_pComponentFactory->CreateQueryReaderFromBlockReader( 
  static_cast<IWICMetadataBlockWriter*>(this),
  &pQueryReader);
```



### <a name="getsize-getpixelformat-and-getresolution"></a><span data-ttu-id="1bf12-133">GetSize, GetPixelFormat und GetResolution</span><span class="sxs-lookup"><span data-stu-id="1bf12-133">GetSize, GetPixelFormat, and GetResolution</span></span>

<span data-ttu-id="1bf12-134">" [**GetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize)", " [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat)" und " [**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) " sind selbsterklärend und geben die angeforderten Eigenschaften des Bilds zurück.</span><span class="sxs-lookup"><span data-stu-id="1bf12-134">[**GetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize), [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat), and [**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) are self-explanatory, and return the requested properties of the image.</span></span>

### <a name="copypixels"></a><span data-ttu-id="1bf12-135">CopyPixels</span><span class="sxs-lookup"><span data-stu-id="1bf12-135">CopyPixels</span></span>

<span data-ttu-id="1bf12-136">[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) ist die Methode, die von einer Anwendung aufgerufen wird, wenn Sie eine Bitmap im Arbeitsspeicher erstellen möchte, die für die Anzeige oder den Drucker gerendert werden kann.</span><span class="sxs-lookup"><span data-stu-id="1bf12-136">[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) is the method an application calls when it wants to create a bitmap in memory that can be rendered to the display or printer.</span></span> <span data-ttu-id="1bf12-137">Dies ist die Methode, die die eigentliche Decodierung der Bildbits durchführt.</span><span class="sxs-lookup"><span data-stu-id="1bf12-137">This is the method that does the actual decoding of the image bits.</span></span> <span data-ttu-id="1bf12-138">Bei den Parametern handelt es sich um ein Rechteck, das den Bereich darstellt, der im Quell Image zum Kopieren in den Arbeitsspeicher relevant ist. der Stride-Wert, der die Anzahl der Bytes in einer Scan Zeile angibt. die Größe des Puffers im Arbeitsspeicher, der von der Anwendung zugewiesen wurde. und ein Zeiger auf den Puffer, in den die angeforderten Bildbits kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1bf12-138">The parameters are a rectangle, which represents the region of interest in the source image to copy into memory; the stride, which specifies the number of bytes in one scan line; the size of the buffer in memory that has been allocated by the application; and a pointer to the buffer into which the requested image bits should be copied.</span></span> <span data-ttu-id="1bf12-139">(Um zu verhindern, dass potenzielle Pufferüberläufe Sicherheitsrisiken einführen, sollten Sie sicherstellen, dass nur so viele Bilddaten in den Puffer kopiert werden, wie der *cbBufferSize* -Parameter angibt.)</span><span class="sxs-lookup"><span data-stu-id="1bf12-139">(To prevent potential buffer overruns from introducing security vulnerabilities, be sure to copy only as much image data into the buffer as the *cbBufferSize* parameter specifies.)</span></span>

### <a name="copypalette"></a><span data-ttu-id="1bf12-140">CopyPalette</span><span class="sxs-lookup"><span data-stu-id="1bf12-140">CopyPalette</span></span>

<span data-ttu-id="1bf12-141">Nur Codecs mit indizierten Pixel Formaten müssen die [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) -Methode implementieren.</span><span class="sxs-lookup"><span data-stu-id="1bf12-141">Only codecs that have indexed pixel formats must implement the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) method.</span></span> <span data-ttu-id="1bf12-142">Wenn ein Bild ein indiziertes Format verwendet, verwenden Sie diese Methode, um die Palette der Farben zurückzugeben, die im Bild verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1bf12-142">If an image uses an indexed format, use this method to return the palette of colors used in the image.</span></span> <span data-ttu-id="1bf12-143">Wenn Ihr Codec nicht über ein indiziertes Format verfügt, geben Sie wincodec \_ Err \_ palettenicht verfügbar zurück.</span><span class="sxs-lookup"><span data-stu-id="1bf12-143">If your codec doesn’t have an indexed format, return WINCODEC\_ERR\_PALETTEUNAVAILABLE.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1bf12-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1bf12-144">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1bf12-145">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="1bf12-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1bf12-146">**IWICBitmapSource**</span><span class="sxs-lookup"><span data-stu-id="1bf12-146">**IWICBitmapSource**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)
</dt> <dt>

[<span data-ttu-id="1bf12-147">**IWICBitmapDecoder**</span><span class="sxs-lookup"><span data-stu-id="1bf12-147">**IWICBitmapDecoder**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[<span data-ttu-id="1bf12-148">**IWICBitmapFrameDecode**</span><span class="sxs-lookup"><span data-stu-id="1bf12-148">**IWICBitmapFrameDecode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

<span data-ttu-id="1bf12-149">**Licher**</span><span class="sxs-lookup"><span data-stu-id="1bf12-149">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1bf12-150">Implementieren von IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="1bf12-150">Implementing IWICBitmapSource</span></span>](-wic-imp-iwicbitmapsource.md)
</dt> <dt>

[<span data-ttu-id="1bf12-151">Implementieren von IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="1bf12-151">Implementing IWICMetadataBlockReader</span></span>](-wic-imp-iwicmetadatablockreader.md)
</dt> <dt>

[<span data-ttu-id="1bf12-152">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="1bf12-152">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="1bf12-153">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="1bf12-153">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



