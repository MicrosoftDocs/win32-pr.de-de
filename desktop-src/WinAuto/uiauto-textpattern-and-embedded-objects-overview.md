---
title: Verfügbar machen von eingebetteten Objekten durch die Benutzeroberflächen Automatisierung
description: In diesem Thema wird beschrieben, wie die Microsoft-Benutzeroberflächen Automatisierung eingebettete Objekte oder untergeordnete Elemente in einem Textdokument oder Container verfügbar macht.
ms.assetid: 5ecf5e94-5329-4abb-aedb-4e303688e5f7
keywords:
- UI-Automatisierung, Übersicht über Textmuster
- UI-Automatisierung, Übersicht über Text Steuerelemente
- UI-Automatisierung, Text-Steuerelement Muster
- UI-Automatisierung, Übersicht über eingebettete Objekte
- Benutzeroberflächen Automatisierung, verfügbar machen von eingebetteten Objekten
- Benutzeroberflächen Automatisierung, Szenarien für eingebettete Objekte
- Textmuster, Info
- Text Steuerelemente, Info
- Text-Steuerelement Muster
- Steuerelement Muster, Text
- Eingebettete Objekte
- verfügbar machen von eingebetteten Objekten
ms.topic: article
ms.date: 08/31/2019
ms.openlocfilehash: b85d7fa9e068400e3a339625acad1036a4cdd111
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727512"
---
# <a name="how-ui-automation-exposes-embedded-objects"></a>Verfügbar machen von eingebetteten Objekten durch die Benutzeroberflächen Automatisierung

In diesem Thema wird beschrieben, wie Microsoft UI Automation die Text-und TextRange-Steuerelement Muster verwendet, um eingebettete Objekte (untergeordnete/Nachfolger Elemente) in einem Text Dokument oder Container verfügbar zu machen.

Bei der Benutzeroberflächen Automatisierung ist ein eingebettetes Objekt ein beliebiges Element mit nicht-Text Grenzen, z. b. ein Bild, einen Hyperlink, eine Tabelle oder einen Dokumenttyp (Microsoft Excel-Kalkulations Tabelle, Microsoft Windows-Mediendatei usw.).

> [!NOTE]
> Dies unterscheidet sich von der Component Object Model (com)-OLE-Definition (siehe [eingebettete Objekte](../com/embedded-objects.md)), in der ein Element in einer Anwendung erstellt und in eine andere Anwendung eingebettet oder verknüpft wird. Ob das Objekt in der ursprünglichen Anwendung bearbeitet werden kann, ist im Kontext der Benutzeroberflächen Automatisierung irrelevant.

## <a name="embedded-objects-and-the-ui-automation-tree"></a>Eingebettete Objekte und die Benutzeroberflächenautomatisierungs-Struktur

Eingebettete Objekte werden als einzelne Elemente in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur behandelt. Sie werden als untergeordnete Elemente des Text Containers verfügbar gemacht, damit Sie über das gleiche Objektmodell wie andere Steuerelemente in der Benutzeroberflächen Automatisierung darauf zugreifen können.

In der folgenden Tabelle sind Beispiele für Container-und nicht-Container-Elemente aufgelistet.

:::row:::
   :::column span="2":::

      **Containerelemente**

   :::column-end:::
   :::column span="":::

      **Nicht-Container-Elemente**

   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::

- Kalender
- Combobox
- DataGrid
- Dokument
- Bearbeiten
- Gruppieren
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

In der folgenden Abbildung wird ein Text Container (Dokument) mit einer eingebetteten Tabelle und einem Bild angezeigt.

![Darstellung eines Dokuments mit einer eingebetteten Tabelle und einem Bild](images/embeddedtable.jpg)

Die Inhaltsansicht der Benutzeroberflächen Automatisierung des vorangehenden Dokuments ist im folgenden Diagramm dargestellt.

![Diagramm der Inhaltsansicht der Benutzeroberflächen Automatisierung eines Dokuments mit eingebetteten Objekten](images/contenttree.jpg)

### <a name="compatible-and-non-compatible-embedded-objects"></a>"Kompatible" und "nicht kompatible" eingebettete Objekte

