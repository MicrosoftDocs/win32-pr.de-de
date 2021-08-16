---
description: Implementieren von IWICBitmapEncoder
ms.assetid: b671e941-ded6-4bde-bc4d-461f13feade0
title: Implementieren von IWICBitmapEncoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69d02105470f837dba0689b665473c01c42f6cd6497a85424ea6eea3371696f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088012"
---
# <a name="implementing-iwicbitmapencoder"></a>Implementieren von IWICBitmapEncoder

-   [IWICBitmapEncoder](#implementing-iwicbitmapencoder)
    -   [Initialisieren](#initialize)
    -   [GetContainerFormat](#getcontainerformat)
    -   [GetEncoderInfo](#getencoderinfo)
    -   [CreateNewFrame](#createnewframe)
    -   [Commit](#commit)
    -   [SetPreview](#setpreview)
-   [Zugehörige Themen](#related-topics)

## <a name="iwicbitmapencoder"></a>IWICBitmapEncoder

-   [Initialisieren](#initialize)
-   [GetContainerFormat](#getcontainerformat)
-   [GetEncoderInfo](#getencoderinfo)
-   [CreateNewFrame](#createnewframe)
-   [Commit](#commit)
-   [SetPreview](#setpreview)

Diese Schnittstelle ist die Entsprechung zur [**IWICBitmapDecoder-Schnittstelle**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) und der Ausgangspunkt für die Codierung einer Bilddatei. Genau wie **IWICBitmapDecoder** zum Abrufen von Eigenschaften auf Containerebene und einzelner Frames aus dem Imagecontainer verwendet wird, wird [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) verwendet, um Eigenschaften auf Containerebene festzulegen und einzelne Imageframes in den Container zu serialisieren. Sie implementieren diese Schnittstelle für Ihre Encoderklasse auf Containerebene.

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

Wie unter [Implementieren von IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)erläutert, weisen einige Bildformate globale Miniaturansichten, Farbkontexte oder Metadaten auf, während viele Bildformate diese nur pro Frame bereitstellen. Daher sind die Methoden zum Festlegen dieser Optionen für [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)optional, aber für [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)erforderlich. Die methoden, die für **IWICBitmapEncoder** optional sind, werden im Abschnitt zu **IWICBitmapFrameEncode** erläutert, in dem sie am häufigsten implementiert werden.

Wenn Sie keine globalen Miniaturansichten unterstützen, geben Sie WINCODEC \_ ERR \_ CODECNOTHUMBNAIL von der SetThumbnail-Methode auf [**IWICBitmapEncoder zurück.**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) Wenn Sie keine Palette auf Containerebene unterstützen oder das image, das Sie codieren, kein indiziertes Format hat, geben Sie WINCODEC \_ ERR \_ PALETTEUNAVAILABLE von der SetPalette-Methode zurück. Geben Sie für alle anderen nicht unterstützten Methoden WINCODEC \_ ERR \_ UNSUPPORTEDOPERATION zurück.

### <a name="initialize"></a>Initialisieren

[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize) ist die erste Methode, die nach der Instanziierung für einen [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) aufgerufen wurde. Ein Bilddatenstrom wird an den Encoder übergeben, und ein Aufrufer kann optional eine Cacheoption angeben. Im Fall des Decoders ist der Stream schreibgeschützt, aber der an einen Encoder übergebene Stream ist ein beschreibbarer Stream, in den der Encoder alle Bilddaten und Metadaten serialisiert. Die Cacheoptionen auf dem Encoder unterscheiden sich ebenfalls.

``` syntax
enum WICBitmapEncoderCacheOption
{
   WICBitmapEncoderCacheInMemory,
   WICBitmapEncoderCacheTempFile,
   WICBitmapEncoderNoCache
}
```

Die Anwendung hat die Möglichkeit, den Encoder anzufordern, die Bilddaten im Arbeitsspeicher zwischenzuspeichern, in einer temporären Datei zwischenzuspeichern oder sie ohne Zwischenspeicherung direkt in die Datenträgerdatei zu schreiben. Wenn der Encoder aufgefordert wird, die Daten in einer temporären Datei zwischenzuspeichern, sollte er eine temporäre Datei auf dem Datenträger erstellen und direkt in diese Datei schreiben, ohne im Arbeitsspeicher zwischenzuspeichern. Wenn der Aufrufer die Option "Kein Cache" auswählt, muss für jeden Frame ein Commit ausgeführt werden, damit der nächste Frame erstellt werden kann.

### <a name="getcontainerformat"></a>GetContainerFormat

[**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getcontainerformat) wird auf die gleiche Weise wie die [GetContainerFormat-Methode](-wic-imp-iwicbitmapdecoder.md) in [Implementieren von IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)implementiert.

### <a name="getencoderinfo"></a>GetEncoderInfo

[**GetEncoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo) gibt ein [**IWICBitmapEncoderInfo-Objekt**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo) zurück. Um das **IWICBitmapEncoderInfo-Objekt** abzurufen, übergeben Sie einfach die GUID Ihres Encoders an die [**CreateComponentInfo-Methode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) in [**IWICImagingFactory,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)und fordern Sie dann die **IWICBitmapEncoderInfo-Schnittstelle** an.

Sehen Sie sich das Beispiel unter [Implementieren von IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md) unter [GetDecoderInfo](-wic-imp-iwicbitmapdecoder.md)an.

### <a name="createnewframe"></a>CreateNewFrame

[**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) ist das Encoderentsprechung von [**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) auf [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder). Diese Methode gibt ein [**IWICBitmapFrameEncode-Objekt**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) zurück, das das Objekt ist, das die Bilddaten für einen bestimmten Frame innerhalb des Containers serialisiert.

Einer der Vorteile von Windows Imaging Component (WIC) besteht darin, dass sie eine Abstraktionsebene für Anwendungen bereitstellt, die es ihnen ermöglicht, mit allen Bildformaten auf die gleiche Weise zu arbeiten. Allerdings sind nicht alle Bildformate identisch. Einige Bildformate verfügen über Funktionen, die andere nicht haben. Damit Anwendungen diese einzigartigen Funktionen nutzen können, ist es erforderlich, eine Möglichkeit für den Codec bereitzustellen, um sie verfügbar zu machen. Dies ist der Zweck von Encoderoptionen. Wenn Ihr Codec Encoderoptionen unterstützt, sollten Sie ein [IPropertyBag2-Objekt](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) erstellen, das die unterstützten Encoderoptionen verfügbar macht, und es im *ppIEncoderOptions-Parameter* dieser Methode zurückgeben. Der Aufrufer kann dann dieses IPropertyBag2-Objekt verwenden, um zu bestimmen, welche Encoderoptionen Ihr Codec unterstützt. Wenn der Aufrufer Werte für eine der unterstützten Encoderoptionen angeben möchte, weist er den Wert der relevanten Eigenschaft im IPropertyBag2-Objekt zu und übergibt ihn in seiner Initialize-Methode an das neu erstellte [**IWICBitmapFrameEncode-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)

Um ein [IPropertyBag2-Objekt](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) zu instanziieren, müssen Sie zunächst eine PROPBAG2-Struktur erstellen, um jede Encoderoption anzugeben, die Ihr Encoder unterstützt, und seinen Datentyp für jede Eigenschaft anzugeben. Anschließend müssen Sie ein IPropertyBag2-Objekt implementieren, das die Wertbereiche für jede Eigenschaft beim Schreiben erzwingt und alle in Konflikt stehenden oder überlappenden Werte abgleicht. Für einfache Sätze nicht in Konflikt stehender Encoderoptionen können Sie die [**CreateEncoderPropertyBag-Methode**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createencoderpropertybag) aufrufen, die ein einfaches IPropertyBag2-Objekt mithilfe der Eigenschaften erstellt, die Sie in Ihrer PROPBAG2-Struktur angeben. Sie müssen weiterhin die Wertbereiche erzwingen. Wenn Sie erweiterte Encoderoptionen benötigen oder konfliktverursachende Werte abstimmen müssen, sollten Sie Ihre eigene IPropertyBag2-Implementierung schreiben.


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



WIC bietet einen kleinen Satz kanonischer Encoderoptionen, die von einigen gängigen Bildformaten verwendet werden. Alle kanonischen Encoderoptionen sind optional, und Codecs sind nicht erforderlich, um sie zu unterstützen. Sie werden als kanonische Optionen bereitgestellt, weil viele Anwendungen die Benutzeroberfläche für Benutzer verfügbar machen, um diese Optionen anzugeben, wenn sie eine Bilddatei in einem Format speichern, das sie unterstützt. Die Bereitstellung einer kanonischen Methode zum Angeben dieser Optionen erleichtert Anwendungen die konsistente Kommunikation mit Encodern. Die kanonischen Encoderoptionen sind in der folgenden Tabelle aufgeführt.



| Encoderoption     | VARTYPE  | Wertbereich               |
|--------------------|----------|---------------------------|
| Lossless           | VT \_ BOOL | Wahr/falsch                |
| ImageQuality       | VT \_ R4   | 0.0-1.0                   |
| CompressionQuality | VT \_ R4   | 0.0-1.0                   |
| BitmapTransform    | VT \_ UI1  | WICBitmapTransformOptions |



 

Wenn Ihr Codec die verlustfreie Codierung unterstützt, sollten Sie die Option Verlustloser Encoder verfügbar machen, damit Anwendungen anfordern können, dass ein Bild verlustfrei codiert wird. Wenn ein Aufrufer diese Eigenschaft auf True festlegt, sollten Sie die Option ImageQuality ignorieren und das Bild verlustfrei codieren.

Mit der Option ImageQuality kann eine Anwendung den Grad der Genauigkeit angeben, mit dem das Bild codiert werden soll. Mit dieser Option kann ein Benutzer einen Kompromiss zwischen der Imagequalität und der Geschwindigkeit und/oder Dateigröße herstellen. JPEG ist ein Beispiel für ein Bildformat, das diesen Kompromiss unterstützt. Der Wert 0,0 gibt an, dass die Genauigkeit von geringer Wichtigkeit ist und der Encoder den verlustigsten Algorithmus verwenden sollte. Der Wert 1,0 gibt an, dass die Genauigkeit am wichtigsten ist und der Encoder die höchstmögliche Genauigkeit beibehalten sollte. (Je nach Codec kann dies mit der Option Verlustlos synonym sein. Wenn Ihr Codec jedoch die verlustfreie Codierung unterstützt und die Option Lossless auf True festgelegt ist, sollte die Option ImageQuality ignoriert werden.)

Mit der CompressionQuality-Option kann eine Anwendung die Effizienz der Komprimierung angeben, die beim Codieren des Bilds verwendet werden soll. Ein sehr effizienter Algorithmus erzeugt möglicherweise eine kleinere Bilddatei mit der gleichen Qualität wie ein weniger effizienter Komprimierungsalgorithmus, die Codierung kann jedoch länger dauern. Mit dieser Option kann ein Benutzer einen Kompromiss zwischen Dateigröße und Codierungsgeschwindigkeit angeben und dabei die gleiche Qualität beibehalten. TIFF ist ein Beispiel für ein Bildformat, das diesen Kompromiss unterstützt. (Beachten Sie, dass ein Format wie JPEG verschiedene Komprimierungsstufen unterstützt, aber eine höhere Komprimierungsrate führt zu einer niedrigeren Bildqualität. Daher würde ein JPEG-Bildformat die Option ImageQuality anstelle der CompressionQuality-Option verfügbar machen.) Der Wert 0,0 für diese Option gibt an, dass Sie das Bild so schnell wie möglich komprimieren sollten, ohne die Genauigkeit auf Kosten einer größeren Dateigröße zu reduzieren. Der Wert 1.0 gibt an, dass Sie die kleinstmögliche Dateigröße (mit der gleichen Qualitätsstufe) erstellen sollten, unabhängig davon, wie lange die Codierung dauern kann. Ein Codec kann sowohl die Option ImageQuality als auch die Option CompressionQuality unterstützen, wobei die Option ImageQuality den akzeptablen Verlustgrad angibt und die Option CompressionQuality einen Größen-/Geschwindigkeits-Kompromiss auf der angegebenen Qualitätsebene bietet.

Die Option BitmapTransform bietet dem Aufrufer die Möglichkeit, bei der Codierung einen Drehwinkel oder eine vertikale oder horizontale Flip-Ausrichtung anzugeben. Die WICBitmapTransformOptions-Enumeration, mit der die angeforderte Transformation angegeben wird, entspricht der Enumeration, die beim Anfordern einer Transformation während der Decodierung über die IWICBitmapSourceTransform-Schnittstelle verwendet wird.

Beachten Sie, dass Encoder nicht auf die kanonischen Encoderoptionen beschränkt sind. Der Zweck von Encoderoptionen besteht darin, Encodern zu ermöglichen, ihre Funktionen verfügbar zu machen, und es gibt keine Beschränkung für die Typen von Funktionen, die Sie verfügbar machen können. Stellen Sie sicher, dass Die Encoderoptionen gut dokumentiert sind. Obwohl eine Anwendung den Eigenschaftenbehälter verwenden kann, den Sie von dieser Methode zurückgeben, um die Namen, Typen und Wertbereiche für die von Ihnen unterstützten Optionen zu ermitteln, ist die einzige Möglichkeit für sie, ihre Bedeutungen zu ermitteln oder sie auf der Benutzeroberfläche verfügbar zu machen, in Ihrer Dokumentation.

### <a name="commit"></a>Commit

[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) ist die Methode, die Sie aufrufen, nachdem alle Bilddaten und Metadaten in den Stream serialisiert wurden. Sie sollten diese Methode verwenden, um die Vorschaubilddaten in den Stream und ggf. globale Miniaturansichten, Metadaten, Paletten oder andere Elemente zu serialisieren. Diese Methode sollte den Dateistream nicht schließen, da von der Anwendung, die den Stream geöffnet hat, erwartet wird, dass er geschlossen wird.

Der Abschnitt der IWICBitmapFrameEncode:Commit-Methode enthält Details dazu, wie sich DIE IWICBitmapEncoderCacheOptions auf das Verhalten dieser Methode auswirken.

### <a name="setpreview"></a>SetPreview

[**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) wird verwendet, um eine Vorschau des Images zu erstellen. Es ist zwar nicht zwingend erforderlich, dass jedes Image über eine Vorschauversion verfügen muss, es wird jedoch dringend empfohlen. Moderne Digitalkameras und Scanner generieren bilder mit sehr hoher Auflösung, die in der Regel sehr groß sind und daher eine erhebliche Verarbeitungszeit für die Decodierung inne haben. Bilder der nächsten Generation von Kameras werden noch größer sein. Es ist eine gute Idee, eine kleinere Version eines Bilds mit niedrigerer Auflösung (in der Regel im JPEG-Format) zur Verfügung zu stellen, die schnell decodiert und "sofort" angezeigt werden kann, wenn ein Benutzer es an fordert. Eine Anwendung kann eine Vorschau anfordern, bevor sie die Decodierung des eigentlichen Bilds angibt, um benutzern eine bessere Benutzererfahrung zu bieten, und ihnen eine Darstellung des Bilds in Bildschirmgröße anzeigen, während sie darauf warten, das tatsächliche Bild zu decodieren. Codecs sollten zwar Vorschauen bereitstellen, Codecs, die [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) nicht unterstützen, sollten dies jedoch definitiv tun.

Wenn Sie eine JPEG-Vorschau bereitstellen, müssen Sie keinen JPEG-Encoder schreiben, um ihn zu codieren. Sie sollten an den JPEG-Encoder delegieren, der mit der WIC-Plattform für die Codierung von Vorschauversionen und Miniaturansichten enthalten ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)
</dt> <dt>

[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Encoderschnittstellen](-wic-encoderinterfaces.md)
</dt> <dt>

[Implementieren von IWICBitmapCodecProgressNotification (Encoder)](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)
</dt> <dt>

[Schreiben eines WIC-Enabled CODEC](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Übersicht über Bildverarbeitungskomponenten](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
