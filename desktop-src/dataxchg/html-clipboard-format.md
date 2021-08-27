---
title: HTML-Zwischenablageformat
description: In diesem Abschnitt wird das HTML-Zwischenablageformat erläutert.
ms.assetid: e891393f-234f-4c94-b581-c4e5f885d2ab
keywords:
- Windows Benutzeroberfläche,Zwischenablage
- Zwischenablage, Schneidedaten
- Zwischenablage,Kopieren von Daten
- Zwischenablage, Daten werden eingefügt
- Zwischenablage, Formate
- Zwischenablage, HTML-Format
- Zwischenablage, Ausschneiden von HTML-Text
- Zwischenablage, Einfügen von HTML-Text
- CF_HTML zwischenablageformat
- Zwischenablage,CF_HTML Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18d73b5101d26fc55002d55e0c15144646b80445
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884973"
---
# <a name="html-clipboard-format"></a>HTML-Zwischenablageformat

Die Anforderungen für die Übertragung von HTML-Text über die Zwischenablage unterscheiden sich je nach Szenario. In diesem Artikel wird das Ausschneiden und Einfügen von Fragmenten eines HTML-Dokuments behandelt. Möglicherweise müssen ganze HTML-Dokumente über die Zwischenablage übertragen werden. Dieser Artikel wird jedoch durch die Anforderung zum Übertragen von Fragmenten des ausgewählten HTML-Texts gesteuert. Daher wird eine Methode, bei der das gesamte HTML-Dokument in die Zwischenablage kopiert werden musste, als zu stark bezeichnet.

Das CF HTML-Zwischenablageformat ermöglicht das Speichern eines Fragments von unformatiertem HTML-Text und dessen Kontext in der Zwischenablage \_ als ASCII. Dadurch kann der Kontext des HTML-Fragments, das aus allen vorangehenden umgebenden Tags besteht, von einer Anwendung untersucht werden, sodass die umgebenden Tags des HTML-Fragments mit ihren Attributen notiert werden können. Obwohl anwendungen entscheiden müssen, wie solche Fragmente interpretiert werden sollen, sind hier einige grundlegende Richtlinien enthalten, die auf IE4/MSHTML-Implementierungen basieren.

Der offizielle Name der Zwischenablage (die von RegisterClipboardFormat verwendete Zeichenfolge) ist HTML-Format.

