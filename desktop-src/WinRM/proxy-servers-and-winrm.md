---
title: Proxyserver und WinRM
description: Windows Die Remoteverwaltung (WinRM) verwendet HTTP und HTTPS, um Nachrichten zwischen client- und servercomputern zu senden. Im Allgemeinen sendet der WinRM-Client Nachrichten direkt an den WinRM-Server. WinRM-Clients können auch für die Verwendung eines Proxyservers konfiguriert werden.
ms.assetid: f8137b3a-7704-4b21-a923-6e2692e18d90
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 663493f9c3e71e44be000f436ad4573f911652a8e142b77ffab41acbff250b60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112938"
---
# <a name="proxy-servers-and-winrm"></a>Proxyserver und WinRM

Windows Die Remoteverwaltung (WinRM) verwendet HTTP und HTTPS, um Nachrichten zwischen client- und servercomputern zu senden. Im Allgemeinen sendet der WinRM-Client Nachrichten direkt an den WinRM-Server. WinRM-Clients können auch für die Verwendung eines Proxyservers konfiguriert werden.

Weitere Informationen finden Sie in den folgenden Abschnitten:

-   [Konfigurieren eines Proxyservers für WinRM 2.0](#configuring-a-proxy-server-for-winrm-20)
    -   [HTTPS-basierte Proxyverbindungen](#https-based-proxy-connections)
    -   [HTTP-basierte Proxyverbindungen](#http-based-proxy-connections)
-   [Konfigurieren eines Proxyservers für WinRM 1.1 und früher](#configuring-a-proxy-server-for-winrm-11-and-earlier)

## <a name="configuring-a-proxy-server-for-winrm-20"></a>Konfigurieren eines Proxyservers für WinRM 2.0

WinRM 2.0 unterstützt eine Vielzahl von Proxykonfigurationen. WinRM unterstützt beispielsweise Proxys für HTTP- und HTTPS-Transporte sowie für authentifizierte und nicht authentifizierte Proxyserver.

### <a name="https-based-proxy-connections"></a>HTTPS-Based Proxyverbindungen

Zur Besseren Sicherheit und verbindungsbasierten Affinität sollte HTTPS als Transportmechanismus verwendet werden.

Wenn der Proxyserver eine Authentifizierung erfordert, müssen die WinRM-Clients und -Server HTTPS verwenden.

> [!Note]  
> Die Authentifizierung beim Proxyserver ist unabhängig von der Authentifizierung beim Zielserver.

 

### <a name="http-based-proxy-connections"></a>HTTP-Based Proxyverbindungen

Wenn keine Proxyserverauthentifizierung erforderlich ist, können http oder HTTPs für den Transport verwendet werden. HTTP-basierte Verbindungen von einem WinRM-Client zu einem WinRM-Server über einen Proxyserver können jedoch problematisch sein.

Die folgenden Probleme können bei der Verwendung von HTTP-basierten Verbindungen auftreten:

-   Der Proxyserver unterstützt keine verbindungsbasierte Authentifizierung, was dazu führen kann, dass bei der Authentifizierung beim Zielserver ein Fehler aufgrund eines Zugriffs verweigert wird.
-   Es sind mehrere Anmeldeinformationen erforderlich, um eine Verbindung mit dem Zielserver und dem Proxyserver herzustellen.
-   HTTP-basierte Proxyserver unterstützen möglicherweise nicht die Möglichkeit, die zugeordneten clientbasierten und serverbasierten Verbindungen zu verwalten. Wenn der Proxy einen Client nicht stark mit einem Server verlinkt und die TCP/IP-Verbindung verwaltet, erhalten nicht authentifizierte Clients möglicherweise Zugriff auf Daten. Außerdem kann die fehlende Verbindungsaffinität dazu führen, dass die Authentifizierung beim Server fehlschlägt.

Wenn HTTP als Transport verwendet werden muss, sollte der Proxyserver die folgende Konfiguration unterstützen, um eine bessere WinRM-Antwort zu erzielen und Zugriffsfehler für WinRM-Clients zu verhindern:

-   Unterstützung für HTTP/1.1. HTTP/1.1 ist bei der Zuordnung der Verbindungsaffinität zwischen Client und Server strenger.
-   Verbindungsbasierte Authentifizierung für negotiate-, Kerberos- und CredSSP-Authentifizierung.

    Für die Authentifizierung einer Anforderung sind mehrere Roundtrips zwischen Client und Server erforderlich. Die meisten Aushandlung für die Authentifizierung ist abgeschlossen, nachdem der Authentifizierungsserver (WinRM) eine Antwort an den Client sendet, die keine 401-Antwort (Nicht autorisiert) ist. Wenn der WinRM-Server eine Antwort an den Client zurückgibt, die keine 401-Antwort ist, sollte der Proxy die Verbindung nicht schließen.

    Zwischen Client und Server können mehrere Anforderungs-/Antwortpaare gesendet werden, bevor die tatsächlichen Paketdaten gesendet werden. WinRM 2.0 verwendet die Negotiate- und Kerberos-Authentifizierungsschemas mit Verschlüsselung, die zusätzliche Roundtrips hinzufügen können. Daten können erst an den Server gesendet werden, wenn die Authentifizierung abgeschlossen ist.

    Der WinRM-Server gibt eine Antwort auf 200-Ebene zurück, die angibt, dass die Authentifizierung abgeschlossen ist. HTTP-basierte Proxyserver beenden möglicherweise die verbindungsbasierte Authentifizierungsaffinität und schließen die TCP/IP-Verbindung, nachdem sie die Antwort auf 200-Ebene vom WinRM-Server empfangen haben. Der letzte Roundtrip vom Client zum Server enthält nicht das ursprüngliche Anforderungspaket. Wenn der Proxyserver die Verbindung schließt, versucht der Server, den Client erneut zu authentifizieren, und die Clientanforderung wird möglicherweise nie an den Server gesendet. Wenn die verbindungsbasierte Affinität nicht beibehalten wird, kann bei der Authentifizierung beim Zielserver ein Fehler aufgrund eines Zugriffs verweigert werden.

-   Verbindungspersistenz. Die TCP/IP-Clientverbindung mit dem Proxy sollte weiterhin derselben TCP/IP-Verbindung vom Proxy zum Server zuordnen. Die Aufrechterhaltung dieser Verbindung trägt dazu bei, eine höhere Leistung zu erzielen. Wenn die Verbindung nicht aufrechterhalten wird, muss jede Anforderung erneut authentifiziert werden, was sich auf die Leistung auswirken kann.

### <a name="encryption-and-winrm-20"></a>Verschlüsselung und WinRM 2.0

WinRM 2.0 unterstützt die Verschlüsselung über HTTP mithilfe der Authentifizierungsschemas Negotiate, Kerberos und CredSSP. Wenn ein WinRM-Server HTTP unterstützt und über einen Proxy darauf zugegriffen wird, muss der WinRM-Server die Verschlüsselung erzwingen und keinen unverschlüsselten Netzwerkdatenverkehr zulassen.

Unter keinen Umständen sollten unverschlüsselte HTTP-Anforderungen über Proxyserver gesendet werden. Wenn Daten einen Proxyserver passieren müssen, bevor sie an den Zielserver gesendet werden, sind die folgenden Sicherheitsprobleme sehr wichtig:

-   Es ist möglich, dass ein böswilliger Proxyserver jedes Anforderung/Antwort-Paar einschließlich Anmeldeinformationen untersuchen kann.
-   Wenn die TCP/IP-Verbindungen nicht stark zwischen dem WinRM-Client und dem Proxyserver sowie zwischen dem Proxyserver und dem Zielserver zugeordnet sind, kann ein nicht autorisierter Client eine Verbindung mit dem Zielserver herstellen, indem er dieselbe authentifizierte Verbindung vom Proxyserver zum Zielserver verwendet. Der Zielserver erlaubt dem nicht authentifizierten Client möglicherweise den Zugriff auf Daten. Wenn die Verschlüsselung erzwungen wird, sendet der Zielserver eine Zugriffs verweigerte Nachricht an den nicht authentifizierten Client.

Die Verwendung der Verschlüsselung würde diese potenziellen Sicherheitsprobleme minimieren.

## <a name="configuring-a-proxy-server-for-winrm-11-and-earlier"></a>Konfigurieren eines Proxyservers für WinRM 1.1 und früher

Wenn ein Proxy erforderlich ist, um den WinRM-Server zu erreichen, verwendet der WinRM-Client die Proxykonfiguration Windows HTTP-Diensten (WinHTTP). Standardmäßig ist WinHTTP nicht für die Verwendung eines Proxyservers konfiguriert. Die WinHTTP-Proxykonfiguration kann [](/previous-versions/windows/desktop/ms761351(v=vs.85)) mithilfe der BefehlszeilenprogrammeProxyCfg.exe[oder netsh](/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)) geändert werden.

**WinRM 1.1 und früher:** WinRM verwendet nicht die Internet Explorer Proxyeinstellungen.

 

 