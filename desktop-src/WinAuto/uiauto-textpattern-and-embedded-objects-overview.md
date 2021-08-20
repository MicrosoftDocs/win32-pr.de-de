---
title: Verfügbar machen eingebetteter Objekte durch Benutzeroberflächenautomatisierung
description: In diesem Thema wird beschrieben, wie Microsoft Benutzeroberflächenautomatisierung eingebettete Objekte oder untergeordnete Elemente in einem Textdokument oder Container verfügbar macht.
ms.assetid: 5ecf5e94-5329-4abb-aedb-4e303688e5f7
keywords:
- Übersicht über Benutzeroberflächenautomatisierung,Textmuster
- Übersicht über Benutzeroberflächenautomatisierung,Textsteuerelemente
- Benutzeroberflächenautomatisierung,Text-Steuerelementmuster
- Übersicht über Benutzeroberflächenautomatisierung,eingebettete Objekte
- Benutzeroberflächenautomatisierung,Verfügbarmachen eingebetteter Objekte
- Benutzeroberflächenautomatisierung,Szenarien für eingebettete Objekte
- Textmuster,Informationen
- Textsteuerelemente, Informationen
- Textsteuerelementmuster
- Steuerelementmuster,Text
- Eingebettete Objekte
- Verfügbarmachen eingebetteter Objekte
ms.topic: article
ms.date: 08/31/2019
ms.openlocfilehash: 2cb5a571d61353d2c8458b42fb65eac19eab0fb228f1e157539470075e392b8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899348"
---
# <a name="how-ui-automation-exposes-embedded-objects"></a>Verfügbar machen eingebetteter Objekte durch Benutzeroberflächenautomatisierung

In diesem Thema wird beschrieben, wie Microsoft Benutzeroberflächenautomatisierung die Text- und TextRange-Steuerelementmuster verwendet, um eingebettete Objekte (untergeordnete/untergeordnete Elemente) in einem Textdokument oder Container verfügbar zu machen.

Für Benutzeroberflächenautomatisierung ist ein eingebettetes Objekt jedes Element, das nicht textbezogene Grenzen aufwies, z. B. ein Bild, einen Link, eine Tabelle oder einen Dokumenttyp (Microsoft Excel Arbeitsblatt, Microsoft Windows Media-Datei usw.).

> [!NOTE]
> Dies unterscheidet sich von der COMPONENT OBJECT MODEL (COM)-OLE-Definition (siehe [Eingebettete Objekte),](../com/embedded-objects.md)bei der ein Element in einer Anwendung erstellt und in einer anderen Anwendung eingebettet oder verknüpft wird. Ob das Objekt in der ursprünglichen Anwendung bearbeitet werden kann, ist im Kontext Benutzeroberflächenautomatisierung irrelevant.

## <a name="embedded-objects-and-the-ui-automation-tree"></a>Eingebettete Objekte und die Benutzeroberflächenautomatisierungs-Struktur

Eingebettete Objekte werden in der Steuerelementansicht der Benutzeroberflächenautomatisierung-Struktur als einzelne Elemente behandelt. Sie werden als untergeordnete Elemente des Textcontainers verfügbar gemacht, sodass sie über das gleiche Objektmodell wie andere Steuerelemente in Benutzeroberflächenautomatisierung aufgerufen werden können.

In der folgenden Tabelle sind Beispiele für Container- und Nichtcontainerelemente aufgeführt.

:::row:::
   :::column span="2":::

      **Containerelemente**

   :::column-end:::
   :::column span="":::

      **Nicht-Containerelemente**

   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::

- Kalender
- Combobox
- DataGrid
- Dokument
- Bearbeiten
- Group
- Header
- HeaderItem
- List
- Menü

   :::column-end:::
   :::column span="":::

- MenuBar
- Bereich
- SplitButton
- Registerkarte
- Tabelle
- Symbolleiste
- Struktur
- TreeItem
- Fenster

   :::column-end:::
   :::column span="":::

- Link
- Kontrollkästchen
- Schaltfläche

  :::column-end:::
:::row-end:::

Die folgende Abbildung zeigt einen Textcontainer (Dokument) mit einer eingebetteten Tabelle und einem eingebetteten Bild.

![Abbildung eines Dokuments mit einer eingebetteten Tabelle und einem eingebetteten Bild](images/embeddedtable.jpg)

Die Benutzeroberflächenautomatisierung Inhaltsansicht des vorherigen Dokuments ist im folgenden Diagramm dargestellt.

