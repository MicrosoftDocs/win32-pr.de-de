---
title: Text- und TextRange-Steuerelementmuster
description: Beschreibt Richtlinien und Konventionen für die Implementierung von ITextProvider, ITextProvider2 und ITextRangeProvider, einschließlich Informationen zu Eigenschaften und Methoden.
ms.assetid: 4d541c31-11f7-4d7e-a0e0-9ed1da873d07
keywords:
- Benutzeroberflächenautomatisierung,Implementieren des Textsteuerelementmusters
- Benutzeroberflächenautomatisierung,Implementieren des TextRange-Steuerelementmusters
- Benutzeroberflächenautomatisierung,Text-Steuerelementmuster
- Benutzeroberflächenautomatisierung,TextRange-Steuerelementmuster
- Benutzeroberflächenautomatisierung,ITextProvider
- Benutzeroberflächenautomatisierung,ITextRangeProvider
- ITextProvider
- ITextRangeProvider
- Implementieren Benutzeroberflächenautomatisierung Text-Steuerelementmusters
- Implementieren Benutzeroberflächenautomatisierung TextRange-Steuerelementmusters
- Textsteuerelementmuster
- TextRange-Steuerelementmuster
- Steuerelementmuster,ITextProvider
- Steuerelementmuster,ITextRangeProvider
- Steuerelementmuster,Implementieren von Benutzeroberflächenautomatisierung Text
- Steuerelementmuster,Implementieren Benutzeroberflächenautomatisierung TextRange
- Steuerelementmuster,Text
- Steuerelementmuster,TextRange
- interfaces,ITextProvider
- interfaces,ITextRangeProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99baf1af267e67ffe3f75a83fb970c991e9ebe5674497db2a2edad8d9cc328b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118826981"
---
# <a name="text-and-textrange-control-patterns"></a>Text- und TextRange-Steuerelementmuster

Beschreibt Richtlinien und Konventionen für die Implementierung von [**ITextProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) [**ITextProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2)und [**ITextRangeProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider)einschließlich Informationen zu Eigenschaften und Methoden. Mit  dem Text-Steuerelementmuster können Anwendungen und Steuerelemente ein einfaches Textobjektmodell verfügbar machen, sodass Clients Textinhalte, Textattribute und eingebettete Objekte aus textbasierten Steuerelementen abrufen können.

Um das  Text-Steuerelementmuster zu unterstützen, implementieren Steuerelemente die Schnittstellen [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) und [**ITextProvider2.**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2) Steuerelementtypen, die das **Text-Steuerelementmuster** unterstützen sollen, umfassen die Steuerelementtypen [Bearbeiten](uiauto-supporteditcontroltype.md) und [Dokument](uiauto-supportdocumentcontroltype.md) sowie alle anderen Steuerelementtypen, mit denen der Benutzer Text eingeben oder schreibgeschützten Text auswählen kann.

Das  Text-Steuerelementmuster kann mit anderen Microsoft Benutzeroberflächenautomatisierung-Steuerelementmustern verwendet werden, um verschiedene Typen eingebetteter Objekte im Text zu unterstützen, einschließlich Tabellen, Links und Befehlsschaltflächen.

Die Schnittstellen [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) und [**ITextProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2) enthalten eine Reihe von Methoden zum Abrufen von Textbereichen. Ein *Textbereich* ist ein Objekt, das eine zusammenhängende Textspanne (oder mehrere, unzusammenhängende Textbereiche) in einem Textcontainer darstellt. Eine **ITextProvider-Methode** erhält einen Textbereich, der das gesamte Dokument darstellt, während andere Textbereiche abrufen, die einen Teil des Dokuments darstellen, z. B. den ausgewählten Text, den sichtbaren Text oder ein in den Text eingebettetes Objekt.

Ein Textbereichsobjekt wird durch das **TextRange-Steuerelementmuster** dargestellt, das über die [**ITextRangeProvider-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) implementiert wird. Das **TextRange-Steuerelementmuster** stellt Methoden und Eigenschaften bereit, die verwendet werden, um Informationen zum Text im Bereich verfügbar zu machen, die Endpunkte des Bereichs zu verschieben, Text auszuwählen oder die Auswahl aufzuheben, den Bereich in die Ansicht zu scrollen usw.

