---
description: In diesem Thema wird die metadatenabfragensprache für Windows Imaging Component (WIC) vorgestellt.
ms.assetid: 5ffa0a69-b53d-4be3-b802-deaaa743e6bd
title: Übersicht über die Metadaten-Abfragesprache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee4b55bdc7079565f98411e28977d3d8c41e191f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104551868"
---
# <a name="metadata-query-language-overview"></a>Übersicht über die Metadaten-Abfragesprache

In diesem Thema wird die metadatenabfragensprache für Windows Imaging Component (WIC) vorgestellt. Mit der Metadatenabfrage-Sprache können Sie Ausdrücke erstellen, mit denen bestimmte Daten (Metadatenelemente) und Speicherorte (Metadatenblöcke) in den Metadaten eines Bilds gesucht werden.

Dieses Thema enthält folgende Abschnitte:

-   [Voraussetzungen](#prerequisites)
-   [Introduction (Einführung)](#introduction)
-   [Anatomie eines Pfad Ausdrucks](#anatomy-of-a-path-expression)
    -   [Block Selection (Blockauswahl)](#block-selection)
    -   [Elementauswahl](#item-selection)
    -   [Escapezeichen](#escape-character)
    -   [Beispielausdrücke](#sample-expressions)
-   [Richtlinien Ausdrücke für Photo-Metadaten](#photo-metadata-policy-expressions)
-   [Zusammenfassung der Metadaten-Abfragesprache](#metadata-query-language-summary)
-   [Zugehörige Themen](#related-topics)

## <a name="prerequisites"></a>Voraussetzungen

Um dieses Thema zu verstehen, sollten Sie mit dem WIC-Metadatensystem vertraut sein, wie in der [WIC-Metadatenübersicht](-wic-about-metadata.md) beschrieben und auf Metadaten zuzugreifen, wie in der Übersicht über das [Lesen und Schreiben von Bild Metadaten](-wic-codec-readingwritingmetadata.md)beschrieben.

## <a name="introduction"></a>Einführung

Sie interagieren in erster Linie mit der metadatenplattform über zwei Component Object Model Komponenten (com): einen Abfrage Reader, der durch die [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) -Schnittstelle dargestellt wird, und einen Abfrage-Writer, der von der [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) -Schnittstelle dargestellt wird Diese Komponenten ermöglichen es Ihnen, Metadaten mithilfe der Metadaten-Abfragesprache zu lesen oder zu schreiben. Die Abfragesprache beschreibt die Syntax eines Pfad Ausdrucks, und die Abfrage Komponenten verwenden diesen Pfad Ausdruck, um auf die gewünschten Metadaten zuzugreifen. Dieser Pfad Ausdruck beschreibt den Speicherort eines Metadatenblocks oder-Elements.

Ein Metadatenblock ist eine benannte Gruppe von Metadaten in einem bestimmten Format. Ein Metadatenblock kann einzelne Metadatenelemente enthalten, wie z. b. einen Autor oder eine Erstellungszeit und zusätzliche Metadatenblöcke Der Name eines Metadatenblocks wird durch sein Format bestimmt. Beispielsweise würde ein Metadatenblock, der App1-Metadaten enthält, den Namen "App1" haben. Zu den gängigen Metadatenformaten gehören App1, EXIF, IFD und XMP.

Ein Metadatenelement ist ein Name-Wert-Paar, das Merkmale wie Autor, Titel und Bewertung beschreibt.

Ein Pfad Ausdruck enthält einen oder mehrere metadatenblocknamen. Außerdem kann ein Metadatenelement in einem Metadatenblock angegeben werden. Der folgende Pfad Ausdruck stellt einen App1-Block dar, der einen IFD-Block enthält, der das Metadatenelement enthält:

-   /App1/IFD/{ushort = 18249}

Das folgende Diagramm veranschaulicht die Zusammensetzung eines JPEG-Beispiel Bilds mit vier Stamm-metadatenblöcken: App0, App1, XMP und ein unbekannter Block. Jedes markierte Element notiert den Typ der Metadaten (Block oder Element) und den Abfrage Ausdruck, der zum Abrufen der Daten verwendet wird.

![JPEG-Bild mit metadatenaufrufen](graphics/jpegwithcallouts.png)

> [!Note]  
> Der Inhalt dieses Diagramms wird in diesem Dokument referenziert und in vielen der Beispiele verwendet.

 

## <a name="anatomy-of-a-path-expression"></a>Anatomie eines Pfad Ausdrucks

Für den Zugriff auf Metadaten mithilfe der WIC-APIs muss in den meisten Fällen ein voll qualifizierter Abfrage Ausdruck verwendet werden. In diesem Thema werden voll qualifizierte Ausdrücke für den Zugriff auf Metadaten erläutert. Wenn Sie Informationen zu den Fällen benötigen, in denen nicht voll qualifizierte Ausdrücke verwendet werden, lesen Sie den Abschnitt Photo Metadata Policy Expression weiter unten in diesem Dokument.

Was ist ein voll qualifizierter Abfrage Ausdruck? In WIC ist ein voll qualifizierter Ausdruck eine Zeichenfolge, die mit dem Pfad Zeichen Schrägstrich (/) beginnt, gefolgt von einem Navigationspfad zu einem Metadatenblock oder einem bestimmten Metadatenelement. Jeder Schritt innerhalb des Navigations Pfads wird durch einen Schrägstrich getrennt, der einen Ausdruck für den Zugriff auf einen Metadatenblock oder ein Metadatenelement bildet. Im folgenden finden Sie beispielsweise einen voll qualifizierten Abfrage Ausdruck, der auf die Microsoft-Foto Bewertung in einem IFD-Block zugreift, der in einem App1-Block eingebettet ist:

-   /App1/IFD/{ushort = 18249}

Wenn WIC diesen Ausdruck analysiert, sucht er zuerst in den Metadaten des Images nach dem App1-Metadatenblock. Wenn der App1-Block gefunden wird, sucht er bei der Suche nach dem Block der gruppierten IFD-Metadaten. Wenn der IFD-Block gefunden wird, sucht er nach dem jeweiligen Metadatenelement, in diesem Fall die microsoftphoto-Bewertung unter dem Tag 18249 innerhalb des IFD-Metadatenblocks. Wenn WIC einen Metadatenblock oder ein Metadatenblock nicht findet, wird die Abfrage abgebrochen.

### <a name="block-selection"></a>Blockauswahl

Der einfachste WIC-metadatenabfragenausdruck ist ein Ausdruck zum Abrufen eines Abfrage Readers/Writer für einen bestimmten Metadatenblock. Durch das Abrufen eines Abfrage Readers/Writer können Sie nachfolgende Abfragen direkt an einen gruppierten Metadatenblock weiterleiten, ohne dass der zugehörige übergeordnete Block behandelt wird. Bei einem Abfrage Ausdruck für die Blockauswahl handelt es sich um einen Navigationspfad zum gewünschten Metadatenblock. In der vorherigen Abbildung gibt es z. b. fünf Metadatenblöcke, von denen zwei in anderen metadatenblöcken enthalten sind. Im folgenden finden Sie die Pfad Ausdrücke für jeden Metadatenblock im JPEG-Beispiel:

-   /app0
-   /App1
-   /app1/ifd
-   /app1/ifd/exif
-   /xmp

Wenn Sie einen Abfrage Reader/-Writer zum Ausführen einer Abfrage verwenden, wird ein neuer Abfrage-/Schreib-Writer zurückgegeben, der die Dienste innerhalb des Gültigkeits Bereichs des angegebenen Metadatenblocks abfragt. Wenn Sie beispielsweise die Abfrage "/App1" ausführen, wird ein neuer Abfrage Reader abgerufen, und die Abfragen des neuen Readers sind relativ zum App1-Block. Dies bedeutet, dass die Abfrage "/IFD" für den neuen Reader gültig ist, da der App1-Block einen IFD-Block enthält. "/XMP" funktioniert jedoch nicht, weil dieser App1-Block keinen XMP-Metadatenblock enthält.

Die Abfragesprache unterstützt auch eine Index Notation. Die Index Notation ermöglicht den Zugriff auf einen bestimmten Metadatenblock, wenn mehrere Blöcke desselben Typs vorhanden sind. Für das JPEG-Beispiel kann der folgende indizierte Pfad Ausdruck verwendet werden:

-   /\[0 \] App1/ \[ 0 ( \] IFD)

In der Abfragesprache beginnen alle Indizes bei Null. Im vorherigen Ausdruck werden bei den ersten NULL Abfragen für den ersten App1-Block und das zweite NULL-Element der erste getusterte IFD-Block abgefragt. Die Index Notation kann auch dann verwendet werden, wenn nicht mehrere Blöcke desselben Typs vorhanden sind. Wenn das Beispiel JPEG einen zweiten App1-Block mit einem eingebetteten IFD-Block enthielt, wird der Ausdruck "/ \[ 1 \] App1/IFD" für den Zugriff auf den zweiten App1-Block verwendet.

Die Index Notation wird häufiger beim Umgang mit PNG-Text Segmenten verwendet, da es wahrscheinlich ist, dass das PNG-Bild mehr als einen Text Block enthält.

> [!Note]  
> Mehrdimensionale Array Indizes werden nicht unterstützt.

 

### <a name="item-selection"></a>Elementauswahl

Sie können auf die Metadatenelemente in einem Metadatenblock zugreifen, indem Sie auf den Blockauswahl Ausdrücken aufbauen. Beachten Sie die Eigenschaften für die XMP-und Microsoft-Foto Bewertung im JPEG-Beispiel. Diese Metadaten sind in zwei metadatenblöcken vorhanden: die App1/IFD-und XMP-Blöcke. Daher können mehr als ein Ausdruck verwendet werden, um auf dieselben Daten zuzugreifen. Der folgende Ausdruck greift auf die microsoftphoto-Bewertung im XMP-Block zu:

-   /XMP/XMP: Bewertung

Der "XMP:"-Teil des Ausdrucks ist ein Schema Anzeige Bezeichner. XMP ist ein erweiterbarer Standard, mit dem Drittanbieter-Entitäten ihre eigenen Schemas veröffentlichen können, die definieren, wie bestimmte Metadatenelemente gespeichert werden. Ein XMP-Schema ist vollständig durch eine URL gekennzeichnet, aber WIC stellt eine Reihe von benutzerfreundlichen bezeichlen für bekannte Schemas bereit. Weitere Informationen finden Sie im Thema [Native Image Format Metadata Queries](-wic-native-image-format-metadata-queries.md) .

Bei JPEG-Bildern können Bewertungsinformationen auch innerhalb des geschachtelten IFD-Blocks App1 gespeichert werden. Im Gegensatz zum XMP-Bewertungs Beispiel verwendet der IFD-Block jedoch keinen Schema Namen, um auf die Bewertungsinformationen zuzugreifen. Stattdessen verwenden Sie einen Daten Ausdruck. Der folgende Ausdruck wird für den Zugriff auf die microsoftphoto-Bewertung im App1-Block mit dem IFD-Block verwendet:

-   /App1/IFD/{ushort = 18249}

In diesem Ausdruck ist der "/App1/IFD"-Teil des Ausdrucks der Navigationspfad zum IFD-Block (wie bereits im Abschnitt zur Blockauswahl erläutert). Der zweite Teil des Ausdrucks "/{ushort = 18249}" greift auf die Daten zu. Dieser Teil des Ausdrucks weist den Abfrage Parser an, die Daten zu finden, die in das unsignierte Kurztag mit dem Tagbezeichner 18249 eingebettet sind.

> [!Note]  
> Eine Liste der allgemeinen Metadatenformate, die von den einzelnen Bildformaten unter unterstützt werden, finden Sie im Thema [Native Image Format Metadata Queries](-wic-native-image-format-metadata-queries.md) .

 

"{Ushort = 18249}" ist ein Daten Ausdruck und kann verschiedene Formen annehmen. Ein Daten Ausdruck ist ein zwei teilige Ausdruck, der das angeforderte Metadatentag oder den angeforderten Schlüssel, in diesem Fall "18249", und den Datentyp des Schlüssels, in diesem Fall "ushort", enthält. Die beiden Teile sind durch ein Gleichheitszeichen (=) getrennt. Wicunter stützt die Mehrzahl der allgemeinen C/C++-Datentypen. Die folgenden Datentypen werden von der Abfragesprache akzeptiert:

-   char
-   UCHAR
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
-   WSTR
-   guid
-   bool

> [!Note]  
> Diese Liste gibt nur die Datentypen an, die von der Metadaten-Abfragesprache unterstützt werden. Verwenden Sie diese Datentypen, wenn Sie einen Daten Ausdruck für die Metadatenabfrage erstellen, z.b. {ushort = 18249}. Der WIC gibt den Wert des Metadatenelements in Form von PROPVARIANT zurück, das sein eigenes Typsystem definiert.

 

Der Wert "18249" im Beispiel ist das datentag. Diese bestimmte Zahl wird von Microsoft definiert und enthält die microsoftphoto-Bewertung. Das datentag kann eine beliebige Anzahl, Zeichenfolge oder GUID sein, abhängig vom gesuchten Datenelement.

Im Gegensatz zum Beispiel für die XMP-Bewertung gibt es keine Namenskollision für den Bewertungs Wert im App1/IFD-Block. Dies liegt daran, dass der XMP-Bewertungs Wert tatsächlich unter einem anderen ushort-Tag (18246) gespeichert wird. Folglich lautet der Ausdruck für den Zugriff auf die XMP-Bewertung im App1/IFD-Block wie folgt:

-   /App1/IFD/{ushort = 18246}

> [!Note]  
> Eine formale Beschreibung der Metadaten-Abfragesprache finden Sie weiter unten in diesem Dokument im Abschnitt Zusammenfassung der Metadaten-Abfragesprache.

 

### <a name="escape-character"></a>Escape-Zeichen

Bei der Abfragesprache wird die Groß-/Kleinschreibung nicht beachtet, und alle Zeichen werden als Kleinbuchstaben behandelt Bei einigen Metadatenformaten (z. b. XMP) wird die Groß-/Kleinschreibung beachtet. Verwenden Sie beim Arbeiten mit einem Metadatenformat, bei dem die Groß-/Kleinschreibung beachtet wird, den umgekehrten Schrägstrich ( \\ ), wenn Sie einen Großbuchstaben angeben möchten.

Das Escapezeichen wird vom sprach Parser verwendet, und das folgende Zeichen, das darauf folgt, wird direkt interpretiert. Beispielsweise wird der Ausdruck {Char = \\ \\ } als "" aufgelöst, \\ und {Char = \\ C} wird als Großbuchstabe C aufgelöst. Ohne das Escapezeichen wäre {Char = \\ } ein Ungültiger Ausdruck, und {char = c} würde als Kleinbuchstabe c interpretiert werden. Achten Sie darauf, den umgekehrten Schrägstrich vor allen Großbuchstaben in Metadatenformaten zu verwenden, bei denen die Groß-/Kleinschreibung beachtet wird.

### <a name="sample-expressions"></a>Beispielausdrücke

Die folgende Tabelle enthält einige Beispiel Ausdrücke und Beschreibungen ihrer Interpretationen durch den Abfrage sprach Parser. 

| Ausdruck                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IFD/XMP/EXIF: Autor            | Entspricht folgendem Navigationspfad: IFD Block-> XMP Block-> "Author"-Eigenschaft im "EXIF"-Schema.                                                                                                                                                                                                                                            |
| /\[1 \] IFD/ \[ 0 \] XMP/EXIF: Autor | Identisch mit dem ersten Element in dieser Tabelle, mit dem Unterschied, dass das \[ \# \] Präfix beschreibt, welches Element im Falle eines Namens Konflikts navigiert werden soll.                                                                                                                                                                                                                                |
| /IFD/{ushort = 700}/Author       | Identisch mit dem ersten Element in dieser Tabelle, mit dem Unterschied, dass es einen Daten Ausdruck verwendet, um auf den XMP-Block anstelle des Block namens "XMP" zu verweisen (der XMP-Block ist unter den unsignierten kurztagbezeichner 700 eingebettet). Außerdem wird von der Eigenschaft "Author" kein Schema angegeben. Der Abfrage Parser versucht, die Eigenschaft über alle Schemas abzugleichen, und gibt die erste Übereinstimmung zurück. |
| /ifd/xmp                       | Stellt einen Navigationspfad zu einem Metadatenblock bereit. Wenn der-Block gefunden wird, wird ein neuer metadatenleser/Writer zurückgegeben.                                                                                                                                                                                                                                                 |
| /\[\*\]Text/Schlüsselwort            | Ruft die Schlüsselwort Eigenschaft für einen PNG-Block ab oder legt Sie fest. Da die PNG-Metadatenspezifikation mehrere Blöcke eines bestimmten Typs zulässt, ruft die \[ \* \] Notation den Daten PNG-Block mit der entsprechenden-Eigenschaft ab oder legt ihn fest. Gemäß der PNG-Spezifikation können keine zwei Blöcke über die gleichen Eigenschaften verfügen.                                                                |



 

Jeder Metadatenblock wird auch durch die metadatenguid eindeutig identifiziert, die anstelle des anzeigen Amen verwendet werden kann. Die folgende Syntax kann anstelle der Angabe von Blocknamen verwendet werden: "/{GUID = GUID}/ \[ n \] {Guid = Guid}/Schema: tagidentifier"

In der folgenden Tabelle werden einige ungültige Beispiele und die Gründe für die Ablehnung von Beispielen aufgeführt. 

| Ungültiger Ausdruck         | Ablehnungs Beschreibung                                                                                                                                                  |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /IFD/ \[ 0 \] \[ 2 \] EXIF/       | Wurde abgelehnt, da mehrdimensionale Array Indizes nicht unterstützt werden.                                                                                                    |
| /IFD/{ushort = 1}/{ushort = 2} | Wird zurückgewiesen, es sei denn, das IFD hat eine TagID = 1, bei der es sich um einen Metadatenhandler handelt, der ein Metadatenelement mit einer TagID                                                        |
| /{ushort = 1}                | Wird zurückgewiesen, wenn die Abfrage Verarbeitung relativ zu einer obersten Ebene der Metadatenhierarchie ist. Dies liegt daran, dass die oberste Ebene nur Metadatenblöcke und keine Datenelemente enthält. |



 

## <a name="photo-metadata-policy-expressions"></a>Richtlinien Ausdrücke für Photo-Metadaten

Wie bereits erwähnt, beginnt ein voll qualifizierter Abfrage Ausdruck mit einem Schrägstrich (/). Ausdrücke, die nicht mit dem Schrägstrich beginnen, werden als Richtlinien Ausdrücke ausgewertet. Ein Richtlinien Ausdruck ermöglicht es Ihnen, die Foto Metadaten nach Bild bezogenen Windows [Shell-Eigenschaften](https://msdn.microsoft.com/library/ms788673(VS.85).aspx)abzufragen. Im Abschnitt zur Datenauswahl weiter oben in diesem Dokument wurde der Ausdruck "/XMP/XMP: Rating" verwendet, um auf die XMP-Bewertungs Eigenschaft zuzugreifen. Diese Eigenschaft kann auch mit dem folgenden Richtlinien Ausdruck abgefragt werden:

-   System. simplerating

Der folgende Abfrage Ausdruck kann verwendet werden, um über das microsoftphoto-Schema auf die Bewertungs Eigenschaft zuzugreifen:

-   System. Rating

Die Ausdrücke der Foto-metadatenrichtlinie Verhalten sich in einigen Punkten von voll qualifizierten Metadatenabfragen unterschiedlich.

Zuerst führt WIC beim Zugriff auf Metadaten mithilfe eines Richtlinien Ausdrucks eine Schiedsgerichtsbarkeit und Konflikt Auflösung aus, wenn dieselbe Eigenschaft in mehreren metadatenblöcken verfügbar ist. Beispielsweise werden sowohl der microsoftphoto-als auch der XMP-Bewertungs Wert sowohl im App1/IFD-Block als auch im XMP-Block gespeichert. Die fotometadatenrichtlinie bestimmt die Rangfolge, für die beim Lesen von Metadaten der Block Wert zurückgegeben wird. Wenn Sie Metadaten schreiben, stellt die fotometadatenrichtlinie sicher, dass die gleichen Eigenschaften in verschiedenen Blöcken konsistent sind. Wenn Sie eine Metadatenabfrage wie z. b. "/XMP/XMP: Rating" verwenden, sind Sie dafür verantwortlich, zwischen den verschiedenen metadatenstandorten zu suchen.

> [!Note]  
> Eine Liste der unterstützten Richtlinien Ausdrücke und deren Mapping-Richtlinien finden Sie im Thema [Photo Metadata Policies](photo-metadata-policies.md) .

 

Zweitens sind Foto-metadatenrichtlinien Ausdrücke unabhängig vom Bildformat, während voll qualifizierte Metadatenabfragen nicht durchlaufen werden. Beispielsweise ist die Abfrage "/XMP/XMP: Rating" spezifisch für das JPEG-Format. TIFF-Images unterstützen auch XMP-Metadaten, aber Sie werden im Vergleich zu JPEG anders gespeichert, sodass die TIFF-Abfrage "/IFD/XMP/XMP: Rating" lauten würde. In beiden Fällen würde der Richtlinien Ausdruck jedoch "System. simplerating" lauten.

Foto-metadatenrichtlinienausdrücke bieten im Vergleich zu voll qualifizierten Metadatenabfragen ein höheres Maß an Abstraktion und Einfachheit und sollten daher bevorzugt werden, wenn kein Zugriff auf die Metadaten auf niedriger Ebene erforderlich ist. Richtlinien Ausdrücke ermöglichen jedoch nur den Zugriff auf einen begrenzten Satz von Bild Metadaten, während die Metadatenabfrage-Sprache Zugriff auf fast alle in einer Bilddatei gespeicherten Metadaten bietet.

## <a name="metadata-query-language-summary"></a>Zusammenfassung der Metadaten-Abfragesprache

In der folgenden Tabelle ist eine formale Definition der WIC-Metadatenabfragesprache definiert. Jedes Grammatik Symbol stellt einen Ausdruck dar, der aus anderen Symbolen besteht. Der Ausdruck kann ein anderes Symbol oder eine Sequenz von anderen Symbolen sein, die durch den senkrechten Strich ( \| ) getrennt sind, und gibt eine "oder"-Auswahl an. Der gesamte Ausdruck auf der rechten Seite ist eine mögliche Ersetzung für das angegebene Symbol auf der linken Seite. 

| Symbol                   | Ausdruck                                                                                                                                                                  |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \<path>             | \<name> \| '/' \<property path>                                                                                                                                   |
| \<property path>    | \<metadata item> \| \<property path> '/' \<property path>                                                                                                    |
| \<metadata item>    | \<index name> \| \<item name> \| \<schema name> ':' \<item name>                                                                                        |
| \<schema name>      | \<item name>                                                                                                                                                           |
| \<item name>        | \<metadata item> \| <indexed item><index>                                                                                                                  |
| \<indexed item>     | \<item> \| \<implied metadata>\<item>                                                                                                                        |
| \<implied metadata> | ' < ' ' \<name> > '                                                                                                                                                    |
| \<item>             | \<name> \| \<index> \<data> \| \<data>                                                                                                                  |
| \<data>             | '{' \<data type> '=' \<value> '}'                                                                                                                                 |
| \<index>            | '\[' \<number> \| \<star> '\]'                                                                                                                                    |
| \<data type>        | ' char ' \| ' UCHAR ' \| ' Short ' \| ' ushort ' \| ' Long ' \| ' ULONG ' \| ' int ' \| ' uint ' \| ' Longlong ' \| ' ULONGLONG ' \| ' float ' \| ' Double ' \| ' Str ' \| ' WSTR ' ' \| GUID ' \| ' bool ' |
| \<data value>       | \<number> \| \<name> \| \<guid>                                                                                                                              |
| \<star>             | '\*'                                                                                                                                                                        |
| \<number>           | number                                                                                                                                                                      |
| \<name>             | Zeichenfolge                                                                                                                                                                      |
| \<guid>             | guid                                                                                                                                                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Übersicht über WIC-Metadaten](-wic-about-metadata.md)
</dt> <dt>

[Übersicht über das Lesen und Schreiben von Bild Metadaten](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Übersicht über die metadatenerweiterbarkeit](-wic-codec-metadatahandlers.md)
</dt> <dt>

[Gewusst wie: Erneutes Codieren eines JPEG-Bilds mit Metadaten](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 



