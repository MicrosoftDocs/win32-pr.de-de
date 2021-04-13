---
title: Authentifizierung (http-Server-API)
description: Ab Version 2,0 führt die HTTP-Server-API serverseitige Authentifizierung für die Anwendung aus.
ms.assetid: e8e41e8e-1b10-4747-b18e-763e0752ade4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d523df90861c83a45f67811edad243ceee5165
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391404"
---
# <a name="authentication-http-server-api"></a>Authentifizierung (http-Server-API)

Einige Server Anwendungen erfordern eine Client Authentifizierung für den Zugriff auf Ressourcen und Dienst-HTTP-Anforderungen. Ab Version 2,0 führt die HTTP-Server-API serverseitige Authentifizierung für die Anwendung aus. In der HTTP-Server-API-Version 1,0 musste die Server Anwendung ihre eigene Authentifizierung implementieren. Zu den Vorteilen der Authentifizierung von der HTTP-Server-API zählen folgende:

-   Anwendungen können mit niedrigen Berechtigungen ausgeführt werden, wodurch die Sicherheitsrisiken verringert werden.
-   Die Authentifizierung wird im Kernel Modus ausgeführt, wodurch die Übergänge vom Benutzermodus in den Kernel Modus während der Authentifizierung reduziert werden.
-   Bei der im Kernel Modus ausgeführten Authentifizierung können Server Anwendungen unter verschiedenen Benutzerkonten ausgeführt werden. In Version 1,0 müssen alle Anwendungen auf dem Computer unter demselben Benutzerkonto ausgeführt werden, um den Dienst Prinzipal Namen (Service Principal Name, SPN) zu authentifizieren.
-   Der NTLM-Authentifizierungs Hand Shake wird nicht zurückgesetzt, wenn ein Arbeitsprozess wieder verwendet wird, während der Handshake verarbeitet wird.

Um die Version 2,0-Authentifizierung zu nutzen, aktiviert die Anwendung die Authentifizierungs Schemas, die die HTTP-Server-API für die URLs anwendet, für die die Anwendung registriert wurde. Die Authentifizierung kann für die Server Sitzung oder URL-Gruppe aktiviert werden. Die URL-Gruppe erbt die von der Server Sitzung aktivierten Authentifizierungs Schemas, wenn keine für die URL-Gruppe festgelegt ist. Die HTTP-Server-API unterstützt die folgenden Schemas:

-   Aushandeln
-   NTLM
-   Digest
-   Basic

Die Serveranwendung kann auch Authentifizierungs Schemas implementieren, die von der HTTP-Server-API nicht unterstützt werden. Die HTTP-Server-API sendet Anforderungen an die Anwendung für Authentifizierungs Schemas, die nicht unterstützt werden, oder für Schemas, die nicht von der Anwendung aktiviert wurden.

### <a name="enabling-authentication"></a>Aktivieren der Authentifizierung

Die Serveranwendung aktiviert und konfiguriert die Authentifizierung für die Server Sitzung oder URL-Gruppe mit den Funktionen [**httpsetserversessionproperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) oder [**httpseturlgroupproperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) wie folgt:

1.  Die Anwendung ermöglicht die Authentifizierung, indem Sie **httpserverauthenticationproperty** im *Property* -Parameter von [**httpsetserversessionproperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) oder [**httpseturlgroupproperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)angibt.
2.  Die Anwendung gibt die Konfigurationsparameter in der [**http \_ - \_ Server Authentifizierungs \_ Info**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) -Struktur im *ppropertyinformation* -Parameter von [**httpsetserversessionproperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) oder [**httpseturlgroupproperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)an. Die Anwendung gibt die aktivierten Authentifizierungs Schemas an, gibt an, ob das Zwischenspeichern von NTLM-Anmelde Informationen deaktiviert ist, und stellt die Basis-und digestparameter in der **http- \_ Server \_ Authentifizierungs \_ Info**

### <a name="authentication-procedure"></a>Authentifizierungs Prozedur

Um die HTTP-Server Authentifizierung zu initiieren, aktiviert die Anwendung die Authentication-Eigenschaft, bevor die erste Anforderung in der Anforderungs Warteschlange eintrifft. Die folgenden Schritte sind der allgemeine Verarbeitungs Ablauf zum Authentifizieren einer Anforderung.

