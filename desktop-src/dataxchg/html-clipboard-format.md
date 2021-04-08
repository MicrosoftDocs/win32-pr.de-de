---
title: HTML-Zwischenablage Format
description: In diesem Abschnitt wird das HTML-Zwischenablage Format erläutert.
ms.assetid: e891393f-234f-4c94-b581-c4e5f885d2ab
keywords:
- Windows-Benutzeroberfläche, Zwischenablage
- Zwischenablage, Daten werden abgeschnitten
- Zwischenablage, Kopieren von Daten
- Zwischenablage, Einfügen von Daten
- Zwischenablage, Formate
- Zwischenablage, HTML-Format
- Zwischenablage, HTML-Text wird abgeschnitten
- Zwischenablage, Einfügen von HTML-Text
- CF_HTML Format der Zwischenablage
- Zwischenablage, CF_HTML Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75cdcd9c2fc982a7cbde38bba4b7dec6738f1793
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037135"
---
# <a name="html-clipboard-format"></a>HTML-Zwischenablage Format

Die Anforderungen für die Übertragung von HTML-Text mithilfe der Zwischenablage unterscheiden sich je nach Szenario. In diesem Artikel geht es um das Ausschnitten und Einfügen von Fragmenten eines HTML-Dokuments. Möglicherweise gibt es Anforderungen zum übertragen ganzer HTML-Dokumente über die Zwischenablage. Dieser Artikel wird jedoch durch eine Anforderung zum Übertragen von Fragmenten aus ausgewähltem HTML-Text gesteuert. Eine Methode, die erfordert, dass das gesamte HTML-Dokument in die Zwischenablage kopiert wird, wird daher als zu schwer zu schwer zu betrachten.

Das Format der CF \_ -HTML-Zwischenablage ermöglicht, dass ein Fragment von unformatiertem HTML-Text und dessen Kontext als ASCII in der Zwischenablage gespeichert wird. Dies ermöglicht es, dass der Kontext des HTML-Fragments, der aus allen vorangehenden umgebenden Tags besteht, von einer Anwendung überprüft werden muss, damit die umgebenden Tags des HTML-Fragments mit ihren Attributen vermerkt werden können. Obwohl es Anwendungen gibt, wie solche Fragmente interpretiert werden können, sind hier einige grundlegende Richtlinien auf der Grundlage von IE4-/MSHTML-Implementierungen enthalten.

Der offizielle Name der Zwischenablage (die von RegisterClipboardFormat verwendete Zeichenfolge) ist das HTML-Format.

