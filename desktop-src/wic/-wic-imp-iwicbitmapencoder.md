---
description: Implementieren von iwicbitmapcoder
ms.assetid: b671e941-ded6-4bde-bc4d-461f13feade0
title: Implementieren von iwicbitmapcoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 590dffcf762d22155a89a8143994d9a4d8bcab02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867335"
---
# <a name="implementing-iwicbitmapencoder"></a>Implementieren von iwicbitmapcoder

-   [Iwicbitmapcoder](#implementing-iwicbitmapencoder)
    -   [Initialisieren](#initialize)
    -   [GetContainerFormat](#getcontainerformat)
    -   [GetEncoderInfo](#getencoderinfo)
    -   ["Kreatenewframe"](#createnewframe)
    -   [Commit](#commit)
    -   [SetPreview](#setpreview)
-   [Zugehörige Themen](#related-topics)

## <a name="iwicbitmapencoder"></a>Iwicbitmapcoder

-   [Initialisieren](#initialize)
-   [GetContainerFormat](#getcontainerformat)
-   [GetEncoderInfo](#getencoderinfo)
-   ["Kreatenewframe"](#createnewframe)
-   [Commit](#commit)
-   [SetPreview](#setpreview)

Diese Schnittstelle ist die Entsprechung der [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) -Schnittstelle und stellt den Ausgangspunkt für das Codieren einer Bilddatei dar. Ebenso wie **IWICBitmapDecoder** zum Abrufen von Eigenschaften auf Container Ebene und einzelnen Frames aus dem Bild Container verwendet wird, wird [**iwicbitmapcoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) zum Festlegen von Eigenschaften auf Container Ebene und zum Serialisieren einzelner Bild Rahmen in den Container verwendet. Sie implementieren diese Schnittstelle in ihrer Encoder-Klasse auf Container Ebene.

``` syntax
interface IWICBitmapEncoder : public IUnknown
{
   // Required methods
   HRESULT Initialize ( IStream *pIStream,
              WICBitmapEncoderCacheOption cacheOption );
   HRESULT GetContainerFormat ( GUID *pguidContainerFormat );
   HRESULT GetEncoderInfo ( IWICBitmapEncoderInfo **pIEncoderInfo );
   HRESULT CreateNewFrame ( IWICBitmapFrameEncode **ppIFrameEncode,
              IPropertyBag2 **ppIEncoderOptions );
   HRESULT Commit ( void );

   // Optional methods
   HRESULT SetPreview ( IWICBitmapSource *pIPreview );
   HRESULT SetThumbnail ( IWICBitmapSource *pIThumbnail );
   HRESULT SetColorContexts ( UINT cCount,
              IWICColorContext **ppIColorContext );
   HRESULT GetMetadataQueryWriter ( IWICMetadataQueryWriter 
              **ppIMetadataQueryWriter );
   HRESULT SetPalette ( IWICPalette *pIPalette);
};
```

Wie unter [Implementieren von IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)erläutert, haben einige Bildformate globale Miniaturansichten, Farb Kontexte oder Metadaten, während viele Bildformate diese nur pro Frame bereitstellen. Daher sind die Methoden zum Festlegen dieser [**Parameter für iwicbitmapcoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)optional, jedoch für [**iwicbitmapframecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)erforderlich. Wir besprechen die Methoden, die für **iwicbitmapcoder** im Abschnitt zu **iwicbitmapframecoder** optional sind, wo Sie am häufigsten implementiert werden.

Wenn Sie keine globalen Miniaturansichten unterstützen, geben Sie wincodec \_ Err \_ codecnominiatur aus der setminiatur-Methode für [**iwicbitmapcoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)zurück. Wenn Sie keine Palette auf Container Ebene unterstützen oder wenn das Abbild, das Sie codieren, kein indiziertes Format hat, geben Sie wincodec \_ Err \_ palettenicht aus der SetPalette-Methode zurück. Bei allen anderen nicht unterstützten Methoden wird wincodec \_ Err \_ unsupportedoperation zurückgegeben.

### <a name="initialize"></a>Initialisieren

[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize) ist die erste Methode, die für einen [**iwicbitmapocoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) aufgerufen wird, nachdem er instanziiert wurde. Ein Bildstream wird an den Encoder übergeben, und ein Aufrufer kann optional eine Cache-Option angeben. Im Fall des Decoders ist der Stream schreibgeschützt, aber der an einen Encoder übergebenen Stream ist ein Beschreib barer Stream, in den der Encoder alle Bilddaten und Metadaten serialisiert. Die Cache Optionen für den Encoder unterscheiden sich ebenfalls.

``` syntax
enum WICBitmapEncoderCacheOption
{
   WICBitmapEncoderCacheInMemory,
   WICBitmapEncoderCacheTempFile,
   WICBitmapEncoderNoCache
}
```

Die Anwendung hat die Wahl, den Encoder zum Zwischenspeichern der Bilddaten im Arbeitsspeicher anzufordern, Sie in einer temporären Datei zwischenzuspeichern oder Sie ohne Zwischenspeichern direkt in die Datenträger Datei zu schreiben. Wenn Sie aufgefordert werden, die Daten in einer temporären Datei zwischenzuspeichern, sollte der Encoder eine temporäre Datei auf dem Datenträger erstellen und direkt in diese Datei schreiben, ohne im Arbeitsspeicher zwischenspeichern. Wenn der Aufrufer die Option Kein Cache auswählt, muss für jeden Frame ein Commit ausgeführt werden, bevor der nächste Frame erstellt werden kann.

### <a name="getcontainerformat"></a>GetContainerFormat

[**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getcontainerformat) wird auf die gleiche Weise implementiert wie die Methode [GetContainerFormat](-wic-imp-iwicbitmapdecoder.md) bei der [Implementierung von IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md).

### <a name="getencoderinfo"></a>GetEncoderInfo

[**GetEncoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo) gibt ein [**iwicbitmapcoderinfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo) -Objekt zurück. Um das **iwicbitmapcoderinfo** -Objekt zu erhalten, übergeben Sie einfach die GUID des Encoders an die Methode " [**fiatecomponentinfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) " in [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), und fordern Sie dann die **iwicbitmapcoderinfo** -Schnittstelle an.

Weitere Informationen finden Sie im Beispiel unter [Implementieren von IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md) unter [GetDecoderInfo](-wic-imp-iwicbitmapdecoder.md).

### <a name="createnewframe"></a>"Kreatenewframe"

" [**Kreatenewframe**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) " ist das Codierungs Pendant von " [**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) " auf " [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)". Diese Methode gibt ein [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) -Objekt zurück, das das Objekt ist, das die Bilddaten für einen bestimmten Frame innerhalb des Containers tatsächlich serialisiert.

Einer der Vorteile der Windows Imaging Component (WIC) besteht darin, dass er eine Abstraktions Ebene für Anwendungen bereitstellt, die es Ihnen ermöglicht, auf die gleiche Weise mit allen Bildformaten zu arbeiten. Allerdings sind nicht alle Bildformate identisch. Einige Bildformate verfügen über Funktionen, die andere nicht haben. Damit Anwendungen diese einzigartigen Funktionen nutzen können, ist es erforderlich, dass der Codec eine Methode bereitstellt, um diese Features verfügbar zu machen. Dies ist der Zweck der Encoder-Optionen. Wenn Ihr Codec Codierungsoptionen unterstützt, sollten Sie ein [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) -Objekt erstellen, das die von Ihnen unterstützten Codierungsoptionen verfügbar macht und im *ppencoderoptions* -Parameter dieser Methode zurückgibt. Der Aufrufer kann dann dieses IPropertyBag2-Objekt verwenden, um zu bestimmen, welche Codierungsoptionen Ihr Codec unterstützt Wenn der Aufrufer Werte für eine der unterstützten Encoder-Optionen angeben möchte, weist er den Wert der relevanten Eigenschaft im IPropertyBag2-Objekt zu und übergibt ihn an das neu erstellte [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) -Objekt in seiner Initialize-Methode.

Um ein [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) -Objekt zu instanziieren, müssen Sie zuerst eine PROPBAG2-Struktur erstellen, um jede vom Encoder unterstützte Encoder-Option und ihren Datentyp für jede Eigenschaft anzugeben. Anschließend müssen Sie ein IPropertyBag2-Objekt implementieren, das die Wertebereiche für jede Eigenschaft beim Schreiben erzwingt und alle in Konflikt stehenden oder überlappenden Werte abgleicht. Für einfache Sätze von nicht in Konflikt stehenden Encoderoptionen können Sie die Methode " [**kreateencoderpropertybag**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createencoderpropertybag) " aufrufen, die ein einfaches IPropertyBag2-Objekt mithilfe der Eigenschaften erstellt, die Sie in der PROPBAG2-Struktur angeben. Sie müssen weiterhin die Wertebereiche erzwingen. Für erweiterte Codierungsoptionen oder wenn Sie widersprüchliche Werte abstimmen müssen, müssen Sie eine eigene IPropertyBag2-Implementierung schreiben.


```C++
UINT cuiPropertyCount = 0;
IPropertyBag2* pPropertyBag = NULL;
PROPBAG2* pPropBagOptions;
HRESULT hr;

// Insert code here to initialize piPropertyBag with the 
// supported options for your encoder, and to initialize 
// cuiPropertyCount to the number of encoder option properties
// you are exposing.
...

hr = pComponentFactory->CreateEncoderPropertyBag( 
   pPropBagOptions, cuiPropertyCount, &pPropertyBag);
```



WIC bietet einen kleinen Satz kanonischer Codierungsoptionen, die von einigen gängigen Bildformaten verwendet werden. Alle kanonischen Codieroptionen sind optional, und Codecs müssen diese nicht unterstützen. Der Grund, warum Sie als kanonische Optionen bereitgestellt werden, liegt darin, dass viele Anwendungen die Benutzeroberfläche verfügbar machen, damit Benutzer diese Optionen angeben können, wenn Sie eine Bilddatei in einem unterstützten Format speichern Das Bereitstellen einer kanonischen Methode zum Angeben dieser Optionen erleichtert es Anwendungen, diese auf konsistente Weise mit Encodern zu kommunizieren. Die kanonischen Encoder-Optionen sind in der folgenden Tabelle aufgeführt.



| Encoder-Option     | VARTYPE  | Wertbereich               |
|--------------------|----------|---------------------------|
| Lossless           | VT \_ bool | True/False                |
| ImageQuality       | VT \_ R4   | 0,0-1.0                   |
| CompressionQuality | VT \_ R4   | 0,0-1.0                   |
| BitmapTransform    | VT \_ UI1  | WICBitmapTransformOptions |



 

Wenn Ihr CODEC eine verlustfreie Codierung unterstützt, sollten Sie die Option für den Verlust des freien Encoders als Möglichkeit für Anwendungen verfügbar machen, die eine Verlust lose Codierung eines Bilds anzufordern. Wenn ein Aufrufer diese Eigenschaft auf "true" festlegt, sollten Sie die Option "ImageQuality" ignorieren und das Bildverlust frei codieren.

Die Option ImageQuality ermöglicht einer Anwendung, den Grad der Genauigkeit anzugeben, mit dem das Bild codiert werden soll. Mit dieser Option kann ein Benutzer einen Kompromiss zwischen Bildqualität und Geschwindigkeit und/oder Dateigröße treffen. JPEG ist ein Beispiel für ein Bildformat, das diese Abwägung unterstützt. Der Wert 0,0 gibt an, dass die Genauigkeit eine niedrige Wichtigkeit hat und der Encoder den größten Verlust Algorithmus verwenden soll. Der Wert 1,0 gibt an, dass die Genauigkeit die wichtigste ist, und der Encoder sollte die höchstmögliche Genauigkeit beibehalten. (Abhängig von Ihrem Codec ist dies möglicherweise mit der Option für die verlustfreie Option gleichbedeutend. Wenn Ihr CODEC jedoch eine verlustfreie Codierung unterstützt und die Option "Verlustfrei" auf "true" festgelegt ist, sollte die Option "ImageQuality" ignoriert werden.)

Die CompressionQuality-Option ermöglicht es einer Anwendung, die Effizienz der Komprimierung anzugeben, die beim Codieren des Bilds verwendet werden soll. Ein sehr effizienter Algorithmus erzeugt möglicherweise eine kleinere Bilddatei mit der gleichen Qualität wie ein weniger effizienter Komprimierungs Algorithmus, kann aber länger dauern. Mit dieser Option kann ein Benutzer einen Kompromiss zwischen der Dateigröße und der Geschwindigkeit der Codierung angeben und gleichzeitig denselben Grad an Qualität beibehalten. TIFF ist ein Beispiel für ein Bildformat, das diesen Kompromiss unterstützt. (Beachten Sie, dass ein Format wie JPEG verschiedene Komprimierungs Ebenen unterstützt, aber eine höhere Komprimierungsrate führt zu einer niedrigeren Bildqualität. Daher würde ein JPEG-Bildformat anstelle der CompressionQuality-Option die ImageQuality-Option verfügbar machen.) Der Wert 0,0 für diese Option gibt an, dass Sie das Bild so schnell wie möglich komprimieren sollten, ohne die Genauigkeit zu verringern, auf Kosten einer größeren Dateigröße. Der Wert 1,0 gibt an, dass Sie die kleinste mögliche Dateigröße (auf derselben Ebene der Qualität) erstellen sollten, unabhängig davon, wie lange es dauert, bis Sie codiert wird. Ein Codec kann sowohl die ImageQuality-Option als auch die CompressionQuality-Option unterstützen, wobei die Option "ImageQuality" den akzeptablen Grad der Verlust Angabe angibt und die CompressionQuality-Option einen Kompromiss zur Größe/Geschwindigkeit auf der angegebenen Qualitätsstufe bietet.

Die BitmapTransform-Option bietet dem Aufrufer die Möglichkeit, beim Codieren einen Drehwinkel oder eine vertikale oder horizontale Drehung anzugeben. Die WICBitmapTransformOptions-Aufzählung, die zum Angeben der angeforderten Transformation verwendet wird, ist dieselbe Enumeration, die beim Anfordern einer Transformation durch die IWICBitmapSourceTransform-Schnittstelle verwendet wird.

Beachten Sie, dass Encoder nicht auf die kanonischen Codierungsoptionen beschränkt sind. Der Zweck der Encoder-Optionen besteht darin, Encodern das verfügbar machen ihrer Funktionen zu ermöglichen, und es gibt keine Beschränkung für die Arten von Funktionen, die Sie verfügbar machen können. Stellen Sie sicher, dass die Encoder-Optionen gut dokumentiert sind. Obwohl eine Anwendung den Eigenschaften Behälter verwenden kann, wird von dieser Methode zurückgegeben, um die Namen, Typen und Wertebereiche für die von Ihnen unterstützten Optionen zu ermitteln. die einzige Möglichkeit, ihre Bedeutungen zu ermitteln oder Sie in der Benutzeroberfläche verfügbar zu machen, ist die Dokumentation.

### <a name="commit"></a>Commit

[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) ist die Methode, die aufgerufen wird, nachdem alle Bilddaten und Metadaten in den Stream serialisiert wurden. Verwenden Sie diese Methode, um die vorschaubilddaten in den Stream und ggf. alle globalen Miniaturansichten, Metadaten, Paletten oder anderen Elemente zu serialisieren. Diese Methode sollte den Dateistream nicht schließen, da die Anwendung, die den Stream geöffnet hat, diese schließen soll.

Der-Abschnitt der IWICBitmapFrameEncode: Commit-Methode enthält Details dazu, wie sich die iwicbitmapcodercacheoptions auf das Verhalten dieser Methode auswirkt.

### <a name="setpreview"></a>SetPreview

[**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) wird verwendet, um eine Vorschau des Images zu erstellen. Es ist zwar nicht zwingend erforderlich, dass jedes Image über eine Vorschauversion verfügt, aber es wird dringend empfohlen. Moderne digitale Kameras und Scanner generieren sehr hochauflösende Images, die tendenziell sehr groß sind und folglich eine beträchtliche Verarbeitungszeit zum Decodieren benötigen. Bilder von der nächsten Generation von Kameras werden noch größer. Es empfiehlt sich, eine kleinere, niedrigere Auflösungs Version eines Images bereitzustellen, in der Regel im JPEG-Format, das schnell decodiert und sofort angezeigt werden kann, wenn ein Benutzer es anfordert. Eine Anwendung kann eine Vorschau anfordern, bevor Sie das eigentliche Abbild anfordert, das decodiert wird, um Benutzern eine bessere Benutzer Leistung zu bieten, und zeigt Ihnen eine Darstellung des Bilds in der Bildschirmgröße an, während die Benutzer auf eine Decodierung des eigentlichen Bilds warten. Obwohl Codecs Vorschau Versionen bereitstellen sollten, sollten Codecs, die [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) nicht unterstützen, dies definitiv tun.

Wenn Sie eine JPEG-Vorschau bereitstellen, müssen Sie keinen JPEG-Encoder schreiben, um Sie zu codieren. Sie sollten die Delegaten an den JPEG-Encoder delegieren, der mit der WIC-Plattform ausgeliefert wird

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[**Iwicbitmapcoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)
</dt> <dt>

[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)
</dt> <dt>

**Licher**
</dt> <dt>

[Encoder-Schnittstellen](-wic-encoderinterfaces.md)
</dt> <dt>

[Implementieren von IWICBitmapCodecProgressNotification (Encoder)](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
