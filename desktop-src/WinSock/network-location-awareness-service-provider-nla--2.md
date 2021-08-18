---
description: PCs, auf denen Microsoft Windows ausgeführt werden, verfügen häufig über zahlreiche Netzwerkverbindungen, z. B. mehrere Netzwerkschnittstellenkarten (NIC), die mit verschiedenen Netzwerken verbunden sind, oder eine physische Netzwerkverbindung und eine DFÜ-Verbindung.
ms.assetid: 73a1999d-0c19-4f9d-8e47-07f819874535
title: Network Location Awareness Service Provider (NLA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7378aff6f51f2785671f1d424a4721f9cd77fad22d60554746f9427d7f24f69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132093"
---
# <a name="network-location-awareness-service-provider-nla"></a>Network Location Awareness Service Provider (NLA)

PCs, auf denen Microsoft Windows ausgeführt werden, verfügen häufig über zahlreiche Netzwerkverbindungen, z. B. mehrere Netzwerkschnittstellenkarten (NIC), die mit verschiedenen Netzwerken verbunden sind, oder eine physische Netzwerkverbindung und eine DFÜ-Verbindung. Windows Sockets konnten bereits seit einiger Zeit verfügbare Netzwerkschnittstellen aufzählen, aber bestimmte wichtige Informationen zu Netzwerkverbindungen waren zuvor nicht verfügbar. Dies schließt Informationen wie das logische Netzwerk ein, an das ein Windows Computer angefügt ist oder ob mehrere Schnittstellen mit demselben Netzwerk verbunden sind.

Der Network Location Awareness-Dienstanbieter, der häufig als NLA bezeichnet wird, ermöglicht Windows Sockets 2-Anwendungen, das logische Netzwerk zu identifizieren, an das ein Windows Computer angefügt ist. Darüber hinaus ermöglicht die NLA Windows Sockets-Anwendungen, zu ermitteln, an welcher physischen Netzwerkschnittstelle eine bestimmte Anwendung bestimmte Informationen gespeichert hat. Die NLA wird als generischer Windows Sockets 2-Namensauflösungsdienstanbieter implementiert.

 

 



