---
title: RPC und das Netzwerk
description: In diesem Abschnitt wird erläutert, wie sie mit der Unzuverlässigkeit des Netzwerks umgehen, wenn RPC verwendet wird, und erläutert, wie APIs auf RPC-Ebene in Netzwerkaktivitäten übersetzt werden. Der Abschnitt bezieht sich nur auf die Protokollsequenzen ncacn \_ ip \_ tcp und ncacn \_ http.
ms.assetid: af7c67ea-32af-40b0-b74b-0a339e5088c4
keywords:
- Remoteprozeduraufruf RPC , bewährte Methoden, RPC und das Netzwerk
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 212e1f3b6f281709a3344367a59d858b7f96b77a6adbdc44fc8556769f2edcaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926652"
---
# <a name="rpc-and-the-network"></a>RPC und das Netzwerk

In diesem Abschnitt wird erläutert, wie sie mit der Unzuverlässigkeit des Netzwerks umgehen, wenn RPC verwendet wird, und erläutert, wie APIs auf RPC-Ebene in Netzwerkaktivitäten übersetzt werden. Der Abschnitt bezieht sich nur auf die [**Protokollsequenzen ncacn \_ ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp) und [**ncacn \_ http.**](/windows/desktop/Midl/ncacn-http)

Dieser Abschnitt ist in die folgenden Themen unterteilt:

-   [Entwicklung im Vergleich zur Bereitstellung im Netzwerk](development-versus-deployment-in-the-network.md)
-   [Verhindern von Client-Side Hängen](preventing-client-side-hangs.md)
-   [Verwalten von Netzwerkverbindungssätzen (Zuordnungen)](managing-network-connection-sets-associations-.md)
-   [Leerlaufverbindungsbereinigung](idle-connection-cleanup.md)
-   [Umgang mit Konnektivitätsverlust](dealing-with-loss-of-connectivity.md)
-   [Serverseitige Bereinigung](server-side-cleanup.md)

 

 