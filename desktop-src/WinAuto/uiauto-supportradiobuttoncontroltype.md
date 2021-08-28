---
title: RadioButton-Steuerelementtyp
description: Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den RadioButton-Steuerelementtyp.
ms.assetid: 6fc4a6a3-f5c0-402b-b9e7-870dfaa3370d
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung des RadioButton-Steuerelementtyps
- Benutzeroberflächenautomatisierung,RadioButton-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Struktur für den RadioButton-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Eigenschaften für den RadioButton-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Steuerelementmuster für den RadioButton-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Ereignisse für den RadioButton-Steuerelementtyp
- Strukturstrukturen, RadioButton-Steuerelementtyp
- Properties, RadioButton-Steuerelementtyp
- Steuerelementmuster, RadioButton-Steuerelementtyp
- Ereignisse, RadioButton-Steuerelementtyp
- Unterstützung für den RadioButton-Steuerelementtyp
- RadioButton-Steuerelementtyp
- Steuerelementtypen, Struktur für RadioButton-Steuerelementtyp
- Steuerelementtypen,Steuerelementmuster für RadioButton-Steuerelementtyp
- Steuerelementtypen,Unterstützung für RadioButton
- Steuerelementtypen,RadioButton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a854eec792943a6fc094796de1e3ea6849c6a5e2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480636"
---
# <a name="radiobutton-control-type"></a>RadioButton-Steuerelementtyp

Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den **RadioButton-Steuerelementtyp.**

Ein Optionsfeld besteht aus einer runden Schaltfläche und anwendungsdefiniertem Text (eine Bezeichnung), einem Symbol oder eine Bitmap, die eine Option anzeigt, die der Benutzer durch Aktivieren der Schaltfläche auswählen kann. Eine Anwendung verwendet in der Regel Optionsfelder in einem Gruppenfeld, um es dem Benutzer zu gestatten, aus einer Gruppe von verwandten, aber sich gegenseitig ausschließenden Optionen auszuwählen. Die Anwendung kann z. B. eine Gruppe von Optionsfeldern darstellen, unter denen der Benutzer eine Formateinstellung für Text auswählen kann, der im Clientbereich markiert ist. Der Benutzer kann ein linksbündiges, rechtsbündiges oder zentriertes Format auswählen, indem er das entsprechende Optionsfeld aktiviert. In der Regel kann der Benutzer jeweils nur eine Option zur Zeit aus einer Gruppe von Optionsfeldern auswählen.

> [!Note]  
> Eine weitere Steuerelementallgemeinisierung für Schaltflächen, bei denen nur eine schaltfläche in einer Gruppe ausgewählt werden kann, ist der Inhalt einer Umschaltfläche. Einige Benutzeroberflächenframeworks betrachten ein Optionsfeld als spezielle Umschaltfläche.

 

