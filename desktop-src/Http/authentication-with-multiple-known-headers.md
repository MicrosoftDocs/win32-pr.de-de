---
title: Authentifizierung mit mehreren bekannten Headern
description: Mit der HTTP \_ MULTIPLE \_ KNOWN \_ HEADERS-Struktur können Serveranwendungen mehrere Authentifizierungsherausforderungen an den Client senden.
ms.assetid: d517fd61-9547-4e1c-b0fd-1eb3d0098db2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbb8fd2071626d8a12f046ac0c3b6c50fcffc794462d5109a89a974f441879bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950929"
---
# <a name="authentication-with-multiple-known-headers"></a>Authentifizierung mit mehreren bekannten Headern

Mit [**der HTTP MULTIPLE KNOWN \_ \_ \_ HEADERS-Struktur**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) können Serveranwendungen mehrere Authentifizierungsherausforderungen an den Client senden. Anwendungen können den Client mit einem einzelnen Authentifizierungsschema fordern, indem sie den **HttpHeaderWwwAuthenticate-Enumerationstyp** im **KnownHeaders-Member** der [**HTTP RESPONSE \_ \_ HEADERS-Struktur**](/windows/desktop/api/Http/ns-http-http_response_headers) angeben, die in [**HTTP RESPONSE enthalten \_ ist.**](http-response.md) Wenn der Server jedoch mit mehreren Authentifizierungsschemas konfrontiert wird, verwendet die Anwendung die HTTP MULTIPLE KNOWN HEADERS-Struktur, um die [**\_ \_ \_ Authentifizierungstypen**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) zur Verfügung zu stellen.

Wenn das **FLAG HTTP RESPONSE INFO \_ \_ \_ FLAGS PRESERVE \_ \_ ORDER** vorhanden ist, sendet HTTP die Authentifizierungsheader in der angegebenen Reihenfolge. Wenn das Flag nicht vorhanden ist, ordnet HTTP die Authentifizierungsschemas wie folgt vom stärksten zum schwachsten an:

1.  Aushandeln
2.  NTLM
3.  Digest
4.  Basic

Wenn es sich bei dem Authentifizierungsschema nicht um eines dieser Schemas handelt, muss die Anwendung das **FLAG HTTP RESPONSE INFO \_ \_ \_ FLAGS PRESERVE \_ \_ ORDER** angeben.

Der **KnownHeader-Member** von [**HTTP MULTIPLE KNOWN \_ \_ \_ HEADERS**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) verweist auf ein Array von [**HTTP KNOWN \_ \_ HEADER-Strukturen.**](/windows/desktop/api/Http/ns-http-http_known_header) Der **pRawValue-Member** der **HTTP KNOWN \_ \_ HEADER-Struktur** muss auf eine Zeichenfolge zeigen, die den Schemanamen angibt. HTTP analysiert die Zeichenfolge, um das Schema zu bestimmen, und führt eine der folgenden Aktionen aus:

-   Wenn die Zeichenfolge einen unbekannten Authentifizierungstyp enthält oder der Authentifizierungstyp in der Konfigurationsgruppe (entweder der URL-Gruppe oder der Serversitzung), die der Anforderung zugeordnet ist, nicht aktiviert ist, fügt die HTTP-Server-API die Zeichenfolge in **pRawValue** an den WWW-Authenticate-Header an. Wenn die Anwendung beispielsweise ein nicht unterstütztes Authentifizierungsschema angibt und **pRawValue** die Zeichenfolge "CustomAuthString" enthält, wird der folgende Text an den Authentifizierungsheader angefügt:

    WWW-Authenticate: CustomAuthSchemeCRLF

    Wenn für die Anwendung die Standardauthentifizierung nicht aktiviert ist und **pRawValue** die Zeichenfolge "Basic realm="BasicRealm" enthält, enthält der Authentifizierungsheader den folgenden Text:

    WWW-Authenticate: Basic realm="BasicRealm"

-   Wenn die Zeichenfolge einen bekannten Authentifizierungstyp enthält und in der Konfigurationsgruppe (entweder der URL-Gruppe oder der Serversitzung) vorhanden ist, die der Anforderung zugeordnet ist, generiert die HTTP-Server-API den WWW-Authenticate Header. Wenn die in **pRawValue** angegebene Zeichenfolge beispielsweise "Digest" ist und Digest für die Serversitzung aktiviert ist, fügt die HTTP-Server-API den folgenden Text an den Authentifizierungsheader an:

    WWW-Authenticate: Digest realm=" testrealm@host.com "

Wenn das Schema im **pRawValue-Member** von [**HTTP KNOWN \_ \_ HEADER**](/windows/desktop/api/Http/ns-http-http_known_header) Negotiate oder NTLM ist, ist der Name des Authentifizierungsschemas ausreichend. Wenn das angegebene Schema Basic ist, wird der Bereichsname an den Schemanamen angefügt. Die Anwendung muss den Bereichsnamen nicht in **pRawValue angeben.** Wenn das angegebene Schema Digest ist, ruft HTTP [**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) auf, um die Herausforderung zu generieren, die an den Schemanamen angefügt wird. Die Parameter für das Schema Basic (Bereich) und Digest (Bereich und Domänenname) werden aus den entsprechenden Konfigurationsgruppen-Authentifizierungsinformationen ermittelt.

Wenn die Anwendung mehrere Authentifizierungsanforderungen an den Client in unbekannten Anforderungsheadern sendet, sendet die HTTP-Server-API diese ohne Eingriff an den Client. Diese Verwendung wird jedoch nicht empfohlen.

 

 