![Diagramm der Benutzeroberflächenautomatisierungs-Inhaltsansicht eines Dokuments mit eingebetteten Objekten](images/contenttree.jpg)

### <a name="compatible-and-non-compatible-embedded-objects"></a>Eingebettete Objekte "Kompatibel" und "Nicht kompatibel"

Einige Benutzeroberflächenautomatisierung-Anbieter verwenden für jedes enthaltene TextPattern-Objekt denselben Textspeicher.  Objekte, die vom gleichen Textspeicher wie ihr Container unterstützt werden, werden als "kompatible" eingebettete Objekte bezeichnet. Diese Objekte können TextPattern-Objekte selbst sein, und in diesem Fall sind ihre Textbereiche mit Textbereichen vergleichbar, die aus ihrem Container abgerufen werden. Dies ermöglicht es den Anbietern, Clientinformationen zu den einzelnen TextPattern-Objekten so verfügbar zu machen, als ob es sich um einen großen Textanbieter handelt.

Anbieter können jedoch unterschiedliche Textspeicher für verschiedene TextPattern-Objekte verwenden, die in einen TextPattern-Container eingebettet sind. Objekte, die nicht vom Textspeicher des Containers unterstützt werden, werden als "nicht kompatible" eingebettete Objekte bezeichnet. Diese Typen eingebetteter Objekte können TextPattern-basierte Objekte sein oder nicht.  

In der folgenden Tabelle sind einige Beispiele für kompatible und nicht kompatible eingebettete Objekte aufgeführt.

| Objekte  | Kompatible eingebettete Objekte | Nicht kompatible eingebettete Objekte |
| --- | --- | --- |
| Eingebettete Objekte ohne TextPattern | Schaltfläche in Microsoft Edge<br>Datentabelle in Microsoft Edge | Schaltfläche in RichTextBlock im XAML-Framework von Microsoft<br>Bilder mit Alttext in Microsoft Edge<br>ListView mit ListItems in RichTextBlock im XAML-Framework von Microsoft |
| Eingebettete TextPattern-Objekte | Eingabesteuerelement vom Typ "text" in Microsoft Edge<br>Tabelle in einem Word-Dokument | TextBox-Element in einem Microsoft Word Dokument |

## <a name="exposing-embedded-objects"></a>Verfügbarmachen eingebetteter Objekte

Die [Text- und TextRange-Steuerelementmuster](uiauto-implementingtextandtextrange.md) machen Eigenschaften und Methoden verfügbar, die die Navigation und Abfrage eingebetteter Objekte erleichtern.

Der Textinhalt (oder innerer Text) eines Textcontainers und eines eingebetteten Objekts, z. B. ein Link oder eine Tabellenzelle, wird sowohl in der Steuerelementansicht als auch in der Inhaltsansicht der Benutzeroberflächenautomatisierung Struktur als einzelner fortlaufender Textstream verfügbar gemacht. Objektgrenzen werden ignoriert. Wenn ein Benutzeroberflächenautomatisierung Client den Text abruft, der auf irgendeine Weise reitet, interpretiert oder analysiert werden soll, sollte der Textbereich auf Sonderfälle überprüft werden, z. B. auf eine Tabelle mit Textinhalt oder andere eingebettete Objekte. Rufen Sie [**IUIAutomationTextRange::GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) auf, um eine [**IUIAutomationElement-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) für jedes eingebettete Objekt abzurufen, und rufen Sie dann [**IUIAutomationTextPattern::RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) auf, um einen Textbereich für jedes Element abzurufen. Dies wird rekursiv ausgeführt, bis der gesamte Textinhalt abgerufen wurde.

> [!NOTE]
> In einem degenerierten (oder reduzierten) Bereich sind der Startendpunkt und der Endpunkt identisch. Degenerate Bereiche werden häufig verwendet, um die Position des Textcursors über die [Methoden ITextProvider](/windows/win32/api/uiautomationcore/nn-uiautomationcore-itextprovider) [GetSelection](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextprovider-getselection) und [GetCaretRange](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextprovider2-getcaretrange) anzugeben.

Das folgende Diagramm zeigt einen Textstream mit eingebetteten Objekten und deren Bereichsspannen.

![Diagramm mit einem Textstream mit eingebetteten Objekten und deren Bereichsspannen](images/rangespans.jpg)

## <a name="embedded-objects-and-textunit"></a>Eingebettete Objekte und TextUnit

