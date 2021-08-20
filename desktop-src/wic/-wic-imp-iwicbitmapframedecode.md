---
description: Implementieren von IWICBitmapFrameDecode
ms.assetid: 7dc626ad-1158-4b67-8ca7-47b4cf88e278
title: Implementieren von IWICBitmapFrameDecode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4b49e3636f5d81202b1060d868ecb40bb99d095dd9f26b6afd0d40c5f5fd0d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205764"
---
# <a name="implementing-iwicbitmapframedecode"></a>Implementieren von IWICBitmapFrameDecode

## <a name="iwicbitmapframedecode"></a>Iwicbitmapframedecode

[**IWICBitmapFrameDecode ist**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) die Schnittstelle auf Frameebene, die Zugriff auf die tatsächlichen Bildbits bietet. Sie implementieren diese Schnittstelle in Ihrer Decodierungsklasse auf Frameebene. Da sie von [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)abgeleitet ist, enthält Ihre Implementierung von **IWICBitmapFrameDecode** eine Implementierung der **IWICBitmapSource-Methoden.** Die zusätzlichen Methoden für **IWICBitmapFrameDecode** bieten Zugriff auf die Miniaturansicht auf Frameebene, alle Farbkontexte für das Bild und den Metadatenabfrageleser für den Frame.

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

-   [GetThumbnail](#getthumbnail)
-   [GetColorContexts](#getcolorcontexts)
-   [GetMetadataQueryReader](#getmetadataqueryreader)
-   [GetSize, GetPixelFormat und GetResolution](#getsize-getpixelformat-and-getresolution)
-   [Copypixels](#copypixels)
-   [CopyPalette](#copypalette)

### <a name="getthumbnail"></a>GetThumbnail

[**GetThumbnail gibt**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) die Miniaturansicht für den aktuellen Frame zurück. Aus Leistungsgründen werden Miniaturansichten am häufigsten in einem JPEG-Format codiert. Genau wie bei der Vorschau auf dem Decoder ist es nicht erforderlich oder empfohlen, einen eigenen JPEG-Decoder für Miniaturansichten zur Verfügung zu stellen. Stattdessen sollten Sie an den JPEG-Decoder delegieren, der von Windows Imaging Component (WIC) bereitgestellt wird.

Weitere Informationen zu Miniaturansichten finden Sie unter der [SetThumbnail-Methode](-wic-imp-iwicbitmapframeencode.md) unter [Implementing IWICBitmapFrameEncode (Implementieren von IWICBitmapFrameEncode).](-wic-imp-iwicbitmapframeencode.md)

### <a name="getcolorcontexts"></a>GetColorContexts

[**GetColorContexts gibt**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) die gültigen Farbkontexte (auch als Farbprofile bezeichnet) zurück, die dem Bild in diesem Frame zugeordnet sind. In den meisten Fällen ist dies nur eins, aber es kann Fälle geben, in denen es zwei oder selten mehr gibt. Der Aufrufer übergibt mindestens ein [**IWICColorContext-Objekt**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) und gibt mit dem *cCount-Parameter* an, wie viele übergeben werden. Diese Methode füllt die **IWICColorContext-Objekte** mit den tatsächlichen Farbkontextdaten für die farblichen Profile auf, die dem Bild zugeordnet sind. Legen Sie *den pcActualCount-Parameter* auf die tatsächliche Anzahl von Farbkontexten fest, die dem Bild zugeordnet sind, auch wenn dies größer als die Anzahl ist, die Sie zurückgeben können. (Wenn mehr Farbkontexte verfügbar sind als die Anzahl der VOM Aufrufer übergebenen **IWICColorContext-Objekte,** weist dies den Aufrufer an, dass mindestens ein anderer verfügbar ist.)

### <a name="getmetadataqueryreader"></a>GetMetadataQueryReader

[**GetMetadataQueryReader gibt**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) einen [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) zurück, mit dem eine Anwendung Metadaten aus dem Bildrahmen abrufen kann. Diese Schnittstelle wird von einem Metadatenhandler implementiert und ermöglicht einer Anwendung das Abfragen bestimmter Metadateneigenschaften, die zu einem bestimmten Metadatenformat gehören. Weitere Informationen finden Sie unter [Implementieren von IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md).

Um einen [**IWICMetadataQueryReader zu instanziieren,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)rufen [**Sie CreateQueryReaderFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createqueryreaderfromblockreader) für [**die IWICComponentFactory auf.**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)


```C++
IWICMetadataQueryReader* pQueryReader = NULL;
HRESULT hr;

hr = m_pComponentFactory->CreateQueryReaderFromBlockReader( 
  static_cast<IWICMetadataBlockWriter*>(this),
  &pQueryReader);
```



### <a name="getsize-getpixelformat-and-getresolution"></a>GetSize, GetPixelFormat und GetResolution

[**GetSize,**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize) [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat)und [**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) sind selbsterklärend und geben die angeforderten Eigenschaften des Bilds zurück.

### <a name="copypixels"></a>Copypixels

[**CopyPixels ist die**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) Methode, die eine Anwendung aufruft, wenn sie eine Bitmap im Arbeitsspeicher erstellen möchte, die auf der Anzeige oder dem Drucker gerendert werden kann. Dies ist die Methode, die die eigentliche Decodierung der Bildbits übernimmt. Die Parameter sind ein Rechteck, das den für das Quellbild zu kopierenden Bereich darstellt, der in den Arbeitsspeicher kopiert werden soll. der Stride, der die Anzahl der Bytes in einer Scanzeile angibt; die Größe des Puffers im Arbeitsspeicher, der von der Anwendung zugeordnet wurde; und ein Zeiger auf den Puffer, in den die angeforderten Bildbits kopiert werden sollen. (Um zu verhindern, dass potenzielle Pufferüberläufe Sicherheitsrisiken einführen, kopieren Sie nur so viele Bilddaten in den Puffer, wie der *cbBufferSize-Parameter* angibt.)

### <a name="copypalette"></a>CopyPalette

Nur Codecs mit indizierten Pixelformaten müssen die [**CopyPalette-Methode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) implementieren. Wenn ein Bild ein indiziertes Format verwendet, verwenden Sie diese Methode, um die Palette der im Bild verwendeten Farben zurück zu geben. Wenn Ihr Codec kein indiziertes Format hat, geben Sie WINCODEC \_ ERR \_ PALETTEUNAVAILABLE zurück.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[**Iwicbitmapsource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)
</dt> <dt>

[**Iwicbitmapdecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[**Iwicbitmapframedecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Implementieren von IWICBitmapSource](-wic-imp-iwicbitmapsource.md)
</dt> <dt>

[Implementieren von IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)
</dt> <dt>

[Schreiben eines WIC-Enabled CODEC](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Übersicht über Bildverarbeitungskomponenten](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



