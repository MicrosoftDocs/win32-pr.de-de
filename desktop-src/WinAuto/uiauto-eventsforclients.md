---
title: Abonnieren von Benutzeroberflächenautomatisierung Ereignissen
description: Mit Microsoft Benutzeroberflächenautomatisierung können Clients interessante Ereignisse abonnieren. Diese Funktion verbessert die Leistung, da die Benutzeroberflächenelemente im System nicht mehr ständig abgefragt werden müssen, um festzustellen, ob sich Informationen, Strukturen oder Zustände geändert haben.
ms.assetid: 7019ecb8-6123-4e00-926c-6725d7e71385
keywords:
- Clients, Benutzeroberflächenautomatisierung Ereignisse
- Clients, Ereignisse für Benutzeroberflächenautomatisierung
- Benutzeroberflächenautomatisierung,Ereignisse für Clients
- Benutzeroberflächenautomatisierung,Clientereignisse
- Benutzeroberflächenautomatisierung,Abonnieren von Ereignissen
- Benutzeroberflächenautomatisierung,Abonnementmethoden
- Benutzeroberflächenautomatisierung, Codebeispiele
- Benutzeroberflächenautomatisierung,Beispiele
- Benutzeroberflächenautomatisierung,Beispiele
- Abonnieren von Benutzeroberflächenautomatisierungs-Ereignissen
- Ereignisse,Benutzeroberflächenautomatisierung Abonnement
- Proben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a0e8dd4cb2d810ad8423c1fa4f75020a9489ceb72acbe1483cb439e943b5676
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119505300"
---
# <a name="subscribing-to-ui-automation-events"></a>Abonnieren von Benutzeroberflächenautomatisierung Ereignissen

Mit Microsoft Benutzeroberflächenautomatisierung können Clients interessante Ereignisse abonnieren. Diese Funktion verbessert die Leistung, da die Benutzeroberflächenelemente im System nicht mehr ständig abgefragt werden müssen, um festzustellen, ob sich Informationen, Strukturen oder Zustände geändert haben.

Die Effizienz wird auch durch die Möglichkeit verbessert, Ereignissen nur innerhalb eines definierten Umfangs zu lauschen. Beispielsweise kann ein Client auf Auswahländerungen an einem Element in einer Liste, an der Liste selbst oder an einem gesamten Dialogfeld lauschen.

> [!Note]  
> Gehen Sie nicht davon aus, dass alle möglichen Ereignisse von einem Benutzeroberflächenautomatisierung Anbieter ausgelöst werden. Beispielsweise führen nicht alle Eigenschaftenänderungen dazu, dass Ereignisse von den Standardproxyanbietern für Windows Forms- und Microsoft Win32-Steuerelemente ausgelöst werden.

 

Eine umfassendere Übersicht über Benutzeroberflächenautomatisierung Ereignisse finden Sie unter [übersicht über Benutzeroberflächenautomatisierung Ereignisse.](uiauto-eventsoverview.md)

> [!Note]  
> Bevor Sie einen Ereignishandler implementieren, sollten Sie mit den Threadingproblemen vertraut sein, die unter Grundlegendes zu [Threadingproblemen](uiauto-threading.md)beschrieben sind.

 

Dieses Thema enthält folgende Abschnitte:

