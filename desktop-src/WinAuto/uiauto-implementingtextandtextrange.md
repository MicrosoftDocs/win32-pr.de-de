---
title: Text-und TextRange-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von ITextProvider, ITextProvider2 und ITextRangeProvider, einschließlich Informationen zu Eigenschaften und Methoden.
ms.assetid: 4d541c31-11f7-4d7e-a0e0-9ed1da873d07
keywords:
- Benutzeroberflächen Automatisierung, Implementieren von Text-Steuerelement Mustern
- Benutzeroberflächen Automatisierung, Implementieren des TextRange-Steuerelement Musters
- UI-Automatisierung, Text-Steuerelement Muster
- UI-Automatisierung, TextRange-Steuerelement Muster
- UI-Automatisierung, ITextProvider
- UI-Automatisierung, ITextRangeProvider
- ITextProvider
- ITextRangeProvider
- Implementieren des Text Steuerelement Musters der Benutzeroberflächen Automatisierung
- Implementieren des Text-Steuerelement Musters der Benutzeroberflächen Automatisierung
- Text-Steuerelement Muster
- TextRange-Steuerelement Muster
- Steuerelement Muster, ITextProvider
- Steuerelement Muster, ITextRangeProvider
- Steuerelement Muster, Implementieren von Benutzeroberflächenautomatisierungs-Text
- Steuerelement Muster, Implementieren der Benutzeroberflächenautomatisierungs-TextRange
- Steuerelement Muster, Text
- Steuerelement Muster, TextRange
- Schnittstellen, ITextProvider
- Schnittstellen, ITextRangeProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f53429dc8ec137a83b6a40db377b5c84aeb36120
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104552756"
---
# <a name="text-and-textrange-control-patterns"></a>Text-und TextRange-Steuerelement Muster

Beschreibt Richtlinien und Konventionen für das Implementieren von [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider), [**ITextProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2)und [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider), einschließlich Informationen zu Eigenschaften und Methoden. Das **Text** -Steuerelement Muster ermöglicht Anwendungen und Steuerelementen, ein einfaches Text Objektmodell verfügbar zu machen, sodass Clients Textinhalte, Text Attribute und eingebettete Objekte aus textbasierten Steuerelementen abrufen können.

Um das **Text** Steuerelement Muster zu unterstützen, implementieren Steuerelemente die [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) -und [**ITextProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2) -Schnittstellen. Zu den Steuerelement Typen, die das **Text** -Steuerelement Muster unterstützen sollten, gehören die Steuerelement Typen [Bearbeiten](uiauto-supporteditcontroltype.md) und [Dokument](uiauto-supportdocumentcontroltype.md) sowie alle anderen Steuerelement Typen, mit denen der Benutzer Text eingeben oder schreibgeschützten Text auswählen kann.

Das **Text** -Steuerelement Muster kann mit anderen Microsoft UI Automation-Steuerelement Mustern verwendet werden, um verschiedene Typen von eingebetteten Objekten im Text zu unterstützen, einschließlich Tabellen, Hyperlinks und Befehls Schaltflächen.

Die [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) -und [**ITextProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2) -Schnittstellen enthalten eine Reihe von Methoden zum Abrufen von Textbereichen. Ein *Textbereich* ist ein Objekt, das einen zusammenhängenden Textbereich darstellt – oder mehrere, nicht zusammenhängende Text spannen – in einem Text Container. Eine **ITextProvider** -Methode ruft einen Textbereich ab, der das gesamte Dokument darstellt, während andere Textbereiche abrufen, die einen Teil des Dokuments darstellen, z. b. den markierten Text, den sichtbaren Text oder ein Objekt, das in den Text eingebettet ist.

Ein Text Bereichs Objekt wird durch das **TextRange** -Steuerelement Muster dargestellt, das über die [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) -Schnittstelle implementiert wird. Das **TextRange** -Steuerelement Muster stellt Methoden und Eigenschaften bereit, mit denen Informationen über den Text im Bereich verfügbar gemacht, die Endpunkte des Bereichs verschoben, Text ausgewählt oder deaktiviert werden, der Bereich in die Ansicht gewechselt wird usw.

Weitere Informationen zu **Text** -und **TextRange** -Steuerelement Mustern finden Sie [unter Unterstützung der Benutzeroberflächen Automatisierung für Textinhalte](uiauto-ui-automation-textpattern-overview.md).

