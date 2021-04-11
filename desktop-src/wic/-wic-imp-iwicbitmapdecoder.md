---
description: Implementieren von IWICBitmapDecoder
ms.assetid: 9e316bdd-803a-47af-b004-7675478eb829
title: Implementieren von IWICBitmapDecoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b31bca377828606fe1beb68d6f1d95d290e01407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042331"
---
# <a name="implementing-iwicbitmapdecoder"></a>Implementieren von IWICBitmapDecoder

## <a name="iwicbitmapdecoder"></a>IWICBitmapDecoder

Wenn eine Anwendung einen Decoder anfordert, wird die [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) -Schnittstelle als erster Punkt der Interaktion mit dem Codec behandelt. Dabei handelt es sich um die Schnittstelle auf Container Ebene, die Zugriff auf die Eigenschaften der obersten Ebene des Containers und, am wichtigsten, die darin enthaltenen Frames bietet. Dies ist die primäre Schnittstelle in Ihrer Decoder-Klasse auf Container-Ebene.

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

Einige Bildformate verfügen über globale Miniaturansichten, Farb Kontexte oder Metadaten, während viele Bildformate diese nur pro Frame bereitstellen. Die Methoden für den Zugriff auf diese Elemente sind für [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)optional, jedoch für [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)erforderlich. Ebenso verwenden einige Codecs keine indizierten Pixel Formate und müssen daher nicht die [CopyPalette](-wic-imp-iwicbitmapframedecode.md) -Methoden für beide Schnittstellen implementieren. Weitere Informationen zu den optionalen **IWICBitmapDecoder** -Methoden finden Sie unter [Implementieren von IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md), wo Sie am häufigsten implementiert werden.

### <a name="querycapability"></a>QueryCapability

[**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) ist die Methode, die für die Codec-Vermittlung verwendet wird. (Informationen finden Sie unter Ermittlung [und Schiedsgerichtsbarkeit](-wic-howwicworks.md) im Thema [wie die Windows Imaging-Komponente funktioniert](-wic-howwicworks.md) .) Wenn zwei Codecs das gleiche Bildformat decodieren können, oder wenn ein Muster Konflikt auftritt, bei dem zwei Codecs dasselbe identifizierende Muster verwenden, können Sie mit dieser Methode den Codec auswählen, mit dem ein bestimmtes Bild am besten verarbeitet werden kann.

Wenn Sie diese Methode aufrufen, übergibt die Windows Imaging Component (WIC) den eigentlichen Stream, der das Bild enthält. Sie müssen überprüfen, ob Sie jeden Frame innerhalb des Bilds decodieren und die Metadatenblöcke durchlaufen können, um genau zu deklarieren, welche Funktionen dieser Decoder in Bezug auf den an ihn übergebenen spezifischen Dateistream hat. Dies ist für alle Decoder wichtig, jedoch besonders wichtig für Bildformate, die auf Tagged Image File Format (TIFF)-Containern basieren. Der Ermittlungs Vorgang funktioniert, indem den Decodern in der Registrierung zugeordneten Mustern Muster in der eigentlichen Bilddatei zugeordnet werden. Wenn Sie Ihr identifizierendes Muster in der Registrierung deklarieren, gewährleisten Sie, dass Ihr Decoder immer für Bilder in Ihrem Bildformat erkannt wird. Der Decoder kann jedoch weiterhin für Bilder in anderen Formaten erkannt werden. Beispielsweise enthalten alle TIFF-Container das TIFF-Muster, bei dem es sich um ein gültiges Identifikationsmuster für das TIFF-Bildformat handelt. Dies bedeutet, dass bei der Ermittlung mindestens zwei identifizierende Muster in Bilddateien für ein beliebiges Bildformat gefunden werden, das auf einem Container im TIFF-Format basiert. Eine ist das TIFF-Muster, und die andere ist das tatsächliche Bildformat Muster. Obwohl es weniger wahrscheinlich ist, gibt es auch Muster Konflikte zwischen anderen nicht verknüpften Bildformaten. Aus diesem Grund ist die Ermittlung und die Schiedsgerichtsbarkeit ein zweistufiger Prozess. Überprüfen Sie immer, ob der an [**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) übergebenen Bildstream tatsächlich eine gültige Instanz Ihres eigenen Bildformats ist. Wenn Ihr Codec ein Bildformat decodiert, für das Sie die Spezifikation nicht besitzen, sollte Ihre **QueryCapability** -Implementierung außerdem prüfen, ob eine Funktion vorhanden ist, die möglicherweise in der Bildformat Spezifikation gültig ist, die Ihr Codec nicht implementiert. Dadurch wird sichergestellt, dass Benutzer keine unnötigen Decodierungs Fehler haben oder unerwartete Ergebnisse mit Ihrem Codec erhalten.

