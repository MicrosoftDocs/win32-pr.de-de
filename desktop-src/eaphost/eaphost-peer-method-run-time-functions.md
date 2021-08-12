---
title: EAPHost-Peermethode Run-Time Funktionen
description: Erfahren Sie mehr über Laufzeitfunktionen der EAPHost-Peermethoden-API. Sehen Sie sich eine Liste der Funktionen an, und zeigen Sie zusätzliche verfügbare Ressourcen an.
ms.assetid: fdfa595d-acf7-4489-88a8-113093567fe5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb3134a2b118b4bce4511e79d8d9ef58708f6b1c2bd7a93ed820fc16ec073914
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118275023"
---
# <a name="eaphost-peer-method-run-time-functions"></a>EAPHost-Peermethode Run-Time Funktionen

Die Laufzeitfunktionen der EAP-Peermethoden-API sind wie folgt.



| Funktion                                                                   | Beschreibung                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession)                         | Startet eine neue Authentifizierungssitzung auf dem Peer-EAPHost.                                                                                                                                                                    |
| [**EapPeerEndSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession)                             | Beendet eine aktuelle EAP-Authentifizierungssitzung zwischen EAPHost und dem Peer.                                                                                                                                               |
| [**EapPeerGetConfigBlobAndUserBlob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob) | Ermöglicht Es EAP-Methodenentwicklern, die verschiedenen Verbindungseigenschaften und Benutzereigenschaften bereitzustellen, die von der -Methode unterstützt werden. EAPHost ruft diese Funktion auf, um die Verbindungseigenschaft und die Benutzereigenschaft der EAP-Methode zu erstellen. |
| [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity)                           | Ruft die Identität für die EAP-Methode ab, die aufruft.                                                                                                                                                                    |
| [**EapPeerGetInfo**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo)                                   | Ruft einen Satz von Funktionszeigern für eine Implementierung der geladenen EAP-Peermethode ab.                                                                                                                                     |
| [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes)       | Ruft ein Array von EAP-Attributen aus der EAP-Methode ab.                                                                                                                                                                     |
| [**EapPeerGetResponsePacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponsepacket)               | Ruft ein Antwortpaket von der EAP-Methode ab.                                                                                                                                                                              |
| [**EapPeerGetResult**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresult)                               | Ruft das Ergebnis einer Authentifizierungssitzung von der EAP-Methode ab.                                                                                                                                                        |
| [**EapPeerGetUIContext**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetuicontext)                         | Ruft den Benutzeroberflächenkontext aus der EAP-Methode ab.                                                                                                                                                                     |
| [**EapPeerInitialize**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize)                             | Initialisiert EAPHost für die Peermethode.                                                                                                                                                                                    |
| [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket)         | Verarbeitet ein Paket, das von EAPHost von einer Supplizierung empfangen wurde.                                                                                                                                                                   |
| [**EapPeerSetCredentials**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials)                     | Stellt neue oder aktualisierte Benutzeranmeldeinformationen für die EAP-Methode bereit.                                                                                                                                                                 |
| [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes)       | Stellt ein aktualisiertes Array von EAP-Attributen für die EAP-Methode bereit.                                                                                                                                                              |
| [**EapPeerSetUIContext**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetuicontext)                         | Stellt einen Benutzeroberflächenkontext für die EAP-Methode bereit.                                                                                                                                                                        |
| [**EapPeerShutdown**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeershutdown)                                 | Fährt die EAP-Methode herunter und bereitet das Entladen der entsprechenden DLL vor.                                                                                                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurationsfunktionen für EAPHost-Peermethoden](eaphost-peer-method-run-time-functions.md)
</dt> </dl>

 

 




