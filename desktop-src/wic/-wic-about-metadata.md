---
description: In diesem Thema wird die von der Windows Imaging Component (WIC) bereitgestellte Abbild Erstellung für Metadatenunterstützung eingeführt.
ms.assetid: 35727810-3c4c-4c11-a4a2-3ae2cf3b8142
title: Übersicht über WIC-Metadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f00e3a77eb74a3fb4a00db05ef9e00028f02ecf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104557743"
---
# <a name="wic-metadata-overview"></a>Übersicht über WIC-Metadaten

In diesem Thema wird die von der Windows Imaging Component (WIC) bereitgestellte Abbild Erstellung für Metadatenunterstützung eingeführt. Er bietet eine Einführung in das Lesen und Schreiben von Bild Metadaten, die Metadatenabfragesprache und die Erweiterbarkeit von metadatenhandlern.

Bild Metadaten sind Daten, die in eine Bilddatei eingebettet sind, die zusätzliche Informationen zum Bild bereitstellt, z. b. das Gerät, das zum Erfassen des Bilds oder der Abmessungen des Bilds verwendet wird. Obwohl Sie in der Bilddatei selbst enthalten ist, sind diese Metadaten nicht Teil der Renderingdaten. WIC stellt Schnittstellen bereit, die es Ihnen ermöglichen, diese Metadaten für verschiedene gängige Metadatenformate zu lesen und zu schreiben, z. b. erweiterbare metadatenplattform (XMP), austauschbare Bilddatei (EXIF) und PNG-Textdaten (Text).

Dieses Thema enthält folgende Abschnitte:

