---
description: Die Windows Sockets 2 (Winsock)-Architektur ist mit der Windows Open System Architecture (WOSA) kompatibel.
ms.assetid: d4cf1462-2e83-49a5-b698-350ff37aa497
title: Architektur von Windows Sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae85ad58a4206d75144e47662bd563fb3235eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130416"
---
# <a name="windows-sockets-2-architecture"></a>Architektur von Windows Sockets 2

Die Windows Sockets 2-Architektur ist mit der Windows Open System Architecture (WOSA) kompatibel, wie unten dargestellt:

![Architektur von Windows Sockets 2](images/ovrvw2-1.png)

Winsock definiert eine Standard-Service Provider Interface (SPI) zwischen der Anwendungsprogrammierschnittstelle (Application Programming Interface, API), deren Funktionen aus ws2 \_32.dll und den Protokoll Stapeln exportiert werden. Folglich ist die Winsock-Unterstützung nicht auf TCP/IP-Protokollstapel beschränkt, wie es bei Windows Sockets 1,1 der Fall ist.

Mit der Windows Sockets 2-Architektur ist es nicht notwendig oder wünschenswert, dass Stack-Anbieter eine eigene Implementierung von ws2-32.dll bereitstellen \_ , da ein einzelner ws2 \_32.dll in allen Stapeln funktionieren muss. Die ws2 \_ -32.dll und Kompatibilitäts-Shims sollten auf die gleiche Weise wie eine Betriebssystem Komponente angezeigt werden.

 

 



