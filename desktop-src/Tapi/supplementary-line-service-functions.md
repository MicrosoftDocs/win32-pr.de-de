---
description: Die Funktionen für den ergänzenden Zeilen Dienst sind in den folgenden Themen nach Kategorie aufgelistet.
ms.assetid: d4338b3c-cd84-4abb-b74e-9df895c8355b
title: Funktionen für ergänzende Zeilen Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21a29831369fd6b886d57cfae075b5b8bf7a83b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349850"
---
# <a name="supplementary-line-service-functions"></a>Funktionen für ergänzende Zeilen Dienste

Die Funktionen für den ergänzenden Zeilen Dienst sind in den folgenden Themen nach Kategorie aufgelistet. Eine Funktion wird als [*asynchron*](a-tapgloss.md) identifiziert, wenn Sie die Vervollständigung in einer Antwortmeldung an die Anwendung angibt. Wenn die Funktion das Ergebnis immer sofort an die Anwendung zurückgibt, gilt die Funktion als [*synchron*](s-tapgloss.md).

Im folgenden finden Sie eine funktionale Gruppierung der Funktionen für den ergänzenden Zeilen Dienst:

-   [Agents](#agents)
-   [Anwendungs Priorität](#application-priority)
-   [Bearermodus und-Rate](#bearer-mode-and-rate)
-   [Akzeptieren und Umleiten von Anrufen](#call-accept-and-redirect)
-   [Rückruf Abschluss](#call-completion)
-   [Telefonkonferenz](#call-conference)
-   [Weiterleitungs Weiterleitung](#call-forwarding)
-   [Halt halten](#call-hold)
-   [Callpark](#call-park)
-   [Abhol Anrufe](#call-pickup)
-   [Rückruf ablehnen](#call-reject)
-   [Aufrufe übertragen](#call-transfer)
-   [Ziffern Überwachung und-Erfassung](#digit-monitoring-and-gathering)
-   [Erstellen von Inband-Ziffern und-Tönen](#generating-inband-digits-and-tones)
-   [Aufrufen](basic-telephony-services-reference.md)
-   [Mediensteuer Element](#media-control)
-   [Medienüberwachung](#media-monitoring)
-   [Proxys](#proxies)
-   [Quality of Service (QoS, Dienstqualität)](#quality-of-service)
-   [Senden von Informationen an eine Remote Partei](#sending-information-to-remote-party)
-   [Verwaltung von Dienstanbietern](#service-provider-management)
-   [Festlegen eines Terminals für Telefon Konversationen](#setting-a-terminal-for-phone-conversations)
-   [Tone-Überwachung](#tone-monitoring)

Es gibt auch [verschiedene](#miscellaneous) ergänzende Zeilen Dienstfunktionen.

## <a name="bearer-mode-and-rate"></a>Bearermodus und-Rate



| Funktion                                       | BESCHREIBUNG                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**linesetcallparametriams**](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams) | Fordert eine Änderung in den callparametern eines vorhandenen Aufrufes an. Synchronous. |



 

## <a name="media-monitoring"></a>Medienüberwachung



| Funktion                                     | BESCHREIBUNG                                                                   |
|----------------------------------------------|-------------------------------------------------------------------------------|
| [**linemonitormedia**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia) | Aktiviert oder deaktiviert die Benachrichtigung im Medien Modus für einen angegebenen-Befehl. Synchronous. |



 

## <a name="digit-monitoring-and-gathering"></a>Ziffern Überwachung und-Erfassung



| Funktion                                       | BESCHREIBUNG                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [**linemonitordigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) | Aktiviert oder deaktiviert die Benachrichtigung über die Ziffern Erkennung für einen angegebenen-Befehl. Synchronous. |
| [**linegather-Ziffern**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)   | Führt die gepufferte Erfassung von Ziffern bei einem-Befehl aus. Synchronous.                  |



 

## <a name="tone-monitoring"></a>Tone-Überwachung



| Funktion                                     | BESCHREIBUNG                                                       |
|----------------------------------------------|-------------------------------------------------------------------|
| [**linemonitortones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) | Gibt an, welche Töne bei einem angegebenen-Befehl erkannt werden sollen. Synchronous. |



 

## <a name="media-control"></a>Mediensteuer Element



| Funktion                                           | BESCHREIBUNG                                                                                                          |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**linesetmediacontrol**](/windows/desktop/api/Tapi/nf-tapi-linesetmediacontrol) | Richtet den Mediendaten Strom eines Aufrufes für das mediensteuer Element ein. Synchronous.                                                        |
| [**linesetmediamode**](/windows/desktop/api/Tapi/nf-tapi-linesetmediamode)       | Legt die Medien Modi des angegebenen Aufrufes in der [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) -Struktur fest. Synchronous. |



 

## <a name="generating-inband-digits-and-tones"></a>Erstellen von Inband-Ziffern und-Tönen



| Funktion                                         | BESCHREIBUNG                                                   |
|--------------------------------------------------|---------------------------------------------------------------|
| [**linegeneratedigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) | Generiert bei einem-aufrufzeichen inbandziffern. Synchronous.               |
| [**linegeneratetone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone)     | Generiert einen angegebenen Satz von Tönen bei einem-Befehl in Inband. Synchronous. |



 

## <a name="call-accept-and-redirect"></a>Akzeptieren und Umleiten von Anrufen



| Funktion                             | BESCHREIBUNG                                                                                               |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**lineaccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept)     | Akzeptiert einen angebotenen Aufruf und beginnt mit der Warnung des Aufrufers (Ringback) und der sogenannten Partei (Ring). Asynchron. |
| [**lineredirect**](/windows/desktop/api/Tapi/nf-tapi-lineredirect) | Leitet einen Angebots Rückruf an eine andere Adresse um. Asynchron.                                              |



 

## <a name="call-reject"></a>Rückruf ablehnen



| Funktion                     | BESCHREIBUNG                                                               |
|------------------------------|---------------------------------------------------------------------------|
| [**linedrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) | Trennt einen-Befehl oder bricht einen aufzurufenden Versuch ab. Asynchron. |



 

## <a name="call-hold"></a>Halt halten



| Funktion                         | BESCHREIBUNG                                           |
|----------------------------------|-------------------------------------------------------|
| [**linehold**](/windows/desktop/api/Tapi/nf-tapi-linehold)     | Platziert den angegebenen-aufrufungs-. Asynchron. |
| [**lineunhold**](/windows/desktop/api/Tapi/nf-tapi-lineunhold) | Ruft einen gehaltenen-Befehl ab. Asynchron.                  |



 

## <a name="securing-calls"></a>Sichern von Aufrufen



| Funktion                                 | BESCHREIBUNG                                                                                                              |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**linesecurecall**](/windows/desktop/api/Tapi/nf-tapi-linesecurecall) | Sichert einen vorhandenen-Rückruf von Störungen durch andere Ereignisse wie z. b. Aufrufe, die auf Datenverbindungen warten. Asynchron. |



 

## <a name="call-transfer"></a>Aufrufe übertragen



| Funktion                                             | BESCHREIBUNG                                                                                                    |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)       | Bereitet einen angegebenen-Befehl für die Übertragung an eine andere Adresse vor. Asynchron.                                       |
| [**linecompletetransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) | Überträgt einen aufgerufen, der für die Übertragung an einen anderen-Befehl eingerichtet wurde, oder wechselt in eine drei-Wege-Konferenz. Asynchron. |
| [**lineblintransfer**](/windows/desktop/api/Tapi/nf-tapi-lineblindtransfer)       | Überträgt einen-Rückruf an eine andere Partei. Asynchron.                                                               |
| [**lineswaphold**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold)                 | Vertauscht den aktiven-Befehl mit dem derzeit bei der Beratung angehaltenen-Rückruf. Asynchron.                              |



 

## <a name="call-conference"></a>Telefonkonferenz



| Funktion                                                         | BESCHREIBUNG                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**linesetupconference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)               | Bereitet einen angegebenen-Rückruf für das Hinzufügen einer anderen Partei vor. Asynchron.                                                                                                                               |
| [**lineprepareaddumconference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) | Bereitet das Hinzufügen einer Partei zu einem bestehenden Konferenzgespräch vor, indem der Konferenzanrufe in den Status "Hold" versetzt und ein Rückruf aufgerufen wird, der später dem Konferenztelefon hinzugefügt werden kann. Asynchron. |
| [**lineaddumconference**](/windows/desktop/api/Tapi/nf-tapi-lineaddtoconference)               | Fügt einen Rückruf für einen vorhandenen Konferenz Rückruf hinzu. Asynchron.                                                                                                                               |
| [**lineremovefromconference**](/windows/desktop/api/Tapi/nf-tapi-lineremovefromconference)     | Entfernt eine Partei aus einem Konferenzgespräch. Asynchron.                                                                                                                                                |



 

## <a name="call-park"></a>Callpark



| Funktion                         | BESCHREIBUNG                                          |
|----------------------------------|------------------------------------------------------|
| [**linepark**](/windows/desktop/api/Tapi/nf-tapi-linepark)     | In wird ein angegebener-Rückruf an einer anderen Adresse Asynchron. |
| [**lineunpark**](/windows/desktop/api/Tapi/nf-tapi-lineunpark) | Ruft einen geparkten-Befehl ab. Asynchron.               |



 

## <a name="call-forwarding"></a>Weiterleitungs Weiterleitung



| Funktion                           | BESCHREIBUNG                                             |
|------------------------------------|---------------------------------------------------------|
| [**lineforward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) | Legt Anforderungs Weiterleitungs Anforderungen fest oder bricht Sie ab. Asynchron. |



 

## <a name="call-pickup"></a>Abhol Anrufe



| Funktion                         | BESCHREIBUNG                                                                                                                                                                                      |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**linepickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) | Ruft eine aufrufswarnung an einer angegebenen Zieladresse ab und gibt ein-Rückruf Handle für den aufzurufenden-Befehl zurück ([**linepickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) kann auch für das warten auf Aufrufe verwendet werden). Asynchron. |



 

## <a name="sending-information-to-remote-party"></a>Senden von Informationen an eine Remote Partei



| Funktion                                                   | BESCHREIBUNG                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**linereleaseuseruserinfo**](/windows/desktop/api/Tapi/nf-tapi-linereleaseuseruserinfo) | Gibt Benutzer Benutzerinformationen frei und ermöglicht dem System, diesen Speicher mit neuen Informationen zu überschreiben. Asynchron. |
| [**linesenduseruserinfo**](/windows/desktop/api/Tapi/nf-tapi-linesenduseruserinfo)       | Sendet Benutzer Benutzerinformationen für den angegebenen-Befehl an die Remote Partei. Asynchron.                                |



 

## <a name="call-completion"></a>Rückruf Abschluss



| Funktion                                         | BESCHREIBUNG                                      |
|--------------------------------------------------|--------------------------------------------------|
| [**linecompletecall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)     | Fügt eine Anforderung zum Abschluss der Anforderung ein. Asynchron.  |
| [**lineuncompletecall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall) | Bricht eine Anforderung zum Abschließen des Aufrufes ab. Asynchron. |



 

## <a name="setting-a-terminal-for-phone-conversations"></a>Festlegen eines Terminals für Telefon Konversationen



| Funktion                                   | BESCHREIBUNG                                                                                                                      |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**linesetterminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) | Gibt das Terminal Gerät an, an das die angegebene Zeile, die Adress Ereignisse oder die Ereignisse zum Abrufen von Medienströmen weitergeleitet werden. Asynchron. |



 

## <a name="application-priority"></a>Anwendungs Priorität



| Funktion                                         | BESCHREIBUNG                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**linegetapppriority**](/windows/desktop/api/Tapi/nf-tapi-linegetapppriority) | Ruft die Informationen zur Übergabe und/oder zur unterstützten telefoniepriorität für eine Anwendung ab. Synchronous. |
| [**linesetapppriority**](/windows/desktop/api/Tapi/nf-tapi-linesetapppriority) | Legt die Übergabe und/oder die unterstützte telefoniepriorität für eine Anwendung fest. Synchronous.              |



 

## <a name="service-provider-management"></a>Verwaltung von Dienstanbietern



| Funktion                                           | BESCHREIBUNG                                                           |
|----------------------------------------------------|-----------------------------------------------------------------------|
| [**lineaddprovider**](/windows/desktop/api/Tapi/nf-tapi-lineaddprovider)         | Installiert einen Telefoniedienstanbieter. Synchronous.                   |
| [**lineconfigprovider**](/windows/desktop/api/Tapi/nf-tapi-lineconfigprovider)   | Zeigt das Konfigurations Dialogfeld eines Dienstanbieters an. Synchronous. |
| [**lineremoveprovider**](/windows/desktop/api/Tapi/nf-tapi-lineremoveprovider)   | Entfernt einen vorhandenen Telefoniedienstanbieter. Synchronous.          |
| [**linegetproviderlist**](/windows/desktop/api/Tapi/nf-tapi-linegetproviderlist) | Ruft eine Liste installierter Dienstanbieter ab. Synchronous.         |



 

## <a name="agents"></a>Agents



| Funktion                                                     | BESCHREIBUNG                                                                                                                             |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**lineagentspecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)               | Ermöglicht der Anwendung den Zugriff auf proprietäre handlerspezifische Funktionen des mit der Adresse verknüpften Agent-Handlers. Asynchron. |
| [**linegetagentactivitylist**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista) | Ruft die Liste der Aktivitäten ab, von denen eine Anwendung die Funktionen auswählt, die ein Agent ausführt. Asynchron.                    |
| [**linegetagentcaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa)                 | Ruft die agentbezogenen Funktionen ab, die auf dem angegebenen Zeilen Gerät unterstützt werden. Asynchron.                                            |
| [**linegetagentgrouplist**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista)       | Ruft die Liste der Agentgruppen ab, in denen sich ein Agent auf dem automatischen-Anrufs anmelden kann. Asynchron.                      |
| [**linegetagentstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)             | Ruft den agentbezogenen Status für die angegebene Adresse ab. Asynchron.                                                                |
| [**linesetagentactivity**](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity)         | Legt den Agent-Aktivitäts Code fest, der einer bestimmten Adresse zugeordnet ist. Asynchron.                                                        |
| [**linesetagentgroup**](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup)               | Legt die Agentgruppen fest, bei denen der Agent bei einer bestimmten Adresse angemeldet ist. Asynchron.                                              |
| [**linesetagentstate**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate)               | Legt den Agent-Status fest, der einer bestimmten Adresse zugeordnet ist. Asynchron.                                                                |



 

## <a name="proxies"></a>Proxys



| Funktion                                       | BESCHREIBUNG                                                                         |
|------------------------------------------------|-------------------------------------------------------------------------------------|
| [**lineproxymess**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)   | Wird von einem registrierten Proxy Anforderungs Handler zum Generieren von TAPI-Nachrichten verwendet. Synchronous.  |
| [**lineproxyresponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) | Gibt den Abschluss einer Proxy Anforderung durch einen registrierten Proxy Handler an. Synchronous. |



 

## <a name="quality-of-service"></a>Quality of Service (QoS, Dienstqualität)



| Funktion                                                           | BESCHREIBUNG                                                                                |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**linesetcallqualityofservice**](/windows/desktop/api/Tapi/nf-tapi-linesetcallqualityofservice) | Fordert eine Änderung der Quality of Service-Parameter für einen vorhandenen-Rückruf an. Asynchron. |



 

## <a name="miscellaneous"></a>Verschiedenes



| Funktion                                             | BESCHREIBUNG                                                                                           |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**linesetcalldata**](/windows/desktop/api/Tapi/nf-tapi-linesetcalldata)           | Legt den **calldata** -Member der [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) -Struktur fest. Asynchron. |
| [**linesetcalltreatment**](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) | Legt die Sounds fest, die der Benutzer erfährt, wenn ein Rückruf nicht offen ist oder angehalten wird. Asynchron.               |
| [**linesetlinedevstatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) | Legt den Gerätestatus der Zeile fest. Asynchron.                                                            |



 

 

 



