---
title: Lauschen auf Clientaufrufe
description: Nachdem Ihre Serveranwendung ihre Schnittstellen registriert, die erforderlichen Bindungsinformationen erstellt und ihre Endpunkte registriert hat, kann sie mit dem Lauschen auf Remoteprozeduraufrufe von Clientprogrammen beginnen.
ms.assetid: ca9d24ed-0acc-45de-bbb2-761c56745a58
keywords:
- Remoteprozeduraufruf-RPC, Tasks, Lauschen auf Clientaufrufe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f94453a3250cfc1adae72aa0af96297a741beb501839f7f7831e3f88a8c218
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928605"
---
# <a name="listening-for-client-calls"></a>Lauschen auf Clientaufrufe

Nachdem Ihre Serveranwendung ihre Schnittstellen registriert, die erforderlichen Bindungsinformationen erstellt und ihre Endpunkte registriert hat, kann sie mit dem Lauschen auf Remoteprozeduraufrufe von Clientprogrammen beginnen.

Um auf Remoteprozeduraufrufe zu lauschen, muss Ihr Serverprogramm [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten)aufrufen, wie im folgenden Codefragment gezeigt:


```C++
RPC_STATUS status;
status = RpcServerListen(
    1,
    RPC_C_LISTEN_MAX_CALLS_DEFAULT,
    0);
```



Ein RPC-Server verfügt über einen oder mehrere Threads, die Clientaufrufe empfangen und an die Routinen in den registrierten Schnittstellen senden. Der erste Parameter für die [**RpcServerListen-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) ist die Mindestanzahl der zu erstellenden Threads. Der -Parameter ist nur ein Hinweis. Die RPC-Laufzeit kann dies ignorieren.

Der zweite Parameter für [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) ist die maximale Anzahl gleichzeitiger Remoteprozeduraufrufe, die verarbeitet werden müssen. Wenn Ihre Anwendung den Maximalen Standardwert verwenden soll, übergeben Sie RPC \_ C LISTEN MAX CALLS DEFAULT als Wert für diesen \_ \_ \_ \_ Parameter.

Die DCE-Spezifikation ruft [**rpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) auf, damit sie weiter ausgeführt wird, bis ein Signal zum Beenden empfangen wird. Eine Microsoft-Erweiterung für diese Funktion besteht in der Möglichkeit, sofort mit dem Lauschen zu beginnen und zurückzukehren. Wenn Ihre Anwendung das DCE-Standardverhalten verwenden soll, legen Sie den dritten Parameter auf 0 (null) fest. Weitere Informationen finden Sie unter [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening)und [**RpcMgmtWaitServerListen.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten)

 

 




