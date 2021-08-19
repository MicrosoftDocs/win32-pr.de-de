---
description: Implementieren von IWICBitmapDecoder
ms.assetid: 9e316bdd-803a-47af-b004-7675478eb829
title: Implementieren von IWICBitmapDecoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0088b756a7a30134224e32fa67ee891f2c48339f9af70447cb760915ad420619
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118711147"
---
# <a name="implementing-iwicbitmapdecoder"></a>Implementieren von IWICBitmapDecoder

## <a name="iwicbitmapdecoder"></a>Iwicbitmapdecoder

Wenn eine Anwendung einen Decoder an fordert, besteht der erste Punkt der Interaktion mit dem Codec über die [**IWICBitmapDecoder-Schnittstelle.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) Dies ist die Schnittstelle auf Containerebene, die Zugriff auf die Eigenschaften der obersten Ebene des Containers und vor allem auf die frames bietet, die er enthält. Dies ist die primäre Schnittstelle ihrer Decoderklasse auf Containerebene.

``` syntax
interface IWICBitmapDecoder : IUnknown
{
// Required methods
   HRESULT QueryCapability (IStream *pIStream, 
      DWORD *pdwCapabilities );
   HRESULT Initialize ( IStream *pIStream,
      WICDecodeOptions cacheOptions );
   HRESULT GetContainerFormat ( GUID *pguidContainerFormat );
   HRESULT GetDecoderInfo ( IWICBitmapDecoderInfo **pIDecoderInfo );
   HRESULT GetFrameCount ( UINT *pCount );
   HRESULT GetFrame ( UINT index, 
      IWICBitmapFrameDecode **ppIBitmapFrame );

// Optional methods
   HRESULT GetPreview ( IWICBitmapSource **ppIPreview );
   HRESULT GetThumbnail ( IWICBitmapSource **ppIThumbnail );
   HRESULT GetColorContexts ( UINT cCount, 
      IWICColorContext **ppIColorContexts, 
      UINT *pcActualCount );
   HRESULT GetMetadataQueryReader ( IWICMetadataQueryReader **ppIMetadataQueryReader);
   HRESULT CopyPalette ( IWICPalette *pIPalette );
}
```

Einige Bildformate verfügen über globale Miniaturansichten, Farbkontexte oder Metadaten, während viele Bildformate diese nur pro Frame bereitstellen. Die Methoden für den Zugriff auf diese Elemente sind für [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)optional, sind jedoch für [**IWICBitmapFrameDecode erforderlich.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) Ebenso verwenden einige Codecs keine indizierten Pixelformate und müssen daher die [CopyPalette-Methoden](-wic-imp-iwicbitmapframedecode.md) nicht auf beiden Schnittstellen implementieren. Weitere Informationen zu den optionalen **IWICBitmapDecoder-Methoden** finden Sie unter [Implementing IWICBitmapFrameDecode (Implementieren von IWICBitmapFrameDecode),](-wic-imp-iwicbitmapframedecode.md)wo sie am häufigsten implementiert werden.

### <a name="querycapability"></a>QueryCapability

[**QueryCapability ist**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) die Methode, die für die Codec-Vermittlung verwendet wird. (Siehe [Ermittlung und Vermittlung](-wic-howwicworks.md) im Thema Funktionsweise der Windows [Imaging-Komponente).](-wic-howwicworks.md) Wenn zwei Codecs das gleiche Bildformat decodieren können, oder wenn ein Musterkollision auftritt, bei dem zwei Codecs das gleiche Identifizierungsmuster verwenden, können Sie mit dieser Methode den Codec auswählen, der jedes bestimmte Bild am besten verarbeiten kann.

Beim Aufrufen dieser Methode übergibt Windows Imaging Component (WIC) den eigentlichen Stream, der das Bild enthält. Sie müssen überprüfen, ob Sie jeden Frame innerhalb des Bilds decodieren und die Metadatenblöcke aufzählen können, um genau zu deklarieren, welche Funktionen dieser Decoder in Bezug auf den spezifischen Dateistream hat, der an ihn übergeben wird. Dies ist wichtig für alle Decoder, aber besonders wichtig für Bildformate, die auf Tagged Image File Format (TIFF)-Containern basieren. Der Ermittlungsprozess funktioniert, indem Muster, die Decodern in der Registrierung zugeordnet sind, mit Mustern in der eigentlichen Imagedatei übereinstimmen. Durch das Deklarieren des Identifizierungsmusters in der Registrierung wird sichergestellt, dass Ihr Decoder immer für Images im Imageformat erkannt wird. Ihr Decoder kann jedoch weiterhin für Bilder in anderen Formaten erkannt werden. Beispielsweise enthalten alle TIFF-Container das TIFF-Muster, ein gültiges Identifizierungsmuster für das TIFF-Bildformat. Dies bedeutet, dass während der Ermittlung mindestens zwei identifizierende Muster in Bilddateien für jedes Bildformat gefunden werden, das auf einem Container im TIFF-Stil basiert. Eine ist das TIFF-Muster, die andere das tatsächliche Bildformatmuster. Obwohl die Wahrscheinlichkeit geringer ist, kann es auch zu Musterkollisionen zwischen anderen nicht verknüpften Bildformaten geben. Aus diesem Grund sind Ermittlung und Vermittlung ein zweistufiger Prozess. Stellen Sie immer sicher, dass der an [**QueryCapability übergebene**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) Bilddatenstrom tatsächlich eine gültige Instanz Ihres eigenen Bildformats ist. Wenn Ihr Codec außerdem ein Bildformat decodiert, für das Sie die Spezifikation nicht besitzen, sollte Ihre **QueryCapability-Implementierung** überprüfen, ob ein Feature vor ort ist, das möglicherweise gemäß der Spezifikation des Bildformats gültig ist, die Ihr Codec nicht implementiert. Dadurch wird sichergestellt, dass benutzer keine unnötigen Decodierungsfehler auftreten oder unerwartete Ergebnisse mit Ihrem Codec erhalten.

