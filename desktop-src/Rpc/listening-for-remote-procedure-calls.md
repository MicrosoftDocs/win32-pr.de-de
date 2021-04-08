---
title: Lauschen auf Remote Prozedur Aufrufe
description: Nachdem ein Serverprogramm seine Bindungs Informationen registriert und seine Anwesenheit in einer Name Service-Datenbank angekündigt hat, kann es mit dem lauschen an den Endpunkt für Remote Prozedur Aufrufe beginnen.
ms.assetid: 1c116e44-03a4-4b86-ae37-0b9187981e53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69d9463e0591279377502394541190be685cccd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036248"
---
# <a name="listening-for-remote-procedure-calls"></a>Lauschen auf Remote Prozedur Aufrufe

Nachdem ein Serverprogramm seine Bindungs Informationen registriert und seine Anwesenheit in einer Name Service-Datenbank angekündigt hat, kann es mit dem lauschen an den Endpunkt für Remote Prozedur Aufrufe beginnen. Server Programme aufrufen die Funktion [**rpcserverlauschen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) , um Endpunkte für Client Aufrufe von Remote Prozeduren zu überwachen.

Die DCE-Spezifikation von [**rpcserverlauschen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) gibt an, dass Sie nicht zurückgegeben werden sollte, bis eine Funktion im Serverprogramm [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening)aufruft. Die Microsoft RPC-Implementierung von **rpcserverlauschen** verwendet zwei Parameter, die nicht in der DCE-Spezifikation vorkommen: *dontwait* und *minimumcallthreads*. Das Serverprogramm kann einen Wert ungleich 0 (null) für den *dontwait* -Parameter übergeben. Wenn dies der Fall ist, wird die **rpcserverlauschen** -Funktion sofort zurückgegeben. Verwenden Sie die [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) -Routine, um den warte Vorgang auszuführen, der normalerweise mit **rpcserverlauschen** verknüpft ist.

 

 




