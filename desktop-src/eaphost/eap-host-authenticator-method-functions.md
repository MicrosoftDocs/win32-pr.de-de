---
title: EAPHost-Authenticator-Methoden Funktionen
description: Erfahren Sie mehr über die API-Funktionen der EAPHost-Authenticator-Methode, z. b. eapmethodauthenticatorfreerrormemory.
ms.assetid: 319516ee-b21d-4375-8c90-e3abe0a457e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93fac5114085fe6c620084d564bbff97cc3b4535
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106342163"
---
# <a name="eaphost-authenticator-method-functions"></a>EAPHost-Authenticator-Methoden Funktionen

Die API-Funktionen der EAPHost-Authenticator-Methode lauten wie folgt.



| Funktion                                                                                               | BESCHREIBUNG                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Eapmethodauthentigorbeginsession**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession)                       | Erstellt eine neue EAP-Authentifizierungs Sitzung auf dem Server EAPHost.                                                                                                                             |
| [**Eapmethodauthentianorendsession**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorendsession)                           | Schließt eine EAP-Authentifizierungs Sitzung auf dem Server-EAPHost.                                                                                                                                 |
| [**Eapmethodauthentietorfreerrormemory**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorfreeerrormemory)                 | Gibt Fehler spezifischen Speicher frei, der von der EAP Authenticator-Methode zugeordnet wird.                                                                                                                   |
| [**Eapmethodauthentitororgetattributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes)                     | Ruft ein Array von EAP-Authentifizierungs Attributen aus der EAP Authenticator-Methode ab.                                                                                                        |
| [**Eapmethodauthentiaseorgetinfo**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetinfo)                                 | Ruft einen Satz von Funktions Zeigern für eine Implementierung der geladenen EAP Authenticator-Methode ab.                                                                                            |
| [**Eapmethodauthentianorgetresult**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetresult)                             | Ruft das Authentifizierungs Ergebnis aus der EAP Authenticator-Methode ab.                                                                                                                        |
| [**Eapmethodauthentianorinitialize**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorinitialize)                           | Initialisiert eine EAP-Authenticator-Methode für den Server EAPHost.                                                                                                                             |
| [**Eapmethodauthentipeorinvokeconfigui**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorinvokeconfigui)                   | Definiert eine Funktion, die das Dialogfeld Benutzeroberfläche der Verbindungs Konfiguration der EAP-Methode auf dem Client auslöst.                                                                           |
| [**Eapmethodauthenti. receivepacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket)                     | Verarbeitet ein vom Server EAPHost empfangenes EAP-Authentifizierungs Paket und gibt eine Antwort Aktion zurück.                                                                                        |
| [**Eapmethodauthentianorsendpacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsendpacket)                           | Ruft ein Authentifizierungs Paket von der EAP Authenticator-Methode ab, das an den Supplicant gesendet werden soll.                                                                                               |
| [**Eapmethodauthentitoror\tattributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes)                     | Stellt aktualisierte EAP-Authentifizierungs Attribute bereit, die für die EAP-Authenticator-Methode festgelegt werden.                                                                                                      |
| [**Eapmethodauthenti| Herunterfahren**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorshutdown)                               | Fährt die EAP-Authenticator-Methode herunter und bereitet Sie darauf vor, Sie vom Server EAPHost zu entladen.                                                                                                  |
| [**Eapmethodauthentianorupdateinnermethodparametriams**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorupdateinnermethodparams) | Aktualisiert die Einstellungen der EAP-Authentifizierungs Sitzung, die zuvor durch einen Aufruf von [**eapmethodauthenticatorbeginsession**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession) vom Server EAPHost festgelegt wurden. |



 

 

 




