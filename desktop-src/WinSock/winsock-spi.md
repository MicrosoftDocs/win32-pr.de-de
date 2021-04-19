---
description: Windows Sockets (Winsock) Service Provider Interface (SPI).
ms.assetid: 59ac7ce6-10e7-40ac-bdce-dc01251b0bc5
title: Winsock SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ecf63a45f5175a86b8f5eb2a77ef0293182e38f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349462"
---
# <a name="winsock-spi"></a>Winsock SPI

Die Winsock-Dienstanbieter Schnittstelle oder Winsock SPI ist eine spezialisierte Disziplin von Winsock, die zum Erstellen von Anbietern verwendet wird. Transportanbieter wie TCP/IP-oder IPX/SPX-Protokollstapel verwenden die Winsock SPI, wie auch Namespace Anbieter wie das DNS (Domain Naming System) des Internets.

Herkömmliche Netzwerk Programmierung, z. b. das Aktivieren von Anwendungen für die Kommunikation über das Netzwerk, erfordert keine Verwendung von Winsock SPI-Schnittstellen. Verwenden Sie stattdessen [Winsock](winsock-reference.md) -Standardschnittstellen.

 

Die Winsock-SPI verwendet die folgende funktionspräfix-Benennungs Konvention.



| Präfix | Bedeutung                          | BESCHREIBUNG                                       |
|--------|----------------------------------|---------------------------------------------------|
| WSP    | Windows Sockets-Dienstanbieter | Einstiegspunkte des Transport Dienstanbieters           |
| WPU    | Windows Sockets-Anbieter-uprufe  | Ws2 \_32.dll Einstiegspunkte für Dienstanbieter    |
| WSC    | Windows Sockets-Konfiguration    | Ws2 \_32.dll Einstiegspunkte für Installations-Applets |
| NSP    | Namespace Anbieter               | Einstiegspunkte des Namespace Anbieters                   |



 

 

 



