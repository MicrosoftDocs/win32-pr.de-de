---
description: PCs mit Microsoft Windows verfügen häufig über zahlreiche Netzwerkverbindungen, z. b. mehrere Netzwerkschnittstellenkarten (NIC), die mit unterschiedlichen Netzwerken verbunden sind, oder eine physische Netzwerkverbindung und eine DFÜ-Verbindung.
ms.assetid: 73a1999d-0c19-4f9d-8e47-07f819874535
title: Network Location Awareness Service Provider (NLA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91d3b5882b63539ce0299c9d4a2d93dc17ef2576
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129144"
---
# <a name="network-location-awareness-service-provider-nla"></a>Network Location Awareness Service Provider (NLA)

PCs mit Microsoft Windows verfügen häufig über zahlreiche Netzwerkverbindungen, z. b. mehrere Netzwerkschnittstellenkarten (NIC), die mit unterschiedlichen Netzwerken verbunden sind, oder eine physische Netzwerkverbindung und eine DFÜ-Verbindung. Windows Sockets ist in der Lage, verfügbare Netzwerkschnittstellen für einige Zeit aufzulisten, aber bestimmte wichtige Informationen zu Netzwerkverbindungen waren zuvor nicht verfügbar. Hierzu gehören Informationen wie z. b. das logische Netzwerk, an das ein Windows-Computer angefügt ist, oder ob mehrere Schnittstellen mit dem gleichen Netzwerk verbunden sind.

Der Network Location Awareness Service-Anbieter, der üblicherweise als NLA bezeichnet wird, ermöglicht Windows Sockets 2-Anwendungen, das logische Netzwerk zu identifizieren, an das ein Windows-Computer angefügt ist. Außerdem ermöglicht NLA Windows Sockets-Anwendungen zu identifizieren, an welche physische Netzwerkschnittstelle eine bestimmte Anwendung bestimmte Informationen gespeichert hat. NLA wird als generischer Dienstanbieter für Windows Sockets 2-Namensauflösung implementiert.

 

 



