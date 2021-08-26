---
title: Schnittstelle (RRAS)
description: Eine Schnittstelle ist eine logische Verbindung mit einem Netzwerk. Jede Schnittstelle wird durch einen eindeutigen Index identifiziert. Multicastroutingprotokolle (z. B. MOSPF) behandeln alle Schnittstellentypen auf ähnliche Weise.
ms.assetid: 761a033c-b95e-46f0-948b-d0a60337390f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f1347f1a8d9afd049dd8283e7199c6da7d8a9dce6990a1e7ea674943f32811f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030160"
---
# <a name="interface-rras"></a>Schnittstelle (RRAS)

Eine Schnittstelle ist eine logische Verbindung mit einem Netzwerk. Jede Schnittstelle wird durch einen eindeutigen Index identifiziert. Multicastroutingprotokolle (z. B. MOSPF) behandeln alle Schnittstellentypen auf ähnliche Weise.

Im Fall einer LAN-Schnittstelle entspricht die Schnittstelle einem tatsächlichen physischen Gerät auf dem Computer (dem LAN-Adapter). Im Fall einer WAN-Schnittstelle wird die Schnittstelle einem Port zugeordnet, wenn eine Verbindung hergestellt wird. WAN-Schnittstellen können auf Tunneln basieren, und der Port kann ein VPN-Port (virtuelles privates Netzwerk) sein.

Windows Betriebssystemen 2000 und höher unterstützen eine Punkt-zu-Multipoint-Schnittstelle. Diese Art von Schnittstelle kann als Auflistung von Punkt-zu-Punkt-Links angezeigt werden, die einen einzelnen Beendigungspunkt gemeinsam verwenden.

Um einen genauen Link in einer Point-to-Multipoint-Schnittstelle eindeutig zu identifizieren, verwendet die MGM-API die Adresse des nächsten Hops der Schnittstellen-ID. Um diese Identifizierung zu unterstützen, verwendet die MGM-API eine erweiterte Schnittstellen-ID, die eine Adresse für den [nächsten Hop](next-hop.md) enthält.

 

 




