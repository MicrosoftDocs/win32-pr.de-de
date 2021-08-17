---
title: EAPHost Supplicant Run-Time Functions
description: Erfahren Sie mehr über EAPHost Supplicant-Laufzeitfunktionen wie EapHostPeerBeginSession und EapHostPeerGetResult.
ms.assetid: b1c473ba-9a12-4929-b4d0-27262117e9c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97481347535de03cb1d3c04f341f382c270f0ae89482060e9952c38cfbdc5b98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785328"
---
# <a name="eaphost-supplicant-run-time-functions"></a>EAPHost Supplicant Run-Time Functions

Die Laufzeitfunktionen der EAP-Supplicant-API lauten wie folgt.



| Funktion                                                                     | BESCHREIBUNG                                                                                                                                                                                                          |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)                   | Startet eine EAP-Authentifizierungssitzung.                                                                                                                                                                                |
| [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection)             | Hält alle zukünftigen Rückrufe an den [**NotificationHandler**](/previous-versions/windows/desktop/api) an, die vom aufrufenden Supplicant für EAPHost in einem vorherigen Aufruf von [**EapHostPeerBeginSession bereitgestellt wurden.**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) |
| [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession)                       | Beendet eine aktuelle EAP-Authentifizierungssitzung zwischen EAPHost und dem aufrufenden Supplicant.                                                                                                                          |
| [**EapHostPeerFreeEapError**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerfreeeaperror)                   | Gibt den von EAPHost-APIs zurückgegebenen EAP-fehlerspezifischen Arbeitsspeicher frei.                                                                                                                                                        |
| [**EapHostFreeRuntimeMemory**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreememory)                    | Gibt speicherplatz frei, der von Laufzeit-APIs verwendet wird.                                                                                                                                                                         |
| [**EapHostPeerGetAuthStatus**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetauthstatus)                 | Erhält den aktuellen EAP-Authentifizierungsstatus des Supplicants von EAPHost.                                                                                                                                             |
| [**EapHostPeerGetIdentity**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetidentity)                     | Fordert Identitätsinformationen von den inneren Methoden an.                                                                                                                                                                |
| [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes) | Erhält ein Array von EAP-Authentifizierungsattributen von EAPHost.                                                                                                                                                      |
| [**EapHostPeerGetResult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult)                         | Erhält das Authentifizierungsergebnis für die angegebene EAP-Authentifizierungssitzung.                                                                                                                                      |
| [**EapHostPeerGetSendPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetsendpacket)                 | Erhält ein Paket von EAPHost, das an den Authentator gesendet werden soll.                                                                                                                                                          |
| [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext)                   | Erhält den Benutzeroberflächenkontext für das Supplicant von EAPHost, das in den [**EapHostPeerInvokeInteractiveUI-APIs**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) für den Supplicant verwendet wird.                             |
| [**EapHostPeerInitialize**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerinitialize)                       | Initialisiert EAPHost für den Supplicant. [**EapHostInitialize und**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerinitialize) [**EapHostUninitialize**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeeruninitialize) müssen als Paar aufgerufen werden.                                      |
| [**EapHostPeerProcessReceivedPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket) | Überträgt das EAP-Paket an EAPHost, nachdem ein EAP-Paket vom Server empfangen wurde.                                                                                                                             |
| [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) | Bietet aktualisierte EAP-Authentifizierungsattribute für EAPHost.                                                                                                                                                           |
| [**EapHostPeerSetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext)                   | Stellt einen neuen oder aktualisierten Benutzeroberflächenkontext für die auf EAPHost geladene EAP-Peermethode bereit.                                                                                                                           |
| [**EapHostPeerUninitialize**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeeruninitialize)                   | Unitisiert EapHost für den Supplicant. [**EapHostInitialize und**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerinitialize) [**EapHostUninitialize**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeeruninitialize) müssen als Paar aufgerufen werden.                                      |



 

 

 