1.  Die Anwendung aktiviert die-Authentifizierung. Weitere Informationen finden Sie im Abschnitt "Aktivieren der Authentifizierung".
    > [!Note]  
    > Der Client sendet eine nicht authentifizierte Anforderung. Die HTTP-Server-API übergibt die Anforderung an die Server Anwendung und ermöglicht es, die anfängliche 401 Challenge zu generieren. Die HTTP-Server-API enthält die [**http- \_ Anforderung \_ auth \_ Info**](/windows/desktop/api/Http/ns-http-http_request_auth_info) -Struktur, die mit der [**http- \_ Anforderungs**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)) Struktur eingebettet ist. Der Member **AuthStatus** gibt **httpauthstatusnotauthenticated** an.

     

2.  Die Anwendung überprüft den **AuthStatus** -Member der [**HTTP-Anforderungs Authentifizierungs- \_ \_ \_ Informations**](/windows/desktop/api/Http/ns-http-http_request_auth_info) Struktur, um zu bestimmen, ob die Anforderung authentifiziert wurde. Wenn die Anforderung nicht authentifiziert wurde, kann die Anwendung die Anforderung als anonym bedienen oder eine anfängliche 401-Authentifizierungs Aufforderung senden.
3.  Wenn die Anwendung die Anforderung als anonym verarbeitet, verarbeitet Sie die Anforderung und sendet die endgültige Antwort an die Client Anwendung, so als ob die Authentifizierung nicht beteiligt wäre.
4.  Wenn die Anwendung stattdessen eine Authentifizierung erfordert, sendet Sie die anfängliche 401-Challenge mit mindestens einem WWW-Authenticate-Header, der die verfügbaren Schemas für den Client angibt. Die Anwendung sollte die http-Struktur " [**\_ Multiple \_ known \_ Headers**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) " verwenden, um den erforderlichen Satz von Headern zu erstellen, wenn mehrere Authentifizierungs Header in der Antwort gesendet werden.
    > [!Note]
    >
    > Der Client sendet die Anforderung erneut mit dem Autorisierungs Header für ein Schema, das aus dem Satz verfügbarer Schemas ausgewählt wurde, der in der ersten 401-Antwort von der Serveranwendung angegeben wurde.
    >
    > Die HTTP-Server-API überprüft den Authorization Request Authorization-Header, um zu bestimmen, ob das Schema aktiviert ist. Wenn dies der Fall ist, führt die HTTP-Server-API die Authentifizierung durch und verarbeitet alle zwischengeschalteten Anforderungs-/401-Antwort-Austausch Vorgänge, bis der Authentifizierungs Hand Shake abgeschlossen ist
    >
    > Wenn die HTTP-Server-API den Authentifizierungs Versuch abschließt, sendet Sie die Anforderung an die Anwendung mit den Ergebnissen des Authentifizierungs Versuchs in der HTTP-Anforderungs Authentifizierungs- [**\_ \_ \_ Informations**](/windows/desktop/api/Http/ns-http-http_request_auth_info) Struktur, die mit der Anforderung zurückgegeben wird. Wenn der Authentifizierungs Versuch aus einem der folgenden Gründe fehlschlägt, übergibt die HTTP-Server-API die Anforderung nicht an die Anwendung:
    >
    > -   Wenn der Authentifizierungs Hand Shake aufgrund eines internen http-Server-API-Fehlers, z. b. eines Speicher Belegungs Fehlers, fehlschlägt, generiert die HTTP-Server-API eine 503-Antwort (Dienst nicht verfügbar) und sendet Sie an den
    > -   Wenn ein ungültiger Autorisierungs Header, z. b. ein Header ohne Schema Name, oder eine falsch formatierte Base64-Codierung der Client Anmelde Informationen aufgetreten ist, generiert die HTTP-Server-API eine 400-Antwort (ungültige Anforderung) und sendet Sie an den Client zurück

     

