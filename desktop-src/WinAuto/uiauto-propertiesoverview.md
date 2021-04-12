---
title: Übersicht über die Benutzeroberflächenautomatisierungs-Eigenschaften
description: Microsoft UI Automation-Anbieter machen Eigenschaften für Benutzeroberflächenautomatisierungs-Elemente verfügbar. Eigenschaften ermöglichen Client Anwendungen das Abrufen von Informationen zu Steuerelementen.
ms.assetid: 35f017cb-f50a-4680-9f01-5079aa59da73
keywords:
- Benutzeroberflächenautomatisierungs, Übersicht über Eigenschaften
- Benutzeroberflächen Automatisierung, Eigenschaften und Ereignisse
- UI-Automatisierung, Ereignisse und Eigenschaften
- Eigenschaften, Informationen zu
- Eigenschaften, Bezeichner
- Eigenschaften, Werte
- Eigenschaften, Ereignisse
- Ereignisse, Eigenschaften
- Eigenschaften, dynamisch
- Dynamische Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0f4e5e1b29ae516059a531b17d50d0631282f82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206192"
---
# <a name="ui-automation-properties-overview"></a>Übersicht über die Benutzeroberflächenautomatisierungs-Eigenschaften

Microsoft UI Automation-Anbieter machen Eigenschaften für Benutzeroberflächenautomatisierungs-Elemente verfügbar. Eigenschaften ermöglichen Client Anwendungen das Abrufen von Informationen zu Steuerelementen.

Die Benutzeroberflächen Automatisierung bietet zwei verschiedene Arten von Eigenschaften: *Automatisierungs Element Eigenschaften* und *Steuerelement Muster* Eigenschaften. Die Automatisierungs Element Eigenschaften bestehen aus einem gemeinsamen Satz von Eigenschaften, z. b. "Name", "AcceleratorKey" und "ClassName", die unabhängig vom Steuer Elementtyp von allen Benutzeroberflächenautomatisierungs-Elementen verfügbar gemacht werden. Die meisten Automatisierungs Element Eigenschaften sind statische Werte.

Steuerelement Muster Eigenschaften sind solche, die von einem Steuerelement verfügbar gemacht werden, das ein bestimmtes Steuerelement Muster unterstützt. Jedes Steuerelement Muster verfügt über einen entsprechenden Satz von Steuerelement Mustern-Eigenschaften, die das Steuerelement verfügbar machen muss. Ein Steuerelement, das das [Raster](uiauto-implementinggrid.md) -Steuerelement Muster unterstützt, macht z. b. die Eigenschaften ColumnCount und RowCount verfügbar. Die meisten Steuerelement Muster Eigenschaften sind dynamische Werte.

Dieses Thema enthält folgende Abschnitte:

-   [Eigenschaftsbezeichner](#property-identifiers)
-   [Eigenschaftswerte](#property-values)
-   [Eigenschaften und Ereignisse](#properties-and-events)
-   [Zugehörige Themen](#related-topics)

## <a name="property-identifiers"></a>Eigenschaftsbezeichner

Jede Eigenschaft wird durch einen numerischen **PropertyId** -Wert identifiziert, der als *Eigenschaften Bezeichner* (ID) bezeichnet wird. Anbieter und Clients verwenden die numerischen IDs in Methoden aufrufen wie [**irawelementprovideradviseevents:: adviseeventadded**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventadded) und [**iuiautomationelement:: GetCachedPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue) , um Eigenschafts Anforderungen zu identifizieren. Eine ausführliche Beschreibung der einzelnen Eigenschaften Bezeichner für die Benutzeroberflächen Automatisierung, einschließlich des Datentyps und des Standardwerts der einzelnen Eigenschaften, finden Sie unter [Eigenschaften](uiauto-entry-propids.md)Bezeichner.

## <a name="property-values"></a>Eigenschaftswerte

Alle Eigenschaften sind schreibgeschützt, auch wenn einige geändert werden können, indem Sie Methoden verwenden, die auf das Steuerelement reagieren, wie z. b. [**IDockProvider:: SetDockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) (Provider) oder [**iuiautomationdockpattern:: SetDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-setdockposition) (Client).

Weitere Informationen zum Abrufen von Eigenschafts Werten finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).

## <a name="properties-and-events"></a>Eigenschaften und Ereignisse

Die Eigenschaften in der Benutzeroberflächen Automatisierung sind eng mit den Eigenschaften für *geänderte Ereignisse* verknüpft. Bei dynamischen Eigenschaften muss eine Client Anwendung wissen, dass sich ein Eigenschafts Wert geändert hat, damit er den Informations Cache aktualisieren oder auf andere Weise auf die neuen Informationen reagieren kann. Clients können sich registrieren, um auf Eigenschaften geänderte Ereignisse für jede Eigenschaft zu lauschen.

Anbieter rufen Ereignisse auf, wenn etwas in der Benutzeroberfläche geändert wird. Wenn beispielsweise ein Kontrollkästchen aktiviert oder deaktiviert ist, wird ein Eigenschaften Änderungs Ereignis von der Anbieter Implementierung des [Toggle](uiauto-implementingtoggle.md) -Steuerelement Musters ausgelöst. Anbieter können abhängig davon, ob Clients Ereignissen oder bestimmten Ereignissen lauschen, selektiv Ereignisse auslösen.

Es werden nicht für alle Eigenschaftenänderung Ereignisse ausgelöst. Dies ist vollständig von der Implementierung des Benutzeroberflächenautomatisierungs-Anbieters für das Element abhängig. Beispielsweise wird durch die Standard Proxy Anbieter für Listenfelder nicht ein Eigenschaften Änderungs Ereignis, wenn die Auswahl Eigenschaft geändert wird. In diesem Fall muss die Anwendung auf das Ereignis lauschen, das ausgelöst wird, wenn die Auswahl geändert wird ([**UIA \_ SelectionItem \_ elementselectedebug-**](uiauto-event-ids.md)ID).

Clients lauschen auf Ereignisse, indem Sie Sie abonnieren, wie unter Abonnieren von Benutzeroberflächenautomatisierungs- [Ereignissen](uiauto-eventsforclients.md)beschrieben. Insbesondere bei Eigenschaften geänderten Ereignissen müssen Clients [**iuiautomationpropertychangedeventhandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) implementieren und die Schnittstelle an [**iuiautomation:: addpropertychangedeventhandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) oder [**iuiautomation:: addpropertychangedeventhandlernativearray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray)übergeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[**GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)
</dt> <dt>

[**Getcurrentpropertyvalueex**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex)
</dt> <dt>

[**GetCachedPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue)
</dt> <dt>

[**Getcachedpropertyvalueex**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalueex)
</dt> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über Benutzeroberflächenautomatisierungs-Ereignisse](uiauto-eventsoverview.md)
</dt> </dl>

 

 




