---
title: Authentifizierung mit mehreren bekannten Headern
description: Die Struktur "http \_ Multiple \_ known \_ Headers" ermöglicht es Server Anwendungen, mehrere Authentifizierungs Herausforderungen an den Client zu senden.
ms.assetid: d517fd61-9547-4e1c-b0fd-1eb3d0098db2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8afbce3c2a41ea143003723acebc7eb83dc463d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337366"
---
# <a name="authentication-with-multiple-known-headers"></a>Authentifizierung mit mehreren bekannten Headern

Die Struktur " [**http \_ Multiple \_ known \_ Headers**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) " ermöglicht es Server Anwendungen, mehrere Authentifizierungs Herausforderungen an den Client zu senden. Anwendungen können den Client mit einem einzelnen Authentifizierungsschema herausfordern, indem Sie den Enumerationstyp **httpheaderwwwauthenticate** im **knownheaders** -Member der [**http- \_ Antwort \_ Header**](/windows/desktop/api/Http/ns-http-http_response_headers) -Struktur angeben, die in der [**http- \_ Antwort**](http-response.md)enthalten ist. Wenn der Server jedoch mit mehreren Authentifizierungs Schemas herausfordert, verwendet die Anwendung die http-Struktur mit [**\_ mehreren \_ bekannten \_ Headern**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) , um die Authentifizierungs Typen bereitzustellen.

Wenn die **http- \_ Antwort- \_ \_ infoFlags das \_ \_ Order** -Flag beibehalten, sendet HTTP die Authentifizierungs Header in der angegebenen Reihenfolge. Wenn das Flag nicht vorhanden ist, ordnet http die Authentifizierungs Schemas wie folgt von der stärksten zum schwächsten an:

1.  Aushandeln
2.  NTLM
3.  Digest
4.  Basic

Wenn es sich bei dem Authentifizierungsschema nicht um eines dieser Schemas handelt, muss die Anwendung das Flag " **\_ \_ \_ \_ \_ Reihenfolge der HTTP-Antwort-Flags beibehalten** " angeben.

Der **knownheader** -Member von [**http \_ Multiple \_ known \_ Headers**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) verweist auf ein Array von [**bekannten http- \_ \_ Header**](/windows/desktop/api/Http/ns-http-http_known_header) Strukturen. Der **prawvalue** -Member der http-Struktur für **\_ bekannte \_ Header** muss auf eine Zeichenfolge verweisen, die den Schema Namen angibt. HTTP analysiert die Zeichenfolge, um das Schema zu bestimmen, und führt eine der folgenden Aktionen aus:

-   Wenn die Zeichenfolge einen unbekannten Authentifizierungstyp enthält oder der Authentifizierungstyp in der Konfigurations Gruppe (entweder der URL-Gruppe oder der Server Sitzung), die der Anforderung zugeordnet ist, nicht aktiviert ist, fügt die HTTP-Server-API die Zeichenfolge in " **prawvalue** " an den WWW-Authenticate-Header an. Wenn die Anwendung z. b. ein nicht unterstütztes Authentifizierungsschema angibt und " **prawvalue** " die Zeichenfolge "customauthstring" enthält, wird der folgende Text an den Authentifizierungs Header angehängt:

    WWW-Authenticate: customauthschemecrlf

    Wenn für die Anwendung keine Standard Authentifizierung aktiviert ist und " **prawvalue** " die Zeichenfolge "Basic Realm =" basisalm "" enthält, enthält der Authentifizierungs Header den folgenden Text:

    WWW-Authenticate: Basic Realm = "basisalm"

-   Wenn die Zeichenfolge einen bekannten Authentifizierungstyp enthält und in der Konfigurations Gruppe (entweder der URL-Gruppe oder der Server Sitzung) vorhanden ist, die der Anforderung zugeordnet ist, generiert die HTTP-Server-API den WWW-Authenticate-Header. Wenn beispielsweise die in " **prawvalue** " angegebene Zeichenfolge "Digest" und der Digest in der Server Sitzung aktiviert ist, fügt die HTTP-Server-API den folgenden Text an den Authentifizierungs Header an:

    WWW-Authenticate: Digest-Bereich = " testrealm@host.com "

Wenn das Schema im **prawvalue** -Member von [**http \_ known \_ Header**](/windows/desktop/api/Http/ns-http-http_known_header) Aushandlungen oder NTLM lautet, genügt der Name des Authentifizierungs Schemas. Wenn das angegebene Schema "Basic" ist, wird der Bereichs Name an den Schema Namen angehängt. die Anwendung muss den Bereichs Namen nicht in " **prawvalue**" angeben. Wenn das angegebene Schema Digest ist, ruft http " [**Accept-SecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) " auf, um die Aufforderung zu generieren, die an den Schema Namen angehängt wird. Die Parameter für das Schema "Basic" (Bereich) und "Digest" (Bereich und Domänen Name) werden aus den entsprechenden Konfigurations Gruppen-Authentifizierungsinformationen abgerufen.

Wenn die Anwendung in unbekannten Anforderungs Headern mehrere Authentifizierungs Herausforderungen an den Client sendet, sendet die HTTP-Server-API diese ohne Eingriff an den Client. Diese Verwendung wird jedoch nicht empfohlen.

 

 




