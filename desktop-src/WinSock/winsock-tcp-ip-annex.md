---
description: In diesem Abschnitt werden TCP/IP-Funktionen (Transmission Control Protocol/Internet Protocol), Datenstrukturen und Steuerelemente beschrieben.
ms.assetid: ff92750b-453e-4328-821c-1098de8e6125
title: Winsock TCP/IP Anhang
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a5cc403f0ff7f7e6b1daeb979ae9b7ec6ab3c3bed455843cec7ae4f43469975
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118822364"
---
# <a name="winsock-tcpip-annex"></a>Winsock TCP/IP Anhang

In diesem Abschnitt werden TCP/IP-Funktionen (Transmission Control Protocol/Internet Protocol), Datenstrukturen und Steuerelemente beschrieben.



| Element          | BESCHREIBUNG                                                                                                                                 |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| Protokollnamen | TCP, UDP                                                                                                                                    |
| BESCHREIBUNG      | Stellt Transportdienste über die IP-Netzwerkebene bereit: UDP für unzuverlässige Datagramme, TCP für zuverlässige, verbindungsorientierte Bytestreams. |
| Adressfamilie   | **AF \_ INET,** **AF \_ INET6**                                                                                                                 |
| Headerdatei      | *Ws2tcpip.h*                                                                                                                                |



 

Es werden zwei grundlegende Arten von Transportdiensten angeboten: unzuverlässige Datagramme (UDP) und reliable connection oriented-byte streams (TCP). Darüber hinaus wird optional ein unformatiertes Socket unterstützt. Unformatierte Sockets ermöglichen einer Anwendung die Kommunikation über andere Protokolle als TCP und UDP wie ICMP. Unformatierte Sockets werden in den **Adressfamilien AF \_ INET** und **AF \_ INET6** mit einigen Einschränkungen unterstützt.

In diesem Abschnitt werden Erweiterungen für Winsock behandelt, die spezifisch für TCP/IP-Protokolle sind. Außerdem werden Aspekte von Winsock-Basisfunktionen beschrieben, die besondere Überlegungen erfordern oder bei verwendung von TCP/IP ein eindeutiges Verhalten aufweisen können.

 

 



