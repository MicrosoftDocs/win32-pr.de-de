---
title: Kontexthandles
description: Es ist manchmal der Fall, dass verteilte Anwendungen das Serverprogramm erfordern, um Statusinformationen zwischen Clientaufrufen zu verwalten.
ms.assetid: 91732a75-0a3a-44bd-9db9-c11be6fd2d70
keywords:
- Remoteprozeduraufruf RPC , beschrieben, Kontexthandles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e73fb49a2e4c09ec818777389194df98e0d7b8bcac618d05ff7b519aefe5eb28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073420"
---
# <a name="context-handles"></a>Kontexthandles

Es ist manchmal der Fall, dass verteilte Anwendungen das Serverprogramm erfordern, um Statusinformationen zwischen Clientaufrufen zu verwalten. Serverprogramme, die mehrere Clients gleichzeitig ausführen, müssen die Zustandsinformationen für jeden Client behalten. Da der Client und der Server unterschiedliche Adressräume auf verschiedenen Computern verwenden und sie einander nicht unbedingt vertrauen, funktionieren gängige Ansätze für die Gemeinsame Nutzung von Daten häufig nicht. Beispielsweise können Client und Server keine Statusinformationen in ihrer Remotesitzung in globalen Variablen verwalten, da sie nicht denselben globalen Adressraum verwenden. Es ist schwierig, die Informationen in einer freigegebenen Datei zu speichern, da sie auf verschiedenen Computern ausgeführt werden. Ein vereinfachter Ansatz kann sein, den ganzen Zustand an den Client zu senden und ihn beim nächsten Aufruf zurückgeben zu müssen, aber dieser Ansatz hat Fehler: Der Server vertraut nicht unbedingt dem Client, um den richtigen Zustand zurück zu geben, und der Zustand kann implizit an einen anderen Zustand auf dem Server gebunden sein, z. B. Dateihandles oder geöffnete Sockets.

Microsoft RPC bietet einen leistungsstarken und sicheren Mechanismus, der als Kontexthandles bezeichnet wird, um den Zustand eines bestimmten Clients auf einem Server zu erhalten. Die Zustandsinformationen werden als Kontext des Servers bezeichnet. Clients können ein Kontexthand handle abrufen, um den Kontext des Servers für ihre einzelnen RPC-Sitzungen zu identifizieren.

Beispielsweise kann jeder Client in einer verteilten Anwendung vom Serverprogramm eine Datendatei für ihre RPC-Sitzung erstellen und aktualisieren. Der Server kann sein Dateihand handle für die Datendatei jedes Clients als Kontexthand handle verwenden. Jedes Mal, wenn ein Client Vorgänge für die Datendatei angibt, die der Server dafür erstellt, übergibt der Client das Kontexthand handle an den Server. Der Client bekommt das Dateihand handle nicht selbst. Er ruft ein nicht transparentes Token ab, das die RPC-Laufzeit des Servers dem Dateihand handle eindeutig zuordnen kann. Da das Kontexthand handle tatsächlich ein Dateihand handle ist, ist das Kontexthandy nur im Adressraum des Servers sinnvoll. Das Clientprogramm kann jedoch das Kontexthand handle verwenden, um den Server darüber zu informieren, auf welcher Datei Updates ausgeführt werden.

Andere Daten können auch Kontexthandles sein. Ein Client und Server können beispielsweise eine Datensatznummer eines Datenbankdatensatz als Dateihand handle verwenden. Wenn der Client eine Reihe von Updates für einen bestimmten Datensatz ausführen muss, könnte er die Datensatznummer als Kontexthand handle abrufen. Die Datensatznummer wird bei jedem Aufruf einer Remoteprozedur zum Aktualisieren des Datenbankdatensatz an den Server übergeben.

Meistens verweist ein Kontexthand handle auf einen Speicherblock auf dem Server, auf dem der Server verschiedene Verwaltungsinformationen speichert.

Dieser Abschnitt enthält Informationen zum Definieren und Verwenden von Kontexthandles. Die Diskussion wird in den folgenden Themen behandelt:

-   [Schnittstellenentwicklung mitHilfe von Kontexthandles](interface-development-using-context-handles.md)
-   [Serverentwicklung mitHilfe von Kontexthandles](server-development-using-context-handles.md)
-   [Cliententwicklung mitHilfe von Kontexthandles](client-development-using-context-handles.md)
-   [Run-down-Routine für Den Serverkontext](server-context-run-down-routine.md)
-   [Clientkontextzurücksetzung](client-context-reset.md)
-   [Multithreadclients und Kontexthandles](multithreaded-clients-and-context-handles.md)

 

 




