---
title: RPC und das Netzwerk
description: In diesem Abschnitt wird erläutert, wie die Netzwerk Zuverlässigkeit bei Verwendung von RPC behandelt wird, und es wird erläutert, wie APIs auf RPC-Ebene in eine Netzwerkaktivität übersetzt werden. Der Abschnitt bezieht sich nur auf die \_ http-Protokoll Sequenzen ncacn IP \_ TCP und ncacn \_ .
ms.assetid: af7c67ea-32af-40b0-b74b-0a339e5088c4
keywords:
- Remote Prozedur Aufruf RPC, bewährte Methoden, RPC und das Netzwerk
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87c0373bb81d9da0bf20eed1fb9f80863604b040
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102095"
---
# <a name="rpc-and-the-network"></a>RPC und das Netzwerk

In diesem Abschnitt wird erläutert, wie die Netzwerk Zuverlässigkeit bei Verwendung von RPC behandelt wird, und es wird erläutert, wie APIs auf RPC-Ebene in eine Netzwerkaktivität übersetzt werden. Der Abschnitt bezieht sich nur auf die HTTP-Protokoll Sequenzen [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp) und [**ncacn \_**](/windows/desktop/Midl/ncacn-http) .

Dieser Abschnitt ist in die folgenden Themen unterteilt:

-   [Entwicklung und Bereitstellung im Netzwerk](development-versus-deployment-in-the-network.md)
-   [Verhindern von Client-Side hängen](preventing-client-side-hangs.md)
-   [Verwalten von Netzwerk Verbindungs Sätzen (Zuordnungen)](managing-network-connection-sets-associations-.md)
-   [Cleanup für Leerlaufverbindung](idle-connection-cleanup.md)
-   [Umgang mit Verbindungsverlust](dealing-with-loss-of-connectivity.md)
-   [Server seitiges Cleanup](server-side-cleanup.md)

 

 