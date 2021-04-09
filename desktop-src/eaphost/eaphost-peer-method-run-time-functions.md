---
title: EAPHost-Peer Methode Run-Time-Funktionen
description: Erfahren Sie mehr über die API-Lauf Zeitfunktionen der EAPHost-Peer Methode. Hier finden Sie eine Liste der Funktionen und weitere verfügbare Ressourcen.
ms.assetid: fdfa595d-acf7-4489-88a8-113093567fe5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfde4adc8d509fcd5d67f9a33bd0617d605716db
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103858471"
---
# <a name="eaphost-peer-method-run-time-functions"></a>EAPHost-Peer Methode Run-Time-Funktionen

Die API-Lauf Zeitfunktionen der EAP-Peer Methode sind wie folgt.



| Funktion                                                                   | BESCHREIBUNG                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Eappeerbeginsession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession)                         | Startet eine neue Authentifizierungs Sitzung auf dem Peer-EAPHost.                                                                                                                                                                    |
| [**Eappeerendsession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession)                             | Beendet eine aktuelle EAP-Authentifizierungs Sitzung zwischen EAPHost und dem Peer.                                                                                                                                               |
| [**Eappeergetconfigblobanduserblob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob) | Ermöglicht Entwicklern von EAP-Methoden, die verschiedenen Verbindungs Eigenschaften und Benutzereigenschaften bereitzustellen, die von der-Methode unterstützt werden. EAPHost ruft diese Funktion auf, um die Verbindungs Eigenschaft und die Benutzer Eigenschaft der EAP-Methode zu erstellen. |
| [**Eappeergetidentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity)                           | Ruft die Identität für die EAP-Methode ab, die von aufgerufen wird.                                                                                                                                                                    |
| [**Eappeergetinfo**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo)                                   | Ruft einen Satz von Funktions Zeigern für eine Implementierung der geladenen EAP-Peer Methode ab.                                                                                                                                     |
| [**Eappeergetresponlattribute**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes)       | Ruft ein Array von EAP-Attributen aus der EAP-Methode ab.                                                                                                                                                                     |
| [**Eappeergetresponsepacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponsepacket)               | Ruft ein Antwortpaket von der EAP-Methode ab.                                                                                                                                                                              |
| [**Eappeergetresult**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresult)                               | Ruft das Ergebnis einer Authentifizierungs Sitzung aus der EAP-Methode ab.                                                                                                                                                        |
| [**Eappeergetuicontext**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetuicontext)                         | Ruft den Benutzeroberflächen Kontext aus der EAP-Methode ab.                                                                                                                                                                     |
| [**Eappeerinitialize**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize)                             | Initialisiert EAPHost für die Peer Methode.                                                                                                                                                                                    |
| [**Eappeerprocessrequestpacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket)         | Verarbeitet ein von EAPHost empfangenes Paket von einem Supplicant.                                                                                                                                                                   |
| [**Eappeersetanmelde Informationen**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials)                     | Stellt neue oder aktualisierte Benutzer Anmelde Informationen für die EAP-Methode bereit.                                                                                                                                                                 |
| [**Eappeerabtresponlattribute**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes)       | Stellt ein aktualisiertes Array von EAP-Attributen für die EAP-Methode bereit.                                                                                                                                                              |
| [**Eappeerabltuicontext**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetuicontext)                         | Stellt einen Kontext für die Benutzeroberfläche der EAP-Methode bereit.                                                                                                                                                                        |
| [**Eappeershutdown**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeershutdown)                                 | Fährt die EAP-Methode herunter und bereitet das Entladen der entsprechenden DLL vor.                                                                                                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[EAPHost-Peer Methoden-Konfigurationsfunktionen](eaphost-peer-method-run-time-functions.md)
</dt> </dl>

 

 




