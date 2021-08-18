---
title: Verwenden von HTTP als RPC-Transport
description: RPC-over-HTTP ermöglicht Clientprogrammen die Verwendung des Internets zum Ausführen von Prozeduren, die von Serverprogrammen in entfernten Netzwerken bereitgestellt werden.
ms.assetid: b5062d70-7625-4a9f-a8c1-025ef8342fcb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8775aab1771dcc6da9cade97d36c7141d6d66d8bc8172a20c8263ef64b8ed7ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010783"
---
# <a name="using-http-as-an-rpc-transport"></a>Verwenden von HTTP als RPC-Transport

RPC-over-HTTP ermöglicht Clientprogrammen die Verwendung des Internets zum Ausführen von Prozeduren, die von Serverprogrammen in entfernten Netzwerken bereitgestellt werden. RPC über HTTP tunnelt seine Aufrufe über einen eingerichteten HTTP-Port. Daher können die Aufrufe netzwerkübergreifende Firewalls sowohl im Client- als auch im Servernetzwerk ermöglichen.

RPC über HTTP leitet seine Aufrufe an den RPC-Proxy weiter, der sich im Netzwerk des RPC-Servers befindet. Der RPC-Proxy stellt eine Verbindung mit dem RPC-Server her und verwaltet sie. Er dient als Proxy, sendet Remoteprozeduraufrufe an den RPC-Server und sendet die Antworten des Servers über das Internet an die Clientanwendung zurück. Dieser Vorgang wird im folgenden Diagramm veranschaulicht.

![Interaktion zwischen einem RPC-Server und einem Internetinformationsserver für RPC-HTTP](images/httprpc1.png)

Das Diagramm zeigt eine Firewall im Netzwerk der Clientanwendung. Dies ist für den Betrieb von RPC über HTTP nicht erforderlich. Wenn das Clientnetzwerk jedoch über eine Firewall verfügt, benötigt es auch ein Proxyserverprogramm wie Microsoft Proxy Server.

Wenn das Clientprogramm einen Remoteprozeduraufruf über HTTP als Transport ausgibt, kontaktiert die RPC-Laufzeitbibliothek auf dem Client den RPC-Proxy. Je nachdem, ob der RPC-Client aufgefordert wurde, HTTP oder HTTPS (HTTP mit SSL) Port 80 bzw. Port 443 zu verwenden. Der RPC-Proxy kontaktiert das RPC-Serverprogramm und stellt eine TCP/IP-Verbindung her. Der Client und der RPC-Proxy verwalten ihre HTTP- oder HTTPS-Verbindung über das Internet. Die HTTP- oder HTTPS-Verbindung des Clients mit dem RPC-Proxy kann eine Firewall (mit entsprechenden Zugriffsberechtigungen) durchlaufen, sofern vorhanden. Der Server kann dann den Remoteprozeduraufruf ausführen und die Verbindung über den RPC-Proxy verwenden, um dem Client zu antworten. Der RPC-Proxy ist eine ISAPI-Erweiterung, die im Kontext von IIS ausgeführt wird.

Wenn der Client oder der Server aus irgendeinem Grund getrennt wird, erkennt der RPC-Proxy die Verbindung und beendet die RPC-Sitzung. Solange die Sitzung fortgesetzt wird, verwaltet der RPC-Proxy seine Verbindungen mit dem Client und dem Server. Sie leitet Remoteprozeduraufrufe vom Client an den Server weiter und sendet Antworten vom Server an den Client.

Das RPC-Clientprogramm kann seine RPC-Aufrufe über das Internet tunneln, indem eine Zeichenfolgenbindung im Format erstellt wird:

``` syntax
[object_uuid@]ncacn_http:rpc_server[endpoint,HttpProxy=proxy_server:http_port,RpcProxy=rpc_proxy:rpc_port,HttpConnectionOption=UseHttpProxy]
```

Hierbei gilt:

