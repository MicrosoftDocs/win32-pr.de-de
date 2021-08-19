---
description: Wenn Multicasting verwendet wird, ist es in der Regel erforderlich, den Bereich anzugeben, in dem der Multicast erfolgen soll.
ms.assetid: 744b43a8-dd89-4e63-ae3c-5bee72864df7
title: SIO_MULTICAST_SCOPE Befehlscode für WSAIoctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c38269167aa2ed142440b0e1105600d26c59514f72d749595ce44ecdf3a0998f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117927369"
---
# <a name="sio_multicast_scope-command-code-for-wsaioctl"></a>SIO \_ MULTICAST \_ SCOPE-Befehlscode für WSAIoctl

Wenn Multicasting verwendet wird, ist es in der Regel erforderlich, den *Bereich* anzugeben, in dem der Multicast erfolgen soll. Der Bereich ist definiert als die Anzahl der Routingnetzwerksegmente, die abgedeckt werden sollen. Ein Bereich von 0 (null) gibt an, dass die Multicastübertragung nicht über das Kabel platziert, sondern über Sockets innerhalb des lokalen Hosts verteilt werden könnte. Der Bereichswert 1 (Standard) gibt an, dass die Übertragung an der Verbindung platziert wird, aber keine Router überschreitet. Höhere Bereichswerte bestimmen die Anzahl der Router, die überschritten werden können. Beachten Sie, dass dies dem TTL-Parameter (Time-to-Live) beim IP-Multicasting entspricht.

Die [**Funktion WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) wird verwendet, um einen Blattknoten mit der Multipointsitzung zu verbinden. Im Folgenden wird erläutert, wie diese Funktion verwendet wird.

 

 