Bevor Sie einen Vorgang für das Image ausführen, müssen Sie die aktuelle Position des Streams speichern, damit Sie ihn an seiner ursprünglichen Position wiederherstellen können, bevor Sie von der -Methode zurückkehren. Die [**WICBitmapDecoderCapabilities-Enumeration,**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) die die Funktionen angibt, wird wie folgt definiert:

``` syntax
enum WICBitmapDecoderCapabilities
{   
   WICBitmapDecoderCapabilitySameEncoder,
   WICBitmapDecoderCapabilityCanDecodeAllImages,
   WICBitmapDecoderCapabilityCanDecodeSomeImages,
   WICBitmapDecoderCapabilityCanEnumerateMetadata,
   WICBitmapDecoderCapabilityCanDecodeThumbnail
}
```

Sie sollten **WICBitmapDecoderCapabilitySameEncoder** nur deklarieren, wenn Der Encoder das Bild codiert hat. Nachdem Sie überprüft haben, ob Sie jeden Frame im Container decodieren können, deklarieren Sie **entweder WICBitmapDecoderCapabilityCanDecodeSomeImages,** wenn Sie einige, aber nicht alle Frames decodieren können, **WICBitmapDecoderCapabilityCanDecodeAllImages,** wenn Sie alle Frames decodieren können, oder keines von beiden, wenn Sie keines von ihnen decodieren können. (Diese beiden Enumerierungen schließen sich gegenseitig aus. Wenn Sie **WICBitmapDecoderCapabilityCanDecodeAllImages** zurückgeben, **wird WICBitmapDecoderCapabilityCanDecodeSomeImages** ignoriert.) **Deklarieren Sie WICBitmapDecoderCapabilityCanEnumerateMetadata,** nachdem Sie überprüft haben, ob Sie die Metadatenblöcke im Imagecontainer aufzählen können. Sie müssen nicht in jedem Frame nach einer Miniaturansicht überprüfen. Wenn es eine globale Miniaturansicht gibt und Sie sie decodieren können, können Sie **WICBitmapDecoderCapabilityCanDecodeThumbnail deklarieren.** Wenn keine globale Miniaturansicht angezeigt wird, versuchen Sie, die Miniaturansicht für Frame 0 zu decodieren. Wenn an einer dieser Stellen keine Miniaturansichten angezeigt werden, deklarieren Sie diese Funktion nicht.

Nachdem Sie die Funktionen des Decoders in Bezug auf den an diese Methode übergebenen Bildstream bestimmt haben, führen Sie einen OR-Vorgang mit [**den WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) aus, die Sie überprüft haben, ob dieser Decoder für dieses Bild ausführen kann, und geben Sie das Ergebnis zurück. Denken Sie daran, den Stream an seiner ursprünglichen Position wiederherzustellen, bevor Sie ihn zurückgeben.

### <a name="initialize"></a>Initialisieren

[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize) wird von einer Anwendung aufgerufen, nachdem ein Decoder ausgewählt wurde, um ein bestimmtes Bild zu decodieren. Der Bildstream wird an den Decoder übergeben, und ein Aufrufer kann optional die [**Cacheoption WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) für den Umgang mit den Metadaten in der Datei angeben.

``` syntax
enum WICDecodeOptions
{
   WICDecodeMetadataCacheOnDemand,
   WICDecodeMetadataCacheOnLoad
}
```

