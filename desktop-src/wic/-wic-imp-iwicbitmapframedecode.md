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
# <a name="implementing-iwicbitmapframedecode"></a>Implementieren von IWICBitmapFrameDecode

## <a name="iwicbitmapframedecode"></a>IWICBitmapFrameDecode

[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) ist die Schnittstelle auf Frame-Ebene, die den Zugriff auf die eigentlichen Bildbits ermöglicht. Sie implementieren diese Schnittstelle in ihrer Decodierung-Klasse auf Frame-Ebene. Da es von [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)abgeleitet ist, enthält Ihre Implementierung von **IWICBitmapFrameDecode** eine Implementierung der **IWICBitmapSource** -Methoden. Die zusätzlichen Methoden für **IWICBitmapFrameDecode** ermöglichen den Zugriff auf die Miniaturansicht auf Frame-Ebene, alle Farb Kontexte für das Bild und den metadatenabfragerleser für den Frame.

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
-   [Getcolorkontexte](#getcolorcontexts)
-   [GetMetadataQueryReader](#getmetadataqueryreader)
-   [GetSize, GetPixelFormat und GetResolution](#getsize-getpixelformat-and-getresolution)
-   [CopyPixels](#copypixels)
-   [CopyPalette](#copypalette)

### <a name="getthumbnail"></a>GetThumbnail

[**Getminiatur**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) gibt die Miniaturansicht für den aktuellen Frame zurück. Aus Leistungsgründen werden Miniaturansichten am häufigsten in einem JPEG-Format codiert. Ebenso wie bei der Vorschau des Decoders ist es nicht notwendig oder empfehlenswert, ihren eigenen JPEG-Decoder für Miniaturansichten bereitzustellen. Stattdessen sollten Sie an den von der Windows Imaging Component (WIC) bereitgestellten JPEG-Decoder delegieren.

Weitere Informationen zu Miniaturansichten finden Sie unter der [setminiatur](-wic-imp-iwicbitmapframeencode.md) -Methode zum [Implementieren von iwicbitmapframecocode](-wic-imp-iwicbitmapframeencode.md).

### <a name="getcolorcontexts"></a>Getcolorkontexte

[**Getcolorkontexte**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) gibt die gültigen Farb Kontexte (auch als Farbprofile bezeichnet) zurück, die mit dem Bild in diesem Frame verknüpft sind. In den meisten Fällen handelt es sich hierbei nur um einen, aber es gibt Fälle, in denen es zwei oder nur selten gibt. Der Aufrufer übergibt mindestens ein [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) -Objekt, wobei der *ccount* -Parameter festgelegt wird, um anzugeben, wie viele Sie übergeben. Diese Methode füllt die **IWICColorContext** -Objekte mit den tatsächlichen Farb Kontext Daten für die Farbprofile auf, die dem Bild zugeordnet sind. Legen Sie den Parameter *pcActualCount* auf die tatsächliche Anzahl der Farb Kontexte fest, die dem Bild zugeordnet sind, auch wenn dieser Wert größer ist als die Zahl, die Sie zurückgeben können. (Falls mehr Farb Kontexte verfügbar sind, als die Anzahl der **IWICColorContext** -Objekte, die vom Aufrufer übergeben werden, weist dies den Aufrufer an, dass mindestens ein anderer Benutzer verfügbar ist.)

### <a name="getmetadataqueryreader"></a>GetMetadataQueryReader

[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) gibt eine [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) zurück, die eine Anwendung verwenden kann, um Metadaten aus dem bildinframe abzurufen. Diese Schnittstelle wird von einem Metadatenhandler implementiert und ermöglicht es einer Anwendung, bestimmte Metadateneigenschaften abzufragen, die zu einem bestimmten Metadatenformat gehören. Weitere Informationen finden Sie unter [Implementieren von IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md).

Um ein [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)zu instanziieren, müssen Sie für [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)den Befehl " [**kreatequeryreaderfromblockreader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createqueryreaderfromblockreader) " aufrufen.


```C++
IWICMetadataQueryReader* pQueryReader = NULL;
HRESULT hr;

hr = m_pComponentFactory->CreateQueryReaderFromBlockReader( 
  static_cast<IWICMetadataBlockWriter*>(this),
  &pQueryReader);
```



### <a name="getsize-getpixelformat-and-getresolution"></a>GetSize, GetPixelFormat und GetResolution

" [**GetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize)", " [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat)" und " [**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) " sind selbsterklärend und geben die angeforderten Eigenschaften des Bilds zurück.

### <a name="copypixels"></a>CopyPixels

[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) ist die Methode, die von einer Anwendung aufgerufen wird, wenn Sie eine Bitmap im Arbeitsspeicher erstellen möchte, die für die Anzeige oder den Drucker gerendert werden kann. Dies ist die Methode, die die eigentliche Decodierung der Bildbits durchführt. Bei den Parametern handelt es sich um ein Rechteck, das den Bereich darstellt, der im Quell Image zum Kopieren in den Arbeitsspeicher relevant ist. der Stride-Wert, der die Anzahl der Bytes in einer Scan Zeile angibt. die Größe des Puffers im Arbeitsspeicher, der von der Anwendung zugewiesen wurde. und ein Zeiger auf den Puffer, in den die angeforderten Bildbits kopiert werden sollen. (Um zu verhindern, dass potenzielle Pufferüberläufe Sicherheitsrisiken einführen, sollten Sie sicherstellen, dass nur so viele Bilddaten in den Puffer kopiert werden, wie der *cbBufferSize* -Parameter angibt.)

### <a name="copypalette"></a>CopyPalette

Nur Codecs mit indizierten Pixel Formaten müssen die [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) -Methode implementieren. Wenn ein Bild ein indiziertes Format verwendet, verwenden Sie diese Methode, um die Palette der Farben zurückzugeben, die im Bild verwendet werden. Wenn Ihr Codec nicht über ein indiziertes Format verfügt, geben Sie wincodec \_ Err \_ palettenicht verfügbar zurück.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)
</dt> <dt>

[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

**Licher**
</dt> <dt>

[Implementieren von IWICBitmapSource](-wic-imp-iwicbitmapsource.md)
</dt> <dt>

[Implementieren von IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



