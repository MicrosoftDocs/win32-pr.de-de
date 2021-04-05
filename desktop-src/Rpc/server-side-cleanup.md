---
title: Server seitiges Cleanup
description: Server seitiges Bereinigung und Remote Prozedur Aufruf (RPC).
ms.assetid: 8a48f698-82ae-464b-bdd9-f0245bbc7733
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a66272fc3cca209d6825ac34d5158094ddff39
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037221"
---
# <a name="server-side-cleanup"></a>Server seitiges Cleanup

Stellen Sie sich das folgende Szenario vor:

Ein Client öffnet ein Kontext Handle und beendet oder verliert die Verbindung mit dem Server. Wie erkennt der Server, dass der Client fehlgeschlagen ist und der Kontext Handle ausgeführt werden soll? Es gibt zwei unter Szenarios: eine besteht darin, dass der Client ordnungsgemäß heruntergefahren wird. In diesem Fall wird der Server benachrichtigt, dass er heruntergefahren wird, und der Server kann bereinigt werden, einschließlich der Ausführung von Kontext-Laufzeiten. Wenn der Client nicht ordnungsgemäß heruntergefahren wird oder der Server nicht benachrichtigt werden kann, verwendet der Server Keep-Alives, um zu bestimmen, ob der Client noch verfügbar ist. Auf der Serverseite hat die [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) -Funktion keine Auswirkung. Stattdessen verwendet der Server die Einstellung Global pro Computer – Keep Alive, die standardmäßig ungefähr zwei Stunden beträgt. Wenn der Client nicht auf die Keep-Alives des Servers antwortet, wird die Verbindung geschlossen. Wenn alle Verbindungen mit einem bestimmten Client Prozess geschlossen sind, bereinigt der Server die ausstehenden Kontext Handles und führt Sie aus.

 

 




