---
title: RPC-über-HTTP-Systemanforderungen, Interoperabilität
description: Microsoft RPC unterstützt RPC über HTTP, wie in der folgenden Tabelle gezeigt.
ms.assetid: 1815315c-1286-4e60-b3a2-a02cb3016fca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 880f078ea481be59448612b5024bbec4d2f54fa5
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/27/2019
ms.locfileid: "104038404"
---
# <a name="rpc-over-http-system-requirements-interoperability"></a>RPC-über-HTTP-Systemanforderungen, Interoperabilität

Microsoft RPC unterstützt RPC über HTTP, wie in der folgenden Tabelle gezeigt.



| Plattform                             | Unterstützt                       | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Server 2003                  | Clients, Server und RPC-Proxy | Unterstützt RPC über HTTP v1 und RPC über HTTP v2-Client und-Server. Der RPC-Proxy unterstützt RPC über HTTP v2, wenn IIS im IIS 6,0-Modus ausgeführt wird. Der RPC-Proxy unterstützt RPC über HTTP v1 und RPC über HTTP v2, wenn IIS im IIS 5,0-Modus ausgeführt wird. Das Ausführen von im IIS 5,0-Modus wird jedoch nicht empfohlen. Weitere Informationen finden Sie unter [RPC-über-HTTP-Bereitstellungs Empfehlungen](rpc-over-http-deployment-recommendations.md) . RPC-über-HTTP-Server und der RPC-Proxy können sich auf unterschiedlichen Computern befinden. |
| Windows XP mit Service Pack 1 (SP1) | Clients und Server            | Unterstützt RPC über HTTP v1 und RPC über HTTP v2-Client und-Server. Der RPC-Proxy wird von nicht unterstützt.                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows XP                           | Clients und Server            | Unterstützt nur RPC über HTTP V1-Client und-Server. Der RPC-Proxy wird von nicht unterstützt.                                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows 2000                         | Clients, Server und RPC-Proxy | RPC-über-HTTP-Serverprogramm und der RPC-Proxy können auf unterschiedlichen Computern ausgeführt werden. RPC-über-HTTP-Client, Server und der RPC-Proxy unterstützen nur RPC über HTTP v1.                                                                                                                                                                                                                                                                                                                   |



 

Außerdem gelten die folgenden Anforderungen:

-   Windows 2000 und höher erfordert die Verwendung von IIS 4,0 oder höher.
-   Der RPC-über-HTTP-Proxy wird nur unter Windows Server-Editionen ausgeführt.
-   Wenn IIS auf einer Server Version von Windows ausgeführt wird, kann das RPC-über-HTTP-Serverprogramm auf jedem Computer ausgeführt werden, für den der RPC-Proxy zum Weiterleiten von Datenverkehr konfiguriert ist. Daher kann Sie auf demselben Computer wie der RPC-Proxy oder auf einem anderen Computer ausgeführt werden.

Damit eine RPC-über-HTTP-Verbindung eingerichtet werden kann, müssen alle RPC-über-HTTP-Clients, RPC-über-HTTP-Server und der RPC-Proxy zustimmen, welche Version von RPC über HTTP verwendet wird. Wenn keine gemeinsame Version von RPC über HTTP vorhanden ist, die für alle drei Unterstützung (Client, Server und RPC-Proxy) verfügbar ist, kann keine RPC-über-HTTP-Verbindung hergestellt werden. In der folgenden Tabelle wird diese Interoperabilität für verschiedene Versionen von RPC über HTTP zusammengefasst.



| RPC-über-HTTP-Client | RPC-Proxy      | RPC-über-HTTP-Server | Funktioniert?                                      | Verwendete Version     |
|----------------------|----------------|----------------------|---------------------------------------------|------------------|
| nur v1              | nur v1        | nur v1              | Ja, mit v1-Einschränkungen                    | RPC über HTTP v1 |
| nur v1              | nur v1        | V1 und v2       | Ja, mit v1-Einschränkungen                    | RPC über HTTP v1 |
| nur v1              | V1 und v2 | nur v1              | Ja, mit v1-Einschränkungen                    | RPC über HTTP v1 |
| nur v1              | V1 und v2 | V1 und v2       | Ja, mit v1-Einschränkungen                    | RPC über HTTP v1 |
| nur v1              | nur v2        | nur v1              | Nein                                          |                  |
| nur v1              | nur v2        | V1 und v2       | Nein                                          |                  |
| V1 und v2       | nur v1        | nur v1              | Ja, mit v1-Einschränkungen                    | RPC über HTTP v1 |
| V1 und v2       | nur v1        | V1 und v2       | Ja, mit v1-Einschränkungen                    | RPC über HTTP v1 |
| V1 und v2       | V1 und v2 | nur v1              | Ja, mit v1-Einschränkungen                    | RPC über HTTP v1 |
| V1 und v2       | V1 und v2 | V1 und v2       | Ja                                         | RPC über HTTP v2 |
| V1 und v2       | nur v2        | nur v1              | Nein                                          |                  |
| V1 und v2       | nur v2        | V1 und v2       | Ja. Dies ist die empfohlene Konfiguration. | RPC über HTTP v2 |



 

Angenommen, ein Windows 2000-Client, ein Windows Server 2003-Proxy mit IIS, der im IIS 6,0-Modus ausgeführt wird, und ein Windows Server 2003 RPC über HTTP-Server. Die erste Tabelle auf dieser Referenzseite zeigt, dass Windows 2000 nur RPC über HTTP v1 unterstützt. Die gleiche Tabelle zeigt, dass ein Windows Server 2003 mit IIS, der im IIS 6,0-Modus ausgeführt wird, nur RPC über HTTP v2 unterstützt und dass ein Windows Server 2003 RPC over HTTP-Server sowohl RPC über HTTP v1 als auch RPC über HTTP v2 unterstützt. Dieses Szenario wird in Zeile 6 der zweiten Tabelle auf dieser Referenzseite beschrieben, auf der gezeigt wird, dass eine RPC-über-HTTP-Verbindung nicht hergestellt werden kann. Außerdem wird in der zweiten Tabelle angezeigt, dass für dieses Szenario zwei Optionen vorhanden sind:

-   Wenn Sicherheit und Stabilität nicht berücksichtigt werden, kann IIS in den IIS 5,0-Modus gewechselt werden, in dem sowohl RPC über HTTP v1 als auch RPC über HTTP v2 unterstützt wird. Dadurch wird die Einrichtung einer RPC-über-HTTP v1-Verbindung ermöglicht.
-   Aktualisieren Sie den Windows 98-Client auf Windows XP mit SP1, und erhalten Sie die Leistung, Sicherheit und Stabilität einer RPC-über-HTTP v2-Verbindung.

 

 