Beginnend mit Windows 8.1 Anbietern die [**ITextRangeProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider2) -Schnittstelle implementieren. Dies ermöglicht das Aufrufen von Kontextmenüs, die einem Textbereich zugeordnet sind. Dies unterstützt Szenarien wie z. b. automatische Textkorrektur oder Eingabemethoden-Editor (IME) Candidate-Auswahl.

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **ITextProvider**](#required-members-for-itextprovider)
-   [Erforderliche Member für **ITextRangeProvider**](#required-members-for-itextrangeprovider)
-   [Unterstützende Text Bereiche](#supporting-text-ranges)
    -   [Bearbeiten eines Text Bereichs nach Text Einheit](#manipulating-a-text-range-by-text-unit)
    -   [Auswählen von Text in einem Textbereich](#selecting-text-in-a-text-range)
    -   [Abrufen von Text aus einem Textbereich](#acquiring-text-from-a-text-range)
    -   [Implementieren von ShowContextMenu](#implementing-showcontextmenu)
-   [Interoperabilität mit der System Einfügemarke](#interoperability-with-the-system-caret)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des **Text** -Steuerelement Musters die folgenden Richtlinien und Konventionen:

-   Jedes Steuerelement, das den Zugriff auf Text ermöglicht (z. b. Text eingeben oder schreibgeschützten Text auswählen), sollte das **Text** -Steuerelement Muster unterstützen.
-   Das **Text** -Steuerelement Muster kann mit allen Benutzeroberflächen Elementen verwendet werden, die Text darstellen, auch eine statische Bezeichnung auf einem Standard-Schaltflächen-Steuerelement. Es ist jedoch für statische Text Steuerelemente, die nicht ausgewählt werden können oder für die keine Einfügemarke vorhanden ist, nicht erforderlich.
-   Um sicherzustellen, dass der Text vollständig zugänglich ist, sollten Steuerelemente, die [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) implementieren, auch die [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) -Schnittstelle unterstützen **IValueProvider** ergänzt **ITextProvider** , indem er eine programmgesteuerte Methode zum Ändern des Texts bereitstellt. Außerdem bietet Sie eine bessere Kompatibilität mit hilfstechnologieclientanwendungen, einschließlich derjenigen, die auf Legacy Technologien wie z. b. Microsoft Active Accessibility basieren. Wenn beide Steuerelement Muster implementiert werden, entsprechen das **TextChanged** -Ereignis ([**UIA \_ Text \_ textchangeabventid**](uiauto-event-ids.md)) und das **automationpropertychanged** -Ereignis ([**UIA \_ automationpropertychangetoventid**](uiauto-event-ids.md)) der **value** -Eigenschaft ([**UIA \_ valuevaluepropertyid**](uiauto-control-pattern-propids.md)). Beide Ereignisse müssen unterstützt werden.
-   Das **Text** -Steuerelement Muster unterstützt nur einen Stream von Text und einen Viewport pro Steuerelement. Wenn die Anwendung mehrere Ansichten von Dokumenten in Bereichen bietet, sollte jede Ansicht (Steuerelement) [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) unabhängig unterstützen.
-   Die [**ITextProvider:: GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection) -Methode gibt möglicherweise einen einzelnen Textbereich zurück, der den aktuell ausgewählten Text darstellt. Wenn ein Steuerelement die Auswahl mehrerer, nicht zusammenhängender Text spannen unterstützt, sollte die **GetSelection** -Methode ein Array zurückgeben, das eine [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) -Schnittstelle für jeden ausgewählten Textabschnitt enthält.
-   Das **Text** -Steuerelement Muster stellt die Einfügemarke als degenerierten (leeren) Text Bereich dar. Die [**ITextProvider:: GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection) -Methode sollte einen degenerierten Textbereich zurückgeben, wenn die Einfügemarke vorhanden und kein Text ausgewählt ist. Weitere Informationen finden Sie unter [Interoperabilität mit der System](#interoperability-with-the-system-caret)Einfügemarke.
-   Die Methode [**ITextProvider:: getvisibleraneriges**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getvisibleranges) gibt möglicherweise einen einzelnen Textbereich zurück, wenn ein zusammenhängender Textbereich im Viewport sichtbar ist, oder es wird ein Array von nicht zusammenhängenden Textbereichen zurückgegeben, die mehrere, teilweise sichtbare Textzeilen darstellen.
-   Die [**ITextProvider:: RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) -Methode sollte einen degenerierten Bereich zurückgeben, wenn das untergeordnete Element keinen Text enthält. Da ein eingebettetes Objekt Text einschließen kann, gibt die **RangeFromChild** -Methode möglicherweise nicht immer einen degenerierten Textbereich zurück. Weitere Informationen finden Sie unter [How UI Automation macht Embedded Objects](uiauto-textpattern-and-embedded-objects-overview.md)verfügbar.
-   Die [**ITextProvider:: RangeFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint) -Methode führt Treffer Tests im Dokumentbereich mithilfe der angegebenen Bildschirm Koordinaten aus. Der resultierende Textbereich sollte mit der Einfügemarke oder der Auswahl übereinstimmen, die durch Klicken auf den Speicherort an den angegebenen Bildschirm Koordinaten entstehen würde. Wenn sich z. b. ein Bild an den angegebenen Bildschirm Koordinaten befindet, sollte der resultierende Textbereich mit dem Textbereich identisch sein, den die [**ITextProvider:: RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) -Methode für das Bild erhalten würde. Wenn eine Client Anwendung einen Textbereich für den Speicherort in der Mitte der System Einfügemarke (der Einfügemarke) anfordert, sollte der resultierende Textbereich mit dem Speicherort des System Caretzeichen identisch sein.
-   Die [**ITextProvider::D ocenentrange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_documentrange) -Eigenschaft sollte immer einen Textbereich bereitstellen, der den gesamten Text enthält, der von der entsprechenden [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) -Implementierung unterstützt wird.
-   Das Ereignis [**UIA \_ Text \_ textchangedeventid**](uiauto-event-ids.md) muss ausgelöst werden, nachdem eine beliebige Text Änderung stattfindet, auch wenn die Änderung nicht im Viewport sichtbar ist. Der Anbieter sollte das Ereignis z. b. auch dann auswerfen, wenn der Benutzer genau denselben Text über den ausgewählten Text einfügt.
-   Der [**UIA \_ Text \_ textselectionchangedebug**](uiauto-event-ids.md) muss immer dann ausgelöst werden, wenn sich die Textauswahl ändert, oder wenn die Einfügemarke (Einfügemarke) zwischen dem Text bewegt wird.

Beachten Sie beim Implementieren des **TextRange** -Steuerelement Musters die folgenden Richtlinien und Konventionen:

-   Alle Methoden des **TextRange** -Steuerelement Musters sollten Text Vorgänge unabhängig vom Sichtbarkeits Zustand des Texts ausführen. Die Sichtbarkeit eines Text Bereichs kann immer durch Abfragen des **IsHidden** -Text Attributs ([**UIA \_ ishiddenattributeid**](uiauto-textattribute-ids.md)) bestimmt werden.
-   Wenn möglich, sollte ein Anbieter sicherstellen, dass alle Textänderungen, wie z. b. Löschvorgänge, Einfügungen und Verschiebungen, in den zugeordneten Text Bereichs Objekten (Instanzen der [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) -Schnittstelle) widergespiegelt werden und ein [**UIA \_ Text \_ -textchangedebug-**](uiauto-event-ids.md) Ereignis auslösen. Clients können das Ereignis als Hinweis verwenden, um redaktionelle Änderungen an dem Text eines Steuer Elements zu bestätigen.
-   Alle Text Bereichs Objekte, die von der [**ITextRangeProvider:: Compare**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compare)-, [**compareEndPoints**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compareendpoints)-und der [**muveendpointbyrange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyrange) -Methode verwendet werden, müssen Peers derselben **Text** Steuerelement-Muster Implementierung sein.
-   Obwohl es nicht erforderlich ist, kann der von der [**ITextRangeProvider:: compareEndPoints**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compareendpoints) -Methode abgerufene *pRetVal* -Wert den Abstand zwischen den beiden Endpunkten in Zeichen ([**TextUnit- \_ Zeichen**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)) angeben. Allerdings sollten Client Anwendungen nicht von der Genauigkeit von *pRetVal* abhängen, die über den positiven oder negativen Wert hinausgeht.
-   Die [**ITextRangeProvider:: expandesenclosingunit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit)-, [**Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move)-und [**MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit) -Methoden erfordern eine sorgfältige Überlegung der angegebenen Text Einheit. Weitere Informationen finden Sie unter Bearbeiten einer TextRange nach Text Einheit.
-   Informationen zu den Implementierungs Anforderungen im Zusammenhang mit den Methoden [**ITextRangeProvider:: SELECT**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select), [**AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection)und [**RemoveFromSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-removefromselection) finden Sie unter Auswählen von Text in einem Textbereich.
-   Die [**ITextRangeProvider:: FindText**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findtext) -und [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) -Methoden suchen vorwärts oder rückwärts nach einer einzelnen übereinstimmenden Text Zeichenfolge oder einem Text Attribut. Sie sollten **null** zurückgeben, wenn keine Entsprechung gefunden wird.
-   Die [**ITextRangeProvider:: GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) -Methode muss die Adresse zurückgeben, die von der [**uiagetreservedmixedattributevalue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue) -oder der [**uiagetreservednotsupportedvalue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservednotsupportedvalue) -Funktion abgerufen wird, wenn das zugehörige Attribut im Bereich variiert, oder wenn das Attribut nicht vom Text Steuerelement unterstützt wird. Mit der **TextRange** -Steuerelement Muster Spezifikation können keine neuen Text Attribut Bezeichner hinzugefügt werden, oder es kann nicht geändert werden, wie die vorhandenen Attribute definiert werden.
-   Wenn möglich sollte die [**ITextRangeProvider:: getboundingrechgles**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getboundingrectangles) -Methode ein Array zurückgeben, das ein umschließendes Rechteck für jede vollständig oder teilweise sichtbare Textzeile in einem Textbereich enthält. Wenn dies nicht möglich ist, kann der Anbieter ein Array zurückgeben, das die umschließenden Rechtecke nur für vollständig sichtbare Zeilen enthält. Dies schränkt jedoch die Fähigkeit einer Client Anwendung ein, die Darstellung des Texts auf dem Bildschirm genau zu beschreiben.
-   Die [**ITextRangeProvider:: GetChildren**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getchildren) -Methode sollte alle untergeordneten Elemente zurückgeben, die in einen Textbereich eingebettet sind, aber es müssen keine untergeordneten Elemente der untergeordneten Elemente zurückgegeben werden. Wenn ein Textbereich z. b. eine Tabelle mit einer Reihe von untergeordneten Zellen enthält, kann die **GetChildren** -Methode nur das Table-Element und nicht die Cell-Elemente zurückgeben. Aus Leistungs-oder Architektur Gründen ist es möglich, dass ein Anbieter nicht alle eingebetteten Objekte verfügbar macht, die in einem Dokument in der Automatisierungs Struktur gehostet werden. In diesem Fall sollte der Anbieter mindestens die Enumeration von untergeordneten Objekten über die **GetChildren** -Methode unterstützen und als Option das [VirtualizedItem](uiauto-implementingvirtualizeditem.md) -Steuerelement Muster für die Unterstützung der Unterstützung der Unterstützung von unterstützen.
-   Die [**ITextRangeProvider:: GetEnclosingElement**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getenclosingelement) -Methode gibt in der Regel den Text Anbieter zurück, der den Textbereich bereitstellt. Wenn der Text Anbieter jedoch untergeordnete Objekte wie z. b. Tabellen oder Hyperlinks unterstützt, kann das einschließende Element ein Nachfolger des Text Anbieters sein. Das Element, das von **GetEnclosingElement** zurückgegeben wird, sollte das Element sein, das dem angegebenen Textbereich am nächsten ist. Wenn sich der Textbereich z. b. in einer Zelle einer Tabelle befindet, sollte **GetEnclosingElement** die enthaltende Zelle anstelle des TABLE-Elements zurückgeben.
-   Die [**ITextRangeProvider:: gettext**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-gettext) -Methode sollte den nur-Text im Bereich zurückgeben. Weitere Informationen finden Sie unter beschaffen von Text aus einem Textbereich.
-   Durch Aufrufen von [**ITextRangeProvider:: ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-scrollintoview) sollte der Text im Viewport des Text Steuer Elements gemäß dem Parameter *aligntotop* ausgerichtet werden. Obwohl es keine Voraussetzung für die horizontale Ausrichtung gibt, sollte der Textbereich sowohl horizontal als auch vertikal sichtbar sein. Bei der Auswertung des *aligntotop* -Parameters muss ein Anbieter die Ausrichtung des Text-Steuer Elements und die Fluss Richtung des Texts berücksichtigen. Wenn beispielsweise " *aligndetop* " für ein vertikal orientiertes Text Steuerelement mit Text, der von rechts nach links verläuft, den Wert " **true** " hat, sollte der Anbieter den Textbereich an der rechten Seite des Viewports ausrichten.
-   Beim Durchlaufen eines Dokuments durch [**TextUnit- \_ Zeile**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit), wenn der Textbereich in eine eingebettete Tabelle wechselt, sollte jede Textzeile in einer Zelle als Linie behandelt werden.

## <a name="required-members-for-itextprovider"></a>Erforderliche Member für **ITextProvider**

Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) -Schnittstelle erforderlich.



| Erforderliche Member                                                                                        | Memberart | Hinweise |
|---------------------------------------------------------------------------------------------------------|-------------|-------|
| [**DocumentRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_documentrange)                                             | Eigenschaft    | Keine  |
| [**SupportedTextSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_supportedtextselection)                           | Eigenschaft    | Keine  |
| [**GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection)                                               | Methode      | Keine  |
| [**GetVisibleRanges**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getvisibleranges)                                       | Methode      | Keine  |
| [**RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild)                                           | Methode      | Keine  |
| [**RangeFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint)                                           | Methode      | Keine  |
| [**UIA \_ \_ -Text textchangedebug**](uiauto-event-ids.md)                   | Ereignis       | Keine  |
| [**UIA \_ \_ -Text textselectionchangedebug**](uiauto-event-ids.md) | Ereignis       | Keine  |



 

Die folgenden zusätzlichen Eigenschaften und Methoden sind für die Implementierung der [**ITextProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2) -Schnittstelle erforderlich.



| Erforderliche Member                                                         | Memberart | Hinweise |
|--------------------------------------------------------------------------|-------------|-------|
| [**Getcaretrange**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextprovider2-getcaretrange)         | Methode      | Keine  |
| [**Rangef-Notation**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider2-rangefromannotation) | Methode      | Keine  |



 

## <a name="required-members-for-itextrangeprovider"></a>Erforderliche Member für **ITextRangeProvider**

Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) -Schnittstelle erforderlich.



| Erforderliche Member                                                                 | Memberart | Hinweise |
|----------------------------------------------------------------------------------|-------------|-------|
| [**Addzu Selection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection)               | Methode      | Keine  |
| [**Klon**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-clone)                                 | Methode      | Keine  |
| [**Vergleich**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compare)                             | Methode      | Keine  |
| [**CompareEndPoints**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compareendpoints)           | Methode      | Keine  |
| [**ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) | Methode      | Keine  |
| [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute)                 | Methode      | Keine  |
| [**FindText**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findtext)                           | Methode      | Keine  |
| [**GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue)         | Methode      | Keine  |
| [**Getboundingrechgles**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getboundingrectangles) | Methode      | Keine  |
| [**GetChildren**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getchildren)                     | Methode      | Keine  |
| [**GetEnclosingElement**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getenclosingelement)     | Methode      | Keine  |
| [**GetText**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-gettext)                             | Methode      | Keine  |
| [**Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move)                                   | Methode      | Keine  |
| [**"Muveendpointbyunit"**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit)       | Methode      | Keine  |
| [**"Muveendpointbyrange"**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyrange)     | Methode      | Keine  |
| [**Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select)                               | Methode      | Keine  |
| [**ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-scrollintoview)               | Methode      | Keine  |



 

Die folgenden zusätzlichen Eigenschaften und Methoden sind für die Implementierung der [**ITextRangeProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider2) -Schnittstelle erforderlich.



| Erforderliche Member                                                      | Memberart | Hinweise                                      |
|-----------------------------------------------------------------------|-------------|--------------------------------------------|
| [**ShowContextMenu**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider2-showcontextmenu) | Methode      | Weitere Informationen finden Sie im Abschnitt "Implementieren von ShowContextMenu" |



 

Dem **TextRange** -Steuerelement Muster sind keine Ereignisse zugeordnet.

## <a name="supporting-text-ranges"></a>Unterstützende Text Bereiche

In diesem Abschnitt wird beschrieben, wie ein Anbieter verschiedene Methoden der [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) -und [**ITextRangeProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider2) -Schnittstellen implementieren muss, um das **TextRange** -Steuerelement Muster zu unterstützen.

### <a name="manipulating-a-text-range-by-text-unit"></a>Bearbeiten eines Text Bereichs nach Text Einheit

Die [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) -Schnittstelle stellt verschiedene Methoden zum Bearbeiten und Navigieren von Textbereichen in einem textbasierten Steuerelement bereit. Die Methoden [**ITextRangeProvider:: Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move), [**MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit)und [**expanddeenclosingunit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) verschieben einen Textbereich oder einen seiner Endpunkte mit der angegebenen Text Einheit, z. b. Zeichen, Wort, Absatz usw. Weitere Informationen finden Sie unter [Benutzeroberflächen Automatisierung-Text Einheiten](/windows/desktop/WinAuto/uiauto-uiautomationtextunits).

Trotz des Namens erweitert die [**ITextRangeProvider:: expandesenclosingunit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) -Methode nicht notwendigerweise einen Textbereich. Stattdessen wird ein Textbereich durch Verschieben der Endpunkte "normalisiert", sodass der Bereich die angegebene Text Einheit umfasst. Der Bereich wird erweitert, wenn er kleiner als die angegebene Einheit ist, oder verkürzt, wenn er länger als die angegebene Einheit ist. Es ist wichtig, dass die **expanddeerclosingunit** -Methode Textbereiche immer konsistent normalisiert. Andernfalls sind andere Aspekte der Text Bereichs Bearbeitung durch eine Text Einheit unvorhersagbar. Das folgende Diagramm zeigt, wie **expandumenclosingunit** einen Textbereich normalisiert, indem die Endpunkte des Bereichs verschoben werden.

![Diagramm, das Text Bereichs-Endpunkt Positionen vor und nach einem aufzurufenden ExpandToEnclosingUnit-Befehl anzeigt](images/expandtoenclosingunit.jpg)

Wenn der Textbereich am Anfang einer Text Einheit beginnt und am Anfang von oder vor der nächsten Textzeile endet, wird der endendpunkt an die nächste Text Einheiten Grenze verschoben (siehe 1 und 2 im vorherigen Diagramm).

Wenn der Textbereich am Anfang einer Text Einheit beginnt und bei oder nach der nächsten Einheiten Grenze endet, wird der endendpunkt beibehalten oder nach dem Start Endpunkt zurück zur nächsten Einheiten Grenze verschoben (siehe 3 und 4 in der vorherigen Abbildung). Wenn zwischen den Anfangs-und endendpunkten mehr als eine Text Einheiten Grenze vorhanden ist, wird der endendpunkt nach dem Start Endpunkt rückwärts zur nächsten Einheiten Grenze verschoben, was zu einem Textbereich mit einer Länge von einer Text Einheit führt.

Wenn der Textbereich in einer Mitte der Text Einheit beginnt, wird der Start Endpunkt rückwärts zum Anfang der Text Einheit verschoben, und der endendpunkt wird nach Bedarf nach oben oder nach hinten nach dem Start Endpunkt verschoben (siehe das vorherige Diagramm 5 bis 8).

Wenn die [**ITextRangeProvider:: Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move) -Methode aufgerufen wird, normalisiert der Anbieter den Textbereich um die angegebene Text Einheit und verwendet dabei dieselbe normalisierungs Logik wie die [**expanddeenclosingunit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) -Methode. Anschließend verschiebt der Anbieter den Bereich um die angegebene Anzahl von Text Einheiten rückwärts oder vorwärts. Wenn Sie den Bereich verschieben, sollte der Anbieter die Grenzen von eingebetteten Objekten im Text ignorieren. (Die Einheiten Grenze selbst kann jedoch durch das vorhanden sein eines eingebetteten Objekts beeinträchtigt werden.) Im folgenden Diagramm wird veranschaulicht, wie die **Move** -Methode einen Textbereich, Unit by Unit, über eingebettete Objekte und Text Einheiten Grenzen hinweg verschiebt.

![Diagramm, das zeigt, wie die Move-Methode Bereichs Endpunkte über Objekt-und Text Einheiten Grenzen hinweg verschiebt](images/move.jpg)

Die [**ITextRangeProvider:: roveendpointbyunit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit) -Methode verschiebt einen der Endpunkte um die angegebene Text Einheit vorwärts oder rückwärts, wie in der folgenden Abbildung dargestellt.

![Diagramm, das zeigt, wie "muveendpointbyunit" den Endpunkt eines Bereichs verschiebt](images/moveendpointbyunit.gif)

Mit der [**ITextRangeProvider:: wveendpointbyrange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyrange) -Methode kann eine Client Anwendung einen Endpunkt eines Text Bereichs auf denselben Speicherort wie den angegebenen Endpunkt eines zweiten Text Bereichs festlegen.

### <a name="selecting-text-in-a-text-range"></a>Auswählen von Text in einem Textbereich

Die [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) -Schnittstelle enthält mehrere Methoden zum Steuern der Auswahl von Text in einem textbasierten Steuerelement.

Die [**ITextRangeProvider:: SELECT**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select) -Methode sollte den Text auswählen, der einem Textbereich entspricht, und die vorherige Auswahl, sofern vorhanden, aus dem Text Steuerelement entfernen. Wenn **Select** für einen degenerierten Textbereich aufgerufen wird, sollte der Anbieter die Einfügemarke an die Position des Text Bereichs verschieben, ohne Text auszuwählen.

Wenn ein Steuerelement die Auswahl mehrerer, nicht zusammenhängender Textabschnitte unterstützt, fügen die [**ITextRangeProvider:: adddeselection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection) -Methode und die [**RemoveFromSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-removefromselection) -Methode Textbereiche zu hinzu, und entfernen Sie Sie aus der Auflistung ausgewählter Textbereiche. Wenn das Steuerelement nur einen ausgewählten Textbereich gleichzeitig unterstützt, der Auswahl Vorgang jedoch zur Auswahl mehrerer nicht zusammenhängender Textbereiche führt, sollte der Anbieter entweder einen **E \_ InvalidOperation** -Fehler zurückgeben oder die aktuelle Auswahl erweitern oder abschneiden. Die [**ITextProvider:: SupportedTextSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_supportedtextselection) -Eigenschaft sollte angeben, ob ein Steuerelement die Auswahl von einzelnen oder mehreren Text Spannen oder überhaupt keine unterstützt.

Wenn ein textbasiertes Steuerelement Text Einfügungen unterstützt, sollte das Aufrufen von [**ITextRangeProvider:: AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection) oder [**RemoveFromSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-removefromselection) für einen degenerierten Textbereich im Steuerelement die Einfügemarke verschieben, aber keinen Text auswählen.

### <a name="acquiring-text-from-a-text-range"></a>Abrufen von Text aus einem Textbereich

Die [**ITextRangeProvider:: gettext**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-gettext) -Methode sollte den nur-Text eines Text Bereichs zurückgeben. Der nur-Text muss alle Steuerzeichen enthalten, die im Quelltext gefunden werden, z. b. Wagen Rückläufe und Unicode-Zeichen von links nach rechts (LRM). Der nur-Text sollte keine Markup Tags enthalten, wie z. b. html, die möglicherweise im Quelltext vorhanden sind. Außerdem sollten alle Escapecodes im Quelltext in die nur-Text-Entsprechungen konvertiert werden. Beispielsweise sollte " &nbsp; " in ein einfaches Leerzeichen konvertiert werden.

Wenn ein eingebettetes Objekt einen Textbereich umfasst, sollte der Klartext den inneren Text des Objekts enthalten, aber nicht den alternativen Text (die Name-Eigenschaft des eingebetteten Objekts), da er möglicherweise inkonsistent mit dem beschreibenden inneren Text ist. Weitere Informationen finden Sie unter [How UI Automation macht Embedded Objects](uiauto-textpattern-and-embedded-objects-overview.md)verfügbar.

### <a name="implementing-showcontextmenu"></a>Implementieren von ShowContextMenu

[**ITextRangeProvider2:: ShowContextMenu**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider2-showcontextmenu) sollte immer das Kontextmenü am Anfangs Endpunkt des Bereichs anzeigen. Dies sollte gleichwertig sein, was geschieht, wenn der Benutzer die Kontextmenü Taste gedrückt hat oder UMSCHALT + F10 mit der Einfügemarke am Anfang des Bereichs.

Wenn die Anzeige des Kontextmenüs in der Regel dazu führt, dass die Einfügemarke an eine angegebene Position verschoben wird, sollte dies auch für das programmgesteuerte Aufrufen von [**ShowContextMenu**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider2-showcontextmenu) für die Benutzeroberflächenautomatisierungs-Unterstützung erfolgen.

## <a name="interoperability-with-the-system-caret"></a>Interoperabilität mit der System Einfügemarke

Die korrekte Unterstützung der Einfügemarke ist für viele Client Anwendungen wichtig, einschließlich derjenigen, die nicht auf der Benutzeroberflächen Automatisierung basieren. Im **Text** -Steuerelement Muster wird die Einfügemarke durch einen degenerierten (leeren) Text Bereich an der Position der System Einfügemarke dargestellt. Wenn die Einfügemarke verschoben wird, sollte ein Steuerelement das **textselectionchanged** -Ereignis ([**UIA \_ Text \_ textselectionchangeabventid**](uiauto-event-ids.md)) auswerfen. Einige Client Anwendungen sind von diesem Ereignis abhängig, um den Speicherort der Einfügemarke zu überwachen und die Textauswahl nachzuverfolgen.

Wenn ein Steuerelement markierten Text enthält, bietet das aktuelle Design des **Text** -Steuerelement Musters keine Möglichkeit, den Speicherort der Einfügemarke direkt einem bestimmten Textbereich zuzuordnen. Der Anbieter muss die Textauswahl nachverfolgen und den Speicherort der Einfügemarke entsprechend festlegen. Da die Auswahl von Text in der Regel durch Verschieben der Einfügemarke bei gedrückter Umschalt-oder STRG-Taste oder beides erreicht wird, kann ein Anbieter die Textauswahl nachverfolgen, indem er den Zustand dieser Tasten überprüft, wenn sich die Auswahl ändert.

Da das Barrierefreiheits Framework integrierte Unterstützung für die System Einfügemarke, aber nicht für eine benutzerdefinierte Einfügemarke bereitstellt, sollten textbasierte Steuerelemente nach Möglichkeit die System Einfügemarke verwenden. Steuerelemente, die eine benutzerdefinierte Einfügemarke verwenden, stellen sicher, dass auf die Einfügemarke zugegriffen werden kann, indem eine System Einfügemarke erstellt wird, die die gleichen Dimensionen wie die benutzerdefinierte Einfügemarke hat, und die System Einfügemarke an derselben Position in der Benutzeroberfläche des Steuer Elements wie die benutzerdefinierte Einfügemarke positioniert Als Alternative kann ein Steuerelement, das eine benutzerdefinierte Einfügemarke verwendet, einen Microsoft Active Accessibility-Anbieter für die [**objID \_**](object-identifiers.md) -Einfügemarke implementieren, um Barrierefreiheits Informationen direkt für Ihre benutzerdefinierte Einfüge

Weitere Informationen zur System Einfügemarke finden Sie unter [Caretzeichen](/windows/desktop/menurc/carets).

Um zu testen, ob Ihr Steuerelement den Speicherort der System Einfügemarke ordnungsgemäß verfügbar macht, verwenden Sie die Tools zum über [prüfen](inspect-objects.md) und [barrierefreie Ereignis](accessible-event-watcher.md) Überwachung.

Die Bildschirm Koordinaten der Mitte der systemcaretzeichen müssen immer mit der Position der Einfügemarke identisch sein. Auf diese Weise kann ein Client die Bildschirm Koordinaten des Caretzeichen in einem Aufrufen von [**ITextProvider:: RangeFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint) verwenden, um einen Textbereich abzurufen, der die Position der Einfügemarke exakt darstellt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Text Steuerelement-Typ](uiauto-supporttextcontroltype.md)
</dt> <dt>

[TextEdit-Steuerelement Muster](textedit-control-pattern.md)
</dt> <dt>

[Textchild-Steuerelement Muster](textchild-control-pattern.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Benutzeroberflächenautomatisierungs-Unterstützung für Textinhalte](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 