Einige Benutzeroberflächenautomatisierungs-Anbieter verwenden denselben Text Speicher für jedes TextPattern-Objekt, das Sie enthalten.  Objekte, die von demselben Text Speicher wie deren Container unterstützt werden, werden als "kompatible" eingebettete Objekte bezeichnet. Diese Objekte können Textpattern-Objekte selbst sein, und in diesem Fall sind Ihre Textbereiche mit Textbereichen vergleichbar, die aus Ihrem Container abgerufen werden. Dies ermöglicht es den Anbietern, Client Informationen zu den einzelnen TextPattern-Objekten so verfügbar zu machen, als handele es sich um einen großen Text Anbieter.

Allerdings können Anbieter verschiedene Text Speicher für verschiedene TextPattern-Objekte verwenden, die in einem TextPattern-Container eingebettet sind. Objekte, die nicht durch den Text Speicher des Containers gesichert werden, werden als "nicht kompatible" eingebettete Objekte bezeichnet. Diese Typen von eingebetteten Objekten sind möglicherweise TextPattern-basierte Objekte.  

In der folgenden Tabelle sind einige Beispiele kompatibler und nicht kompatibler eingebetteter Objekte aufgeführt.

|   | Kompatible eingebettete Objekte | Nicht kompatible eingebettete Objekte |
| --- | --- | --- |
| Nicht-TextPattern Embedded-Objekte | Schaltfläche in Microsoft Edge<br>Datentabelle in Microsoft Edge | Schaltfläche in richtextblock im XAML-Framework von Microsoft<br>Bilder mit alt-Text in Microsoft Edge<br>ListView mit ListItems in richtextblock im XAML-Framework von Microsoft |
| TextPattern Embedded-Objekte | Eingabe Steuerelement vom Typ "Text" in Microsoft Edge<br>Tabelle in einem Word-Dokument | TextBox-Element in einem Microsoft Word-Dokument |

## <a name="exposing-embedded-objects"></a>Verfügbar machen von eingebetteten Objekten

Die [Text-und TextRange](uiauto-implementingtextandtextrange.md) -Steuerelement Muster machen Eigenschaften und Methoden verfügbar, die das Navigieren und Abfragen von eingebetteten Objekten vereinfachen.

