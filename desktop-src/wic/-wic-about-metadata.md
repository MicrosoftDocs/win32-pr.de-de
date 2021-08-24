---
description: In diesem Thema wird die Unterstützung von Bildverarbeitungsmetadaten beschrieben, die von der Windows Imaging Component (WIC) bereitgestellt wird.
ms.assetid: 35727810-3c4c-4c11-a4a2-3ae2cf3b8142
title: Übersicht über WIC-Metadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80cfeb8afe773d661b0953e509f73be4234f2fbfc0a6b7b1f667815031614a56
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772540"
---
# <a name="wic-metadata-overview"></a>Übersicht über WIC-Metadaten

In diesem Thema wird die Unterstützung von Bildverarbeitungsmetadaten beschrieben, die von der Windows Imaging Component (WIC) bereitgestellt wird. Es bietet eine Einführung in das Lesen und Schreiben von Bildmetadaten, der Metadatenabfragesprache und der Erweiterbarkeit von Metadatenhandlern.

Bildmetadaten sind Daten, die in eine Bilddatei eingebettet sind und zusätzliche Informationen zum Bild bereitstellen, z. B. das Gerät, das zum Erfassen des Bilds verwendet wird, oder die Abmessungen des Bilds. Obwohl sie in der Bilddatei selbst enthalten ist, sind diese Metadaten nicht Teil der Renderingdaten. WIC bietet Schnittstellen, mit denen Sie diese Metadaten für verschiedene gängige Metadatenformate lesen und schreiben können, einschließlich Extensible Metadata Platform (XMP), Exchangeable Image File (EXIF) und Png Textual Data (tEXt).

Dieses Thema enthält folgende Abschnitte:

-   [Voraussetzungen](#prerequisites)
-   [Introduction (Einführung)](#introduction)
-   [Lesen von Bildmetadaten](#reading-image-metadata)
-   [Schreiben von Bildmetadaten](#writing-image-metadata)
-   [Metadatenerweiterbarkeit](#metadata-extensibility)
-   [Unterstützte Metadatenformate](#supported-metadata-formats)
-   [Zusammenfassung der Metadatenkomponente](#metadata-component-summary)
-   [Zugehörige Themen](#related-topics)

## <a name="prerequisites"></a>Voraussetzungen

Um dieses Thema zu verstehen, sollten Sie mit dem WIC-Encoder und den Decoderschnittstellen und den zugehörigen Component Object Model-Komponenten (COM) vertraut sein, wie in der Übersicht über Windows [Imaging-Komponenten beschrieben.](-wic-about-windows-imaging-codec.md) Darüber hinaus ist es hilfreich, sich allgemein mit einigen der heute eingesetzten Bildbearbeitungsmetadatenformate vertraut zu machen.

## <a name="introduction"></a>Einführung

Metadaten stellen erweiterte Informationen zu einem Bild bereit. Diese Informationen können auf verschiedene Weise verwendet werden. Ein Bild kann Metadaten wie Eine Beschreibung, Bewertung, Kategorietags und Copyrightinformationen enthalten. Der Zugriff auf die Metadaten erleichtert das Ausführen von Aufgaben wie Ressourcenverwaltung, Dateispeicherort oder Ermittlung von Copyrightinformationen. Mit dem Windows Fotogalerie in Windows Vista können Sie z. B. Bildbeschreibungen und Kategorietags hinzufügen. Dies ermöglicht eine bessere Aufholbarkeit von Bildern und eine bequeme Möglichkeit, Bilder zu kategorisieren. Mithilfe der WIC-APIs und gängiger Metadatenformate können Anwendungen diese Art von Metadaten problemlos in Oder aus Bildern schreiben oder lesen.

Das folgende Diagramm veranschaulicht den Inhalt einer JPEG-Datei, die eingebettete Metadatenblöcke und Metadatenelemente enthält.

![JPEG-Bild mit Bewertungsmetadaten](graphics/jpeg.png)

In diesem Beispielbild werden die Metadaten in die Bilddatei in einem Bildrahmen eingebettet. Das JPEG-Format unterstützt nicht mehrere Bildrahmen, sodass die Metadaten konzeptionell an diesen einzelnen Frame angefügt werden. Formaten, die mehrere Frames unterstützen, z. B. TIFF, können Metadaten an jeden Bildrahmen angefügt werden, wie in diesem Diagramm dargestellt. Obwohl dies derzeit nicht üblich ist und von den nativen Bildcodecs nicht unterstützt wird, unterstützen einige Bildformate möglicherweise auch Metadaten außerhalb eines Bildrahmens. WIC ist flexibel genug, um Metadaten auf Frameebene und Metadaten außerhalb des einzelnen Bildrahmens zu verarbeiten.

## <a name="reading-image-metadata"></a>Lesen von Bildmetadaten

Die WIC-APIs stellen COM-Komponenten bereit, die anwendungen das Lesen und Schreiben von Bildmetadaten ermöglichen.

Die primäre Möglichkeit zum Lesen von Metadaten besteht darin, einen [**Metadatenabfrageleser (IWICMetadataQueryReader) für**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)den Zugriff auf bestimmte Metadatenelemente zu verwenden. Die Metadatenabfrageleser-Komponente wird vom Codec implementiert und kann auf Decoderebene oder über einzelne Bildframes aufgerufen werden. Dies ist die gängigere Methode. Der folgende Code veranschaulicht den Zugriff auf einen Abfragereader für einen einzelnen Frame mithilfe der **GetMetadataQueryReader-Methode** des Abfragelesers.


```
// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}
```



Ein Abfrageleser stellt Methoden zum Abrufen von Informationen zu bestimmten Metadaten und eine Möglichkeit zum Angeben eines abzurufenden Metadatenelements bereit. Im folgenden Code wird ein Abfrageausdruck verwendet, um ein bestimmtes Metadatenelement innerhalb des IFD-Blocks (App1 Nested Image File Directory) an fordern. Dies erfolgt mithilfe der **GetMetadataByName-Methode** des Abfragelesers. Der folgende Code veranschaulicht die Verwendung des Abfragereaders zum Abrufen des MicrosoftPhoto-Bewertungswerts.


```
PROPVARIANT value;
PropVariantInit(&value);

LPCWSTR pwzRatingQuery = L"/app1/ifd/{ushort=18249}";

if (SUCCEEDED(hr))
{
    hr = pQueryReader->GetMetadataByName(pwzRatingQuery, &value);
}
```



Die pwzRatingQuery-Variable im vorherigen Beispiel ist die Abfragezeichenfolge für den Zugriff auf das Metadatenelement MicrosoftPhoto rating. Diese Zeichenfolge wird mithilfe der Metadatenabfragesprache erstellt. Zum Erstellen dieser Zeichenfolge sind Kenntnisse des Metadatenformats und der Metadatenabfragesprache erforderlich, um einzelne Metadatenelemente abzurufen. Weitere Informationen zur Abfragesprache für Metadaten finden Sie unter Übersicht über [die Metadatenabfragesprache.](-wic-codec-metadataquerylanguage.md)

Im Hintergrund verwendet ein Abfrageleser einen Metadatenleser ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)), um auf die vom Abfrageausdruck beschriebenen Metadaten zu zugreifen. Zusätzlich zur Verwendung eines Abfragelesers können Sie auch direkt auf einen Metadatenleser zugreifen, um Metadaten zu lesen. Sie können einen Metadatenleser aus dem Decoder oder einzelnen Frames abrufen, indem Sie eine [**Blockleserschnittstelle (IWICMetadataBlockReader)**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)abfragen.

## <a name="writing-image-metadata"></a>Schreiben von Bildmetadaten

Das Schreiben von Metadaten ähnelt der Art und Weise, wie sie gelesen wird, mit der Ausnahme, dass ein Metadatenabfragewriter ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) verwendet wird. Die Schnittstelle des Abfragewriters wird vom Bildencoder implementiert, und wie beim Abfrageleser erfolgt der Zugriff auf Metadaten sowohl für den Encoder als auch für einzelne Frames (abhängig von der Bildformatunterstützung).

Der folgende Code veranschaulicht, wie sie einen Abfragewriter aus einem Encoderframe abrufen und den zuvor gelesenen Bewertungswert entfernen.


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



Eine weitere Möglichkeit zum Schreiben von Metadaten besteht in schnellen Metadatenaktualisierungen. Die schnelle Metadatencodierung ist eine Möglichkeit, Bildmetadaten zu schreiben, ohne eine Bilddatei erneut codieren zu müssen. Dies erfolgt, indem neue Metadateninformationen in einen aufschlossenen Bereich des Metadatenformats geschrieben werden. Der schnelle Metadatenencoder ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)) wird basierend auf dem Bilddecoder aus der Komponenten-Factory erhalten. Der schnelle Metadatenencoder erhält dann einen Abfragewriter, der zum Schreiben der Metadaten verwendet wird. Schließlich committ der schnelle Encoder die Änderung.

Der folgende Code veranschaulicht, wie Sie einen schnellen Metadatenencoder abrufen und zum Schreiben des MicrosoftRating-Werts verwenden.


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



Nicht alle Metadatenformate unterstützen schnelle Metadaten. Informationen dazu, welche nativ unterstützten Formate eine schnelle Metadatencodierung unterstützen, finden Sie in der Tabelle im Abschnitt [Unterstützte Metadatenformate](#supported-metadata-formats) weiter unten in diesem Dokument.

Im Hintergrund verwendet ein Abfragewriter einen [**Metadatenwriter (IWICMetadataWriter),**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)um die vom Abfrageausdruck beschriebenen Metadaten zu schreiben. Zusätzlich zur Verwendung eines Abfragelesers können Sie auch direkt auf einen Metadatenwriter zugreifen, um Metadaten zu schreiben. Sie können einen Metadatenwriter aus dem Decoder oder einzelnen Frames abrufen, indem Sie eine Blockwriter-Schnittstelle [**(IWICMetadataBlockWriter)**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)abfragen.

## <a name="metadata-extensibility"></a>Metadatenerweiterbarkeit

Wie bereits erwähnt, stellt WIC mehrere Metadatenhandler zum Lesen und Schreiben von Metadaten für gängige Metadatenformate bereit. Es gibt jedoch einige Metadatenformate, die nicht nativ unterstützt werden. Daher bietet WIC APIs zum Erstellen zusätzlicher Metadatenhandler, die die Metadatenunterstützung auf andere Formate erweitern können.

Zur vollständigen Unterstützung anderer Metadatenformate müssen zwei Arten von Handlern entwickelt werden: ein Metadatenleser zum Lesen von Metadaten und ein Metadatenwriter zum Schreiben von Metadaten. Obwohl diese beiden Handler in der Regel paarweise für ein bestimmtes Format implementiert werden, ist dies nicht erforderlich. Es kann fälle geben, in denen nur die Lese- oder nur die Schreibfähigkeit benötigt wird.

Weitere Informationen zur Erweiterbarkeit von Metadaten mithilfe der WIC-APIs finden Sie in der Übersicht über [die Metadatenerweiterbarkeit.](-wic-codec-metadatahandlers.md)

## <a name="supported-metadata-formats"></a>Unterstützte Metadatenformate

WIC bietet Unterstützung für mehrere gängige Metadatenformate. Die folgende Tabelle enthält die unterstützten Metadatenformate, deren Versionen, die Bildformate, die das Metadatenformat unterstützen, und ob das Metadatenformat eine schnelle Metadatencodierung unterstützt. Weitere Informationen zur schnellen Metadatencodierung finden Sie im Abschnitt [Schreiben von Bildmetadaten](#writing-image-metadata) weiter oben in diesem Dokument.



| Unterstützte Metadatenformate | Metadatenspezifikationsversion | Bildformatunterstützung | Unterstützt die schnelle Metadatencodierung. |
|----------------------------|--------------------------------|----------------------|---------------------------------|
| App0                       | JFIF 1.02                      | JPEG                 | Nein                              |
| App1                       | JFIF 1.02                      | JPEG, TIFF           | Nein                              |
| App13                      | Unbekannt                        | JPEG, TIFF           | Nein                              |
| IFD                        | TIFF 6.0                       | JPEG, TIFF           | Ja                             |
| Irb1                        | Unbekannt                        | JPEG, TIFF           | Nein                              |
| EXIF                       | Exif 2.2                       | JPEG, TIFF           | Ja                             |
| Xmp                        | XMP 1.0 (September 2005)            | JPEG, TIFF           | Ja                             |
| GPS                        | Exif 2.2                       | JPEG, TIFF           | Ja                             |
| Iptc                       | IPTC 4.0                       | JPEG, TIFF           | Ja                             |
| Text                       | PNG 1.2                        | PNG                  | Nein                              |



 

> [!Note]  
> IPTC unterstützt FME nur, wenn die Blöcke größer werden, da IPTC keine Auf padding unterstützt.

 

## <a name="metadata-component-summary"></a>Zusammenfassung der Metadatenkomponente

In der folgenden Tabelle werden die WIC-Schnittstellen, die Metadaten unterstützen, und die entsprechenden Komponenten beschrieben. Diese Komponenten ermöglichen den Zugriff auf die Metadaten eines Images. Weitere Informationen zu diesen Komponenten finden Sie unter Windows Imaging Component Overview ( Übersicht [über Bildverarbeitungskomponenten).](-wic-about-windows-imaging-codec.md) 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Komponente</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Bitmap-Decoder (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a>)</td>
<td><ul>
<li>Liest einen Bilddatenstrom und erzeugt eine nutzbare Bitmapquelle. Zugeordnet mit einem Containerformat wie Tagged Image File Format (TIFF) oder Joint Photographic Experts Group (JPEG).</li>
<li>Implementiert eine <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader-Schnittstelle,</strong></a> um alle Metadatenblöcke im Datenstrom des Decoders aufzählen zu können, die sich nicht in einem Frame befinden.</li>
<li>Macht einen Abfrageleser verfügbar, um die Metadaten zu lesen, die dem Bild zugeordnet sind, das sich nicht in einem Frame befindet.</li>
</ul></td>
</tr>
<tr class="even">
<td>Bitmapframe-Decodierung (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a>)</td>
<td><ul>
<li>Greifen Sie auf einzelne Frames aus dem Bildstream zu, der vom Decoder gehalten wird.</li>
<li>Implementiert eine <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader-Schnittstelle,</strong></a> um alle Metadatenblöcke im Datenstrom des Frames aufzählen zu können.</li>
<li>Macht einen Abfrageleser verfügbar, um die dem Frame zugeordneten Metadaten mithilfe von Abfrageausdrücken zu lesen.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Bitmap-Encoder (<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a>)</td>
<td><ul>
<li>Schreibt eine Bitmapquelle in einen Bildstream. Ist einem Containerformat wie TIFF oder JPEG zugeordnet.</li>
<li>Implementiert eine <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter-Schnittstelle,</strong></a> um eine Liste von Metadatenblöcken zu erstellen, die in den Datenstrom des Encoders geschrieben werden.</li>
<li>Macht einen Abfragewriter verfügbar, um die dem Bild zugeordneten Metadaten mithilfe von Abfrageausdrücken zu schreiben.</li>
</ul></td>
</tr>
<tr class="even">
<td>Bitma Frame Encode (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a>)</td>
<td><ul>
<li>Erstellt einen Frame, der in den Stream codiert wird, der vom Encoder gehalten wird.</li>
<li>Implementiert eine <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter-Schnittstelle,</strong></a> um eine Liste von Metadatenblöcken zu erstellen, die in den Datenstrom des Frames geschrieben werden.</li>
<li>Macht einen Abfragewriter verfügbar, um die dem Frame zugeordneten Metadaten mithilfe von Abfrageausdrücken zu schreiben.</li>
</ul></td>
</tr>
</tbody>
</table>



 

In der folgenden Tabelle werden die WIC-Metadatenkomponenten beschrieben. Mit diesen Komponenten können Sie die Metadaten in einem Bild lesen und schreiben, das von den in der vorherigen Tabelle aufgeführten Komponenten verfügbar gemacht wird. 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Komponente</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Metadata Query Reader (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader"><strong>IWICMetadataQueryReader</strong></a>)</td>
<td><ul>
<li>Verwendet eine Abfragezeichenfolge und navigiert durch die zugrunde liegende Metadatenhierarchie, um Metadaten zu erhalten.</li>
</ul></td>
</tr>
<tr class="even">
<td>Metadata Query Writer (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter"><strong>IWICMetadataQueryWriter</strong></a>)</td>
<td><ul>
<li>Verwendet eine Abfragezeichenfolge und navigiert in der zugrunde liegenden Metadatenhierarchie zum Abrufen, Festlegen und Entfernen von Metadaten.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Metadata Block Reader (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a>)</td>
<td><ul>
<li>Verwaltet eine schreibgeschützte Auflistung von <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader-Objekten</strong></a> am Anfang der Metadatenhierarchie und ermöglicht die Enumeration aller Metadatenblöcke.</li>
<li>Wird von einem Bitmapdecoder und einem decodierten Bitmapframe implementiert.</li>
<li>Wird von Komponentenentwicklern von Drittanbietern für benutzerdefinierte Codecs implementiert.</li>
</ul></td>
</tr>
<tr class="even">
<td>Metadata Block Writer (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a>)</td>
<td><ul>
<li>Verwaltet eine Lese- und Schreibsammlung <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>von IWICMetadataWriter-Objekten</strong></a> am Anfang der Metadatenhierarchie.</li>
<li>Wird von einem Bitmapencoder und einer Bitmapframecodierung implementiert.</li>
<li>Wird von Komponentenentwicklern von Drittanbietern für benutzerdefinierte Codecs implementiert.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Metadatenleser (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a>)</td>
<td><ul>
<li>Analysiert einen Datenstrom von Metadaten und verwaltet eine schreibgeschützte Auflistung der Metadatenelemente. Wird einem Metadatenformat wie EXIF, IFD und XMP zugeordnet.</li>
<li>Fungiert als Wörterbuch und gibt einen Wert zurück, wenn ein Format- und ID-Paar angegeben wird.</li>
<li>Wird von Komponentenentwicklern von Drittanbietern für benutzerdefinierte Metadatentypen implementiert.</li>
</ul></td>
</tr>
<tr class="even">
<td>Metadata Writer (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a>)</td>
<td><ul>
<li>Analysiert und serialisiert einen Datenstrom von Metadaten und verwaltet eine Lese-/Schreibsammlung von Metadatenelementen.</li>
<li>Wird von Komponentenentwicklern von Drittanbietern für benutzerdefinierte Metadatentypen implementiert.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Fast Metadata Encoder<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder"><strong>IWICFastMetadataEncoder</strong></a></td>
<td><ul>
<li>Macht Semantik für das Schreiben in eine Metadatenhierarchie verfügbar, die Metadaten aktualisiert, ohne das Bild neu zu codieren.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows Übersicht über Bildverarbeitungskomponenten](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Übersicht über die Metadatenabfragesprache](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[Übersicht über das Lesen und Schreiben von Bildmetadaten](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Übersicht über die Erweiterbarkeit von Metadaten](-wic-codec-metadatahandlers.md)
</dt> <dt>

[How-to: Re-encode a JPEG Image with Metadata](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 



