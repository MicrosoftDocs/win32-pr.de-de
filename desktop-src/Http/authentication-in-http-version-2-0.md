---
title: Authentifizierung (HTTP-Server-API)
description: Ab Version 2.0 führt die HTTP-Server-API die serverseitige Authentifizierung für die Anwendung durch.
ms.assetid: e8e41e8e-1b10-4747-b18e-763e0752ade4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4e3c35dc4e244fd51af42bb3c52d225d233364f61fc79a8127ef450e84016fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078360"
---
# <a name="authentication-http-server-api"></a>Authentifizierung (HTTP-Server-API)

Für einige Serveranwendungen ist eine Clientauthentifizierung erforderlich, um auf Ressourcen und HTTP-Anforderungen des Diensts zuzugreifen. Ab Version 2.0 führt die HTTP-Server-API die serverseitige Authentifizierung für die Anwendung durch. In version 1.0 der HTTP-Server-API musste die Serveranwendung eine eigene Authentifizierung implementieren. Einige Vorteile der Authentifizierung, die von der HTTP-Server-API durchgeführt wird, sind:

-   Anwendungen können mit geringen Berechtigungen ausgeführt werden, wodurch Sicherheitsrisiken reduziert werden.
-   Die Authentifizierung erfolgt im Kernelmodus, wodurch die Übergänge vom Benutzermodus in den Kernelmodus während der Authentifizierung reduziert werden.
-   Die im Kernelmodus ausgeführte Authentifizierung ermöglicht die Ausführung von Serveranwendungen auf verschiedenen Benutzerkonten. In Version 1.0 müssen alle Anwendungen auf dem Computer unter demselben Benutzerkonto ausgeführt werden, um sich beim Dienstprinzipanamen (Service Principle Name, SPN) zu authentifizieren.
-   Der NTLM-Authentifizierungshandshake wird nicht zurückgesetzt, wenn ein Arbeitsprozess wiederverwendet wird, während der Handshake verarbeitet wird.

Um die Version 2.0-Authentifizierung nutzen zu können, aktiviert die Anwendung die Authentifizierungsschemas, die die HTTP-Server-API auf die URLs anwendet, für die die Anwendung registriert wurde. Die Authentifizierung kann für die Serversitzung oder URL-Gruppe aktiviert werden. Die URL-Gruppe erbt die von der Serversitzung aktivierten Authentifizierungsschemas, wenn keine für die URL-Gruppe festgelegt sind. Die HTTP-Server-API unterstützt die folgenden Schemas:

-   Aushandeln
-   NTLM
-   Digest
-   Basic

Die Serveranwendung kann auch Authentifizierungsschemas implementieren, die von der HTTP-Server-API nicht unterstützt werden. Die HTTP-Server-API sendet Anforderungen an die Anwendung für Authentifizierungsschemas, die nicht unterstützt werden, oder für Schemas, die nicht von der Anwendung aktiviert wurden.

### <a name="enabling-authentication"></a>Aktivieren der Authentifizierung

Die Serveranwendung aktiviert und konfiguriert die Authentifizierung in der Serversitzung oder URL-Gruppe mit den Funktionen [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) oder [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) wie folgt:

1.  Die Anwendung ermöglicht die Authentifizierung durch Angabe von **HttpServerAuthenticationProperty** im *Property-Parameter* von [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) oder [**HttpSetUrlGroupProperty.**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
2.  Die Anwendung gibt die Konfigurationsparameter in der [**HTTP \_ SERVER AUTHENTICATION \_ \_ INFO-Struktur**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) im *pPropertyInformation-Parameter* von [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) oder [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)an. Die Anwendung gibt die aktivierten Authentifizierungsschemas an, gibt an, ob das Zwischenspeichern von NTLM-Anmeldeinformationen deaktiviert ist, und stellt die Parameter Basic und Digest in der **HTTP \_ SERVER AUTHENTICATION \_ \_ INFO-Struktur** bereit.

### <a name="authentication-procedure"></a>Authentifizierungsprozedur

Um die HTTP-Serverauthentifizierung zu initiieren, aktiviert die Anwendung die Authentifizierungseigenschaft, bevor die erste Anforderung in der Anforderungswarteschlange eingeht. Die folgenden Schritte sind der allgemeine Verarbeitungsablauf für die Authentifizierung einer Anforderung.

1.  Die Anwendung aktiviert die Authentifizierung. Weitere Informationen finden Sie im vorherigen Abschnitt "Aktivieren der Authentifizierung".
    > [!Note]  
    > Der Client sendet eine nicht authentifizierte Anforderung. Die HTTP-Server-API übergibt die Anforderung an die Serveranwendung und ermöglicht es ihr, die anfängliche 401-Abfrage zu generieren. Die HTTP-Server-API enthält die [**HTTP \_ REQUEST \_ AUTH \_ INFO-Struktur,**](/windows/desktop/api/Http/ns-http-http_request_auth_info) die in die HTTP [**\_ REQUEST-Struktur**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)) eingebettet ist. Das **AuthStatus-Element** gibt **HttpAuthStatusNotAuthenticated** an.

     