-   *Object \_ uuid* gibt eine RPC-Objekt-UUID an. Weitere Informationen finden Sie unter [Generieren von Schnittstellen-UUIDs](generating-interface-uuids.md) und [String UUID.](string-uuid.md)
-   **ncacn \_ http** wählt die Protokollsequenzspezifikation für RPC über HTTP aus. Weitere Informationen finden Sie unter [Protokollsequenzkonstanten](protocol-sequence-constants.md) und [Zeichenfolgenbindung.](string-binding.md)
-   *rpc \_ server* ist die Netzwerkadresse des Computers, der den RPC-Serverprozess ausführt. Die Serveradresse muss in einem vom RPC-Proxycomputer sichtbaren und verständlichen Formular angegeben werden, nicht vom Client. Da der Client keine direkte Verbindung mit dem Server herstellt, muss er nicht in der Lage sein, den Namen des Servers aufzulösen oder eine Verbindung mit ihm herzustellen. Der RPC-Proxy stellt die Verbindung im Namen des Clients her. Daher muss *der \_ RPC-Server* ein Name sein, der vom RPC-Proxy erkannt werden kann.
-   *endpoint* gibt den TCP/IP-Port an, auf den der RPC-Serverprozess auf Remoteprozeduraufrufe lauscht. Weitere Informationen finden Sie unter [Suchen von Endpunkten.](finding-endpoints.md)
-   **HttpProxy** gibt optional einen HTTP-Proxyserver im NETZWERK des RPC-Clients an, z. B. Microsoft Proxy Server. Wenn ein Proxyserver ausgewählt ist, wird keine Portnummer angegeben, der RPC-Stub verwendet standardmäßig Port 80, wenn SSL nicht angefordert wird, und Port 443, wenn SSL angegeben ist.
-   **RpcProxy** gibt die Adresse und Portnummer des IIS-Computers an, der als Proxy für den RPC-Server fungiert. Sie müssen dies nur angeben, wenn sich der RPC-Serverprozess auf einem anderen Computer als der RPC-Proxy befindet. Wenn Sie keine Portnummer angeben, verwendet der RPC-Clientstub standardmäßig Port 80, wenn SSL nicht angegeben ist, und Port 443, wenn SSL (HTTPS) angegeben ist.
-   **HttpConnectionOption** ermöglicht ihnen optional, das Verhalten von RPC beim Herstellen von HTTP-Verbindungen zu leiten. Der **UseHttpProxy-Wert** weist RPC an, seinen Datenverkehr jederzeit über den HTTP-Proxy weiterzuleiten. Dies gilt auch, wenn für den Client die Internetoptionen in Internet Explorer auf "Proxyserver für lokale Adressen umgehen" festgelegt sind.

    Diese Option wird auf Windows 7, Windows Server 2008 R2, Windows 8.1 und Windows Server 2012 R2 mit installiertem KB2916915 unterstützt. Diese Option wird für Windows 8 und Windows Server 2012 nicht unterstützt. Anwendungen können ermitteln, ob diese Option von der RPC-Runtime unterstützt wird, indem sie den Registrierungswert **ConnectionOptionsFlag** überprüfen, der sich unter dem folgenden Registrierungsschlüssel befindet:

    **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Rpc**

    Wenn das Bit 0 (LSB) dieses Registrierungswerts festgelegt ist, wird diese spezifische Option unterstützt. Andernfalls wird diese Option von der RPC-Runtime im System nicht unterstützt.

Weitere Informationen zum Erstellen von Zeichenfolgenbindungen finden Sie unter [Bindung und Handles.](binding-and-handles.md)

Das RPC-Serverprogramm kann getunnelte RPC-Aufrufe akzeptieren, indem es an der \_ ncacn-HTTP-Protokollsequenz lauscht.

Microsoft verfügt über zwei Hauptimplementierungen von RPC über HTTP: Version 1 und Version 2.

Version 1 (rpc über HTTP v1 genannt) wird über Windows XP unterstützt. Version 1 des RPC-Proxys wird über Windows 2000 unterstützt.

Version 2 (rpc über HTTP v2 genannt) ist die aktuelle Version.

Die beiden Versionen verfügen über unterschiedliche Funktionen und eingeschränkte Interoperabilität. Eine Zusammenfassung der Unterschiede finden Sie hier. Überlegungen zur Interoperabilität finden Sie unter [Systemanforderungen und Interoperabilität für RPC über HTTP.](system-requirements-and-interoperability-for-rpc-over-http.md)

-   RPC über HTTP v1 erfordert, dass SSL-Tunneling für alle HTTP-Proxys/Firewalls zwischen dem RPC über HTTP-Client und dem RPC-Proxy aktiviert ist. RPC über HTTP v1 versucht, eine SSL-Tunnel über Port 80 zu erstellen, obwohl die gesendeten Daten nicht tatsächlich SSL-verschlüsselt sind. Proxys und Firewalls lehnen solche Anforderungen in der Regel ab, es sei denn, sie sind explizit für deren Zulassen konfiguriert. RPC über HTTP v2 ist nicht erforderlich.
-   RPC über HTTP v1 kann keine SSL-Sitzung mit dem RPC-Proxy herstellen. Der RPC über HTTP v2 kann den gesamten RPC über HTTP-Datenverkehr innerhalb einer SSL-Sitzung senden. v2 erfordert standardmäßig, dass die Daten innerhalb einer SSL-Sitzung gesendet werden.
-   RPC über HTTP v1 kann sich nicht beim RPC-Proxy authentifizieren. RPC über HTTP v2 kann authentifiziert werden. v2 erfordert standardmäßig eine Authentifizierung beim RPC-Proxy.
-   RPC-Proxy v1 funktioniert nicht ordnungsgemäß, wenn der IIS-Computer, auf dem er installiert ist, Teil einer Webfarm ist. RPC-Proxy v2 funktioniert ordnungsgemäß, wenn der IIS-Computer, auf dem er installiert ist, Teil einer Webfarm ist.