Bevor Sie einen Vorgang für das Bild ausführen, müssen Sie die aktuelle Position des Streams speichern, damit Sie Sie an ihrer ursprünglichen Position wiederherstellen können, bevor Sie von der-Methode zurückgegeben werden. Die [**wicbitmapdecoderfunktionen**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) -Enumeration, die die Funktionen angibt, wird wie folgt definiert:

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

Sie sollten **WICBitmapDecoderCapabilitySameEncoder** nur deklarieren, wenn der Encoder der Codierer ist, der das Image codiert hat. Wenn Sie überprüft haben, ob Sie die einzelnen Frames im Container decodieren können, deklarieren Sie entweder **WICBitmapDecoderCapabilityCanDecodeSomeImages** , wenn Sie einige, aber nicht alle Frames decodieren können, **WICBitmapDecoderCapabilityCanDecodeAllImages** , wenn Sie alle Frames decodieren können, oder keines von beiden. (Diese zwei auffügeenden schließen sich gegenseitig aus. Wenn Sie **WICBitmapDecoderCapabilityCanDecodeAllImages** zurückgeben, wird **WICBitmapDecoderCapabilityCanDecodeSomeImages** ignoriert.) Deklarieren Sie **WICBitmapDecoderCapabilityCanEnumerateMetadata** , nachdem Sie sich vergewissert haben, dass Sie die Metadatenblöcke im Bild Container durchlaufen können. Sie müssen nicht in jedem Frame eine Miniaturansicht überprüfen. Wenn eine globale Miniaturansicht vorliegt und Sie Sie decodieren können, können Sie **wicbitmapdecodercapabilitycandecodeminiatur** deklarieren. Wenn keine globale Miniaturansicht vorhanden ist, versuchen Sie, die Miniaturansicht für Frame 0 zu decodieren. Wenn keine Miniaturansicht an einem dieser Orte vorhanden ist, deklarieren Sie diese Funktion nicht.

Nachdem Sie die Funktionen des Decoders in Bezug auf den an diese Methode übergebenen Bildstream festgelegt haben, führen Sie eine OR-Operation mit den [**wicbitmapdecoderfunktionen**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) aus, die Sie überprüft haben, die dieser Decoder für dieses Bild ausführen kann, und geben das Ergebnis zurück. Denken Sie daran, den Datenstrom vor der Rückgabe an seine ursprüngliche Position wiederherzustellen.

### <a name="initialize"></a>Initialisieren

[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize) wird von einer Anwendung aufgerufen, nachdem ein Decoder zum Decodieren eines bestimmten Bilds ausgewählt wurde. Der Bildstream wird an den Decoder übergeben, und ein Aufrufer kann optional die [**wicdecodeoptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) -Cache Option für den Umgang mit den Metadaten in der Datei angeben.

``` syntax
enum WICDecodeOptions
{
   WICDecodeMetadataCacheOnDemand,
   WICDecodeMetadataCacheOnLoad
}
```

