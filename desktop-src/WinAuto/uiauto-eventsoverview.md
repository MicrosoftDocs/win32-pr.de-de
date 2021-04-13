---
title: Übersicht über Benutzeroberflächenautomatisierungs-Ereignisse
description: Die Microsoft UI Automation-Ereignis Benachrichtigung ist ein wesentliches Feature für Hilfstechnologien wie Sprachausgabe und Bildschirmlupe.
ms.assetid: 0ded64ba-188e-427e-897f-4381237ace75
keywords:
- UI-Automatisierung, Übersicht über Ereignisse
- Benutzeroberflächen Automatisierung, Ereignis Kategorien
- Benutzeroberflächen Automatisierung, Ereignis Benachrichtigungen
- Ereignisbenachrichtigungen
- Ereignisse, Kategorien
- Ereignisse, Ereignis Benachrichtigungen
- Eigenschaften Änderungs Ereignisse
- Element Aktions Ereignisse
- Struktur Änderungs Ereignisse
- Globale Desktop Änderungs Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ddd61ed72ae0e92a13f6b59b493427fd7be421
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315273"
---
# <a name="ui-automation-events-overview"></a>Übersicht über Benutzeroberflächenautomatisierungs-Ereignisse

Die Microsoft UI Automation-Ereignis Benachrichtigung ist ein wesentliches Feature für Hilfstechnologien wie Sprachausgabe und Bildschirmlupe. Diese Benutzeroberflächenautomatisierungs-Clients verfolgen Ereignisse, die von Benutzeroberflächenautomatisierungs-Anbietern ausgelöst werden, wenn in der Benutzeroberfläche etwas passiert, und verwenden die Informationen, um die Endbenutzer

Die Effizienz wird dadurch erhöht, dass Anbieteranwendungen Ereignisse selektiv (abhängig davon, ob Clients für diese Ereignisse abonniert sind) oder gar nicht auslösen dürfen (wenn kein Client auf Ereignisse wartet).

Benutzeroberflächenautomatisierungs-Ereignisse werden in die folgenden Kategorien unterteilt.



| Ereigniskategorie        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Eigenschaftenänderung       | Wird ausgelöst, wenn sich eine Eigenschaft im Benutzeroberflächenautomatisierungs-Element oder Steuerelement Muster ändert Wenn ein Client z. b. ein Kontrollkästchen-Steuerelement einer Anwendung überwachen muss, kann er sich registrieren, um auf ein Eigenschaften Änderungs Ereignis in der [**iuiautomationtogglepattern:: currenttogglestate**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtogglepattern-get_currenttogglestate) -Eigenschaft zu lauschen. Wenn das Kontrollkästchen-Steuerelement aktiviert oder deaktiviert wird, löst der Anbieter das Ereignis aus, und der Client kann entsprechend reagieren. |
| Elementaktion        | Wird ausgelöst, wenn eine Änderung in der Benutzeroberfläche von Endbenutzern oder programmgesteuerten Aktivitäten resultiert, z. b. wenn auf eine Schaltfläche geklickt oder über [**iuiautomationinvokepattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern)aufgerufen wird.                                                                                                                                                                                                                                                     |
| Strukturänderung      | Wird ausgelöst, wenn sich die Struktur der Benutzeroberflächenautomatisierungs-Struktur ändert. Die Struktur wird geändert, wenn neue Benutzeroberflächenelemente angezeigt, ausgeblendet oder vom Desktop entfernt werden.                                                                                                                                                                                                                                                                                                              |
| Globale Desktopänderung | Wird ausgelöst, wenn Aktionen auftreten, die für den Client von allgemeinem Interesse sind, z. B., wenn der Fokus von einem Element zum anderen wechselt oder ein Fenster geschlossen wird.                                                                                                                                                                                                                                                                                                                      |
| Benachrichtigung          | Wird ausgelöst, wenn eine APP die [**uiaraisenotificationevent**](https://www.bing.com/search?q=**UiaRaiseNotificationEvent**) -Funktion aufruft. [**Notificationkind**](/windows/win32/api/uiautomationcore/ne-uiautomationcore-notificationkind) gibt den Typ der Benachrichtigung an.                                                                                                                                                                                                                                                 |



 

Einige Ereignisse bedeuten nicht zwangsläufig, dass sich der Zustand der Benutzeroberfläche geändert hat. Wenn z. b. der Benutzer auf ein Texteingabefeld klickt und dann auf eine Schaltfläche klickt, um das Feld zu aktualisieren, wird ein [**UIA \_ Text \_ textchangedeventid-**](uiauto-event-ids.md) Ereignis ausgelöst, auch wenn der Benutzer den Text nicht geändert hat. Bei der Verarbeitung eines Ereignisses muss eine Clientanwendung möglicherweise erst überprüfen, ob sich tatsächlich etwas geändert hat, bevor eine Aktion ausgeführt wird.

Die folgenden Ereignisse können auch dann ausgelöst werden, wenn sich der Zustand der Benutzeroberfläche nicht geändert hat.

-   [**UIA \_ Automationpropertychangedebug**](uiauto-event-ids.md) (abhängig von der geänderten Eigenschaft)
-   [**UIA \_ SelectionItem \_ elementselectedebug**](uiauto-event-ids.md)
-   [**UIA- \_ Auswahl \_ invalidatedeventid**](uiauto-event-ids.md)
-   [**UIA \_ \_ -Text textchangedebug**](uiauto-event-ids.md)

Eine Beschreibung aller Benutzeroberflächenautomatisierungs-Ereignisse finden Sie unter [Ereignis](uiauto-event-ids.md)Bezeichner.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Abonnieren von Benutzeroberflächenautomatisierungs-Ereignissen](uiauto-eventsforclients.md)
</dt> </dl>

 

 