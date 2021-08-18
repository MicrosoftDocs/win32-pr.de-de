---
title: WebDAV-API-Funktionen
description: Die folgenden Funktionen werden in der WebDAV-API verwendet.
ms.assetid: 489cdc17-aca8-4621-bc61-f0f3b9ac22b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 401f527bcd98f86f8116df5b25ba1ea71e0f432e19dc89eae00582a2a0b4865e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995040"
---
# <a name="webdav-api-functions"></a>WebDAV-API-Funktionen

Die folgenden Funktionen werden in der WebDAV-API verwendet.



| Funktion                                                             | Beschreibung                                                                                                                                                                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DavAddConnection**](/windows/desktop/api/davclnt/nf-davclnt-davaddconnection)                         | Erstellt eine sichere Verbindung mit einem WebDAV-Server oder einer Remotedatei oder einem Remoteverzeichnis auf einem WebDAV-Server.                                                                                                                                   |
| [*DavAuthCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback)                                | Der WebDAV-Client ruft die anwendungsdefinierte [*DavAuthCallback-Rückruffunktion*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback) auf, um den Benutzer zur Eingabe von Anmeldeinformationen aufzugeben.                                                                                           |
| [**DavCancelConnectionsToServer**](/windows/desktop/api/davclnt/nf-davclnt-davcancelconnectionstoserver) | Schließt alle Verbindungen mit einem WebDAV-Server oder einer Remotedatei oder einem Remoteverzeichnis auf einem WebDAV-Server.                                                                                                                                        |
| [**DavDeleteConnection**](/windows/desktop/api/davclnt/nf-davclnt-davdeleteconnection)                   | Schließt eine Verbindung, die mithilfe der [**DavAddConnection-Funktion erstellt**](/windows/desktop/api/davclnt/nf-davclnt-davaddconnection) wurde.                                                                                                                              |
| [**DavFlushFile**](/windows/desktop/api/davclnt/nf-davclnt-davflushfile)                                 | Leert die Daten aus der lokalen Version einer Remotedatei auf den WebDAV-Server.                                                                                                                                                        |
| [*DavFreeCredCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback_freecred)                        | Der WebDAV-Client ruft die anwendungsdefinierte [*DavFreeCredCallback-Rückruffunktion*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback_freecred) auf, um die Anmeldeinformationen frei zu geben, die von der [*DavAuthCallback-Rückruffunktion*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback) abgerufen wurden. |
| [**DavGetExtendedError**](/windows/desktop/api/davclnt/nf-davclnt-davgetextendederror)                   | Ruft die erweiterten Fehlercodeinformationen ab, die der WebDAV-Server für den vorherigen fehlgeschlagenen E/A-Vorgang zurückgegeben hat.                                                                                                                  |
| [**DavGetHTTPFromUNCPath**](/windows/desktop/api/davclnt/nf-davclnt-davgethttpfromuncpath)               | Konvertiert den angegebenen UNC-Pfad in einen entsprechenden HTTP-Pfad.                                                                                                                                                                           |
| [**DavGetTheLockOwnerOfTheFile**](/windows/desktop/api/davclnt/nf-davclnt-davgetthelockownerofthefile)   | Gibt den Dateisperrbesitzer für eine Datei zurück, die auf einem WebDAV-Server gesperrt ist.                                                                                                                                                             |
| [**DavGetUNCFromHTTPPath**](/windows/desktop/api/davclnt/nf-davclnt-davgetuncfromhttppath)               | Konvertiert den angegebenen HTTP-Pfad in einen entsprechenden UNC-Pfad.                                                                                                                                                                           |
| [**DavInvalidateCache**](/windows/desktop/api/davclnt/nf-davclnt-davinvalidatecache)                     | Erklärt den Inhalt des lokalen Caches für eine Remotedatei auf einem WebDAV-Server für ungültig.                                                                                                                                                     |
| [**DavRegisterAuthCallback**](/windows/desktop/api/Davclnt/nf-davclnt-davregisterauthcallback)           | Registriert eine anwendungsdefinierte Rückruffunktion, mit der der WebDAV-Client den Benutzer zur Eingabe von Anmeldeinformationen auffordern kann.                                                                                                                 |
| [**DavUnregisterAuthCallback**](/windows/desktop/api/Davclnt/nf-davclnt-davunregisterauthcallback)       | Aufheben der Registrierung einer registrierten Rückruffunktion, die vom WebDAV-Client verwendet wird, um den Benutzer zur Eingabe von Anmeldeinformationen aufforderungen.                                                                                                                            |



 

 

 




