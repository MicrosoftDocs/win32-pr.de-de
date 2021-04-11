---
title: Abonnieren von Benutzeroberflächenautomatisierungs-Ereignissen
description: Die Microsoft-Benutzeroberflächen Automatisierung ermöglicht Clients das Abonnieren von Ereignissen, die von Interesse sind. Diese Funktion verbessert die Leistung, da die Notwendigkeit besteht, die Benutzeroberflächen Elemente im System ständig abzufragen, um festzustellen, ob Informationen, Strukturen oder Zustände geändert wurden.
ms.assetid: 7019ecb8-6123-4e00-926c-6725d7e71385
keywords:
- Clients, Benutzeroberflächenautomatisierungs-Ereignisse
- Clients, Ereignisse für die Benutzeroberflächen Automatisierung
- Benutzeroberflächenautomatisierungs, Ereignisse für Clients
- Benutzeroberflächenautomatisierungs, Client Ereignisse
- Benutzeroberflächen Automatisierung, abonnieren von Ereignissen
- Benutzeroberflächenautomatisierungs, Abonnement Methoden
- UI-Automatisierung, Codebeispiele
- Benutzeroberflächen Automatisierung, Beispiele
- UI-Automatisierung, Beispiele
- Abonnieren von Benutzeroberflächenautomatisierungs-Ereignissen
- Ereignisse, Benutzeroberflächenautomatisierungs-Abonnement
- Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d9a89df1b9d2afc401e07b6cd77d1307d912f11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310220"
---
# <a name="subscribing-to-ui-automation-events"></a>Abonnieren von Benutzeroberflächenautomatisierungs-Ereignissen

Die Microsoft-Benutzeroberflächen Automatisierung ermöglicht Clients das Abonnieren von Ereignissen, die von Interesse sind. Diese Funktion verbessert die Leistung, da die Notwendigkeit besteht, die Benutzeroberflächen Elemente im System ständig abzufragen, um festzustellen, ob Informationen, Strukturen oder Zustände geändert wurden.

Die Effizienz wird auch durch die Möglichkeit verbessert, Ereignissen nur innerhalb eines definierten Umfangs zu lauschen. Ein Client kann z. b. auf Auswahl Änderungen an einem Element in einer Liste, in der Liste selbst oder in einem gesamten Dialogfeld lauschen.

> [!Note]  
> Gehen Sie nicht davon aus, dass alle möglichen Ereignisse von einem Benutzeroberflächenautomatisierungs-Anbieter ausgelöst werden. Beispielsweise bewirken nicht alle Eigenschafts Änderungen, dass Ereignisse von den Standard Proxy Anbietern für Windows Forms-und Microsoft Win32-Steuerelemente ausgelöst werden.

 

Eine umfassendere Übersicht über Benutzeroberflächenautomatisierungs-Ereignisse finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).

> [!Note]  
> Vor der Implementierung eines Ereignis Handlers sollten Sie mit den Threading Problemen vertraut sein, die Untergrund Legendes zu [Threading Problemen](uiauto-threading.md)beschrieben werden.

 

Dieses Thema enthält folgende Abschnitte:

-   [Registrieren von Ereignis Handlern](#registering-event-handlers)
-   [Beispiele](#examples)
-   [Zugehörige Themen](#related-topics)

## <a name="registering-event-handlers"></a>Registrieren von Ereignis Handlern

Client Anwendungen abonnieren Ereignisse einer bestimmten Art, indem Sie einen Ereignishandler mit einer der folgenden [**iuiautomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) -Methoden registrieren.



| Abonnement Methode                                                                                                                                                                                                | Ereignistyp       | Rückruf Schnittstelle                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------------------------------------------------------------------------------------------------|
| [**Addfocuschangedebug-thandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addfocuschangedeventhandler)                                                                                                                            | Fokusänderung     | [**Iuiautomationfocuschangedebug-thandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler)         |
| [**Addpropertychangeabventhandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler), [ **addpropertychangeenventhandlernativearray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray) | Eigenschaftenänderung  | [**Iuiautomationpropertychangeabventhandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler)   |
| [**Addstructurechangeabventhandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addstructurechangedeventhandler)                                                                                                                    | Strukturänderung | [**Iuiautomationstructurechangeabventhandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler) |
| [**Addnotificationeventhandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation5-addnotificationeventhandler)                                                                                                                           | Benachrichtigung     | [**Iuiautomationnotificationeventhandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotificationeventhandler)         |
| [**AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler)                                                                                                                                | Sonstige Ereignisse     | [**Iuiautomationeventhandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationeventhandler)                                 |



 

Wenn ein Client einen Ereignishandler für alle Nachfolger Elemente ([**TreeScope \_**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope)-Nachfolger) hinzufügt, fügt die Benutzeroberflächen Automatisierung nur einen Handler für den Stamm der Teilstruktur hinzu, und der Handler lauscht auf alle nachfolgenden Elemente. Die Benutzeroberflächen Automatisierung fügt Ereignishandler nicht rekursiv hinzu.

Wenn ein Client die [**iuiautomation:: removealleventhandlers**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removealleventhandlers) -Methode aufruft, entfernt die Benutzeroberflächen Automatisierung alle Ereignishandler aus dem Client Prozess.

Um Ereignisse zu empfangen und zu verarbeiten, implementieren Sie ein Ereignis Behandlungs Objekt, das eine Rückruf Schnittstelle verfügbar macht, und Sie müssen das Objekt durch Aufrufen einer Ereignis Registrierungsmethode (z. b. [**iuiautomation:: addpropertychangedeventhandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler)) registrieren. Die Rückruf Schnittstelle verfügt über eine einzige Methode. Die Benutzeroberflächen Automatisierung ruft diese Methode auf, wenn das Ereignis verarbeitet wird.

Beim Herunterfahren oder wenn Benutzeroberflächenautomatisierungs-Ereignisse für die Anwendung nicht mehr von Interesse sind, sollten Benutzeroberflächenautomatisierungs-Clients eine oder mehrere der folgenden [**iuiautomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) -Methoden abrufen.

> [!Note]  
> Ein Benutzeroberflächenautomatisierungs-Client sollte nicht mehrere Threads verwenden, um Ereignishandler hinzuzufügen oder zu entfernen. Unerwartetes Verhalten kann auftreten, wenn ein Ereignishandler hinzugefügt oder entfernt wird, während ein anderer in demselben Client Prozess hinzugefügt oder entfernt wird.

 



| Methode                                                                                                | BESCHREIBUNG                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RemoveAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removeautomationeventhandler)             | Hebt die Registrierung eines Ereignis Handlers auf, der mithilfe von [**AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler)registriert wurde.                                                                                                                                  |
| [**Removefocuschangedebugsthandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removefocuschangedeventhandler)         | Hebt die Registrierung eines Ereignis Handlers auf, der mithilfe von [**addfocuschangedeventhandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addfocuschangedeventhandler)registriert wurde.                                                                                                                              |
| [**Removepropertychangeabventhandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removepropertychangedeventhandler)   | Hebt die Registrierung eines Ereignis Handlers auf, der mithilfe von [**addpropertychangedeventhandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) oder [**addpropertychangedeventhandlerativearray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray)registriert wurde. |
| [**RemoveStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removestructurechangedeventhandler) | Hebt die Registrierung eines Ereignis Handlers auf, der mithilfe von [**AddStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addstructurechangedeventhandler)registriert wurde.                                                                                                                      |
| [**Removenotificationeventhandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation5-removenotificationeventhandler)        | Hebt die Registrierung eines Ereignis Handlers auf, der von Weas mithilfe von [**addnotificationeventhandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation5-addnotificationeventhandler)registriert wurde.                                                                                                                            |
| [**Removealleventhandlers**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removealleventhandlers)                         | Hebt die Registrierung aller registrierten Ereignishandler auf.                                                                                                                                                                                                                                      |



 

Es ist möglich, dass ein Ereignis an einen Ereignishandler übermittelt wird, nachdem der Handler nicht abonniert wurde, wenn das Ereignis gleichzeitig mit der Anforderung zum Kündigen des Ereignisses empfangen wird. Die bewährte Methode besteht darin, den Component Object Model (com)-Standard zu befolgen und das Ereignishandlerobjekt zu zerstören, bis der Verweis Zähler Null erreicht hat. Das zerstören eines Ereignis Handlers unmittelbar nach dem Aufheben des Abonnements für Ereignisse kann zu einer Zugriffsverletzung führen, wenn ein Ereignis spät zugestellt wird.

## <a name="examples"></a>Beispiele

Codebeispiele, die zeigen, wie Benutzeroberflächenautomatisierungs-Ereignisse behandelt werden, finden Sie unter [Implementieren von Ereignis Handlern](uiauto-howto-implement-event-handlers.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Benutzeroberflächenautomatisierungs-Ereignisse](uiauto-eventsoverview.md)
</dt> <dt>

[Grundlegendes zu Threading Problemen](uiauto-threading.md)
</dt> </dl>

 

 