Ein [ITextProvider-Objekt](/windows/win32/api/uiautomationcore/nn-uiautomationcore-itextprovider) kann und von einer angegebenen [TextUnit](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textunit)durchlaufen werden. Anbieter, die eingebettete Objekte enthalten, können auf ähnliche Weise durchlaufen werden, aber eingebettete Objekte wirken sich auf den Durchlauf aus. Im Folgenden finden Sie einige Punkte, die Sie beachten sollten:

- Jedes nicht kompatible eingebettete Objekt wird durch das Ersetzungszeichen U+FFFC im Textspeicher des TextPattern des Containerelements dargestellt. Sie wird auch sowohl als Zeicheneinheit als auch als Worteinheit betrachtet.
- Kompatible eingebettete Objekte können aus mehreren Zeichen und Wörtern bestehen.
- Das einschließende Element ist das element ganz unten, das den gesamten Textbereich umfasst.
- Untergeordnete Elemente eines Bereichs sind auch untergeordnete Elemente eines Containerelements, das teilweise oder vollständig in den Bereich eingeschlossen ist.
- Im Idealfall (insbesondere bei Containerelementen wie Table) geht eine Wortgrenze nicht über die Objektgrenze hinaus. Im folgenden Beispiel enthält die Worteinheit "Bar" keine Textposition außerhalb des `</td>` Tags ( ist nicht Teil des `<br \>` Worts "Bar").

```Xaml
<table style="width:100%">
  <tr>
    <th>Name</th>
    <th>Notes</th>
  </tr>
  <tr>
    <td>Eve Jackson</td>
    <td>Foo Bar</td>
  </tr>
</table>
<br/>
```

- Im Allgemeinen `<br \>` wird als einzelnes Wort behandelt, sodass es nicht über eine Zeilengrenze hinausgeht.
- Eine Ausnahme von der vorherigen Regel ist, dass eine Word-Texteinheit vollständige Objekte in sich selbst enthält. Beispielsweise `<p>Hello <a href="#">link</a> here.</p>` enthält , das Inlinecontainer enthält, die Wörter "Hello ", "link" und "here". Dabei weist "link" ein TextPattern-Objekt als einschließendes Element und ein Linkobjekt als untergeordnetes Element auf.
- Im Fall von Zeicheneinheiten ist das Objekt das einschließende Element (Texteinheiten wie diese sollten keine untergeordneten Elemente aufweisen).
- Anmerkungsobjekte sollten nicht als eingebettetes Objekt dargestellt werden. Beispielsweise das Vorhandensein anderer Autorenspezifizierer in einem gemeinsam erstellten Dokument.
- Eingebettete Objekte nehmen mindestens eine Cursorposition ein, Anmerkung ist nur Metadaten.
- Jede Objektgrenze (Start und Ende) wird durch eine Formatunterbrechung im TextPattern-Dokumentbereich dargestellt.
- Bei HTML führt jedes HTML-Tag nicht unbedingt zu einem Benutzeroberflächenautomatisierung-Objekt. Beispielsweise müssen Inhalte innerhalb von <em></em> Hervorhebungstags nicht als Element dargestellt werden, sondern als Textstream, in dem UIA_IsItalicAttributeId TRUE zurückgibt.
- Der Startendpunkt ist inklusiv und der bevorzugte Endpunkt, während der Endpunkt "End" exklusiv ist. Dies ist nützlich, wenn der Bereich degeneriert ist und die Endpunkte Start und End an derselben Position für diesen Bereich gehören.

## <a name="comparing-embedded-objects"></a>Vergleichen eingebetteter Objekte

Geschachtelte TextPattern-Objekte, die sich in einer ähnlichen untergeordneten Beziehung befinden und denselben Unterstützungstextspeicher verwenden, werden als vergleichbar bezeichnet. In diesem Fall können Bereiche aus einem der TextPattern-Objekte mithilfe von [ITextRangeProvider::Compare](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-compare) und [ITextRangeProvider::CompareEndpoints](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-compareendpoints)verglichen werden. Beide führen zu einem gültigen numerischen Wert, der ihre relative Position angibt.

Ein Nicht-TextPattern-Objekt, das in ein TextPattern-Objekt eingebettet ist, ist mit dem TextPattern vergleichbar, wenn das -Objekt einen gültigen Bereich im TextPattern[(ITextProvider::RangeFromChild](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextprovider-rangefromchild)) hat und der Inhalt hinter dem Textbereich nicht leer und kein Ersatzzeichen ist.