2.  Die Anwendung untersucht das **AuthStatus-Element** der [**HTTP REQUEST \_ \_ AUTH \_ INFO-Struktur,**](/windows/desktop/api/Http/ns-http-http_request_auth_info) um zu ermitteln, ob die Anforderung authentifiziert wurde. Wenn die Anforderung nicht authentifiziert wurde, kann die Anwendung die Anforderung anonym bedienen oder eine anfängliche 401-Authentifizierungsaufforderung senden.
3.  Wenn die Anwendung die Anforderung anonym verarbeitet, verarbeitet sie die Anforderung und sendet die endgültige Antwort an die Clientanwendung, so als wäre die Authentifizierung nicht beteiligt.
4.  Wenn die Anwendung stattdessen eine Authentifizierung erfordert, sendet sie die anfängliche 401-Abfrage mit einem oder mehreren WWW-Authenticate-Headern, die die verfügbaren Schemas an den Client angeben. Die Anwendung sollte die [**HTTP \_ MULTIPLE KNOWN \_ \_ HEADERS-Struktur**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) verwenden, um den erforderlichen Satz von Headern zu erstellen, wenn mehr als ein Authentifizierungsheader in der Antwort gesendet wird.
    > [!Note]
    >
    > Der Client übermittelt die Anforderung erneut mit dem Autorisierungsheader für ein Schema, das aus dem Satz verfügbarer Schemas ausgewählt wurde, die von der Serveranwendung in der ersten 401-Antwort angegeben wurden.
    >
    > Die HTTP-Server-API überprüft den Autorisierungsheader der Autorisierungsanforderung, um zu ermitteln, ob das Schema aktiviert ist. Wenn ja, führt die HTTP-Server-API die Authentifizierung durch und verarbeitet alle Austauschvorgänge für Zwischenanforderungen/401-Antworten, bis der Authentifizierungshandshake abgeschlossen ist.
    >
    > Wenn die HTTP-Server-API den Authentifizierungsversuch abschließt, sendet sie die Anforderung mit den Ergebnissen des Authentifizierungsversuchs in der [**HTTP \_ REQUEST \_ AUTH \_ INFO-Struktur,**](/windows/desktop/api/Http/ns-http-http_request_auth_info) die mit der Anforderung zurückgegeben wird, an die Anwendung. Wenn der Authentifizierungsversuch aus einem der folgenden Gründe fehlschlägt, übergibt die HTTP-Server-API die Anforderung nicht an die Anwendung:
    >
    > -   Wenn der Authentifizierungshandshake aufgrund eines internen HTTP-Server-API-Fehlers (z. B. eines Speicherbelegungsfehlers) fehlschlägt, generiert die HTTP-Server-API eine Antwort vom Typ 503 (Dienst nicht verfügbar) und sendet sie zurück an den Client.
    > -   Wenn ein falsch formatiertes Autorisierungsheader wie ein Header ohne Schemaname oder eine falsch formatierte Base64-Codierung von Clientanmeldeinformationen gefunden wird, generiert die HTTP-Server-API eine Antwort vom Typ 400 (ungültige Anforderung) und sendet sie zurück an den Client.

     

