---
title: RPC über HTTP-Systemanforderungen, Interoperabilität
description: Microsoft RPC unterstützt RPC über HTTP, wie in der folgenden Tabelle gezeigt.
ms.assetid: 1815315c-1286-4e60-b3a2-a02cb3016fca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefc9019789821499168a76d4d2e02ef485529e08b99c5f0759a19bfb4a46f6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017310"
---
# <a name="rpc-over-http-system-requirements-interoperability"></a>RPC über HTTP-Systemanforderungen, Interoperabilität

Microsoft RPC unterstützt RPC über HTTP, wie in der folgenden Tabelle gezeigt.



| Plattform                             | Unterstützt                       | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Server 2003                  | Clients, Server und RPC-Proxy | Unterstützt RPC über HTTP v1 und RPC über HTTP v2-Client und -Server. Der RPC-Proxy unterstützt RPC über HTTP v2, wenn IIS im IIS 6.0-Modus ausgeführt wird. Der RPC-Proxy unterstützt RPC über HTTP v1 und RPC über HTTP v2, wenn IIS im IIS 5.0-Modus ausgeführt wird. Die Ausführung im IIS 5.0-Modus wird jedoch nicht empfohlen. Weitere Informationen finden Sie [unter RPC over HTTP Deployment Empfehlungen (RPC über HTTP-Bereitstellung Empfehlungen).](rpc-over-http-deployment-recommendations.md) RPC über HTTP-Server und der RPC-Proxy können sich auf verschiedenen Computern befinden. |
| Windows XP mit Service Pack 1 (SP1) | Clients und Server            | Unterstützt RPC über HTTP v1 und RPC über HTTP v2-Client und -Server. Rpc-Proxy wird nicht unterstützt.                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows XP                           | Clients und Server            | Unterstützt nur RPC über HTTP v1-Client und -Server. Rpc-Proxy wird nicht unterstützt.                                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows 2000                         | Clients, Server und RPC-Proxy | RPC über HTTP-Serverprogramm und der RPC-Proxy können auf verschiedenen Computern ausgeführt werden. RPC über HTTP-Client, Server und RPC-Proxy unterstützen nur RPC über HTTP v1.                                                                                                                                                                                                                                                                                                                   |



 

Darüber hinaus gelten folgende Anforderungen:

-   Windows 2000 und höher erfordert die Verwendung von IIS 4.0 oder höher.
-   Der RPC über HTTP-Proxy wird nur auf Windows Servereditionen ausgeführt.
-   Wenn IIS auf einer Serverversion von Windows ausgeführt wird, kann das RPC über HTTP-Serverprogramm auf jedem Computer ausgeführt werden, an den der RPC-Proxy für die Weiterleitung von Datenverkehr konfiguriert ist. Daher kann sie auf demselben Computer wie der RPC-Proxy oder auf einem anderen Computer ausgeführt werden.

Damit eine RPC-über-HTTP-Verbindung hergestellt werden kann, müssen sich der gesamte RPC über HTTP-Client, der RPC über HTTP-Server und der RPC-Proxy darauf einigen, welche Version von RPC über HTTP verwendet wird. Wenn es keine gemeinsame Version von RPC über HTTP gibt, die von allen drei unterstützt wird (Client, Server und RPC-Proxy), kann keine RPC über HTTP-Verbindung hergestellt werden. In der folgenden Tabelle wird diese Interoperabilität für verschiedene Versionen von RPC über HTTP zusammengefasst.



| RPC über HTTP-Client | RPC-Proxy      | RPC über HTTP-Server | Funktioniert?                                      | Verwendete Version     |
|----------------------|----------------|----------------------|---------------------------------------------|------------------|
| Nur v1              | Nur v1        | Nur v1              | Ja, mit v1-Einschränkungen                    | RPC über HTTP v1 |
| Nur v1              | Nur v1        | v1 und v2       | Ja, mit v1-Einschränkungen                    | RPC über HTTP v1 |
| Nur v1              | v1 und v2 | Nur v1              | Ja, mit v1-Einschränkungen                    | RPC über HTTP v1 |
| Nur v1              | v1 und v2 | v1 und v2       | Ja, mit v1-Einschränkungen                    | RPC über HTTP v1 |
| Nur v1              | Nur v2        | Nur v1              | Nein                                          |                  |
| Nur v1              | Nur v2        | v1 und v2       | Nein                                          |                  |
| v1 und v2       | Nur v1        | Nur v1              | Ja, mit v1-Einschränkungen                    | RPC über HTTP v1 |
| v1 und v2       | Nur v1        | v1 und v2       | Ja, mit v1-Einschränkungen                    | RPC über HTTP v1 |
| v1 und v2       | v1 und v2 | Nur v1              | Ja, mit v1-Einschränkungen                    | RPC über HTTP v1 |
| v1 und v2       | v1 und v2 | v1 und v2       | Ja                                         | RPC über HTTP v2 |
| v1 und v2       | Nur v2        | Nur v1              | Nein                                          |                  |
| v1 und v2       | Nur v2        | v1 und v2       | Ja. Dies ist die empfohlene Konfiguration. | RPC über HTTP v2 |



 

Stellen Sie sich beispielsweise einen Windows 2000-Client, einen Windows Server 2003-Proxy mit IIS im IIS 6.0-Modus und einen Windows Server 2003 RPC über HTTP-Server vor. Die erste Tabelle auf dieser Referenzseite zeigt, dass Windows 2000 nur RPC über HTTP v1 unterstützt. Die gleiche Tabelle zeigt, dass ein Windows Server 2003 mit IIS, der im IIS 6.0-Modus ausgeführt wird, nur RPC über HTTP v2 unterstützt und dass ein Windows Server 2003 RPC über HTTP-Server sowohl RPC über HTTP v1 als auch RPC über HTTP v2 unterstützt. Dieses Szenario wird in Zeile 6 der zweiten Tabelle auf dieser Referenzseite beschrieben, auf der angezeigt wird, dass kein RPC über HTTP-Verbindung hergestellt werden kann. Darüber hinaus zeigt die zweite Tabelle, dass für dieses Szenario zwei Optionen vorhanden sind:

-   Wenn Sicherheit und Stabilität nicht berücksichtigt werden, kann IIS in den IIS 5.0-Modus umgeschaltet werden, in dem sowohl RPC über HTTP v1 als auch RPC über HTTP v2 unterstützt wird. Dies würde die Einrichtung einer RPC-verbindung über HTTP v1 ermöglichen.
-   Aktualisieren Sie den Windows 98-Client auf Windows XP mit SP1, und erhalten Sie die Leistung, Sicherheit und Stabilität einer RPC über HTTP v2-Verbindung.

 

 