Einige Anwendungen verwenden Metadaten mehr als andere. Die meisten Anwendungen müssen nicht auf alle Metadaten in einer Bilddatei zugreifen, und es werden bestimmte Metadaten angefordert, wenn Sie benötigt werden. Andere Anwendungen würden stattdessen alle Metadaten vorab zwischenspeichern, um den Datei Datenstrom zu öffnen und die Datenträger-e/a jedes Mal auszuführen, wenn Sie auf Metadaten zugreifen müssen. Wenn der Aufrufer keine Metadatencache-Option angibt, sollte das Standardverhalten beim Zwischenspeichern bei Bedarf Zwischenspeichern erfolgen. Dies bedeutet, dass keine Metadaten in den Arbeitsspeicher geladen werden sollen, bis die Anwendung eine bestimmte Anforderung für diese Metadaten sendet. Wenn die Anwendung **WICDecodeMetadataCacheOnLoad** angibt, sollten die Metadaten sofort in den Speicher geladen und zwischengespeichert werden. Wenn Metadaten beim Laden zwischengespeichert werden, kann der Datei Datenstrom freigegeben werden, nachdem die Metadaten zwischengespeichert wurden.

### <a name="getcontainerformat"></a>GetContainerFormat

Zum Implementieren von [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat)geben Sie einfach die GUID des Bildformats des Bilds zurück, für das der Decoder instanziiert wird. Diese Methode ist auch auf [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) und [**iwicbitmapcoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)implementiert.

### <a name="getdecoderinfo"></a>GetDecoderInfo

[**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) gibt ein [**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo) -Objekt zurück. Um das **IWICBitmapDecoderInfo** -Objekt zu erhalten, übergeben Sie einfach die GUID Ihres Decoders an die Methode " [**fiatecomponentinfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) " in [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), und fordern Sie dann die **IWICBitmapDecoderInfo** -Schnittstelle an, wie im folgenden Beispiel gezeigt.


```C++
IWICComponentInfo* pComponentInfo = NULL;
HRESULT hr;
 
hr = m_pImagingFactory->CreateComponentInfo(CLSID_This, &pComponentInfo);

hr = pComponentInfo->QueryInterface(IID_IWICBitmapDecoderInfo, (void**)ppIDecoderInfo);

```



### <a name="getframecount"></a>GetFrameCount

[**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) gibt nur die Anzahl der Frames im Container zurück. Einige Containerformate unterstützen mehrere Frames, und andere unterstützen nur einen Frame pro Container.

### <a name="getframe"></a>GetFrame

[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) ist eine wichtige Methode für die [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) -Schnittstelle, da der Frame die eigentlichen Bildbits enthält und das von dieser Methode zurückgegebene Frame-Decoderobjekt das Objekt ist, das die tatsächliche Decodierung des angeforderten Bilds durchführt. Dies ist das andere Objekt, das beim Schreiben eines Decoders implementiert werden muss. Weitere Informationen zu Frame-Decodern finden Sie unter [Implementieren von IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md).

### <a name="getpreview"></a>GetPreview

[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) gibt eine Vorschau des Images zurück. Eine ausführliche Erläuterung zu Vorschauen finden Sie unter [Implementieren der iwicbitmapcoder](-wic-imp-iwicbitmapencoder.md) -Methode auf der Schnittstelle [Implementieren der iwicbitmakcoder](-wic-imp-iwicbitmapencoder.md) -Schnittstelle.

Wenn Ihr Bildformat eine eingebettete JPEG-Vorschau enthält, wird dringend empfohlen, anstatt einen JPEG-Decoder zum Decodieren zu schreiben, delegieren Sie an den JPEG-Decoder, der mit der WIC-Plattform ausgeliefert wird, um Vorschauen und Miniaturansichten zu decodieren. Suchen Sie zu diesem Zweck den Anfang der Daten des Vorschau Bilds im Stream, und rufen Sie die Methode " [**foratedecoderfromstream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) " für [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)auf.


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

[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

**Licher**
</dt> <dt>

[Decoder-Schnittstellen](-wic-decoderinterfaces.md)
</dt> <dt>

[Implementieren von IWICBitmapCodecProgressNotification (Decoder)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