-   [Beschreibung](#description)
-   [Szenarios](#scenarios)

## <a name="description"></a>BESCHREIBUNG

CF \_ HTML ist vollständig Text formatiert (unter anderem im HTML-Geist, und verwendet UTF-8) und enthält eine `description` , eine optionale und `context` im Kontext der `fragment` .

Im folgenden finden Sie ein Beispiel für eine Zwischenablage:


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



Die Beschreibung enthält die Versionsnummer und Offsets der Zwischenablage, die angeben, wo der Kontext und das Fragment beginnen und enden. Die Beschreibung ist eine Liste von ASCII-Text Schlüsselwörtern (min/Maj ist nicht aussagekräftig), gefolgt von einer Zeichenfolge und getrennt durch einen Doppelpunkt (:).

**Version**: die Versionsnummer der Zwischenablage. Die Start Version ist 0,9.

**StartHTML**: byteCount vom Anfang der Zwischenablage bis zum Anfang des Kontexts oder-1, wenn kein Kontext angezeigt wird.

**EndHTML**: byteCount vom Anfang der Zwischenablage bis zum Ende des Kontexts oder-1, wenn kein Kontext angezeigt wird.

**StartFragment**: byteCount vom Anfang der Zwischenablage bis zum Anfang des Fragments.

**EndFragment**: byteCount vom Anfang der Zwischenablage bis zum Ende des Fragments.

**Startselection**: byteCount vom Anfang der Zwischenablage bis zum Anfang der Auswahl.

**Endselection**: byteCount vom Anfang der Zwischenablage bis zum Ende der Auswahl.

Die Schlüsselwörter startselection und endselection sind optional und müssen weggelassen werden, wenn Sie nicht möchten, dass die Anwendung diese Informationen generiert.

Weitere Informationen zu dieser Art können später hinzugefügt werden, da der HTML-Code bei starthtmloffset beginnt. Beispielsweise könnten später mehrere Paare von StartFragment/EndFragment hinzugefügt werden, um die nicht zusammenhängende Auswahl von Fragmenten zu unterstützen.

Um die Vorteile der Programme zu erzeugen, die bytecounts erzeugen, könnte bytecounts von Nullen aufgefüllt werden. Programme, die die byteCount-Elemente erzeugen, können z. b. willkürlich die zehn (10) Nullen für jedes Schlüsselwort (StartHTML: 0000000000) beeinflussen und dann, wenn die exakte StartHTML-byteCount bekannt ist (z. b. 71), die entsprechende Anzahl der Nullen durch byteCount (StartHTML: 0000000071)

Der einzige Zeichensatz, der von der Zwischenablage unterstützt wird, ist Unicode in der UTF-8-Codierung. Da die ersten Zeichen von UTF-8 und ASCII Stimmen, ist die Beschreibung immer ASCII, aber die Bytes des Kontexts (beginnend bei StartHTML) können alle anderen Zeichen verwenden, die in UTF-8 codiert sind.

Das Zeilenende im Header des Zwischenablage Formats könnte CR, CR/LF oder LF lauten.

Das Fragment enthält reines, gültiges HTML, das den Bereich darstellt, den der Benutzer ausgewählt hat (z. b. zum Kopieren). Diese enthält den markierten Text sowie die öffnenden Tags und Attribute eines beliebigen Elements, das über ein Endtag im ausgewählten Text verfügt, sowie Endtags am Ende des Fragments für beliebige Starttags. Dies sind alle Informationen, die für das einfache Einfügen eines HTML-Fragments erforderlich sind.

Dem Fragment sollten die HTML-Kommentare vorangestellt und gefolgt werden. <!--StartFragment--> und <!--EndFragment--> (kein Platz zwischen dem!--und dem Text zulässig), um bequem anzugeben, wo das Fragment beginnt und endet. Daher wird der Beginn und das Ende des Fragments durch das vorhanden sein dieser Kommentare und durch Start Fragment und EndFragment-Byte Anzahl in der Beschreibung angegeben. Diese Informationen werden von den Tools erwartet. Diese Redundanz wurde eingeführt, um schnell den Anfang des Fragments (aus der Byte Anzahl) zu finden und die Position des Fragments direkt in der HTML-Struktur zu markieren.

Die Auswahl gibt im Fragment den exakten HTML-Bereich an, den der Benutzer ausgewählt hat (z. b. zum Kopieren). Dadurch werden dem Fragment Weitere Informationen hinzugefügt, indem der genaue markierte Text angegeben wird, ohne dass die öffnenden Tags und Endtags hinzugefügt wurden, um sicherzustellen, dass das Fragment wohl geformt ist.

Die Auswahl ist optional, da genügend Informationen im Fragment für das einfache Einfügen enthalten sind. Wenn die Auswahl nicht gespeichert wird, werden sowohl startselection als auch endselection nicht in der Kopfzeile gespeichert.

Der Kontext ist ein gültiges, umfassendes HTML-Dokument. Dieser Artikel enthält das Fragment und alle vorangehenden Tags (Start-und Endtags; diese vorangehenden Tags stellen alle übergeordneten Knoten des Fragments dar, bis zum HTML-Knoten). Der Artikel enthält auch den kompletten Head und ermöglicht das Einschließen der Basis-und Titel Elemente, damit diese zusätzlichen Informationen abgerufen werden können. Eine Anwendung, die ein HTML-Fragment in die Zwischenablage kopiert, kann ein Basiselement erstellen, das in den Kontext aufgenommen werden soll, wenn ein solches Element nicht bereits vorhanden ist, sodass partielle URLs im Fragment aufgelöst werden können.

Der Kontext ist optional, da genügend Informationen im Fragment enthalten sind, um ein einfaches Einfügen eines HTML-Fragments durchführen zu können. Wenn der Kontext nicht gespeichert wird, wird nur das Fragment und StartHTML = EndHTML =-1 gespeichert.

## <a name="scenarios"></a>Szenarien

In den folgenden Szenarien wird beschrieben, wie der HTML-Editor von IE4/MSHTML HTML-Ausschneiden und Einfügen behandelt. andere Anwendungen können diese Szenarien verwenden oder nicht. Das hier beschriebene Zwischenablage Format soll Flexibilität bei der Funktionsweise einer Anwendung ermöglichen. (In diesen Szenarien werden nur gute HTML-Code angezeigt, d. h. keine überlappenden Tags.)

1.  Einfaches Fragment von HTML.
    -   -   HTML-Text:

            <BODY>Dies <B>ist normal, wenn dies Fett </B>formatiert ist. Dies wird <I> <B> </B>kursiv</I> formatiert.</BODY>

        -   Angezeigt als:

            Dies **ist normal, wenn dies Fett** formatiert ist.    *    Dies wird kursiv formatiert *

        -   Der Text zwischen \* \* wird ausgewählt und in die Zwischenablage kopiert:

            Dies **ist normal, wenn dies fett formatiert** \* \*     * **ist** und   dieses * \* \* *kursiv* formatiert ist.

        -   Dies erfolgt in der Zwischenablage (Beachten Sie, dass es sich um eine IE4/MSHTML-Interpretation handelt):

            Version: 0.9

            StartHTML: 71

            EndHTML: 160

            StartFragment: 130

            EndFragment: 150

            **Startselection: 130**

            **Endselection: 150**

            <!DOCTYPE ...>

            <BODY>

            <!-- StartFragment -->>

            **<B>Fett</B>formatiert <I><B></B></I>**

            <!-- EndFragment -->

            </BODY>

            </HTML>

        -   In diesem Szenario werden nur das Body-Tag und das HTML-Tag im Kontext angezeigt, wenn es dem ausgewählten Fragment vorangestellt ist. Beachten Sie, dass Starttags und Endtags in den Kontext eingeschlossen werden. Die Auswahl, die durch startselection und endselection getrennt ist, wird in Fett Schrift angezeigt.

2.  Fragment einer Tabelle in HTML.
    -   -   HTML-Text:

            <BODY><TABLE BORDER><TR><TH ROWSPAN=2>Head1</TH><TD>Element 1</TD><TD>Item 2</TD><TD>Element 3</TD><TD>Element 4</TD></TR><TR><TD>Element 5</TD><TD>Element 6</TD><TD>Element 7</TD><TD>Element 8</TD></TR><TR><TH>Head2</TH><TD>Element 9</TD><TD>Element 10</TD><TD>Element 11</TD><TD>Element 12</TD></TR></TABLE></BODY>

        -   Angezeigt als: ><TABLE BORDER><TR><TH ROWSPAN=2>Head1</TH><TD>Element 1</TD><TD>Item 2</TD><TD>Element 3</TD><TD>Element 4</TD></TR><TR><TD>Element 5</TD><TD>Element 6</TD><TD>Element 7</TD><TD>Element 8</TD></TR><TR><TH>Head2</TH><TD>Element 9</TD><TD>Element 10</TD><TD>Element 11</TD><TD>Element 12</TD></TR></TABLE><! \[ CDATA\[\]\]>
        -   Die Elemente Element 6, Item7, Element 10 und Element 11 der Tabelle werden als Block ausgewählt und in die Zwischenablage kopiert.
        -   Dies erfolgt in der Zwischenablage (Beachten Sie, dass es sich um eine IE4/MSHTML-Interpretation handelt):

            <!DOCTYPE ...>

            <HTML><BODY><TABLE BORDER>

            <!--StartFragment-->

            **<TR><TD>Element 6 </TD> <TD> Element 7 </TD> </TR> <TR> <TD> Element 10 </TD> <TD> Element 11</TD></TR>**

            <!--EndFragment-->

            </TABLE>

            </BODY></HTML>The selection, as delimited by StartSelection and EndSelection, is shown in bold.

3.  Einfügen eines Fragments einer geordneten Liste in Klartext.
    -   -   HTML-Text:

            <BODY><OL TYPE = a><LI>Element 1<LI>Item 2<LI>Element 3<LI>Element 4<LI>Element 5<LI>Element 6</OL></BODY>

        -   Angezeigt als:
            1.  Element 1
            2.  Item 2
            3.  Element 3
            4.  Element 4
            5.  Element 5
            6.  Element 6
        -   Der Benutzer wählt die Elemente 3 bis 5 aus und kopiert sie in die Zwischenablage. Der folgende HTML-Code befindet sich in der Zwischenablage:

            <DOCTYPE... ><HTML><BODY><OL TYPE = a>

            <!-- StartFragment-->

            **<LI>Element 3, Element <LI> 4, <LI> Element 5**

            <!-- EndFragment-->

            </OL></BODY></HTML>

            Die Auswahl, die durch startselection und endselection getrennt ist, wird fett formatiert angezeigt.

        -   Wenn dieses Fragment nun in ein leeres Dokument eingefügt wird, wird der folgende HTML-Code erstellt:

            <BODY><OL TYPE = a><LI>Element 3<LI>Element 4<LI>Element 5</OL></BODY>

        -   Folgendes wird angezeigt:
            1.  Element 3
            2.  Element 4
            3.  Element 5

4.  Einfügen eines teilweise ausgewählten Bereichs.
    -   -   HTML-Text:

            <P> IE4/MSHTML ist ein WYSIWYG-Editor, der Folgendes unterstützt:<UL><LI>Ausschneiden<LI>Kopieren<LI>Einfügen</UL><P>Dies ist ein großartiges Tool!

        -   Angezeigt als: IE4/MSHTML ist ein WYSIWYG-Editor, der Folgendes unterstützt:
            -   -   Ausschneiden
                -   Kopieren
                -   Einfügen

        -   Der Benutzer wählt aus "WYSIWYG" bis "Cop" aus. Der folgende HTML-Code befindet sich in der Zwischenablage:

            <DOCTYPE... ><HTML><BODY>

            <!-- StartFragment-->

            <P>

            **WYSIWYG-Editor, der**

            **<UL><LI>COP Ausschneiden <LI>**

            </UL>

            <!-- EndFragment-->

            </BODY></HTML>The selection, as delimited by StartSelection and EndSelection, is shown in bold.

     
    -   -   Der Benutzer wählt zwischen "OPY" und "groß" aus.

            Der folgende HTML-Code befindet sich in der Zwischenablage:

            <DOCTYPE... ><HTML><BODY>

            <!-- StartFragment-->

            <UL><LI>

            **OPY <LI> Einfügen </UL> <P> Dies ist ein hervorragend.**

            </P>

            <!-- EndFragment-->

            </BODY></HTML>

            Die Auswahl, die durch startselection und endselection getrennt ist, wird in Fett Schrift angezeigt.

 

 




