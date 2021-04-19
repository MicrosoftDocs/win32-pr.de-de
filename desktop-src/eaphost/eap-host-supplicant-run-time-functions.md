---
title: EAPHost-Supplicant-Run-Time Funktionen
description: Erfahren Sie mehr über EAPHost-Supplicant-Lauf Zeitfunktionen wie eaphosteterbeginsession und eaphostpeer ergetresult.
ms.assetid: b1c473ba-9a12-4929-b4d0-27262117e9c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2bbb6aee83cff6354877b661acb7f3389f5b77b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106342160"
---
# <a name="eaphost-supplicant-run-time-functions"></a>EAPHost-Supplicant-Run-Time Funktionen

Die Lauf Zeitfunktionen der EAP-Supplicant-API lauten wie folgt.



| Funktion                                                                     | BESCHREIBUNG                                                                                                                                                                                                          |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Eaphosteterbeginsession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)                   | Startet eine EAP-Authentifizierungs Sitzung.                                                                                                                                                                                |
| [**Eaphostpeer-clearconnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection)             | Hält alle zukünftigen Rückrufe an den [**notificationhandler**](/previous-versions/windows/desktop/api) an, der von dem aufrufenden Supplicant an EAPHost in einem vorherigen Aufruf von [**eaphostpeer erbeginsession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)bereitgestellt wird. |
| [**Eaphostpeer-EndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession)                       | Beendet eine aktuelle EAP-Authentifizierungs Sitzung zwischen EAPHost und dem aufrufenden Supplicant.                                                                                                                          |
| [**Eaphostpeerfreeaperror**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerfreeeaperror)                   | Gibt den von den EAPHost-APIs zurückgegebenen EAP-Fehler spezifischen Speicher frei.                                                                                                                                                        |
| [**Eaphostfreeruntimememory**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreememory)                    | Gibt Speicherplatz frei, der von Lauf Zeit-APIs verwendet wird.                                                                                                                                                                         |
| [**Eaphostpeergetauthstatus**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetauthstatus)                 | Ruft den aktuellen EAP-Authentifizierungs Status des Supplicant von EAPHost ab.                                                                                                                                             |
| [**Eaphostpeer ergetidentity**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetidentity)                     | Fordert Identitätsinformationen von den inneren Methoden an.                                                                                                                                                                |
| [**Eaphostpeer Attribute**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes) | Ruft ein Array von EAP-Authentifizierungs Attributen von EAPHost ab.                                                                                                                                                      |
| [**Eaphostpeer ergetresult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult)                         | Ruft das Authentifizierungs Ergebnis für die angegebene EAP-Authentifizierungs Sitzung ab.                                                                                                                                      |
| [**Eaphostpeer-getsendpacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetsendpacket)                 | Ruft ein Paket von EAPHost ab, das an den Authentifikator gesendet wird.                                                                                                                                                          |
| [**Eaphostetergetuicontext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext)                   | Ruft den Benutzeroberflächen Kontext für den Supplicant von EAPHost ab, der in den [**eaphosteterinvokeinteractiveui**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) -APIs für den Supplicant verwendet wird.                             |
| [**Eaphostpeer Initialize**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerinitialize)                       | Initialisiert EAPHost für den Supplicant. [**Eaphostinitialize**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerinitialize) und [**eaphostuninitialize**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeeruninitialize) müssen als Paar aufgerufen werden.                                      |
| [**Eaphostpeer-processreceivedpacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket) | Überträgt das EAP-Paket an EAPHost, nachdem ein EAP-Paket vom Server empfangen wurde.                                                                                                                             |
| [**Eaphostpeer Attribute**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) | Stellt aktualisierte EAP-Authentifizierungs Attribute für EAPHost bereit.                                                                                                                                                           |
| [**Eaphostpeer Name**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext)                   | Stellt einen neuen oder aktualisierten Benutzeroberflächen Kontext für die EAP-Peer Methode bereit, die auf EAPHost geladen wurde.                                                                                                                           |
| [**Eaphostpeer-Initialize**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeeruninitialize)                   | Vereinigt EAPHost für den Supplicant. [**Eaphostinitialize**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerinitialize) und [**eaphostuninitialize**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeeruninitialize) müssen als Paar aufgerufen werden.                                      |



 

 

 




