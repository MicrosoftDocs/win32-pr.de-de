---
title: HTTP Server API Version 1.0 Functions
description: Die HTTP-Server-API stellt die folgenden Funktionen zum Schreiben von Anwendungen bereit.
ms.assetid: 1da9907d-a09d-41e1-aca1-9a8e2b91296f
keywords:
- HTTP Server API Version 1.0 Functions
- Functions HTTP , HTTP Server API Version 1.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8520753e56e995b5751b55ff71cf49f8e82d414e702b2df255c2901e69c397fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047200"
---
# <a name="http-server-api-version-10-functions"></a>HTTP Server API Version 1.0 Functions

Die HTTP-Server-API stellt die folgenden Funktionen zum Schreiben von Anwendungen bereit.

## <a name="general"></a>Allgemein



| Funktion                                             | BESCHREIBUNG                                                                                                                       |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle) | Erstellt eine HTTP-Anforderungswarteschlange und gibt ein Handle an sie zurück.                                                                         |
| [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize)             | Initialisiert die HTTP-Server-API für die Verwendung durch den aufrufenden Prozess.                                                                   |
| [**HttpPrepareUrl**](/windows/desktop/api/Http/nf-http-httpprepareurl)             | Analysiert, analysiert und normalisiert eine nicht normalisierte Unicode- oder Punycode-URL, sodass die Verwendung in anderen HTTP-Funktionen sicher und gültig ist. |
| [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate)               | Weist die HTTP-Server-API an, alle Ressourcen zu bereinigen, die einem bestimmten Prozess zugeordnet sind.                                       |



 

## <a name="cache-management"></a>Cacheverwaltung



| Funktion                                                       | BESCHREIBUNG                                                                                            |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**HttpAddFragmentToCache**](/windows/desktop/api/Http/nf-http-httpaddfragmenttocache)       | Speichert ein Datenfragment zwischen, sodass es zum Erstellen einer dynamischen Antwort ohne Lesezugriff vom Datenträger verwendet werden kann. |
| [**HttpFlushResponseCache**](/windows/desktop/api/Http/nf-http-httpflushresponsecache)       | Entfernt angegebene zwischengespeicherte Fragmente aus dem HTTP-Cache.                                                |
| [**HttpReadFragmentFromCache**](/windows/desktop/api/Http/nf-http-httpreadfragmentfromcache) | Ruft ein angegebenes zwischengespeichertes Antwortfragment ab.                                                        |



 

## <a name="configuration"></a>Konfiguration



| Funktion                                                                 | BESCHREIBUNG                                                       |
|--------------------------------------------------------------------------|-------------------------------------------------------------------|
| [**HttpDeleteServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) | Löscht angegebene Informationen aus dem HTTP-Konfigurationsspeicher.  |
| [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration)   | Fragt den HTTP-Konfigurationsspeicher nach angegebenen Informationen ab.   |
| [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration)       | Legt die angegebenen Werte im HTTP-Server-API-Konfigurationsspeicher fest. |



 

## <a name="input-and-output"></a>Eingabe und Ausgabe



| Funktion                                                             | BESCHREIBUNG                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------|
| [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest)             | Ruft eine HTTP-Anforderung aus einer angegebenen Anforderungswarteschlange ab.      |
| [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) | Ruft Entitätstextdaten einer bestimmten HTTP-Anforderung ab.       |
| [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)                 | Sendet eine HTTP-Antwort für eine bestimmte HTTP-Anforderung.          |
| [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)     | Sendet Entitätstextdaten einer HTTP-Antwort.                    |
| [**HttpWaitForDisconnect**](/windows/desktop/api/Http/nf-http-httpwaitfordisconnect)               | Benachrichtigt die Anwendung, wenn ein HTTP-Client die Verbindung getrennt hat. |



 

## <a name="ssl"></a>SSL



| Funktion                                                             | BESCHREIBUNG                                             |
|----------------------------------------------------------------------|---------------------------------------------------------|
| [**HttpReceiveClientCertificate**](/windows/desktop/api/Http/nf-http-httpreceiveclientcertificate) | Ruft das Clientzertifikat für eine SSL-Verbindung ab. |



 

## <a name="url-registration"></a>URL-Registrierung



| Funktion                               | BESCHREIBUNG                                                                                     |
|----------------------------------------|-------------------------------------------------------------------------------------------------|
| [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl)       | Registriert eine URL, sodass HTTP-Anforderungen dafür an eine angegebene Anforderungswarteschlange weitergeleitet werden.           |
| [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl) | Aufheben der Registrierung einer angegebenen URL, sodass Anforderungen dafür nicht mehr an eine angegebene Warteschlange weitergeleitet werden. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[HTTP-Server-API- Version 1.0-Strukturen](http-server-api-version-1-0-structures.md)
</dt> </dl>

 

 




