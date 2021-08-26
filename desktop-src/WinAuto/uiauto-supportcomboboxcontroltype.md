---
title: ComboBox-Steuerelementtyp
description: Dieses Thema enthält Informationen zur Unterstützung von Microsoft Benutzeroberflächenautomatisierung für den ComboBox-Steuerelementtyp.
ms.assetid: e7c64dc1-e1e3-4f99-adde-d0d63eb6c4c9
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung für ComboBox-Steuerelementtyp
- Benutzeroberflächenautomatisierung,ComboBox-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Struktur für comboBox-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Eigenschaften für den ComboBox-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Steuerelementmuster für ComboBox-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Ereignisse für den ComboBox-Steuerelementtyp
- Strukturstrukturen, ComboBox-Steuerelementtyp
- Properties, ComboBox-Steuerelementtyp
- Steuerelementmuster, ComboBox-Steuerelementtyp
- Ereignisse, ComboBox-Steuerelementtyp
- Unterstützung für den ComboBox-Steuerelementtyp
- ComboBox-Steuerelementtyp
- Steuerelementtypen, Struktur für ComboBox-Steuerelementtyp
- Steuerelementtypen,Steuerelementmuster für ComboBox-Steuerelementtyp
- Steuerelementtypen,Unterstützung für ComboBox
- Steuerelementtypen, ComboBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9d9f38dab9877aee38773e5c900ee125d2ba6a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480106"
---
# <a name="combobox-control-type"></a>ComboBox-Steuerelementtyp

Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den **ComboBox-Steuerelementtyp.**

Ein Kombinationsfeld ist ein Listenfeld, das mit einem statischen Steuerelement oder einem Bearbeitungssteuerelement kombiniert ist und das momentan ausgewählte Element im Listenfeldbereich des Kombinationsfelds anzeigt. Der Listenfeldbereich des Steuerelements wird dauerhaft oder nur dann angezeigt, wenn der Dropdownpfeil (der eine Schaltfläche ist) neben dem Steuerelement ausgewählt wurde. Wenn das Auswahlfeld ein Bearbeitungssteuerelement ist, kann der Benutzer Informationen eingeben, die in der Liste nicht vorhanden sind. Andernfalls kann er nur Elemente in der Liste auswählen.

In den folgenden Abschnitten werden die erforderlichen Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **ComboBox-Steuerelementtyp** definiert. Die Benutzeroberflächenautomatisierung Anforderungen gelten für alle Kombinationsfeldsteuerelemente, bei denen das Benutzeroberflächenframework bzw. die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Struktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Struktur

Die folgende Tabelle zeigt eine typische Steuerelement- und Inhaltsansicht der Benutzeroberflächenautomatisierung-Struktur, die sich auf Kombinationsfeldsteuerelemente bezieht, und beschreibt, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Benutzeroberflächenautomatisierung-Struktur finden Sie unter [Benutzeroberflächenautomatisierung Tree Overview](uiauto-treeoverview.md).




| Steuerelementansicht | Inhaltsansicht | 
|--------------|--------------|
| <ul><li>Kombinationsfeld<ul><li>Bearbeitung (0 oder 1)</li><li>Liste (0 oder 1)</li><li>Listenelement (untergeordnetes Element von Liste; 0 bis viele)</li><li>Schaltfläche (1)</li></ul></li></ul> | <ul><li>Kombinationsfeld<ul><li>Listenelement (0 bis viele)</li></ul></li></ul> | 




 

