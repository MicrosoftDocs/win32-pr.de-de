---
title: Grundlegendes zu Threadingproblemen
description: In diesem Thema werden allgemeine Threadingszenarien für Microsoft Benutzeroberflächenautomatisierung-Clientimplementierungen beschrieben, und es wird erläutert, wie Probleme vermieden werden, die auftreten können, wenn ein Client threading falsch verwendet.
ms.assetid: 0772969a-da55-488e-8b21-7368434df8a9
keywords:
- Clients, Benutzeroberflächenautomatisierung Threadingprobleme
- Clients, Threadingprobleme
- Clients, Ereignishandler-Threadingmodell
- Clients,Benutzeroberflächenautomatisierung Ereignishandler-Threadingmodell
- Clients, Benutzeroberflächenautomatisierung Affinität
- Clients, Affinität
- Benutzeroberflächenautomatisierung,Threadingprobleme
- Benutzeroberflächenautomatisierung,Ereignishandler-Threadingmodell
- Benutzeroberflächenautomatisierung,Affinity
- Threadingprobleme
- Threadingmodell für Ereignishandler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b096df24034e6ed61f9629a49b47a40a95a36792dc9cfe1836a72266ac7a583
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118824529"
---
# <a name="understanding-threading-issues"></a>Grundlegendes zu Threadingproblemen

In diesem Thema werden allgemeine Threadingszenarien für Microsoft Benutzeroberflächenautomatisierung-Clientimplementierungen beschrieben, und es wird erläutert, wie Probleme vermieden werden, die auftreten können, wenn ein Client threading falsch verwendet.

Dieses Thema enthält folgende Abschnitte:

-   [Benutzeroberflächenautomatisierung und der UI-Thread](#ui-automation-and-the-ui-thread)
-   [Threadingmodell für Ereignishandler](#threading-model-for-event-handlers)
-   [COM-Apartmentaffinität auf 64-Bit-Windows](#com-apartment-affinity-on-64-bit-windows)
-   [Zugehörige Themen](#related-topics)

## <a name="ui-automation-and-the-ui-thread"></a>Benutzeroberflächenautomatisierung und der UI-Thread

Aufgrund der Art und Weise, wie Benutzeroberflächenautomatisierung Windows Nachrichten verwendet, können Konflikte auftreten, wenn eine Clientanwendung versucht, mit ihrer eigenen Benutzeroberfläche im UI-Thread zu interagieren. Diese Konflikte können zu einer sehr langsamen Leistung führen oder sogar dazu führen, dass die Anwendung nicht mehr reagiert.

Wenn Ihre Clientanwendung mit allen Elementen auf dem Desktop interagieren soll, einschließlich der eigenen Benutzeroberfläche, sollten Sie alle Benutzeroberflächenautomatisierung Aufrufe von einem separaten Thread ausführen. Dies schließt das Suchen von Elementen ein, z. B. mithilfe von [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) oder der [**IUIAutomationElement::FindAll-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) und der Verwendung von Steuerelementmustern. Dieser Thread sollte keine Fenster besitzen und ein Component Object Model (COM) Multithread-Apartment-Modellthread (MTA) sein (ein Thread, der COM initialisiert, indem [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) mit dem **COINIT \_ MULTITHREADED-Flag** aufgerufen wird).)

Es ist sicher, Benutzeroberflächenautomatisierung Aufrufe in einem Benutzeroberflächenautomatisierung Ereignishandler vorzunehmen, da der Ereignishandler immer für einen Nicht-UI-Thread aufgerufen wird. Wenn Sie jedoch Ereignisse abonnieren, die von der Benutzeroberfläche Ihrer Clientanwendung stammen können, müssen Sie [**IUIAutomation::AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler)oder eine verwandte Methode in einem Nicht-UI-Thread aufrufen (der auch ein MTA-Thread sein sollte). Entfernen Sie Ereignishandler im gleichen Thread.

Ein Benutzeroberflächenautomatisierung Client sollte nicht mehrere Threads verwenden, um Ereignishandler hinzuzufügen oder zu entfernen. Unerwartetes Verhalten kann auftreten, wenn ein Ereignishandler hinzugefügt oder entfernt wird, während ein anderer im selben Clientprozess hinzugefügt oder entfernt wird.

## <a name="threading-model-for-event-handlers"></a>Threadingmodell für Ereignishandler

Ein Benutzeroberflächenautomatisierung Client sollte das COM MTA-Threadingmodell für Threads verwenden, die Ereignishandler implementieren. Die Verwendung des STA-Modells (Singlethreaded Apartment) kann Probleme verursachen, z. B. das Entfernen von Ereignishandlern aus dem Thread durch Clients verhindern.

## <a name="com-apartment-affinity-on-64-bit-windows"></a>COM-Apartmentaffinität auf 64-Bit-Windows

Gemäß der COM-Spezifikation wird die Lebensdauer eines Remoteobjekts durch die Lebensdauer des Apartment gesteuert, in dem die [CoCreateInstance-Funktion](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) aufgerufen wird, um das Objekt zu erstellen. Wenn das ursprüngliche Apartment heruntergefahren wird, wird auch das Remoteobjekt freigegeben.

Für Benutzeroberflächenautomatisierung Clients kann dieses COM-Verhalten bedeuten, dass die Lebensdauer des Remotehilfselements 32/64 (erstellt von UIAutomationCore.dll), das von einem 32-Bit-Element verwendet wird, von der Apartmentlebensdauer des Threads gesteuert wird, der das Element erstellt hat. Wenn der Benutzeroberflächenautomatisierung Client das Element an einen anderen Thread marshallt, kann das Element ungültig werden, wenn das ursprüngliche Apartment heruntergefahren wird. Der Benutzeroberflächenautomatisierung-Client sollte diese Probleme ordnungsgemäß behandeln, indem er Fehler abfängt, während gemarshallte Automatisierungselemente verwendet werden.

Das gleiche Problem kann bei einem 32-Bit-Benutzeroberflächenautomatisierung-Client auftreten, der über 64-Bit-Elemente verfügt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Abrufen von Benutzeroberflächenautomatisierungs-Elementen](uiauto-obtainingelements.md)
</dt> <dt>

[Abonnieren von Benutzeroberflächenautomatisierung Ereignissen](uiauto-eventsforclients.md)
</dt> <dt>

[Übersicht über Benutzeroberflächenautomatisierungs-Ereignisse](uiauto-eventsoverview.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[INFO: Beschreibungen und Funktionsweisen von OLE-Threadingmodellen](https://support.microsoft.com/kb/150777)
</dt> </dl>

 

 