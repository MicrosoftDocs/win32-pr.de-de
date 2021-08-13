---
description: Die Funktionen des ergänzenden Liniendiensts sind in den folgenden Themen nach Kategorie aufgeführt.
ms.assetid: d4338b3c-cd84-4abb-b74e-9df895c8355b
title: Ergänzende Liniendienstfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0f2bdd609f092adebd5270a4cc8a3fe35bedce17ad57d8e4e85b5875001255f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119476343"
---
# <a name="supplementary-line-service-functions"></a>Ergänzende Liniendienstfunktionen

Die Funktionen des ergänzenden Liniendiensts sind in den folgenden Themen nach Kategorie aufgeführt. Eine Funktion wird als asynchron [*identifiziert,*](a-tapgloss.md) wenn sie in einer ANTWORT-Nachricht an die Anwendung auf den Abschluss hinweist. Wenn die Funktion ihr Ergebnis immer sofort an die Anwendung zurückgibt, wird die Funktion als synchron [*betrachtet.*](s-tapgloss.md)

Im Folgenden finden Sie eine funktionale Gruppierung der ergänzenden Liniendienstfunktionen:

-   [Agents](#agents)
-   [Anwendungspriorität](#application-priority)
-   [Bearermodus und -rate](#bearer-mode-and-rate)
-   [Annehmen und Umleiten von Aufrufen](#call-accept-and-redirect)
-   [Aufrufabschluss](#call-completion)
-   [Telefonkonferenz](#call-conference)
-   [Anrufweiterleitung](#call-forwarding)
-   [Aufrufen von "Hold"](#call-hold)
-   [Callpark](#call-park)
-   [Abholung des Anrufs](#call-pickup)
-   [Ablehnen aufrufen](#call-reject)
-   [Anrufübertragung](#call-transfer)
-   [Überwachung und Erfassung von Ziffern](#digit-monitoring-and-gathering)
-   [Generieren von Inbandziffern und -tönen](#generating-inband-digits-and-tones)
-   [Tätigen von Aufrufen](basic-telephony-services-reference.md)
-   [Mediensteuerung](#media-control)
-   [Medienüberwachung](#media-monitoring)
-   [Proxys](#proxies)
-   [Quality of Service (QoS, Dienstqualität)](#quality-of-service)
-   [Senden von Informationen an eine Remoteparty](#sending-information-to-remote-party)
-   [Verwaltung von Dienstanbietern](#service-provider-management)
-   [Festlegen eines Terminals für Telefonanrufe](#setting-a-terminal-for-phone-conversations)
-   [Tonüberwachung](#tone-monitoring)

Es gibt auch [verschiedene ergänzende](#miscellaneous) Liniendienstfunktionen.

## <a name="bearer-mode-and-rate"></a>Bearermodus und -rate



| Funktion                                       | BESCHREIBUNG                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**lineSetCallParams**](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams) | Fordert eine Änderung der Aufrufparameter eines vorhandenen Aufrufs an. Synchronous. |



 

## <a name="media-monitoring"></a>Medienüberwachung



| Funktion                                     | BESCHREIBUNG                                                                   |
|----------------------------------------------|-------------------------------------------------------------------------------|
| [**lineMonitorMedia**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia) | Aktiviert oder deaktiviert die Medienmodusbenachrichtigung bei einem angegebenen Aufruf. Synchronous. |



 

## <a name="digit-monitoring-and-gathering"></a>Ziffernüberwachung und -erfassung



| Funktion                                       | BESCHREIBUNG                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) | Aktiviert oder deaktiviert die Benachrichtigung zur Ziffernerkennung bei einem angegebenen Aufruf. Synchronous. |
| [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)   | Führt die gepufferte Sammlung von Ziffern für einen Aufruf aus. Synchronous.                  |



 

## <a name="tone-monitoring"></a>Tonüberwachung



| Funktion                                     | BESCHREIBUNG                                                       |
|----------------------------------------------|-------------------------------------------------------------------|
| [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) | Gibt an, welche Töne bei einem angegebenen Aufruf erkannt werden. Synchronous. |



 

## <a name="media-control"></a>Mediensteuerung



| Funktion                                           | BESCHREIBUNG                                                                                                          |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**lineSetMediaControl**](/windows/desktop/api/Tapi/nf-tapi-linesetmediacontrol) | Richtet den Medienstream eines Aufrufs für die Mediensteuerung ein. Synchronous.                                                        |
| [**lineSetMediaMode**](/windows/desktop/api/Tapi/nf-tapi-linesetmediamode)       | Legt die Medienmodus(en) des angegebenen Aufrufs in seiner [**LINECALLINFO-Struktur**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) fest. Synchronous. |



 

## <a name="generating-inband-digits-and-tones"></a>Generieren von Inbandziffern und -tönen



| Funktion                                         | BESCHREIBUNG                                                   |
|--------------------------------------------------|---------------------------------------------------------------|
| [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) | Generiert Inbandziffern bei einem Aufruf. Synchronous.               |
| [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone)     | Generiert einen bestimmten Satz von Tönen inband bei einem Aufruf. Synchronous. |



 

## <a name="call-accept-and-redirect"></a>Aufrufen von "Annehmen" und "Umleiten"



| Funktion                             | BESCHREIBUNG                                                                                               |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**lineAccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept)     | Akzeptiert einen angebotenen Anruf und beginnt damit, sowohl den Aufrufer (Ringback) als auch die aufgerufene Partei (Ring) zu warnen. Asynchron. |
| [**lineRedirect**](/windows/desktop/api/Tapi/nf-tapi-lineredirect) | Leitet einen Angebotsaufruf an eine andere Adresse um. Asynchron.                                              |



 

## <a name="call-reject"></a>Aufrufen von "Reject"



| Funktion                     | BESCHREIBUNG                                                               |
|------------------------------|---------------------------------------------------------------------------|
| [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) | Trennt einen Aufruf oder verabsehrt einen aufrufversuch, der in Bearbeitung ist. Asynchron. |



 

## <a name="call-hold"></a>Aufrufen von "Hold"



| Funktion                         | BESCHREIBUNG                                           |
|----------------------------------|-------------------------------------------------------|
| [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold)     | Legt den angegebenen Aufruf fest. Asynchron. |
| [**lineUnhold**](/windows/desktop/api/Tapi/nf-tapi-lineunhold) | Ruft einen gehaltenen Aufruf ab. Asynchron.                  |



 

## <a name="securing-calls"></a>Sichern von Aufrufen



| Funktion                                 | BESCHREIBUNG                                                                                                              |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**lineSecureCall**](/windows/desktop/api/Tapi/nf-tapi-linesecurecall) | Schützt einen vorhandenen Aufruf vor Störungen durch andere Ereignisse, z. B. Aufrufwartesignale für Datenverbindungen. Asynchron. |



 

## <a name="call-transfer"></a>Anrufübertragung



| Funktion                                             | BESCHREIBUNG                                                                                                    |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)       | Bereitet einen angegebenen Aufruf für die Übertragung an eine andere Adresse vor. Asynchron.                                       |
| [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) | Überträgt einen Anruf, der für die Übertragung an einen anderen Anruf eingerichtet wurde, oder nimmt an einer dreistufigen Konferenz teil. Asynchron. |
| [**lineBlindTransfer**](/windows/desktop/api/Tapi/nf-tapi-lineblindtransfer)       | Überträgt einen Aufruf an eine andere Partei. Asynchron.                                                               |
| [**lineSwapHold**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold)                 | Tauscht den aktiven Anruf durch den Anruf, der sich derzeit in der Beratungsaufforderung befindet. Asynchron.                              |



 

## <a name="call-conference"></a>Telefonkonferenz



| Funktion                                                         | BESCHREIBUNG                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)               | Bereitet einen bestimmten Aufruf auf das Hinzufügen einer anderen Partei vor. Asynchron.                                                                                                                               |
| [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) | Bereitet das Hinzufügen einer Partei zu einer vorhandenen Telefonkonferenz vor, indem die Telefonkonferenz in einen Wartezustand gestellt und ein Beratungsaufruf erstellt wird, der später dem Telefonat hinzugefügt werden kann. Asynchron. |
| [**lineAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineaddtoconference)               | Fügt einer vorhandenen Telefonkonferenz einen Beratungsanruf hinzu. Asynchron.                                                                                                                               |
| [**lineRemoveFromConference**](/windows/desktop/api/Tapi/nf-tapi-lineremovefromconference)     | Entfernt eine Partei aus einer Telefonkonferenz. Asynchron.                                                                                                                                                |



 

## <a name="call-park"></a>Call Park



| Funktion                         | BESCHREIBUNG                                          |
|----------------------------------|------------------------------------------------------|
| [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark)     | Bekommt einen bestimmten Aufruf an einer anderen Adresse. Asynchron. |
| [**lineUnpark**](/windows/desktop/api/Tapi/nf-tapi-lineunpark) | Ruft einen geparkten Aufruf ab. Asynchron.               |



 

## <a name="call-forwarding"></a>Anrufweiterleitung



| Funktion                           | BESCHREIBUNG                                             |
|------------------------------------|---------------------------------------------------------|
| [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) | Legt Aufrufweiterleitungsanforderungen fest oder bricht sie ab. Asynchron. |



 

## <a name="call-pickup"></a>Anrufannahme



| Funktion                         | BESCHREIBUNG                                                                                                                                                                                      |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) | Ruft eine Anrufwarnung an einer angegebenen Zieladresse ab und gibt ein Aufrufhandle für den übernommenen Aufruf zurück ([**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) kann auch für wartende Aufrufe verwendet werden). Asynchron. |



 

## <a name="sending-information-to-remote-party"></a>Senden von Informationen an die Remotepartei



| Funktion                                                   | BESCHREIBUNG                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**lineReleaseUserUserInfo**](/windows/desktop/api/Tapi/nf-tapi-linereleaseuseruserinfo) | Gibt Benutzerinformationen frei, wodurch das System diesen Speicher mit neuen Informationen überschreiben kann. Asynchron. |
| [**lineSendUserUserInfo**](/windows/desktop/api/Tapi/nf-tapi-linesenduseruserinfo)       | Sendet Benutzer-/Benutzerinformationen an die Remotepartei beim angegebenen Aufruf. Asynchron.                                |



 

## <a name="call-completion"></a>Aufrufabschluss



| Funktion                                         | BESCHREIBUNG                                      |
|--------------------------------------------------|--------------------------------------------------|
| [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)     | Platziert eine Anforderung zur Anrufvervollständigung. Asynchron.  |
| [**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall) | Bricht eine Aufrufabschlussanforderung ab. Asynchron. |



 

## <a name="setting-a-terminal-for-phone-conversations"></a>Festlegen eines Terminals für Telefon Konversationen



| Funktion                                   | BESCHREIBUNG                                                                                                                      |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) | Gibt das Terminalgerät an, an das die angegebene Zeile, Adressereignisse oder Aufrufmedienstreamereignisse weitergeleitet werden. Asynchron. |



 

## <a name="application-priority"></a>Anwendungspriorität



| Funktion                                         | BESCHREIBUNG                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**lineGetAppPriority**](/windows/desktop/api/Tapi/nf-tapi-linegetapppriority) | Ruft Informationen zur Priorität der Handoff- und/oder Unterstützten Telefonie für eine Anwendung ab. Synchronous. |
| [**lineSetAppPriority**](/windows/desktop/api/Tapi/nf-tapi-linesetapppriority) | Legt die Priorität der Übergabe und/oder der unterstützten Telefonie für eine Anwendung fest. Synchronous.              |



 

## <a name="service-provider-management"></a>Dienstanbieterverwaltung



| Funktion                                           | BESCHREIBUNG                                                           |
|----------------------------------------------------|-----------------------------------------------------------------------|
| [**lineAddProvider**](/windows/desktop/api/Tapi/nf-tapi-lineaddprovider)         | Installiert einen Telefoniedienstanbieter. Synchronous.                   |
| [**lineConfigProvider**](/windows/desktop/api/Tapi/nf-tapi-lineconfigprovider)   | Zeigt das Konfigurationsdialogfeld eines Dienstanbieters an. Synchronous. |
| [**lineRemoveProvider**](/windows/desktop/api/Tapi/nf-tapi-lineremoveprovider)   | Entfernt einen vorhandenen Telefoniedienstanbieter. Synchronous.          |
| [**lineGetProviderList**](/windows/desktop/api/Tapi/nf-tapi-linegetproviderlist) | Ruft eine Liste der installierten Dienstanbieter ab. Synchronous.         |



 

## <a name="agents"></a>Agents



| Funktion                                                     | BESCHREIBUNG                                                                                                                             |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)               | Ermöglicht der Anwendung den Zugriff auf proprietäre handlerspezifische Funktionen des Agenthandlers, der der Adresse zugeordnet ist. Asynchron. |
| [**lineGetAgentActivityList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista) | Ruft die Liste der Aktivitäten ab, aus denen eine Anwendung die Funktionen auswählt, die ein Agent ausführt. Asynchron.                    |
| [**lineGetAgentCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa)                 | Ruft die Agent-bezogenen Funktionen ab, die auf dem angegebenen Zeilengerät unterstützt werden. Asynchron.                                            |
| [**lineGetAgentGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista)       | Ruft die Liste der Agentgruppen ab, bei denen sich ein Agent beim Verteiler für automatische Aufrufe anmelden kann. Asynchron.                      |
| [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)             | Ruft den Agent-bezogenen Status für die angegebene Adresse ab. Asynchron.                                                                |
| [**lineSetAgentActivity**](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity)         | Legt den Agentaktivitätscode fest, der einer bestimmten Adresse zugeordnet ist. Asynchron.                                                        |
| [**lineSetAgentGroup**](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup)               | Legt die Agentgruppen fest, bei denen der Agent an einer bestimmten Adresse angemeldet ist. Asynchron.                                              |
| [**lineSetAgentState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate)               | Legt den Agentzustand fest, der einer bestimmten Adresse zugeordnet ist. Asynchron.                                                                |



 

## <a name="proxies"></a>Proxys



| Funktion                                       | BESCHREIBUNG                                                                         |
|------------------------------------------------|-------------------------------------------------------------------------------------|
| [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)   | Wird von einem registrierten Proxyanforderungshandler zum Generieren von TAPI-Nachrichten verwendet. Synchronous.  |
| [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) | Gibt den Abschluss einer Proxyanforderung durch einen registrierten Proxyhandler an. Synchronous. |



 

## <a name="quality-of-service"></a>Quality of Service (QoS, Dienstqualität)



| Funktion                                                           | BESCHREIBUNG                                                                                |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**lineSetCallQualityOfService**](/windows/desktop/api/Tapi/nf-tapi-linesetcallqualityofservice) | Fordert eine Änderung der Dienstqualitätsparameter für einen vorhandenen Aufruf an. Asynchron. |



 

## <a name="miscellaneous"></a>Sonstiges



| Funktion                                             | BESCHREIBUNG                                                                                           |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**lineSetCallData**](/windows/desktop/api/Tapi/nf-tapi-linesetcalldata)           | Legt den **CallData-Member** der [**LINECALLINFO-Struktur**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) fest. Asynchron. |
| [**lineSetCallTreatment**](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) | Legt die Töne fest, die der Benutzer anhört, wenn ein Aufruf nicht beantwortet oder zurückgehalten wird. Asynchron.               |
| [**lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) | Legt den Gerätestatus der Zeile fest. Asynchron.                                                            |



 

 

 



