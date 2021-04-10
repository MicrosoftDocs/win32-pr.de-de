---
description: In diesem Abschnitt werden TCP/IP-Funktionen (Transmission Control Protocol/Internet Protocol), Datenstrukturen und Steuerelemente beschrieben.
ms.assetid: ff92750b-453e-4328-821c-1098de8e6125
title: Winsock-TCP/IP-Anhang
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4fd86a016ed80d9c71ac1647323508cb4dc7b08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214985"
---
# <a name="winsock-tcpip-annex"></a>Winsock-TCP/IP-Anhang

In diesem Abschnitt werden TCP/IP-Funktionen (Transmission Control Protocol/Internet Protocol), Datenstrukturen und Steuerelemente beschrieben.



| Element          | BESCHREIBUNG                                                                                                                                 |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| Protokoll Name (n) | TCP, UDP                                                                                                                                    |
| BESCHREIBUNG      | Stellt Transportdienste über die IP-Netzwerkschicht bereit: UDP für unzuverlässige Datagramme, TCP für zuverlässige, Verbindungs orientierte Byte Datenströme. |
| Adressfamilie   | **AF \_ INET**, **AF \_ inet6**                                                                                                                 |
| Headerdatei      | *Ws2tcpip. h*                                                                                                                                |



 

Es werden zwei grundlegende Arten von Transportdiensten angeboten: unzuverlässige Datagramme (UDP) und zuverlässige Verbindungs orientierte – Byte Datenströme (TCP). Außerdem wird optional ein RAW-Socket unterstützt. Mit unformatierten Sockets kann eine Anwendung über andere Protokolle als TCP und UDP, wie z. b. ICMP, kommunizieren. Unformatierte Sockets werden von **der \_ AF** -und der **AF \_ inet6** -Adressfamilie mit einigen Einschränkungen unterstützt.

In diesem Abschnitt werden die für TCP/IP-Protokolle spezifischen Erweiterungen von Winsock behandelt. Außerdem werden Aspekte von Basis-Winsock-Funktionen beschrieben, die besondere Überlegungen erfordern oder bei der Verwendung von TCP/IP das einmalige Verhalten aufweisen können.

 

 



