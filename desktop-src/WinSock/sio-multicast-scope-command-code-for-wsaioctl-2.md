---
description: Wenn Multicasting verwendet wird, ist es in der Regel erforderlich, den Bereich anzugeben, in dem der Multicast auftreten soll.
ms.assetid: 744b43a8-dd89-4e63-ae3c-5bee72864df7
title: SIO_MULTICAST_SCOPE Befehls Code für WSAIoctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209a43e461907dcded8e59c6ffee9b1376989d6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042009"
---
# <a name="sio_multicast_scope-command-code-for-wsaioctl"></a>SIO- \_ Multicast- \_ Bereichs Befehls Code für WSAIoctl

Wenn Multicasting verwendet wird, ist es in der Regel erforderlich, den *Bereich* anzugeben, in dem der Multicast auftreten soll. Der Bereich wird als die Anzahl der zu deckenden Routing Netzwerksegmente definiert. Ein Bereich von 0 (null) gibt an, dass die Multicast Übertragung nicht bei der Übertragung platziert würde, sondern über Sockets innerhalb des lokalen Hosts verteilt werden könnte. Ein Bereichs Wert von 1 (Standardwert) gibt an, dass die Übertragung in das Netzwerk übertragen wird, ohne Router zu überschreiten. Höhere Bereichs Werte bestimmen die Anzahl von Routern, die möglicherweise überschritten werden. Beachten Sie, dass dies dem Time-to-Live (TTL)-Parameter in IP-Multicasting entspricht.

Die Funktion " [**wsajoinleaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) " wird verwendet, um einen Blattknoten mit der Multipoint-Sitzung zu verknüpfen. Im folgenden finden Sie eine Erläuterung zur Verwendung dieser Funktion.

 

 