-   [Beschreibung](#description)
-   [Szenarios](#scenarios)

## <a name="description"></a>Beschreibung

CF HTML ist ein vollständig text-Format (u.a. im HTML-Format und verwendet \_ UTF-8) und enthält ein , ein optionales und im Kontext `description` `context` das `fragment` .

Im Folgenden finden Sie ein Beispiel für eine Zwischenablage:


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



Die Beschreibung enthält die Versionsnummer und offsets der Zwischenablage, die angeben, wo der Kontext und das Fragment beginnen und enden. Die Beschreibung ist eine Liste von ASCII-Textschlüsselwörtern (min/list ist nicht sinnvoll), gefolgt von einer Zeichenfolge und getrennt durch einen Doppelpunkt (:).

**Version:** vv-Versionsnummer der Zwischenablage. Die Startversion ist 0.9.

**StartHTML:** bytecount vom Anfang der Zwischenablage bis zum Anfang des Kontexts oder -1, wenn kein Kontext angezeigt wird.

**EndHTML:** bytecount vom Anfang der Zwischenablage bis zum Ende des Kontexts oder -1, wenn kein Kontext angezeigt wird.

**StartFragment:** bytecount vom Anfang der Zwischenablage bis zum Anfang des Fragments.

**EndFragment:** bytecount vom Anfang der Zwischenablage bis zum Ende des Fragments.

**StartSelection:** bytecount vom Anfang der Zwischenablage bis zum Anfang der Auswahl.

**EndSelection:** bytecount vom Anfang der Zwischenablage bis zum Ende der Auswahl.

Die Schlüsselwörter StartSelection und EndSelection sind optional und müssen ausgelassen werden, wenn die Anwendung diese Informationen nicht generieren soll.

Weitere Informationen dieser Art können später hier hinzugefügt werden, da der HTML-Code am StartHTMLoffset beginnt. Beispielsweise könnten später mehrere Paare von StartFragment/EndFragment hinzugefügt werden, um die nicht zusammenhängende Auswahl von Fragmenten zu unterstützen.

Zur Vereinfachung der Programme, die die Bytecounts generieren, können Bytezählungen durch Nullen aufschlossen werden. Programme, die die Bytecounts generieren, können z. B. beliebig zehn (10) Nullen für jedes Schlüsselwort (StartHTML: 0000000000) beeinflussen. Wenn dann die genaue StartHTML-Byteanzahl bekannt ist (z.B. 71), kann das Programm die entsprechende Anzahl von Nullen durch die Byteanzahl (StartHTML: 0000000071) ersetzen.

Der einzige Zeichensatz, der von der Zwischenablage unterstützt wird, ist Unicode in seiner UTF-8-Codierung. Da die ersten Zeichen von UTF-8 und ASCII übereinstimmen, ist die Beschreibung immer ASCII, aber die Bytes des Kontexts (ab StartHTML) können alle anderen Zeichen verwenden, die in UTF-8 codiert sind.

Das Ende der Zeilen im Formatheader der Zwischenablage kann CR oder CR/LF oder LF sein.

Das Fragment enthält reinen, gültigen HTML-Code, der den bereich darstellt, den der Benutzer ausgewählt hat (z. B. zum Kopieren). Dieser enthält den ausgewählten Text sowie die öffnenden Tags und Attribute jedes Elements, das ein Endtag innerhalb des ausgewählten Texts enthält, und Endtags am Ende des Fragments für jedes enthaltene Starttag. Dies sind alle Informationen, die für das einfache Einfügen eines HTML-Fragments erforderlich sind.

Dem Fragment sollten die HTML-Kommentare vorangehende und gefolgt werden. <!--StartFragment--> und <!--EndFragment--> (Kein Leerzeichen zwischen dem !-- und dem Text), um bequem anzugeben, wo das Fragment beginnt und endet. Daher werden der Anfang und das Ende des Fragments durch das Vorhandensein dieser Kommentare und durch die Byteanzahl StartFragment und EndFragment in der Beschreibung angegeben. Von Tools wird erwartet, dass diese Informationen erzeugt werden. Diese Redundanz wurde eingeführt, um schnell den Anfang des Fragments (aus der Byteanzahl) zu finden und die Position des Fragments direkt in der HTML-Struktur zu markieren.

Die Auswahl gibt innerhalb des Fragments den genauen HTML-Bereich an, den der Benutzer ausgewählt hat (z. B. zum Kopieren). Dadurch werden dem Fragment weitere Informationen hinzugefügt, indem der genau ausgewählte Text ohne die öffnenden Tags und Endtags angegeben wird, die hinzugefügt wurden, um sicherzustellen, dass das Fragment wohlgeformter HTML-Code ist.

Die Auswahl ist optional, da im Fragment genügend Informationen für das einfache Einfing enthalten sind. Wenn die Auswahl nicht gespeichert ist, werden sowohl StartSelection als auch EndSelection nicht im Header gespeichert.

Der Kontext ist ein gültiges, vollständiges HTML-Dokument. Dieser Artikel enthält das Fragment und alle vorangehenden umgebenden Tags (Start- und Endtags; diese vorangehenden umgebenden Tags stellen alle übergeordneten Knoten des Fragments bis zum HTML-Knoten dar). Der Artikel enthält auch den vollständigen HEAD und ermöglicht beispielsweise das Ein- und Ausliefern der BASE- und TITLE-Elemente, damit diese zusätzlichen Informationen erhalten werden können. Eine Anwendung, die ein HTML-Fragment in die Zwischenablage kopiert, kann ein BASE-Element erstellen, das in den Kontext eingefügt werden soll, wenn ein solches Element nicht bereits vorhanden ist, damit partielle URLs im Fragment aufgelöst werden können.

Der Kontext ist optional, da genügend Informationen im Fragment enthalten sind, damit ein HTML-Fragment einfach einfügen kann. Wenn der Kontext nicht gespeichert wird, wird nur das Fragment und StartHTML=EndHTML=-1 gespeichert.

## <a name="scenarios"></a>Szenarien

In den folgenden Szenarien wird beschrieben, wie der IE4/MSHTML-HTML-Editor das Ausschneiden und Einfügen von HTML behandelt. Andere Anwendungen folgen diesen Szenarien möglicherweise oder nicht. Das hier beschriebene Zwischenablageformat soll Flexibilität bei der Funktionsweise einer Anwendung ermöglichen. (Diese Szenarien zeigen nur guten HTML-Code, d. h. keine überlappenden Tags.)

1.  Einfaches HTML-Fragment.
    -   -   HTML-Text:

            &lt;BODY &gt; This is normal This is bold <B>This </B>is bold <I> <B>italic </B>This is italic </I> &lt; /BODY&gt;

        -   Wird wie hier angezeigt:

            This is normal **This is bold This** is bold **_italic_* This is italic*  

        -   Der Text zwischen dem \* \* wird ausgewählt und in die Zwischenablage kopiert:

            This is normal **This is** \* \* **bold This** is bold **_italic_* This* is \* \* *italic*   

        -   Dies wird in der Zwischenablage angezeigt (beachten Sie, dass dies die Interpretation von IE4/MSHTML ist):

            Version:0.9

            StartHTML:71

            EndHTML:160

            StartFragment:130

            EndFragment:150

            **StartSelection:130**

            **EndSelection:150**

            <!DOCTYPE ...>

            &lt;KÖRPER&gt;

            <!-- StartFragment -->>

            **<B>bold</B><I><B>Dies ist fett italisch</B>This</I>**

            <!-- EndFragment -->

            &lt;/BODY&gt;

            &lt;/HTML&gt;

        -   In diesem Szenario werden nur das BODY-Tag und das HTML-Tag im Kontext vor dem ausgewählten Fragment angezeigt. Beachten Sie, dass Starttags und Endtags im Kontext enthalten sind. Die Auswahl, wie durch StartSelection und EndSelection getrennt, wird fett dargestellt.

2.  Fragment einer Tabelle in HTML.
    -   -   HTML-Text:

            &lt;KÖRPER&gt;<TABLE BORDER><TR><TH ROWSPAN=2>Head1</TH><TD>Element 1</TD><TD>Item 2</TD><TD>Element 3</TD><TD>Element 4</TD></TR><TR><TD>Element 5</TD><TD>Element 6</TD><TD>Element 7</TD><TD>Element 8</TD></TR><TR><TH>Head2</TH><TD>Element 9</TD><TD>Element 10</TD><TD>Element 11</TD><TD>Element 12</TD></TR></TABLE>&lt;/BODY&gt;

        -   Wird als angezeigt: ><TABLE BORDER><TR><TH ROWSPAN=2>Head1</TH><TD>Element 1</TD><TD>Item 2</TD><TD>Element 3</TD><TD>Element 4</TD></TR><TR><TD>Element 5</TD><TD>Element 6</TD><TD>Element 7</TD><TD>Element 8</TD></TR><TR><TH>Head2</TH><TD>Element 9</TD><TD>Element 10</TD><TD>Element 11</TD><TD>Element 12</TD></TR></TABLE><! \[ CDATA\[\]\]>
        -   Die Elemente Item 6, Item7, Item 10 und Item 11 der Tabelle werden als Block ausgewählt und in die Zwischenablage kopiert.
        -   Dies wird in der Zwischenablage erfolgen (beachten Sie, dass dies die Interpretation von IE4/MSHTML ist):

            <!DOCTYPE ...>

            &lt;&gt; &lt; HTML-TEXT&gt;<TABLE BORDER>

            <!--StartFragment-->

            **<TR><TD>Element 6 </TD> <TD> Element 7 </TD> </TR> <TR> <TD> Element 10 </TD> <TD> Element 11</TD></TR>**

            <!--EndFragment-->

            </TABLE>

            &lt;/BODY &gt; &lt; /HTML &gt; Die Auswahl, die durch StartSelection und EndSelection getrennt ist, wird fett dargestellt.

3.  Einfügen eines Fragments einer sortierten Liste in Nur-Text.
    -   -   HTML-Text:

            &lt;KÖRPER&gt;<OL TYPE = a><LI>Element 1<LI>Item 2<LI>Element 3<LI>Element 4<LI>Element 5<LI>Element 6</OL>&lt;/BODY&gt;

        -   Wird als angezeigt:
            1.  Element 1
            2.  Item 2
            3.  Element 3
            4.  Element 4
            5.  Element 5
            6.  Element 6
        -   Der Benutzer wählt die Elemente 3 bis 5 aus und kopiert sie in die Zwischenablage. Der folgende HTML-Code befindet sich in der Zwischenablage:

            <DOCTYPE...>&lt; &gt; &lt; HTML-TEXT&gt;<OL TYPE = a>

            <!-- StartFragment-->

            **<LI>Element 3 <LI> Element 4 <LI> Element 5**

            <!-- EndFragment-->

            </OL>&lt;/BODY&gt;&lt;/HTML&gt;

            Die Auswahl, die durch StartSelection und EndSelection getrennt ist, wird fett dargestellt.

        -   Wenn dieses Fragment jetzt in ein leeres Dokument eingefügt wird, wird der folgende HTML-Code erstellt:

            &lt;KÖRPER&gt;<OL TYPE = a><LI>Element 3<LI>Element 4<LI>Element 5</OL>&lt;/BODY&gt;

        -   Wird als angezeigt:
            1.  Element 3
            2.  Element 4
            3.  Element 5

4.  Einfügen einer teilweise ausgewählten Region.
    -   -   HTML-Text:

            <P> IE4/MSHTML ist ein WYSIWYG-Editor, der unterstützt:<UL><LI>Ausschneiden<LI>Kopieren<LI>Einfügen</UL><P>Dies ist ein großartiges Tool!

        -   Erscheint als:IE4/MSHTML ist ein WYSIWYG-Editor, der unterstützt:
            -   -   Ausschneiden
                -   Kopieren
                -   Einfügen

        -   Der Benutzer wählt von "WYSIWYG" bis "Cop" aus. Der folgende HTML-Code befindet sich in der Zwischenablage:

            <DOCTYPE...>&lt; &gt; &lt; HTML-TEXT&gt;

            <!-- StartFragment-->

            <P>

            **WYSIWYG-Editor, der unterstützt**

            **<UL><LI>Cut <LI> Cop**

            </UL>

            <!-- EndFragment-->

            &lt;/BODY &gt; &lt; /HTML &gt; Die Auswahl, die durch StartSelection und EndSelection getrennt ist, wird fett dargestellt.

     
    -   -   Der Benutzer wählt von "opy" bis "Great" aus.

            Der folgende HTML-Code befindet sich in der Zwischenablage:

            <DOCTYPE...>&lt; &gt; &lt; HTML-TEXT&gt;

            <!-- StartFragment-->

            <UL><LI>

            **opy <LI> Paste This is a </UL> <P> Great**

            </P>

            <!-- EndFragment-->

            &lt;/BODY &gt; &lt; /HTML&gt;

            Die Auswahl, die durch StartSelection und EndSelection getrennt ist, wird fett dargestellt.

 

 




