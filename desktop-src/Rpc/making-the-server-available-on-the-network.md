---
title: Verfügbar machen des Servers im Netzwerk
description: Bevor eine Serveranwendung Remoteprozeduraufrufe akzeptieren kann, muss sie im Netzwerk verfügbar sein.
ms.assetid: 1fad55e2-7221-4153-b530-b36ea42e03e1
keywords:
- Rpc für Remoteprozeduraufrufe , Aufgaben, die den Server verfügbar machen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55385a1ba10f7f8ca28622af0b145ce25ef1bbbd0ab8df327687ce7fd7db6f77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020054"
---
# <a name="making-the-server-available-on-the-network"></a>Verfügbar machen des Servers im Netzwerk

Bevor eine Serveranwendung Remoteprozeduraufrufe akzeptieren kann, muss sie im Netzwerk verfügbar sein. Dazu gibt der Server der RPC-Laufzeit an, dass er bereit ist, Aufrufe für eine oder mehrere Protokollsequenzen zu akzeptieren. Die Auswahl der Protokollsequenzen, die von einer Serveranwendung unterstützt werden, ist eine wichtige Entscheidung. unterschiedliche Protokollsequenzen verfügen über sehr unterschiedliche Funktionen. Server, die erwarten, dass Aufrufe lokal empfangen werden, sollten **ncalrpc verwenden.** Server, die Remoteaufrufe akzeptieren, sollten **ncacn \_ ip \_ tcp verwenden.** Server sollten nicht überprüfen, ob die Protokollsequenz, für die sie Aufrufe empfangen, die Protokollsequenz ist, für die sie aufrufe erwarten. Weitere Informationen finden Sie unter Warnen vor anderen RPC-Endpunkten, die im selben Prozess ausgeführt werden. Weitere Informationen finden Sie unter Best RPC Programming Practices (Bewährte RPC-Programmiermethoden).

Im folgenden Beispiel wird **ncacn \_ ip \_ tcp verwendet.**

Die meisten Serverprogramme verwenden alle im Netzwerk verfügbaren Protokollsequenzen. Dazu rufen sie die [**RpcServerUseProtseq-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) auf, wie im folgenden Codefragment gezeigt:


```C++
RPC_STATUS status;
status = RpcServerUseAllProtseq(
    L"ncacn_ip_tcp",
    RPC_C_PROTSEQ_MAX_REQS_DEFAULT,    // Protseq dependent parameter
    NULL);                             // Always specify NULL here.
```



Der erste Parameter für die [**RpcServerUseProtseq-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) ist die Protokollsequenz. Der zweite Parameter ist von der Protokollsequenz abhängig. Wie im Codefragment veranschaulicht, legen die meisten Serverprogramme diesen Parameter auf **RPC \_ C \_ PROTSEQ \_ MAX \_ REQS DEFAULT \_ fest.** Dieser Wert legt fest, dass die RPC-Bibliothek den Standardwert verwendet. Der dritte Parameter ist ein Sicherheitsdeskriptor und sollte nicht in Anwendungen verwendet werden. Weitere Informationen finden Sie unter [**Sicherheit.**](security.md)

Sie können auch die [**Funktionen RpcServerUseAllProtseqs,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs) [**RpcServerUseProtseqEx,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep)oder [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) verwenden.

Nachdem eine Serveranwendung mindestens eine Protokollsequenz ausgewählt hat, müssen Server, die dynamische Endpunkte verwenden, Bindungsinformationen für jede von ihr verwendete Protokollsequenz erstellen. Der Server speichert die Bindungsinformationen in einem Bindungsvektor, den er dann in den Endpunktzuordnungsdienst exportieren kann.

Verwenden Sie [**die RpcServerInqBindings-Funktion,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) um einen Bindungsvektor für die Serveranwendung zu erhalten, wie im folgenden Beispiel gezeigt:


```C++
RPC_STATUS status;
RPC_BINDING_VECTOR *rpcBindingVector;
 
status = RpcServerInqBindings(&rpcBindingVector);
```



Der einzige Parameter, der an die [**RpcServerInqBindings-Funktion übergeben**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) wird, ist ein Zeiger auf einen Zeiger auf eine [**RPC BINDING \_ \_ VECTOR-Struktur.**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector) Die RPC-Laufzeitbibliothek ordnet dynamisch ein Array von Bindungsvektoren zu und speichert die Adresse des Arrays in der Parametervariablen (in diesem Fall **rpcBindingVector**). Jede Serveranwendung ist dafür verantwortlich, diesen Bindungsvektor mithilfe der [**RpcBindingVectorFree-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree) frei zu geben, sobald die Verwendung abgeschlossen ist (z. B. nachdem sie ihn an die entsprechenden Funktionen übergeben hat).

 

 