In den folgenden Abschnitten werden die erforderlichen Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **RadioButton-Steuerelementtyp** definiert. Die Benutzeroberflächenautomatisierung Anforderungen gelten für alle Schaltflächensteuerelemente, bei denen das Benutzeroberflächenframework bzw. die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Struktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Anmerkungen](#remarks)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Struktur

Die folgende Tabelle zeigt eine typische Steuerelement- und Inhaltsansicht der Benutzeroberflächenautomatisierung Struktur, die sich auf Optionsfeldsteuerelemente bezieht, und beschreibt, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Benutzeroberflächenautomatisierung-Struktur finden Sie unter [Benutzeroberflächenautomatisierung Tree Overview](uiauto-treeoverview.md).




| Steuerelementansicht | Inhaltsansicht | 
|--------------|--------------|
| <ul><li>RadioButton</li></ul> | <ul><li>RadioButton</li></ul> | 




 

Es sind keine untergeordneten Elemente in der Steuerelementansicht oder der Inhaltsansicht enthalten.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Eigenschaften aufgeführt, deren Wert oder Definition für die Steuerelemente, die den **RadioButton-Steuerelementtyp** implementieren (z. B. Schaltflächensteuerelemente), besonders relevant sind. Weitere Informationen zu Benutzeroberflächenautomatisierung Eigenschaften finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert           | Hinweise                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.      | Der Wert dieser Eigenschaft muss für alle Peerelemente in der rohen Ansicht der Benutzeroberflächenautomatisierung-Struktur eindeutig sein.                                  |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise.      | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                      |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Siehe Hinweise.      | Der klickbare Punkt muss ein Punkt sein, der das Optionsfeld auswählt, wenn darauf geklickt wird.                                                             |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **RadioButton** |                                                                                                                                               |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE            | Das Optionsfeld-Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierung-Struktur enthalten.                                                    |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE            | Das Optionsfeld-Steuerelement ist immer in der Steuerelementansicht der Benutzeroberflächenautomatisierung-Struktur enthalten.                                                    |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Siehe Hinweise.      | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                     |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL            | Optionsfeldsteuerelemente sind durch ihren Inhalt selbstbeschriftet.                                                                                     |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise.      | Lokalisierte Zeichenfolge, die dem **RadioButton-Steuerelementtyp** entspricht. Der Standardwert ist "Optionsfeld" für en-US oder Englisch (USA). |
| [**\_UIA-NamePropertyId**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.      | Der Name des Optionsfeld-Steuerelements ist der Text, der neben der Schaltfläche angezeigt wird, die den Auswahlzustand beibehält.                      |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Steuerelementmuster aufgeführt, die von allen Optionsfeldsteuerelementen unterstützt werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster/Mustereigenschaft                                               | Unterstützung/Wert | Hinweise                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)                | Erforderlich      | Alle Optionsfeldsteuerelemente müssen das [SelectionItem-Steuerelementmuster](uiauto-implementingselectionitem.md) unterstützen, damit sie selbst ausgewählt werden können.                                                                                                                                                                                                                                                             |
| [**Selectioncontainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) | Siehe Hinweise.    | Die [**SelectionContainer-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) muss immer abgeschlossen werden, damit ein Benutzeroberflächenautomatisierung Client bestimmen kann, welche anderen Optionsfelder innerhalb eines bestimmten Kontexts miteinander in Beziehung stehen. Für die Microsoft Win32-Version des Optionsfelds wird diese Eigenschaft nicht unterstützt, da es nicht möglich ist, diese Informationen aus diesem Legacyframework abzurufen. |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                              | Nie         | Das Optionsfeld kann seinen Zustand nicht durchlaufen, nachdem es festgelegt wurde. Das [](uiauto-implementingtoggle.md) Umschalten-Steuerelementmuster darf nie für ein Optionsfeld unterstützt werden.                                                                                                                                                                                                                                      |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Ereignisse aufgeführt, die von Schaltflächensteuerelementen unterstützt werden müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                     | Hinweise                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                        |                                                                                                                                |
| [**UIA \_ BoundingRectanglePropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)   |                                                                                                                                |
| [**UIA \_ IsEnabledPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                   | Wenn das Steuerelement die [**IsEnabled-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen.       |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)               | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen.     |
| [**UIA \_ \_ SelectionItem-ElementRemovedFromSelectionEventId**](uiauto-event-ids.md) | Wenn das Steuerelement das [SelectionItem-Steuerelementmuster](uiauto-implementingselectionitem.md) unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ \_ SelectionItem-ElementSelectedEventId**](uiauto-event-ids.md)                         | Wenn das Steuerelement das [SelectionItem-Steuerelementmuster](uiauto-implementingselectionitem.md) unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                    |                                                                                                                                |



 

## <a name="remarks"></a>Hinweise

Ein Optionsfeld stellt eine einzelne auswählbare Option in einer Gruppe von Peer-Optionsfeldern dar. Im Idealfall sollten Optionsfelder über ein Gruppierungselement verfügen, das die Grenzen der Peerschaltflächen verdeutlicht. Häufig wird die Grenze jedoch durch die Benutzeroberflächenelementstruktur impliziert. Beispielsweise kann ein Menü eine Reihe von aufeinanderfolgenden Optionsfeldern anstelle von Menüelementen oder eine Reihe von Optionsfeldern enthalten, die nach einer Gruppenbezeichnung, aber vor einem umsetzbaren Element wie der Schaltfläche auftreten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




