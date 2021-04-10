---
description: Die Socketfunktion erstellte Sockets mit dem überlappenden Attribut, das standardmäßig im ersten Wsock32.dll festgelegt ist, der 32-Bit-Version von Windows Sockets 1,1.
ms.assetid: 2ebf71fd-fcb3-4f2f-bf52-14cd13af012f
title: Standardzustand für das überlappende Attribut eines Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11bc46fbf08731b0f73d841291f6815b43d02785
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129204"
---
# <a name="default-state-for-a-sockets-overlapped-attribute"></a>Standardzustand für das überlappende Attribut eines Sockets

Die [**Socketfunktion**](/windows/desktop/api/Winsock2/nf-winsock2-socket) erstellte Sockets mit dem überlappenden Attribut, das standardmäßig im ersten Wsock32.dll festgelegt ist, der 32-Bit-Version von Windows Sockets 1,1. Um die Abwärtskompatibilität mit aktuell bereitgestellten Wsock32.dll-Implementierungen sicherzustellen, ist dies auch bei Windows Sockets 2 der Fall. Das heißt, dass in Windows Sockets 2 Sockets, die mit der **Socket** -Funktion erstellt werden, über das überlappende Attribut verfügen. Um jedoch kompatibler mit dem Rest der Windows-API zu sein, haben Sockets, die mit [**wsasocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) erstellt werden, standardmäßig das überlappende Attribut. Dieses Attribut wird nur angewendet, wenn das überlappende WSA- \_ Flag \_ festgelegt ist.

 

 



