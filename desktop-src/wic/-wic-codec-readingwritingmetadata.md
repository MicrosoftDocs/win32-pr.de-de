---
description: Dieses Thema bietet eine Übersicht darüber, wie Sie die Windows Imaging Component (WIC)-APIs zum Lesen und Schreiben von Metadaten verwenden können, die in Bilddateien eingebettet sind.
ms.assetid: b1e0b936-a13a-42dd-8470-957ba1d90423
title: Übersicht über das Lesen und Schreiben von Bildmetadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 191ffbe919e09acb153505fd3b43b50453b67708259206bffe66a0322d485a1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088140"
---
# <a name="overview-of-reading-and-writing-image-metadata"></a>Übersicht über das Lesen und Schreiben von Bildmetadaten

Dieses Thema bietet eine Übersicht darüber, wie Sie die Windows Imaging Component (WIC)-APIs zum Lesen und Schreiben von Metadaten verwenden können, die in Bilddateien eingebettet sind.

Dieses Thema enthält folgende Abschnitte:

-   [Voraussetzungen](#prerequisites)
-   [Introduction (Einführung)](#introduction)
-   [Lesen von Metadadaten mithilfe eines Abfragelesers](#reading-metadadata-using-a-query-reader)
    -   [Abrufen eines Abfragelesers](#obtaining-a-query-reader)
    -   [Lesen von Metadaten](#reading-metadata)
    -   [Zusätzliche Methoden für Abfrageleser](#additional-query-reader-methods)
-   [Schreiben von Metadaten mithilfe eines Abfragewriters](#writing-metadata-using-a-query-writer)
    -   [Abrufen eines Abfragewriters](#obtaining-a-query-writer)
    -   [Hinzufügen von Metadaten](#adding-metadata)
    -   [Entfernen von Metadaten](#removing-metadata)
    -   [Kopieren von Metadaten für die erneute Codierung](#copying-metadata-for-re-encoding)
-   [Schnelle Metadatencodierung](#fast-metadata-encoding)
    -   [Hinzufügen von Padding zu Metadatenblöcken](#adding-padding-to-metadata-blocks)
    -   [Abrufen eines schnellen Metadatenencoder](#obtaining-a-fast-metadata-encoder)
    -   [Verwenden des schnellen Metadatenencoder](#using-the-fast-metadata-encoder)
-   [Zugehörige Themen](#related-topics)

## <a name="prerequisites"></a>Voraussetzungen

Um dieses Thema zu verstehen, sollten Sie mit dem WIC-Metadatensystem vertraut sein, wie unter [Übersicht über WIC-Metadaten beschrieben.](-wic-about-metadata.md) Sie sollten auch mit der Abfragesprache vertraut sein, die zum Lesen und Schreiben von Metadaten verwendet wird, wie unter Übersicht über [die Metadatenabfragesprache beschrieben.](-wic-codec-metadataquerylanguage.md)

## <a name="introduction"></a>Einführung

WIC bietet Anwendungsentwicklern Component Object Model (COM)-Komponenten zum Lesen und Schreiben von Metadaten, die in Bilddateien eingebettet sind. Es gibt zwei Möglichkeiten zum Lesen und Schreiben von Metadaten:

-   Verwenden eines Abfragelesers/-writers und eines Abfrageausdrucks zum Abfragen von Metadatenblöcken für geschachtelte Blöcke oder bestimmte Metadaten innerhalb eines Blocks.
-   Verwenden eines Metadatenhandlers (Metadatenleser oder Metadatenwriter) für den Zugriff auf die geschachtelten Metadatenblöcke oder bestimmten Metadaten innerhalb der Metadatenblöcke.

Die einfachste Möglichkeit besteht in der Verwendung eines Abfragelesers/-writers und eines Abfrageausdrucks für den Zugriff auf die Metadaten. Ein Abfrageleser ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) wird verwendet, um Metadaten zu lesen, während ein Abfragewriter ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) zum Schreiben von Metadaten verwendet wird. Beide verwenden einen Abfrageausdruck, um die gewünschten Metadaten zu lesen oder zu schreiben. Im Hintergrund verwendet ein Abfrageleser (und Writer) einen Metadatenhandler, um auf die vom Abfrageausdruck beschriebenen Metadaten zu zugreifen.

Die erweiterte Methode besteht im direkten Zugriff auf die Metadatenhandler. Ein Metadatenhandler wird aus den einzelnen Frames mithilfe eines Blockreaders ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)) oder eines Blockwriters ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)) erhalten. Die beiden verfügbaren Typen von Metadatenhandlern sind der [**Metadatenreader ( IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) und der Metadatenwriter ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)).

Das folgende Diagramm des Inhalts einer JPEG-Bilddatei wird in den Beispielen in diesem Thema verwendet. Das durch dieses Diagramm dargestellte Bild wurde mithilfe von Microsoft Paint; Die Bewertungsmetadaten wurden mithilfe des Fotogalerie von Windows Vista hinzugefügt.

![Abbildung des JPEG-Bilds mit Bewertungsmetadaten](graphics/jpeg.png)

## <a name="reading-metadadata-using-a-query-reader"></a>Lesen von Metadadaten mithilfe eines Abfragelesers

Die einfachste Möglichkeit zum Lesen von Metadaten ist die Verwendung der Abfrageleserschnittstelle [**IWICMetadataQueryReader.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) Mit dem Abfrageleser können Sie Metadatenblöcke und Elemente in Metadatenblöcken mithilfe eines Abfrageausdrucks lesen.

Es gibt drei Möglichkeiten, einen Abfrageleser zu erhalten: über einen Bitmapdecoder ([**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)), über seine einzelnen Frames ([**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)) oder über einen Abfragewriter ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).

### <a name="obtaining-a-query-reader"></a>Abrufen eines Abfragelesers

Der folgende Beispielcode zeigt, wie Sie einen Bitmapdecoder aus der Bildverarbeitungs-Factory abrufen und einen einzelnen Bitmapframe abrufen. Dieser Code führt auch Einrichtungsarbeiten aus, die erforderlich sind, um einen Abfrageleser aus einem decodierten Frame zu erhalten.


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



Der Bitmapdecoder für die test.jpg wird mithilfe der **CreateDecoderFromFilename-Methode** der Imaging Factory ermittelt. Bei dieser Methode wird der vierte Parameter auf den Wert WICDecodeMetadataCacheOnDemand aus der [**WICDecodeOptions-Enumeration**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) festgelegt. Dies weist den Decoder an, die Metadaten zwischenspeichern, wenn die Metadaten benötigt werden. entweder durch Abrufen eines Abfragelesers oder des zugrunde liegenden Metadatenlesers. Mit dieser Option können Sie den Datenstrom in den Metadaten beibehalten, die für die schnelle Metadatencodierung erforderlich sind, und die verlustfreie Decodierung des JPEG-Bilds ermöglichen. Alternativ können Sie den anderen **WICDecodeOptions-Wert** verwenden, WICDecodeMetadataCacheOnLoad, der die eingebetteten Bildmetadaten zwischenspeichert, sobald das Bild geladen wird.

Um den Abfrageleser des Frames zu erhalten, rufen Sie einfach die **GetMetadataQueryReader-Methode** des Frames auf. Der folgende Code veranschaulicht diesen Aufruf.


```
// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}
```



Ebenso kann ein Abfrageleser auch auf Decoderebene erhalten werden. Ein einfacher Aufruf der **GetMetadataQueryReader-Methode** des Decoders ruft den Abfragereader des Decoders ab. Im Gegensatz zum Abfragereader eines Frames liest der Abfrageleser eines Decoders Metadaten für ein Bild, das sich außerhalb der einzelnen Frames befindet. Dieses Szenario ist jedoch nicht üblich, und die nativen Imageformate unterstützen diese Funktion nicht. Die nativen Bildcodecs, die von WIC bereitgestellt werden, lesen und schreiben Metadaten auf Frameebene, auch für Einzelframeformate wie JPEG.

### <a name="reading-metadata"></a>Lesen von Metadaten

Bevor Sie mit dem eigentlichen Lesen von Metadaten arbeiten, sehen Sie sich das folgende Diagramm einer JPEG-Datei an, die eingebettete Metadatenblöcke und tatsächliche abzurufende Daten enthält. Dieses Diagramm enthält Aufrufe für bestimmte Metadatenblöcke und Elemente innerhalb des Bilds, die den Metadatenabfrageausdruck für jeden Block oder jedes Element bereitstellen.

![Abbildung eines JPEG-Bilds mit Metadaten-Rückrufen](graphics/jpegwithcallouts.png)

Um eingebettete Metadatenblöcke oder bestimmte Elemente nach Namen zu abfragen, rufen Sie die **GetMetadataByName-Methode** auf. Diese Methode verwendet einen Abfrageausdruck und eine [PROPVARIANT,](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) in der das Metadatenelement zurückgegeben wird. Der folgende Code fragt einen geschachtelten Metadatenblock ab und konvertiert die vom PROPVARIANT-Wert bereitgestellte [IUnknown-Komponente](/windows/win32/api/unknwn/nn-unknwn-iunknown) in einen Abfragereader, falls gefunden.


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



Der Abfrageausdruck "/app1/ifd" fragen den IFD-Block ab, der im Block App1 geschachtelt ist. Die JPEG-Bilddatei enthält den geschachtelten IFD-Metadatenblock, sodass [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) mit einem Variablentyp (vt) von und einem Zeiger auf eine `VT_UNKNOWN` [IUnknown-Schnittstelle](/windows/win32/api/unknwn/nn-unknwn-iunknown) (val) zurückgegeben wird. Anschließend fragen Sie die IUnknown-Schnittstelle nach einem Abfrageleser ab.

Der folgende Code veranschaulicht eine neue Abfrage, die auf dem neuen Abfragereader relativ zum geschachtelten IFD-Block basiert.


```
if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetMetadataByName(L"/{ushort=18249}", &value);
    PropVariantClear(&value); // Clear value for new query
}
```



Der Abfrageausdruck "/{ushort=18249}" fragt den IFD-Block nach der MicrosoftPhoto-Bewertung ab, die unter dem Tag 18249 eingebettet ist. Der [PROPVARIANT-Wert](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) enthält nun den Werttyp `VT_UI2` und den Datenwert 50.

Es ist jedoch nicht erforderlich, vor dem Abfragen bestimmter Datenwerte einen geschachtelten Block zu erhalten. Anstatt beispielsweise die geschachtelte IFD und dann die MicrosoftPhoto-Bewertung abfragen zu müssen, können Sie stattdessen den Stammmetadatenblock und die im folgenden Code gezeigte Abfrage verwenden, um die gleichen Informationen zu erhalten.


```
if (SUCCEEDED(hr))
{
    hr = pQueryReader->GetMetadataByName(L"/app1/ifd/{ushort=18249}", &value);
    PropVariantClear(&value);
}
```



Zusätzlich zum Abfragen bestimmter Metadatenelemente in einem Metadatenblock können Sie auch alle Metadatenelemente in einem Metadatenblock aufzählen (ohne Metadatenelemente in geschachtelten Metadatenblöcken). Zum Aufzählen der Metadatenelemente im aktuellen Block wird die **GetEnumeration-Methode** des Abfragelesers verwendet. Diese Methode erhält eine **IEnumString-Schnittstelle,** die mit den Metadatenelementen im aktuellen Block aufgefüllt wird. Im folgenden Code werden beispielsweise die XMP-Bewertung und die MicrosoftPhoto-Bewertung für den geschachtelten IFD-Block aufzählt, der zuvor ermittelt wurde.


```
IEnumString *metadataItems = NULL;

if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetEnumerator(&metadataItems);
}
```



Weitere Informationen zum Identifizieren geeigneter Tags für verschiedene Bildformate und Metadatenformate finden Sie unter [Metadatenabfragen im Native Image-Format.](-wic-native-image-format-metadata-queries.md)

### <a name="additional-query-reader-methods"></a>Zusätzliche Methoden für Abfrageleser

Zusätzlich zum Lesen von Metadaten können Sie auch zusätzliche Informationen zum Abfrageleser und Metadaten auf andere Mittel abrufen. Der Abfragereader stellt zwei Methoden zur Verfügung, die Informationen zum Abfragereader bereitstellen: **GetContainerFormat** und **GetLocation.**

Mit dem eingebetteten Abfrageleser können Sie **getContainerFormat** verwenden, um den Typ des Metadatenblocks zu bestimmen, und Sie können **GetLocation** aufrufen, um den Pfad relativ zum Stammmetadatenblock zu erhalten. Der folgende Code fragt den eingebetteten Abfragereader nach seinem Speicherort ab.


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



Der Aufruf von **GetContainerFormat für** den eingebetteten Abfragereader gibt die GUID des IFD-Metadatenformats zurück. Der Aufruf von **GetLocation gibt** den Namespace "/app1/ifd" zurück. mit dem relativen Pfad, von dem aus nachfolgende Abfragen an den neuen Abfrageleser ausgeführt werden. Der vorangehende Code ist natürlich nicht sehr nützlich, veranschaulicht jedoch, wie die **GetLocation-Methode** zum Suchen geschachtelter Metadatenblöcke verwendet wird.

## <a name="writing-metadata-using-a-query-writer"></a>Schreiben von Metadaten mithilfe eines Abfragewriters

> [!Note]  
> Einige der in diesem Abschnitt bereitgestellten Codebeispiele werden nicht im Kontext der tatsächlichen Schritte angezeigt, die zum Schreiben von Metadaten erforderlich sind. Informationen zum Anzeigen der Codebeispiele im Kontext eines funktionierenden Beispiels finden Sie im Tutorial How-to: Re-encode an Image with Metadata (Anleitung: Erneutes Codieren eines Bilds mit Metadaten).

 

Die Hauptkomponente zum Schreiben von Metadaten ist der Abfragewriter ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)). Mit dem Abfragewriter können Sie Metadatenblöcke und -elemente innerhalb eines Metadatenblocks festlegen und entfernen.

Wie der Abfrageleser gibt es drei Möglichkeiten, einen Abfragewriter zu erhalten: über einen Bitmapencoder ([**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)), über seine einzelnen Frames ([**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)) oder über einen schnellen Metadatenencoder ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)).

### <a name="obtaining-a-query-writer"></a>Abrufen eines Abfragewriters

Der gängigste Abfragewriter ist für einen einzelnen Frame einer Bitmap. Dieser Abfragewriter legt die Metadatenblöcke und -elemente eines Bildrahmens fest und entfernt sie. Um den Abfragewriter eines Bildrahmens zu erhalten, rufen Sie die **GetMetadataQueryWriter-Methode** des Frames auf. Der folgende Code veranschaulicht den einfachen Methodenaufruf zum Abrufen des Abfragewriters eines Frames.


```
IWICMetadataQueryWriter &pFrameQWriter = NULL;

//Obtain a query writer from the frame.
hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
```



Ebenso kann ein Abfragewriter auch für die Encoderebene erhalten werden. Ein einfacher Aufruf der **GetMetadataQueryWriter-Methode** des Encoders ruft den Abfragewriter des Encoders ab. Im Gegensatz zum Abfragewriter eines Frames schreibt der Abfragewriter eines Encoders Metadaten für ein Bild außerhalb des einzelnen Frames. Dieses Szenario ist jedoch nicht üblich, und die nativen Imageformate unterstützen diese Funktion nicht. Die nativen Bildcodecs, die von WIC bereitgestellt werden, lesen und schreiben Metadaten auf Frameebene, auch für Singleframeformate wie JPEG.

Sie können einen Abfragewriter auch direkt aus der Imageerstellungsfactory abrufen ([**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)). Es gibt zwei Imaging Factory-Methoden, die einen Abfragewriter zurückgeben: **CreateQueryWriter** und **CreateQueryWriterFromReader.**

**CreateQueryWriter** erstellt einen Abfragewriter für das angegebene Metadatenformat und den angegebenen Anbieter. Mit diesem Abfragewriter können Sie Metadaten für ein bestimmtes Metadatenformat schreiben und dem Bild hinzufügen. Der folgende Code veranschaulicht einen **CreateQueryWriter-Aufruf** zum Erstellen eines XMP-Abfragewriters.


```
IWICMetadataQueryWriter *pXMPWriter = NULL;

// Create XMP block
GUID vendor = GUID_VendorMicrosoft;
hr = pFactory->CreateQueryWriter(
        GUID_MetadataFormatXMP,
        &vendor,
        &pXMPWriter);
```



In diesem Beispiel wird der Anzeigename `GUID_MetadataFormatXMP` als *guidMetadataFormat-Parameter* verwendet. Sie stellt die GUID des XMP-Metadatenformats dar, und der Anbieter stellt den von Microsoft erstellten Handler dar. Alternativ kann **NULL** als *pguidVendor-Parameter* mit den gleichen Ergebnissen übergeben werden, wenn kein anderer XMP-Handler vorhanden ist. Wenn ein benutzerdefinierter XMP-Handler zusammen mit dem nativen XMP-Handler installiert wird, führt die Übergabe von **NULL** für den Anbieter dazu, dass der Abfragewriter mit der niedrigsten GUID zurückgegeben wird.

**CreateQueryWriterFromReader** ähnelt der **CreateQueryWriter-Methode,** mit der Ausnahme, dass der neue Abfragewriter vorab mit den vom Abfrageleser bereitgestellten Daten aufgefüllt wird. Dies ist nützlich, um ein Bild erneut zu codieren, während die vorhandenen Metadaten beibehalten werden, oder um unerwünschte Metadaten zu entfernen. Der folgende Code veranschaulicht einen **CreateQueryWriterFromReader-Aufruf.**


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

Nachdem Sie einen Abfragewriter erhalten haben, können Sie ihn verwenden, um Metadatenblöcke und Elemente hinzuzufügen. Zum Schreiben von Metadaten verwenden Sie die **SetMetadataByName-Methode** des Abfragewriters. **SetMetadataByName** verwendet zwei Parameter: einen Abfrageausdruck (*wzName*) und einen Zeiger auf ein [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) (*pvarValue*). Der Abfrageausdruck definiert den festzulegenden Block oder das Element, während PROPVARIANT den tatsächlich festzulegenden Datenwert bereitstellt.

Im folgenden Beispiel wird veranschaulicht, wie Sie einen Titel mithilfe des XMP-Abfragewriters hinzufügen, der zuvor mit der **CreateQueryWriter-Methode** abgerufen wurde.


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



In diesem Beispiel wird der Werttyp (vt) auf `VT_LPWSTR` festgelegt, was angibt, dass eine Zeichenfolge als Datenwert verwendet wird. Da der Typ des *Werts* eine Zeichenfolge ist, wird *pwszVal* verwendet, um den zu verwendenden Titel festzulegen. **SetMetadataByName** wird dann mit dem Abfrageausdruck "/dc:title" und dem neu festgelegten [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)aufgerufen. Der verwendete Abfrageausdruck gibt an, dass die Title-Eigenschaft im DC-Schema (Digital Camera) festgelegt werden soll. Beachten Sie, dass der Ausdruck nicht "/xmp/dc:title" lautet. Dies liegt daran, dass der Abfragewriter bereits XMP-spezifisch ist und keinen eingebetteten XMP-Block enthält, was "/xmp/dc:title" vorschlagen würde.

Bis zu diesem Zeitpunkt haben Sie einem Bildrahmen keine Metadaten hinzugefügt. Sie haben einfach einen Abfragewriter mit Daten aufgefüllt. Um einem Frame einen Metadatenblock hinzuzufügen, der durch den Abfragewriter dargestellt wird, rufen Sie **erneut SetMetadataByName** auf, indem Sie den Abfragewriter als Wert von [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)verwenden. Dadurch werden die Metadaten im Abfragewriter effektiv in den Bildrahmen kopiert. Der folgende Code veranschaulicht, wie die Metadaten im XMP-Abfragewriter hinzugefügt werden, die zuvor im Stammmetadatenblock eines Frames abgerufen wurden.


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



In diesem Beispiel wird ein Werttyp (vt) von verwendet, der `VT_UNKOWN` einen COM-Schnittstellenwerttyp angibt. Der XMP-Abfragewriter (piXMPWriter) wird dann als Wert von [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)verwendet und fügt mithilfe der AddRef-Methode einen Verweis darauf hinzu. Schließlich wird der XMP-Abfragewriter festgelegt, indem die **SetMetadataByName-Methode** des Frames aufgerufen und der Abfrageausdruck "/" übergeben wird, der den Stammblock und die neu festgelegte PROPVARIANT angibt.

> [!Note]  
> Wenn der Frame bereits den Metadatenblock enthält, den Sie hinzufügen möchten, werden die hinzugefügten Metadaten hinzugefügt und vorhandene Metadaten überschrieben.

 

### <a name="removing-metadata"></a>Entfernen von Metadaten

Mit einem Abfragewriter können Sie auch Metadaten entfernen, indem Sie die **RemoveMetadataByName-Methode** aufrufen. **RemoveMetadataByName** verwendet einen Abfrageausdruck und entfernt ggf. den Metadatenblock oder das Element. Der folgende Code veranschaulicht, wie der zuvor hinzugefügte Titel entfernt wird.


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
> Der Code in diesem Abschnitt ist nur gültig, wenn die Quell- und Zielbildformate identisch sind. Sie können nicht alle Metadaten eines Bilds in einem einzigen Vorgang kopieren, wenn sie in ein anderes Bildformat codieren.

 

Zum Beibehalten von Metadaten während der erneuten Codierung eines Bilds in dasselbe Bildformat stehen Methoden zum Kopieren aller Metadaten in einem einzigen Vorgang zur Verfügung. Jeder dieser Vorgänge folgt einem ähnlichen Muster. legt die Metadaten des decodierten Frames direkt in den neuen Frame fest, der codiert wird.

Die bevorzugte Methode zum Kopieren von Metadaten besteht darin, den Blockwriter des neuen Frames mit dem Blockreader des decodierten Frames zu initialisieren. Der folgende Code veranschaulicht diese Methode.


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



In diesem Beispiel werden der Blockleser und der Blockwriter aus dem Quellframe bzw. zielframe abgerufen. Der Blockwriter wird dann vom Blockreader initialisiert. Dadurch wird der Blockreader mit den vorab aufgefüllten Metadaten des Blockreaders initialisiert.

Eine weitere Methode zum Kopieren von Metadaten ist das Schreiben des Metadatenblocks, auf den der Abfrageleser mithilfe des Abfragewriters des Encoders verweist. Der folgende Code veranschaulicht diese Methode.


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



Hier wird ein Abfrageleser aus dem decodierten Frame abgerufen und dann als Eigenschaftswert von [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) mit einem Werttyp verwendet, der auf VT UNKNOWN festgelegt \_ ist. Der Abfragewriter für den Encoder wird abgerufen, und der Abfrageausdruck "/" wird verwendet, um die Metadaten im Stammnavigationspfad festzulegen. Sie können diese Methode auch verwenden, wenn Sie geschachtelte Metadatenblöcke festlegen, indem Sie den Abfrageausdruck an den gewünschten Speicherort anpassen.

Auf ähnliche Weise können Sie einen Abfragewriter basierend auf dem Abfrageleser des decodierten Frames erstellen, indem Sie die **CreateQueryWriterFromReader-Methode** der Imageerstellungsfactory verwenden. Der in diesem Vorgang erstellte Abfragewriter wird vorab mit den Metadaten des Abfragelesers aufgefüllt und kann dann im Frame festgelegt werden. Der folgende Code veranschaulicht den **Kopiervorgang CreateQueryWriterFromReader.**


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



Diese Methode verwendet einen separaten Abfragewriter, der auf den Daten des Abfragelesers basiert. Dieser neue Abfragewriter wird dann im Frame festgelegt.

Auch hier funktionieren diese Vorgänge zum Kopieren von Metadaten nur, wenn die Quell- und Zielimages das gleiche Format aufweisen. Dies liegt daran, dass die Metadatenblöcke von verschiedenen Bildformaten an unterschiedlichen Speicherorten gespeichert werden. Jpeg und TIFF unterstützen beispielsweise XMP-Metadatenblöcke. In JPEG-Bildern befindet sich der XMP-Block im Stammmetadatenblock, wie in der [Übersicht über WIC-Metadaten](-wic-about-metadata.md)veranschaulicht. In einem TIFF-Image ist der XMP-Block jedoch in einem IFD-Stammblock geschachtelt. Das folgende Diagramm veranschaulicht die Unterschiede zwischen einem JPEG-Bild und einem TIFF-Bild mit den gleichen Bewertungsmetadaten.

![JPEG- und TIFF-Vergleich.](graphics/jpgvstiff.png)

## <a name="fast-metadata-encoding"></a>Schnelle Metadatencodierung

Es ist nicht immer erforderlich, ein Bild neu zu codieren, um neue Metadaten in es zu schreiben. Metadaten können auch mithilfe eines schnellen Metadatenencoders geschrieben werden. Ein schneller Metadatenencoder kann eine begrenzte Menge von Metadaten in ein Bild schreiben, ohne das Bild neu zu codieren. Dies wird erreicht, indem die neuen Metadaten in die leere Auffüllung geschrieben werden, die von einigen Metadatenformaten bereitgestellt wird. Die nativen Metadatenformate, die das Auffüllen von Metadaten unterstützen, sind Exif, IFD, GPS und XMP.

### <a name="adding-padding-to-metadata-blocks"></a>Hinzufügen von Padding zu Metadatenblöcken

Bevor Sie eine schnelle Metadatencodierung durchführen können, muss innerhalb des Metadatenblocks Platz zum Schreiben weiterer Metadaten vorhanden sein. Wenn innerhalb der vorhandenen Auffüllung nicht genügend Platz zum Schreiben der neuen Metadaten vorhanden ist, tritt bei der schnellen Metadatencodierung ein Fehler auf. Um einem Bild Metadatenauffüllung hinzuzufügen, muss das Bild neu codiert werden. Sie können die Auffüllung auf die gleiche Weise wie jedes andere Metadatenelement hinzufügen, indem Sie einen Abfrageausdruck verwenden, wenn der Metadatenblock, den Sie auffüllen, dies unterstützt. Im folgenden Beispiel wird veranschaulicht, wie Sie einem ifd-Block, der in einen App1-Block eingebettet ist, Auffüllung hinzufügen.


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



Um Auffüllung hinzuzufügen, erstellen Sie eine PROPVARIANT vom Typ VT \_ UI4 und einen Wert, der der Anzahl der hinzuzufügenden Bytes der Auffüllung entspricht. Ein typischer Wert ist 4.096 Bytes. Die Metadatenabfragen für JPEG, TIFF und JPEG-XR befinden sich in dieser Tabelle.



| Metadatenformat | JPEG-Metadatenabfrage                  | TIFF, JPEG-XR-Metadatenabfrage    |
|-----------------|--------------------------------------|---------------------------------|
| IFD             | /app1/ifd/PaddingSchema:Padding      | /ifd/PaddingSchema:Padding      |
| Exif            | /app1/ifd/exif/PaddingSchema:Padding | /ifd/exif/PaddingSchema:Padding |
| Xmp             | /xmp/PaddingSchema:Padding           | /ifd/xmp/PaddingSchema:Padding  |
| GPS             | /app1/ifd/gps/PaddingSchema:Padding  | /ifd/gps/PaddingSchema:Padding  |



 

### <a name="obtaining-a-fast-metadata-encoder"></a>Abrufen eines schnellen Metadatenencoders

Wenn Sie über ein Bild mit Metadatenauffüllung verfügen, kann ein schneller Metadatenencoder mithilfe der Imageerstellungsfactorymethoden **CreateFastMetadataEncoderFromDecoder** und **CreateFastMetadataEncoderFromFrameDecode** abgerufen werden.

Wie der Name schon sagt, erstellt **CreateFastMetadataEncoderFromDecoder** einen schnellen Metadatenencoder für Metadaten auf Decoderebene. Die von WIC bereitgestellten nativen Bildformate unterstützen keine Metadaten auf Decoderebene, aber diese Methode wird bereitgestellt, falls ein solches Bildformat in Zukunft entwickelt wird.

Das häufigere Szenario ist das Abrufen eines schnellen Metadatenencoders aus einem Bildrahmen mithilfe von **CreateFastMetadataEncoderFromFrameDecode.** Der folgende Code erhält den schnellen Metadatenencoder eines decodierten Frames und ändert den Bewertungswert im Block App1.


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



### <a name="using-the-fast-metadata-encoder"></a>Verwenden des schnellen Metadatenencoder

Über den schnellen Metadatenencoder können Sie einen Abfragewriter abrufen. Dadurch können Sie Metadaten mithilfe eines Abfrageausdrucks schreiben, wie zuvor gezeigt. Nachdem Metadaten im Abfragewriter festgelegt wurden, commiten Sie den schnellen Metadatenencoder, um das Metadatenupdate zu finalisieren. Der folgende Code veranschaulicht das Festlegen und Committen der Metadatenänderungen.


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



Wenn **commit** aus irgendeinem Grund fehlschlägt, müssen Sie das Image neu codieren, um sicherzustellen, dass dem Image die neuen Metadaten hinzugefügt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows Übersicht über Bildverarbeitungskomponenten](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Übersicht über WIC-Metadaten](-wic-about-metadata.md)
</dt> <dt>

[Übersicht über die Metadatenabfragesprache](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[Übersicht über die Erweiterbarkeit von Metadaten](-wic-codec-metadatahandlers.md)
</dt> <dt>

[How-to: Re-encode a JPEG Image with Metadata](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 
