---
title: Übersicht über die Benutzeroberflächenautomatisierungs-Eigenschaften
description: Microsoft Benutzeroberflächenautomatisierung-Anbieter machen Eigenschaften für Benutzeroberflächenautomatisierung verfügbar. Eigenschaften ermöglichen Clientanwendungen das Abrufen von Informationen zu Steuerelementen.
ms.assetid: 35f017cb-f50a-4680-9f01-5079aa59da73
keywords:
- Benutzeroberflächenautomatisierung,Eigenschaftenübersicht
- Benutzeroberflächenautomatisierung, Eigenschaften und Ereignisse
- Benutzeroberflächenautomatisierung, Ereignisse und Eigenschaften
- Properties,about
- Eigenschaften,Bezeichner
- Eigenschaften, Werte
- Eigenschaften,Ereignisse
- Ereignisse,Eigenschaften
- Eigenschaften,dynamisch
- Dynamische Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58267fae50fe71c320b334c35b8da7831657e00bdd1b222db596addd40f3afef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745030"
---
# <a name="ui-automation-properties-overview"></a>Übersicht über die Benutzeroberflächenautomatisierungs-Eigenschaften

Microsoft Benutzeroberflächenautomatisierung-Anbieter machen Eigenschaften für Benutzeroberflächenautomatisierung verfügbar. Eigenschaften ermöglichen Clientanwendungen das Abrufen von Informationen zu Steuerelementen.

Benutzeroberflächenautomatisierung macht zwei verschiedene Arten von Eigenschaften verfügbar: *Automatisierungselementeigenschaften,* und *das Steuerelementmuster gibt an.* Die Automatisierungselementeigenschaften bestehen aus einem allgemeinen Satz von Eigenschaften, z. B. Name, AcceleratorKey und ClassName, die von allen Benutzeroberflächenautomatisierung-Elementen verfügbar gemacht werden, unabhängig vom Steuerelementtyp. Die meisten Automatisierungselementeigenschaften sind statische Werte.

Steuerelementmustereigenschaften sind Eigenschaften, die von einem Steuerelement verfügbar gemacht werden, das ein bestimmtes Steuerelementmuster unterstützt. Jedes Steuerelementmuster verfügt über einen entsprechenden Satz von Steuerelementmustereigenschaften, die das Steuerelement verfügbar machen muss. Beispielsweise macht ein Steuerelement, [](uiauto-implementinggrid.md) das das Grid-Steuerelementmuster unterstützt, die Eigenschaften ColumnCount und RowCount verfügbar. Die meisten Steuerelementmustereigenschaften sind dynamische Werte.

Dieses Thema enthält folgende Abschnitte:

-   [Eigenschaftsbezeichner](#property-identifiers)
-   [Eigenschaftswerte](#property-values)
-   [Eigenschaften und Ereignisse](#properties-and-events)
-   [Zugehörige Themen](#related-topics)

## <a name="property-identifiers"></a>Eigenschaftsbezeichner

Jede Eigenschaft wird durch einen **numerischen PROPERTYID-Wert** identifiziert, der als *Eigenschaftenbezeichner (ID)* bezeichnet wird. Anbieter und Clients verwenden die numerischen IDs in Methodenaufrufen wie [**IRawElementProviderAdviseEvents::AdviseEventAdded**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventadded) und [**IUIAutomationElement::GetCachedPropertyValue,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue) um Eigenschaftenanforderungen zu identifizieren. Eine ausführliche Beschreibung der einzelnen Eigenschaftenbezeichner Benutzeroberflächenautomatisierung, einschließlich des Datentyps und Standardwerts der einzelnen Eigenschaften, finden Sie unter [Eigenschaftenbezeichner](uiauto-entry-propids.md).

## <a name="property-values"></a>Eigenschaftswerte

Alle Eigenschaften sind schreibgeschützt, obwohl einige mithilfe von Methoden geändert werden können, die auf das Steuerelement angewendet werden, z. B. [**IDockProvider::SetDockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) (Anbieter) oder [**IUIAutomationDockPattern::SetDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-setdockposition) (Client).

Informationen zum Abrufen von Eigenschaftswerten finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements](uiauto-propertiesforclients.md).

## <a name="properties-and-events"></a>Eigenschaften und Ereignisse

Eng mit den Eigenschaften in Benutzeroberflächenautomatisierung ist das Konzept von Durch Eigenschaften *geänderten Ereignissen verknüpft.* Für dynamische Eigenschaften benötigt eine Clientanwendung eine Möglichkeit zu wissen, dass sich ein Eigenschaftswert geändert hat, damit sie ihren Informationscache aktualisieren oder auf andere Weise auf die neuen Informationen reagieren kann. Clients können sich registrieren, um auf Durch Eigenschaften geänderte Ereignisse für jede Eigenschaft zu lauschen.

Anbieter geben Ereignisse aus, wenn sich etwas in der Benutzeroberfläche ändert. Wenn beispielsweise ein Kontrollkästchen aktiviert oder aktiviert ist, wird von der Anbieterimplementierung des [Steuerelementmusters Umschalten](uiauto-implementingtoggle.md) ein durch eine Eigenschaft geändertes Ereignis ausgelöst. Anbieter können abhängig davon, ob Clients Ereignissen oder bestimmten Ereignissen lauschen, selektiv Ereignisse auslösen.

Es werden nicht für alle Eigenschaftenänderung Ereignisse ausgelöst. Dies ist vollständig von der Implementierung des Benutzeroberflächenautomatisierungs-Anbieters für das Element abhängig. Die Standardproxyanbieter für Listenfelder geben z. B. kein Durch eine Eigenschaft geändertes Ereignis aus, wenn sich die Selection-Eigenschaft ändert. In diesem Fall muss die Anwendung auf das Ereignis lauschen, das ausgelöst wird, wenn sich die Auswahl ändert ([**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)).

Clients lauschen auf Ereignisse, indem sie sie abonnieren, wie unter Abonnieren von Ereignissen [Benutzeroberflächenautomatisierung beschrieben.](uiauto-eventsforclients.md) Insbesondere bei Ereignissen mit Geänderter Eigenschaft müssen Clients [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) implementieren und die Schnittstelle [**an IUIAutomation::AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) oder [**IUIAutomation::AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray)übergeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[**Getcurrentpropertyvalue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)
</dt> <dt>

[**GetCurrentPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex)
</dt> <dt>

[**Getcachedpropertyvalue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue)
</dt> <dt>

[**GetCachedPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalueex)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über Benutzeroberflächenautomatisierungs-Ereignisse](uiauto-eventsoverview.md)
</dt> </dl>

 

 




