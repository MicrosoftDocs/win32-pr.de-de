---
title: Lauschen auf Client Anrufe
description: Nachdem die Serveranwendung ihre Schnittstellen registriert, die erforderlichen Bindungs Informationen erstellt und ihre Endpunkte registriert hat, ist Sie bereit, mit dem lauschen auf Remote Prozedur Aufrufe von Client Programmen zu beginnen.
ms.assetid: ca9d24ed-0acc-45de-bbb2-761c56745a58
keywords:
- Remote Prozedur Aufruf RPC, Tasks, Überwachen von Client aufrufen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f375a4620e301f59d168bf5f7a4dbeedc0fb89f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856743"
---
# <a name="listening-for-client-calls"></a>Lauschen auf Client Anrufe

Nachdem die Serveranwendung ihre Schnittstellen registriert, die erforderlichen Bindungs Informationen erstellt und ihre Endpunkte registriert hat, ist Sie bereit, mit dem lauschen auf Remote Prozedur Aufrufe von Client Programmen zu beginnen.

Um Remote Prozedur Aufrufe zu lauschen, muss das Serverprogramm [**rpcserverlistener**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten)aufrufen, wie im folgenden Code Fragment gezeigt:


```C++
RPC_STATUS status;
status = RpcServerListen(
    1,
    RPC_C_LISTEN_MAX_CALLS_DEFAULT,
    0);
```



Ein RPC-Server verfügt über einen oder mehrere Threads, die Client Aufrufe abrufen und an die Routinen in den registrierten Schnittstellen übermitteln. Der erste Parameter für die [**rpcserverlauschen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) -Funktion ist die Mindestanzahl der zu erstellenden Threads. Der-Parameter ist nur ein Hinweis. die RPC-Laufzeit kann diese ignorieren.

Der zweite Parameter für [**rpcserverlauschen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) ist die maximale Anzahl von gleichzeitigen Remote Prozedur aufrufen, die verarbeitet werden sollen. Wenn Sie möchten, dass Ihre Anwendung den maximalen Standardwert verwendet, wird der Standardwert für "RPC-C-lauschen (max)" \_ \_ \_ \_ \_ als Wert für diesen Parameter übergeben.

Die DCE-Spezifikation erfordert, dass [**rpcserverlauschen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) weiterhin ausgeführt wird, bis ein Signal zum Abbrechen empfangen wird. Eine Microsoft-Erweiterung für diese Funktion besteht darin, Sie zu aktivieren, um die Überwachung zu starten und sofort zurückzukehren. Wenn Sie möchten, dass Ihre Anwendung das standardmäßige DCE-Verhalten verwendet, legen Sie den dritten Parameter auf 0 (null) fest. Weitere Informationen finden Sie unter [**rpcserverlistener**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening)und [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) .

 

 