Der Text Inhalt (oder innere Text) eines Text Containers und ein eingebettetes Objekt, z. b. ein Link oder eine Tabellenzelle, werden in der Steuerelement Ansicht und der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur als einzelner, kontinuierlicher Textstream verfügbar gemacht. Objekt Grenzen werden ignoriert. Wenn ein Benutzeroberflächenautomatisierungs-Client den Text abruft, um ihn zu empfangen, zu interpretieren oder zu analysieren, sollte der Textbereich auf besondere Fälle, z. b. eine Tabelle mit Text Inhalt oder andere eingebettete Objekte, geprüft werden. Rufen Sie [**iuiautomationtextrange:: GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) auf, um eine [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Schnittstelle für jedes eingebettete Objekt zu erhalten, und rufen Sie dann [**iuiautomationtextpattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) auf, um einen Textbereich für jedes Element zu erhalten. Dies wird rekursiv ausgeführt, bis der gesamte Textinhalt abgerufen wurde.

> [!NOTE]
> Bei einem degenerierten (oder reduzierten) Bereich sind der Start Endpunkt und der endendpunkt identisch. Degenerierte Bereiche werden häufig verwendet, um die Textcursor Position durch die Methoden " [GetSelection](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextprovider-getselection) " und " [getcaretrange](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextprovider2-getcaretrange) " von [ITextProvider](/windows/win32/api/uiautomationcore/nn-uiautomationcore-itextprovider) anzugeben.

Das folgende Diagramm zeigt einen Textstream mit eingebetteten Objekten und deren Bereichs spannen.

![Diagramm, das einen Textstream mit eingebetteten Objekten und deren Bereichs spannen anzeigt](images/rangespans.jpg)

## <a name="embedded-objects-and-textunit"></a>Eingebettete Objekte und TextUnit

Ein [ITextProvider](/windows/win32/api/uiautomationcore/nn-uiautomationcore-itextprovider) -Objekt kann von einem angegebenen [TextUnit](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textunit)durchlaufen werden. Anbieter, die eingebettete Objekte enthalten, können auf die gleiche Weise durchlaufen werden, eingebettete Objekte wirken sich jedoch auf das durchlaufen aus. Beachten Sie Folgendes:

- Alle nicht kompatiblen eingebetteten Objekte werden durch das Ersetzungs Zeichen U + fffc im Text Speicher des TextPattern des Container Elements dargestellt. Sie wird auch als Zeichen Einheit und als Word-Einheit betrachtet.
- Kompatible eingebettete Objekte können aus mehreren Zeichen und Wörtern bestehen.
- Das einschließende Element ist das unterste Element, das den gesamten Textbereich umfasst.
- Untergeordnete Elemente eines Bereichs sind auch untergeordnete Elemente eines Container Elements, das teilweise oder vollständig in den Bereich eingeschlossen ist.
- Im Idealfall (insbesondere bei Container Elementen wie Table) geht eine Wort Grenze nicht über die Objekt Grenze hinaus. Im folgenden Beispiel enthält die Word-Einheit "Bar" keine Textposition, die sich außerhalb des Tags befindet `</td>` ( `<br \>` ist nicht Teil des Worts "Bar").

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

- Im allgemeinen `<br \>` wird als einzelnes Wort behandelt, sodass es nicht über eine Linien Grenze hinausgeht.
- Eine Ausnahme von der vorherigen Regel besteht darin, dass eine Word-Text Einheit vollständige Objekte enthält. Beispielsweise `<p>Hello <a href="#">link</a> here.</p>` enthält, das Inline Container enthält, die Wörter "Hello", "Link" und "This". Wobei "Link" ein Textpattern-Objekt als einschließendes Element und ein Link Objekt als untergeordnetes Element aufweist.
- Im Fall von Zeicheneinheiten ist das Objekt das einschließende Element (Text Einheiten wie dieses sollten keine untergeordneten Elemente aufweisen).
- Annotation-Objekte sollten nicht als eingebettetes Objekt dargestellt werden. Beispielsweise das vorhanden sein anderer Autoren Bezeichner in einem gemeinsam verfassten Dokument.
- Eingebettete Objekte nehmen mindestens eine Cursorposition an, die Anmerkung ist nur Metadaten.
- Jede Objekt Grenze (Start und Ende) wird durch einen Format Umbruch im Textpattern-Dokumentbereich dargestellt.
- Bei HTML führt jedes HTML-Tag nicht notwendigerweise zu einem Benutzeroberflächenautomatisierungs-Objekt. Beispielsweise müssen Inhalte innerhalb von <em></em> Schwerpunkt Tags nicht als-Element, sondern als Textstream dargestellt werden, in dem UIA_IsItalicAttributeId "true" zurückgibt.
- Der Start Endpunkt ist inklusiv und der bevorzugte Endpunkt, während der Endpunkt exklusiv ist. Dies ist nützlich, wenn der Bereich degeneriert wird und die Start-und Endpunkte derselben Position für diesen Bereich angehören.

## <a name="comparing-embedded-objects"></a>Vergleichen von eingebetteten Objekten

Als vergleichbar bezeichnete TextPattern-Objekte, die sich in einer ähnlichen untergeordneten Beziehung befinden und denselben Sicherungs Text Speicher gemeinsam verwenden. In diesem Fall können Bereiche von einem der Textpattern-Objekte mithilfe von [ITextRangeProvider:: Compare](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-compare) und [ITextRangeProvider:: compareEndPoints](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-compareendpoints)verglichen werden. Beide führen zu einem gültigen numerischen Wert, der die relative Position angibt.

Ein nicht-TextPattern-Objekt, das in ein Textpattern-Objekt eingebettet ist, ist mit dem TextPattern vergleichbar, wenn das Objekt einen gültigen Bereich im Textpattern ([ITextProvider:: RangeFromChild](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextprovider-rangefromchild)) aufweist und der Inhalt hinter dem Textbereich nicht leer ist und kein Ersatz Zeichen ist.

## <a name="embedded-textpattern-objects-and-the-document-textunit"></a>Eingebettete TextPattern-Objekte und das Dokument TextUnit

Bei eingebetteten TextPattern-Objekten erkennt die [Dokument](/windows/win32/api/uiautomationcore/ne-uiautomationcore-textunit) Einheit nur den Inhalt, der in diesem Element enthalten ist.

### <a name="word-textpattern-element-hierarchy"></a>Word-TextPattern-Element Hierarchie

- Das document-Element implementiert TextPattern, und [Document](/windows/win32/api/uiautomationcore/ne-uiautomationcore-textunit) gibt den gesamten Word-Dokumentbereich zurück.
- Einzelne Seiten des Dokuments, das TextPattern und [Document](/windows/win32/api/uiautomationcore/ne-uiautomationcore-textunit) implementiert, geben den Inhalt dieser einzelnen Seiten zurück (auch wenn die Seiten denselben Text Speicher mit dem gesamten Dokument TextPattern verwenden).

### <a name="webpage-and-text-input-controls-in-edge"></a>Steuerelemente für Webseiten und Texteingaben in Edge

- Das Hauptelement der Webseite für Webseiten implementiert TextPattern und macht den gesamten Webseiteninhalt verfügbar.
- Die einzelnen Texteingabe Steuerelemente unterstützen TextPattern, wobei ein Dokumentbereich den in jedem Eingabefeld enthaltenen Text darstellt (auch wenn Sie denselben Text Speicher mit der ganzen Webseite gemeinsam verwenden).

## <a name="common-scenarios"></a>Häufige Szenarios

In diesem Abschnitt werden Beispiele für gängige Szenarien vorgestellt, die eingebettete Objekte umfassen: Hyperlinks, Bilder und Tabellen. In den folgenden Beispielen stellt die linke geschweifter Klammer ({) den Start Endpunkt des Text Bereichs dar, und die Rechte geschweifter Klammer (}) stellt den endendpunkt dar.

### <a name="hyperlink-example-1-a-text-range-that-contains-an-embedded-text-hyperlink"></a>Hyperlink-Beispiel 1: ein Textbereich, der einen eingebetteten Textlink enthält

Der folgende Textbereich enthält einen eingebetteten Textlink.

  {Die URL https://www.microsoft.com ist in den Text eingebettet}.

Das Aufrufen der Methoden [**iuiautomationtextrange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext), [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement), [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)und [**iuiautomationtextpattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) führt zu den in der folgenden Tabelle beschriebenen Verhalten.

| Aufgerufene Methode                                                                                                                                                                                                                                                     | Ergebnis                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iuiautomationtextrange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                                                                                                                                                                                  | Gibt die Zeichenfolge "die URL https://www.microsoft.com ist in Text eingebettet" zurück.                                                                               |
| [**Iuiautomationtextrange:: GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)                                                                                                                                                          | Gibt das innerste Benutzeroberflächenautomatisierungs-Element zurück, das den Textbereich einschließt, in diesem Fall das Automation-Element, das den Text Anbieter darstellt. |
| [**Iuiautomationtextrange:: GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)                                                                                                                                                                          | Gibt ein Benutzeroberflächenautomatisierungs-Element zurück, das das Link Steuerelement                                                                                      |
| [**Iuiautomationtextpattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild), wobei das Benutzeroberflächenautomatisierungs-Element von der vorherigen [**iuiautomationtextrange:: GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) -Methode zurückgegeben wurde. | Gibt den Bereich zurück, der " https://www.microsoft.com " darstellt.                                                                                            |
### <a name="hyperlink-example-2-a-text-range-that-partially-spans-an-embedded-text-hyperlink"></a>Hyperlink-Beispiel 2: ein Textbereich, der sich teilweise über einen eingebetteten Textlink erstreckt

Der folgende Textbereich erstreckt sich teilweise über einen eingebetteten Textlink.

  Die URL "https://{www}" ist in den Text eingebettet.

Das Aufrufen der Methoden [**iuiautomationtextrange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext), [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)und [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) führt zu den in der folgenden Tabelle beschriebenen Verhalten.

| Aufgerufene Methode                                                                                            | Ergebnis                                                                                                         |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**Iuiautomationtextrange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                         | Gibt die Zeichenfolge „www“ zurück.                                                                                      |
| [**Iuiautomationtextrange:: GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) | Gibt das innerste Benutzeroberflächenautomatisierungs-Element zurück, das den Textbereich einschließt. in diesem Fall das Link Steuerelement. |
| [**Iuiautomationtextrange:: GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)                 | Gibt **null** zurück, da der Textbereich nicht die gesamte URL-Zeichenfolge umfasst.                                   |

### <a name="hyperlink-example-3-a-text-range-that-partially-spans-the-content-of-a-text-container"></a>Hyperlink-Beispiel 3: ein Textbereich, der den Inhalt eines Text Containers teilweise umfasst

Der folgende Textbereich erstreckt sich teilweise über den Inhalt eines Text Containers. Der Textcontainer enthält einen eingebetteten Textlink, der nicht im Textbereich enthalten ist.

  {Die URL} https://www.microsoft.com ist in den Text eingebettet.

Das Aufrufen der Methoden [**iuiautomationtextrange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext), [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)und [**Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) führt zu den in der folgenden Tabelle beschriebenen Verhaltensweisen.

| Aufgerufene Methode                                                                                            | Ergebnis                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iuiautomationtextrange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                         | Gibt die Zeichenfolge „Die URL“ zurück.                                                                                                                                                                                                     |
| [**Iuiautomationtextrange:: GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) | Gibt das innerste Benutzeroberflächenautomatisierungs-Element zurück, das den Textbereich einschließt, in diesem Fall das Element, das den Text Anbieter darstellt.                                                                                     |
| [**Iuiautomationtextrange:: Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move)                               | Verschiebt den Text Bereichs Bereich in "https://", da der Text des Links aus einzelnen Wörtern besteht. In diesem Fall wird der Link nicht als einzelnes Objekt behandelt.<br/> Die URL {http} ist in den Text eingebettet.<br/> |

### <a name="image-example-1-a-text-range-that-contains-an-embedded-image"></a>Bildbeispiel 1: ein Textbereich, der ein eingebettetes Bild enthält

Der folgende Textbereich enthält ein eingebettetes Bild eines-Shuttles.

 {Das Bild ![Abbildung eines-Shuttles](images/shuttle.jpg) ist in den Text eingebettet}.

Das Aufrufen der Methoden [**iuiautomationtextrange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext), [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement), [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)und [**iuiautomationtextpattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) führt zu den in der folgenden Tabelle beschriebenen Verhalten.

| Aufgerufene Methode                                                                                                                                                                                                                                                    | Ergebnis                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iuiautomationtextrange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                                                                                                                                                                                 | Gibt die Zeichenfolge "das Bild ist in den Text eingebettet" zurück. Jeder mit dem Bild verknüpfte alt-Text ist nicht im Textstream enthalten.                |
| [**Iuiautomationtextrange:: GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)                                                                                                                                                         | Gibt das innerste Benutzeroberflächenautomatisierungs-Element zurück, das den Textbereich einschließt, in diesem Fall das Element, das den Text Anbieter darstellt. |
| [**Iuiautomationtextrange:: GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)                                                                                                                                                                         | Gibt ein Benutzeroberflächenautomatisierungs-Element zurück, das das Bild Steuerelement                                                                               |
| [**Iuiautomationtextpattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) , wobei das Benutzeroberflächenautomatisierungs-Element von der vorherigen [**iuiautomationtextrange:: GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) -Methode zurückgegeben wurde. | Gibt den degenerierten Bereich zurück.                                                                                                                 |

### <a name="image-example-2-a-text-range-that-partially-spans-the-content-of-a-text-container"></a>Bildbeispiel 2: ein Textbereich, der den Inhalt eines Text Containers teilweise umfasst

Der folgende Textbereich erstreckt sich teilweise über den Inhalt eines Text Containers. Der Textcontainer enthält ein eingebettetes Bild, das nicht im Textbereich enthalten ist.

 {Das Image} ![Abbildung eines-Shuttles](images/shuttle.jpg) ist in den Text eingebettet.

Das Aufrufen der Methoden [**iuiautomationtextrange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext), [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)und [**Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) führt zu den in der folgenden Tabelle beschriebenen Verhaltensweisen.

| Aufgerufene Methode                                                                                                          | Ergebnis                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iuiautomationtextrange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                                       | Gibt die Zeichenfolge „Das Bild“ zurück.                                                                                                                                                                                                                                                 |
| [**Iuiautomationtextrange:: GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)               | Gibt das innerste Benutzeroberflächenautomatisierungs-Element zurück, das den Textbereich einschließt, in diesem Fall das Element, das den Text Anbieter darstellt.                                                                                                                                   |
| [**Iuiautomationtextrange:: Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) with Parameters of (**TextUnit \_ Word**, 2). | Verschiebt den Textbereichsabschnitt nach „ist“. Da nur textbasierte eingebettete Objekte als Teil des Textstreams betrachtet werden, wirkt sich das Bild in diesem Beispiel nicht auf [**iuiautomationtextrange:: Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) oder seinen Rückgabewert aus, in diesem Fall 2. |

### <a name="table"></a>Tabelle

### <a name="table-example-1-gets-the-text-container-from-the-content-of-a-cell"></a>Tabellen Beispiel 1: Abrufen des Text Containers aus dem Inhalt einer Zelle

In der folgenden Tabelle wird der Text Container aus dem Inhalt einer Zelle abgerufen.

| Zelle mit Bild                                            | Zelle mit Text |
|------------------------------------------------------------|----------------|
| ![Abbildung eines-Shuttles](images/shuttle.jpg)           | X              |
| ![Darstellung von Leerraum und einem Teleskop](images/space.jpg) | J              |
| ![Abbildung eines Mikro-Skund](images/microscope.jpg)     | Z              |

Das Aufrufen der Methoden [**iuiautomationgridpattern:: GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem), [**iuiautomationtextpattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild)und [**iuiautomationtextrange:: GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) führt zu den in der folgenden Tabelle beschriebenen Verhalten.

| Aufgerufene Methode                                                                                                                                                                                                                       | Ergebnis                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iuiautomationgridpattern:: GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) mit Parametern (0,0).                                                                                                                        | Gibt das Benutzeroberflächenautomatisierungs-Element zurück, das den Inhalt der Tabellenzelle darstellt. in diesem Fall ist das Element ein Text Steuerelement.                                                               |
| [**iuiautomationtextpattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild)                                                                                                                                  | Gibt den Bereich des Bilds zurück. ![Abbildung eines-Shuttles](images/shuttle.jpg).                                                                                                            |
| [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) für das Objekt, das von der vorherigen [**iuiautomationtextpattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) -Methode zurückgegeben wurde. | Gibt das Benutzeroberflächenautomatisierungs-Element zurück, das die Tabellenzelle darstellt In diesem Fall ist das-Element ein Text Steuerelement, das das [TableItem](uiauto-implementingtableitem.md) -Steuerelement Muster unterstützt. |
| [**Iuiautomationtextrange:: GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) für das Objekt, das von der vorherigen **GetEnclosingElement** -Methode zurückgegeben wurde.                                                    | Gibt das Benutzeroberflächenautomatisierungs-Element zurück, das die Tabelle darstellt                                                                                                                                   |
| [**Iuiautomationtextrange:: GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) für das Objekt, das von der vorherigen **GetEnclosingElement** -Methode zurückgegeben wurde.                                                    | Gibt das Benutzeroberflächenautomatisierungs-Element zurück, das den Text Anbieter selbst darstellt.                                                                                                                 |

### <a name="table-example-2-gets-the-text-content-of-a-cell"></a>Tabellen Beispiel 2: Abrufen des Text Inhalts einer Zelle

In der Tabelle im vorhergehenden Beispiel wird der Text Inhalt einer Zelle abgerufen.

Das Aufrufen der Methoden [**iuiautomationgridpattern:: GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) und [**iuiautomationtextpattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) führt zu den in der folgenden Tabelle beschriebenen Verhalten.

| Aufgerufene Methode                                                                                                                                                                                                                                                          | Ergebnis                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**Iuiautomationgridpattern:: GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) mit Parametern (1, 1).                                                                                                                                                            | Gibt das Benutzeroberflächenautomatisierungs-Element zurück, das den Inhalt der Tabellenzelle darstellt. In diesem Fall ist das-Element ein Text Steuerelement. |
| [**Iuiautomationtextpattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) , wobei das Benutzeroberflächenautomatisierungs-Element das Objekt ist, das von der vorherigen [**iuiautomationgridpattern:: GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) -Methode zurückgegeben wurde. | Gibt „Y“ zurück.                                                                                                               |

Beim Durchlaufen eines Dokuments durch [**TextUnit- \_ Zeile**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit), wenn der Textbereich in eine eingebettete Tabelle wechselt, sollte jede Textzeile in einer Zelle als Linie behandelt werden.

## <a name="related-topics"></a>Zugehörige Themen

### <a name="conceptual"></a>Konzept

- [Informationen zu Text-und TextRange-Steuerelement Mustern](uiauto-about-text-and-textrange-patterns.md)
- [Benutzeroberflächenautomatisierungs-Text Attribute](uiauto-textattributes.md)
- [Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
- [Benutzeroberflächenautomatisierungs-Unterstützung für Textinhalte](uiauto-ui-automation-textpattern-overview.md)