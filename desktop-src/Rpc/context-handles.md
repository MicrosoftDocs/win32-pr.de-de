---
title: Kontext Handles
description: Manchmal ist es bei verteilten Anwendungen erforderlich, dass das Serverprogramm Statusinformationen zwischen Client aufrufen beibehält.
ms.assetid: 91732a75-0a3a-44bd-9db9-c11be6fd2d70
keywords:
- Remote Prozedur Aufruf RPC, beschrieben, Kontext Handles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8ff36ff8f1a36843293060e091b7eecee0d8666
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338992"
---
# <a name="context-handles"></a>Kontext Handles

Manchmal ist es bei verteilten Anwendungen erforderlich, dass das Serverprogramm Statusinformationen zwischen Client aufrufen beibehält. Server Programme, die mehrere Clients gleichzeitig bedienen, müssen die Zustandsinformationen für jeden Client beibehalten. Da der Client und der Server unterschiedliche Adressräume auf unterschiedlichen Computern verwenden und sich nicht notwendigerweise gegenseitig vertrauen, funktionieren häufige Ansätze für die Datenfreigabe häufig nicht. Beispielsweise können Client und Server keine Statusinformationen in Ihrer Remote Sitzung in globalen Variablen verwalten, da Sie nicht denselben globalen Adressraum gemeinsam verwenden. Es ist schwierig, die Informationen in einer freigegebenen Datei aufzubewahren, da Sie auf unterschiedlichen Computern ausgeführt werden. Ein vereinfachter Ansatz besteht darin, den gesamten Zustand an den Client zu senden und den Client beim nächsten-Rückruf zurückzugeben, aber dieser Ansatz weist Mängel auf: der Server vertraut nicht notwendigerweise dem Client, um den richtigen Status zurückzugeben, und der Zustand ist möglicherweise implizit an einen anderen Status auf dem Server gebunden, z. b. Datei Handles oder geöffnete Sockets.

Microsoft RPC bietet einen leistungsfähigen und sicheren Mechanismus namens Kontext Handles, mit dem der Zustand eines bestimmten Clients auf einem Server beibehalten wird. Die Zustandsinformationen werden als Kontext des Servers bezeichnet. Clients können einen Kontext Handle abrufen, um den Kontext des Servers für die einzelnen RPC-Sitzungen zu identifizieren.

Beispielsweise kann für jeden Client in einer verteilten Anwendung das Serverprogramm eine Datendatei für die RPC-Sitzung erstellen und aktualisieren. Der Server kann sein Datei Handle für die Datendatei jedes Clients als Kontext Handle verwenden. Jedes Mal, wenn ein Client Vorgänge für die Datendatei anfordert, die der Server dafür erstellt hat, übergibt der Client das Kontext Handle an den Server. Der Client erhält nicht das eigentliche Datei handle. Es wird ein nicht transparentes Token abgerufen, das von der RPC-Laufzeit des Servers dem Datei Handle eindeutig zugeordnet werden kann. Da es sich bei dem Kontext Handle tatsächlich um ein Datei Handle handelt, ist das Kontext Handle nur im Adressraum des Servers sinnvoll. Allerdings kann das Client Programm das Kontext Handle verwenden, um dem Server mitzuteilen, welche Datei Updates ausführen soll.

Andere Daten können auch Kontext Handles sein. Beispielsweise können ein Client und ein Server eine Datensatznummer eines Datenbankdaten Satzes als Datei Handle verwenden. Wenn der Client eine Reihe von Updates für einen bestimmten Datensatz ausführen muss, kann er die Datensatznummer als Kontext Handle abrufen. Die Datensatznummer wird bei jedem Aufruf einer Remote Prozedur zum Aktualisieren des Datenbankdaten Satzes an den Server übergeben.

In den meisten Fällen verweist ein Kontext Handle auf einen Speicherblock auf dem Server, auf dem der Server verschiedene Verwaltungsinformationen beibehält.

Dieser Abschnitt enthält Informationen zum Definieren und Verwenden von Kontext Handles. Die Erörterung finden Sie in den folgenden Themen:

-   [Schnittstellen Entwicklung mithilfe von Kontext Handles](interface-development-using-context-handles.md)
-   [Server Entwicklung mithilfe von Kontext Handles](server-development-using-context-handles.md)
-   [Client Entwicklung mithilfe von Kontext Handles](client-development-using-context-handles.md)
-   [Server Kontext-Lauf-ab-Routine](server-context-run-down-routine.md)
-   [Client Kontext Zurücksetzung](client-context-reset.md)
-   [Multithread-Clients und Kontext Handles](multithreaded-clients-and-context-handles.md)

 

 




