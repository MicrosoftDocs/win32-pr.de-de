---
title: Verwenden der Sicherheit auf Transport Ebene auf dem Server
description: Verwenden der Sicherheit auf Transport Ebene auf dem Server mit Remote Prozedur Aufruf (RPC).
ms.assetid: 8ad86d46-cdc8-44f0-bb56-4d5069f33e64
keywords:
- Remote Prozedur Aufruf RPC, Tasks, mit Sicherheit auf Transport Ebene auf dem Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39af5b8fb43a57683804eb7b91067ca9faad4390
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473412"
---
# <a name="using-transport-level-security-on-the-server"></a>Verwenden der Sicherheit auf Transport Ebene auf dem Server

In diesem Abschnitt werden die Diskussionen über die Sicherheit auf Transport Ebene erläutert, die in die folgenden Themen unterteilt sind:

-   [Verwenden von Transport-Level Sicherheit auf dem Client](using-transport-level-security-on-the-client.md)

Wenn Sie [ncacn \_ NP](/windows/desktop/Midl/ncacn-np) oder [Ncalrpc](/windows/desktop/Midl/ncalrpc) als Protokoll Sequenz verwenden, gibt der Server beim Auswählen der Protokoll Sequenz eine Sicherheits Beschreibung für den Endpunkt an. Weitere Informationen zu Protokoll Sequenzen finden Sie unter [Angeben von Protokoll Sequenzen](specifying-protocol-sequences.md). Die Anwendung stellt die Sicherheits Beschreibung als zusätzlichen Parameter (eine Erweiterung der standardmäßigen OSF-DCE-Parameter) für alle Funktionen bereit, die mit den Präfixen [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) und [**RpcServerUseAllProtSeqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs)beginnen. Der Sicherheits Deskriptor steuert, ob ein Client eine Verbindung mit dem Endpunkt herstellen kann.

Jedem Prozess und Thread ist ein Sicherheits Token zugeordnet. Dieses Token enthält eine Standard Sicherheits Beschreibung, die für alle Objekte verwendet wird, die vom Prozess erstellt werden, z. b. den-Endpunkt. Wenn die Anwendung keine Sicherheits Beschreibung angibt, wenn eine Funktion mit den Präfixen [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) und [**RpcServerUseAllProtSeqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs)aufgerufen wird, wendet die RPC-Lauf Zeit Bibliothek die Standard Sicherheits Beschreibung vom Prozess Sicherheits Token auf den Endpunkt an.

Um sicherzustellen, dass die Serveranwendung für alle Clients zugänglich ist, sollte der Administrator die Serveranwendung auf einem Prozess starten, der über eine Standard Sicherheits Beschreibung verfügt, die von allen Clients verwendet werden kann. Im Allgemeinen verfügen nur System Prozesse über eine Standard Sicherheits Beschreibung.

Weitere Informationen zu diesen Funktionen und den Funktionen [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) und [**rpkrevertdeself**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself).

 

 