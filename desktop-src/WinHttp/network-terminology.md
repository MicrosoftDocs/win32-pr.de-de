---
description: Beim Entwickeln einer Anwendung, die Microsoft Windows HTTP-Dienste (WinHTTP) verwendet, ist es wichtig, sich mit den folgenden Konzepten und der Terminologie vertraut zu machen, die sich auf das Netzwerk im allgemeinen und insbesondere auf das HTTP-Protokoll beziehen.
ms.assetid: 6ea0c16f-1233-4580-97bb-14e224646857
title: Netzwerkterminologie (WinHTTP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8173b921957a95ebde7f00034c31b2f016b78ab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362316"
---
# <a name="network-terminology-winhttp"></a>Netzwerkterminologie (WinHTTP)

Beim Entwickeln einer Anwendung, die Microsoft Windows HTTP-Dienste (WinHTTP) verwendet, ist es wichtig, sich mit den folgenden Konzepten und der Terminologie vertraut zu machen, die sich auf das Netzwerk im allgemeinen und insbesondere auf das HTTP-Protokoll beziehen.

-   [HTTP-Transaktionen](#http-transactions)
-   [Proxyserver](#proxy-servers)
-   [Synchrone und asynchrone Modi](#synchronous-and-asynchronous-modes)
-   [Authentifizierung](#authentication)

## <a name="http-transactions"></a>HTTP-Transaktionen

Wenn Sie mit HTTP-Transaktionen arbeiten, tauschen Sie Informationen in einem Netzwerk an einem anderen Computer aus. Bei den ausgetauschten Informationen kann es sich um eine Datei handeln, die Text oder Multimedia enthält, oder es kann sich um die Ergebnisse einer Datenbankabfrage handeln. Ein Teil der über ein Netzwerk ausgetauschten Informationen wird als *Ressource* bezeichnet. Normalerweise ist der Computer, der eine Ressource sendet, der Server, und der Computer, der diese Ressource empfängt, ist ein Client. Es ist jedoch auch möglich, dass ein Client Daten an einen-Server sendet. Manchmal umfasst eine HTTP-Transaktion einen Server der mittleren Ebene. Ein Server der mittleren Ebene sammelt mehrere Ressourcen von anderen Servern, kompiliert die Informationen in eine Ressource und sendet diese Ressource an den Client.

Der Vorgang zum Abrufen einer Ressource mithilfe des HTTP-Protokolls erfordert, dass eine Reihe von Nachrichten zwischen dem Client und dem Server ausgetauscht werden. Der Client startet die Transaktion, indem er eine Nachricht sendet, die eine Ressource anfordert. Diese Meldung wird als HTTP-Anforderung oder manchmal nur als Anforderung bezeichnet. Eine HTTP-Anforderung besteht aus den folgenden Komponenten:

-   Methode, Uniform Resource Identifier (URI), Protokoll Versionsnummer
-   Header
-   Entitäts Text

Wenn ein Server eine Anforderung empfängt, sendet er eine Nachricht zurück an den Client. Die vom Server gesendete Nachricht wird als HTTP-Antwort bezeichnet. Eine HTTP-Antwort besteht aus den folgenden Komponenten:

-   Protokoll Versionsnummer, Statuscode, Status Text
-   Header
-   Entitäts Text

Die Antwort gibt entweder an, dass die Anforderung nicht verarbeitet werden kann, oder stellt die angeforderten Informationen bereit. Abhängig vom Typ der Anforderung können dies Informationen zu einer Ressource sein, z. b. Größe und Typ, oder es kann sich um eine oder alle Ressourcen handeln. Der Teil einer Antwort, der einige oder alle der angeforderten Ressource enthält, wird als "Antwortdaten" oder "Entitäts Text" bezeichnet, und die Antwort ist erst dann vollständig, wenn alle Antwortdaten empfangen wurden.

Ausführliche Informationen zu http-Transaktionen und zum HTTP-Protokoll finden Sie unter [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt), Hypertext Transfer Protocol – HTTP/1.1.

## <a name="proxy-servers"></a>Proxyserver

Obwohl eine von einem Client gesendete Anforderung letztendlich vom Zielserver empfangen wird, übergibt die Transaktion manchmal zuerst einen Proxy Server. Ein Proxy fängt die Anforderung ab und kann sogar die Anforderung ändern, bevor Sie an den Server gesendet wird. Wenn der Server antwortet, übergibt die Antwort auch den Proxy, bevor Sie an den Client weitergeleitet wird. Der Proxy kann die Header in dieser Antwort ändern.

Durch das Abfangen und Übersetzen von Netzwerk Transaktionen kann ein Proxy folgende Aktionen ausführen:

-   Schützen Sie den Client, indem Sie potenziell gefährliche Transaktionen überwachen.
-   Ermöglicht es dem Client, mithilfe von Protokollen zu kommunizieren, die von der Client Software möglicherweise nicht implementiert werden.
-   Dient als Gateway zwischen einem privaten Netzwerk und einem öffentlichen Netzwerk.

Die WinHTTP-API enthält ein Proxy Konfigurationstool, das es Ihnen ermöglicht, WinHTTP Informationen zu beliebigen Proxy Servern bereitzustellen, die ihre HTTP-Transaktionen abfangen. Weitere Informationen zur Verwendung des Proxy Konfigurationstools finden Sie unter [ProxyCfg.exe, einem Proxy Konfigurationstool](proxycfg-exe--a-proxy-configuration-tool.md).

## <a name="synchronous-and-asynchronous-modes"></a>Synchrone und asynchrone Modi

Es gibt zwei Programmier Modelle zum Abrufen von Ressourcen über ein Netzwerk mithilfe von WinHTTP – das synchrone und asynchrone Modell. In einem synchronen Modell wird ein Aufrufvorgang oder eine Methode nicht beendet, bis der angeforderte Vorgang abgeschlossen ist oder ein Fehler auftritt. Wenn Ihre Anwendung z. b. eine Ressource mit WinHTTP synchron anfordert, wird der nächste Schritt erst fortgesetzt, wenn die angeforderten Daten empfangen wurden.

Ein asynchrones Modell ermöglicht hingegen einer Anwendung, andere Aufgaben auszuführen, während Sie darauf wartet, dass die Ressource abgerufen wird. Wenn eine andere WinHTTP-Funktion oder-Methode aufgerufen wird und ein vorheriger Vorgang nicht abgeschlossen wurde, gibt die Funktion einen Fehler zurück. Bei der asynchronen Verwendung von WinHTTP sind Component Object Model (com)-Ereignisse und-Rückruf verfügbar, um eine Anwendung über den Fortschritt in einem http-Vorgang zu benachrichtigen.

## <a name="authentication"></a>Authentifizierung

Die Authentifizierung ist der Prozess, mit dem ein HTTP-Proxy oder http-Server die Anmelde Informationen eines Benutzers überprüft, bevor er den Zugriff auf Ressourcen zulässt. Verschiedene Authentifizierungs Schemas werden im Internet verwendet. In der Regel werden der Name und das Kennwort eines Benutzers mit einer autorisierten Liste verglichen, und wenn das System eine Entsprechung erkennt, wird der Zugriff auf den in der Berechtigungs Liste für den Benutzer angegebenen Wertebereich gewährt.

WinHTTP-Funktionen unterstützen die Server-und Proxy Authentifizierung für HTTP-Sitzungen. WinHTTP unterstützt die folgenden Authentifizierungs Schemas: Basic, Digest (siehe [RFC 2617](https://www.ietf.org/rfc/rfc2617.txt)), [NTLM-Authentifizierung](../com/ntlmssp.md), aushandeln/ [Kerberos](../com/kerberos-v5-protocol.md)und Microsoft Passport 1,4. Ausführliche Informationen zur Authentifizierung sowie ein Beispiel für die Verwendung der Authentifizierung in einer Microsoft Visual C++-Anwendung finden Sie unter [Authentifizierung in WinHTTP](authentication-in-winhttp.md).

Informationen zu Sicherheitsüberlegungen bezüglich der Basic-und Passport-Authentifizierung finden Sie unter [WinHTTP-Sicherheitsüberlegungen](winhttp-security-considerations.md).

 

 