Einige Anwendungen verwenden Metadaten mehr als andere. Die meisten Anwendungen müssen nicht auf alle Metadaten in einer Bilddatei zugreifen und fordern bei Bedarf bestimmte Metadaten an. Andere Anwendungen würden stattdessen alle Metadaten im Vorhinhin zwischenspeichern, anstatt den Dateidatenstrom geöffnet zu lassen und jedes Mal, wenn sie auf Metadaten zugreifen müssen, Datenträger-E/A durchzuführen. Wenn der Aufrufer keine Metadatencacheoption an gibt, sollte das Standardverhalten für das Zwischenspeichern bei Bedarf zwischengespeichert werden. Dies bedeutet, dass keine Metadaten in den Arbeitsspeicher geladen werden sollten, bis die Anwendung eine bestimmte Anforderung für diese Metadaten stellt. Wenn die Anwendung **WICDecodeMetadataCacheOnLoad** angibt, sollten die Metadaten sofort in den Arbeitsspeicher geladen und zwischengespeichert werden. Wenn Metadaten beim Laden zwischengespeichert werden, kann der Dateistream freigegeben werden, nachdem die Metadaten zwischengespeichert wurden.

### <a name="getcontainerformat"></a>GetContainerFormat

Um [**GetContainerFormat zu implementieren,**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat)geben Sie einfach die GUID des Bildformats des Bilds zurück, für das der Decoder instanziiert wird. Diese Methode wird auch in [**IWICMetadataBlockReader und**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) [**IWICBitmapEncoder implementiert.**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)

### <a name="getdecoderinfo"></a>GetDecoderInfo

[**GetDecoderInfo gibt**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) ein [**IWICBitmapDecoderInfo-Objekt**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo) zurück. Um das **IWICBitmapDecoderInfo-Objekt** zu erhalten, übergeben Sie einfach die GUID Ihres Decoders an die [**CreateComponentInfo-Methode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) in [**IWICImagingFactory,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)und fordern Sie dann die **IWICBitmapDecoderInfo-Schnittstelle** dafür an, wie im folgenden Beispiel gezeigt.


```C++
IWICComponentInfo* pComponentInfo = NULL;
HRESULT hr;
 
hr = m_pImagingFactory->CreateComponentInfo(CLSID_This, &pComponentInfo);

hr = pComponentInfo->QueryInterface(IID_IWICBitmapDecoderInfo, (void**)ppIDecoderInfo);

```



### <a name="getframecount"></a>GetFrameCount

[**GetFrameCount gibt**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) nur die Anzahl der Frames im Container zurück. Einige Containerformate unterstützen mehrere Frames, während andere nur einen Frame pro Container unterstützen.

### <a name="getframe"></a>Getframe

[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) ist eine wichtige Methode für die [**IWICBitmapDecoder-Schnittstelle,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) da der Frame die tatsächlichen Bildbits enthält und das von dieser Methode zurückgegebene Framedecoderobjekt das Objekt ist, das die eigentliche Decodierung des angeforderten Bilds übernimmt. Dies ist das andere Objekt, das Sie beim Schreiben eines Decoders implementieren müssen. Weitere Informationen zu Framedecodern finden Sie unter [Implementing IWICBitmapFrameDecode (Implementieren von IWICBitmapFrameDecode).](-wic-imp-iwicbitmapframedecode.md)

### <a name="getpreview"></a>GetPreview

[**GetPreview gibt**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) eine Vorschau des Bilds zurück. Eine ausführliche Erläuterung der Vorschauversionen finden Sie unter [Implementing IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md) method on the Implementing IWICBitmapEncoder interface (Implementieren der [IWICBitmapEncoder-Methode).](-wic-imp-iwicbitmapencoder.md)

Wenn Ihr Bildformat eine eingebettete JPEG-Vorschau enthält, wird dringend empfohlen, anstelle eines JPEG-Decoders zum Decodieren an den JPEG-Decoder zu delegieren, der mit der WIC-Plattform zum Decodieren von Vorschauen und Miniaturansichten enthalten ist. Suchen Sie dazu bis zum Anfang der Vorschaubilddaten im Stream, und rufen Sie die [**CreateDecoderFromStream-Methode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) für [**die IWICImagingFactory auf.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)


```C++
IWICBitmapDecoder* pPreviewDecoder = NULL;
IWICBitmapFrameDecode* pPreviewFrame = NULL;
IWICBitmapSource* pPreview = NULL;
HRESULT hr;

hr = m_pImagingFactory->CreateDecoderFromStream(
                               m_pStream, NULL, 
                               WICDecodeMetadataCacheOnDemand, &pPreviewDecoder);
hr = pPreviewDecoder->GetFrame(0, pPreviewFrame);
hr = pPreviewFrame->QueryInterface(IID_IWICBitmapSource, (void**)&pPreview);

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[**Iwicbitmapdecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[**Iwicbitmapframedecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Decoderschnittstellen](-wic-decoderinterfaces.md)
</dt> <dt>

[Implementieren von IWICBitmapCodecProgressNotification (Decoder)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> <dt>

[Schreiben eines WIC-Enabled CODEC](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Übersicht über Bildverarbeitungskomponenten](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



