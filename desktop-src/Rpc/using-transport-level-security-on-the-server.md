---
title: Verwenden der Sicherheit auf Transportebene auf dem Server
description: Verwenden der Sicherheit auf Transportebene auf dem Server mit Remoteprozeduraufruf (RPC).
ms.assetid: 8ad86d46-cdc8-44f0-bb56-4d5069f33e64
keywords:
- Rpc für Remoteprozeduraufrufe , Tasks mit Sicherheit auf Transportebene auf dem Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6abd1f072f249336f4804aed56fb1122556596c43286383b763839d988a2406b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010588"
---
# <a name="using-transport-level-security-on-the-server"></a>Verwenden der Sicherheit auf Transportebene auf dem Server

Dieser Abschnitt enthält Diskussionen zur Sicherheit auf Transportebene, unterteilt in die folgenden Themen:

-   [Verwenden Transport-Level Sicherheit auf dem Client](using-transport-level-security-on-the-client.md)

Wenn Sie [ncacn \_ np](/windows/desktop/Midl/ncacn-np) oder [ncalrpc](/windows/desktop/Midl/ncalrpc) als Protokollsequenz verwenden, gibt der Server zum Zeitpunkt der Auswahl der Protokollsequenz einen Sicherheitsdeskriptor für den Endpunkt an. Weitere Informationen zu Protokollsequenzen finden Sie unter [Specifying Protocol Sequences](specifying-protocol-sequences.md). Ihre Anwendung stellt den Sicherheitsdeskriptor als zusätzlichen Parameter (eine Erweiterung der OSF-DCE-Standardparameter) für alle Funktionen zur Verfügung, die mit den Präfixen [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) und [**RpcServerUseAllProtseqs beginnen.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs) Der Sicherheitsdeskriptor steuert, ob ein Client eine Verbindung mit dem Endpunkt herstellen kann.

Jeder Prozess und Thread ist einem Sicherheitstoken zugeordnet. Dieses Token enthält einen Standardsicherheitsdeskriptor, der für alle objekte verwendet wird, die der Prozess erstellt, z. B. den Endpunkt. Wenn Ihre Anwendung beim Aufrufen einer Funktion mit den Präfixen [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) und [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs)keinen Sicherheitsdeskriptor anordnt, wendet die RPC-Laufzeitbibliothek den Standardsicherheitsdeskriptor aus dem Prozesssicherheitstoken auf den Endpunkt an.

Um zu gewährleisten, dass alle Clients auf die Serveranwendung zugreifen können, sollte der Administrator die Serveranwendung in einem Prozess starten, der über eine Standardsicherheitsbeschreibung verfügt, die von allen Clients verwendet werden kann. Im Allgemeinen verfügen nur Systemprozesse über einen Standardsicherheitsdeskriptor.

Weitere Informationen zu diesen Funktionen und den Funktionen [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) und [**RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself).

 

 