5.  Die Serveranwendung untersucht den **AuthStatus-Member** der [**HTTP REQUEST \_ \_ AUTH \_ INFO-Struktur,**](/windows/desktop/api/Http/ns-http-http_request_auth_info) um zu ermitteln, ob die Authentifizierung erfolgreich war. Wenn die Authentifizierung fehlschlägt, enthält die HTTP-Server-API den von [AcceptSecurityContext](/previous-versions/windows/embedded/ms937012(v=msdn.10)) zurückgegebenen Fehler im **SecStatus-Member** der **HTTP REQUEST \_ \_ AUTH \_ INFO-Struktur.** Wenn der Authentifizierungsversuch aufgrund ungültiger Anmeldeinformationen fehlschlägt, kann die Anwendung eine weitere 401-Abfrage mit dem gewünschten WWW-Authenticate-Header generieren oder die Anforderung als anonym behandeln.
6.  Wenn die Authentifizierung erfolgreich war, verwendet die Anwendung das in der [**HTTP \_ REQUEST \_ AUTH \_ INFO-Struktur**](/windows/desktop/api/Http/ns-http-http_request_auth_info) bereitgestellte Token, um die Identität des Clients zu annehmen und auf Ressourcen zuzugreifen. Das an die Anwendung zurückgegebene Zugriffstokenhandle ist gültig, solange die Anforderungs-ID gültig ist, in der Regel, bis die Anwendung die Antwort auf die Anforderung abgeschlossen hat. Das Token kann jedoch während dieses Zeitraums ablaufen, und die Anwendung muss möglicherweise eine weitere 401-Abfrage an den Client senden.
7.  Die Anwendung sendet die letzte 200 OK-Antwort und muss das Handle für das Zugriffstoken schließen.
    > [!Note]  
    > Die HTTP-Server-API fügt die daten zur gegenseitigen Authentifizierung an die letzte 200 OK-Antwort an, wenn eine während des Authentifizierungshandshakes generiert wurde.

     

### <a name="ntlm-null-sessions"></a>NTLM NULL-Sitzungen

Beachten Sie, dass eine NTLM NULL-Sitzung, die im endgültigen Sicherheitskontext angegeben ist, nicht als authentifiziert behandelt wird. In diesem Fall wird die Anforderung mit einem HttpAuthStatusFailure-Fehler in der [**HTTP \_ REQUEST \_ AUTH \_ INFO-Struktur**](/windows/desktop/api/Http/ns-http-http_request_auth_info) an die Anwendung gesendet, und die Anwendung kann eine weitere 401-Abfrage senden.

### <a name="preemptive-authentication"></a>Präemptive Authentifizierung

Gemäß dem HTTP-Protokoll kann der Client, nachdem er die Authentifizierung für eine Ressource eingerichtet hat, präemptiv den entsprechenden Autorisierungsheader mit nachfolgenden aufeinanderfolgenden Anforderungen für die Ressource senden, ohne auf eine 401-Abfrage vom Server zu warten. Wenn das im Autorisierungsheader angegebene Schema weiterhin von der Anwendung aktiviert und von der HTTP-Server-API unterstützt wird, versucht der HTTP-Server die Authentifizierung, ohne die Anforderung an die Anwendung zu senden. Wenn diese Art von authentifizierter Anforderung von der Anwendung empfangen wird, kann sie die Anforderung verwerfen und die anfängliche 401-Abfrage erneut generieren oder die Anforderung als authentifiziert bedienen.

### <a name="mutual-authentication"></a>Gegenseitige Authentifizierung

Gegenseitige Authentifizierungsdaten werden generiert, wenn das Aushandlungsschema während des Handshakes verwendet und in Kerberos aufgelöst wird und der Client zur gegenseitigen Authentifizierung aufgefordert wurde. Die gegenseitigen Authentifizierungsdaten werden automatisch von der HTTP-Server-API in der letzten 200 OK-Antwort eingefügt, die von der Serveranwendung gesendet wird. Standardmäßig übergibt die HTTP-Server-API die Daten der gegenseitigen Authentifizierung nicht an die Serveranwendung, da sie das Senden automatisch verarbeitet. Wenn die Serveranwendung jedoch das ReceiveMutualAuth-Flag in der [**HTTP \_ SERVER AUTHENTICATION \_ \_ INFO-Struktur**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) in der Konfiguration aktiviert, werden die Daten zur gegenseitigen Authentifizierung in der [**HTTP REQUEST \_ \_ AUTH \_ INFO-Struktur,**](/windows/desktop/api/Http/ns-http-http_request_auth_info) die mit der authentifizierten [**\_ HTTP-ANFORDERUNG**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85))eingebettet ist, an die Anwendung übergeben. In diesem Fall sollte die Anwendung die Daten zur gegenseitigen Authentifizierung mit der letzten 200 OK-Antwort senden. Wenn mehrere Standorte von einem einzelnen Computer bedient werden, verwenden alle Standorte auf dem Computer die Anmeldeinformationen für das Lokale Computerkonto in der Domäne für die gegenseitige Authentifizierung.

 

 