## <a name="embedded-textpattern-objects-and-the-document-textunit"></a>Eingebettete TextPattern-Objekte und die Document TextUnit

Bei eingebetteten TextPattern-Objekten erkennt die [Dokumenteinheit](/windows/win32/api/uiautomationcore/ne-uiautomationcore-textunit) nur den Inhalt, der in diesem Element enthalten ist.

### <a name="word-textpattern-element-hierarchy"></a>Word TextPattern-Elementhierarchie

- Das Dokumentelement implementiert TextPattern, und [Document](/windows/win32/api/uiautomationcore/ne-uiautomationcore-textunit) gibt den gesamten Word-Dokumentbereich zurück.
- Einzelne Seiten des Dokuments implementieren TextPattern, und [Document](/windows/win32/api/uiautomationcore/ne-uiautomationcore-textunit) gibt den Inhalt dieser einzelnen Seiten zurück (obwohl die Seiten denselben Textspeicher für das gesamte Dokument TextPattern verwenden).

### <a name="webpage-and-text-input-controls-in-edge"></a>Steuerelemente für Webseiten- und Texteingaben in Edge

- Das Pane-Element der Hauptwebseite implementiert TextPattern und macht den gesamten Webseiteninhalt verfügbar.
- Einzelne Texteingabesteuerelemente unterstützen TextPattern, wobei ein Dokumentbereich den in jedem Eingabefeld enthaltenen Text darstellt (obwohl sie denselben Textspeicher für die gesamte Webseite gemeinsam nutzen).

## <a name="common-scenarios"></a>Häufige Szenarios

Dieser Abschnitt enthält Beispiele für gängige Szenarien, die eingebettete Objekte umfassen: Hyperlinks, Bilder und Tabellen. In den folgenden Beispielen stellt die linke geschweifte Klammer ({) den Startendpunkt des Textbereichs und die rechte geschweifte Klammer (}) den Endpunkt End dar.

### <a name="hyperlink-example-1-a-text-range-that-contains-an-embedded-text-hyperlink"></a>HyperLink Beispiel 1: Ein Textbereich, der einen eingebetteten Textlink enthält

Der folgende Textbereich enthält einen eingebetteten Textlink.

  {Die URL https://www.microsoft.com ist in Text eingebettet}.

Das Aufrufen der Methoden [**IUIAutomationTextRange::GetText,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) [**GetEnclosingElement,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)und [**IUIAutomationTextPattern::RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) führt zu den in der folgenden Tabelle beschriebenen Verhaltensweisen.

| Aufgerufene Methode                                                                                                                                                                                                                                                     | Ergebnis                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                                                                                                                                                                                  | Gibt die Zeichenfolge "Die URL https://www.microsoft.com ist in Text eingebettet" zurück.                                                                               |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)                                                                                                                                                          | Gibt das innerste Benutzeroberflächenautomatisierung -Element zurück, das den Textbereich einschließt, in diesem Fall das Automatisierungselement, das den Textanbieter selbst darstellt. |
| [**IUIAutomationTextRange::GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)                                                                                                                                                                          | Gibt ein Benutzeroberflächenautomatisierung -Element zurück, das das Linksteuerelement darstellt.                                                                                      |
| [**IUIAutomationTextPattern::RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild), wobei das Benutzeroberflächenautomatisierung Element von der vorherigen [**IUIAutomationTextRange::GetChildren-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) zurückgegeben wurde. | Gibt den Bereich zurück, der "" https://www.microsoft.com darstellt.                                                                                            |
### <a name="hyperlink-example-2-a-text-range-that-partially-spans-an-embedded-text-hyperlink"></a>HyperLink– Beispiel 2: Ein Textbereich, der einen eingebetteten Textlink teilweise umfasst

Der folgende Textbereich umfasst teilweise einen eingebetteten Textlink.

  Die URL https://{www} ist in Text eingebettet.

Das Aufrufen der Methoden [**IUIAutomationTextRange::GetText,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)und [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) führt zu den in der folgenden Tabelle beschriebenen Verhaltensweisen.

| Aufgerufene Methode                                                                                            | Ergebnis                                                                                                         |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                         | Gibt die Zeichenfolge „www“ zurück.                                                                                      |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) | Gibt das innerste Benutzeroberflächenautomatisierung Element zurück, das den Textbereich einschließt. in diesem Fall das Linksteuerelement. |
| [**IUIAutomationTextRange::GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)                 | Gibt **NULL** zurück, da sich der Textbereich nicht über die gesamte URL-Zeichenfolge erstreckt.                                   |

