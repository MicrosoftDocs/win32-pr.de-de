---
title: Lauschen auf Remoteprozeduraufrufe
description: Nachdem ein Serverprogramm seine Bindungsinformationen registriert und das Vorhandensein in einer Namensdienstdatenbank angekündigt hat, kann es mit dem Lauschen auf den Endpunkt auf Remoteprozeduraufrufe beginnen.
ms.assetid: 1c116e44-03a4-4b86-ae37-0b9187981e53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb60b6d383c7c31b7eb59aab6f17fcdad1fde108b6f26d4fa73627d34f74340
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020110"
---
# <a name="listening-for-remote-procedure-calls"></a>Lauschen auf Remoteprozeduraufrufe

Nachdem ein Serverprogramm seine Bindungsinformationen registriert und das Vorhandensein in einer Namensdienstdatenbank angekündigt hat, kann es mit dem Lauschen auf den Endpunkt auf Remoteprozeduraufrufe beginnen. Serverprogramme rufen die [**RpcServerListen-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) auf, um Endpunkte auf Clientaufrufe von Remoteprozeduren zu überwachen.

Die DCE-Spezifikation von [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) gibt an, dass sie erst dann zurückgeben soll, wenn eine Funktion im Serverprogramm [**RpcMgmtStopServerListening aufruft.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) Die Microsoft RPC-Implementierung von **RpcServerListen** verwendet zwei Parameter, die nicht in der DCE-Spezifikation enthalten sind: *DontWait* und *MinimumCallThreads*. Ihr Serverprogramm kann einen Wert ungleich 0 (null) für den *DontWait-Parameter* übergeben. Wenn dies der Typ ist, **gibt die RpcServerListen-Funktion** sofort zurück. Verwenden Sie [**die RpcMgmtWaitServerListen-Routine,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) um den Wartevorgang durchzuführen, der normalerweise **RpcServerListen zugeordnet ist.**

 

 




