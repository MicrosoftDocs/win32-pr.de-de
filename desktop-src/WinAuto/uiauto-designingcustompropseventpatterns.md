---
title: Entwerfen von benutzerdefinierten Eigenschaften, Ereignissen und Steuerelement Mustern
description: Der Entwurf einer benutzerdefinierten Eigenschaft, eines Ereignisses oder eines Steuerelement Musters sollte in einer Vielzahl von Steuerungs Implementierungen nützlich sein.
ms.assetid: e4b224a0-3958-4ae7-96cb-fe6dc16511a7
keywords:
- Benutzeroberflächen Automatisierung, benutzerdefinierte Eigenschaften
- UI-Automatisierung, Übersicht über Ereignisse
- UI-Automatisierung, Übersicht über Steuerelement Muster
- Benutzeroberflächen Automatisierung, Entwerfen von benutzerdefinierten Eigenschaften
- Benutzeroberflächen Automatisierung, Entwerfen von Ereignissen
- Benutzeroberflächen Automatisierung, Entwerfen von Steuerelement Mustern
- UI-Automatisierung, WinEvents
- benutzerdefinierte Eigenschaften, entwerfen
- Ereignisse, entwerfen
- Ereignisse, WinEvents
- Steuerelement Muster, entwerfen
- WinEvents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e6973356fe6be922e73eef70e5107b6dcabe0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390375"
---
# <a name="design-custom-properties-events-and-control-patterns"></a>Entwerfen von benutzerdefinierten Eigenschaften, Ereignissen und Steuerelement Mustern

Der Entwurf einer benutzerdefinierten Eigenschaft, eines Ereignisses oder eines Steuerelement Musters sollte in einer Vielzahl von Steuerungs Implementierungen nützlich sein. Steuerungs-oder anwendungsspezifische Entwürfe, die nur in begrenzten Szenarios nützlich sind, sollten vermieden werden. Der Entwurf sollte das Beispiel für die vorhandenen Eigenschaften, Ereignisse und Steuerelemente der Microsoft-Benutzeroberflächen Automatisierung befolgen, die sorgfältig festgelegt wurden, um die Anforderungen einer Vielzahl von Barrierefreiheits-und automatisierten Testanwendungen zu erfüllen.

