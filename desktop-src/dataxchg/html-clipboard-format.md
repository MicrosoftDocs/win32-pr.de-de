---
title: HTML-Zwischenablageformat
description: In diesem Abschnitt wird das HTML-Format der Zwischenablage erläutert.
ms.assetid: e891393f-234f-4c94-b581-c4e5f885d2ab
keywords:
- Windows Benutzeroberfläche, Zwischenablage
- Zwischenablage, Datenschneiden
- Zwischenablage,Kopieren von Daten
- Zwischenablage,Einfügen von Daten
- Zwischenablage, Formate
- Zwischenablage, HTML-Format
- Zwischenablage, Ausschneiden von HTML-Text
- Zwischenablage, Einfügen von HTML-Text
- CF_HTML Format der Zwischenablage
- Zwischenablage,CF_HTML Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cafeb80c790ac511b3ffcd750ea4fbfafceeb7fb919842bb12a696b9655ab6ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118811657"
---
# <a name="html-clipboard-format"></a>HTML-Zwischenablageformat

Die Anforderungen für die Übertragung von HTML-Text über die Zwischenablage unterscheiden sich je nach Szenario. In diesem Artikel geht es um das Ausschneiden und Einfügen von Fragmenten eines HTML-Dokuments. Möglicherweise müssen ganze HTML-Dokumente über die Zwischenablage übertragen werden. dieser Artikel basiert jedoch auf der Anforderung, Fragmente von ausgewähltem HTML-Text zu übertragen. Daher wird eine Methode, bei der das gesamte HTML-Dokument in die Zwischenablage kopiert werden musste, als zu schwer angesehen.

Das CF \_ HTML-Zwischenablageformat ermöglicht das Speichern eines Unformatierten HTML-Texts und seines Kontexts in der Zwischenablage als ASCII. Dadurch kann der Kontext des HTML-Fragments, das aus allen vorangehenden umgebenden Tags besteht, von einer Anwendung untersucht werden, sodass die umgebenden Tags des HTML-Fragments mit ihren Attributen notiert werden können. Obwohl es an Anwendungen liegt, zu entscheiden, wie solche Fragmente interpretiert werden sollen, sind hier einige grundlegende Richtlinien basierend auf IE4-/MSHTML-Implementierungen enthalten.

Der offizielle Name der Zwischenablage (die von RegisterClipboardFormat verwendete Zeichenfolge) lautet HTML-Format.

