---
title: Systemanforderungen für RPC-Message Queuing-Anwendungen
description: Um den Message Queuing-Transport in einer RPC-Client-/Serveranwendung zu verwenden, müssen auf den Server- und Clientcomputern die entsprechende Betriebssystemplattform und Message Queuing installiert sein.
ms.assetid: f90318a6-0be6-4e1a-a1a5-1709808b5d3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46d9775e720c725ad3b0d06a0be0cf67aa438f739c6a0d1162f4940ac59e561e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924647"
---
# <a name="system-requirements-for-rpc-message-queuing-applications"></a>Systemanforderungen für RPC-Message Queuing-Anwendungen

Um den Message Queuing-Transport in einer RPC-Client-/Serveranwendung zu verwenden, müssen auf den Server- und Clientcomputern die entsprechende Betriebssystemplattform und Message Queuing installiert sein.

Anforderungen für Servercomputer:

-   Microsoft Windows Server 2003, Windows XP oder Windows 2000 oder höher.
-   SQL Server Version 6.5 oder höher.
-   Message Queuing primären Enterprise Controller oder primären Standortcontrollers.
-   SERVERSEITIGE RPC-Transport-DLL (RpcMqSvr.dll).

Anforderungen für Clientcomputer:

-   Microsoft Windows Server 2003, Windows XP oder Windows 2000 oder höher.
-   Microsoft Message Queuing Client.
-   RPC clientseitige Transport-DLL (RpcMqCl.dll).

Wenn die MSMQ-Komponenten auf den Client- und Servercomputern installiert sind, werden die System registrierungen automatisch so konfiguriert, dass sie das [ncadg mq message-queuing-Transportprotokoll \_ ](/windows/desktop/Midl/ncadg-mq) für Remoteprozeduraufrufe enthalten.

Um Ihre RPC-MSMQ-Anwendung zu erstellen, benötigen Sie Folgendes:

-   Microsoft Windows Server 2003, Windows XP oder Windows 2000 oder höher
-   MIDL Version 3.1.76 oder höher.

 

 