-   [Voraussetzungen](#prerequisites)
-   [Introduction (Einführung)](#introduction)
-   [Lesen von Bild Metadaten](#reading-image-metadata)
-   [Schreiben von Bild Metadaten](#writing-image-metadata)
-   [Metadatenerweiterbarkeit](#metadata-extensibility)
-   [Unterstützte Metadatenformate](#supported-metadata-formats)
-   [Metadatenkomponentenübersicht](#metadata-component-summary)
-   [Zugehörige Themen](#related-topics)

## <a name="prerequisites"></a>Voraussetzungen

Um dieses Thema zu verstehen, sollten Sie mit den WIC-Encodern und-decoderschnittstellen und den zugehörigen COM-Komponenten (Related Component Object Model) vertraut sein, wie in der [Übersicht über Windows Imaging Component](-wic-about-windows-imaging-codec.md)beschrieben. Außerdem ist es hilfreich, eine allgemeine Vertrautheit mit einigen der heute verwendeten Abbild Erstellungs Metadatenformate zu haben.

## <a name="introduction"></a>Einführung

Metadaten stellen erweiterte Informationen zu einem Bild bereit. Diese Informationen können auf verschiedene Weise verwendet werden. Ein Image kann Metadaten enthalten, wie z. b. eine Beschreibung, eine Bewertung, kategorietags und Copyright Informationen. Der Zugriff auf die Metadaten erleichtert das Ausführen von Aufgaben wie z. b. Asset Management, Datei Speicherort oder die Bestimmung von Copyright Informationen. Beispielsweise können Sie mit der Windows-Fotogalerie in Windows Vista den Bildern Beschreibungen und kategorietags hinzufügen. Dies ermöglicht eine bessere Auffindbarkeit von Bildern und eine bequeme Möglichkeit zum Kategorisieren von Bildern. Mithilfe der WIC-APIs und der allgemeinen Metadatenformate können Anwendungen diese Art von Metadaten problemlos in oder aus Bildern schreiben oder lesen.

Das folgende Diagramm veranschaulicht den Inhalt einer JPEG-Datei, die eingebettete Metadatenblöcke und Metadatenelemente enthält.

![JPEG-Bild mit Bewertungs Metadaten](graphics/jpeg.png)

In diesem Beispiel Bild werden die Metadaten in die Bilddatei innerhalb eines Bild Rahmens eingebettet. Das JPEG-Format unterstützt nicht mehrere Bild Rahmen, sodass die Metadaten konzeptionell mit diesem einzelnen Frame verknüpft sind. Bei Formaten, die mehrere Frames unterstützen (z. b. TIFF), können Metadaten an jeden Bildframe angefügt werden, wie in diesem Diagramm dargestellt. Obwohl es heute nicht üblich und nicht von den Codecs für Native Images unterstützt wird, können einige Bildformate auch Metadaten außerhalb eines Bild Rahmens unterstützen. WIC ist flexibel genug, um sowohl Metadaten und Metadaten auf Frame-Ebene außerhalb des einzelnen Frames eines Bilds zu verarbeiten.

## <a name="reading-image-metadata"></a>Lesen von Bild Metadaten

Die WIC-APIs stellen COM-Komponenten bereit, die es Anwendungen erleichtern, Bild Metadaten zu lesen und zu schreiben.

Die primäre Methode zum Lesen von Metadaten ist die Verwendung eines Metadatenabfrage-Readers ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) für den Zugriff auf bestimmte Metadatenelemente. Die Komponente für die Metadatenabfrage-Reader wird durch den Codec implementiert, und der Zugriff auf die decoderebene oder über einzelne Bild Rahmen ist die gängigste Methode. Der folgende Code zeigt, wie Sie mithilfe der **GetMetadataQueryReader** -Methode des Abfrage Readers auf einen Abfrage Reader für einen einzelnen Frame zugreifen können.


```
// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}
```



Ein Abfrage Reader stellt Methoden zum Abrufen von Informationen über bestimmte Metadaten und eine Möglichkeit zum Angeben eines abzurufenden Metadatenelements bereit. Im folgenden Code wird ein Abfrage Ausdruck verwendet, um ein bestimmtes Metadatenelement im IFD-Block (App1 geschachteltes Image Dateiverzeichnis) anzufordern. Dies erfolgt mithilfe der **GetMetadataByName** -Methode des Abfrage Readers. Der folgende Code veranschaulicht die Verwendung des Abfrage Readers zum Abrufen des microsoftphoto-Bewertungs Werts.


```
PROPVARIANT value;
PropVariantInit(&value);

LPCWSTR pwzRatingQuery = L"/app1/ifd/{ushort=18249}";

if (SUCCEEDED(hr))
{
    hr = pQueryReader->GetMetadataByName(pwzRatingQuery, &value);
}
```



Die Variable pwzratingquery im vorherigen Beispiel ist die Abfrage Zeichenfolge für den Zugriff auf das Metadatenelement microsoftphoto-Bewertung. Diese Zeichenfolge wird mithilfe der Metadatenabfrage-Sprache erstellt. Um diese Zeichenfolge zu erstellen, sind Kenntnisse über das Metadatenformat und die Metadatenabfrage Sprache erforderlich, um einzelne Metadatenelemente abzurufen. Weitere Informationen zur Metadatenabfragesprache finden Sie in der [Übersicht über die metadatenquery-Sprache](-wic-codec-metadataquerylanguage.md).

Im Hintergrund verwendet ein Abfrage Leser einen metadatenreader ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)), um auf die vom Abfrage Ausdruck beschriebenen Metadaten zuzugreifen. Zusätzlich zur Verwendung eines Abfrage Readers können Sie auch direkt auf einen metadatenreader zugreifen, um Metadaten zu lesen. Sie können einen metadatenleser vom Decoder oder einzelnen Frames abrufen, indem Sie eine [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)-Schnittstelle (Block Reader) Abfragen.

## <a name="writing-image-metadata"></a>Schreiben von Bild Metadaten

Der Prozess zum Schreiben von Metadaten ähnelt der Vorgehensweise zum Lesen, mit der Ausnahme, dass ein Metadatenabfrage-Writer ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) verwendet wird. Die Query Writer-Schnittstelle wird vom Bild Encoder implementiert, und wie im Abfrage Reader erfolgt der Zugriff auf Metadaten sowohl im Encoder als auch in einzelnen Frames (abhängig von der Unterstützung des Bildformats).

Der folgende Code veranschaulicht, wie Sie einen Abfrage-Writer von einem encoderframe abrufen und den zuvor gelesenen Bewertungs Wert entfernen.


```
// Get the frame's query writer
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
}

if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/app1/ifd/{ushort=18249}");
}
```



Eine andere Möglichkeit zum Schreiben von Metadaten ist das schnelle Aktualisieren von Metadaten. Die schnelle metadatencodierung ist eine Möglichkeit zum Schreiben von Bild Metadaten, ohne eine Bilddatei erneut codieren zu müssen. Dies erfolgt durch das Schreiben neuer Metadateninformationen in einen aufgefüllten Bereich des metadatenformats. Der fast Metadata Encoder ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)) wird aus der komponentenfactory abgerufen, basierend auf dem Image Decoder. Der schnelle metadatenencoder erhält dann einen Abfrage-Writer, der zum Schreiben der Metadaten verwendet wird. Schließlich führt der schnelle Encoder einen Commit für die Änderung aus.

Der folgende Code veranschaulicht, wie Sie einen schnellen metadatenencoder abrufen und ihn verwenden, um den Wert für die Erstellung von mikrosoftrating zu schreiben.


```
if (SUCCEEDED(hr))
{
    IWICFastMetadataEncoder *pFME = NULL;
    IWICMetadataQueryWriter *pFMEQW = NULL;

    hr = pFactory->CreateFastMetadataEncoderFromFrameDecode(
        pFrameDecode,
        &pFME);

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



Nicht alle Metadatenformate unterstützen schnelle Metadaten. Informationen dazu, welche nativ unterstützten Formate eine schnelle metadatencodierung unterstützen, finden Sie in der Tabelle im Abschnitt [unterstützte Metadatenformate](#supported-metadata-formats) weiter unten in diesem Dokument.

Im Hintergrund verwendet ein Abfrage Schreiber einen metadatenwriter ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)), um die vom Abfrage Ausdruck beschriebenen Metadaten zu schreiben. Zusätzlich zur Verwendung eines Abfrage Readers können Sie auch direkt auf einen metadatenwriter zugreifen, um Metadaten zu schreiben. Sie können einen metadatenwriter vom Decoder oder einzelnen Frames abrufen, indem Sie Abfragen für eine blockwriter-Schnittstelle ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)) verwenden.

## <a name="metadata-extensibility"></a>Metadatenerweiterbarkeit

Wie bereits erwähnt, stellt WIC mehrere Metadatenhandler bereit, um Metadaten für gängige Metadatenformate zu lesen und zu schreiben. Es gibt jedoch einige Metadatenformate, die nicht nativ unterstützt werden. Daher stellt WIC APIs zum Erstellen zusätzlicher Metadatenhandler bereit, mit denen die Metadatenunterstützung in andere Formate erweitert werden kann.

Um andere Metadatenformate vollständig zu unterstützen, müssen zwei Arten von Handlern entwickelt werden – ein metadatenleser zum Lesen von Metadaten und ein metadatenwriter zum Schreiben von Metadaten. Obwohl diese beiden Handler in der Regel in Paaren für ein bestimmtes Format implementiert werden, ist dies nicht zwingend erforderlich. Es gibt möglicherweise Fälle, in denen nur die Lesefähigkeit oder nur die Schreibfähigkeit erforderlich ist.

Weitere Informationen zur Erweiterbarkeit von Metadaten mithilfe der WIC-APIs finden Sie in der [Übersicht über die metadatenerweiterbarkeit](-wic-codec-metadatahandlers.md).

## <a name="supported-metadata-formats"></a>Unterstützte Metadatenformate

WIC bietet Unterstützung für verschiedene gängige Metadatenformate. In der folgenden Tabelle werden die unterstützten Metadatenformate, ihre Versionen, die Bildformate aufgelistet, die das Metadatenformat unterstützen, und ob das Metadatenformat eine schnelle metadatencodierung unterstützt Weitere Informationen zur schnellen metadatencodierung finden Sie weiter oben in diesem Dokument im Abschnitt [Schreiben von Image Metadaten](#writing-image-metadata) .



| Unterstützte Metadatenformate | Metadatenspezifikations Version | Unterstützung für Bildformate | Unterstützt die schnelle metadatencodierung |
|----------------------------|--------------------------------|----------------------|---------------------------------|
| App0                       | Jspf 1,02                      | JPEG                 | Nein                              |
| App1                       | Jspf 1,02                      | JPEG, TIFF           | Nein                              |
| App13                      | Unbekannt                        | JPEG, TIFF           | Nein                              |
| IFD                        | TIFF 6,0                       | JPEG, TIFF           | Ja                             |
| UNB                        | Unbekannt                        | JPEG, TIFF           | Nein                              |
| EXIF                       | EXIF 2,2                       | JPEG, TIFF           | Ja                             |
| XMP                        | XMP 1,0 (September 2005)            | JPEG, TIFF           | Ja                             |
| GPS                        | EXIF 2,2                       | JPEG, TIFF           | Ja                             |
| IPTC                       | IPTC 4,0                       | JPEG, TIFF           | Ja                             |
| Text                       | PNG 1,2                        | PNG                  | Nein                              |



 

> [!Note]  
> IPTC unterstützt nur dann den Befehl "f", wenn die Blöcke vergrößert werden, da IPTC keine Auffüll Zeichen unterstützt.

 

## <a name="metadata-component-summary"></a>Metadatenkomponentenübersicht

In der folgenden Tabelle werden die WIC-Schnittstellen beschrieben, die Metadaten unterstützen, sowie die entsprechenden Komponenten. Diese Komponenten ermöglichen den Zugriff auf die Metadaten eines Bilds. Weitere Informationen zu diesen Komponenten finden Sie unter Übersicht über die [Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md). 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Komponente</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Bitmap-Decoder (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a>)</td>
<td><ul>
<li>Liest einen Bildstream und erzeugt eine verwendbare Bitmapquelle. Ist einem Containerformat zugeordnet, z. b. Tagged Image File Format (TIFF) oder Joint Photographic Experts Group (JPEG).</li>
<li>Implementiert eine <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> -Schnittstelle, um alle Metadatenblöcke im Datenstrom des Decoders aufzulisten, die sich nicht in einem Frame befinden.</li>
<li>Macht einen Abfrage Reader zum Lesen der Metadaten verfügbar, die dem Bild zugeordnet sind, das sich nicht in einem Frame befindet.</li>
</ul></td>
</tr>
<tr class="even">
<td>Bitmap-Frame-Decodierung (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a>)</td>
<td><ul>
<li>Greift auf einzelne Frames aus dem Bildstream zu, der vom Decoder gespeichert wird.</li>
<li>Implementiert eine <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> -Schnittstelle, um alle Metadatenblöcke im Datenstrom des Frames aufzuzählen.</li>
<li>Macht einen Abfrage Reader zum Lesen der mit dem Frame verknüpften Metadaten mithilfe von Abfrage Ausdrücken verfügbar.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Bitmap-Encoder (<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>iwicbitmapcoder</strong></a>)</td>
<td><ul>
<li>Schreibt eine Bitmap-Quelle in einen Bildstream. Einem Containerformat wie TIFF oder JPEG zugeordnet.</li>
<li>Implementiert eine <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> -Schnittstelle zum Erstellen einer Liste von metadatenblöcken, die in den Datenstream des Encoders geschrieben werden sollen.</li>
<li>Macht mithilfe von Abfrage Ausdrücken einen Abfrage Schreiber zum Schreiben der Metadaten verfügbar, die dem Image zugeordnet sind.</li>
</ul></td>
</tr>
<tr class="even">
<td>Bitma-Frame Codierung (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>iwicbitmapframecocode</strong></a>)</td>
<td><ul>
<li>Erstellt einen Frame, der in den vom Encoder gehaltenen Stream codiert wird.</li>
<li>Implementiert eine <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> -Schnittstelle zum Erstellen einer Liste von metadatenblöcken, die in den Datenstrom des Frames geschrieben werden sollen.</li>
<li>Macht einen Abfrage-Writer zum Schreiben der mit dem Frame verknüpften Metadaten mithilfe von Abfrage Ausdrücken verfügbar.</li>
</ul></td>
</tr>
</tbody>
</table>



 

In der folgenden Tabelle werden die WIC-Metadatenkomponenten beschrieben. Diese Komponenten ermöglichen es Ihnen, die Metadaten in einem Bild zu lesen und zu schreiben, das von den in der vorherigen Tabelle aufgeführten Komponenten verfügbar gemacht wird. 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Komponente</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Metadatenabfrage-Reader (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader"><strong>IWICMetadataQueryReader</strong></a>)</td>
<td><ul>
<li>Nimmt eine Abfrage Zeichenfolge und navigiert die zugrunde liegende Metadatenhierarchie, um Metadaten zu erhalten.</li>
</ul></td>
</tr>
<tr class="even">
<td>Metadatenabfrage-Writer (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter"><strong>IWICMetadataQueryWriter</strong></a>)</td>
<td><ul>
<li>Nimmt eine Abfrage Zeichenfolge und navigiert die zugrunde liegende Metadatenhierarchie, um Metadaten zu erhalten, festzulegen und zu entfernen.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Metadatenblockreader (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a>)</td>
<td><ul>
<li>Verwaltet eine schreibgeschützte Auflistung von <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a> -Objekten am Anfang der Metadatenhierarchie und ermöglicht die Enumeration aller Metadatenblöcke.</li>
<li>Wird von einem Bitmap-Decoder und einem decodierten BitmapFrame implementiert.</li>
<li>Wird von Komponentenentwicklern von Drittanbietern für benutzerdefinierte Codecs implementiert.</li>
</ul></td>
</tr>
<tr class="even">
<td>Metadatenblockwriter (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a>)</td>
<td><ul>
<li>Verwaltet eine Lese-und Schreib Auflistung von <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a> -Objekten am Anfang der Metadatenhierarchie.</li>
<li>Wird von einem Bitmap-Encoder und einem Bitmap-Frame codieren implementiert.</li>
<li>Wird von Komponentenentwicklern von Drittanbietern für benutzerdefinierte Codecs implementiert.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Metadatenleser (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a>)</td>
<td><ul>
<li>Analysiert einen Datenstrom von Metadaten und verwaltet eine schreibgeschützte Auflistung der Metadatenelemente. Zugeordnet mit einem Metadatenformat wie "EXIF", "IFD" und "XMP".</li>
<li>Fungiert als Wörterbuch und gibt einen Wert zurück, wenn ein Format und ein ID-Paar angegeben werden.</li>
<li>Wird von Komponentenentwicklern von Drittanbietern für benutzerdefinierte Metadatentypen implementiert.</li>
</ul></td>
</tr>
<tr class="even">
<td>Metadatenwriter (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a>)</td>
<td><ul>
<li>Analysiert und serialisiert einen Datenstrom von Metadaten und verwaltet eine Lese-/schreibeigenauflistung von Metadatenelementen.</li>
<li>Wird von Komponentenentwicklern von Drittanbietern für benutzerdefinierte Metadatentypen implementiert.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Schneller metadatenencoder<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder"><strong>IWICFastMetadataEncoder</strong></a></td>
<td><ul>
<li>Macht Semantik zum Schreiben in einer Metadatenhierarchie verfügbar, die Metadaten an einem Ort aktualisiert, ohne das Bild neu zu codieren.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Übersicht über die Metadaten-Abfragesprache](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[Übersicht über das Lesen und Schreiben von Bild Metadaten](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Übersicht über die metadatenerweiterbarkeit](-wic-codec-metadatahandlers.md)
</dt> <dt>

[Gewusst wie: Erneutes Codieren eines JPEG-Bilds mit Metadaten](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 



