---
title: Verwenden von http als RPC-Transport
description: RPC-über-HTTP ermöglicht Client Programmen die Verwendung des Internets zum Ausführen von Prozeduren, die von Serverprogrammen in entfernten Netzwerken bereitgestellt werden.
ms.assetid: b5062d70-7625-4a9f-a8c1-025ef8342fcb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5860757a6c5df9937e77fc078df2526affb967fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471365"
---
# <a name="using-http-as-an-rpc-transport"></a>Verwenden von http als RPC-Transport

RPC-über-HTTP ermöglicht Client Programmen die Verwendung des Internets zum Ausführen von Prozeduren, die von Serverprogrammen in entfernten Netzwerken bereitgestellt werden. RPC-über-HTTP-Tunnel durch einen eingerichteten HTTP-Port. Daher können die zugehörigen Aufrufe Netzwerk Firewalls sowohl in den Client-als auch in den Server Netzwerken überschreiten.

RPC-über-HTTP leitet die Aufrufe an den RPC-Proxy weiter, der sich im Netzwerk des RPC-Servers befindet. Der RPC-Proxy stellt eine Verbindung mit dem RPC-Server her und verwaltet diese. Er dient als Proxy, der Remote Prozedur Aufrufe an den RPC-Server sendet und die Antwort des Servers über das Internet an die Client Anwendung sendet. Dieser Vorgang wird in der folgenden Abbildung veranschaulicht.

![Interaktion zwischen einem RPC-Server und einem Internet Informationsserver für RPC http](images/httprpc1.png)

Das Diagramm zeigt eine Firewall im Netzwerk der Client Anwendung. Dies ist für den Betrieb von RPC-über-HTTP nicht erforderlich. Wenn das Client Netzwerk jedoch über eine Firewall verfügt, wird auch ein Proxy Serverprogramm wie Microsoft Proxy Server benötigt.

Wenn das Client Programm einen Remote Prozedur Aufruf mithilfe von http als Transport ausgibt, kontaktiert die RPC-Lauf Zeit Bibliothek auf dem Client den RPC-Proxy. Abhängig davon, ob der RPC-Client zur Verwendung von http oder HTTPS (http mit SSL) aufgefordert wurde, wird Port 80 bzw. Port 443 verwendet. Der RPC-Proxy kontaktiert das RPC-Serverprogramm und stellt eine TCP/IP-Verbindung her. Der Client und der RPC-Proxy behalten ihre http-oder HTTPS-Verbindung über das Internet bei. Die http-oder HTTPS-Verbindung des Clients mit dem RPC-Proxy kann eine Firewall (abhängig von den entsprechenden Zugriffsberechtigungen) durchlaufen, sofern eine vorhanden ist. Der Server kann dann den Remote Prozedur Aufruf ausführen und die Verbindung über den RPC-Proxy verwenden, um an den Client zu antworten. Der RPC-Proxy ist eine ISAPI-Erweiterung, die im Kontext von IIS ausgeführt wird.

Wenn der Client oder der Server aus irgendeinem Grund die Verbindung trennt, wird er vom RPC-Proxy erkannt und die RPC-Sitzung beendet. Solange die Sitzung fortgesetzt wird, behält der RPC-Proxy seine Verbindungen mit dem Client und dem Server bei. Remote Prozedur Aufrufe werden vom Client an den Server weiterleiten und Antworten vom Server an den Client gesendet.

Das RPC-Client Programm kann seine RPC-Aufrufe über das Internet Tunneln, indem er eine Zeichen folgen Bindung im folgenden Format erstellt:

``` syntax
[object_uuid@]ncacn_http:rpc_server[endpoint,HttpProxy=proxy_server:http_port,RpcProxy=rpc_proxy:rpc_port,HttpConnectionOption=UseHttpProxy]
```

Hierbei gilt:

-   *Objekt \_ UUID* gibt eine RPC-Objekt-UUID an. Weitere Informationen finden Sie unter [generierende Schnittstelle UUIDs](generating-interface-uuids.md) und [Zeichenfolge UUID](string-uuid.md).
-   **ncacn \_ http** wählt die Protokoll Sequenz Spezifikation für RPC über HTTP aus. Weitere Informationen finden Sie unter [Protokoll Sequenz Konstanten](protocol-sequence-constants.md) und [Zeichen folgen Bindung](string-binding.md).
-   der *RPC- \_ Server* ist die Netzwerkadresse des Computers, auf dem der RPC-Server Prozess ausgeführt wird. Die Server Adresse muss in einem Formular angegeben werden, das vom RPC-Proxy Computer, nicht vom-Client, sichtbar und verständlich ist. Da der Client keine direkte Verbindung mit dem Server herstellt, muss er nicht in der Lage sein, den Namen des Servers aufzulösen oder eine Verbindung mit ihm herzustellen. Der RPC-Proxy stellt die Verbindung im Auftrag des Clients her, und aus diesem Grund muss der *RPC- \_ Server* ein Name sein, der vom RPC-Proxy erkannt werden kann.
-   *Endpunkt* gibt den TCP/IP-Port an, den der RPC-Server Prozess für Remote Prozedur Aufrufe überwacht. Weitere Informationen finden Sie untersuchen von [Endpunkten](finding-endpoints.md).
-   **Httpproxy** gibt optional einen HTTP-Proxy Server im Netzwerk des RPC-Clients an, z. b. Microsoft Proxy Server. Wenn ein Proxy Server ausgewählt ist, wird keine Portnummer angegeben. der RPC-Stub verwendet standardmäßig Port 80, wenn SSL nicht angefordert wird, und Port 443, wenn SSL angegeben wird.
-   **RpcProxy** gibt die Adresse und die Portnummer des IIS-Computers an, der als Proxy für den RPC-Server fungiert. Sie müssen dies nur angeben, wenn der RPC-Server Prozess sich auf einem anderen Computer als der RPC-Proxy befindet. Wenn Sie keine Portnummer angeben, verwendet der Client-Stub für den RPC-Client standardmäßig Port 80, wenn SSL nicht angegeben ist, und verwendet Port 443, wenn SSL (HTTPS) angegeben wird.
-   **Httpconnectionoption** ermöglicht optional das RPC-Verhalten beim Herstellen von http-Verbindungen. Der **usehttpproxy** -Wert weist RPC an, den Datenverkehr jederzeit über den HTTP-Proxy zu leiten. Dies gilt auch, wenn der Client seine Internetoptionen in Internet Explorer auf "Proxy Server für lokale Adressen umgehen" festgelegt hat.

    Diese Option wird unter Windows 7, Windows Server 2008 R2, Windows 8.1 und Windows Server 2012 R2 mit installiertem KB2916915 unterstützt. Diese Option wird unter Windows 8 und Windows Server 2012 nicht unterstützt. Anwendungen können bestimmen, ob diese Option von der RPC-Laufzeit unterstützt wird, indem Sie den Registrierungs Wert **connectionoptionsflag** unter dem folgenden Registrierungsschlüssel überprüfen:

    **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ RPC**

    Wenn das Bit 0 (LSB) dieses Registrierungs Werts festgelegt ist, wird diese spezielle Option unterstützt. Andernfalls wird diese Option von der RPC-Laufzeit im System nicht unterstützt.

Weitere Informationen zum Erstellen von Zeichen folgen Bindungen finden Sie unter [Bindung und Handles](binding-and-handles.md).

Das RPC-Serverprogramm kann getunnerte RPC-Aufrufe akzeptieren, indem er die HTTP-Protokoll Sequenz von ncacn abhört \_ .

Microsoft verfügt über zwei Haupt Implementierungen von RPC über http: Version 1 und Version 2.

Version 1 (RPC über HTTP v1) wird durch Windows XP unterstützt. Version 1 des RPC-Proxys wird über Windows 2000 unterstützt.

Version 2 (RPC-über-HTTP v2) ist die aktuelle Version.

Die beiden Versionen verfügen über unterschiedliche Funktionen und eine eingeschränkte Interoperabilität. Eine Zusammenfassung der Unterschiede finden Sie hier. Überlegungen zur Interoperabilität finden Sie unter [System Anforderungen und Interoperabilität für RPC über HTTP](system-requirements-and-interoperability-for-rpc-over-http.md).

-   RPC über HTTP v1 erfordert, dass SSL-Tunnelung für alle HTTP-Proxys/Firewalls zwischen dem RPC-über-HTTP-Client und dem RPC-Proxy aktiviert ist. RPC über HTTP v1 versucht, einen SSL-Tunnel über Port 80 zu erstellen, auch wenn die gesendeten Daten nicht tatsächlich SSL-verschlüsselt sind. Proxys und Firewalls lehnen diese Anforderungen in der Regel ab, sofern Sie nicht explizit dafür konfiguriert sind RPC-über-HTTP v2 ist nicht erforderlich.
-   RPC-über-HTTP v1 kann keine SSL-Sitzung mit dem RPC-Proxy herstellen. Der RPC über HTTP v2 kann den gesamten RPC-über-HTTP-Datenverkehr innerhalb einer SSL-Sitzung senden. Standardmäßig erfordert v2, dass die Daten innerhalb einer SSL-Sitzung gesendet werden.
-   RPC-über-HTTP v1 kann sich nicht beim RPC-Proxy authentifizieren. RPC-über-HTTP v2 kann authentifiziert werden. Standardmäßig ist für V2 eine Authentifizierung beim RPC-Proxy erforderlich.
-   Der RPC-Proxy v1 funktioniert nicht ordnungsgemäß, wenn der IIS-Computer, auf dem er installiert ist, Teil einer Webfarm ist. Der RPC-Proxy v2 funktioniert ordnungsgemäß, wenn der IIS-Computer, auf dem er installiert ist, Teil einer Webfarm ist.

