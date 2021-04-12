---
title: Verwenden von Text Bereichen
description: In diesem Thema wird beschrieben, wie die Eigenschaften und Methoden der iuiautomationtextrange-Schnittstelle verwendet werden, um auf den Text Inhalt eines textbasierten Steuer Elements zuzugreifen und ihn zu bearbeiten.
ms.assetid: 66BC7324-5322-4996-AF62-766936559F0E
keywords:
- Clients mit Text Bereichs Objekten
- textbasierte Steuerelemente
- Clients, Textbereiche
- Clients, TextRange-Steuerelement Muster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a2aef7c23db6903e3492fec7c83ba7c14599c63
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390562"
---
# <a name="using-text-ranges"></a>Verwenden von Text Bereichen

In diesem Thema wird beschrieben, wie die Eigenschaften und Methoden der [**iuiautomationtextrange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) -Schnittstelle verwendet werden, um auf den Text Inhalt eines textbasierten Steuer Elements zuzugreifen und ihn zu bearbeiten. Sie enthält die folgenden Abschnitte:

-   [Was ist ein Text Bereich?](#using-text-ranges)
-   [Abrufen von Text Bereichs Objekten](#acquiring-text-range-objects)
-   [Auswählen von Text in einem Textbereich](#selecting-text-in-a-text-range)
-   [Abrufen von Text aus einem Textbereich](#retrieving-text-from-a-text-range)
-   [Abrufen von Textattributen aus einem Textbereich](#retrieving-text-attributes-from-a-text-range)
-   [Abrufen von eingebetteten Objekten aus einem Text Bereich](#retrieving-embedded-objects-from-a-text-range)
-   [Bearbeiten eines Text Bereichs](#manipulating-a-text-range)
-   [Scrollen eines Text Bereichs in eine Ansicht](#scrolling-a-text-range-into-view)
-   [Abrufen des einschließenden Elements eines Text Bereichs](#retrieving-the-enclosing-element-of-a-text-range)
-   [Vergleichen und Klonen von Text Bereichen](#comparing-and-cloning-text-ranges)
-   [Anmerkungen werden abgerufen.](#retrieving-annotations)
    -   [Abrufen von Anmerkungen-Typen aus einem Text Bereich](#retrieving-annotations-types-from-a-text-range)
    -   [Abrufen aller Anmerkungen aus einem Text Bereich](#retrieving-all-annotations-from-a-text-range)
    -   [Abrufen von Informationen zu einer bestimmten Anmerkung](#retrieving-information-about-a-particular-annotation)
    -   [Abrufen des Zieltexts der Anmerkung](#retrieving-the-annotation-target-text)
-   [Abrufen von visuellen Stilen](#retrieving-visual-styles)
-   [Aufrufen von Kontextmenüs aus Text Bereichen](#invoking-context-menus-from-text-ranges)
-   [Zugehörige Themen](#related-topics)

## <a name="what-is-a-text-range"></a>Was ist ein Text Bereich?

Das Microsoft UI Automation-Textobjekt Modell basiert auf dem Konzept des *Text Bereichs*. Ein Textbereich ist ein Objekt, das die [**iuiautomationtextrange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) -Schnittstelle verfügbar macht und einen zusammenhängenden Textbereich in einem textbasierten Steuerelement darstellt. Jeder Textbereich verfügt sowohl über einen Start Endpunkt als auch über einen endendpunkt, und der gesamte Text Inhalt zwischen den beiden Endpunkten wird als Teil des Bereichs behandelt. Ein Textbereich, dessen Start Endpunkt und endendpunkt sich am gleichen Speicherort befinden, wird als *degenerierter* (oder leerer) Textbereich bezeichnet. Ein degenerierter Textbereich wird verwendet, um eine bestimmte Position im Text eines-Steuer Elements zu markieren, z. b. die Position der Text Einfügemarke.

## <a name="acquiring-text-range-objects"></a>Abrufen von Text Bereichs Objekten

Client Anwendungen erhalten Text Bereichs Objekte mithilfe der Eigenschaften und Methoden der [**iuiautomationtextpattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) -Schnittstelle. Die [**iuiautomationtextrangepattern::D ocumentrange**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-get_documentrange) -Eigenschaft ruft einen Textbereich ab, der den gesamten Text Inhalt eines textbasierten Steuer Elements darstellt, während andere Methoden Textbereiche abrufen, die einen Teil des Inhalts darstellen, z. b. den markierten Text, den sichtbaren Text oder ein Objekt, das in den Text eingebettet ist.

Mit der [**iuiautomationtextrangepattern:: GetVisibleRanges**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-getvisibleranges) -Methode und der [**GetSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-getselection) -Methode können Arrays von Text Bereichs Objekten abgerufen werden. Wenn ein Steuerelement teilweise von einem überlappenden Fenster oder einem anderen Objekt verdeckt wird, gibt **GetVisibleRanges** ein Array zurück, das ein Text Bereichs Objekt für jede teilweise sichtbare Textzeile enthält. Wenn ein textbasiertes Steuerelement die Auswahl mehrerer, nicht zusammenhängender Text spannen unterstützt, gibt **GetSelection** ein Array zurück, das ein Text Bereichs Objekt für jede ausgewählte Spanne enthält.

Die [**iuiautomationtextrangepattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) -Methode ermöglicht es einer Client Anwendung, einen Textbereich abzurufen, der ein Objekt einschließt, das in den Text Inhalt eingebettet ist. Der Client gibt den [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Schnittstellen Zeiger eines eingebetteten Objekts an, z. b. ein Bild, eine Tabelle oder einen Hyperlink, und die-Methode gibt einen Textbereich zurück, der das-Objekt einschließt. Wenn dem eingebetteten Objekt jedoch kein Text zugeordnet ist, gibt die Methode einen degenerierten Textbereich zurück.

Eine Client Anwendung kann die [**iuiautomationtextrangepattern:: RangeFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint) -Methode verwenden, um einen Textbereich für den sichtbaren Text oder das eingebettete Objekt abzurufen, das den angegebenen Bildschirm Koordinaten am nächsten liegt.

## <a name="selecting-text-in-a-text-range"></a>Auswählen von Text in einem Textbereich

Die [**iuiautomationtextrange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) -Schnittstelle enthält eine Reihe von Methoden, die es einer Client Anwendung ermöglichen, die Auswahl von Text in einem textbasierten Steuerelement zu steuern.

Client Anwendungen können die [**iuiautomationtextrange:: SELECT**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-select) -Methode verwenden, um den Text auszuwählen, der einem Textbereich entspricht, und um ggf. die vorherige Auswahl aus dem Text Steuerelement zu entfernen. Durch das Aufrufen von **Select** mit einem degenerierten Textbereich wird die Einfügemarke an die Position des Text Bereichs verschoben, ohne dass Text ausgewählt wird.

Wenn ein Steuerelement die Auswahl mehrerer, nicht zusammenhängender Textabschnitte unterstützt, kann ein Client die [**iuiautomationtextrange:: adddeselection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-addtoselection) -Methode und die [**RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-removefromselection) -Methode verwenden, um Textbereiche der Auflistung ausgewählter Textbereiche hinzuzufügen und daraus zu entfernen. Wenn das Steuerelement nur einen markierten Textbereich gleichzeitig unterstützt, der Auswahl Vorgang aber dazu führt, dass mehrere nicht zusammenhängende Textbereiche ausgewählt werden, gibt die Methode entweder einen **E \_ InvalidOperation** -Fehler zurück oder erweitert oder verkürzt die aktuelle Auswahl. Eine Client Anwendung kann ermitteln, ob ein Steuerelement die Auswahl von einzelnen oder mehreren Text spannen bzw. gar keinen Text unterstützt, indem die [**iuiautomationtextpattern:: SupportedTextSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-get_supportedtextselection) -Eigenschaft überprüft wird.

Wenn ein textbasiertes Steuerelement Text Einfügungen unterstützt, wird durch den Aufruf von [**iuiautomationtextrange:: AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-addtoselection) oder [**RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-removefromselection) für einen degenerierten Textbereich im-Steuerelement die Einfügemarke verschoben, aber es wird kein Text ausgewählt.

## <a name="retrieving-text-from-a-text-range"></a>Abrufen von Text aus einem Textbereich

Client Anwendungen können die [**iuiautomationtextrange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) -Methode verwenden, um den reinen Text eines Text Bereichs abzurufen. Der nur-Text enthält alle im Quelltext gefundenen Steuerzeichen, z. b. Wagen Rückläufe und Unicode-Zeichen von links nach rechts (LRM). Der Klartext enthält keine Markup Tags, wie z. b. html, die möglicherweise im Quelltext vorhanden sind. Außerdem werden alle Escapecodes im Quelltext in die nur-Text-Entsprechungen konvertiert. Beispielsweise wird " &nbsp; " in ein einfaches Leerzeichen konvertiert.

Wenn ein eingebettetes Objekt einen Textbereich umfasst, enthält der Klartext den inneren Text des Objekts, jedoch nicht den alternativen Text (die Name-Eigenschaft des eingebetteten Objekts). Weitere Informationen finden Sie unter [How UI Automation macht Embedded Objects](uiauto-textpattern-and-embedded-objects-overview.md)verfügbar.

Mit der [**iuiautomationtextrange:: FindText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findtext) -Methode wird ein Textbereich für eine bestimmte Zeichenfolge durchsucht, und wenn Sie gefunden wird, wird ein neuer Textbereich zurückgegeben, der die Zeichenfolge umfasst.

## <a name="retrieving-text-attributes-from-a-text-range"></a>Abrufen von Textattributen aus einem Textbereich

Text Attribute bestimmen den Formatierungs Stil des Texts in einem textbasierten Steuerelement und enthalten beispielsweise die Vordergrundfarbe, den Aufzählungs Stil, den Schrift Grad usw. Die Benutzeroberflächen Automatisierung unterstützt eine Reihe von Textattributen und definiert einen Bezeichner für jedes unterstützte Attribut. Eine Client Anwendung kann einen Textbereich für den Wert eines bestimmten Text Attributs Abfragen, indem ein Attribut Bezeichner in einem Aufruf der [**iuiautomationtextrange:: GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) -Methode angegeben wird, zusammen mit einem Zeiger auf eine [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) -Struktur, die den Attribut Wert empfängt. Ausführliche Informationen zu jedem Text Attribut, das von der Benutzeroberflächen Automatisierung unterstützt wird, finden Sie unter [Text Attribute Identifiers](uiauto-textattribute-ids.md).

Der von [**GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) abgerufene Wert stellt den Wert des Attributs für den gesamten Textbereich dar. Wenn der gesamte Text im Bereich denselben Wert für das angegebene Attribut hat, wird dieser Wert von **GetAttributeValue** zurückgegeben. Wenn der Wert des Attributs im Textbereich variiert, gibt **GetAttributeValue** einen [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Zeiger auf ein statisches Tokenobjekt zurück, das als **reservedmixedattribute** -Objekt bezeichnet wird. Um zu ermitteln, ob der Wert eines Attributs in einem Textbereich variiert, sollte eine Client Anwendung die Ergebnisse von **GetAttributeValue** mit dem **reservedmixedattribute** -Objekt vergleichen, das von der [**iuiautomation:: reservedmixedattributevalue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_reservedmixedattributevalue) -Eigenschaft abgerufen wurde.

Ein textbasiertes Steuerelement ist nicht erforderlich, um alle Text Attribute der Benutzeroberflächen Automatisierung zu unterstützen. Wenn ein Client die [**iuiautomationtextrange:: GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) -Methode aufruft und den Bezeichner eines nicht unterstützten Attributs übergibt, gibt die Methode einen [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Zeiger auf ein statisches Tokenobjekt zurück, das als **reservednotsupported** -Objekt bezeichnet wird. Um zu ermitteln, ob ein bestimmtes Attribut unterstützt wird, sollte eine Client Anwendung die Ergebnisse von **GetAttributeValue** mit dem **reservednotsupported** -Objekt vergleichen, das von der [**iuiautomation:: reservednotsupportedvalue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_reservednotsupportedvalue) -Eigenschaft abgerufen wurde.

Client Anwendungen können die [**iuiautomationtextrange:: FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) -Methode verwenden, um einen Textbereich nach Text zu durchsuchen, der über ein bestimmtes Text Attribut verfügt. Wenn Sie gefunden wird, gibt die Methode einen neuen Textbereich zurück, der den übereinstimmenden Text umfasst. Beachten Sie, dass **FindAttribute** einen Textbereich für den übereinstimmenden Text zurückgibt, auch wenn der Text nicht sichtbar ist.

## <a name="retrieving-embedded-objects-from-a-text-range"></a>Abrufen von eingebetteten Objekten aus einem Text Bereich

Ein Textbereich kann eingebettete Objekte (z. b. Tabellen, Bilder, Hyperlinks usw.) enthalten. Eine Client Anwendung kann eine Auflistung aller eingebetteten Objekte in einem Bereich abrufen, indem Sie die [**iuiautomationtextrange:: GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) -Methode aufrufen. Eingebettete Objekte, die sich mit dem Bereich überlappen, aber nicht vollständig von diesem eingeschlossen sind, sind auch in der Auflistung enthalten. Wenn der Bereich keine eingebetteten Objekte enthält, ruft **GetChildren** eine leere Auflistung ab.

Obwohl Sie vom Anbieter des textbasierten Steuer Elements abhängt, gibt die [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) -Methode in der Regel keine untergeordneten Elemente der eingebetteten Elemente zurück. Wenn ein Textbereich z. b. eine Tabelle mit einer Reihe von untergeordneten Zellen enthält, gibt die **GetChildren** -Methode in der Regel nur das Table-Element und nicht die Cell-Elemente zurück.

Aus Leistungs-oder Architektur Gründen können [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) möglicherweise [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Objekte nicht für alle eingebetteten Objekte in einem Textbereich abrufen. Stattdessen gibt der Anbieter möglicherweise eine Auflistung zurück, die virtualisierte Elemente einschließt. Weitere Informationen finden Sie unter [Arbeiten mit virtualisierten Elementen](uiauto-workingwithvirtualizeditems.md).

## <a name="manipulating-a-text-range"></a>Bearbeiten eines Text Bereichs

Die [**iuiautomationtextrange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) -Schnittstelle stellt verschiedene Methoden zum Bearbeiten und Navigieren von Textbereichen in einem textbasierten Steuerelement bereit. Die Methoden [**iuiautomationtextrange:: Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move), [**MoveEndpointByUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-moveendpointbyunit)und [**expanddeenclosingunit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit) verschieben einen Textbereich oder einen seiner Endpunkte mit der angegebenen Text Einheit, z. b. Zeichen, Wort, Absatz usw. Weitere Informationen finden Sie unter [Benutzeroberflächen Automatisierung-Text Einheiten](/windows/desktop/WinAuto/uiauto-uiautomationtextunits).

Trotz des Namens erweitert die [**expanddeenclosingunit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit) -Methode nicht notwendigerweise einen Textbereich. Stattdessen wird ein Textbereich durch Verschieben der Endpunkte "normalisiert", sodass der Bereich die angegebene Text Einheit exakt umfasst. Der Bereich wird erweitert, wenn er kleiner als die angegebene Einheit ist, oder verkürzt, wenn er länger als die angegebene Einheit ist. Das folgende Diagramm zeigt, wie **expandumenclosingunit** einen Textbereich normalisiert, indem die Endpunkte des Bereichs verschoben werden.

![Diagramm, das Endpunkt Positionen vor und nach einem aufzurufenden ExpandToEnclosingUnit-Befehl anzeigt](images/expandtoenclosingunit.jpg)

Wenn der Textbereich am Anfang einer Text Einheit beginnt und am Anfang von oder vor der nächsten Textzeile endet, wird der endendpunkt an die nächste Text Einheiten Grenze verschoben (siehe 1 und 2 in der vorherigen Abbildung).

Wenn der Textbereich am Anfang einer Text Einheit beginnt und bei oder nach der nächsten Einheiten Grenze endet, wird der endendpunkt beibehalten oder nach dem Start Endpunkt zurück zur nächsten Einheiten Grenze verschoben (siehe 3 und 4 in der vorherigen Abbildung). Wenn zwischen den Anfangs-und endendpunkten mehr als eine Text Einheiten Grenze vorhanden ist, wird der endendpunkt nach dem Start Endpunkt rückwärts zur nächsten Einheiten Grenze verschoben, was zu einem Textbereich mit einer Länge von einer Text Einheit führt.

Wenn der Textbereich in der Mitte einer Text Einheit beginnt, wird der Start Endpunkt rückwärts zum Anfang der Text Einheit verschoben, und der endendpunkt wird ggf. nach vorne oder rückwärts an die nächste Einheiten Grenze nach dem Start Endpunkt verschoben (siehe die vorherige Abbildung 5 bis 8).

Wenn die [**iuiautomationtextrange:: Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) -Methode aufgerufen wird, normalisiert der Anbieter den Textbereich um die angegebene Text Einheit. Anschließend verschiebt der Anbieter den Bereich um die angegebene Anzahl von Text Einheiten rückwärts oder vorwärts. Beim Verschieben des Bereichs ignoriert der Anbieter die Grenzen von eingebetteten Objekten im Text. (Die Einheiten Grenze selbst kann jedoch durch das vorhanden sein eines eingebetteten Objekts beeinträchtigt werden.) Im folgenden Diagramm wird veranschaulicht, wie die **Move** -Methode einen Textbereich, Unit by Unit, über eingebettete Objekte und Text Einheiten Grenzen hinweg verschiebt.

![Diagramm, das zeigt, wie die Move-Methode Bereichs Endpunkte über Objekt-und Text Einheiten Grenzen hinweg verschiebt](images/move.jpg)

Die [**iuiautomationtextrange:: muveendpointbyunit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-moveendpointbyunit) -Methode verschiebt einen der Endpunkte um die angegebene Text Einheit vorwärts oder rückwärts. In der folgenden Abbildung wird gezeigt, wie ein Endpunkt vorwärts bewegt wird.

![Diagramm, das zeigt, wie "muveendpointbyunit" den Endpunkt eines Bereichs verschiebt](images/moveendpointbyunit.gif)

Mit der [**iuiautomationtextrange:: wveendpointbyrange**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-moveendpointbyrange) -Methode kann eine Client Anwendung einen Endpunkt eines Text Bereichs auf denselben Speicherort wie den angegebenen Endpunkt eines zweiten Text Bereichs festlegen.

## <a name="scrolling-a-text-range-into-view"></a>Scrollen eines Text Bereichs in eine Ansicht

Die [**iuiautomationtextrange:: ScrollIntoView**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-scrollintoview) -Methode scrollt einen Textbereich, sodass der Text im Viewport des textbasierten Steuer Elements sichtbar ist. Beim Aufrufen von **ScrollIntoView** kann ein Client angeben, ob der Text am oberen oder unteren Rand des Viewports ausgerichtet werden soll.

## <a name="retrieving-the-enclosing-element-of-a-text-range"></a>Abrufen des einschließenden Elements eines Text Bereichs

Eine Client Anwendung kann die [**iuiautomationtextrange:: GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) -Methode verwenden, um den [**iuiautomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) -Schnittstellen Zeiger des innersten Elements abzurufen, das einen Textbereich einschließt. Das einschließende Element ist in der Regel der Text Anbieter, der den Textbereich bereitstellt. Wenn der Text Anbieter jedoch untergeordnete Elemente wie Tabellen oder Hyperlinks unterstützt, kann das einschließende Element ein Nachfolger des Text Anbieters sein.

## <a name="comparing-and-cloning-text-ranges"></a>Vergleichen und Klonen von Text Bereichen

Die [**iuiautomationtextrange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) -Schnittstelle enthält zwei Methoden zum Vergleichen von Textbereichen. Mit der [**iuiautomationtextrange:: Compare**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-compareendpoints) -Methode werden die Anfangs-und Endpunkte von zwei Textbereichen verglichen und **true** zurückgegeben, wenn beide Endpunkte identisch sind. Die **iuiautomationtextrange:: compareEndPoints** -Methode vergleicht entweder den Start-oder endendpunkt der beiden Bereiche. Der Rückgabewert ist 0 (null), wenn die Endpunkte gleich sind, oder ein positiver Wert oder ein negativer Wert, der die relativen Positionen der beiden Endpunkte angibt.

Client Anwendungen können die [**iuiautomationtextrange:: Clone**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-clone) -Methode verwenden, um eine exakte Kopie des Text Bereichs zu erstellen. Der neue Textbereich kann unabhängig vom ursprünglichen Textbereich bearbeitet werden.

## <a name="retrieving-annotations"></a>Anmerkungen werden abgerufen.

Ein Textbereich kann Anmerkungen enthalten, wenn Sie vom textbasierten Steuerelement unterstützt werden. Es gibt viele verschiedene Arten von Anmerkungen. Die UIAutomationClient. h-Header Datei definiert einen Satz benannter konstanter Werte, mit denen die Typen von Anmerkungen identifiziert werden, die von der Benutzeroberflächen Automatisierung unterstützt werden. Weitere Informationen finden Sie unter [**Annotation-Typbezeichner**](uiauto-annotation-type-identifiers.md).

Einige Arten von Anmerkungen werden durch ein Automatisierungs Element dargestellt, das das [Annotation](uiauto-implementingannotation.md) -Steuerelement Muster unterstützt ([**iuiautomationannotationpattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationannotationpattern) -Schnittstelle). Andere Arten von Anmerkungen werden über das [TextRange](uiauto-about-text-and-textrange-patterns.md) -Steuerelement Muster verfügbar gemacht. Ein Anbieter könnte z. b. einen einfachen Rechtschreibfehler Indikator verfügbar machen, indem die [**iuiautomationtextrange:: GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) -Methode ein [**annotationtypes**](uiauto-textattribute-ids.md) -Text Attribut von [**AnnotationType \_ Rechtschreib enror**](uiauto-annotation-type-identifiers.md)und einen NULL-Wert für das [**annotationobjects**](uiauto-textattribute-ids.md) Text-Attribut zurückgibt.

### <a name="retrieving-annotations-types-from-a-text-range"></a>Abrufen von Anmerkungen-Typen aus einem Text Bereich

Sie können eine Liste der Typen von Anmerkungen, die in einem Textbereich vorhanden sind, mithilfe der [**iuiautomationtextrange:: GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) -Methode abrufen. Geben Sie beim Aufrufen der-Methode eine Text Attribut-ID von [**UIA \_ annotationtypesattributeid**](uiauto-textattribute-ids.md) und einen Zeiger auf einen Parameter des Typs [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant)an. Wenn die-Methode zurückgibt, enthält der **Variant** -Parameter eine Liste von Anmerkung-typbezeichatoren, eine für jeden Typ von Anmerkung im Textbereich. Weitere Informationen finden Sie unter [**Annotation-Typbezeichner**](uiauto-annotation-type-identifiers.md).

### <a name="retrieving-all-annotations-from-a-text-range"></a>Abrufen aller Anmerkungen aus einem Text Bereich

Um die Anmerkungen aus einem Textbereich abzurufen, rufen Sie die [**iuiautomationtextrange:: GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) -Methode auf, indem Sie eine Text Attribut-ID von [**UIA \_ annotationobjectsattributeid**](uiauto-textattribute-ids.md) und einen Zeiger auf einen Parameter des Typs [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant)angeben. Wenn die-Methode zurückgibt, enthält der **Variant** -Parameter eine [**iuiautomationelementarray**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray) -Schnittstelle, die ein Array von Automatisierungs Elementen darstellt, eines für jede Anmerkung im Textbereich. Die [**iuiautomationelementarray:: length**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelementarray-get_length) -Eigenschaft gibt die Anzahl der Elemente im Array an, und die [**iuiautomationelementarray:: GetElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelementarray-getelement) -Methode ruft die [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Schnittstelle für ein bestimmtes Element ab.

### <a name="retrieving-information-about-a-particular-annotation"></a>Abrufen von Informationen zu einer bestimmten Anmerkung

Rufen Sie zum Abrufen von Informationen über eine bestimmte Anmerkung zuerst die [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Schnittstelle für das Anmerkung-Element ab, wie im vorherigen Abschnitt beschrieben. Rufen Sie als nächstes die [**iuiautomationannotationpattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationannotationpattern) -Schnittstelle für die Anmerkung ab, indem Sie das [**iuiautomationelement:: getcurrentpatternas**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpatternas) -Methode mit der Steuerelement Muster-ID [**UIA \_ annotationpatternid**](uiauto-controlpattern-ids.md), einem Schnittstellen Bezeichner von IID \_ iuiautomationannotationpattern und der Adresse einer Variablen, die den **iuiautomationannotation** -Zeiger für die Anmerkung empfängt. Fragen Sie die Eigenschaften der **iuiautomationannotation** -Schnittstelle ab, um den Namen des Anmerkung-Typs und den Typ-ID, den Namen des Autors der Anmerkung, das Datum und die Uhrzeit der Anmerkung und die **iuiautomationelement** -Schnittstelle für das Element, das mit Anmerkungen versehen wird, abzurufen.

### <a name="retrieving-the-annotation-target-text"></a>Abrufen des Zieltexts der Anmerkung

In der Regel gilt eine Anmerkung für eine Teilmenge des Texts in einem Textbereich. Nachdem Sie die [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Schnittstelle für eine Anmerkung abgerufen haben, können Sie die-Schnittstelle an die [**IUIAutomationTextRange2:: rangefromannotation**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider2-rangefromannotation) -Methode übergeben, um einen Textbereich abzurufen, der den Text enthält, der das Ziel der Anmerkung ist.

## <a name="retrieving-visual-styles"></a>Abrufen von visuellen Stilen

Ein Anbieter implementiert das [Stile](/windows/desktop/WinAuto/uiauto-implementingstyles) -Steuerelement Muster, um ein UI-Element zu beschreiben, das einen bestimmten Stil, eine bestimmte Füllfarbe, ein Füllmuster oder eine Form aufweist. Dies ist besonders nützlich, wenn Elemente in einem Dokument beschrieben werden, die häufig über solche Stile verfügen. Solche Stile enthalten häufig Informationen, die für Kunden mit Behinderungen nützlich sind. Stile können z. b. eine bestimmte Zeichenfolge als Titel eines Dokuments oder ein bestimmtes Flussdiagramm Objekt als Diamant oder Kreis beschreiben.

Sie können die [**iuiautomationtextrange:: GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) -Methode verwenden, um die Namen und Bezeichner der visuellen Stile abzurufen, die in einem Textbereich verwendet werden. Verwenden Sie das Attribut [**UIA \_ stylenameattributeid**](uiauto-textattribute-ids.md) Text, um die Stilnamen abzurufen, und [**UIA \_ styleidattributeid**](uiauto-textattribute-ids.md) , um die Format Bezeichner abzurufen.

Ein textbasiertes Steuerelement, das visuelle Stile unterstützt, kann das [Stile](/windows/desktop/WinAuto/uiauto-implementingstyles) -Steuerelement Muster implementieren, damit Clients auf Informationen über einen visuellen Stil zugreifen können, der vom Steuerelement verwendet wird. Clients greifen auf das Stile-Steuerelement Muster über die [**iuiautomationstylespattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationstylespattern) -Schnittstelle zu. Sie können diese Schnittstelle abrufen, indem Sie die [**iuiautomationelement:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) -Methode oder [**getcurrentpatternas**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpatternas) -Methode aufrufen und dabei [**UIA \_ stylespatternid**](uiauto-controlpattern-ids.md) als Bezeichner für das Steuerelement Muster angeben.

Die [**iuiautomationstylespattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationstylespattern) -Schnittstelle enthält Eigenschaften und Methoden, die die folgenden Informationen zu einem visuellen Stil bereitstellen:

-   Der Name des visuellen Stils, z. b. "Normal" oder "Überschrift 1".
-   Der Bezeichner des visuellen Stils. Weitere Informationen finden Sie unter [](uiauto-style-identifiers.md)Format Bezeichner.
-   Die Farbe, die zum Ausfüllen des textbasierten Steuer Elements verwendet wird.
-   Die Farbe des Musters, das verwendet wird, um das textbasierte Steuerelement auszufüllen.
-   Die Form des textbasierten Steuer Elements.
-   Die erweiterten Eigenschaften; Das heißt, eine Liste von Steuerelement spezifischen Format Namen und Werten.

## <a name="invoking-context-menus-from-text-ranges"></a>Aufrufen von Kontextmenüs aus Text Bereichen

Beginnend mit Windows 8.1 unterstützt Textbereiche möglicherweise die [**IUIAutomationTextRange2**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange2) -Schnittstelle. Diese Schnittstelle unterstützt die [**ShowContextMenu**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange2-showcontextmenu) -Methode. Sie können diese Methode aufrufen, um ein beliebiges Kontextmenü aufzurufen, das einem Textbereich zugeordnet ist. Das Szenario hierfür ist die automatische Korrektur von Textbereichen oder der Auswahl von IME Candidate. In diesen Fällen wird ein Kontextmenü angezeigt, das die Interaktion von Benutzern unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Text-und TextRange-Steuerelement Muster](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Benutzeroberflächenautomatisierungs-Unterstützung für Textinhalte](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Arbeiten mit Text basierten Steuerelementen](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 