5.  Die Serveranwendung überprüft den **AuthStatus** -Member der [**HTTP-Anforderungs Authentifizierungs- \_ \_ \_ Informations**](/windows/desktop/api/Http/ns-http-http_request_auth_info) Struktur, um zu ermitteln, ob die Authentifizierung erfolgreich war. Wenn bei der Authentifizierung ein Fehler auftritt, enthält die HTTP-Server-API den von " [Accept-SecurityContext](/previous-versions/windows/embedded/ms937012(v=msdn.10)) " zurückgegebenen Fehler im **secstatus** -Member der HTTP-Anforderungs Authentifizierungs- **\_ \_ \_ Informations** Struktur. Wenn der Authentifizierungs Versuch aufgrund von ungültigen Anmelde Informationen fehlschlägt, kann die Anwendung eine weitere 401-Abfrage mit der gewünschten WWW-Authenticate Kopfzeile generieren, oder es kann beschlossen werden, die Anforderung als anonym zu bedienen.
6.  Wenn die Authentifizierung erfolgreich war, verwendet die Anwendung das in der HTTP-Anforderungs Authentifizierungs- [**\_ \_ \_ Informations**](/windows/desktop/api/Http/ns-http-http_request_auth_info) Struktur bereitgestellte Token, um die Identität des Clients anzunehmen und auf Ressourcen zuzugreifen. Das an die Anwendung zurückgegebene zugriffstokenhandle ist gültig, solange die Anforderungs-ID gültig ist, was in der Regel so lange dauert, bis die Anwendung die Antwort auf die Anforderung abschließt. Das Token kann jedoch während dieses Zeitraums ablaufen, und die Anwendung muss möglicherweise eine weitere 401-Challenge an den Client senden.
7.  Die Anwendung sendet die endgültige 200 OK-Antwort und muss das Handle für das Zugriffs Token schließen.
    > [!Note]  
    > Die HTTP-Server-API fügt die gegenseitigen Authentifizierungsdaten an die endgültige 200 OK-Antwort an, wenn eine während des Authentifizierungs Handshakes generiert wurde.

     

### <a name="ntlm-null-sessions"></a>NTLM-Null-Sitzungen

Beachten Sie, dass eine NTLM-NULL-Sitzung, die im abschließenden Sicherheitskontext angegeben wird, nicht als authentifiziert behandelt wird. In diesem Fall wird die Anforderung mit einem httpauthstatus-Fehler in der [**\_ \_ \_ Info**](/windows/desktop/api/Http/ns-http-http_request_auth_info) -Struktur der HTTP-Anforderungs Authentifizierung an die Anwendung gesendet, und die Anwendung kann eine weitere 401 Challenge senden.

### <a name="preemptive-authentication"></a>Präemptiv Authentifizierung

Nach dem HTTP-Protokoll kann der Client nach der Einrichtung der Authentifizierung für eine Ressource den entsprechenden Autorisierungs Header mit nachfolgenden aufeinander folgenden Anforderungen für die Ressource vorzeitig senden, ohne auf eine 401-Challenge vom Server zu warten. Wenn das im Autorisierungs Header angegebener Schema weiterhin von der Anwendung aktiviert und von der HTTP-Server-API unterstützt wird, versucht der HTTP-Server die Authentifizierung, ohne die Anforderung an die Anwendung zu senden. Wenn diese Art der authentifizierten Anforderung von der Anwendung empfangen wird, können Sie die Anforderung verwerfen und die anfängliche 401-Challenge erneut generieren oder die Anforderung als authentifiziert bedienen.

### <a name="mutual-authentication"></a>Gegenseitige Authentifizierung

Gegenseitige Authentifizierungsdaten werden generiert, wenn das Aushandlungs Schema beim Handshake verwendet wird und es zu Kerberos aufgelöst wird und der Client eine gegenseitige Authentifizierung angefordert hat. Die gegenseitigen Authentifizierungsdaten werden automatisch von der HTTP-Server-API in die endgültige 200 OK-Antwort eingefügt, die von der Server Anwendung gesendet wird. Standardmäßig übergibt die HTTP-Server-API die Daten der gegenseitigen Authentifizierung nicht an die Server Anwendung, da Sie das Senden der Anwendung automatisch verarbeitet. Wenn die Serveranwendung jedoch das receivemutualauth-Flag in der [**http- \_ Server \_ Authentifizierungs \_ Informations**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) Struktur in der Konfiguration aktiviert, werden die gegenseitigen Authentifizierungsdaten in der HTTP-Anforderungs Authentifizierungs- [**\_ \_ \_ Informations**](/windows/desktop/api/Http/ns-http-http_request_auth_info) Struktur, die mit der authentifizierten [**http- \_ Anforderung**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85))eingebettet ist, an die Anwendung übermittelt. In diesem Fall sollte die Anwendung die gegenseitigen Authentifizierungsdaten mit der letzten 200 OK-Antwort senden. Wenn mehrere Standorte von einem einzelnen Computer bedient werden, werden von allen Standorten auf dem Computer die Anmelde Informationen für das lokale Computer Konto in der Domäne für die gegenseitige Authentifizierung verwendet.

 

 