> [!Note]  
> Wenn Microsoft Internet Explorer auf dem Computer des Client Programms installiert ist und Ihr Client in der Zeichen folgen Bindung keinen **httpproxy** angibt, durchsucht der RPC-Clientstub die Registrierung auf dem Client Computer nach einem **httpproxy** -Eintrag. Wenn eine solche gefunden wird, wird der im Registrierungs Eintrag angegebene Proxy verwendet.

 

Angenommen, Ihr Client Programm muss über das Internet eine Verbindung mit einem RPC-Server auf einem Computer mit dem Namen "Server7.Microsoft.com" herstellen. Nehmen Sie außerdem an, dass der RPC-Proxy auf Major7.Microsoft.com ausgeführt wird. Das RPC-Serverprogramm lauscht an Port 2225. Der Client verwendet die Zeichen folgen Bindung:

``` syntax
ncacn_http:Server7.microsoft.com[2225, RpcProxy=Major7.microsoft.com]
```

Wenn der RPC-Proxy den Servernamen als Server7 auflösen kann, ohne dass ein voll qualifizierter Domänen Name erforderlich ist, können Sie auch Folgendes angeben:

``` syntax
ncacn_http:Server7 [2225, RpcProxy=Major7.microsoft.com]
```

Wenn das Client Netzwerk eine Firewall und einen Internet Proxyserver mit dem Namen myProxy verwendet und Internet Explorer auf dem Client nicht für die Verwendung dieses Proxys konfiguriert ist, müssen Sie die Zeichen folgen Bindung des Clients wie folgt ändern:

``` syntax
ncacn_http:Server7.microsoft.com[,HttpProxy=myproxy:80,RpcProxy=Major7.microsoft.com:80]
```

Dadurch wird der Client angewiesen, eine Verbindung mit dem RPC-Serverprogramm auf Server7.Microsoft.com herzustellen. Dazu verwendet der Client zuerst Port 80 (oder Port 443, wenn SSL verwendet wird), um eine Verbindung mit myProxy herzustellen. Dadurch erhält das Client Programm Zugriff auf das Internet. Über das Internet stellt das Client Programm als nächstes eine Verbindung mit dem RPC-Proxy auf Major7.Microsoft.com her. Der RPC-Proxy stellt eine Verbindung mit dem RPC-Serverprogramm her, das auf Server7.Microsoft.com ausgeführt wird.

Wenn das Client Netzwerk eine Firewall verwendet und der RPC-Proxy nicht direkt erreicht werden kann, um eine schnellere Verbindung herzustellen, kann die Client Zeichenfolgen-Bindung wie folgt geändert werden:

``` syntax
ncacn_http:Server7.microsoft.com[RpcProxy=Major7.microsoft.com:80,HttpConnectionOption=UseHttpProxy]
```

Mit der **httpconnectionoption** können Sie das RPC-Verhalten beim Herstellen von http-Verbindungen weiterleiten. Der **usehttpproxy** -Wert weist RPC an, den Datenverkehr jederzeit über den HTTP-Proxy zu leiten. Dies gilt auch, wenn der Client seine Internetoptionen in Internet Explorer auf "Proxy Server für lokale Adressen umgehen" festgelegt hat. Dadurch wird der Client angewiesen, eine zwangsweise über den HTTP-Proxy eine Verbindung mit dem RPC-Proxy herzustellen. Dies beschleunigt die Zeit, um eine Verbindung herzustellen, da die Verzögerung bei der Suche nach dem RPC-Server unmittelbar vor der Verwendung des HTTP-Proxys umgangen wird.

Wenn die Option **httpconnectionoption** verwendet wird und Internet Explorer auf dem Client nicht für die Verwendung dieses HTTP-Proxys konfiguriert ist, können Verbindungen mit **\_ ungültigen RPC S- \_ \_ Netzwerk \_ Optionen** fehlschlagen.

Die meisten Computer sind heute für das Webbrowser konfiguriert. Daher müssen die meisten Clients den **httpproxy** nicht angeben, da Sie aus den internetkonnektivitätseinstellungen abgerufen werden.

 

 




