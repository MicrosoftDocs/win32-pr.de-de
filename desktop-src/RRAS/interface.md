---
title: Schnittstelle (RRAS)
description: Eine Schnittstelle ist eine logische Verbindung mit einem Netzwerk. Jede Schnittstelle wird durch einen eindeutigen Index identifiziert. Multicast Routing Protokolle (z. b. "MUF") befassen sich ähnlich mit allen Schnittstellentypen.
ms.assetid: 761a033c-b95e-46f0-948b-d0a60337390f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd1e3988eac75bd465bf9a9b890f360f850a0d7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103949316"
---
# <a name="interface-rras"></a>Schnittstelle (RRAS)

Eine Schnittstelle ist eine logische Verbindung mit einem Netzwerk. Jede Schnittstelle wird durch einen eindeutigen Index identifiziert. Multicast Routing Protokolle (z. b. "MUF") befassen sich ähnlich mit allen Schnittstellentypen.

Im Fall einer LAN-Schnittstelle entspricht die Schnittstelle einem tatsächlichen physischen Gerät auf dem Computer (dem LAN-Adapter). Bei einer WAN-Schnittstelle wird die Schnittstelle einem Port zugeordnet, wenn eine Verbindung hergestellt wird. WAN-Schnittstellen können auf Tunneln basieren, und der Port könnte ein VPN-Port (virtuelles privates Netzwerk) sein.

Windows 2000 und spätere Betriebssysteme unterstützen eine Point-to-Multipoint-Schnittstelle. Diese Art von Schnittstelle kann als eine Auflistung von Punkt-zu-Punkt-Links angezeigt werden, die einen einzelnen Beendigungs Punkt aufweisen.

Zur eindeutigen Identifizierung einer exakten Verknüpfung in einer Punkt-zu-Multipoint-Schnittstelle verwendet die MGM-API die Adresse des nächsten Hops der Schnittstellen-ID. Zur Unterstützung dieser Identifizierung verwendet die MGM-API eine erweiterte Schnittstellen-ID, die eine Adresse für den [nächsten Hop](next-hop.md) enthält.

 

 




