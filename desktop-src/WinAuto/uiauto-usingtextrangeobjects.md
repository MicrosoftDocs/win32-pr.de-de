---
title: Verwenden von Textbereichen
description: In diesem Thema wird beschrieben, wie sie die Eigenschaften und Methoden der IUIAutomationTextRange-Schnittstelle verwenden, um auf den Textinhalt eines textbasierten Steuerelements zuzugreifen und diesen zu bearbeiten.
ms.assetid: 66BC7324-5322-4996-AF62-766936559F0E
keywords:
- Clients mithilfe von Textbereichsobjekten
- textbasierte Steuerelemente
- Clients, Textbereiche
- Clients, TextRange-Steuerelementmuster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2c409f39d437135854463e83c361a9afd22204758c360119bd0033e4fd11416
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563988"
---
# <a name="using-text-ranges"></a>Verwenden von Textbereichen

In diesem Thema wird beschrieben, wie sie die Eigenschaften und Methoden der [**IUIAutomationTextRange-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) verwenden, um auf den Textinhalt eines textbasierten Steuerelements zuzugreifen und diesen zu bearbeiten. Sie enthält die folgenden Abschnitte:

-   [Was ist ein Textbereich?](#using-text-ranges)
-   [Abrufen von Textbereichsobjekten](#acquiring-text-range-objects)
-   [Auswählen von Text in einem Textbereich](#selecting-text-in-a-text-range)
-   [Abrufen von Text aus einem Textbereich](#retrieving-text-from-a-text-range)
-   [Abrufen von Textattributen aus einem Textbereich](#retrieving-text-attributes-from-a-text-range)
-   [Abrufen eingebetteter Objekte aus einem Textbereich](#retrieving-embedded-objects-from-a-text-range)
-   [Bearbeiten eines Textbereichs](#manipulating-a-text-range)
-   [Scrollen eines Textbereichs in die Ansicht](#scrolling-a-text-range-into-view)
-   [Abrufen des einschließenden Elements eines Textbereichs](#retrieving-the-enclosing-element-of-a-text-range)
-   [Vergleichen und Klonen von Textbereichen](#comparing-and-cloning-text-ranges)
-   [Abrufen von Anmerkungen](#retrieving-annotations)
    -   [Abrufen von Anmerkungstypen aus einem Textbereich](#retrieving-annotations-types-from-a-text-range)
    -   [Abrufen aller Anmerkungen aus einem Textbereich](#retrieving-all-annotations-from-a-text-range)
    -   [Abrufen von Informationen zu einer bestimmten Anmerkung](#retrieving-information-about-a-particular-annotation)
    -   [Abrufen des Anmerkungszieltexts](#retrieving-the-annotation-target-text)
-   [Abrufen visueller Stile](#retrieving-visual-styles)
-   [Aufrufen von Kontextmenüs aus Textbereichen](#invoking-context-menus-from-text-ranges)
-   [Zugehörige Themen](#related-topics)

## <a name="what-is-a-text-range"></a>Was ist ein Textbereich?

Das Microsoft Benutzeroberflächenautomatisierung Textobjektmodell basiert auf dem Konzept des *Textbereichs*. Ein Textbereich ist ein Objekt, das die [**IUIAutomationTextRange-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) verfügbar macht und eine zusammenhängende Textspanne in einem textbasierten Steuerelement darstellt. Jeder Textbereich verfügt sowohl über einen Startendpunkt als auch über einen Endendpunkt, und der gesamte Textinhalt zwischen den beiden Endpunkten wird als Teil des Bereichs betrachtet. Ein Textbereich, dessen Startendpunkt und Endendpunkt sich an derselben Position befinden, wird als *degeneriertes* (oder leeres) Textbereich bezeichnet. Ein degenerater Textbereich wird verwendet, um eine bestimmte Position im Text eines Steuerelements zu markieren, z. B. die Position der Texteinfügemarke.

## <a name="acquiring-text-range-objects"></a>Abrufen von Textbereichsobjekten

Clientanwendungen erhalten Textbereichsobjekte mithilfe der Eigenschaften und Methoden der [**IUIAutomationTextPattern-Schnittstelle.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) Die [**IUIAutomationTextRangePattern::D ocumentRange-Eigenschaft**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-get_documentrange) ruft einen Textbereich ab, der den gesamten Textinhalt eines textbasierten Steuerelements darstellt, während andere Methoden Textbereiche abrufen, die einen Teil des Inhalts darstellen, z. B. den ausgewählten Text, den sichtbaren Text oder ein in den Text eingebettetes Objekt.

Die [**Methoden IUIAutomationTextRangePattern::GetVisibleRanges**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-getvisibleranges) und [**GetSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-getselection) können Arrays von Textbereichsobjekten abrufen. Wenn ein Steuerelement durch ein überlappendes Fenster oder ein anderes Objekt teilweise verdeckt wird, gibt **GetVisibleRanges** ein Array zurück, das ein Textbereichsobjekt für jede teilweise sichtbare Textzeile enthält. Ebenso gibt **GetSelection** ein Array zurück, das ein Textbereichsobjekt für jede ausgewählte Spanne enthält, wenn ein textbasiertes Steuerelement die Auswahl mehrerer, unzusammenhängender Textspannen unterstützt.

Mit der [**IUIAutomationTextRangePattern::RangeFromChild-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) kann eine Clientanwendung einen Textbereich abrufen, der ein in den Textinhalt eingebettetes Objekt einschließt. Der Client gibt den [**IUIAutomationElement-Schnittstellenzeiger**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) eines eingebetteten Objekts an, z. B. ein Bild, eine Tabelle oder einen Link, und die Methode gibt einen Textbereich zurück, der das Objekt einschließt. Wenn dem eingebetteten Objekt jedoch kein Text zugeordnet ist, gibt die Methode einen degenerieren Textbereich zurück.

Eine Clientanwendung kann die [**IUIAutomationTextRangePattern::RangeFromPoint-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint) verwenden, um einen Textbereich für den sichtbaren Text oder das eingebettete Objekt abzurufen, das den angegebenen Bildschirmkoordinaten am nächsten liegt.

## <a name="selecting-text-in-a-text-range"></a>Auswählen von Text in einem Textbereich

Die [**IUIAutomationTextRange-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) enthält eine Reihe von Methoden, mit denen eine Clientanwendung die Textauswahl in einem textbasierten Steuerelement steuern kann.

Clientanwendungen können die [**IUIAutomationTextRange::Select-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-select) verwenden, um den Text auszuwählen, der einem Textbereich entspricht, und um ggf. die vorherige Auswahl aus dem Textsteuerelement zu entfernen. Wenn **Sie Select** mit einem degenerieren Textbereich aufrufen, wird die Einfügemarke an die Position des Textbereichs verschoben, ohne Text auszuwählen.

Wenn ein Steuerelement die Auswahl mehrerer, unzusammenhängender Textbereiche unterstützt, kann ein Client die Methoden [**IUIAutomationTextRange::AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-addtoselection) und [**RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-removefromselection) verwenden, um Textbereiche der Auflistung ausgewählter Textbereiche hinzuzufügen und daraus zu entfernen. Wenn das Steuerelement jeweils nur einen ausgewählten Textbereich unterstützt, der Auswahlvorgang jedoch zur Auswahl mehrerer unzusammenhängender Textbereiche führen würde, gibt die Methode entweder einen **E \_ INVALIDOPERATION-Fehler** zurück oder erweitert oder schneidet die aktuelle Auswahl ab. Eine Clientanwendung kann ermitteln, ob ein Steuerelement die Auswahl einzelner oder mehrerer Textspannen oder gar keine unterstützt, indem die [**IUIAutomationTextPattern::SupportedTextSelection-Eigenschaft**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-get_supportedtextselection) überprüft wird.

Wenn ein textbasiertes Steuerelement Texteinfügungen unterstützt, verschiebt das Aufrufen von [**IUIAutomationTextRange::AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-addtoselection) oder [**RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-removefromselection) für einen degenerieren Textbereich im Steuerelement die Einfügemarke, wählt jedoch keinen Text aus.

## <a name="retrieving-text-from-a-text-range"></a>Abrufen von Text aus einem Textbereich

Clientanwendungen können die [**IUIAutomationTextRange::GetText-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) verwenden, um den Nur-Text eines Textbereichs abzurufen. Der Nur-Text enthält alle Steuerzeichen im Quelltext, z. B. Wagenrückläufe und die Unicode-LRM (Left-to-Right Mark). Der Nur-Text enthält keine Markuptags wie HTML, die möglicherweise im Quelltext vorhanden sind. Außerdem werden alle Escapecodes im Quelltext in die Nur-Text-Entsprechungen konvertiert. Beispielsweise wird " &nbsp; " in ein einfaches Leerzeichen konvertiert.

Wenn ein eingebettetes Objekt einen Textbereich umfasst, enthält der Nur-Text den inneren Text des Objekts, aber nicht den alternativen Text (die Name-Eigenschaft des eingebetteten Objekts). Weitere Informationen finden Sie unter [How Benutzeroberflächenautomatisierung Exposes Embedded Objects](uiauto-textpattern-and-embedded-objects-overview.md).

Die [**IUIAutomationTextRange::FindText-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findtext) durchsucht einen Textbereich nach einer bestimmten Zeichenfolge und gibt, wenn sie gefunden wird, einen neuen Textbereich zurück, der die Zeichenfolge umfasst.

## <a name="retrieving-text-attributes-from-a-text-range"></a>Abrufen von Textattributen aus einem Textbereich

Textattribute bestimmen den Formatierungsstil des Texts in einem textbasierten Steuerelement und enthalten z. B. Vordergrundfarbe, Aufzählungszeichen, Schriftgrad usw. Benutzeroberflächenautomatisierung unterstützt eine Reihe von Textattributen und definiert einen Bezeichner für jedes unterstützte Attribut. Eine Clientanwendung kann einen Textbereich für den Wert eines bestimmten Textattributs abfragen, indem sie einen Attributbezeichner in einem Aufruf der [**IUIAutomationTextRange::GetAttributeValue-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) sowie einen Zeiger auf eine [**VARIANT-Struktur**](/windows/win32/api/oaidl/ns-oaidl-variant) angibt, die den Attributwert empfängt. Ausführliche Informationen zu jedem Textattribut, das Benutzeroberflächenautomatisierung unterstützt, finden Sie unter [Textattributbezeichner.](uiauto-textattribute-ids.md)

Der von [**GetAttributeValue abgerufene**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) Wert stellt den Wert des Attributs im gesamten Textbereich dar. Wenn der gesamte Text im Bereich den gleichen Wert für das angegebene Attribut hat, wird dieser Wert von **GetAttributeValue** zurückgegeben. Wenn der Wert des Attributs jedoch innerhalb des Textbereichs variiert, gibt **GetAttributeValue** einen [**IUnknown-Zeiger**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) auf ein statisches Tokenobjekt zurück, das als **ReservedMixedAttribute-Objekt** bezeichnet wird. Um zu ermitteln, ob der Wert eines Attributs in einem Textbereich variiert, sollte eine Clientanwendung die Ergebnisse von **GetAttributeValue** mit dem **ReservedMixedAttribute-Objekt** vergleichen, das aus der [**IUIAutomation::ReservedMixedAttributeValue-Eigenschaft**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_reservedmixedattributevalue) abgerufen wurde.

Ein textbasiertes Steuerelement ist nicht erforderlich, um alle Benutzeroberflächenautomatisierung Textattribute zu unterstützen. Wenn ein Client die [**IUIAutomationTextRange::GetAttributeValue-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) aufruft und den Bezeichner eines nicht unterstützten Attributs übergibt, gibt die Methode einen [**IUnknown-Zeiger**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) auf ein statisches Tokenobjekt namens **ReservedNotSupported-Objekt** zurück. Um zu ermitteln, ob ein bestimmtes Attribut unterstützt wird, sollte eine Clientanwendung die Ergebnisse von **GetAttributeValue** mit dem **ReservedNotSupported-Objekt** vergleichen, das aus der [**IUIAutomation::ReservedNotSupportedValue-Eigenschaft**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_reservednotsupportedvalue) abgerufen wurde.

Clientanwendungen können die [**IUIAutomationTextRange::FindAttribute-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) verwenden, um einen Textbereich nach Text zu durchsuchen, der über ein bestimmtes Textattribut verfügt. Wenn gefunden, gibt die Methode einen neuen Textbereich zurück, der den übereinstimmenden Text umfasst. Beachten Sie, dass **FindAttribute** einen Textbereich für übereinstimmenden Text zurückgibt, auch wenn der Text nicht sichtbar ist.

## <a name="retrieving-embedded-objects-from-a-text-range"></a>Abrufen eingebetteter Objekte aus einem Textbereich

Ein Textbereich kann eingebettete Objekte wie Tabellen, Bilder, Links usw. enthalten. Eine Clientanwendung kann eine Auflistung aller eingebetteten Objekte in einem Bereich abrufen, indem sie die [**IUIAutomationTextRange::GetChildren-Methode aufruft.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) Eingebettete Objekte, die sich mit dem Bereich überschneiden, aber nicht vollständig darin eingeschlossen sind, sind ebenfalls in der Auflistung enthalten. Wenn der Bereich keine eingebetteten Objekte enthält, ruft **GetChildren** eine leere Auflistung ab.

Obwohl dies vom Anbieter des textbasierten Steuerelements abhängt, gibt die [**GetChildren-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) in der Regel keine untergeordneten Elemente der eingebetteten Elemente zurück. Wenn ein Textbereich beispielsweise eine Tabelle mit einer Reihe von untergeordneten Zellen enthält, gibt die **GetChildren-Methode** in der Regel nur das Tabellenelement und nicht die Zellenelemente zurück.

Aus Leistungs- oder Architekturgründen ist [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) möglicherweise nicht in der Lage, [**IUIAutomationElement-Objekte**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) für alle eingebetteten Objekte in einem Textbereich abzurufen. Stattdessen gibt der Anbieter möglicherweise eine Auflistung zurück, die virtualisierte Elemente enthält. Weitere Informationen finden Sie unter [Arbeiten mit virtualisierten Elementen.](uiauto-workingwithvirtualizeditems.md)

## <a name="manipulating-a-text-range"></a>Bearbeiten eines Textbereichs

Die [**IUIAutomationTextRange-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) bietet mehrere Methoden zum Bearbeiten und Navigieren in Textbereichen in einem textbasierten Steuerelement. Die [**Methoden IUIAutomationTextRange::Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move), [**MoveEndpointByUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-moveendpointbyunit)und [**ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit) verschieben einen Textbereich oder einen seiner Endpunkte durch die angegebene Texteinheit, z. B. Zeichen, Wort, Absatz usw. Weitere Informationen finden Sie unter [Benutzeroberflächenautomatisierung Texteinheiten.](/windows/desktop/WinAuto/uiauto-uiautomationtextunits)

Trotz des Namens erweitert die [**ExpandToEnclosingUnit-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit) nicht unbedingt einen Textbereich. Stattdessen wird ein Textbereich "normalisiert", indem die Endpunkte so verschoben werden, dass der Bereich die angegebene Texteinheit genau umfasst. Der Bereich wird erweitert, wenn er kleiner als die angegebene Einheit ist, oder verkürzt, wenn er länger als die angegebene Einheit ist. Das folgende Diagramm zeigt, wie **ExpandToEnclosingUnit** einen Textbereich normalisiert, indem die Endpunkte des Bereichs verschoben werden.

![Diagramm mit Endpunktpositionen vor und nach einem Aufruf von expandtoenclosingunit](images/expandtoenclosingunit.jpg)

Wenn der Textbereich am Anfang einer Texteinheit beginnt und am Anfang oder vor der nächsten Texteinheitsgrenze endet, wird der Endpunkt an die nächste Texteinheitsgrenze verschoben (siehe 1 und 2 in der vorherigen Abbildung).

Wenn der Textbereich am Anfang einer Texteinheit beginnt und bei oder nach der nächsten Einheitengrenze endet, bleibt der Endendpunkt erhalten oder wird nach dem Startendpunkt zurück zur nächsten Einheitengrenze verschoben (siehe 3 und 4 in der vorherigen Abbildung). Wenn zwischen dem Start- und dem Endendpunkt mehr als eine Texteinheitsgrenze vorhanden ist, wird der Endendpunkt nach dem Startendpunkt zurück zur nächsten Einheitengrenze verschoben, was zu einem Textbereich führt, der eine Texteinheit lang ist.

Wenn der Textbereich in der Mitte einer Texteinheit beginnt, wird der Startendpunkt rückwärts an den Anfang der Texteinheit verschoben, und der Endpunkt wird nach Bedarf vorwärts oder rückwärts zur nächsten Einheitengrenze nach dem Startendpunkt verschoben (siehe 5 bis 8 in der vorherigen Abbildung).

Wenn die [**IUIAutomationTextRange::Move-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) aufgerufen wird, normalisiert der Anbieter den Textbereich durch die angegebene Texteinheit. Anschließend verschiebt der Anbieter den Bereich um die angegebene Anzahl von Texteinheiten rückwärts oder vorwärts. Beim Verschieben des Bereichs ignoriert der Anbieter die Grenzen eingebetteter Objekte im Text. (Die Begrenzung der Einheit selbst kann jedoch durch das Vorhandensein eines eingebetteten Objekts beeinflusst werden.) Das folgende Diagramm zeigt, wie die **Move-Methode** einen Textbereich unitweise über eingebettete Objekte und Texteinheitsgrenzen hinweg verschiebt.

![Diagramm, das zeigt, wie die Verschiebemethode Bereichsendpunkte über Objekt- und Texteinheitsgrenzen hinweg verschiebt](images/move.jpg)

Die [**IUIAutomationTextRange::MoveEndpointByUnit-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-moveendpointbyunit) verschiebt einen der Endpunkte um die angegebene Texteinheit vorwärts oder rückwärts. Die folgende Abbildung zeigt, wie ein Endpunkt vorwärts bewegt wird.

![Diagramm, das zeigt, wie moveendpointbyunit den Endpunkt eines Bereichs verschiebt](images/moveendpointbyunit.gif)

Die [**IUIAutomationTextRange::MoveEndpointByRange-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-moveendpointbyrange) ermöglicht einer Clientanwendung, einen Endpunkt eines Textbereichs auf denselben Speicherort wie den angegebenen Endpunkt eines zweiten Textbereichs festzulegen.

## <a name="scrolling-a-text-range-into-view"></a>Scrollen eines Textbereichs in die Ansicht

Die [**IUIAutomationTextRange::ScrollIntoView-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-scrollintoview) führt einen Bildlauf in einem Textbereich durch, sodass der Text im Viewport des textbasierten Steuerelements sichtbar ist. Beim Aufrufen **von ScrollIntoView** kann ein Client angeben, ob der Text am oberen oder unteren Rand des Viewports ausgerichtet werden soll.

## <a name="retrieving-the-enclosing-element-of-a-text-range"></a>Abrufen des umschließenden Elements eines Textbereichs

Eine Clientanwendung kann die [**IUIAutomationTextRange::GetEnclosingElement-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) verwenden, um den [**IUIAutomation-Schnittstellenzeiger**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) des innersten Elements abzurufen, das einen Textbereich umschließt. Das umschließende Element ist in der Regel der Textanbieter, der den Textbereich liefert. Wenn der Textanbieter jedoch untergeordnete Elemente wie Tabellen oder Links unterstützt, kann das umschließende Element ein Nachfolger des Textanbieters sein.

## <a name="comparing-and-cloning-text-ranges"></a>Vergleichen und Klonen von Textbereichen

Die [**IUIAutomationTextRange-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) enthält zwei Methoden zum Vergleichen von Textbereichen. Die [**IUIAutomationTextRange::Compare-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-compareendpoints) vergleicht die Start- und Endendpunkte von zwei Textbereichen und gibt **TRUE** zurück, wenn beide Endpunkte identisch sind. Die **IUIAutomationTextRange::CompareEndpoints-Methode** vergleicht entweder den Start- oder den Endendpunkt der beiden Bereiche. Der Rückgabewert ist 0 (null), wenn die Endpunkte identisch sind, oder ein positiver oder negativer Wert, der die relativen Positionen der beiden Endpunkte angibt.

Clientanwendungen können die [**IUIAutomationTextRange::Clone-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-clone) verwenden, um eine genaue Kopie des Textbereichs zu erstellen. Der neue Textbereich kann unabhängig vom ursprünglichen Textbereich bearbeitet werden.

## <a name="retrieving-annotations"></a>Abrufen von Anmerkungen

Ein Textbereich kann Anmerkungen enthalten, wenn sie vom textbasierten Steuerelement unterstützt werden. Es gibt viele verschiedene Arten von Anmerkungen. Die Headerdatei UIAutomationClient.h definiert einen Satz benannter konstanter Werte, die die Typen von Anmerkungen identifizieren, die Benutzeroberflächenautomatisierung werden. Weitere Informationen finden Sie unter [**Anmerkungstypbezeichner.**](uiauto-annotation-type-identifiers.md)

Einige Arten von Anmerkungen werden durch ein [](uiauto-implementingannotation.md) Automatisierungselement dargestellt, das das Annotation-Steuerelementmuster [**(IUIAutomationAnnotationPattern-Schnittstelle)**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationannotationpattern) unterstützt. Andere Arten von Anmerkungen werden über das [TextRange-Steuerelementmuster](uiauto-about-text-and-textrange-patterns.md) verfügbar gemacht. Beispielsweise könnte ein Anbieter einen einfachen Rechtschreibfehlerindikator verfügbar machen, indem die [**IUIAutomationTextRange::GetAttributeValue-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) ein [**AnnotationTypes-Textattribut**](uiauto-textattribute-ids.md) von [**AnnotationType \_ SpellingError**](uiauto-annotation-type-identifiers.md)und einen NULL-Wert für das [**AnnotationObjects-Textattribut**](uiauto-textattribute-ids.md) zurückgibt.

### <a name="retrieving-annotations-types-from-a-text-range"></a>Abrufen von Anmerkungstypen aus einem Textbereich

Sie können eine Liste der Anmerkungstypen, die in einem Textbereich vorhanden sind, mithilfe der [**IUIAutomationTextRange::GetAttributeValue-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) abrufen. Geben Sie beim Aufrufen der -Methode eine Textattribut-ID von [**UIA \_ AnnotationTypesAttributeId**](uiauto-textattribute-ids.md) und einen Zeiger auf einen Parameter vom Typ [**VARIANT an.**](/windows/win32/api/oaidl/ns-oaidl-variant) Wenn die Methode zurückgegeben wird, enthält der **VARIANT-Parameter** eine Liste von Anmerkungstypbezeichnern, einen für jeden Anmerkungstyp im Textbereich. Weitere Informationen finden Sie unter [**Anmerkungstypbezeichner.**](uiauto-annotation-type-identifiers.md)

### <a name="retrieving-all-annotations-from-a-text-range"></a>Abrufen aller Anmerkungen aus einem Textbereich

Rufen Sie zum Abrufen der Anmerkungen aus einem Textbereich die [**IUIAutomationTextRange::GetAttributeValue-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) auf, und geben Sie dabei eine Textattribut-ID [**von UIA \_ AnnotationObjectsAttributeId**](uiauto-textattribute-ids.md) und einen Zeiger auf einen Parameter vom Typ [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant)an. Wenn die Methode zurückgegeben wird, enthält der **VARIANT-Parameter** eine [**IUIAutomationElementArray-Schnittstelle,**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray) die ein Array von Automatisierungselementen darstellt, eines für jede Anmerkung im Textbereich. Die [**IUIAutomationElementArray::Length-Eigenschaft**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelementarray-get_length) gibt die Anzahl der Elemente im Array an, und die [**IUIAutomationElementArray::GetElement-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelementarray-getelement) ruft die [**IUIAutomationElement-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) für ein bestimmtes Element ab.

### <a name="retrieving-information-about-a-particular-annotation"></a>Abrufen von Informationen zu einer bestimmten Anmerkung

Um Informationen zu einer bestimmten Anmerkung abzurufen, rufen Sie zunächst die [**IUIAutomationElement-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) für das Anmerkungselement ab, wie im vorherigen Abschnitt beschrieben. Rufen Sie als Nächstes die [**IUIAutomationAnnotationPattern-Schnittstelle**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationannotationpattern) für die Anmerkung ab, indem Sie die [**IUIAutomationElement::GetCurrentPatternAs-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpatternas) mit der Steuerelementmuster-ID [**UIA \_ AnnotationPatternId,**](uiauto-controlpattern-ids.md)einem Schnittstellenbezeichner von IID IUIAutomationAnnotationPattern und der Adresse einer Variablen aufrufen, die den \_ **IUIAutomationAnnotation-Zeiger** für die Anmerkung empfängt. Fragen Sie die Eigenschaften der **IUIAutomationAnnotation-Schnittstelle** ab, um den Namen und die Typ-ID des Anmerkungstyps, den Namen des Anmerkungsautors, das Datum und die Uhrzeit der Anmerkung sowie die **IUIAutomationElement-Schnittstelle** für das Element abzurufen, das mit Anmerkungen kommentiert wird.

### <a name="retrieving-the-annotation-target-text"></a>Abrufen des Anmerkungszieltexts

In der Regel gilt eine Anmerkung für eine Teilmenge des Texts in einem Textbereich. Nachdem Sie die [**IUIAutomationElement-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) für eine Anmerkung abgerufen haben, können Sie die Schnittstelle an die [**IUIAutomationTextRange2::RangeFromAnnotation-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider2-rangefromannotation) übergeben, um einen Textbereich abzurufen, der den Text enthält, der das Ziel der Anmerkung ist.

## <a name="retrieving-visual-styles"></a>Abrufen visueller Stile

Ein Anbieter implementiert [](/windows/desktop/WinAuto/uiauto-implementingstyles) das Stil-Steuerelementmuster, um ein Benutzeroberflächenelement mit einem bestimmten Stil, einer bestimmten Füllfarbe, einem Füllmuster oder einer Form zu beschreiben. Dies ist besonders nützlich, wenn Elemente in einem Dokument beschrieben werden, die häufig über solche Stile verfügen. Stile wie diese enthalten häufig Informationen, die für Kunden mit Behinderungen nützlich sind. Stile können beispielsweise eine bestimmte Zeichenfolge als Titel eines Dokuments oder ein bestimmtes Flussdiagrammobjekt als Raute oder Kreis beschreiben.

Sie können die [**IUIAutomationTextRange::GetAttributeValue-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) verwenden, um die Namen und Bezeichner der visuellen Stile abzurufen, die in einem Textbereich verwendet werden. Verwenden Sie [**das Textattribut UIA \_ StyleNameAttributeId,**](uiauto-textattribute-ids.md) um die Formatnamen abzurufen, und [**UIA \_ StyleIdAttributeId,**](uiauto-textattribute-ids.md) um die Stilbezeichner abzurufen.

Ein textbasiertes Steuerelement, das visuelle [](/windows/desktop/WinAuto/uiauto-implementingstyles) Stile unterstützt, kann das Stil-Steuerelementmuster implementieren, um Clients den Zugriff auf Informationen zu einem vom Steuerelement verwendeten visuellen Stil zu ermöglichen. Clients greifen über die [**IUIAutomationStylesPattern-Schnittstelle auf das Stil-Steuerelementmuster**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationstylespattern) zu. Sie können diese Schnittstelle abrufen, indem Sie die [**IUIAutomationElement::GetCurrentPattern-**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) oder [**GetCurrentPatternAs-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpatternas) aufrufen und [**UIA \_ StylesPatternId**](uiauto-controlpattern-ids.md) als Steuerelementmusterbezeichner angeben.

Die [**IUIAutomationStylesPattern-Schnittstelle enthält**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationstylespattern) Eigenschaften und Methoden, die die folgenden Informationen zu einem visuellen Stil bereitstellen:

-   Der Name des visuellen Stils, z. B. "Normal" oder "Überschrift 1".
-   Der Bezeichner des visuellen Stils. Weitere Informationen finden Sie unter [**Formatbezeichner.**](uiauto-style-identifiers.md)
-   Die Farbe, die zum Ausfüllen des textbasierten Steuerelements verwendet wird.
-   Die Farbe des Musters, das zum Ausfüllen des textbasierten Steuerelements verwendet wird.
-   Die Form des textbasierten Steuerelements.
-   Die erweiterten Eigenschaften; das heißt, eine Liste von steuerelementspezifischen Formatnamen und -werten.

## <a name="invoking-context-menus-from-text-ranges"></a>Aufrufen von Kontextmenüs aus Textbereichen

Ab Windows 8.1 unterstützen Textbereiche möglicherweise die [**IUIAutomationTextRange2-Schnittstelle.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange2) Diese Schnittstelle unterstützt die [**ShowContextMenu-Methode.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange2-showcontextmenu) Sie können diese Methode aufrufen, um jedes Kontextmenü auf aufrufen, das einem Textbereich zugeordnet ist. Das Szenario dafür ist die automatischeCorrection von Textbereichen oder die Auswahl eines IME-Kandidaten. In diesen Fällen wird ein Kontextmenü angezeigt, das die Benutzerinteraktion unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Text- und TextRange-Steuerelementmuster](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Benutzeroberflächenautomatisierung Unterstützung für Textinhalte](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Arbeiten mit textbasierten Steuerelementen](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 