Weitere Informationen zu den **Text-** und **TextRange-Steuerelementmustern** finden Sie unter [Benutzeroberflächenautomatisierung-Unterstützung für Textinhalt.](uiauto-ui-automation-textpattern-overview.md)

Ab Windows 8.1 Anbieter die [**ITextRangeProvider2-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider2) implementieren können. Dies ermöglicht das Aufrufen von Kontextmenüs, die einem Textbereich zugeordnet sind. Dies unterstützt Szenarien wie die automatische Textkorrektur oder die Ime-Kandidatenauswahl (Input Method Editor).

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **ITextProvider**](#required-members-for-itextprovider)
-   [Erforderliche Member für **ITextRangeProvider**](#required-members-for-itextrangeprovider)
-   [Unterstützen von Textbereichen](#supporting-text-ranges)
    -   [Bearbeiten eines Textbereichs nach Texteinheit](#manipulating-a-text-range-by-text-unit)
    -   [Auswählen von Text in einem Textbereich](#selecting-text-in-a-text-range)
    -   [Abrufen von Text aus einem Textbereich](#acquiring-text-from-a-text-range)
    -   [Implementieren von ShowContextMenu](#implementing-showcontextmenu)
-   [Interoperabilität mit dem System caret](#interoperability-with-the-system-caret)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie  beim Implementieren des Textsteuerelementmusters die folgenden Richtlinien und Konventionen:

-   Jedes Steuerelement, das den Zugriff auf Text ermöglicht (z. B.  das Eingeben von Text oder das Auswählen von schreibgeschütztem Text), sollte das Text-Steuerelementmuster unterstützen.
-   Das  Text-Steuerelementmuster kann mit jedem Benutzeroberflächenelement verwendet werden, das Text darstellt, sogar mit einer statischen Bezeichnung auf einem Standardschaltflächensteuerelement. Für statische Textsteuerelemente, die nicht ausgewählt werden können oder über keine Einfügemarke verfügen, ist dies jedoch nicht erforderlich.
-   Um sicherzustellen, dass der Text vollständig zugänglich ist, sollten Steuerelemente, die [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) implementieren, auch die [**IValueProvider-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) unterstützen. **IValueProvider** ergänzt **ITextProvider** durch eine programmgesteuerte Möglichkeit, den Text zu ändern. Darüber hinaus bietet es eine höhere Kompatibilität mit Clientanwendungen für Hilfstechnologien, einschließlich anwendungen, die auf älteren Technologien wie Microsoft Active Accessibility basieren. Wenn beide Steuerelementmuster implementiert werden, entsprechen das **TextChanged-Ereignis** ([**UIA \_ \_ TextChangedEventId**](uiauto-event-ids.md)) und das **AutomationPropertyChanged-Ereignis** ([**UIA \_ AutomationPropertyChangedEventId**](uiauto-event-ids.md)) der **Value-Eigenschaft** ([**UIA \_ ValueValuePropertyId**](uiauto-control-pattern-propids.md)). Beide Ereignisse müssen unterstützt werden.
-   Das  Text-Steuerelementmuster unterstützt nur einen Textstream und einen Viewport pro Steuerelement. Wenn die Anwendung mehrere Ansichten des Dokuments in Bereichen anbietet, sollte jede Ansicht (Steuerelement) [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) unabhängig unterstützen.
-   Die [**ITextProvider::GetSelection-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection) gibt möglicherweise einen einzelnen Textbereich zurück, der den aktuell ausgewählten Text darstellt. Wenn ein Steuerelement die Auswahl mehrerer, nicht zusammenhängender Textbereiche unterstützt, sollte die **GetSelection-Methode** ein Array zurückgeben, das eine [**ITextRangeProvider-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) für jede ausgewählte Textspanne enthält.
-   Das  Text-Steuerelementmuster stellt die Einfügemarke als degenerieren (leeren) Textbereich dar. Die [**ITextProvider::GetSelection-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection) sollte einen degenerieren Textbereich zurückgeben, wenn die Einfügemarke vorhanden ist und kein Text ausgewählt ist. Weitere Informationen finden Sie unter [Interoperabilität mit dem System caret](#interoperability-with-the-system-caret).
-   Die [**ITextProvider::GetVisibleRanges-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getvisibleranges) gibt möglicherweise einen einzelnen Textbereich zurück, wenn ein zusammenhängender Textbereich im Viewport sichtbar ist, oder sie gibt ein Array von nicht zusammenhängenden Textbereichen zurück, die mehrere teilweise sichtbare Textzeilen darstellen.
-   Die [**ITextProvider::RangeFromChild-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) sollte einen degenerieren Bereich zurückgeben, wenn das untergeordnete Element keinen Text enthält. Da ein eingebettetes Objekt Text enthalten kann, gibt die **RangeFromChild-Methode** möglicherweise nicht immer einen degenerieren Textbereich zurück. Weitere Informationen finden Sie unter [How Benutzeroberflächenautomatisierung Exposes Embedded Objects](uiauto-textpattern-and-embedded-objects-overview.md).
-   Die [**ITextProvider::RangeFromPoint-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint) führt Treffertests im Dokumentbereich mit den angegebenen Bildschirmkoordinaten durch. Der resultierende Textbereich sollte mit der Einfügemarke oder Auswahl konsistent sein, die sich aus dem Klicken auf die Position an den angegebenen Bildschirmkoordinaten ergeben würde. Wenn sich beispielsweise ein Bild an den angegebenen Bildschirmkoordinaten befindet, sollte der resultierende Textbereich mit dem Textbereich identisch sein, den die [**ITextProvider::RangeFromChild-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) für das Bild abrufen würde. Wenn eine Clientanwendung einen Textbereich für die Position in der Mitte des Systemeinfügezeichens (die Einfügemarke) anfordert, sollte der resultierende Textbereich mit dem Textbereich des Systems identisch sein.
-   Die [**ITextProvider::D ocumentRange-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_documentrange) sollte immer einen Textbereich bereitstellen, der den gesamten Text enthält, der von der entsprechenden [**ITextProvider-Implementierung**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) unterstützt wird.
-   Das [**UIA \_ \_ TextChangedEventId-Ereignis**](uiauto-event-ids.md) muss nach einer Textänderung ausgelöst werden, auch wenn die Änderung im Viewport nicht sichtbar ist. Beispielsweise sollte der Anbieter das -Ereignis auslösen, auch wenn der Benutzer genau den gleichen Text über den ausgewählten Text eingibt.
-   Die [**UIA \_ \_ TextSelectionChangedEventId**](uiauto-event-ids.md) muss immer dann ausgelöst werden, wenn sich die Textauswahl ändert oder die Einfügemarke (Caretzeichen) zwischen dem Text verschoben wird.

Beachten Sie  beim Implementieren des TextRange-Steuerelementmusters die folgenden Richtlinien und Konventionen:

-   Alle Methoden  des TextRange-Steuerelementmusters sollten Textvorgänge unabhängig vom Sichtbarkeitszustand des Texts ausführen. Die Sichtbarkeit eines Textbereichs kann immer durch Abfragen des **IsHidden-Textattributs** [**(UIA \_ IsHiddenAttributeId)**](uiauto-textattribute-ids.md)bestimmt werden.
-   Wenn möglich, sollte ein Anbieter sicherstellen, dass alle Textänderungen, z. B. Löschungen, Einfügungen und Verschiebungen, in den zugeordneten Textbereichsobjekten (Instanzen der [**ITextRangeProvider-Schnittstelle)**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) wiedergegeben werden, und ein [**UIA \_ \_ TextChangedEventId-Ereignis**](uiauto-event-ids.md) auslösen. Clients können das -Ereignis als Hinweis verwenden, um änderungen zu bestätigen, die an dem Text eines Steuerelements vorgenommen wurden.
-   Alle Textbereichsobjekte, die von den Methoden [**ITextRangeProvider::Compare,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compare) [**CompareEndpoints**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compareendpoints)und [**MoveEndpointByRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyrange) verwendet werden, müssen Peers der gleichen Text-Steuerelementmusterimplementierungen sein. 
-   Obwohl dies nicht erforderlich ist, kann der von der [**ITextRangeProvider::CompareEndpoints-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compareendpoints) abgerufene *pRetVal-Wert* den Abstand zwischen den beiden Endpunkten in Zeichen [**(TextUnit-Zeichen) \_**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)angeben. Clientanwendungen sollten jedoch nicht von der Genauigkeit von *pRetVal* abhängig sein, die über den positiven oder negativen Wert hinausgeht.
-   Die Methoden [**ITextRangeProvider::ExpandToEnclosingUnit,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) [**Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move)und [**MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit) erfordern eine sorgfältige Berücksichtigung der angegebenen Texteinheit. Weitere Informationen finden Sie unter Bearbeiten eines Textranges nach Texteinheit.
-   Implementierungsanforderungen im Zusammenhang mit den Methoden [**ITextRangeProvider::Select,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select) [**AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection)und [**RemoveFromSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-removefromselection) finden Sie unter Auswählen von Text in einem Textbereich.
-   Die [**Methoden ITextRangeProvider::FindText**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findtext) und [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) suchen vorwärts oder rückwärts nach einer einzelnen übereinstimmenden Textzeichenfolge oder einem Textattribut. Sie sollten **NULL** zurückgeben, wenn keine Übereinstimmung gefunden wird.
-   Die [**ITextRangeProvider::GetAttributeValue-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) muss die von der [**Funktion UiaGetReservedMixedAttributeValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue) oder [**UiaGetReservedNotSupportedValue erhaltene**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservednotsupportedvalue) Adresse zurückgeben, wenn das zugeordnete Attribut im Bereich variiert oder das Attribut vom Textsteuerelement nicht unterstützt wird. Die  TextRange-Steuerelementmusterspezifikation lässt weder das Hinzufügen neuer Textattributbezeichner noch das Ändern der Definition der vorhandenen Attribute zu.
-   Nach Möglichkeit sollte die [**ITextRangeProvider::GetBoundingRectangles-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getboundingrectangles) ein Array zurückgeben, das ein umschließendes Rechteck für jede vollständig oder teilweise sichtbare Textzeile in einem Textbereich enthält. Wenn dies nicht möglich ist, kann der Anbieter ein Array zurückgeben, das die umgrenzten Rechtecke nur vollständig sichtbarer Linien enthält. Dies schränkt jedoch die Fähigkeit einer Clientanwendung ein, genau zu beschreiben, wie der Text auf dem Bildschirm dargestellt wird.
-   Die [**ITextRangeProvider::GetChildren-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getchildren) sollte alle untergeordneten Elemente zurückgeben, die in einen Textbereich eingebettet sind. Sie muss jedoch keine untergeordneten Elemente der untergeordneten Elemente zurückgeben. Wenn ein Textbereich z. B. eine Tabelle mit einer Reihe von untergeordneten Zellen enthält, gibt die **GetChildren-Methode** möglicherweise nur das Tabellenelement und nicht die Zellenelemente zurück. Aus Leistungs- oder Architekturgründen kann ein Anbieter möglicherweise nicht alle eingebetteten Objekte verfügbar machen, die in einem Dokument in der Automatisierungsstruktur gehostet werden. In diesem Fall sollte der Anbieter zumindest die Aufzählung von untergeordneten Objekten über die **GetChildren-Methode** unterstützen und als Option das [VirtualizedItem-Steuerelementmuster](uiauto-implementingvirtualizeditem.md) für die Unterstützung der Devirtualisierung unterstützen.
-   Die [**ITextRangeProvider::GetEnclosingElement-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getenclosingelement) gibt in der Regel den Textanbieter zurück, der den Textbereich angibt. Wenn der Textanbieter jedoch untergeordnete Objekte wie Tabellen oder Links unterstützt, kann das einschließende Element ein Nachfolger des Textanbieters sein. Das von **GetEnclosingElement** zurückgegebene Element sollte das Element sein, das dem angegebenen Textbereich am nächsten liegt. Wenn sich der Textbereich beispielsweise in einer Zelle einer Tabelle befindet, sollte **GetEnclosingElement** die enthaltende Zelle anstelle des Tabellenelements zurückgeben.
-   Die [**ITextRangeProvider::GetText-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-gettext) sollte den Nur-Text im Bereich zurückgeben. Weitere Informationen finden Sie unter Abrufen von Text aus einem Textbereich.
-   Beim [**Aufrufen von ITextRangeProvider::ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-scrollintoview) sollte der Text im Viewport des Textsteuerfelds ausgerichtet werden, wie durch den *alignToTop-Parameter* angegeben. Obwohl es in Bezug auf die horizontale Ausrichtung keine Anforderung gibt, sollte der Textbereich sowohl horizontal als auch vertikal sichtbar sein. Beim Auswerten des *alignToTop-Parameters* muss ein Anbieter die Ausrichtung des Textsteuerfelds und die Flussrichtung des Texts berücksichtigen. Wenn *alignToTop* beispielsweise **für** ein vertikal ausgerichtetes Textsteuerfeld TRUE ist, das Text enthält, der von rechts nach links fließt, sollte der Anbieter den Textbereich an der rechten Seite des Viewports ausrichten.
-   Wenn der Textbereich durch ein Dokument durch [**TextUnit \_ Line**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)in eine eingebettete Tabelle eintritt, sollte jede Textzeile in einer Zelle als Zeile behandelt werden.

## <a name="required-members-for-itextprovider"></a>Erforderliche Member für **ITextProvider**

Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**ITextProvider-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) erforderlich.



| Erforderliche Member                                                                                        | Memberart | Hinweise |
|---------------------------------------------------------------------------------------------------------|-------------|-------|
| [**DocumentRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_documentrange)                                             | Eigenschaft    | Keine  |
| [**SupportedTextSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_supportedtextselection)                           | Eigenschaft    | Keine  |
| [**GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection)                                               | Methode      | Keine  |
| [**GetVisibleRanges**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getvisibleranges)                                       | Methode      | Keine  |
| [**RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild)                                           | Methode      | Keine  |
| [**RangeFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint)                                           | Methode      | Keine  |
| [**UIA \_ Text \_ TextChangedEventId**](uiauto-event-ids.md)                   | Ereignis       | Keine  |
| [**UIA \_ Text \_ TextSelectionChangedEventId**](uiauto-event-ids.md) | Ereignis       | Keine  |



 

Die folgenden zusätzlichen Eigenschaften und Methoden sind für die Implementierung der [**ITextProvider2-Schnittstelle**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2) erforderlich.



| Erforderliche Member                                                         | Memberart | Hinweise |
|--------------------------------------------------------------------------|-------------|-------|
| [**GetCaretRange**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextprovider2-getcaretrange)         | Methode      | Keine  |
| [**RangeFromAnnotation**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider2-rangefromannotation) | Methode      | Keine  |



 

## <a name="required-members-for-itextrangeprovider"></a>Erforderliche Member für **ITextRangeProvider**

Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**ITextRangeProvider-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) erforderlich.



| Erforderliche Member                                                                 | Memberart | Hinweise |
|----------------------------------------------------------------------------------|-------------|-------|
| [**AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection)               | Methode      | Keine  |
| [**Klon**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-clone)                                 | Methode      | Keine  |
| [**Vergleich**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compare)                             | Methode      | Keine  |
| [**CompareEndpoints**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compareendpoints)           | Methode      | Keine  |
| [**ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) | Methode      | Keine  |
| [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute)                 | Methode      | Keine  |
| [**Findtext**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findtext)                           | Methode      | Keine  |
| [**GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue)         | Methode      | Keine  |
| [**GetBoundingRectangles**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getboundingrectangles) | Methode      | Keine  |
| [**GetChildren**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getchildren)                     | Methode      | Keine  |
| [**GetEnclosingElement**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getenclosingelement)     | Methode      | Keine  |
| [**GetText**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-gettext)                             | Methode      | Keine  |
| [**Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move)                                   | Methode      | Keine  |
| [**MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit)       | Methode      | Keine  |
| [**MoveEndpointByRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyrange)     | Methode      | Keine  |
| [**Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select)                               | Methode      | Keine  |
| [**ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-scrollintoview)               | Methode      | Keine  |



 

Die folgenden zusätzlichen Eigenschaften und Methoden sind für die Implementierung der [**ITextRangeProvider2-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider2) erforderlich.



| Erforderliche Member                                                      | Memberart | Hinweise                                      |
|-----------------------------------------------------------------------|-------------|--------------------------------------------|
| [**ShowContextMenu**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider2-showcontextmenu) | Methode      | Weitere Informationen finden Sie im Abschnitt "Implementing ShowContextMenu" (Implementieren von ShowContextMenu). |



 

Dem **TextRange-Steuerelementmuster** sind keine Ereignisse zugeordnet.

## <a name="supporting-text-ranges"></a>Unterstützen von Textbereichen

In diesem Abschnitt wird beschrieben, wie ein Anbieter verschiedene Methoden der [**Schnittstellen ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) und [**ITextRangeProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider2) implementieren sollte, um das **TextRange-Steuerelementmuster** zu unterstützen.

### <a name="manipulating-a-text-range-by-text-unit"></a>Bearbeiten eines Textbereichs nach Texteinheit

Die [**ITextRangeProvider-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) stellt mehrere Methoden zum Bearbeiten und Navigieren in Textbereichen in einem textbasierten Steuerelement bereit. Die [**Methoden ITextRangeProvider::Move,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move) [**MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit)und [**ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) verschieben einen Textbereich oder einen seiner Endpunkte um die angegebene Texteinheit, z. B. Zeichen, Wort, Absatz, und so weiter. Weitere Informationen finden Sie unter [Benutzeroberflächenautomatisierung Texteinheiten](/windows/desktop/WinAuto/uiauto-uiautomationtextunits).

Trotz des Namens erweitert die [**ITextRangeProvider::ExpandToEnclosingUnit-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) nicht notwendigerweise einen Textbereich. Stattdessen wird ein Textbereich "normalisiert", indem die Endpunkte so bewegt werden, dass der Bereich die angegebene Texteinheit umfasst. Der Bereich wird erweitert, wenn er kleiner als die angegebene Einheit ist, oder verkürzt, wenn er länger als die angegebene Einheit ist. Es ist wichtig, dass die **ExpandToEnclosingUnit-Methode** Textbereiche immer konsistent normalisiert. Andernfalls sind andere Aspekte der Textbereichsbearbeitung nach Texteinheit unvorhersehbar. Das folgende Diagramm zeigt, wie **ExpandToEnclosingUnit** einen Textbereich normalisiert, indem die Endpunkte des Bereichs bewegt werden.

![Diagramm mit Textbereichs-Endpunktpositionen vor und nach einem Aufruf von expandtoenclosingunit](images/expandtoenclosingunit.jpg)

Wenn der Textbereich am Anfang einer Texteinheit beginnt und am Anfang oder vor der nächsten Texteinheitsgrenze endet, wird der Endendpunkt an die nächste Texteinheitsgrenze verschoben (siehe 1 und 2 im vorherigen Diagramm).

Wenn der Textbereich am Anfang einer Texteinheit beginnt und an oder nach der Begrenzung der nächsten Einheit endet, bleibt der Endendpunkt zurück oder wird nach dem Startendpunkt zurück zur nächsten Einheitsgrenze verschoben (siehe 3 und 4 in der vorherigen Abbildung). Wenn mehr als eine Texteinheitsgrenze zwischen dem Start- und dem Endendpunkt besteht, wird der Endendpunkt nach dem Startendpunkt zurück zur nächsten Einheitsgrenze verschoben, was zu einem Textbereich mit einer Länge von einer Texteinheit führt.

Wenn der Textbereich in der Mitte der Texteinheit beginnt, wird der Startendpunkt zurück an den Anfang der Texteinheit verschoben, und der Endpunkt wird bei Bedarf vorwärts oder rückwärts zur nächsten Einheitsgrenze nach dem Startendpunkt verschoben (siehe 5 bis 8 im vorherigen Diagramm).

Wenn die [**ITextRangeProvider::Move-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move) aufgerufen wird, normalisiert der Anbieter den Textbereich nach der angegebenen Texteinheit und verwendet dabei die gleiche Normalisierungslogik wie die [**ExpandToEnclosingUnit-Methode.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) Anschließend verschiebt der Anbieter den Bereich um die angegebene Anzahl von Texteinheiten rückwärts oder vorwärts. Beim Verschieben des Bereichs sollte der Anbieter die Grenzen eingebetteter Objekte im Text ignorieren. (Die Begrenzung der Einheit selbst kann jedoch durch das Vorhandensein eines eingebetteten Objekts beeinflusst werden.) Das folgende Diagramm zeigt, wie die **Move-Methode** einen Textbereich unitweise über eingebettete Objekte und Texteinheitsgrenzen hinweg verschiebt.

![Diagramm, das zeigt, wie die Verschiebemethode Bereichsendpunkte über Objekt- und Texteinheitsgrenzen hinweg verschiebt](images/move.jpg)

Die [**ITextRangeProvider::MoveEndpointByUnit-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit) verschiebt einen der Endpunkte um die angegebene Texteinheit vorwärts oder rückwärts, wie in der folgenden Abbildung dargestellt.

![Diagramm, das zeigt, wie moveendpointbyunit den Endpunkt eines Bereichs verschiebt](images/moveendpointbyunit.gif)

Mit [**der ITextRangeProvider::MoveEndpointByRange-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyrange) kann eine Clientanwendung einen Endpunkt eines Textbereichs auf denselben Speicherort wie den angegebenen Endpunkt eines zweiten Textbereichs festlegen.

### <a name="selecting-text-in-a-text-range"></a>Auswählen von Text in einem Textbereich

Die [**ITextRangeProvider-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) enthält mehrere Methoden zum Steuern der Textauswahl in einem textbasierten Steuerelement.

Die [**ITextRangeProvider::Select-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select) sollte den Text auswählen, der einem Textbereich entspricht, und die vorherige Auswahl (sofern enthalten) aus dem Textsteuerfeld entfernen. Wenn **Select** für einen degenerierten Textbereich aufgerufen wird, sollte der Anbieter die Einfügemarke an die Position des Textbereichs verschieben, ohne Text auszuwählen.

Wenn ein Steuerelement die Auswahl mehrerer, nicht assozlinker Textbereiche unterstützt, fügen die [**Methoden ITextRangeProvider::AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection) und [**RemoveFromSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-removefromselection) Der Auflistung der ausgewählten Textbereiche Textbereiche hinzu und entfernen sie daraus. Wenn das Steuerelement nur einen ausgewählten Textbereich gleichzeitig unterstützt, der Auswahlvorgang jedoch zur Auswahl mehrerer nicht führender Textbereiche führen würde, sollte der Anbieter entweder einen **E \_ INVALIDOPERATION-Fehler** zurückgeben oder die aktuelle Auswahl erweitern oder abschneiden. Die [**ITextProvider::SupportedTextSelection-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_supportedtextselection) sollte angeben, ob ein Steuerelement die Auswahl einzelner oder mehrerer Textspanne oder überhaupt keine unterstützt.

Wenn ein textbasiertes Steuerelement Texteinfügungen unterstützt, sollte der Aufruf von [**ITextRangeProvider::AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection) oder [**RemoveFromSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-removefromselection) für einen degenerierten Textbereich im Steuerelement die Einfügemarke verschieben, aber keinen Text auswählen.

### <a name="acquiring-text-from-a-text-range"></a>Abrufen von Text aus einem Textbereich

Die [**ITextRangeProvider::GetText-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-gettext) sollte den Nur-Text eines Textbereichs zurückgeben. Der Nur-Text sollte alle Steuerzeichen enthalten, die im Quelltext gefunden werden, z. B. Wagenrücklauf und die Unicode-Links-nach-Rechts-Markierung (LRM). Der Nur-Text sollte keine Markuptags wie HTML enthalten, die möglicherweise im Quelltext vorhanden sind. Außerdem sollten alle Escapecodes im Quelltext in die Nur-Text-Entsprechungen konvertiert werden. Beispielsweise sollte " &nbsp; " in ein einfaches Leerzeichen konvertiert werden.

Wenn ein eingebettetes Objekt einen Textbereich umfasst, sollte der Nur-Text den inneren Text des Objekts enthalten, aber nicht den alternativen Text (die Name-Eigenschaft des eingebetteten Objekts), da er möglicherweise inkonsistent mit dem beschreibenden inneren Text ist. Weitere Informationen finden Sie unter [How Benutzeroberflächenautomatisierung Exposes Embedded Objects](uiauto-textpattern-and-embedded-objects-overview.md).

### <a name="implementing-showcontextmenu"></a>Implementieren von ShowContextMenu

[**ITextRangeProvider2::ShowContextMenu**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider2-showcontextmenu) sollte immer das Kontextmenü am Anfangspunkt des Bereichs anzeigen. Dies sollte dem entsprechen, was geschieht, wenn der Benutzer die Kontextmenütaste oder UMSCHALT+F10 mit der Einfügemarke am Anfang des Bereichs gedrückt hat.

Wenn das Anzeigen des Kontextmenüs in der Regel dazu führt, dass die Einfügemarke an eine bestimmte Position bewegt wird, sollte dies für den programmgesteuerten Aufruf von [**ShowContextMenu**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider2-showcontextmenu) für die Benutzeroberflächenautomatisierung erfolgen.

## <a name="interoperability-with-the-system-caret"></a>Interoperabilität mit dem System caret

Die korrekte Unterstützung der Einfügemarke ist für viele Clientanwendungen wichtig, einschließlich anwendungen, die nicht auf Benutzeroberflächenautomatisierung. Im **Text-Steuerelementmuster** wird die Einfügemarke durch einen degenerierten (leeren) Textbereich an der Position des System caret dargestellt. Wenn sich die Einfügemarke bewegt, sollte ein Steuerelement das **TextSelectionChanged-Ereignis** [**(UIA \_ \_ TextSelectionChangedEventId) ausgelöst werden.**](uiauto-event-ids.md) Einige Clientanwendungen sind von diesem Ereignis abhängig, um die Position der Einfügemarke zu überwachen und die Textauswahl zu verfolgen.

Wenn ein Steuerelement ausgewählten Text enthält,  bietet der aktuelle Entwurf des Text-Steuerelementmusters keine Möglichkeit, die Position der Einfügemarke direkt einem bestimmten Textbereich zu zuordnen. Der Anbieter muss die Textauswahl nachverfolgen und die Position der Einfügemarke entsprechend festlegen. Da die Textauswahl in der Regel durch Bewegen der Einfügemarke erfolgt, während die UMSCHALTTASTE oder STRG-Taste gedrückt wird oder beides, kann ein Anbieter die Textauswahl nachverfolgen, indem er den Zustand dieser Tasten überprüft, wenn sich die Auswahl ändert.

Da das Barrierefreiheitsframework integrierte Unterstützung für das System caret, aber nicht für ein benutzerdefiniertes Caret-Caret-Steuerelement bietet, sollten textbasierte Steuerelemente nach Möglichkeit das System caret verwenden. Steuerelemente, die ein benutzerdefiniertes Caret-Caret-Steuerelement verwenden, können sicherstellen, dass auf das Caret-Caret-Steuerelement zugegriffen werden kann, indem ein System caret erstellt wird, das die gleichen Dimensionen wie das benutzerdefinierte Caret-Caret-Caret hat, und das System caret-Caret an der gleichen Position in der Benutzeroberfläche des Steuerelements positioniert wie das benutzerdefinierte Caret-Caret- d.&amp;160;B. an der Einfügemarke. Alternativ kann ein Steuerelement, das ein benutzerdefiniertes Caret-Zeichen verwendet, einen Microsoft Active Accessibility-Anbieter für [**OBJID \_ CARET**](object-identifiers.md) implementieren, um Barrierefreiheitsinformationen direkt für Ihr benutzerdefiniertes Caret-Caret-Steuerelement zur Verfügung zu stellen.

Weitere Informationen zum System caret finden Sie unter [Carets](/windows/desktop/menurc/carets).

Verwenden Sie die Tools [Inspect](inspect-objects.md) und [Accessible Event Watcher,](accessible-event-watcher.md) um zu testen, ob das Steuerelement den Speicherort des System caret ordnungsgemäß verfügbar macht.

Die Bildschirmkoordinaten der Mitte der Bitmap des System caret-Zeichens sollten immer mit der Position der Einfügemarke übereinstimmen. Auf diese Weise kann ein Client die Caretbildschirmkoordinaten in einem Aufruf von [**ITextProvider::RangeFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint) verwenden, um einen Textbereich abzurufen, der die Position der Einfügemarke genau darstellt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelementtypen und ihre unterstützten Steuerelementmuster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Textsteuertyp](uiauto-supporttextcontroltype.md)
</dt> <dt>

[TextEdit-Steuerelementmuster](textedit-control-pattern.md)
</dt> <dt>

[TextChild-Steuerelementmuster](textchild-control-pattern.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Benutzeroberflächenautomatisierung Unterstützung für Textinhalte](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 