---
description: Bei der Entwicklung einer Anwendung, die Microsoft Windows HTTP Services (WinHTTP) verwendet, ist es wichtig, die folgenden Konzepte und Terminologie zu verstehen, die sich auf Netzwerke im Allgemeinen und das HTTP-Protokoll im Besonderen beziehen.
ms.assetid: 6ea0c16f-1233-4580-97bb-14e224646857
title: Netzwerkterminologie (WinHTTP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bec92d5dd99247fab3ade48760db343983cd7092ea96ac8bd059ed892c9aa42a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643800"
---
# <a name="network-terminology-winhttp"></a>Netzwerkterminologie (WinHTTP)

Bei der Entwicklung einer Anwendung, die Microsoft Windows HTTP Services (WinHTTP) verwendet, ist es wichtig, die folgenden Konzepte und Terminologie zu verstehen, die sich auf Netzwerke im Allgemeinen und das HTTP-Protokoll im Besonderen beziehen.

-   [HTTP-Transaktionen](#http-transactions)
-   [Proxyserver](#proxy-servers)
-   [Synchroner und asynchroner Modus](#synchronous-and-asynchronous-modes)
-   [Authentifizierung](#authentication)

## <a name="http-transactions"></a>HTTP-Transaktionen

Wenn Sie mit HTTP-Transaktionen arbeiten, tauschen Sie Informationen mit einem anderen Computer an anderer Stelle in einem Netzwerk aus. Bei den ausgetauschten Informationen kann es sich um eine Datei mit Text oder Multimedia oder um die Ergebnisse einer Datenbankabfrage handelt. Eine Information, die über ein Netzwerk ausgetauscht wird, wird als Ressource *bezeichnet.* Normalerweise ist der Computer, der eine Ressource sendet, der Server und der Computer, der diese Ressource empfängt, ein Client. Es ist jedoch auch möglich, dass ein Client Daten an einen Server sendet. Manchmal umfasst eine HTTP-Transaktion einen Server der mittleren Ebene. Ein Server der mittleren Ebene sammelt mehrere Ressourcen von anderen Servern, kompiliert die Informationen in eine Ressource und sendet diese Ressource an den Client.

Der Vorgang zum Abrufen einer Ressource mithilfe des HTTP-Protokolls erfordert, dass eine Reihe von Nachrichten zwischen dem Client und dem Server ausgetauscht wird. Der Client beginnt die Transaktion, indem er eine Nachricht sendet, die eine Ressource an fordert. Diese Nachricht wird als HTTP-Anforderung oder manchmal nur als Anforderung bezeichnet. Eine HTTP-Anforderung besteht aus den folgenden Komponenten.

-   Methode, Uniform Resource Identifier (URI), Protokollversionsnummer
-   Header
-   Entitätskörper

Wenn ein Server eine Anforderung empfängt, antwortet er, indem er eine Nachricht zurück an den Client sendet. Die vom Server gesendete Nachricht wird als HTTP-Antwort bezeichnet. Eine HTTP-Antwort besteht aus den folgenden Komponenten.

-   Protokollversionsnummer, Statuscode, Statustext
-   Header
-   Entitätskörper

Die Antwort gibt entweder an, dass die Anforderung nicht verarbeitet werden kann, oder stellt angeforderte Informationen zur Verfügung. Je nach Anforderungstyp kann dies Informationen zu einer Ressource sein, z. B. Größe und Typ, oder es kann sich um einige oder alle Ressourcen selbst geben. Der Teil einer Antwort, der einige oder alle der angeforderten Ressourcen enthält, wird als "Antwortdaten" oder "Entitätskörper" bezeichnet, und die Antwort ist erst abgeschlossen, wenn alle Antwortdaten empfangen wurden.

Ausführliche Informationen zu HTTP-Transaktionen und zum HTTP-Protokoll finden Sie unter [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt), Hypertext Transfer Protocol – HTTP/1.1.

## <a name="proxy-servers"></a>Proxyserver

Obwohl eine von einem Client gesendete Anforderung schließlich vom Zielserver empfangen wird, wird die Transaktion manchmal zuerst über einen Proxyserver übertragen. Ein Proxy fängt die Anforderung ab und kann sie sogar ändern, bevor sie an den Server gesendet wird. Wenn der Server antwortet, durchläuft die Antwort auch den Proxy, bevor er an den Client weitergeleitet wird. Der Proxy kann die Header in dieser Antwort ändern.

Durch das Abfangen und Übersetzen von Netzwerktransaktionen kann ein Proxy:

-   Schützen Sie den Client, indem Sie potenziell gefährliche Transaktionen überwachen.
-   Ermöglichen Sie es dem Client, mithilfe von Protokollen zu kommunizieren, die möglicherweise nicht von der Clientsoftware implementiert werden.
-   Fungieren sie als Gateway zwischen einem privaten und einem öffentlichen Netzwerk.

Die WinHTTP-API enthält ein Proxykonfigurationstool, mit dem Sie WinHTTP Informationen zu allen Proxyservern bereitstellen können, die Ihre HTTP-Transaktionen abfangen. Informationen zur Verwendung des Proxykonfigurationstools finden Sie unter [ProxyCfg.exe, einem Proxykonfigurationstool.](proxycfg-exe--a-proxy-configuration-tool.md)

## <a name="synchronous-and-asynchronous-modes"></a>Synchroner und asynchroner Modus

Es gibt zwei Programmiermodelle zum Abrufen von Ressourcen über ein Netzwerk mit WinHTTP– das synchrone und das asynchrone Modell. In einem synchronen Modell wird ein Aufruf einer Funktion oder Methode erst abgeschlossen, wenn der angeforderte Vorgang abgeschlossen ist oder ein Fehler auftritt. Wenn Ihre Anwendung beispielsweise eine Ressource synchron mit WinHTTP anfragt, wird sie erst mit dem nächsten Schritt fortgesetzt, wenn die angeforderten Daten empfangen wurden.

Ein asynchrones Modell hingegen ermöglicht es einer Anwendung, andere Aufgaben auszuführen, während auf den Abruf der Ressource gewartet wird. Wenn eine andere WinHTTP-Funktion oder -Methode aufgerufen wird und ein vorheriger Vorgang nicht abgeschlossen wurde, gibt die Funktion einen Fehler zurück. Bei asynchroner Verwendung von WinHTTP sind Component Object Model (COM)-Ereignisse und -Rückrufe verfügbar, um eine Anwendung über den Fortschritt eines HTTP-Vorgangs zu benachrichtigen.

## <a name="authentication"></a>Authentifizierung

Die Authentifizierung ist der Prozess, bei dem ein HTTP-Proxy oder HTTP-Server die Anmeldeinformationen eines Benutzers überprüft, bevor er den Zugriff auf Ressourcen zulässt. Im Internet werden verschiedene Authentifizierungsschemas verwendet. Normalerweise werden der Name und das Kennwort eines Benutzers mit einer autorisierten Liste verglichen. Wenn das System eine Übereinstimmung erkennt, wird der Zugriff in dem Umfang gewährt, der in der Berechtigungsliste für den Benutzer angegeben ist.

WinHTTP-Funktionen unterstützen sowohl die Server- als auch die Proxyauthentifizierung für HTTP-Sitzungen. WinHTTP unterstützt die folgenden Authentifizierungsschemas: Basic, Digest (siehe [RFC 2617),](https://www.ietf.org/rfc/rfc2617.txt) [NTLM-Authentifizierung,](../com/ntlmssp.md)Negotiate/Kerberos und Microsoft Passport 1.4. [](../com/kerberos-v5-protocol.md) Ausführliche Informationen zur Authentifizierung sowie ein Beispiel für die Verwendung der Authentifizierung in einer Microsoft Visual C++-Anwendung finden Sie unter [Authentifizierung in WinHTTP.](authentication-in-winhttp.md)

Informationen zu Sicherheitsüberlegungen in Bezug auf die Standard- und Passport-Authentifizierung finden Sie unter [Überlegungen zur WinHTTP-Sicherheit.](winhttp-security-considerations.md)

 

 
