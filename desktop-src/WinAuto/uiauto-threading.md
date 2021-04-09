---
title: Grundlegendes zu Threading Problemen
description: In diesem Thema werden häufige Threading Szenarios für Microsoft Benutzeroberflächenautomatisierungs-Client Implementierungen beschrieben und erläutert, wie Probleme vermieden werden, die auftreten können, wenn ein Client fälschlicherweise Threading verwendet.
ms.assetid: 0772969a-da55-488e-8b21-7368434df8a9
keywords:
- Clients, Benutzeroberflächenautomatisierungs-Threading Probleme
- Clients, Threading Probleme
- Clients, ereignishandlerthreading-Modell
- Clients, Benutzeroberflächenautomatisierungs-ereignishandlerthreading Modell
- Clients, Benutzeroberflächenautomatisierungs-Affinität
- Clients, Affinität
- Benutzeroberflächenautomatisierungs, Threading Probleme
- UI-Automatisierung, ereignishandlerthreading-Modell
- Benutzeroberflächen Automatisierung, Affinität
- Threadingprobleme
- ereignishandlerthreading-Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a002132efe4055bb247c7d7290e271e153ac297e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039043"
---
# <a name="understanding-threading-issues"></a>Grundlegendes zu Threading Problemen

In diesem Thema werden häufige Threading Szenarios für Microsoft Benutzeroberflächenautomatisierungs-Client Implementierungen beschrieben und erläutert, wie Probleme vermieden werden, die auftreten können, wenn ein Client fälschlicherweise Threading verwendet.

Dieses Thema enthält folgende Abschnitte:

-   [Benutzeroberflächen Automatisierung und der UI-Thread](#ui-automation-and-the-ui-thread)
-   [Threading Modell für Ereignishandler](#threading-model-for-event-handlers)
-   [COM-Apartment Affinität auf 64-Bit-Windows](#com-apartment-affinity-on-64-bit-windows)
-   [Zugehörige Themen](#related-topics)

## <a name="ui-automation-and-the-ui-thread"></a>Benutzeroberflächen Automatisierung und der UI-Thread

Aufgrund der Art und Weise, wie die Benutzeroberflächen Automatisierung Windows-Meldungen verwendet, können Konflikte auftreten, wenn eine Client Anwendung versucht, mit ihrer eigenen Benutzeroberfläche im UI-Thread zu interagieren. Diese Konflikte können zu einer sehr langsamen Leistung führen oder sogar dazu führen, dass die Anwendung nicht mehr reagiert.

Wenn Ihre Client Anwendung mit allen Elementen auf dem Desktop interagieren soll, einschließlich der eigenen Benutzeroberfläche, sollten Sie alle Aufrufe der Benutzeroberflächen Automatisierung von einem separaten Thread ausführen. Dies umfasst das Auffinden von Elementen, z. b. durch die Verwendung von [**iuiautomationtreewalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) oder der [**iuiautomationelement:: FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) -Methode und die Verwendung von Steuerelement Mustern. Dieser Thread sollte keine Fenster besitzen und sollte ein Component Object Model (com) Multithread-Apartment (MTA)-Modell Thread sein (einer, der com initialisiert, indem er [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) mit dem **coinit- \_ multithreadflag** aufruft).

Es ist sicher, Benutzeroberflächenautomatisierungs-Aufrufe in einem Benutzeroberflächenautomatisierungs-Ereignishandler durchzuführen, da der Ereignishandler immer für einen nicht-UI-Thread aufgerufen wird. Wenn Sie jedoch Ereignisse abonnieren, die von der Benutzeroberfläche der Client Anwendung stammen können, müssen Sie den Aufruf von [**iuiautomation:: AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler)oder einer verknüpften Methode in einem nicht-UI-Thread durchführen (der auch ein MTA-Thread sein sollte). Entfernen Sie Ereignishandler im gleichen Thread.

Ein Benutzeroberflächenautomatisierungs-Client sollte nicht mehrere Threads verwenden, um Ereignishandler hinzuzufügen oder zu entfernen. Unerwartetes Verhalten kann auftreten, wenn ein Ereignishandler hinzugefügt oder entfernt wird, während ein anderer in demselben Client Prozess hinzugefügt oder entfernt wird.

## <a name="threading-model-for-event-handlers"></a>Threading Modell für Ereignishandler

Ein Benutzeroberflächenautomatisierungs-Client sollte das com MTA-Threading Modell für Threads verwenden, die Ereignishandler implementieren. Das STA-Modell (Single Thread-Apartment) kann Probleme verursachen, z. b. das Entfernen von Ereignis Handlern durch Clients aus dem Thread.

## <a name="com-apartment-affinity-on-64-bit-windows"></a>COM-Apartment Affinität auf 64-Bit-Windows

Gemäß der com-Spezifikation wird die Lebensdauer eines Remote Objekts von der Lebensdauer des Apartment gesteuert, in dem die [cokreateinstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion aufgerufen wird, um das Objekt zu erstellen. Wenn das Original Apartment heruntergefahren wird, wird auch das Remote Objekt freigegeben.

Für Benutzeroberflächenautomatisierungs-Clients kann dieses com-Verhalten bedeuten, dass die Lebensdauer des von einem 32-Bit-Element verwendeten Remote-32/64-Hilfsprogramms (von UIAutomationCore.dll) von der Lebensdauer des Threads gesteuert wird, der das Element erstellt hat. Wenn der Benutzeroberflächenautomatisierungs-Client das Element an einen anderen Thread marshundiert, kann das Element ungültig werden, wenn das ursprüngliche Apartment heruntergefahren wird. Der Benutzeroberflächenautomatisierungs-Client sollte diese Probleme durch Abfangen von Fehlern bei der Verwendung von gemarshallten Automatisierungs Elementen ordnungsgemäß behandeln.

Das gleiche Problem kann bei einem 32-Bit-Benutzeroberflächenautomatisierungs-Client auftreten, der 64-Bit-Elemente aufweist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Abrufen von Benutzeroberflächenautomatisierungs-Elementen](uiauto-obtainingelements.md)
</dt> <dt>

[Abonnieren von Benutzeroberflächenautomatisierungs-Ereignissen](uiauto-eventsforclients.md)
</dt> <dt>

[Übersicht über Benutzeroberflächenautomatisierungs-Ereignisse](uiauto-eventsoverview.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[Info: Beschreibungen und Funktionsweise von OLE Threading-Modellen](https://support.microsoft.com/kb/150777)
</dt> </dl>

 

 