Das Implementieren der Spezifikation für eine benutzerdefinierte Eigenschaft, ein Ereignis oder ein Steuerelement Muster umfasst die Zusammenarbeit und Vereinbarung von Parteien auf der Client-und der Anbieterseite und erfordert, dass beide Parteien die Spezifikation einheitlich implementieren. Es wird empfohlen, mit Branchenorganisationen wie z. b. der [Barrierefreiheit-Interoperabilitäts-Alliance (AIA)](https://www.atia.org/) zu arbeiten, um die Spezifikation für die benutzerdefinierte Eigenschaft, das Ereignis oder das Steuerelement Muster zu entwerfen Auf diese Weise kann ein Konsens erreicht werden, und die Interoperabilität mit den verschiedensten Anwendungen kann sichergestellt werden.

Dieses Thema enthält folgende Abschnitte:

-   [Verwendungszwecke von benutzerdefinierten Eigenschaften und Ereignissen](#when-to-use-custom-properties-and-events)
-   [Entwerfen von benutzerdefinierten Eigenschaften](#designing-custom-properties)
-   [Entwerfen von benutzerdefinierten Ereignissen](#designing-custom-events)
    -   [Benutzerdefinierte Benutzeroberflächenautomatisierungs-Ereignisse und WinEvents](#custom-ui-automation-events-and-winevents)
-   [Entwerfen von benutzerdefinierten Steuerelement Mustern](#designing-custom-control-patterns)
-   [Benutzerdefinierte Steuerelement Typen](#custom-control-types)
-   [Zugehörige Themen](#related-topics)

## <a name="when-to-use-custom-properties-and-events"></a>Verwendungszwecke von benutzerdefinierten Eigenschaften und Ereignissen

Stellen Sie vor dem Erstellen einer benutzerdefinierten Eigenschaft, eines Ereignisses oder eines Steuerelement Musters sicher, dass die Benutzeroberflächen Automatisierung keine vorhandene Lösung bereitstellt. Das Erstellen eines benutzerdefinierten "Click"-Steuerelement Musters ist beispielsweise nicht erforderlich, da diese Funktionalität bereits vom [Aufruf](uiauto-implementinginvoke.md) Steuerungs Muster beschrieben wird.

Wenn Sie festlegen, dass eine benutzerdefinierte Eigenschaft, ein Ereignis oder ein Steuerelement Muster erforderlich ist, stellen Sie sicher, dass es nicht zu ungenau oder generisch ist. Ein Steuerelement Muster namens "Show" ist z. b. nicht nützlich, da die Sichtbarkeit eines Steuer Elements durch eine Availability-Eigenschaft des Elements angegeben werden kann, wie z. b. [**UIA \_ isexpandredusepatternavailablepropertyid**](uiauto-control-pattern-availability-propids.md) oder [**UIA \_ isscrollitempatternavailablepropertyid**](uiauto-control-pattern-availability-propids.md).

Vergewissern Sie sich vor der Implementierung einer benutzerdefinierten Lösung sorgfältig, dass Sie benötigt wird, und entwerfen Sie die Funktionalität vollständig.

## <a name="designing-custom-properties"></a>Entwerfen von benutzerdefinierten Eigenschaften

Die Benutzeroberflächen Automatisierung beinhaltet zwei grundlegende Arten von Eigenschaften: Automatisierungs Element Eigenschaften und Steuerelement Muster Eigenschaften. Die Automatisierungs Element Eigenschaften bestehen aus einem gemeinsamen Satz von Eigenschaften, z. b. "Name", "AcceleratorKey" und "ClassName", die unabhängig vom Steuer Elementtyp von allen Benutzeroberflächenautomatisierungs-Elementen verfügbar gemacht werden. Steuerelement Muster Eigenschaften werden von einem Steuerelement über ein bestimmtes Steuerelement Muster verfügbar gemacht. Jedes Steuerelement Muster verfügt über einen entsprechenden Satz von Steuerelement Mustern-Eigenschaften, die das Steuerelement verfügbar machen muss. Ein Steuerelement, das das [Raster](uiauto-implementinggrid.md) -Steuerelement Muster unterstützt, macht z. b. die Eigenschaften ColumnCount und RowCount verfügbar.

Eine benutzerdefinierte Automatisierungs Element Eigenschaft oder Steuerelement Muster-Eigenschaft sollte den folgenden Entwurfs Richtlinien entsprechen:

-   Eine benutzerdefinierte Eigenschaft muss einen der folgenden Datentypen aufweisen, die durch die [**uiautomationtype**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype) -Enumeration angegeben werden. Für benutzerdefinierte Eigenschaften werden keine anderen Datentypen unterstützt.
    -   **Uiautomationtype \_ bool**
    -   **Uiautomationtype \_ Double**
    -   **Uiautomationtype- \_ Element**
    -   **Uiautomationtype \_ int**
    -   **Uiautomationtype- \_ Punkt**
    -   **Uiautomationtype- \_ Zeichenfolge**
-   Wenn die benutzerdefinierte Eigenschaft Zeichen folgen Daten ([**BSTR**](/previous-versions/windows/desktop/automat/bstr)) enthält, muss die Spezifikation angeben, ob die Eigenschaft lokalisierbar ist (d. h. ob die Zeichenfolge in verschiedene Benutzeroberflächen Sprachen übersetzt werden kann).
-   Die benutzerdefinierte Eigenschaft sollte sich nicht mit den Features oder Funktionen vorhandener Eigenschaften überschneiden.

## <a name="designing-custom-events"></a>Entwerfen von benutzerdefinierten Ereignissen

Anwendungen verwenden Benutzeroberflächenautomatisierungs-Ereignis Benachrichtigungen, um auf Änderungen und Aktionen in Bezug auf Benutzeroberflächen Elemente zu reagieren Den meisten Eigenschaften wurden geänderte Ereignisse zugeordnet, die von der Benutzeroberflächen Automatisierung ausgelöst werden, wenn sich der Wert der-Eigenschaft ändert. Wenn Sie eine benutzerdefinierte Eigenschaft einführen, sollten Sie in Erwägung gezogen werden, ggf. entsprechende benutzerdefinierte Ereignisse einzuführen.

Ein benutzerdefiniertes Ereignis sollte den folgenden Entwurfs Richtlinien entsprechen:

-   Das benutzerdefinierte Ereignis muss "Zustands frei" sein. Sie kann nicht mit einer bestimmten Eigenschaft oder einem bestimmten Wert verknüpft werden.
-   Das benutzerdefinierte Ereignis sollte sich nicht mit der Definition oder Rolle eines vorhandenen Ereignisses überschneiden.

### <a name="custom-ui-automation-events-and-winevents"></a>Benutzerdefinierte Benutzeroberflächenautomatisierungs-Ereignisse und WinEvents

[WinEvents](winevents-infrastructure.md) sind eine nützliche prozessübergreifende Kommunikation und ein Ereignis Mechanismus in der Microsoft Windows-Plattform. Allerdings ist das Einführen einer neuen WinEvent-ID riskant, da dies Konflikte mit anderen Anwendungen oder dem Betriebssystem verursachen kann, was dazu führt, dass das System instabil wird. Um Konflikte zu vermeiden, hat Microsoft mehrere verschiedene Kategorien von WinEvents definiert und in jeder Kategorie mindestens einen Wertebereich für die Verwendung als WinEvent-IDs definiert. Weitere Informationen finden Sie unter [Zuordnung von WinEvent-IDs](allocation-of-winevent-ids.md).

Benutzeroberflächenautomatisierungs-Ereignisse vermeiden Konflikte, indem Sie die Ereignis-ID intern im Benutzeroberflächenautomatisierungs-Framework zuordnen.

## <a name="designing-custom-control-patterns"></a>Entwerfen von benutzerdefinierten Steuerelement Mustern

Ein Steuerelement Muster ist eine Schnittstelle mit Eigenschaften, Methoden und Ereignissen, die eine diskrete Funktionalität definieren, die in einem Automation-Element verfügbar ist. Steuerelement Muster-Methoden ermöglichen es Benutzeroberflächenautomatisierungs-Clients, einen bestimmten Aspekt des Steuer Elements zu bearbeiten. Die Eigenschaften und Ereignisse des Steuerelement Musters enthalten Informationen zu einem Aspekt des Steuer Elements und stellen Informationen über den Zustand des Automatisierungs Elements bereit, das das Steuerelement Muster implementiert.

Ein benutzerdefiniertes Steuerelement Muster sollte den folgenden Entwurfs Richtlinien entsprechen:

-   Ein benutzerdefiniertes Steuerelement Muster sollte ein bestimmtes Szenario abdecken. Beispielsweise ist das [ItemContainer](uiauto-implementingitemcontainer.md) -Steuerelement Muster für das Abfragen eines enthaltenen Objekts unabhängig vom virtualisierungszustand gedacht, aber es listet die enthaltenen Objekte nicht auf oder zählt sie nicht.
-   Ein benutzerdefiniertes Steuerelement Muster sollte sich nicht mit den Funktionen vorhandener Steuerelement Muster überlappen. Beispielsweise sollten die Steuerelement Muster " [Aufruf](uiauto-implementinginvoke.md) " und " [ExpandCollapse](uiauto-implementingexpandcollapse.md) " nicht kombiniert und als neues Steuerelement Muster dargestellt werden. Verwenden Sie entweder vorhandene Steuerelement Muster erneut, oder definieren Sie eindeutige Szenarien mit neuen Steuerelement Mustern.
-   Mehrere benutzerdefinierte Steuerelement Muster können zur Unterstützung komplexer Szenarien entworfen werden. Beispielsweise arbeiten die Steuerelement Muster " [Selection](uiauto-implementingselection.md) " und " [SelectionItem](uiauto-implementingselectionitem.md) " zusammen, um allgemeine Objektauswahl Szenarios zu unterstützen.

## <a name="custom-control-types"></a>Benutzerdefinierte Steuerelement Typen

Obwohl sich dieses Thema auf das Registrieren von benutzerdefinierten Benutzeroberflächenautomatisierungs-Eigenschaften,-Ereignissen und-Steuerelement Mustern konzentriert, ist es auch möglich, neue Steuerelement Typen einzuführen. Anders als benutzerdefinierte Eigenschaften, Ereignisse und Steuerelement Muster kann ein benutzerdefinierter Steuerelement nicht Programm gesteuert zur Laufzeit registriert werden, da es sich tatsächlich lediglich um einen potenziellen Wert der ControlType-Eigenschaft der Benutzeroberflächen Automatisierung handelt. Eine benutzerdefinierte Steuerelement-ID kann jedoch definiert, veröffentlicht und zur Verwendung durch andere Clients und Anbieter verfügbar gemacht werden. Weitere Informationen zu Steuerelement Typen finden Sie unter [UI Automation Control Types Overview](uiauto-controltypesoverview.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Registrieren von benutzerdefinierten Eigenschaften, Ereignissen und Steuerelement Mustern](uiauto-regcustompropseventpatterns.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Eigenschaften](uiauto-propertiesoverview.md)
</dt> <dt>

[Übersicht über Benutzeroberflächenautomatisierungs-Ereignisse](uiauto-eventsoverview.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 