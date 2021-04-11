---
description: Clouds werden von den Peer Gruppierungs-und graphinginfrastrukturen verwendet.
ms.assetid: 01327211-0461-4922-925e-67bebe3e6158
title: Clouds
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 743d668387c78b3c22e49e98585494a36506cc74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131696"
---
# <a name="clouds"></a>Clouds

Clouds werden von den Peer [Gruppierungs](grouping-api.md) -und [graphinginfrastrukturen](graphing-api.md) verwendet. Das [Peer Name Resolution-Protokoll (PNRP)](pnrp-namespace-provider-api.md) identifiziert eine Cloud als Gruppe von Peers, die innerhalb desselben IPv6-Bereichs kommunizieren können. Clouds sind eng mit den IPv6-Bereichen verknüpft. In der folgenden Liste sind einige der eindeutigen Cloud-Features aufgeführt:

-   Eine Cloud wird durch einen Namen identifiziert, und die verfügbaren Clouds können mithilfe von [**wsalookupservicebegin**](pnrp-and-wsalookupservicebegin.md)aufgelistet werden.
-   Wenn ein Computer mit dem Internet verbunden ist, ist er Teil einer globalen Cloud, der durch die Zeichenfolge "Global" gekennzeichnet ist \_ .
-   Wenn ein Computer mit einem oder mehreren LAN (Local Area Networks) verbunden ist, sind für jeden Link individuelle Clouds verfügbar.
-   Ein Computer kann mit vielen Netzwerken verbunden werden, indem mehrere Netzwerkadapter oder ein virtuelles privates Netzwerk (VPN) verwendet werden. Dies bedeutet, dass ein Computer mit einer Schnittstelle in vielen Clouds sichtbar sein kann.
-   Sie können PNRP zum Registrieren und Auflösen von Peernamen in einer bestimmten Cloud verwenden.

 

 



