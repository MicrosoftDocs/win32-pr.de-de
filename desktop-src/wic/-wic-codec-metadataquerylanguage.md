---
description: In diesem Thema wird die Metadatenabfragesprache für Windows Imaging Component (WIC) vorgestellt.
ms.assetid: 5ffa0a69-b53d-4be3-b802-deaaa743e6bd
title: Übersicht über die Metadatenabfragesprache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c69effefd288f13c72239a41c5ace1a518775337cc496a2defa864d179cd6cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117668232"
---
# <a name="metadata-query-language-overview"></a>Übersicht über die Metadatenabfragesprache

In diesem Thema wird die Metadatenabfragesprache für Windows Imaging Component (WIC) vorgestellt. Sie verwenden die Metadatenabfragesprache, um Ausdrücke zu erstellen, die bestimmte Daten (Metadatenelemente) und Speicherorte (Metadatenblöcke) in den Metadaten eines Bilds suchen.

Dieses Thema enthält folgende Abschnitte:

-   [Voraussetzungen](#prerequisites)
-   [Introduction (Einführung)](#introduction)
-   [Aufbau eines Pfadausdrucks](#anatomy-of-a-path-expression)
    -   [Block Selection (Blockauswahl)](#block-selection)
    -   [Elementauswahl](#item-selection)
    -   [Escapezeichen](#escape-character)
    -   [Beispielausdrücke](#sample-expressions)
-   [Richtlinienausdrücke für Fotometadaten](#photo-metadata-policy-expressions)
-   [Zusammenfassung der Metadatenabfragesprache](#metadata-query-language-summary)
-   [Zugehörige Themen](#related-topics)

## <a name="prerequisites"></a>Voraussetzungen

Um dieses Thema zu verstehen, sollten Sie mit dem WIC-Metadatensystem wie in der [Übersicht über WIC-Metadaten](-wic-about-metadata.md) beschrieben vertraut sein und auf Metadaten zugreifen, wie in der [Übersicht über das Lesen und Schreiben von Bildmetadaten](-wic-codec-readingwritingmetadata.md)beschrieben.

## <a name="introduction"></a>Einführung

Sie interagieren mit der Metadatenplattform hauptsächlich über zwei Component Object Model -Komponenten (COM): einen Abfrageleser, der durch die [**IWICMetadataQueryReader-Schnittstelle**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) dargestellt wird, und einen Abfragewriter, der durch die [**IWICMetadataQueryWriter-Schnittstelle**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) dargestellt wird. Mit diesen Komponenten können Sie Metadaten mithilfe der Metadatenabfragesprache lesen oder schreiben. Die Abfragesprache beschreibt die Syntax eines Pfadausdrucks, und die Abfragekomponenten verwenden diesen Pfadausdruck, um auf die gewünschten Metadaten zuzugreifen. Dieser Pfadausdruck beschreibt den Speicherort eines Metadatenblocks oder -elements.

Ein Metadatenblock ist eine benannte Gruppe von Metadaten in einem bestimmten Format. Ein Metadatenblock kann einzelne Metadatenelemente wie einen Erstellungszeitpunkt oder zusätzliche Metadatenblöcke enthalten. Der Name eines Metadatenblocks wird durch sein Format bestimmt. Beispielsweise würde ein Metadatenblock, der App1-Metadaten enthält, "app1" heißen. Zu den gängigen Metadatenformaten gehören App1, Exif, IFD und XMP.

Ein Metadatenelement ist ein Name-Wert-Paar, das Merkmale wie Autor, Titel und Bewertung beschreibt.

Ein Pfadausdruck enthält mindestens einen Metadatenblocknamen. Sie kann auch ein Metadatenelement innerhalb eines Metadatenblocks angeben. Der folgende Pfadausdruck stellt einen App1-Block dar, der einen IFD-Block enthält, der das Metadatenelement enthält:

-   /app1/ifd/{ushort=18249}

Das folgende Diagramm veranschaulicht die Darstellung eines JPEG-Beispielbilds mit vier Stammmetadatenblöcken: App0, App1, XMP und einem unbekannten Block. Jedes hervorgehobene Element notiert den Typ der Metadaten (Block oder Element) und den Abfrageausdruck, der zum Abrufen der Daten verwendet wird.

![JPEG-Bild mit Metadatenaufrufen](graphics/jpegwithcallouts.png)

> [!Note]  
> Auf den Inhalt dieses Diagramms wird in diesem Dokument verwiesen und in vielen der Beispiele verwendet.

 

## <a name="anatomy-of-a-path-expression"></a>Aufbau eines Pfadausdrucks

Für den Zugriff auf Metadaten mithilfe der WIC-APIs muss in den meisten Fällen ein vollqualifizierte Abfrageausdruck verwendet werden. In diesem Thema werden vollqualifizierte Ausdrücke für den Zugriff auf Metadaten erläutert. Wenn Sie Informationen zu den Fällen benötigen, in denen nicht vollqualifizierte Ausdrücke verwendet werden, lesen Sie den Abschnitt Fotometadatenrichtlinienausdruck weiter unten in diesem Dokument.

Was ist ein vollqualifizierte Abfrageausdruck? In WIC ist ein vollqualifizierter Ausdruck eine Zeichenfolge, die mit dem Pfadzeichen-Schrägstrich (/) beginnt, gefolgt von einem Navigationspfad zu einem Metadatenblock oder einem bestimmten Metadatenelement. Jeder Schritt innerhalb des Navigationspfads wird durch einen Schrägstrich getrennt und bildet einen Ausdruck für den Zugriff auf einen Metadatenblock oder ein Metadatenelement. Im Folgenden finden Sie beispielsweise einen vollqualifizierten Abfrageausdruck, der in einem IFD-Block, der in einem App1-Block geschachtelt ist, auf Microsoft Photo Rating zugreift:

-   /app1/ifd/{ushort=18249}

Wenn WIC diesen Ausdruck analysiert, wird zunächst in den Metadaten des Bilds nach dem App1-Metadatenblock gesucht. Wenn der App1-Block gefunden wird, wird die Suche nach dem geschachtelten IFD-Metadatenblock fortgesetzt. Wenn der IFD-Block gefunden wird, sucht er innerhalb des IFD-Metadatenblocks nach dem spezifischen Metadatenelement , in diesem Fall nach der MicrosoftPhoto-Bewertung unter dem Tag 18249. Wenn WIC zu einem beliebigen Zeitpunkt keinen Metadatenblock oder kein Metadatenelement findet, wird die Abfrage abgebrochen.

### <a name="block-selection"></a>Blockauswahl

Der einfachste WIC-Metadatenabfrageausdruck ist ein Ausdruck, um einen Abfrageleser/Writer für einen bestimmten Metadatenblock abzurufen. Durch das Abrufen eines Abfragelesers/-writers können Sie nachfolgende Abfragen direkt an einen geschachtelten Metadatenblock leiten, ohne den übergeordneten Block zu verwenden. Ein Blockauswahlabfrageausdruck ist ein Navigationspfad zum gewünschten Metadatenblock. In der vorherigen Abbildung gibt es beispielsweise fünf Metadatenblöcke, von denen zwei in anderen Metadatenblöcken geschachtelt sind. Im FOLGENDEN sind die Pfadausdrücke für jeden Metadatenblock im JPEG-Beispiel beschrieben:

-   /app0
-   /app1
-   /app1/ifd
-   /app1/ifd/exif
-   /xmp

Wenn Sie einen Abfrageleser/-writer zum Ausführen einer Abfrage verwenden, wird ein neuer Abfrageleser/-writer zurückgegeben, der Abfragen innerhalb des Bereichs des angegebenen Metadatenblocks abwickelt. Wenn Sie beispielsweise die Abfrage "/app1" ausführen, wird ein neuer Abfrageleser abgerufen, und Abfragen an den neuen Reader sind relativ zum App1-Block. Dies bedeutet, dass die Abfrage "/ifd" für den neuen Reader gültig ist, da der App1-Block einen IFD-Block enthält. "/xmp" funktioniert jedoch nicht, da dieser App1-Block keinen XMP-Metadatenblock enthält.

Die Abfragesprache unterstützt auch eine Index notation. Die Index notation ermöglicht den Zugriff auf einen bestimmten Metadatenblock, wenn mehrere Blöcke desselben Typs vorhanden sind. Für das JPEG-Beispiel kann der folgende indizierte Pfadausdruck verwendet werden:

-   /\[0 \] \[ app1/0 \] ifd

In der Abfragesprache beginnen alle Indizes bei 0 (null). Im vorherigen Ausdruck fragt die erste Null für den ersten App1-Block und die zweite Null den ersten geschachtelten IFD-Block ab. Die Index notation kann auch dann verwendet werden, wenn nicht mehrere Blöcke desselben Typs vorhanden sind. Wenn das JPEG-Beispiel einen zweiten App1-Block mit einem eingebetteten IFD-Block enthält, wird der Ausdruck "/ \[ 1 \] app1/ifd" verwendet, um auf den zweiten App1-Block zuzugreifen.

Die Index notation wird beim Umgang mit PNG-tEXt-Blöcken häufiger, da es wahrscheinlich ist, dass das PNG-Bild mehr als einen tEXt-Block hat.

> [!Note]  
> Mehrdimensionale Arrayindizes werden nicht unterstützt.

 

### <a name="item-selection"></a>Elementauswahl

Sie können auf die Metadatenelemente in einem Metadatenblock zugreifen, indem Sie auf den Blockauswahlausdrücken aufbauen. Betrachten Sie die Bewertungseigenschaften XMP und Microsoft Photo im JPEG-Beispiel. Diese Metadaten sind in zwei Metadatenblöcken vorhanden: in den Blöcken App1/IFD und XMP. Daher können mehrere Ausdrücke verwendet werden, um auf dieselben Daten zuzugreifen. Der folgende Ausdruck greift auf die MicrosoftPhoto-Bewertung im XMP-Block zu:

-   /xmp/xmp:Rating

Der Teil "xmp:" des Ausdrucks ist ein schemafreundlicher Bezeichner. XMP ist ein erweiterbarer Standard und ermöglicht es Entitäten von Drittanbietern, eigene Schemas zu veröffentlichen, die definieren, wie bestimmte Metadatenelemente gespeichert werden. Ein XMP-Schema wird vollständig durch eine URL identifiziert, aber WIC stellt eine Reihe von benutzerfreundlichen Bezeichnern für bekannte Schemas bereit. Weitere Informationen finden Sie im Thema Native [Image Format Metadata Queries](-wic-native-image-format-metadata-queries.md) .

Bei JPEG-Bildern können Bewertungsinformationen auch im geschachtelten IFD-Block App1 gespeichert werden. Im Gegensatz zum XMP-Bewertungsbeispiel verwendet der IFD-Block jedoch keinen Schemanamen, um auf die Bewertungsinformationen zuzugreifen. Sie verwenden stattdessen einen Datenausdruck. Der folgende Ausdruck wird verwendet, um auf die MicrosoftPhoto-Bewertung im geschachtelten IFD-Block App1 zuzugreifen:

-   /app1/ifd/{ushort=18249}

In diesem Ausdruck ist der Teil "/app1/ifd" des Ausdrucks der Navigationspfad zum IFD-Block (wie zuvor im Abschnitt Blockauswahl erläutert). Der zweite Teil des Ausdrucks "/{ushort=18249}" greift auf die Daten zu. Dieser Teil des Ausdrucks weist den Abfrageparser an, die daten zu suchen, die in das unsigned short-Tag eingebettet sind, das den Tagbezeichner 18249 aufweist.

> [!Note]  
> Eine Liste der gängigen Metadatenformate, die von den einzelnen Bildformaten unterstützt werden, finden Sie im Thema [Native Image Format Metadata Queries](-wic-native-image-format-metadata-queries.md) .

 

{ushort=18249} ist ein Datenausdruck und kann mehrere Formen annehmen. Ein Datenausdruck ist ein zweiteiler Ausdruck, der das angeforderte Metadatentag oder den angeforderten Schlüssel (in diesem Fall "18249" ) und den Datentyp des Schlüssels (in diesem Fall "ushort" ) enthält. Die beiden Teile sind durch ein Gleichheitszeichen (=) getrennt. WIC unterstützt einen Großteil der gängigen C/C++-Datentypen. Die folgenden Datentypen werden von der Abfragesprache akzeptiert:

-   char
-   uchar
-   short
-   ushort
-   long
-   ulong
-   INT
-   uint
-   longlong
-   float
-   double
-   str
-   wstr
-   guid
-   bool

> [!Note]  
> Diese Liste gibt nur die Datentypen an, die von der Metadatenabfragesprache unterstützt werden. Verwenden Sie diese Datentypen, wenn Sie einen Metadatenabfragedatenausdruck wie {ushort=18249} erstellen. Der WIC gibt den Wert des Metadatenelements in Form von PROPVARIANT zurück, das sein eigenes Typsystem definiert.

 

"18249" im Beispiel ist das Datentag. Diese bestimmte Zahl wird von Microsoft so definiert, dass sie die MicrosoftPhoto-Bewertung enthält. Das Datentag kann abhängig vom gesuchten Datenelement eine beliebige Zahl, Zeichenfolge oder GUID sein.

Im Gegensatz zum XMP-Bewertungsbeispiel gibt es keine Namenskonflikte für den Bewertungswert im Block App1/IFD. Dies liegt daran, dass der XMP-Bewertungswert tatsächlich unter einem anderen ushort-Tag (18246) gespeichert wird. Daher lautet der Ausdruck für den Zugriff auf die XMP-Bewertung im App1/IFD-Block:

-   /app1/ifd/{ushort=18246}

> [!Note]  
> Eine formale Beschreibung der Metadatenabfragesprache finden Sie im Abschnitt Metadata Query Language Summary weiter unten in diesem Dokument.

 

### <a name="escape-character"></a>Escape-Zeichen

Bei der Abfragesprache wird die Groß-/Kleinschreibung nicht beachtet, und alle Zeichen werden als Kleinbuchstaben behandelt. Bei einigen Metadatenformaten (z. B. XMP) wird jedoch die Groß-/Kleinschreibung beachtet. Wenn Sie mit einem Metadatenformat mit Beachtung der Groß-/Kleinschreibung arbeiten, verwenden Sie den umgekehrten Schrägstrich \\ (), wenn Sie ein Großbuchstaben angeben möchten.

Das Escapezeichen wird vom Sprachparser verwendet, und das folgende zeichen, das darauf folgt, wird direkt interpretiert. Beispielsweise wird der Ausdruck {char= \\ \\ } als ' ' ' \\ und {char= \\ C} als Großbuchstabe C aufgelöst. Ohne das Escapezeichen wäre {char= \\ } ein ungültiger Ausdruck, und {char=C} würde als Kleinbuchstaben c interpretiert. Achten Sie darauf, den umgekehrten Schrägstrich vor allen Großbuchstaben in Metadatenformaten zu verwenden, bei denen die Groß-/Kleinschreibung beachtet wird.

### <a name="sample-expressions"></a>Beispielausdrücke

Die folgende Tabelle enthält einige Beispielausdrücke und Beschreibungen ihrer Interpretationen durch den Abfragesprachparser. 

| Ausdruck                     | Beschreibung                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ifd/xmp/exif:Author            | Entspricht dem folgenden Navigationspfad: IFD-Block -> XMP-Block -> "Author"-Eigenschaft im Exif-Schema.                                                                                                                                                                                                                                            |
| /\[1 \] \[ ifd/0 \] xmp/exif:Author | Identisch mit dem ersten Element in dieser Tabelle, mit dem Unterschied, dass das \[ \# \] Präfix beschreibt, welches Element bei einem Namenskonflikt navigiert werden soll.                                                                                                                                                                                                                                |
| /ifd/{ushort=700}/Author       | Identisch mit dem ersten Element in dieser Tabelle, mit dem Unterschied, dass ein Datenausdruck verwendet wird, um auf den XMP-Block anstelle des Blocknamens "xmp" zu verweisen (XMP-Block ist unter dem unsignierten Kurztagbezeichner 700 eingebettet). Außerdem gibt die Eigenschaft "Author" kein Schema an. Der Abfrageparser versucht, die -Eigenschaft für alle Schemas abzugleichen und die erste Übereinstimmung zurückzugeben. |
| /ifd/xmp                       | Stellt einen Navigationspfad zu einem Metadatenblock bereit. Wenn der -Block gefunden wird, wird ein neuer Metadatenleser/Writer zurückgegeben.                                                                                                                                                                                                                                                 |
| /\[\*\]tEXt/Keyword            | Ruft die Keyword-Eigenschaft für einen PNG-Block ab oder legt sie fest. Da die PNG-Metadatenspezifikation mehrere Blöcke eines bestimmten Typs zulässt, ruft die \[ \* \] Notation den PNG-Datenabschnitt mit der entsprechenden Eigenschaft ab bzw. legt diese fest. Gemäß der PNG-Spezifikation können keine zwei Blöcke die gleichen Eigenschaften aufweisen.                                                                |



 

Jeder Metadatenblock wird auch durch die Metadaten-GUID eindeutig identifiziert, die anstelle des Anzeigeblocknamens verwendet werden kann. Die folgende Syntax kann anstelle von Blocknamen verwendet werden: "/{guid=GUID}/ \[ n \] {guid=GUID}/schema:tagidentifier"

Die folgende Tabelle enthält einige ungültige Beispiele und die Gründe, warum sie abgelehnt werden. 

| Ungültiger Ausdruck         | Beschreibung der Ablehnung                                                                                                                                                  |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /ifd/ \[ 0 \] \[ 2 \] exif/       | Abgelehnt, da mehrdimensionale Arrayindizes nicht unterstützt werden.                                                                                                    |
| /ifd/{ushort=1}/{ushort=2} | Abgelehnt, es sei denn, die IFD verfügt über eine tagID=1, bei der es sich um einen Metadatenhandler handelt, der ein Metadatenelement mit einer tagID=2 enthält.                                                        |
| /{ushort=1}                | Abgelehnt, wenn die Abfrageverarbeitung relativ zu einer obersten Ebene der Metadatenhierarchie ist. Dies liegt daran, dass die oberste Ebene nur Metadatenblöcke und keine Datenelemente enthält. |



 

## <a name="photo-metadata-policy-expressions"></a>Richtlinienausdrücke für Fotometadaten

Wie bereits erwähnt, beginnt ein vollqualifizierte Abfrageausdruck mit einem Schrägstrich (/). Ausdrücke, die nicht mit dem Schrägstrich beginnen, werden als Richtlinienausdrücke ausgewertet. Mit einem Richtlinienausdruck können Sie die Fotometadaten für bildbezogene Windows [Shelleigenschaften](https://msdn.microsoft.com/library/ms788673(VS.85).aspx)abfragen. Im Abschnitt Datenauswahl weiter oben in diesem Dokument wurde der Ausdruck "/xmp/xmp:Rating" verwendet, um auf die XMP-Bewertungseigenschaft zuzugreifen. Diese Eigenschaft kann auch mit dem folgenden Richtlinienausdruck abgefragt werden:

-   System.SimpleRating

Um über das MicrosoftPhoto-Schema auf die Bewertungseigenschaft zuzugreifen, kann der folgende Abfrageausdruck verwendet werden:

-   System.Rating

Fotometadaten-Richtlinienausdrücke verhalten sich auf einige wichtige Weise anders als vollqualifizierte Metadatenabfragen.

Erstens führt WIC beim Zugriff auf Metadaten mithilfe eines Richtlinienausdrucks eine Vermittlung und Konfliktlösung durch, falls dieselbe Eigenschaft in mehreren Metadatenblöcken verfügbar ist. Beispielsweise werden sowohl die MicrosoftPhoto- als auch die XMP-Bewertungswerte sowohl im App1/IFD-Block als auch im XMP-Block gespeichert. Die Fotometadatenrichtlinie bestimmt die Rangfolge, für die der Blockwert beim Lesen von Metadaten zurückgegeben wird. Wenn Sie Metadaten schreiben, stellt die Richtlinie für Fotometadaten sicher, dass die gleichen Eigenschaften in verschiedenen Blöcken konsistent sind. Wenn Sie eine Metadatenabfrage wie "/xmp/xmp:Rating" verwenden, sind Sie für die Beliebigkeit zwischen den verschiedenen Metadatenspeicherorten verantwortlich.

> [!Note]  
> Eine Liste der unterstützten Richtlinienausdrücke und deren Zuordnungsrichtlinien finden Sie im Thema Richtlinien für [Fotometadaten.](photo-metadata-policies.md)

 

Zweitens sind Fotometadaten-Richtlinienausdrücke unabhängig vom Bildformat, vollqualifizierte Metadatenabfragen hingegen nicht. Beispielsweise ist die Abfrage "/xmp/xmp:Rating" spezifisch für das JPEG-Format. TIFF-Bilder unterstützen auch XMP-Metadaten, werden aber anders als JPEG gespeichert, sodass die TIFF-Abfrage "/ifd/xmp/xmp:Rating" lauten würde. In beiden Fällen wäre der Richtlinienausdruck jedoch "System.SimpleRating".

Fotometadaten-Richtlinienausdrücke bieten im Vergleich zu vollqualifizierten Metadatenabfragen ein höheres Maß an Abstraktion und Einfachheit und sollten daher in Fällen bevorzugt werden, in denen kein Low-Level-Metadatenzugriff erforderlich ist. Richtlinienausdrücke bieten jedoch nur Zugriff auf einen begrenzten Satz von Bildmetadaten, während die Metadatenabfragesprache Zugriff auf fast alle Metadaten bietet, die in einer Bilddatei gespeichert sind.

## <a name="metadata-query-language-summary"></a>Zusammenfassung der Metadatenabfragesprache

Die folgende Tabelle ist eine formale Definition der WIC-Metadatenabfragesprache. Jedes Grammatiksymbol stellt einen Ausdruck dar, der aus anderen Symbolen besteht. Der Ausdruck kann ein anderes Symbol oder eine Sequenz anderer Symbole sein, die durch den vertikalen Balken () getrennt sind und \| eine "oder"-Auswahl angeben. Der gesamte Ausdruck auf der rechten Seite ist eine mögliche Ersetzung für das angegebene Symbol auf der linken Seite. 

| Symbol                   | Ausdruck                                                                                                                                                                  |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \<path>             | \<name> \| '/' \<property path>                                                                                                                                   |
| \<property path>    | \<metadata item> \| \<property path> '/' \<property path>                                                                                                    |
| \<metadata item>    | \<index name> \| \<item name> \| \<schema name> ':' \<item name>                                                                                        |
| \<schema name>      | \<item name>                                                                                                                                                           |
| \<item name>        | \<metadata item> \| <indexed item><index>                                                                                                                  |
| \<indexed item>     | \<item> \| \<implied metadata>\<item>                                                                                                                        |
| \<implied metadata> | "<" \<name> ">"                                                                                                                                                    |
| \<item>             | \<name> \| \<index> \<data> \| \<data>                                                                                                                  |
| \<data>             | '{' \<data type> '=' \<value> '}'                                                                                                                                 |
| \<index>            | '\[' \<number> \| \<star> '\]'                                                                                                                                    |
| \<data type>        | 'char' \| 'uchar' \| 'short' \| 'ushort' \| \| 'long' 'ulong' \| 'int' \| 'uint' \| 'longlong' \| 'ulonglong' \| 'float' \| 'double' \| 'str' \| 'wstr' \| 'guid' \| 'bool' |
| \<data value>       | \<number> \| \<name> \| \<guid>                                                                                                                              |
| \<star>             | '\*'                                                                                                                                                                        |
| \<number>           | number                                                                                                                                                                      |
| \<name>             | Zeichenfolge                                                                                                                                                                      |
| \<guid>             | guid                                                                                                                                                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows Übersicht über Bildverarbeitungskomponenten](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Übersicht über WIC-Metadaten](-wic-about-metadata.md)
</dt> <dt>

[Übersicht über das Lesen und Schreiben von Bildmetadaten](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Übersicht über die Metadatenerweiterbarkeit](-wic-codec-metadatahandlers.md)
</dt> <dt>

[Vorgehensweise: Erneutes Codieren eines JPEG-Bilds mit Metadaten](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 