### <a name="hyperlink-example-3-a-text-range-that-partially-spans-the-content-of-a-text-container"></a>HyperLink– Beispiel 3: Ein Textbereich, der den Inhalt eines Textcontainers teilweise umfasst

Der folgende Textbereich umfasst teilweise den Inhalt eines Textcontainers. Der Textcontainer enthält einen eingebetteten Textlink, der nicht im Textbereich enthalten ist.

  {Die URL} https://www.microsoft.com ist in Text eingebettet.

Das Aufrufen der Methoden [**IUIAutomationTextRange::GetText,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)und [**Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) führt zu den in der folgenden Tabelle beschriebenen Verhaltensweisen.

| Aufgerufene Methode                                                                                            | Ergebnis                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                         | Gibt die Zeichenfolge „Die URL“ zurück.                                                                                                                                                                                                     |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) | Gibt das innerste Benutzeroberflächenautomatisierung -Element zurück, das den Textbereich einschließt, in diesem Fall das Element, das den Textanbieter selbst darstellt.                                                                                     |
| [**IUIAutomationTextRange::Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move)                               | Verschiebt den Textbereich in "https://", da der Text des Links aus einzelnen Wörtern besteht. In diesem Fall wird der Link nicht als einzelnes Objekt behandelt.<br/> Die URL {http} ist in den Text eingebettet.<br/> |

### <a name="image-example-1-a-text-range-that-contains-an-embedded-image"></a>Abbildung Beispiel 1: Ein Textbereich, der ein eingebettetes Bild enthält

Der folgende Textbereich enthält ein eingebettetes Bild eines Hotels.

 {Das Bild ![Abbildung eines Motivs](images/shuttle.jpg) ist in text} eingebettet.

Das Aufrufen der Methoden [**IUIAutomationTextRange::GetText,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) [**GetEnclosingElement,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)und [**IUIAutomationTextPattern::RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) führt zu den in der folgenden Tabelle beschriebenen Verhaltensweisen.

| Aufgerufene Methode                                                                                                                                                                                                                                                    | Ergebnis                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                                                                                                                                                                                 | Gibt die Zeichenfolge "Das Bild ist in Text eingebettet" zurück. Alttext, der dem Bild zugeordnet ist, ist nicht im Textstream enthalten.                |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)                                                                                                                                                         | Gibt das innerste Benutzeroberflächenautomatisierung -Element zurück, das den Textbereich einschließt, in diesem Fall das Element, das den Textanbieter selbst darstellt. |
| [**IUIAutomationTextRange::GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)                                                                                                                                                                         | Gibt ein Benutzeroberflächenautomatisierung -Element zurück, das das Bildsteuerelement darstellt.                                                                               |
| [**IUIAutomationTextPattern::RangeFromChild,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) wobei das Benutzeroberflächenautomatisierung Element von der vorherigen [**IUIAutomationTextRange::GetChildren-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) zurückgegeben wurde. | Gibt den degenerieren Bereich zurück.                                                                                                                 |

### <a name="image-example-2-a-text-range-that-partially-spans-the-content-of-a-text-container"></a>Abbildung Beispiel 2: Ein Textbereich, der den Inhalt eines Textcontainers teilweise umfasst

Der folgende Textbereich umfasst teilweise den Inhalt eines Textcontainers. Der Textcontainer enthält ein eingebettetes Bild, das nicht im Textbereich enthalten ist.

 {Das Image} ![Abbildung eines Motivs](images/shuttle.jpg) ist in Text eingebettet.

Das Aufrufen der Methoden [**IUIAutomationTextRange::GetText,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)und [**Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) führt zu den in der folgenden Tabelle beschriebenen Verhaltensweisen.

| Aufgerufene Methode                                                                                                          | Ergebnis                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                                       | Gibt die Zeichenfolge „Das Bild“ zurück.                                                                                                                                                                                                                                                 |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)               | Gibt das innerste Benutzeroberflächenautomatisierung -Element zurück, das den Textbereich einschließt, in diesem Fall das Element, das den Textanbieter selbst darstellt.                                                                                                                                   |
| [**IUIAutomationTextRange::Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) mit Parametern von (**TextUnit \_ Word**, 2). | Verschiebt den Textbereichsabschnitt nach „ist“. Da nur textbasierte eingebettete Objekte als Teil des Textstreams betrachtet werden, wirkt sich das Bild in diesem Beispiel nicht auf [**IUIAutomationTextRange::Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) oder seinen Rückgabewert aus, in diesem Fall 2. |

