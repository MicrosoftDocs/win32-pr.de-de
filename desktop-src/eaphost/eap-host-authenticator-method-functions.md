---
title: EAPHost Authenticator-Methodenfunktionen
description: Erfahren Sie mehr über EAPHost Authenticator-Methoden-API-Funktionen, z. B. EapMethodAuthenticatorFreeErrorMemory.
ms.assetid: 319516ee-b21d-4375-8c90-e3abe0a457e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f3cc21d636c2a1b107897c3b000fca3f279288e13c14d1219f5b13515c2e8a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984270"
---
# <a name="eaphost-authenticator-method-functions"></a>EAPHost Authenticator-Methodenfunktionen

Die API-Funktionen der EAPHost-Authenticator-Methode sind wie folgt.



| Funktion                                                                                               | Beschreibung                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapMethodAuthenticatorBeginSession**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession)                       | Erstellt eine neue EAP-Authentifizierungssitzung auf dem Server EAPHost.                                                                                                                             |
| [**EapMethodAuthenticatorEndSession**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorendsession)                           | Schließt eine EAP-Authentifizierungssitzung auf dem Server EAPHost.                                                                                                                                 |
| [**EapMethodAuthenticatorFreeErrorMemory**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorfreeerrormemory)                 | Gibt fehlerspezifischen Speicher frei, der von der EAP-Authentifikatormethode belegt wird.                                                                                                                   |
| [**EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes)                     | Ruft ein Array von EAP-Authentifizierungsattributen aus der EAP-Authentifikatormethode ab.                                                                                                        |
| [**EapMethodAuthenticatorGetInfo**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetinfo)                                 | Ruft einen Satz von Funktionszeigern für eine Implementierung der geladenen EAP-Authentifikatormethode ab.                                                                                            |
| [**EapMethodAuthenticatorGetResult**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetresult)                             | Ruft das Authentifizierungsergebnis von der EAP-Authentifikatormethode ab.                                                                                                                        |
| [**EapMethodAuthenticatorInitialize**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorinitialize)                           | Initialisiert eine EAP-Authentifikatormethode für den Server EAPHost.                                                                                                                             |
| [**EapMethodAuthenticatorInvokeConfigUI**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorinvokeconfigui)                   | Definiert eine Funktion, die die Benutzeroberfläche für die Verbindungskonfiguration der EAP-Methode auf dem Client auslöst.                                                                           |
| [**EapMethodAuthenticatorReceivePacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket)                     | Verarbeitet ein vom Server EAPHost empfangenes EAP-Authentifizierungspaket und gibt eine Antwortaktion zurück.                                                                                        |
| [**EapMethodAuthenticatorSendPacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsendpacket)                           | Ruft ein Authentifizierungspaket von der EAP-Authentifikatormethode ab, das an die Unterstützung gesendet werden soll.                                                                                               |
| [**EapMethodAuthenticatorSetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes)                     | Stellt aktualisierte EAP-Authentifizierungsattribute bereit, die für die EAP-Authentifikatormethode festgelegt werden sollen.                                                                                                      |
| [**EapMethodAuthenticatorShutdown**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorshutdown)                               | Fährt die EAP-Authentifikatormethode herunter und bereitet das Entladen vom Server EAPHost vor.                                                                                                  |
| [**EapMethodAuthenticatorUpdateInnerMethodParams**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorupdateinnermethodparams) | Aktualisiert die Einstellungen der EAP-Authentifizierungssitzung, die zuvor durch einen Aufruf von [**EapMethodAuthenticatorBeginSession**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession) vom Server EAPHost festgelegt wurden. |



 

 

 




