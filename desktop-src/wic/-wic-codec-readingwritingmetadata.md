---
description: Dieses Thema bietet einen Überblick über die Verwendung der WIC-APIs (Windows Imaging Component) zum Lesen und Schreiben von Metadaten, die in Bilddateien eingebettet sind.
ms.assetid: b1e0b936-a13a-42dd-8470-957ba1d90423
title: Übersicht über das Lesen und Schreiben von Bild Metadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 484d562b71184c20adf054f1de2a4203878da9b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959943"
---
# <a name="overview-of-reading-and-writing-image-metadata"></a>Übersicht über das Lesen und Schreiben von Bild Metadaten

Dieses Thema bietet einen Überblick über die Verwendung der WIC-APIs (Windows Imaging Component) zum Lesen und Schreiben von Metadaten, die in Bilddateien eingebettet sind.

Dieses Thema enthält folgende Abschnitte:

-   [Voraussetzungen](#prerequisites)
-   [Introduction (Einführung)](#introduction)
-   [Lesen von Metadadata mithilfe eines Abfrage Readers](#reading-metadadata-using-a-query-reader)
    -   [Abrufen eines Abfrage Readers](#obtaining-a-query-reader)
    -   [Lesen von Metadaten](#reading-metadata)
    -   [Zusätzliche Abfrage Reader-Methoden](#additional-query-reader-methods)
-   [Schreiben von Metadaten mit einem Abfrage-Writer](#writing-metadata-using-a-query-writer)
    -   [Abrufen eines Abfrage-Writers](#obtaining-a-query-writer)
    -   [Hinzufügen von Metadaten](#adding-metadata)
    -   [Entfernen von Metadaten](#removing-metadata)
    -   [Kopieren von Metadaten für die erneute Codierung](#copying-metadata-for-re-encoding)
-   [Schnelle metadatencodierung](#fast-metadata-encoding)
    -   [Hinzufügen von Padding zu metadatenblöcken](#adding-padding-to-metadata-blocks)
    -   [Abrufen eines schnellen metadatenencoders](#obtaining-a-fast-metadata-encoder)
    -   [Verwenden des schnellen metadatenencoders](#using-the-fast-metadata-encoder)
-   [Zugehörige Themen](#related-topics)

## <a name="prerequisites"></a>Voraussetzungen

Um dieses Thema zu verstehen, sollten Sie mit dem WIC-Metadatensystem vertraut sein, wie in der [WIC-Metadatenübersicht](-wic-about-metadata.md)beschrieben. Sie sollten auch mit der Abfragesprache vertraut sein, die zum Lesen und Schreiben von Metadaten verwendet wird, wie unter [Übersicht über die metadatenquery-Sprache](-wic-codec-metadataquerylanguage.md)beschrieben.

## <a name="introduction"></a>Einführung

WIC bietet Anwendungsentwicklern Component Object Model (com)-Komponenten zum Lesen und Schreiben von Metadaten, die in Bilddateien eingebettet sind. Es gibt zwei Möglichkeiten, um Metadaten zu lesen und zu schreiben:

-   Verwenden eines Abfrage Readers/Writer und eines Abfrage Ausdrucks, um Metadatenblöcke für geschachtelte Blöcke oder bestimmte Metadaten innerhalb eines-Blocks abzufragen.
-   Verwenden eines metadatenhandlers (ein metadatenreader oder ein metadatenwriter) für den Zugriff auf geschachtelte Metadatenblöcke oder bestimmte Metadaten innerhalb der Metadatenblöcke.

Am einfachsten ist es, einen Abfrage Reader/-Writer und einen Abfrage Ausdruck zu verwenden, um auf die Metadaten zuzugreifen. Ein Abfrage Reader ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) wird zum Lesen von Metadaten verwendet, während ein Abfrage Schreiber ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) verwendet wird, um Metadaten zu schreiben. Beide verwenden einen Abfrage Ausdruck, um die gewünschten Metadaten zu lesen oder zu schreiben. Im Hintergrund verwendet ein Abfrage Leser (und Writer) einen Metadatenhandler, um auf die vom Abfrage Ausdruck beschriebenen Metadaten zuzugreifen.

Die erweiterte Methode besteht darin, direkt auf die Metadatenhandler zuzugreifen. Ein Metadatenhandler wird aus den einzelnen Frames mithilfe eines Block Readers ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)) oder eines blockwriter ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)) abgerufen. Die beiden verfügbaren Metadatenhandler sind der metadatenreader ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) und der metadatenwriter ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)).

Das folgende Diagramm des Inhalts einer JPEG-Bilddatei wird in den Beispielen in diesem Thema verwendet. Das durch dieses Diagramm dargestellte Bild wurde mit Microsoft Paint erstellt. die Bewertungs Metadaten wurden mithilfe der Photo Gallery-Funktion von Windows Vista hinzugefügt.

![Abbildung des JPEG-Bilds mit Bewertungs Metadaten](graphics/jpeg.png)

## <a name="reading-metadadata-using-a-query-reader"></a>Lesen von Metadadata mithilfe eines Abfrage Readers

Die einfachste Möglichkeit zum Lesen von Metadaten ist die Verwendung der Abfrage Lese Schnittstelle, [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader). Der Abfrage Reader ermöglicht das Lesen von metadatenblöcken und Elementen innerhalb von metadatenblöcken mithilfe eines Abfrage Ausdrucks.

Es gibt drei Möglichkeiten zum Abrufen eines Abfrage Readers: über einen Bitmap-Decoder ([**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)), über die einzelnen Frames ([**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)) oder über einen Abfrage-Writer ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).

### <a name="obtaining-a-query-reader"></a>Abrufen eines Abfrage Readers

Der folgende Beispielcode zeigt, wie Sie einen Bitmap-Decoder aus der Imaging Factory abrufen und einen einzelnen BitmapFrame abrufen. Dieser Code führt auch Setup Schritte aus, die zum Abrufen eines Abfrage Readers von einem decodierten Frame erforderlich sind.


```
IWICImagingFactory *pFactory = NULL;
IWICBitmapDecoder *pDecoder = NULL;
IWICBitmapFrameDecode *pFrameDecode = NULL;
IWICMetadataQueryReader *pQueryReader = NULL;
IWICMetadataQueryReader *pEmbedReader = NULL;
PROPVARIANT value;

// Initialize COM
CoInitialize(NULL);

// Initialize PROPVARIANT
PropVariantInit(&value);

//Create the COM imaging factory
HRESULT hr = CoCreateInstance(
    CLSID_WICImagingFactory,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_IWICImagingFactory,
    (LPVOID*)&pFactory);

// Create the decoder
if (SUCCEEDED(hr))
{
    hr = pFactory->CreateDecoderFromFilename(
        L"test.jpg",
        NULL,
        GENERIC_READ,
        WICDecodeMetadataCacheOnDemand,
        &pDecoder);
}

// Get a single frame from the image
if (SUCCEEDED(hr))
{
    hr = pDecoder->GetFrame(
         0,  //JPEG has only one frame.
         &pFrameDecode); 
}
```



Der Bitmap-Decoder für die test.jpg Datei wird mithilfe der Methode " **kreatedecoderfromfilename** " der Imaging Factory abgerufen. In dieser Methode wird der vierte Parameter auf den Wert WICDecodeMetadataCacheOnDemand aus der [**wicdecodeoptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) -Enumeration festgelegt. Dadurch wird der Decoder aufgefordert, die Metadaten zwischenzuspeichern, wenn die Metadaten benötigt werden. entweder durch Abrufen eines Abfrage Readers oder des zugrunde liegenden metadatenreaders. Wenn Sie diese Option verwenden, können Sie den Datenstrom in den Metadaten aufbewahren, die für die schnelle metadatencodierung erforderlich sind Alternativ können Sie auch den anderen **wicdecodeoptions** -Wert, WICDecodeMetadataCacheOnLoad, verwenden, der die eingebetteten Bild Metadaten zwischenspeichert, sobald das Bild geladen wird.

Um den Abfrage Reader des Frames abzurufen, führen Sie einen einfachen Abruf der **GetMetadataQueryReader** -Methode des Frames aus. Der folgende Code veranschaulicht diesen-Befehl.


```
// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}
```



Ebenso kann ein Abfrage Reader auch auf der decoderebene abgerufen werden. Ein einfacher Aufrufder **GetMetadataQueryReader** -Methode des Decoders Ruft den Abfrage Reader des Decoders ab. Im Gegensatz zum Abfrage Leser eines Frames liest der Abfrage Reader eines Decoders Metadaten für ein Bild, das sich außerhalb der einzelnen Frames befindet. Dieses Szenario ist jedoch nicht üblich, und die nativen Image Formate unterstützen diese Funktion nicht. Das systemeigene Bild, das von WIC bereitgestellt wird, dient zum Lesen und Schreiben von Metadaten auf Frame-Ebene, auch bei Einzel Frame Formaten wie JPEG.

### <a name="reading-metadata"></a>Lesen von Metadaten

Bevor Sie mit dem Lesen von Metadaten fortfahren, sehen Sie sich das folgende Diagramm einer JPEG-Datei an, die eingebettete Metadatenblöcke und die tatsächlich abzurufenden Daten enthält. Dieses Diagramm stellt Legenden für bestimmte Metadatenblöcke und Elemente innerhalb des Bilds bereit und stellt den metadatenabfrageausdruck für jeden Block oder jedes Element bereit.

![Abbildung des JPEG-Bilds mit metadatenaufrufen](graphics/jpegwithcallouts.png)

Um eingebettete Metadatenblöcke oder bestimmte Elemente anhand des Namens abzufragen, müssen Sie die **GetMetadataByName** -Methode aufzurufen. Diese Methode nimmt einen Abfrage Ausdruck und eine [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) an, in der das Metadatenelement zurückgegeben wird. Der folgende Code fragt einen gruppierten Metadatenblock ab und konvertiert die [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Komponente, die vom PROPVARIANT-Wert bereitgestellt wird, in einen Abfrage Reader, sofern gefunden.


```
if (SUCCEEDED(hr))
{
    // Get the nested IFD reader
    hr = pQueryReader->GetMetadataByName(L"/app1/ifd", &value);
    if (value.vt == VT_UNKNOWN)
    {
        hr = value.punkVal->QueryInterface(IID_IWICMetadataQueryReader, (void **)&pEmbedReader);
    }
    PropVariantClear(&value); // Clear value for new query
}
```



Der Abfrage Ausdruck "/App1/IFD" fragt den im App1-Block geblösteten IFD-Block ab. Die JPEG-Bilddatei enthält den in der Tabelle eingefügten IFD-Metadatenblock, sodass die [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) mit einem Variablentyp (VT) von `VT_UNKNOWN` und einem Zeiger auf eine [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle (punkVal) zurückgegeben wird. Anschließend Fragen Sie die IUnknown-Schnittstelle nach einem Abfrage Reader ab.

Der folgende Code veranschaulicht eine neue Abfrage auf der Grundlage des neuen Abfrage Readers in Bezug auf den Block mit dem Block "IFD".


```
if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetMetadataByName(L"/{ushort=18249}", &value);
    PropVariantClear(&value); // Clear value for new query
}
```



Der Abfrage Ausdruck "/{ushort = 18249}" fragt den IFD-Block für die microsoftphoto-Bewertung ab, die unter Tag 18249 eingebettet ist. Der [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Wert enthält jetzt den Werttyp `VT_UI2` und den Datenwert 50.

Es ist jedoch nicht erforderlich, einen-Block zu erhalten, bevor bestimmte Datenwerte abgefragt werden. Anstatt z. b. die geclusterte IFD und dann die microsoftphoto-Bewertung abzufragen, können Sie stattdessen den Block "root Metadata" und die im folgenden Code gezeigte Abfrage verwenden, um dieselben Informationen zu erhalten.


```
if (SUCCEEDED(hr))
{
    hr = pQueryReader->GetMetadataByName(L"/app1/ifd/{ushort=18249}", &value);
    PropVariantClear(&value);
}
```



Zusätzlich zum Abfragen spezifischer Metadatenelemente in einem Metadatenblock können Sie auch alle Metadatenelemente in einem Metadatenblock auflisten (ohne Metadatenelemente in gruppierten metadatenblöcken). Um die Metadatenelemente im aktuellen Block aufzulisten, wird die **GetEnumeration** -Methode des Abfrage Readers verwendet. Diese Methode ruft eine **IEnumString** -Schnittstelle ab, die mit den Metadatenelementen im aktuellen Block gefüllt ist. Der folgende Code listet z. b. die XMP-Bewertung und die microsoftphoto-Bewertung für den zuvor erhaltenen Block-IFD-Block auf.


```
IEnumString *metadataItems = NULL;

if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetEnumerator(&metadataItems);
}
```



Weitere Informationen zum Identifizieren geeigneter Tags für verschiedene Bildformate und Metadatenformate finden Sie unter [Metadatenabfragen für das Native Image](-wic-native-image-format-metadata-queries.md).

### <a name="additional-query-reader-methods"></a>Zusätzliche Abfrage Reader-Methoden

Zusätzlich zum Lesen von Metadaten können Sie auch zusätzliche Informationen über den Abfrage Leser abrufen und Metadaten auf andere Weise abrufen. Der Abfrage Reader stellt zwei Methoden bereit, die Informationen über den Abfrage Reader, **GetContainerFormat** und **getLocation** bereitstellen.

Mit dem eingebetteten Abfrage Reader können Sie **GetContainerFormat** verwenden, um den Typ des Metadatenblocks zu bestimmen, und Sie können **getLocation** aufrufen, um den Pfad relativ zum stammmetadatenblock abzurufen. Der folgende Code fragt den eingebetteten Abfrage Reader nach seinem Speicherort ab.


```
// Determine the metadata block format

if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetContainerFormat(&containerGUID);
}

// Determine the query reader's location
if (SUCCEEDED(hr))
{
    UINT length;
    WCHAR readerNamespace[100];
    hr = pEmbedReader->GetLocation(100, readerNamespace, &length);
}
```



Der get-Befehl von **GetContainerFormat** für den eingebetteten Abfrage Reader gibt die GUID des IFD-metadatenformats zurück. Der **getLocation** -Rückruf gibt einen Namespace von "/App1/IFD" zurück. Bereitstellen des relativen Pfads, von dem nachfolgende Abfragen für den neuen Abfrage Reader ausgeführt werden. Der vorangehende Code ist natürlich nicht sehr nützlich, es wird jedoch veranschaulicht, wie die **getLocation** -Methode zum Suchen von geschposteten metadatenblöcken verwendet werden kann.

## <a name="writing-metadata-using-a-query-writer"></a>Schreiben von Metadaten mit einem Abfrage-Writer

> [!Note]  
> Einige der in diesem Abschnitt bereitgestellten Codebeispiele werden im Kontext der eigentlichen Schritte, die zum Schreiben von Metadaten erforderlich sind, nicht angezeigt. Um die Codebeispiele im Kontext eines funktionierenden Beispiels anzuzeigen, finden Sie weitere Informationen unter Gewusst wie: Erneutes Codieren eines Bilds mit Metadaten.

 

Die Hauptkomponente zum Schreiben von Metadaten ist der Abfrage-Writer ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)). Mit dem Query Writer können Sie Metadatenblöcke und Elemente innerhalb eines Metadatenblocks festlegen und entfernen.

Ebenso wie der Abfrage Reader gibt es drei Möglichkeiten, einen Abfragewriter abzurufen: über einen Bitmap-Encoder ([**iwicbitmapcoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)), über seine einzelnen Frames ([**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)) oder über einen schnellen metadatenencoder ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)).

### <a name="obtaining-a-query-writer"></a>Abrufen eines Abfrage-Writers

Der häufigste Abfrage-Writer ist für einen einzelnen Frame einer Bitmap. Dieser Abfrage-Writer legt die Metadatenblöcke und Elemente eines Bilds fest und entfernt Sie. Um den Abfrage-Writer eines Bild Frames abzurufen, rufen Sie die **GetMetadataQueryWriter** -Methode des Frames auf. Der folgende Code veranschaulicht den einfachen Methoden Aufrufzum Abrufen des Abfrage Writers eines Frames.


```
IWICMetadataQueryWriter &pFrameQWriter = NULL;

//Obtain a query writer from the frame.
hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
```



Auf ähnliche Weise kann auch ein Abfrage-Writer für die Encoder-Ebene abgerufen werden. Ein einfacher Rückruf der **GetMetadataQueryWriter** -Methode des Encoders Ruft den Abfragewriter des Encoders ab. Im Gegensatz zum Abfrage-Writer eines Frames schreibt der Abfrage Schreiber eines Encoders Metadaten für ein Bild außerhalb des einzelnen Frames. Dieses Szenario ist jedoch nicht üblich, und die nativen Image Formate unterstützen diese Funktion nicht. Das systemeigene Bild, das von WIC bereitgestellt wird, dient zum Lesen und Schreiben von Metadaten auf Frame-Ebene, auch bei Einzel Frame Formaten wie JPEG.

Sie können einen Abfrage-Writer auch direkt von der Imaging Factory ([**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)) abrufen. Es gibt zwei Imaging Factory-Methoden, die einen Abfrage-Writer zurückgeben: " **kreatequerywriter** " und " **kreatequeryschreiterfromreader**".

Mit " **anatequerywriter** " wird ein Abfrage Schreiber für das angegebene Metadatenformat und den angegebenen Anbieter erstellt. Dieser Abfragewriter ermöglicht das Schreiben von Metadaten für ein bestimmtes Metadatenformat und das Hinzufügen zum Image. Der folgende Code veranschaulicht einen " **anatequerywriter** "-Befehl zum Erstellen eines XMP-Abfrage-Writers.


```
IWICMetadataQueryWriter *pXMPWriter = NULL;

// Create XMP block
GUID vendor = GUID_VendorMicrosoft;
hr = pFactory->CreateQueryWriter(
        GUID_MetadataFormatXMP,
        &vendor,
        &pXMPWriter);
```



In diesem Beispiel wird der Anzeige Name `GUID_MetadataFormatXMP` als *guidMetadataFormat* -Parameter verwendet. Sie stellt die GUID des XMP-metadatenformats dar, und der Hersteller stellt den von Microsoft erstellten Handler dar. Alternativ kann **null** als *pguidVendor* -Parameter mit denselben Ergebnissen übergeben werden, wenn kein anderer XMP-Handler vorhanden ist. Wenn ein benutzerdefinierter XMP-Handler neben dem systemeigenen XMP-Handler installiert wird, führt das Übergeben von **null** für den Hersteller dazu, dass der Abfragewriter mit der niedrigsten GUID zurückgegeben wird.

" **Kreatequeryschreiterfromreader** " ähnelt der Methode " **kreatequerywriter** ", mit dem Unterschied, dass Sie den neuen Abfragewriter mit den vom Abfrage Reader bereitgestellten Daten vorab füllt. Dies ist nützlich für die erneute Codierung eines Bilds bei Beibehaltung der vorhandenen Metadaten oder zum Entfernen unerwünschter Metadaten. Der folgende Code veranschaulicht einen Befehl zum Aufrufen von " **exatequeryschreiterfromreader** ".


```
hr = pFrameDecode->GetMetadataQueryReader(&pFrameQReader);

// Copy metadata using query readers
if(SUCCEEDED(hr) && pFrameQReader)
{
    IWICMetadataQueryWriter *pNewWriter = NULL;

    GUID vendor = GUID_VendorMicrosoft;
    hr = pFactory->CreateQueryWriterFromReader(
        pFrameQReader,
        &vendor,
        &pNewWriter);
```



### <a name="adding-metadata"></a>Hinzufügen von Metadaten

Nachdem Sie einen Abfrage-Writer erhalten haben, können Sie ihn verwenden, um Metadatenblöcke und Elemente hinzuzufügen. Um Metadaten zu schreiben, verwenden Sie die **SetMetadataByName** -Methode des Abfrage-Writers. **SetMetadataByName** nimmt zwei Parameter an: einen Abfrage Ausdruck (*wzName*) und einen Zeiger auf eine [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) (*pvarvalue*). Der Abfrage Ausdruck definiert den festzulegenden Block oder das Element, während die PROPVARIANT den tatsächlich festzulegenden Datenwert bereitstellt.

Das folgende Beispiel veranschaulicht das Hinzufügen eines Titels mithilfe des XMP-Abfrage-Writers, der zuvor mithilfe der Methode " **kreatequerywriter** " abgerufen wurde.


```
// Write metadata to the XMP writer
if (SUCCEEDED(hr))
{
    PROPVARIANT value;
    PropVariantInit(&value);

    value.vt = VT_LPWSTR;
    value.pwszVal = L"Metadata Test Image.";
   
    hr = pXMPWriter->SetMetadataByName(L"/dc:title", &value);

    PropVariantClear(&value);
}
```



In diesem Beispiel ist der Werttyp (VT) auf festgelegt `VT_LPWSTR` , was bedeutet, dass eine Zeichenfolge als Datenwert verwendet wird. Da der *Werttyp* eine Zeichenfolge ist, wird *pwszval* verwendet, um den zu verwendenden Titel festzulegen. **SetMetadataByName** wird dann mit dem Abfrage Ausdruck ""/DC: Title "und der neu festgelegten [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)aufgerufen. Der verwendete Abfrage Ausdruck gibt an, dass die Title-Eigenschaft im Schema der digitalen Kamera (DC) festgelegt werden sollte. Beachten Sie, dass der Ausdruck nicht "/XMP/DC: Title" ist; Dies liegt daran, dass der Abfrage Schreiber bereits für XMP spezifisch ist und keinen eingebetteten XMP-Block enthält, den "/XMP/DC: Title" vorschlagen würde.

Bis zu diesem Punkt haben Sie einem Bild Rahmen noch keine Metadaten hinzugefügt. Sie haben einfach einen Abfrage-Writer mit Daten aufgefüllt. Um einem Frame einen Metadatenblock hinzuzufügen, der durch den Abfrage-Writer dargestellt wird, wird **SetMetadataByName** erneut mit dem Abfrage-Writer als Wert der [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)aufgerufen. Auf diese Weise werden die Metadaten im Abfrage-Writer in den Bildframe kopiert. Der folgende Code veranschaulicht, wie Sie die Metadaten im XMP-Abfrage-Writer hinzufügen, die zuvor dem Stamm-Metadatenblock eines Frames abgerufen wurden.


```
// Get the frame's query writer and write the XMP query writer to it
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);

    // Copy the metadata in the XMP query writer to the frame
    if (SUCCEEDED(hr))
    {
        PROPVARIANT value;

        PropVariantInit(&value);
        value.vt = VT_UNKNOWN;
        value.punkVal = pXMPWriter;
        value.punkVal->AddRef();

        hr = pFrameQWriter->SetMetadataByName(L"/", &value);

        PropVariantClear(&value);
    }
}
```



In diesem Beispiel wird ein Werttyp (VT) von verwendet, der `VT_UNKOWN` einen COM-Schnittstellen Werttyp angibt. Der XMP-Abfrage-Writer (pixmpwriter) wird dann als Wert für die [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)verwendet, und es wird mithilfe der adressf-Methode ein Verweis darauf hinzugefügt. Schließlich wird der XMP-Abfrage-Writer festgelegt, indem die **SetMetadataByName** -Methode des Frames aufgerufen und der Abfrage Ausdruck "/", der den Stamm Block angibt, und die neu festgelegte PROPVARIANT übergeben werden.

> [!Note]  
> Wenn der Frame bereits den Metadatenblock enthält, den Sie hinzufügen möchten, werden die Metadaten hinzugefügt, die Sie hinzufügen, und vorhandene Metadaten werden überschrieben.

 

### <a name="removing-metadata"></a>Entfernen von Metadaten

Mit einem Abfrage-Writer können Sie auch Metadaten entfernen, indem Sie die **RemoveMetadataByName** -Methode aufrufen. **RemoveMetadataByName** nimmt einen Abfrage Ausdruck an und entfernt den Metadatenblock bzw. das Element, sofern vorhanden. Der folgende Code veranschaulicht, wie der zuvor hinzugefügte Titel entfernt wird.


```
if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/xmp/dc:title");
}
```



Der folgende Code veranschaulicht, wie der gesamte XMP-Metadatenblock entfernt wird.


```
if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/xmp");
}
```



### <a name="copying-metadata-for-re-encoding"></a>Kopieren von Metadaten für die erneute Codierung

> [!Note]  
> Der Code in diesem Abschnitt ist nur gültig, wenn die Quell-und Ziel Image Formate identisch sind. Wenn Sie in ein anderes Bildformat codieren, können Sie nicht alle Metadaten eines Bilds in einem einzelnen Vorgang kopieren.

 

Zum Beibehalten von Metadaten beim erneuten Codieren eines Bilds in dasselbe Bildformat stehen Methoden zum Kopieren aller Metadaten in einem einzelnen Vorgang zur Verfügung. Jeder dieser Vorgänge folgt einem ähnlichen Muster: jede legt die Metadaten des decodierten Frames direkt in den neuen Frame fest, der codiert wird.

Die bevorzugte Methode zum Kopieren von Metadaten besteht darin, den blockwriter des neuen Frames mit dem Block Reader des decodierten Frames zu initialisieren. Der folgende Code veranschaulicht diese Methode.


```
if (SUCCEEDED(hr) && formatsEqual)
{
    // Copy metadata using metadata block reader/writer
    if (SUCCEEDED(hr))
    {
        pFrameDecode->QueryInterface(
            IID_IWICMetadataBlockReader,
            (void**)&pBlockReader);
    }
    if (SUCCEEDED(hr))
    {
        pFrameEncode->QueryInterface(
            IID_IWICMetadataBlockWriter,
            (void**)&pBlockWriter);
    }
    if (SUCCEEDED(hr))
    {
        pBlockWriter->InitializeFromBlockReader(pBlockReader);
    }
}
```



In diesem Beispiel werden der Block Reader und der blockwriter aus dem Quellframe bzw. dem Zielframe abgerufen. Der blockwriter wird dann vom Block Reader initialisiert. Dies initialisiert den Block Reader mit den vorab aufgefüllten Metadaten des Block Readers.

Eine andere Methode zum Kopieren von Metadaten besteht darin, den Metadatenblock zu schreiben, auf den der Abfrage Reader mit dem Abfrage Schreiber des Encoders verweist. Der folgende Code veranschaulicht diese Methode.


```
if (SUCCEEDED(hr) && formatsEqual)
{
    hr = pFrameDecode->GetMetadataQueryReader(&pFrameQReader);

    // Copy metadata using query readers
    if(SUCCEEDED(hr))
    {
        hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
        if (SUCCEEDED(hr))
        {
            PropVariantClear(&value);
            value.vt=VT_UNKNOWN;
            value.punkVal=pFrameQReader;
            value.punkVal->AddRef();
            hr = pFrameQWriter->SetMetadataByName(L"/", &value);
            PropVariantClear(&value);
        }
    }
}
```



Hier wird ein Abfrage Reader aus dem decodierten Frame abgerufen und dann als Eigenschafts Wert der [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) verwendet, wobei ein Werttyp auf VT Unknown festgelegt ist \_ . Der Abfragewriter für den Encoder wird abgerufen, und der Abfrage Ausdruck "/" wird verwendet, um die Metadaten im Stamm Navigationspfad festzulegen. Sie können diese Methode auch verwenden, wenn Sie gruppierten Metadatenblöcke festlegen, indem Sie den Abfrage Ausdruck an den gewünschten Speicherort anpassen.

Auf ähnliche Weise können Sie einen Abfrage-Writer basierend auf dem Abfrage Reader des decodierten Frames erstellen, indem Sie die **Methode "Methode" von "** Image der Abbild Erstellung" verwenden. Der in diesem Vorgang erstellte Abfrage-Writer wird mit den Metadaten aus dem Abfrage Leser aufgefüllt und kann dann im Frame festgelegt werden. Der folgende Code veranschaulicht den Kopiervorgang " **dedeequeryschreiterfromreader** ".


```
IWICMetadataQueryWriter *pNewWriter = NULL;

GUID vendor = GUID_VendorMicrosoft;
hr = pFactory->CreateQueryWriterFromReader(
    pFrameQReader,
    &vendor,
    &pNewWriter);

if (SUCCEEDED(hr))
{
    // Get the frame's query writer
    hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
}

// Set the query writer to the frame.
if (SUCCEEDED(hr))
{
    PROPVARIANT value;

    PropVariantInit(&value);
    value.vt = VT_UNKNOWN;
    value.punkVal = pNewWriter;
    value.punkVal->AddRef();
    hr = pFrameQWriter->SetMetadataByName(L"/",&value);
}
```



Diese Methode verwendet einen separaten Abfrage-Writer, der auf den Daten des Abfrage Readers basiert. Dieser neue Abfragewriter wird dann im Frame festgelegt.

Diese Vorgänge zum Kopieren von Metadaten funktionieren nur, wenn die Quell-und Ziel Images das gleiche Format aufweisen. Dies liegt daran, dass unterschiedliche Bildformate die Metadatenblöcke an verschiedenen Speicherorten speichern. Beispielsweise unterstützen sowohl JPEG als auch TIFF XMP-Metadatenblöcke. In JPEG-Bildern befindet sich der XMP-Block im stammmetadatenblock, wie in der [WIC-Metadatenübersicht](-wic-about-metadata.md)veranschaulicht. In einem TIFF-Bild ist der XMP-Block jedoch in einem IFD-Stammblock eingebettet. Das folgende Diagramm veranschaulicht die Unterschiede zwischen einem JPEG-Bild und einem TIFF-Bild mit denselben Bewertungs Metadaten.

![Vergleich zwischen JPEG und TIFF.](graphics/jpgvstiff.png)

## <a name="fast-metadata-encoding"></a>Schnelle metadatencodierung

Es ist nicht immer erforderlich, ein Bild neu zu codieren, um neue Metadaten zu schreiben. Metadaten können auch mithilfe eines schnellen metadatenencoders geschrieben werden. Ein schneller metadatenencoder kann eine begrenzte Menge an Metadaten in ein Bild schreiben, ohne das Bild neu zu codieren. Dies erfolgt durch das Schreiben der neuen Metadaten innerhalb der leeren Auffüll Zeichen, die von einigen Metadatenformaten bereitgestellt werden. Die nativen Metadatenformate, die die Auffüll Auffüll Vorgänge unterstützen, sind EXIF, IFD, GPS und XMP.

### <a name="adding-padding-to-metadata-blocks"></a>Hinzufügen von Padding zu metadatenblöcken

Bevor Sie eine schnelle metadatencodierung durchführen können, muss im Metadatenblock Platz vorhanden sein, um weitere Metadaten zu schreiben. Wenn nicht genügend Platz innerhalb der vorhandenen Auffüll Zeichen vorhanden ist, um die neuen Metadaten zu schreiben, schlägt die schnelle metadatencodierung fehl. Zum Hinzufügen von metadatenauffüllungen zu einem Bild muss das Bild erneut codiert werden. Sie können Auffüll Zeichen genauso wie jedes andere Metadatenelement hinzufügen, indem Sie einen Abfrage Ausdruck verwenden, wenn der Metadatenblock, den Sie auffüllen, ihn unterstützt. Im folgenden Beispiel wird veranschaulicht, wie einem in einem App1-Block eingebetteten IFD-Block Auffüll Zeichen hinzugefügt werden.


```
if (SUCCEEDED(hr))
{
    // Add metadata padding
    PROPVARIANT padding;

    PropVariantInit(&padding);
    padding.vt = VT_UI4;
    padding.uiVal = 4096; // 4KB

    hr = pFrameQWriter->SetMetadataByName(L"/app1/ifd/PaddingSchema:padding", &padding);

    PropVariantClear(&padding);
}
```



Um Auffüll Zeichen hinzuzufügen, erstellen Sie eine PROPVARIANT vom Typ VT \_ UI4 und einen Wert, der der Anzahl der hinzu zufügenden Bytes von Auffüll Zeichen entspricht. Ein typischer Wert ist 4096 Bytes. Die Metadatenabfragen für JPEG, TIFF und JPEG-XR befinden sich in dieser Tabelle.



| Metadatenformat | JPEG-Metadatenabfrage                  | TIFF, JPEG-XR-Metadatenabfrage    |
|-----------------|--------------------------------------|---------------------------------|
| IFD             | /App1/IFD/PaddingSchema: Padding      | /IFD/PaddingSchema: Padding      |
| EXIF            | /App1/IFD/EXIF/PaddingSchema: Padding | /IFD/EXIF/PaddingSchema: Padding |
| XMP             | /XMP/PaddingSchema: Padding           | /IFD/XMP/PaddingSchema: Padding  |
| GPS             | /App1/IFD/GPS/PaddingSchema: Padding  | /IFD/GPS/PaddingSchema: Padding  |



 

### <a name="obtaining-a-fast-metadata-encoder"></a>Abrufen eines schnellen metadatenencoders

Wenn Sie ein Bild mit metadatenauffüll Zeichen haben, kann ein schneller metadatenencoder mithilfe der Imaging Factory-Methoden **CreateFastMetadataEncoderFromDecoder** und **CreateFastMetadataEncoderFromFrameDecode** abgerufen werden.

Wie der Name schon sagt, erstellt **CreateFastMetadataEncoderFromDecoder** einen schnellen metadatenencoder für Metadaten auf Decoder-Ebene. Die von WIC bereitgestellten systemeigenen Image Formate unterstützen keine Metadaten auf Decoder-Ebene, aber diese Methode wird für den Fall bereitgestellt, dass ein solches Bildformat in der Zukunft entwickelt wird.

Das gängigste Szenario ist das Abrufen eines schnellen metadatenencoders aus einem Bildframe mithilfe von **CreateFastMetadataEncoderFromFrameDecode**. Der folgende Code Ruft den schnellen metadatenencoder eines decodierten Frames ab und ändert den Bewertungs Wert im App1-Block.


```
if (SUCCEEDED(hr))
{
    IWICFastMetadataEncoder *pFME = NULL;
    IWICMetadataQueryWriter *pFMEQW = NULL;

    hr = pFactory->CreateFastMetadataEncoderFromFrameDecode(
        pFrameDecode, 
        &pFME);
}
```



### <a name="using-the-fast-metadata-encoder"></a>Verwenden des schnellen metadatenencoders

Aus dem schnellen metadatenencoder können Sie einen Abfragewriter abrufen. Dies ermöglicht es Ihnen, Metadaten mithilfe eines Abfrage Ausdrucks zu schreiben, wie zuvor gezeigt. Nachdem Metadaten im Abfrage-Writer festgelegt wurden, müssen Sie einen Commit für den schnellen metadatenencoder durchsetzen, um die Metadatenaktualisierung abzuschließen. Der folgende Code veranschaulicht das Festlegen und Ausführen von Änderungen an Metadatenänderungen.


```
    if (SUCCEEDED(hr))
    {
        hr = pFME->GetMetadataQueryWriter(&pFMEQW);
    }

    if (SUCCEEDED(hr))
    {
        // Add additional metadata
        PROPVARIANT value;

        PropVariantInit(&value);

        value.vt = VT_UI4;
        value.uiVal = 99;
        hr = pFMEQW->SetMetadataByName(L"/app1/ifd/{ushort=18249}", &value);

        PropVariantClear(&value);
    }

    if (SUCCEEDED(hr))
    {
        hr = pFME->Commit();
    }
}
```



Wenn **Commit** aus irgendeinem Grund fehlschlägt, müssen Sie das Image erneut codieren, um sicherzustellen, dass die neuen Metadaten dem Image hinzugefügt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Übersicht über WIC-Metadaten](-wic-about-metadata.md)
</dt> <dt>

[Übersicht über die Metadaten-Abfragesprache](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[Übersicht über die metadatenerweiterbarkeit](-wic-codec-metadatahandlers.md)
</dt> <dt>

[Gewusst wie: Erneutes Codieren eines JPEG-Bilds mit Metadaten](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 
