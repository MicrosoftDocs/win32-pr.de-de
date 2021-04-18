---
title: WebDAV-API-Funktionen
description: Die folgenden Funktionen werden in der WebDAV-API verwendet.
ms.assetid: 489cdc17-aca8-4621-bc61-f0f3b9ac22b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1917cd6ebb64470eec6fde9188cc39341142fc8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339836"
---
# <a name="webdav-api-functions"></a>WebDAV-API-Funktionen

Die folgenden Funktionen werden in der WebDAV-API verwendet.



| Funktion                                                             | BESCHREIBUNG                                                                                                                                                                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Davaddconnection**](/windows/desktop/api/davclnt/nf-davclnt-davaddconnection)                         | Erstellt eine sichere Verbindung mit einem WebDAV-Server oder eine Remote Datei oder ein Remote Verzeichnis auf einem WebDAV-Server.                                                                                                                                   |
| [*Davauthcallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback)                                | Der WebDAV-Client ruft die Anwendungs definierte [*davauthcallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback) -Rückruffunktion auf, um den Benutzer zur Eingabe von Anmelde Informationen aufzufordern.                                                                                           |
| [**Davcancelconnectionstoserver**](/windows/desktop/api/davclnt/nf-davclnt-davcancelconnectionstoserver) | Schließt alle Verbindungen mit einem WebDAV-Server oder eine Remote Datei oder ein Remote Verzeichnis auf einem WebDAV-Server.                                                                                                                                        |
| [**Davdeleteconnection**](/windows/desktop/api/davclnt/nf-davclnt-davdeleteconnection)                   | Schließt eine Verbindung, die mit der [**davaddconnection**](/windows/desktop/api/davclnt/nf-davclnt-davaddconnection) -Funktion erstellt wurde.                                                                                                                              |
| [**Davflushfile**](/windows/desktop/api/davclnt/nf-davclnt-davflushfile)                                 | Leert die Daten aus der lokalen Version einer Remote Datei auf den WebDAV-Server.                                                                                                                                                        |
| [*Davfreecredcallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback_freecred)                        | Der WebDAV-Client ruft die Anwendungs definierte [*davfreecredcallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback_freecred) -Rückruffunktion auf, um die Anmelde Informationen freizugeben, die von der [*davauthcallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback) -Rückruffunktion abgerufen wurden. |
| [**Davgetextendecoderror**](/windows/desktop/api/davclnt/nf-davclnt-davgetextendederror)                   | Ruft die erweiterten Fehlercode Informationen ab, die der WebDAV-Server für den vorherigen fehlgeschlagenen e/a-Vorgang zurückgegeben hat.                                                                                                                  |
| [**Davgethttpfromuncpath**](/windows/desktop/api/davclnt/nf-davclnt-davgethttpfromuncpath)               | Konvertiert den angegebenen UNC-Pfad in einen entsprechenden HTTP-Pfad.                                                                                                                                                                           |
| [**Davgetthelockbesitzofder file**](/windows/desktop/api/davclnt/nf-davclnt-davgetthelockownerofthefile)   | Gibt den Besitzer der Datei Sperre für eine Datei zurück, die auf einem WebDAV-Server gesperrt ist.                                                                                                                                                             |
| [**Davgetuncfromhttppath**](/windows/desktop/api/davclnt/nf-davclnt-davgetuncfromhttppath)               | Konvertiert den angegebenen HTTP-Pfad in einen entsprechenden UNC-Pfad.                                                                                                                                                                           |
| [**Davinvalidatecache**](/windows/desktop/api/davclnt/nf-davclnt-davinvalidatecache)                     | Erklärt den Inhalt des lokalen Caches für eine Remote Datei auf einem WebDAV-Server für ungültig.                                                                                                                                                     |
| [**Davregisterauthcallback**](/windows/desktop/api/Davclnt/nf-davclnt-davregisterauthcallback)           | Registriert eine Anwendungs definierte Rückruffunktion, die vom WebDAV-Client verwendet werden kann, um den Benutzer zur Eingabe von Anmelde Informationen aufzufordern.                                                                                                                 |
| [**Davunregisterauthcallback**](/windows/desktop/api/Davclnt/nf-davclnt-davunregisterauthcallback)       | Hebt die Registrierung einer registrierten Rückruffunktion auf, die der WebDAV-Client verwendet, um den Benutzer zur Eingabe von Anmelde Informationen aufzufordern.                                                                                                                            |



 

 

 




