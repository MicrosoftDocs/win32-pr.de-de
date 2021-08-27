---
title: AppBar-Steuerelementtyp
description: Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den AppBar-Steuerelementtyp.
ms.assetid: B56F4E7A-934F-8516-9B1B-B23B80D54273
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung für den AppBar-Steuerelementtyp
- Benutzeroberflächenautomatisierung,AppBar-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Steuerelementmuster für den AppBar-Steuerelementtyp
- Steuerelementmuster, AppBar-Steuerelementtyp
- Unterstützung für den AppBar-Steuerelementtyp
- AppBar-Steuerelementtyp
- Steuerelementtypen, AppBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fc8cf562b125267e9b35239e8490f11ed6ae830
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472886"
---
# <a name="appbar-control-type"></a>AppBar-Steuerelementtyp

Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den **AppBar-Steuerelementtyp.**

Eine App-Leiste ist ein Benutzeroberflächenelement, das dem Benutzer Navigation, Befehle und Tools präsentiert. Für Windows Store Apps können App-Balken für Apps angezeigt werden, indem Sie Windows+ Z drücken.

In den folgenden Abschnitten werden die Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **AppBar-Steuerelementtyp** definiert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Strukturstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Ereignisse](#required-events)
-   [Relevante Ereignisse](#relevant-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Strukturstruktur

Die folgende Tabelle zeigt ein typisches Steuerelement und eine Inhaltsansicht der Benutzeroberflächenautomatisierung-Struktur, die sich auf **AppBar-Steuerelemente** bezieht, und beschreibt, was in jeder Ansicht enthalten sein kann. **Die** Schaltfläche ist das gängigste Element in **einer AppBar,** aber auch andere Steuerelemente, die Aktionen für eine App aufrufen, sind möglich. Eine **AppBar kann** auch 0 oder mehr Trennzeichen (Trennzeichen-Steuerelementtyp) enthalten, die in der Steuerelementansicht als zwischen den anderen Steuerelementen platziert angezeigt werden. Weitere Informationen zur Struktur Benutzeroberflächenautomatisierung Struktur finden Sie unter [Benutzeroberflächenautomatisierung Strukturübersicht.](uiauto-treeoverview.md)




| Steuerelementansicht | Inhaltsansicht | 
|--------------|--------------|
| <ul><li>AppBar<ul><li>Schaltfläche (0 oder viele)</li><li>Andere Steuerelemente (0 oder viele)</li></ul></li></ul> | <ul><li>Nicht zutreffend<ul><li>Schaltfläche (0 oder viele)</li><li>Andere Steuerelemente (0 oder viele)</li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung aufgeführt, deren Wert oder Definition für die Steuerelemente, die den **AppBar-Steuerelementtyp** implementieren, besonders relevant ist. Weitere Informationen zu Eigenschaften Benutzeroberflächenautomatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements.](uiauto-propertiesforclients.md)



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert      | Hinweise                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise. | Der Wert dieser Eigenschaft muss für alle Peerelemente in der rohen Ansicht der Benutzeroberflächenautomatisierung sein.                                                                                                                |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise. | Der von dieser Eigenschaft verfügbar gemachte Wert muss sämtliche darin enthaltenen Steuerelemente umfassen.                                                                                                                                    |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **AppBar** |                                                                                                                                                                                                                             |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE      | Ein App-Leisten-Steuerelement ist nicht in der Inhaltsansicht der Benutzeroberflächenautomatisierung enthalten.                                                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Ein App-Leisten-Steuerelement ist immer in der Steuerelementansicht der Benutzeroberflächenautomatisierung enthalten.                                                                                                                                        |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Siehe Hinweise  | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen. Steuerelemente in der App-Leiste können in der Regel den Tastaturfokus haben.                                                                                    |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | Siehe Hinweise. | Der Wert dieser Eigenschaft ist hängt davon ab, ob das Steuerelement auf dem Bildschirm angezeigt werden kann.                                                                                                                                        |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Null       | App-Leistensteuerelemente verfügen in der Regel nicht über eine Bezeichnung.                                                                                                                                                                               |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise. | Lokalisierte Zeichenfolge, die dem **AppBar-Steuerelementtyp** entspricht. Der Standardwert ist "App-Leiste" für en-US oder Englisch (USA).                                                                                         |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise. | Das App-Leisten-Steuerelement benötigt keinen Namen, es sei denn, eine Anwendung verfügt über mehr als eine App-Leiste. Wenn eine Anwendung mehrere App-Leisten auflistet, verwenden Sie diese Eigenschaft, um verschiedene Namen verfügbar zu machen, z. B. "Top" oder "Bottom". |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung aufgeführt, die von App-Balkensteuerelementen unterstützt werden müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                   | Hinweise                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ BoundingRectanglePropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**UIA \_ IsEnabledPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                 | Wenn das Steuerelement die [**IsEnabled-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen.   |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)             | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="relevant-events"></a>Relevante Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung aufgeführt, die besonders für die Steuerelemente relevant sind, die den **AppBar-Steuerelementtyp** implementieren, aber nicht unbedingt erforderlich sind.



| Benutzeroberflächenautomatisierung-Ereignis                                                                                 | Hinweise                                                                              |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**\_UIA-MenüClosedEventId**](uiauto-event-ids.md)                            | Plattformimplementierungen können dieses Ereignis beim Schließen des App-Leisten-Steuerelements ausleiten. |
| [**\_UIA-MenüOpenedEventId**](uiauto-event-ids.md)                            | Plattformimplementierungen können dieses Ereignis beim Öffnen des App-Leisten-Steuerelements ausleiten. |
| [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) | Ereignishandler mit Geänderter Eigenschaft.                                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> <dt>

**Referenz**
</dt> <dt>

[**AppBar-XAML-Steuerelement**](/uwp/api/Windows.UI.Xaml.Controls.AppBar)
</dt> <dt>

[**WinJS.UI.AppBar-Objekt**](/previous-versions/windows/apps/br229670(v=win.10))
</dt> </dl>

 

 