-   [Beschreibung](#description)
-   [Szenarios](#scenarios)

## <a name="description"></a>BESCHREIBUNG

CF \_ HTML ist vollständig textformat (z.B. im HTML-Format und verwendet UTF-8) und enthält ein , ein `description` optionales und im Kontext das `context` `fragment` .

Im Folgenden sehen Sie ein Beispiel für eine Zwischenablage:


```
Version:0.9
    StartHTML:71
    EndHTML:170
    StartFragment:140
    EndFragment:160
    StartSelection:140
    EndSelection:160
    <!DOCTYPE>
    <HTML>
    <HEAD>
    <TITLE> The HTML Clipboard</TITLE>
    <BASE HREF="https://sample/specs">
    </HEAD>
    <BODY>
    <UL>
    <!--StartFragment -->
    <LI> The Fragment </LI>
    <!--EndFragment -->
    </UL>
    </BODY>
    </HTML>
```



Die Beschreibung enthält die Versionsnummer und Offsets der Zwischenablage, die angeben, wo der Kontext und das Fragment beginnen und enden. Bei der Beschreibung handelt es sich um eine Liste von ASCII-Textschlüsselwörtern (min/soll nicht sinnvoll), gefolgt von einer Zeichenfolge und getrennt durch einen Doppelpunkt (:).

**Version:** Versionsnummer der Zwischenablage. Ab Version 0.9.

**StartHTML:** Bytecount vom Anfang der Zwischenablage bis zum Anfang des Kontexts oder -1, wenn kein Kontext vorhanden ist.

**EndHTML:** Bytecount vom Anfang der Zwischenablage bis zum Ende des Kontexts oder -1, wenn kein Kontext vorhanden ist.

**StartFragment:** Bytecount vom Anfang der Zwischenablage bis zum Anfang des Fragments.

**EndFragment:** Bytecount vom Anfang der Zwischenablage bis zum Ende des Fragments.

**StartSelection:** Bytecount vom Anfang der Zwischenablage bis zum Anfang der Auswahl.

**EndSelection:** bytecount vom Anfang der Zwischenablage bis zum Ende der Auswahl.

Die Schlüsselwörter StartSelection und EndSelection sind optional und müssen beide ausgelassen werden, wenn die Anwendung diese Informationen nicht generieren soll.

Weitere Informationen dieser Art können hier später hinzugefügt werden, da der HTML-Code am StartHTMLoffset beginnt. Beispielsweise können später mehrere Paare von StartFragment/EndFragment hinzugefügt werden, um die nicht zusammenhängende Auswahl von Fragmenten zu unterstützen.

Zur Vereinfachung der Programme, die die Byteanzahlen generieren, können Bytecounts durch Nullen aufgefüllt werden. Beispielsweise können Programme, die die Bytecounts generieren, willkürlich zehn (10) Nullen für jedes Schlüsselwort (StartHTML: 0000000000) beeinflussen. Wenn dann der genaue StartHTML-Bytecount bekannt ist (z. B. 71), kann das Programm die entsprechende Anzahl von Nullen durch das Bytecount (StartHTML: 0000000071) ersetzen.

Der einzige Zeichensatz, der von der Zwischenablage unterstützt wird, ist Unicode in der UTF-8-Codierung. Da die ersten Zeichen von UTF-8 und ASCII übereinstimmen, ist die Beschreibung immer ASCII, aber die Bytes des Kontexts (beginnend bei StartHTML) können alle anderen Zeichen verwenden, die in UTF-8 codiert sind.

Das Ende von Zeilen im Formatheader der Zwischenablage kann CR oder CR/LF oder LF sein.

Das Fragment enthält reinen, gültigen HTML-Code, der den bereich darstellt, den der Benutzer ausgewählt hat (z. B. zum Kopieren). Dieser enthält den ausgewählten Text sowie die öffnenden Tags und Attribute jedes Elements, das über ein Endtag innerhalb des ausgewählten Texts verfügt, sowie Endtags am Ende des Fragments für alle enthaltenen Starttags. Dies sind alle Informationen, die für das einfache Einfügen eines HTML-Fragments erforderlich sind.

Dem Fragment sollten die HTML-Kommentare vorangestellt und darauf folgen. <!--StartFragment--> und <!--EndFragment--> (zwischen dem !-- und dem Text ist kein Leerzeichen zulässig), um bequem anzugeben, wo das Fragment beginnt und endet. Daher werden Der Anfang und das Ende des Fragments durch das Vorhandensein dieser Kommentare und durch startFragment- und EndFragment-Byteanzahlen in der Beschreibung angegeben. Es wird erwartet, dass Tools diese Informationen erzeugen. Diese Redundanz wurde eingeführt, um den Anfang des Fragments (aus der Byteanzahl) schnell zu finden und die Position des Fragments direkt in der HTML-Struktur zu markieren.

Die Auswahl gibt innerhalb des Fragments den genauen HTML-Bereich an, den der Benutzer ausgewählt hat (z. B. zu Kopieren). Dadurch werden dem Fragment weitere Informationen hinzugefügt, indem der genaue ausgewählte Text ohne die öffnenden Tags und Endtags angegeben wird, die hinzugefügt wurden, um sicherzustellen, dass das Fragment wohlgeformten HTML-Code hat.

Die Auswahl ist optional, da im Fragment ausreichend Informationen für das einfache Einfügen enthalten sind. Wenn die Auswahl nicht gespeichert wird, werden sowohl StartSelection als auch EndSelection nicht im Header gespeichert.

Der Kontext ist ein gültiges, vollständiges HTML-Dokument. Dieser Artikel enthält das Fragment und alle vorangehenden umgebenden Tags (Start- und Endtags; diese vorhergehenden umgebenden Tags stellen alle übergeordneten Knoten des Fragments bis zum HTML-Knoten dar). Der Artikel enthält auch den vollständigen HEAD-Inhalt und ermöglicht z. B. die Aufnahme der BASE- und TITLE-Elemente, damit diese zusätzlichen Informationen abgerufen werden können. Eine Anwendung, die ein HTML-Fragment in die Zwischenablage kopiert, kann ein BASE-Element erstellen, das in den Kontext eingeschlossen werden soll, wenn ein solches Element noch nicht vorhanden ist, sodass partielle URLs im Fragment aufgelöst werden können.

Der Kontext ist optional, da genügend Informationen im Fragment enthalten sind, damit ein HTML-Fragment einfach eingefügt werden kann. Wenn der Kontext nicht gespeichert wird, wird nur das Fragment und startHTML=EndHTML=-1 gespeichert.

## <a name="scenarios"></a>Szenarien

In den folgenden Szenarien wird beschrieben, wie der IE4/MSHTML-HTML-Editor html ausschneiden und einfügen kann. andere Anwendungen folgen diesen Szenarien möglicherweise oder nicht. Das hier beschriebene Zwischenablageformat soll Flexibilität bei der Auswahl der Funktion einer Anwendung ermöglichen. (Diese Szenarien zeigen nur guten HTML-Code, d.h. keine überlappenden Tags.)

1.  Einfaches HTML-Fragment.
    -   -   HTML-Text:

            <BODY>Dies ist <B>normal. Dies ist </B> <I> <B>fett. Dies ist kursiv. </B>Dies ist kursiv.</I></BODY>

        -   Wird als angezeigt:

            Dies ist **normal. Dies ist**  **_fett. Dies ist kursiv._*  Dies ist kursiv.*

        -   Der Text zwischen \* \* wird ausgewählt und in die Zwischenablage kopiert:

            Dies ist **normal. Dies ist** \* \* **_fett. Dies ist kursiv._* Dies* \* \* *ist kursiv.*   

        -   Dies wird in der Zwischenablage erfolgen (beachten Sie, dass dies die Interpretation von IE4/MSHTML ist):

            Version:0.9

            StartHTML:71

            EndHTML:160

            StartFragment:130

            EndFragment:150

            **StartSelection:130**

            **EndSelection:150**

            <!DOCTYPE ...>

            <BODY>

            <!-- StartFragment -->>

            **<B>bold</B><I><B>Dies ist fett kursiv</B>This</I>**

            <!-- EndFragment -->

            </BODY>

            </HTML>

        -   In diesem Szenario werden nur das BODY-Tag und das HTML-Tag im Kontext vor dem ausgewählten Fragment angezeigt. Beachten Sie, dass Starttags und Endtags im Kontext enthalten sind. Die Auswahl, die durch StartSelection und EndSelection getrennt ist, wird fett dargestellt.

2.  Fragment einer Tabelle in HTML.
    -   -   HTML-Text:

            <BODY><TABLE BORDER><TR><TH ROWSPAN=2>Head1</TH><TD>Element 1</TD><TD>Item 2</TD><TD>Element 3</TD><TD>Element 4</TD></TR><TR><TD>Element 5</TD><TD>Element 6</TD><TD>Element 7</TD><TD>Element 8</TD></TR><TR><TH>Head2</TH><TD>Element 9</TD><TD>Element 10</TD><TD>Element 11</TD><TD>Element 12</TD></TR></TABLE></BODY>

        -   Wird als angezeigt: ><TABLE BORDER><TR><TH ROWSPAN=2>Head1</TH><TD>Element 1</TD><TD>Item 2</TD><TD>Element 3</TD><TD>Element 4</TD></TR><TR><TD>Element 5</TD><TD>Element 6</TD><TD>Element 7</TD><TD>Element 8</TD></TR><TR><TH>Head2</TH><TD>Element 9</TD><TD>Element 10</TD><TD>Element 11</TD><TD>Element 12</TD></TR></TABLE><! \[ Cdata\[\]\]>
        -   Die Elemente Item 6, Item7, Item 10 und Item 11 der Tabelle werden als Block ausgewählt und in die Zwischenablage kopiert.
        -   Dies wird in der Zwischenablage erfolgen (beachten Sie, dass dies die Interpretation von IE4/MSHTML ist):

            <!DOCTYPE ...>

            <HTML><BODY><TABLE BORDER>

            <!--StartFragment-->

            **<TR><TD>Element 6 </TD> <TD> Element 7 </TD> </TR> <TR> <TD> Element 10 </TD> <TD> Element 11</TD></TR>**

            <!--EndFragment-->

            </TABLE>

            </BODY></HTML>The selection, as delimited by StartSelection and EndSelection, is shown in bold.

3.  Einfügen eines Fragments einer sortierten Liste in Nur-Text.
    -   -   HTML-Text:

            <BODY><OL TYPE = a><LI>Element 1<LI>Item 2<LI>Element 3<LI>Element 4<LI>Element 5<LI>Element 6</OL></BODY>

        -   Wird als angezeigt:
            1.  Element 1
            2.  Item 2
            3.  Element 3
            4.  Element 4
            5.  Element 5
            6.  Element 6
        -   Der Benutzer wählt die Elemente 3 bis 5 aus und kopiert sie in die Zwischenablage. Der folgende HTML-Code befindet sich in der Zwischenablage:

            <DOCTYPE...><HTML><BODY><OL TYPE = a>

            <!-- StartFragment-->

            **<LI>Element 3 <LI> Element 4 <LI> Element 5**

            <!-- EndFragment-->

            </OL></BODY></HTML>

            Die Auswahl, die durch StartSelection und EndSelection getrennt ist, wird fett dargestellt.

        -   Wenn dieses Fragment jetzt in ein leeres Dokument eingefügt wird, wird der folgende HTML-Code erstellt:

            <BODY><OL TYPE = a><LI>Element 3<LI>Element 4<LI>Element 5</OL></BODY>

        -   Wird als angezeigt:
            1.  Element 3
            2.  Element 4
            3.  Element 5

4.  Einfügen eines teilweise ausgewählten Bereichs.
    -   -   HTML-Text:

            <P> IE4/MSHTML ist ein WYSIWYG-Editor, der unterstützt:<UL><LI>Ausschneiden<LI>Kopieren<LI>Einfügen</UL><P>Dies ist ein großartiges Tool!

        -   Erscheint als:IE4/MSHTML ist ein WYSIWYG-Editor, der unterstützt:
            -   -   Ausschneiden
                -   Kopieren
                -   Einfügen

        -   Der Benutzer wählt von "WYSIWYG" bis "Cop" aus. Der folgende HTML-Code befindet sich in der Zwischenablage:

            <DOCTYPE...><HTML><BODY>

            <!-- StartFragment-->

            <P>

            **WYSIWYG-Editor, der unterstützt**

            **<UL><LI>Cut <LI> Cop**

            </UL>

            <!-- EndFragment-->

            </BODY></HTML>The selection, as delimited by StartSelection and EndSelection, is shown in bold.

     
    -   -   Der Benutzer wählt von "opy" bis "Great" aus.

            Der folgende HTML-Code befindet sich in der Zwischenablage:

            <DOCTYPE...><HTML><BODY>

            <!-- StartFragment-->

            <UL><LI>

            **opy <LI> Paste This is a </UL> <P> Great**

            </P>

            <!-- EndFragment-->

            </BODY></HTML>

            Die Auswahl, die durch StartSelection und EndSelection getrennt ist, wird fett dargestellt.

 

 




