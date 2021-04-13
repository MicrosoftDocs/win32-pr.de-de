---
title: System Anforderungen für RPC-Message Queuinganwendungen
description: Damit der Nachrichten Warteschlangen-Transport in einer RPC-Client/Server-Anwendung verwendet werden kann, müssen auf dem Server und den Client Computern die geeignete Betriebssystem Plattform und Message Queuing Software installiert sein.
ms.assetid: f90318a6-0be6-4e1a-a1a5-1709808b5d3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1274c888506a6868eb7ded5ba96c5f1ea8dc8b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390830"
---
# <a name="system-requirements-for-rpc-message-queuing-applications"></a>System Anforderungen für RPC-Message Queuinganwendungen

Damit der Nachrichten Warteschlangen-Transport in einer RPC-Client/Server-Anwendung verwendet werden kann, müssen auf dem Server und den Client Computern die geeignete Betriebssystem Plattform und Message Queuing Software installiert sein.

Folgende Anforderungen gelten für Server Computer:

-   Microsoft Windows Server 2003, Windows XP oder Windows 2000 oder höher.
-   SQL Server Version 6,5 oder höher.
-   Message Queuing primärer Enterprise Controller oder primärer Standort Controller.
-   Serverseitige RPC-Transport-dll (RpcMqSvr.dll).

Anforderungen für Client Computer:

-   Microsoft Windows Server 2003, Windows XP oder Windows 2000 oder höher.
-   Microsoft Message Queuing-Client.
-   Client seitige RPC-Transport-dll (RpcMqCl.dll).

Wenn die MSMQ-Komponenten auf dem Client-und dem Server Computer installiert sind, werden die System Registrierungen automatisch so konfiguriert, dass Sie das [ncadg \_ MQ](/windows/desktop/Midl/ncadg-mq) -Nachrichten Warteschlangen-Transportprotokoll für Remote Prozedur Aufrufe enthalten.

Zum Erstellen der RPC-MSMQ-Anwendung benötigen Sie Folgendes:

-   Microsoft Windows Server 2003, Windows XP oder Windows 2000 oder höher
-   Mittel l Version 3.1.76 oder höher.

 

 