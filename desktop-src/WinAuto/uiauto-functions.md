---
title: Funktionen für Anbieter
description: In diesem Abschnitt werden die Funktionen für Benutzeroberflächenautomatisierungs-Anbieter für Microsoft Win32-Anwendungen beschrieben.
ms.assetid: 76012ec7-0114-4b6b-a35e-5cfde5b90230
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea0542c3d0b313e1bed8ec040924349e37a29fea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337433"
---
# <a name="functions-for-providers"></a>Funktionen für Anbieter

In diesem Abschnitt werden die Funktionen für Benutzeroberflächenautomatisierungs-Anbieter für Microsoft Win32-Anwendungen beschrieben.

## <a name="in-this-section"></a>In diesem Abschnitt



| Funktion                                                                                                 | BESCHREIBUNG                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Uiaclientsarelistening**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaclientsarelistening)<br/>                       | Ruft einen Wert ab, der angibt, ob eine Client Anwendung Microsoft UI Automation-Ereignisse abonniert hat.<br/>                                             |
| [**Uiadisconnectallproviders**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiadisconnectallproviders)<br/>                         | Gibt alle Benutzeroberflächenautomatisierungs-Ressourcen frei, die von allen dem aufrufenden Prozess zugeordneten Anbietern aufbewahrt werden. <br/>                                               |
| [**Uiadisconnectprovider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiadisconnectprovider)<br/>                                 | Gibt alle Verweise frei, die ein bestimmter Anbieter für Benutzeroberflächenautomatisierungs-Objekte enthält.<br/>                                                                      |
| [**Uiagetreservedmixedattributevalue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue)<br/> | Ruft einen reservierten Wert ab, der angibt, dass sich der Wert eines Text Attributs für die Benutzeroberflächen Automatisierung innerhalb eines Text Bereichs ändert.<br/>                                      |
| [**Uiagetreservednotsupportedvalue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservednotsupportedvalue)<br/>     | Ruft einen reservierten Wert ab, der angibt, dass eine Benutzeroberflächenautomatisierungs-Eigenschaft oder ein Text Attribut nicht unterstützt wird.<br/>                                               |
| [**Uiahostproviderfromhwnd**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahostproviderfromhwnd)<br/>                     | Ruft den Host Anbieter für ein Fenster ab.<br/>                                                                                                                    |
| [**Uiaiaccessiblefromprovider**](/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaiaccessiblefromprovider)<br/>                   | Ruft eine [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Implementierung ab, die Microsoft Active Accessibility-Daten im Auftrag eines Benutzeroberflächenautomatisierungs-Anbieters bereitstellt.<br/> |
| [**Uiaproviderfornonclient**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaproviderfornonclient)<br/>                     | Ruft den Anbieter für den gesamten nicht-Client Bereich eines Fensters oder für ein Steuerelement im nicht-Client Bereich eines Fensters ab.<br/>                                      |
| [**Uiaproviderfromiaccessible**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaproviderfromiaccessible)<br/>               | Erstellt einen Benutzeroberflächenautomatisierungs-Anbieter, der auf dem angegebenen Microsoft Active Accessibility-Objekt basiert.<br/>                                                          |
| [**Uiaraieinasynccontentloadedevent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseasynccontentloadedevent)<br/>     | Wird von einem Anbieter aufgerufen, um den Benutzeroberflächenautomatisierungs-Kern zu benachrichtigen, dass Inhalt asynchron geladen wird.<br/>                                                      |
| [**Uiaraiserautomationevent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationevent)<br/>                     | Benachrichtigt Listener über ein Ereignis.<br/>                                                                                                                         |
| [**Uiaraiminautomationpropertychangede Vent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationpropertychangedevent)<br/>    | Wird von Anbietern aufgerufen, um den Benutzeroberflächenautomatisierungs-Kern zu benachrichtigen, dass eine Element Eigenschaft geändert wurde.<br/>                                                              |
| [**Uiaraisetter changesevent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisechangesevent)<br/>                           | Wird von Anbietern aufgerufen, um den Benutzeroberflächenautomatisierungs-Kern zu benachrichtigen, dass eine Änderung aufgetreten ist.<br/>                                                                        |
| [**Uiaraisenotificationevent**](https://www.bing.com/search?q=**UiaRaiseNotificationEvent**)<br/>             | Wird von Anbietern aufgerufen, um ein Benachrichtigungs Ereignis zu initiieren.<br/>                                                                                                   |
| [**Uiaraiminstructurechangede Vent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisestructurechangedevent)<br/>         | Wird von einem Anbieter aufgerufen, um den Benutzeroberflächenautomatisierungs-Kern zu benachrichtigen, dass die Struktur geändert wurde.<br/>                                                              |
| [**Uiaraiabtextedittextchangeabvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisetextedittextchangedevent)<br/>   | Wird von einem Anbieter aufgerufen, um den Benutzeroberflächenautomatisierungs-Kern zu benachrichtigen, dass ein Text Steuerelement Programm gesteuert Text geändert hat.<br/>                                            |
| [**Uiareturnrawelementprovider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider)<br/>             | Ruft eine Schnittstelle zum Benutzeroberflächenautomatisierungs-Anbieter für ein Fenster ab.<br/>                                                                                           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzeroberflächen-Automatisierungsanbieter](uiauto-entry-uiautoprovidersforwin32apps.md)
</dt> </dl>

 