-   [Registrieren von Ereignishandlern](#registering-event-handlers)
-   [Beispiele](#examples)
-   [Zugehörige Themen](#related-topics)

## <a name="registering-event-handlers"></a>Registrieren von Ereignishandlern

Clientanwendungen abonnieren Ereignisse einer bestimmten Art, indem sie einen Ereignishandler mit einer der folgenden [**IUIAutomation-Methoden**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) registrieren.



| Subscription-Methode                                                                                                                                                                                                | Ereignistyp       | Rückrufschnittstelle                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------------------------------------------------------------------------------------------------|
| [**AddFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addfocuschangedeventhandler)                                                                                                                            | Fokusänderung     | [**IUIAutomationFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler)         |
| [**AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler), [ **AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray) | Eigenschaftenänderung  | [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler)   |
| [**AddStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addstructurechangedeventhandler)                                                                                                                    | Strukturänderung | [**IUIAutomationStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler) |
| [**AddNotificationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation5-addnotificationeventhandler)                                                                                                                           | Benachrichtigung     | [**IUIAutomationNotificationEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotificationeventhandler)         |
| [**AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler)                                                                                                                                | Sonstige Ereignisse     | [**IUIAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationeventhandler)                                 |



 

Wenn ein Client einen Ereignishandler für alle Nachfolger [**(TreeScope \_ Descendants)**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope)hinzufügt, fügt Benutzeroberflächenautomatisierung nur einen Handler für den Stamm der Unterstruktur hinzu, und der Handler lauscht über alle Nachfolger. Benutzeroberflächenautomatisierung fügt ereignishandler nicht rekursiv hinzu.

Wenn ein Client die [**IUIAutomation::RemoveAllEventHandlers-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removealleventhandlers) aufruft, entfernt Benutzeroberflächenautomatisierung alle Ereignishandler aus dem Clientprozess.

Zum Empfangen und Behandeln von Ereignissen implementieren Sie ein Ereignisbehandlungsobjekt, das eine Rückrufschnittstelle verfügbar macht, und Sie müssen das Objekt registrieren, indem Sie eine Ereignisregistrierungsmethode wie [**IUIAutomation::AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler)aufrufen. Die Rückrufschnittstelle verfügt über eine einzelne Methode. Benutzeroberflächenautomatisierung ruft diese Methode auf, wenn das Ereignis verarbeitet wird.

Beim Herunterfahren oder wenn Benutzeroberflächenautomatisierung Ereignisse für die Anwendung nicht mehr von Interesse sind, sollten Benutzeroberflächenautomatisierung Clients mindestens eine der folgenden [**IUIAutomation-Methoden**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) aufrufen.

> [!Note]  
> Ein Benutzeroberflächenautomatisierung Client sollte nicht mehrere Threads verwenden, um Ereignishandler hinzuzufügen oder zu entfernen. Unerwartetes Verhalten kann auftreten, wenn ein Ereignishandler hinzugefügt oder entfernt wird, während ein anderer im selben Clientprozess hinzugefügt oder entfernt wird.

 



| Methode                                                                                                | Beschreibung                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RemoveAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removeautomationeventhandler)             | Aufheben der Registrierung eines Ereignishandlers, der mit [**AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler)registriert wurde.                                                                                                                                  |
| [**RemoveFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removefocuschangedeventhandler)         | Aufheben der Registrierung eines Ereignishandlers, der mit [**AddFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addfocuschangedeventhandler)registriert wurde.                                                                                                                              |
| [**RemovePropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removepropertychangedeventhandler)   | Aufheben der Registrierung eines Ereignishandlers, der mit [**AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) oder [**AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray)registriert wurde. |
| [**RemoveStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removestructurechangedeventhandler) | Aufheben der Registrierung eines Ereignishandlers, der mit [**AddStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addstructurechangedeventhandler)registriert wurde.                                                                                                                      |
| [**RemoveNotificationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation5-removenotificationeventhandler)        | Aufheben der Registrierung eines Ereignishandlers, der mit [**AddNotificationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation5-addnotificationeventhandler)registriert wurde.                                                                                                                            |
| [**RemoveAllEventHandlers**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removealleventhandlers)                         | Hebt die Registrierung aller registrierten Ereignishandler auf.                                                                                                                                                                                                                                      |



 

Es ist möglich, dass ein Ereignis an einen Ereignishandler übermittelt wird, nachdem das Abonnement des Handlers gekündigt wurde, wenn das Ereignis gleichzeitig mit der Anforderung zum Kündigen des Ereignisses empfangen wird. Die bewährte Methode besteht darin, den COM-Standard (Component Object Model) zu befolgen und zu vermeiden, dass das Ereignishandlerobjekt zerstört wird, bis der Verweiszähler 0 (null) erreicht hat. Das Löschen eines Ereignishandlers unmittelbar nach dem Abmelden von Ereignissen kann zu einer Zugriffsverletzung führen, wenn ein Ereignis zu spät übermittelt wird.

## <a name="examples"></a>Beispiele

Codebeispiele, die zeigen, wie Benutzeroberflächenautomatisierung-Ereignisse behandelt werden, finden Sie unter [Implementieren von Ereignishandlern.](uiauto-howto-implement-event-handlers.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Benutzeroberflächenautomatisierungs-Ereignisse](uiauto-eventsoverview.md)
</dt> <dt>

[Grundlegendes zu Threadingproblemen](uiauto-threading.md)
</dt> </dl>

 

 




