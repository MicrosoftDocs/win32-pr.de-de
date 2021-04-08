---
title: Proxy Server und WinRM
description: Windows-Remoteverwaltung (WinRM) verwendet HTTP und HTTPS zum Senden von Nachrichten zwischen dem Client-und dem Server Computer. Im allgemeinen sendet der WinRM-Client Nachrichten direkt an den WinRM-Server. WinRM-Clients können auch so konfiguriert werden, dass Sie einen Proxy Server verwenden.
ms.assetid: f8137b3a-7704-4b21-a923-6e2692e18d90
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e07bbfebb4c8f0eb9e77a8942d54677b55c60006
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727400"
---
# <a name="proxy-servers-and-winrm"></a>Proxy Server und WinRM

Windows-Remoteverwaltung (WinRM) verwendet HTTP und HTTPS zum Senden von Nachrichten zwischen dem Client-und dem Server Computer. Im allgemeinen sendet der WinRM-Client Nachrichten direkt an den WinRM-Server. WinRM-Clients können auch so konfiguriert werden, dass Sie einen Proxy Server verwenden.

Weitere Informationen finden Sie in den folgenden Abschnitten:

-   [Konfigurieren eines Proxy Servers für WinRM 2,0](#configuring-a-proxy-server-for-winrm-20)
    -   [HTTPS-basierte Proxy Verbindungen](#https-based-proxy-connections)
    -   [HTTP-basierte Proxy Verbindungen](#http-based-proxy-connections)
-   [Konfigurieren eines Proxy Servers für WinRM 1,1 und früher](#configuring-a-proxy-server-for-winrm-11-and-earlier)

## <a name="configuring-a-proxy-server-for-winrm-20"></a>Konfigurieren eines Proxy Servers für WinRM 2,0

WinRM 2,0 unterstützt eine breite Palette von Proxy Konfigurationen. WinRM unterstützt z. b. Proxys für http-und HTTPS-Transporte sowie für authentifizierte und nicht authentifizierte Proxy Server.

### <a name="https-based-proxy-connections"></a>HTTPS-Based von Proxy Verbindungen

Um eine bessere Sicherheit und Verbindungs basierte Affinität zu erzielen, sollte HTTPS als Transportmechanismus verwendet werden.

Wenn für den Proxy Server eine Authentifizierung erforderlich ist, müssen die WinRM-Clients und-Server HTTPS verwenden.

> [!Note]  
> Die Authentifizierung beim Proxy Server ist unabhängig von der Authentifizierung beim Zielserver.

 

### <a name="http-based-proxy-connections"></a>HTTP-Based von Proxy Verbindungen

Wenn keine Proxy Server Authentifizierung erforderlich ist, kann entweder http oder HTTPS für den Transport verwendet werden. HTTP-basierte Verbindungen von einem WinRM-Client zu einem WinRM-Server über einen Proxy Server können jedoch problematisch sein.

Bei der Verwendung von http-basierten Verbindungen können folgende Probleme auftreten:

-   Der Proxy Server unterstützt keine Verbindungs basierte Authentifizierung, was dazu führen kann, dass die Authentifizierung auf dem Zielserver mit einem Fehler vom Typ "Zugriff verweigert" fehlschlägt.
-   Zum Herstellen einer Verbindung mit dem Zielserver und dem Proxy Server sind mehrere Anmelde Informationen erforderlich.
-   HTTP-basierte Proxy Server unterstützen möglicherweise nicht die Fähigkeit, die zugeordneten Client basierten und serverbasierten Verbindungen aufrechtzuerhalten. Wenn der Proxy einen Client nicht stark mit einem Server verbindet und die TCP/IP-Verbindung aufrecht erhält, erhalten nicht authentifizierte Clients möglicherweise Zugriff auf Daten. Die fehlende Verbindungs Affinität kann auch dazu führen, dass die Authentifizierung auf dem Server fehlschlägt.

Wenn http als Transport verwendet werden muss, sollte der Proxy Server die folgende Konfiguration unterstützen, um eine bessere WinRM-Antwort zu erzielen und Zugriffs Verweigerungs Fehler für WinRM-Clients zu verhindern:

-   Unterstützung für HTTP/1.1. HTTP/1.1 ist bei der Zuordnung der Verbindungs Affinität zwischen Client und Server strenger.
-   Verbindungs basierte Authentifizierung für die Authentifizierung von Aushandlungs-, Kerberos-und kredssp-Authentifizierung.

    Die Authentifizierung einer Anforderung erfordert mehrere Roundtrips zwischen Client und Server. Die meisten Aushandlung der Authentifizierung ist fertiggestellt, nachdem der authentifizier Ende Server (WinRM) eine Antwort an den Client gesendet hat, die keine 401-Antwort (nicht autorisiert) ist. Wenn der WinRM-Server eine Antwort an den Client zurückgibt, bei der es sich nicht um eine 401-Antwort handelt, sollte der Proxy die Verbindung nicht schließen.

    Es können mehrere Anforderungs-/Antwort-Paare zwischen Client und Server gesendet werden, bevor die eigentlichen Paketdaten gesendet werden. WinRM 2,0 verwendet die Aushandlungs-und Kerberos-Authentifizierungs Schemas mit Verschlüsselung, wodurch zusätzliche Roundtrips hinzugefügt werden können. Daten können erst an den Server gesendet werden, wenn die Authentifizierung beendet ist.

    Der WinRM-Server gibt eine Antwort auf 200-Ebene zurück, die angibt, dass die Authentifizierung fertiggestellt wurde. HTTP-basierte Proxy Server beenden möglicherweise die Verbindungs basierte Authentifizierungs Affinität und schließen die TCP/IP-Verbindung nach dem Empfang der Antwort auf 200-Ebene vom WinRM-Server. Der abschließende Roundtrip vom Client zum Server enthält nicht das ursprüngliche Anforderungspaket. Wenn die Verbindung vom Proxy Server geschlossen wird, versucht der Server, den Client erneut zu authentifizieren, und die Client Anforderung wird möglicherweise nie an den Server gesendet. Wenn die Verbindungs basierte Affinität nicht beibehalten wird, kann die Authentifizierung beim Zielserver mit einem Fehler vom Typ "Zugriff verweigert" fehlschlagen.

-   Verbindungs Persistenz. Die TCP/IP-Client Verbindung mit dem Proxy sollte weiterhin derselben TCP/IP-Verbindung vom Proxy zum Server zugeordnet werden. Die Beibehaltung dieser Verbindung sorgt für eine höhere Leistung. Wenn die Verbindung nicht beibehalten wird, muss jede Anforderung erneut authentifiziert werden, was sich auf die Leistung auswirken kann.

### <a name="encryption-and-winrm-20"></a>Verschlüsselung und WinRM 2,0

WinRM 2,0 unterstützt die Verschlüsselung über HTTP mithilfe der Authentifizierungs Schemas aushandeln, Kerberos und kredssp. Wenn ein WinRM-Server HTTP unterstützt und über einen Proxy darauf zugegriffen wird, muss der WinRM-Server die Verschlüsselung erzwingen und unverschlüsselten Netzwerk Datenverkehr nicht zulassen.

Unter keinen Umständen sollten unverschlüsselte HTTP-Anforderungen über Proxy Server gesendet werden. Wenn Daten über einen Proxy Server übergeben werden müssen, bevor Sie an den Zielserver gesendet werden, sind die folgenden Sicherheitsprobleme sehr wichtig:

-   Es ist möglich, dass ein böswilliger Proxy Server jedes Anforderungs-/Antwort-Paar einschließlich Anmelde Informationen untersucht.
-   Wenn die TCP/IP-Verbindungen zwischen dem WinRM-Client und dem Proxy Server sowie zwischen dem Proxy Server und dem Zielserver nicht stark zugeordnet sind, könnte ein nicht autorisierter Client eine Verbindung mit dem Zielserver herstellen, indem er die gleiche authentifizierte Verbindung vom Proxy Server zum Zielserver verwendet. Der Zielserver gestattet dem nicht authentifizierten Client möglicherweise den Zugriff auf Daten. Wenn die Verschlüsselung erzwungen wird, sendet der Zielserver eine Meldung vom Typ "Zugriff verweigert" an den nicht authentifizierten Client.

Die Verwendung der Verschlüsselung würde diese potenziellen Sicherheitsprobleme mindern.

## <a name="configuring-a-proxy-server-for-winrm-11-and-earlier"></a>Konfigurieren eines Proxy Servers für WinRM 1,1 und früher

Wenn ein Proxy erforderlich ist, um den WinRM-Server zu erreichen, benötigt der WinRM-Client die Windows HTTP-Dienste (WinHTTP)-Proxykonfiguration. WinHTTP ist standardmäßig nicht für die Verwendung eines Proxy Servers konfiguriert. Die WinHTTP-Proxykonfiguration kann mit den Befehlszeilen Programmen [ProxyCfg.exe](/previous-versions/windows/desktop/ms761351(v=vs.85)) oder [netsh](/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)) geändert werden.

**WinRM 1,1 und früher:** WinRM verwendet die Internet Explorer-Proxy Einstellungen nicht.

 

 