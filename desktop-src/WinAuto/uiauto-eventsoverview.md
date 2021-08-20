---
title: Übersicht über Benutzeroberflächenautomatisierungs-Ereignisse
description: Die Microsoft Benutzeroberflächenautomatisierung-Ereignisbenachrichtigung ist ein wichtiges Feature für Hilfstechnologien wie Sprachausgaben und Bildschirmlupe.
ms.assetid: 0ded64ba-188e-427e-897f-4381237ace75
keywords:
- übersicht über Benutzeroberflächenautomatisierung,Ereignisse
- Benutzeroberflächenautomatisierung, Ereigniskategorien
- Benutzeroberflächenautomatisierung, Ereignisbenachrichtigungen
- Ereignisbenachrichtigungen
- Ereignisse, Kategorien
- Ereignisse, Ereignisbenachrichtigungen
- Eigenschaftenänderungsereignisse
- Elementaktionsereignisse
- Strukturänderungsereignisse
- Globale Desktopänderungsereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ec99a479d390c72232f28521394b2d178f1ad76c913d72ec80aa0a4c93e0d57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859570"
---
# <a name="ui-automation-events-overview"></a>Übersicht über Benutzeroberflächenautomatisierungs-Ereignisse

Die Microsoft Benutzeroberflächenautomatisierung-Ereignisbenachrichtigung ist ein wichtiges Feature für Hilfstechnologien wie Sprachausgaben und Bildschirmlupe. Diese Benutzeroberflächenautomatisierung-Clients verfolgen Ereignisse nach, die von Benutzeroberflächenautomatisierung-Anbietern ausgelöst werden, wenn etwas auf der Benutzeroberfläche geschieht, und verwenden die Informationen, um Endbenutzer zu benachrichtigen.

Die Effizienz wird dadurch erhöht, dass Anbieteranwendungen Ereignisse selektiv (abhängig davon, ob Clients für diese Ereignisse abonniert sind) oder gar nicht auslösen dürfen (wenn kein Client auf Ereignisse wartet).

Benutzeroberflächenautomatisierungs-Ereignisse werden in die folgenden Kategorien unterteilt.



| Ereigniskategorie        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Eigenschaftenänderung       | Wird ausgelöst, wenn sich eine Eigenschaft für Benutzeroberflächenautomatisierung Element- oder Steuerelementmuster ändert. Wenn ein Client beispielsweise ein Anwendungs-Kontrollkästchen-Steuerelement überwachen muss, kann er sich registrieren, um auf ein Eigenschaftsänderungsereignis für die [**IUIAutomationTogglePattern::CurrentToggleState-Eigenschaft zu**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtogglepattern-get_currenttogglestate) lauschen. Wenn das Kontrollkästchen-Steuerelement aktiviert oder deaktiviert wird, löst der Anbieter das Ereignis aus, und der Client kann entsprechend reagieren. |
| Elementaktion        | Wird ausgelöst, wenn eine Änderung der Benutzeroberfläche aus einer Endbenutzer- oder programmgesteuerten Aktivität resultiert, z. B. wenn über [**IUIAutomationInvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern)auf eine Schaltfläche geklickt oder aufgerufen wird.                                                                                                                                                                                                                                                     |
| Strukturänderung      | Wird ausgelöst, wenn sich die Struktur der Benutzeroberflächenautomatisierung-Struktur ändert. Die Struktur wird geändert, wenn neue Benutzeroberflächenelemente angezeigt, ausgeblendet oder vom Desktop entfernt werden.                                                                                                                                                                                                                                                                                                              |
| Globale Desktopänderung | Wird ausgelöst, wenn Aktionen auftreten, die für den Client von allgemeinem Interesse sind, z. B., wenn der Fokus von einem Element zum anderen wechselt oder ein Fenster geschlossen wird.                                                                                                                                                                                                                                                                                                                      |
| Benachrichtigung          | Wird ausgelöst, wenn eine App die [**UiaRchildNotificationEvent-Funktion aufruft.**](https://www.bing.com/search?q=**UiaRaiseNotificationEvent**) [**NotificationKind**](/windows/win32/api/uiautomationcore/ne-uiautomationcore-notificationkind) gibt den Typ der Benachrichtigung an.                                                                                                                                                                                                                                                 |



 

Einige Ereignisse bedeuten nicht zwangsläufig, dass sich der Zustand der Benutzeroberfläche geändert hat. Wenn der Benutzer beispielsweise zu einem Texteingabefeld registerkartent und dann auf eine Schaltfläche klickt, um das Feld zu aktualisieren, wird ein [**\_ \_ UIA-TextChangedEventId-Ereignis**](uiauto-event-ids.md) ausgelöst, auch wenn der Benutzer den Text nicht tatsächlich geändert hat. Bei der Verarbeitung eines Ereignisses muss eine Clientanwendung möglicherweise erst überprüfen, ob sich tatsächlich etwas geändert hat, bevor eine Aktion ausgeführt wird.

Die folgenden Ereignisse können auch dann ausgelöst werden, wenn sich der Zustand der Benutzeroberfläche nicht geändert hat.

-   [**UIA \_ AutomationPropertyChangedEventId**](uiauto-event-ids.md) (abhängig von der geänderten Eigenschaft)
-   [**UIA \_ \_ SelectionItem-ElementSelectedEventId**](uiauto-event-ids.md)
-   [**UIA \_ Selection \_ InvalidatedEventId**](uiauto-event-ids.md)
-   [**UIA \_ Text \_ TextChangedEventId**](uiauto-event-ids.md)

Eine Beschreibung aller Benutzeroberflächenautomatisierung Ereignisse finden Sie unter [Ereignisbezeichner.](uiauto-event-ids.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Abonnieren von Benutzeroberflächenautomatisierung Ereignissen](uiauto-eventsforclients.md)
</dt> </dl>

 

 