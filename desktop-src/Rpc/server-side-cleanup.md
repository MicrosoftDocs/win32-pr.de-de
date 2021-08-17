---
title: Serverseitige Bereinigung
description: Serverseitige Bereinigung und Remoteprozeduraufruf (RPC).
ms.assetid: 8a48f698-82ae-464b-bdd9-f0245bbc7733
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 223cd15eb659a62c4a758098e9b0f70e977ebb069a2a305d2909b97b5fb12010
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925292"
---
# <a name="server-side-cleanup"></a>Serverseitige Bereinigung

Imagine folgendes Szenario:

Ein Client öffnet ein Kontexthand handle und beendet dann entweder die Verbindung mit dem Server oder verliert sie. Wie erkennt der Server, dass der Client ausgefallen ist und das Kontexthand handle heruntergefahren werden sollte? Es gibt zwei Unterscenarios: Einer ist, dass der Client in einer geordneten Weise heruntergefahren wird. In diesem Fall wird der Server benachrichtigt, dass er heruntergefahren wird, und der Server kann eine Bereinigung durchführen, einschließlich der Ausführung von Kontext run downs. Wenn der Client nicht in einer geordneten Weise heruntergefahren wird oder den Server nicht benachrichtigen kann, verwendet der Server keep alives, um zu bestimmen, ob der Client weiterhin verfügbar ist. Auf Serverseite hat die [**RpcMgmtSetComTimeout-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) keine Auswirkungen. Stattdessen verwendet der Server die Einstellung global pro Computer –Keep Alive, die standardmäßig ungefähr zwei Stunden beträgt. Wenn der Client nicht auf keep alives des Servers antwortet, wird die Verbindung geschlossen. Wenn alle Verbindungen mit einem bestimmten Clientprozess geschlossen werden, bereinigt der Server ausstehende Kontexthandles und führt sie aus.

 

 




