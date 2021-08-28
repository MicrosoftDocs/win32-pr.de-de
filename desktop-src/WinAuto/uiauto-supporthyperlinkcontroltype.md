---
title: Link-Steuerelementtyp
description: Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den Steuerelementtyp "Hyperlink".
ms.assetid: 6dd16ae6-eff0-4913-8916-5092aec34f1f
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung für den Steuerelementtyp "Hyperlink"
- Benutzeroberflächenautomatisierung,Steuerelementtyp "Hyperlink"
- Benutzeroberflächenautomatisierung,Struktur für linken Steuerelementtyp
- Benutzeroberflächenautomatisierung,Eigenschaften für den Steuerelementtyp "Hyperlink"
- Benutzeroberflächenautomatisierung,Steuerelementmuster für den Steuerelementtyp "Hyperlink"
- Benutzeroberflächenautomatisierung,Events für den Steuerelementtyp "Hyperlink"
- Strukturstrukturen,Link-Steuerelementtyp
- Properties,Link-Steuerelementtyp
- Steuerelementmuster,Steuerelementtyp "Hyperlink"
- events,Link-Steuerelementtyp
- Unterstützung für den Steuerelementtyp "Hyperlink"
- HyperLink-Steuerelementtyp
- Steuerelementtypen,Struktur für Hyperlink-Steuerelementtyp
- Steuerelementtypen,Steuerelementmuster für Den Link-Steuerelementtyp
- Steuerelementtypen,Unterstützung für Hyperlink
- Steuerelementtypen, Hyperlink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52735983429a60061a548bf4cce71b7b128f4b6e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466957"
---
# <a name="hyperlink-control-type"></a>Link-Steuerelementtyp

Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den **Steuerelementtyp "Hyperlink".**

Linksteuerelemente erstellen Links, mit denen Benutzer innerhalb derselben Seite oder von einer Seite zur anderen navigieren können.

In den folgenden Abschnitten werden die Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **Steuerelementtyp Hyperlink** definiert. Die Benutzeroberflächenautomatisierung gelten für alle Linksteuerelemente, bei denen das Benutzeroberflächenframework/die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Strukturstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Anmerkungen](#remarks)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Strukturstruktur

Die folgende Tabelle zeigt ein typisches Steuerelement und eine Inhaltsansicht der Benutzeroberflächenautomatisierung struktur, die sich auf Linksteuerelemente bezieht, und beschreibt, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Struktur Benutzeroberflächenautomatisierung Struktur finden Sie unter [Benutzeroberflächenautomatisierung Strukturübersicht.](uiauto-treeoverview.md)




| Steuerelementansicht | Inhaltsansicht | 
|--------------|--------------|
| <ul><li>Hyperlink</li></ul> | <ul><li>Hyperlink</li></ul> | 




 

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung, deren Wert oder Definition für die Linksteuerelemente besonders relevant ist. Weitere Informationen zu Eigenschaften Benutzeroberflächenautomatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements.](uiauto-propertiesforclients.md)



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert         | Hinweise                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.    | Der Wert dieser Eigenschaft muss für alle Steuerelemente in einer Anwendung eindeutig sein.                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise.    | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                 |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Siehe Hinweise.    | Der klickbare Punkt des Linksteuerfelds muss ein Punkt sein, der den Link startet, wenn mit einem Mauszeiger geklickt wird.                     |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Link** |                                                                                                                                          |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE          | Das Link-Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierung enthalten.                                                  |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE          | Das Linksteuer steuerelement ist immer in der Steuerelementansicht der Benutzeroberflächenautomatisierung enthalten.                                                  |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Siehe Hinweise.    | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Siehe Hinweise.    | Wenn es eine statische Textbezeichnung gibt, muss diese Eigenschaft einen Verweis auf dieses Steuerelement verfügbar machen.                                                  |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise.    | Lokalisierte Zeichenfolge, die dem **Steuerelementtyp Hyperlink** entspricht. Der Standardwert ist "hyperlink" für en-US oder English (USA). |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.    | Der Name des Linksteuerfelds ist der Text, der unterstrichen auf dem Bildschirm angezeigt wird.                                                  |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung- und Steuerelementmuster aufgeführt, die von Linksteuerelementen unterstützt werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster/Mustereigenschaft                  | Unterstützung/Wert                | Hinweise                                                                                                                                                                                                                                                  |
|---------------------------------------------------|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) | Erforderlich                     | Alle Linksteuerelemente müssen das [Invoke-Steuerelementmuster](uiauto-implementinginvoke.md) unterstützen.                                                                                                                                                       |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)   | Depends (Abhängig)                      | Linksteuerelemente sollten das [Value-Steuerelementmuster](uiauto-implementingvalue.md) unterstützen, wenn der Link Informationen enthält, die für den Benutzer nutzbar und aussagekräftig sind.                                                                              |
| [**Wert**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)      | Beispiel: „https://www..“. | Eine URL für eine Internet- oder Intranetadresse ist ein Beispiel für einen Link, der informationen enthält, die für den Benutzer aussagekräftig sind. Ein programmgesteuerter Link ist jedoch nur für eine Anwendung sinnvoll und wird für die **Value-Eigenschaft nicht** empfohlen. |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung aufgeführt, die von Linksteuerelementen unterstützt werden müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                   | Hinweise                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ BoundingRectanglePropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)                                                     |                                                                                                                            |
| [**UIA \_ IsEnabledPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                 | Wenn das Steuerelement die [**IsEnabled-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen.   |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)             | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="remarks"></a>Hinweise

Der Steuerelementtyp Hyperlink sollte nur auf ein Objekt angewendet werden, das beim Klicken die Navigation verursacht. sie sollte nicht auf den Container des Links angewendet werden. Beispielsweise sollten nur die klickbaren "Hotspots" in einer Imagemap den **Steuerelementtyp Hyperlink** haben. Dasselbe gilt für Links in einem Textfeld oder Dokumentcontainer. In diesem Fall sollte nur der Linktext oder das Bild den **Steuerelementtyp Hyperlink** und nicht den Container haben.

Das [Text-Steuerelementmuster](uiauto-implementingtextandtextrange.md) eignet sich ideal für die Unterstützung eingebetteter Links in Text- oder Dokumentelementen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




