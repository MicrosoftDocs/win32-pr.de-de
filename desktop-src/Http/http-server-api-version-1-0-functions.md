---
title: Funktionen der HTTP-Server-API, Version 1,0
description: Die HTTP-Server-API stellt die folgenden Funktionen zum Schreiben von Anwendungen bereit.
ms.assetid: 1da9907d-a09d-41e1-aca1-9a8e2b91296f
keywords:
- Funktionen der HTTP-Server-API, Version 1,0
- Funktionen http, http-Server-API, Version 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050821e40695268d6e3fa2c946d2e8859748db2b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207198"
---
# <a name="http-server-api-version-10-functions"></a>Funktionen der HTTP-Server-API, Version 1,0

Die HTTP-Server-API stellt die folgenden Funktionen zum Schreiben von Anwendungen bereit.

## <a name="general"></a>Allgemein



| Funktion                                             | BESCHREIBUNG                                                                                                                       |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**Httpkreatehttphandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle) | Erstellt eine HTTP-Anforderungs Warteschlange und gibt ein Handle für diese zurück.                                                                         |
| [**Httpinitialize**](/windows/desktop/api/Http/nf-http-httpinitialize)             | Initialisiert die HTTP-Server-API für die Verwendung durch den aufrufenden Prozess.                                                                   |
| [**Httpprepareurl**](/windows/desktop/api/Http/nf-http-httpprepareurl)             | Analysiert, analysiert und normalisiert eine nicht normalisierte Unicode-oder Punycode-URL, sodass Sie sicher und in anderen HTTP-Funktionen verwendet werden kann. |
| [**Httpbeenden**](/windows/desktop/api/Http/nf-http-httpterminate)               | Leitet die HTTP-Server-API an, um alle einem bestimmten Prozess zugeordneten Ressourcen zu bereinigen.                                       |



 

## <a name="cache-management"></a>Cache Verwaltung



| Funktion                                                       | BESCHREIBUNG                                                                                            |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**Httpaddfragmenttocache**](/windows/desktop/api/Http/nf-http-httpaddfragmenttocache)       | Speichert ein Daten Fragment zwischen, sodass es verwendet werden kann, um eine dynamische Antwort ohne Lesevorgang vom Datenträger zu erstellen. |
| [**Httpflushresponlcache**](/windows/desktop/api/Http/nf-http-httpflushresponsecache)       | Entfernt die angegebenen zwischengespeicherten Fragmente aus dem HTTP-Cache.                                                |
| [**Httpreadfragmentfromcache**](/windows/desktop/api/Http/nf-http-httpreadfragmentfromcache) | Ruft ein angegebenes zwischen gespeicherter Antwort Fragment ab.                                                        |



 

## <a name="configuration"></a>Konfiguration



| Funktion                                                                 | BESCHREIBUNG                                                       |
|--------------------------------------------------------------------------|-------------------------------------------------------------------|
| [**Httpdelta eteserviceconfiguration**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) | Löscht die angegebenen Informationen aus dem http-Konfigurations Speicher.  |
| [**Httpqueryserviceconfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration)   | Fragt den HTTP-Konfigurations Speicher nach angegebenen Informationen ab.   |
| [**Httpsetserviceconfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration)       | Legt die angegebenen Werte im Konfigurations Speicher der HTTP-Server-API fest. |



 

## <a name="input-and-output"></a>Eingabe und Ausgabe



| Funktion                                                             | BESCHREIBUNG                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------|
| [**Httpreceivehttprequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest)             | Ruft eine HTTP-Anforderung aus einer angegebenen Anforderungs Warteschlange ab.      |
| [**Httpreceiverequestentitybody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) | Ruft Entitäts Text Daten einer bestimmten HTTP-Anforderung ab.       |
| [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)                 | Sendet eine HTTP-Antwort für eine bestimmte HTTP-Anforderung.          |
| [**Httpsendresponabentitybody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)     | Sendet Entitäts Text Daten einer HTTP-Antwort.                    |
| [**Httpwaitfordisconnect**](/windows/desktop/api/Http/nf-http-httpwaitfordisconnect)               | Benachrichtigt die Anwendung, wenn ein HTTP-Client eine Verbindungs Trennung durch hat. |



 

## <a name="ssl"></a>SSL



| Funktion                                                             | BESCHREIBUNG                                             |
|----------------------------------------------------------------------|---------------------------------------------------------|
| [**Httpreceiveclientcertificate**](/windows/desktop/api/Http/nf-http-httpreceiveclientcertificate) | Ruft das Client Zertifikat für eine SSL-Verbindung ab. |



 

## <a name="url-registration"></a>URL-Registrierung



| Funktion                               | BESCHREIBUNG                                                                                     |
|----------------------------------------|-------------------------------------------------------------------------------------------------|
| [**Httpaddurl**](/windows/desktop/api/Http/nf-http-httpaddurl)       | Registriert eine URL so, dass HTTP-Anforderungen für Sie an eine angegebene Anforderungs Warteschlange weitergeleitet werden.           |
| [**Httpremoveurl**](/windows/desktop/api/Http/nf-http-httpremoveurl) | Hebt die Registrierung einer angegebenen URL auf, sodass keine Anforderungen mehr an eine angegebene Warteschlange weitergeleitet werden. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[HTTP Server-API, Version 1,0, Strukturen](http-server-api-version-1-0-structures.md)
</dt> </dl>

 

 




