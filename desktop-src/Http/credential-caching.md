---
title: Zwischenspeichern von Anmeldeinformationen
description: Zwischenspeichern von Anmeldeinformationen
ms.assetid: 6e411333-56fa-455b-a90a-f2b54f3c9545
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a139d0cd90495de87f42de08687fd3157acaf6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947905"
---
# <a name="credential-caching"></a>Zwischenspeichern von Anmeldeinformationen

## <a name="credential-caching-on-ntlm-ka-connections"></a>Zwischenspeichern von Anmelde Informationen für NTLM Ka-Verbindungen

Die HTTP-Server-API speichert Anmelde Informationen nur bei Keep-Alive Verbindungen (KA) für die NTLM-Authentifizierung. Standardmäßig speichert die HTTP-Server-API die Anmelde Informationen, die bei der ersten Anforderung abgerufen wurden, die über eine Ka-Verbindung gesendet wurde Der Client kann nachfolgende Anforderungen für Ka-Verbindungen ohne Autorisierungs Header senden und die Authentifizierung auf der Grundlage des zuvor eingerichteten Kontexts abrufen. In diesem Fall sendet die HTTP-Server-API das Token basierend auf den zwischengespeicherten Anmelde Informationen an die Anwendung. Anmelde Informationen für eine Anforderung, die von einem Proxy gesendet wird, werden nicht zwischengespeichert. Die Anwendung deaktiviert das Zwischenspeichern von NTLM-Anmelde Informationen, indem das Flag **disablentlmkredentialcaching** in der [**http- \_ Server \_ Authentifizierungs \_ Info**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) -Struktur festgelegt wird, die in Aufrufen von httpsetserversessionproperty oder httpseturlgroupproperty angegeben wird. Wenn das Zwischenspeichern von Anmelde Informationen deaktiviert ist, werden die zwischengespeicherten Anmelde Informationen von der HTTP-Server-API verworfen

## <a name="ntlm-credential-caching-for-specific-urls"></a>Zwischenspeichern von NTLM-Anmelde Informationen für bestimmte URLs

Die Anwendung bestimmt, ob die von der HTTP-Server-API zurückgegebenen Anforderungs Anmelde Informationen zwischengespeichert werden, indem der Flags-Parameter der HTTP-Anforderungs Authentifizierungs- \_ \_ \_ Informationsstruktur überprüft wird. Dieser Parameter gibt das \_ Token für die HTTP-Anforderungs Authentifizierung \_ \_ \_ \_ für \_ die zwischengespeicherte Erstellung an, \_ Wenn das zurückgegebene NTLM-Token aus dem Cache abgerufen wurde. Das Zwischenspeichern von Anmelde Informationen wird für eine URL-Gruppe für alle URLs in der Gruppe angegeben. Das Zwischenspeichern von Anmelde Informationen auf URL-Basis wird nicht unterstützt. Anwendungen können jedoch ermitteln, ob zwischengespeicherte Anmelde Informationen pro URL akzeptiert oder abgelehnt werden sollen, indem Sie \_ \_ in der HTTP-Anforderungs Authentifizierungs-Informationsstruktur das Flag für die HTTP-Anforderungs Authentifizierung \_ \_ für das \_ \_ zwischengespeicherte Flag für die \_ http- \_ Anforderungs \_ \_ Authentifizierung überprüfen. Die Anwendung lehnt die zwischengespeicherten Anmelde Informationen ab, indem eine 401-Authentifizierungs Aufforderung an den Client gesendet wird. Der Client sendet die Anforderung dann erneut mit den Autorisierungs Headern, wodurch ein neuer Authentifizierungs Hand Shake mit der HTTP-Server-API ausgelöst wird.

## <a name="basic-authentication"></a>Standardauthentifizierung

Wenn ein Standard Authentifizierungs Header in der Anforderung enthalten ist, analysiert die HTTP-Server-API den Header, um den Benutzernamen und das Kennwort zu erhalten. Der Benutzername wird dann in die Benutzer-und Domänen Teile analysiert. Die HTTP-Server-API speichert das Zugriffs Token, das für die Standard Authentifizierung abgerufen wurde, basierend auf dem Benutzernamen und dem Domänen Schlüssel zwischen. Wenn eine neue Anforderung empfangen wird, ruft die HTTP-Server-API das Zugriffs Token basierend auf dem Benutzernamen und der Domäne ab. Das Kennwort in der Anforderung wird dann mit dem zwischengespeicherten Kennwort überprüft. Das zwischengespeicherte Zugriffs Token wird gelöscht, wenn das Gültigkeits Limit für die Gültigkeitsdauer (TTL) erreicht wird.

 

 