### <a name="table"></a>Tabelle

### <a name="table-example-1-gets-the-text-container-from-the-content-of-a-cell"></a>Tabelle Beispiel 1: Ruft den Textcontainer aus dem Inhalt einer Zelle ab.

Die folgende Tabelle ruft den Textcontainer aus dem Inhalt einer Zelle ab.

| Zelle mit Bild                                            | Zelle mit Text |
|------------------------------------------------------------|----------------|
| ![Abbildung eines Motivs](images/shuttle.jpg)           | X              |
| ![Abbildung des Raumes und eines Kops](images/space.jpg) | J              |
| ![Abbildung eines Motivs](images/microscope.jpg)     | Z              |

Das Aufrufen der Methoden [**IUIAutomationGridPattern::GetItem,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) [**IUIAutomationTextPattern::RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild)und [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) führt zu den in der folgenden Tabelle beschriebenen Verhaltensweisen.

| Aufgerufene Methode                                                                                                                                                                                                                       | Ergebnis                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationGridPattern::GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) mit Parametern (0, 0).                                                                                                                        | Gibt das Benutzeroberflächenautomatisierung -Element zurück, das den Inhalt der Tabellenzelle darstellt. In diesem Fall ist das Element ein Textsteuerelement.                                                               |
| [**iuiautomationtextpattern::rangefromchild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild)                                                                                                                                  | gibt den Bereich des Bilds zurück. ![Abbildung eines Motivs](images/shuttle.jpg).                                                                                                            |
| [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) für das Objekt, das von der vorherigen [**IUIAutomationTextPattern::RangeFromChild-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) zurückgegeben wurde. | Gibt das Benutzeroberflächenautomatisierung -Element zurück, das die Tabellenzelle darstellt. In diesem Fall ist das -Element ein Textsteuerelement, das das [TableItem-Steuerelementmuster](uiauto-implementingtableitem.md) unterstützt. |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) für das Objekt, das von der vorherigen **GetEnclosingElement-Methode** zurückgegeben wurde.                                                    | Gibt das Benutzeroberflächenautomatisierung -Element zurück, das die Tabelle darstellt.                                                                                                                                   |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) für das Objekt, das von der vorherigen **GetEnclosingElement-Methode** zurückgegeben wurde.                                                    | Gibt das Benutzeroberflächenautomatisierung -Element zurück, das den Textanbieter selbst darstellt.                                                                                                                 |

### <a name="table-example-2-gets-the-text-content-of-a-cell"></a>Tabelle Beispiel 2: Ruft den Textinhalt einer Zelle ab

Die Tabelle im vorherigen Beispiel ruft den Textinhalt einer Zelle ab.

Der Aufruf der [**Methoden IUIAutomationGridPattern::GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) und [**IUIAutomationTextPattern::RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) führt zu den in der folgenden Tabelle beschriebenen Verhaltensweisen.

| Aufgerufene Methode                                                                                                                                                                                                                                                          | Ergebnis                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationGridPattern::GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) mit Parametern (1,1).                                                                                                                                                            | Gibt das Benutzeroberflächenautomatisierung -Element zurück, das den Inhalt der Tabellenzelle darstellt. In diesem Fall ist das Element ein Textsteuerelement. |
| [**IUIAutomationTextPattern::RangeFromChild,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) wobei das Benutzeroberflächenautomatisierung Element das Objekt ist, das von der vorherigen [**IUIAutomationGridPattern::GetItem-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) zurückgegeben wurde. | Gibt „Y“ zurück.                                                                                                               |

Wenn der Textbereich in eine eingebettete Tabelle eintritt, sollte jede Textzeile in einer Zelle als Zeile behandelt werden, wenn ein Dokument von [**TextUnit \_ Line**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)durchlaufen wird.

## <a name="related-topics"></a>Zugehörige Themen

### <a name="conceptual"></a>Konzept

- [Informationen zu Text- und TextRange-Steuerelementmustern](uiauto-about-text-and-textrange-patterns.md)
- [Benutzeroberflächenautomatisierung Textattribute](uiauto-textattributes.md)
- [Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
- [Benutzeroberflächenautomatisierung-Unterstützung für Textinhalte](uiauto-ui-automation-textpattern-overview.md)