Das Bearbeitungssteuerelement in der Steuerelementansicht des Kombinationsfelds ist nur erforderlich, wenn das Kombinationsfeld bearbeitet werden kann, um eingaben zu können, wie es im Fall des Kombinationsfelds im Dialogfeld **Ausführen** der Fall ist.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Eigenschaften aufgeführt, deren Wert oder Definition für den **ComboBox-Steuerelementtyp** besonders relevant ist. Weitere Informationen zu Benutzeroberflächenautomatisierung Eigenschaften finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert      | Hinweise                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise. | Der Wert dieser Eigenschaft muss für alle Peerelemente in der rohen Ansicht der Benutzeroberflächenautomatisierung-Struktur eindeutig sein.                                                                                                                                                                                                     |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise. | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                                                                                                                         |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Siehe Hinweise. | Unterstützt, wenn es ein umschließendes Rechteck gibt. Wenn nicht jeder Punkt innerhalb des umschließenden Rechtecks klickbar ist und das Element spezielle Treffertests durchführt, überschreibt und stellt einen klickbaren Punkt bereit.                                                                                                             |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | Kombinationsfeld   |                                                                                                                                                                                                                                                                                                                  |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Siehe Hinweise. | Im Hilfetext für Kombinationsfeld-Steuerelemente sollte erläutert werden, warum der Benutzer aufgefordert wird, eine Option aus dem Kombinationsfeld auszuwählen. Der Text ist mit den in einer QuickInfo angezeigten Informationen vergleichbar. Beispiel: „Wählen Sie ein Element aus, um die Anzeigeauflösung des Bildschirms festzulegen.“                                                |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Kombinationsfeld-Steuerelemente sind immer in der Inhaltsansicht der Benutzeroberflächenautomatisierung-Struktur enthalten.                                                                                                                                                                                                                            |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Kombinationsfeld-Steuerelemente sind immer in der Steuerelementansicht der Benutzeroberflächenautomatisierung-Struktur enthalten.                                                                                                                                                                                                                            |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | TRUE       | Kombinationsfeld-Steuerelemente können den Tastaturfokus erhalten. Wenn jedoch ein Benutzeroberflächenautomatisierung Client den Fokus auf ein Kombinationsfeld festlegt, kann jedes Element in der Unterstruktur des Kombinationsfelds den Fokus erhalten.                                                                                                                                          |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Siehe Hinweise. | Ein Kombinationsfeld-Steuerelement hat normalerweise eine statische Textbezeichnung, auf die diese Eigenschaft verweist.                                                                                                                                                                                                                             |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise. | Lokalisierte Zeichenfolge, die dem **ComboBox-Steuerelementtyp** entspricht. Der Standardwert ist "Kombinationsfeld" für en-US oder Englisch (USA).                                                                                                                                                                          |
| [**\_UIA-NamePropertyId**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise. | Der Name des Kombinationsfeld-Steuerelements wird in der Regel aus einer statischen Textbezeichnung generiert. Wenn keine statische Textbezeichnung vorhanden ist, müssen Sie einen Wert für die **Name-Eigenschaft** zuweisen. Die **Name-Eigenschaft** sollte nie den aktuellen Inhalt des Kombinationsfelds enthalten oder sich ändern, wenn sich der Inhalt des Kombinationsfelds ändert. |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Steuerelementmuster aufgeführt, die von allen Kombinationsfeldsteuerelementen unterstützt werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster                                                   | Support  | Notizen                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Erforderlich | Das [ExpandCollapse-Steuerelementmuster](uiauto-implementingexpandcollapse.md) muss unterstützt werden, da ein Kombinationsfeld-Steuerelement immer eine Dropdownschaltfläche enthalten muss.                                                                                                                                                                                |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)           | Depends (Abhängig)  | Zeigt die aktuelle Auswahl im Kombinationsfeld an. Die Unterstützung für [das Auswahl-Steuerelementmuster](uiauto-implementingselection.md) wird an das Listenfeld unterhalb des Kombinationsfelds delegiert, ist aber möglicherweise nicht immer möglich.                                                                                                                               |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | Depends (Abhängig)  | Wenn das Kombinationsfeld beliebige Textwerte [](uiauto-implementingvalue.md) verwenden kann, muss das Value-Steuerelementmuster unterstützt werden. Mit diesem Muster kann der Zeichenfolgeninhalt des Kombinationsfelds programmgesteuert festgelegt werden. Wenn das Value-Steuerelementmuster nicht unterstützt wird, muss der Benutzer aus den Listenelementen in der Unterstruktur des Kombinationsfelds auswählen. |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                 | Nie    | Das [Bildlauf-Steuerelementmuster](uiauto-implementingscroll.md) wird nie direkt in einem Kombinationsfeld unterstützt. Dies wird unterstützt, wenn ein in einem Kombinationsfeld enthaltenes Listenfeld scrollen kann und nur, wenn das Listenfeld auf dem Bildschirm sichtbar ist.                                                                                                              |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung, die Kombinationsfeldsteuerelemente unterstützen müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                                                | Hinweise                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [**UIA \_ BoundingRectanglePropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                              |                                                                                                                            |
| [**UIA \_ IsEnabledPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                                              | Wenn das Steuerelement die [**IsEnabled-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen.   |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                                          | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                            |
| [**UIA \_ ExpandCollapseExpandCollapseStatePropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md) |                                                                                                                            |
| [**UIA \_ Durch die ValueValuePropertyId-Eigenschaft**](uiauto-control-pattern-propids.md) geändertes Ereignis.                                               | Wenn das Steuerelement das [Value-Steuerelementmuster](uiauto-implementingvalue.md) unterstützt, muss es dieses Ereignis unterstützen.             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




