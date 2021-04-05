---
title: Verfügbar machung des Servers im Netzwerk
description: Bevor eine Serveranwendung Remote Prozedur Aufrufe akzeptieren kann, muss Sie im Netzwerk verfügbar sein.
ms.assetid: 1fad55e2-7221-4153-b530-b36ea42e03e1
keywords:
- Remote Prozedur Aufruf RPC, Tasks, Bereitstellen des Servers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ee2826e4e63e7e78e7f87f6afc120b80e885cd3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037170"
---
# <a name="making-the-server-available-on-the-network"></a>Verfügbar machung des Servers im Netzwerk

Bevor eine Serveranwendung Remote Prozedur Aufrufe akzeptieren kann, muss Sie im Netzwerk verfügbar sein. Zu diesem Zweck zeigt der Server der RPC-Laufzeit an, dass er bereit ist, Aufrufe für eine oder mehrere Protokoll Sequenzen zu akzeptieren. Die Auswahl der Protokoll Sequenzen, die eine Serveranwendung unterstützt, ist eine wichtige Entscheidung. verschiedene Protokoll Sequenzen verfügen über sehr unterschiedliche Funktionen. Server, die erwarten, dass Aufrufe lokal empfangen werden, sollten **Ncalrpc** verwenden. Server, die Remote Aufrufe akzeptieren, sollten **ncacn \_ IP \_ TCP** verwenden. Server sollten nicht überprüfen, ob die Protokoll Sequenz, für die Sie Aufrufe empfangen, die Protokoll Sequenz ist, für die Sie erwarten, dass Sie Aufrufe empfangen. Weitere Informationen finden Sie unter warnen von anderen RPC-Endpunkten, die in demselben Prozess ausgeführt werden, bei den Best Practices für die RPC-Programmierung.

Im folgenden Beispiel wird **ncacn \_ IP \_ TCP** verwendet.

In den meisten Serverprogrammen werden alle im Netzwerk verfügbaren Protokoll Sequenzen verwendet. Dazu rufen Sie die [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) -Funktion auf, wie im folgenden Code Fragment gezeigt:


```C++
RPC_STATUS status;
status = RpcServerUseAllProtseq(
    L"ncacn_ip_tcp",
    RPC_C_PROTSEQ_MAX_REQS_DEFAULT,    // Protseq dependent parameter
    NULL);                             // Always specify NULL here.
```



Der erste Parameter für die [**rpcserveruseprotabq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) -Funktion ist die Protokoll Sequenz. Der zweite Parameter ist von der Protokoll Sequenz abhängig. Wie im Code Fragment dargestellt, legen die meisten Serverprogramme diesen Parameter auf **RPC \_ C \_ Protseq \_ Max \_ reqs \_ default** fest. Dieser Wert legt fest, dass die RPC-Bibliothek den Standardwert verwendet. Der dritte Parameter ist eine Sicherheits Beschreibung und sollte nicht in Anwendungen verwendet werden. Weitere Informationen finden Sie unter [**Sicherheit**](security.md).

Sie können auch die Funktionen [**rpcserveruseallprotabqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), [**rpcserveruseprotsqex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex), [**rpcserveruseprotsetqep**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep)oder [**rpcserveruseprotabqepex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) verwenden.

Nachdem eine Serveranwendung mindestens eine Protokoll Sequenz ausgewählt hat, müssen Server, die dynamische Endpunkte verwenden, Bindungs Informationen für jede verwendete Protokoll Sequenz erstellen. Der Server speichert die Bindungs Informationen in einem Bindungs Vektor, den er dann in den Endpunkt Mapper-Dienst exportieren kann.

Verwenden Sie die Funktion [**rpcserverinqbinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) , um einen Bindungs Vektor für die Serveranwendung zu erhalten, wie im folgenden Beispiel gezeigt:


```C++
RPC_STATUS status;
RPC_BINDING_VECTOR *rpcBindingVector;
 
status = RpcServerInqBindings(&rpcBindingVector);
```



Der einzige Parameter, der an die [**rpcserverinqbinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) -Funktion übergeben wird, ist ein Zeiger auf einen Zeiger auf eine [**RPC- \_ Bindungs \_ Vektor**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector) Struktur. Die RPC-Lauf Zeit Bibliothek weist dynamisch ein Array von Bindungs Vektoren zu und speichert die Adresse des Arrays in der Parameter Variablen (in diesem Fall **rpcbindingvector**). Jede Serveranwendung ist dafür verantwortlich, diesen Bindungs Vektor mithilfe der [**rpcbindingvectorfree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree) -Funktion freizugeben, sobald Sie die Verwendung abgeschlossen hat (z. b. Nachdem Sie an die entsprechenden Funktionen übermittelt wurde).

 

 




