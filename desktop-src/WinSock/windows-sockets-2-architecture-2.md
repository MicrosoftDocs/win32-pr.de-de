---
description: Die Winsock-Architektur (Windows Sockets 2) ist mit der Windows Open System Architecture (WOSA) kompatibel.
ms.assetid: d4cf1462-2e83-49a5-b698-350ff37aa497
title: Windows Sockets 2-Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ad3dd29f692df94e1f66c13c00c75eeca36fb04d18c5f2e95e67b91773698f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569154"
---
# <a name="windows-sockets-2-architecture"></a>Windows Sockets 2-Architektur

Die Windows Sockets 2-Architektur ist mit der Windows Open System Architecture (WOSA) kompatibel, wie unten dargestellt:

![Windows Sockets 2-Architektur](images/ovrvw2-1.png)

Winsock definiert eine STANDARD-Dienstanbieterschnittstelle (SPI) zwischen der Anwendungsprogrammierschnittstelle (APPLICATION PROGRAMMING Interface, API), deren Funktionen aus WS2 \_32.dll und den Protokollstapeln exportiert werden. Daher ist die Winsock-Unterstützung nicht auf TCP/IP-Protokollstapel beschränkt, wie dies bei Windows Sockets 1.1 der Fall ist.

Bei der Windows Sockets 2-Architektur ist es nicht erforderlich oder wünschenswert, dass Stapelanbieter ihre eigene Implementierung von \_ WS2-32.dll bereitstellen, da eine einzelne WS2-32.dll \_ für alle Stapel funktionieren muss. Die \_ WS2-32.dll und Kompatibilitätss shims sollten auf die gleiche Weise wie eine Betriebssystemkomponente angezeigt werden.

 

 