> [!Note]  
> Wenn Microsoft Internet Explorer auf dem Computer des Clientprogramms installiert ist und Ihr Client in der Zeichenfolgenbindung keinen **HttpProxy** angibt, durchsucht der RPC-Clientstub die Registrierung auf dem Clientcomputer nach einem **HttpProxy-Eintrag.** Wenn ein Proxy gefunden wird, wird der im Registrierungseintrag angegebene Proxy verwendet.

 

Angenommen, Ihr Clientprogramm muss beispielsweise über das Internet eine Verbindung mit einem RPC-Server auf einem Computer namens Server7.microsoft.com herstellen. Nehmen wir außerdem an, dass der RPC-Proxy auf Major7.microsoft.com ausgeführt wird. Das RPC-Serverprogramm lauscht an Port 2225. Ihr Client würde die Zeichenfolgenbindung verwenden:

``` syntax
ncacn_http:Server7.microsoft.com[2225, RpcProxy=Major7.microsoft.com]
```

Wenn der RPC-Proxy den Servernamen als Server7 auflösen kann, ohne einen vollqualifizierten Domänennamen zu erfordern, können Sie auch Folgendes angeben:

``` syntax
ncacn_http:Server7 [2225, RpcProxy=Major7.microsoft.com]
```

Wenn das Clientnetzwerk eine Firewall und einen Internetproxyserver namens myproxy verwendet und Internet Explorer auf dem Client nicht für die Verwendung dieses Proxys konfiguriert ist, müssen Sie die Zeichenfolgenbindung des Clients in Folgendes ändern:

``` syntax
ncacn_http:Server7.microsoft.com[,HttpProxy=myproxy:80,RpcProxy=Major7.microsoft.com:80]
```

Dadurch wird der Client aufgefordert, eine Verbindung mit dem RPC-Serverprogramm auf Server7.microsoft.com herzustellen. Zu diesem Zwecke verwendet der Client zuerst Port 80 (oder Port 443, wenn SSL verwendet wird), um eine Verbindung mit myproxy herzustellen. Dadurch erhält das Clientprogramm Zugriff auf das Internet. Über das Internet stellt das Clientprogramm als Nächstes eine Verbindung mit dem RPC-Proxy auf Major7.microsoft.com her. Der RPC-Proxy stellt eine Verbindung mit dem RPC-Serverprogramm her, das auf Server7.microsoft.com ausgeführt wird.

Wenn das Clientnetzwerk eine Firewall verwendet und der RPC-Proxy nicht direkt erreicht werden kann, kann die Clientzeichenfolgenbindung in Folgendes geändert werden, um eine Verbindung schneller herzustellen:

``` syntax
ncacn_http:Server7.microsoft.com[RpcProxy=Major7.microsoft.com:80,HttpConnectionOption=UseHttpProxy]
```

**HttpConnectionOption** ermöglicht es Ihnen, das Verhalten von RPC beim Herstellen von HTTP-Verbindungen zu leiten. Der **UseHttpProxy-Wert** weist RPC an, seinen Datenverkehr jederzeit über den HTTP-Proxy weiterzuleiten. Dies gilt auch, wenn für den Client die Internetoptionen in Internet Explorer auf "Proxyserver für lokale Adressen umgehen" festgelegt sind. Dadurch wird der Client aufgefordert, eine verbindung mit dem RPC-Proxy über den HTTP-Proxy zu erzwingen. Dadurch wird die Zeit zum Herstellen einer Verbindung beschleunigt, da jede Verzögerung bei der Suche nach dem RPC-Server direkt vor der Verwendung des HTTP-Proxys umgangen wird.

Wenn die Option **HttpConnectionOption** verwendet wird und Internet Explorer auf dem Client nicht für die Verwendung dieses HTTP-Proxys konfiguriert ist, können Verbindungen mit **RPC S INVALID NETWORK \_ \_ \_ \_ OPTIONS** fehlschlagen.

Die überwiegende Mehrheit der Computer ist heute für Webbrowsen konfiguriert. Daher müssen die meisten Clients den **HttpProxy** nicht angeben, da er aus den Internetkonnektivitätseinstellungen abgerufen wird.

 

 




