---
title: EAPHost-Peer Methoden-Konfigurationsfunktionen
description: Erfahren Sie mehr über die Konfigurationsfunktionen der EAPHost-Peer Methode. Hier finden Sie eine Liste der Konfigurationsfunktionen und weitere verfügbare Ressourcen.
ms.assetid: ba5c90b2-5185-4810-84a2-d08e62e8105c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3081f8a54482c48c7c506a25bfaf7f18cf3193ff
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106341554"
---
# <a name="eaphost-peer-method-configuration-functions"></a>EAPHost-Peer Methoden-Konfigurationsfunktionen

Die API-Konfigurationsfunktionen der EAP-Peer Methode sind wie folgt.



| Funktion                                                                                                  | BESCHREIBUNG                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapPeerConfigBlob2Xml**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerconfigblob2xml)                                                    | Konvertiert das konfigurationsblob in XML.                                                                                                                                                                                                                          |
| [**EapPeerConfigXml2Blob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerconfigxml2blob)                                                    | Konvertiert XML in das Konfigurations-BLOB.                                                                                                                                                                                                                        |
| [**EapPeerCredentialsXml2Blob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeercredentialsxml2blob)                                          | Konvertiert XML-Anmelde Informationen in ein BLOB.                                                                                                                                                                                                                            |
| [**Eappeerfreerrormemory**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory)                                                  | Gibt den von EAPHost-Peer-APIs zurückgegebenen EAP-Fehler spezifischen Speicher frei.                                                                                                                                                                                               |
| [**Eappeerfrememory**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreememory)                                                            | Gibt den von EAP-Methoden out-Parametern zugewiesenen Arbeitsspeicher frei.                                                                                                                                                                                                      |
| [**Eappeerinvokeconfigui**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeconfigui)                                                    | Löst das Benutzeroberflächen Dialogfeld für die Verbindungs Konfiguration der EAP-Methode auf dem Client aus.                                                                                                                                                                   |
| [**Eappeerinvokeidentityui**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui)                                                | Löst ein benutzerdefiniertes Dialogfeld für die interaktive Benutzeroberfläche aus, um Benutzer Identitätsinformationen für die EAP-Methode auf dem Client abzurufen.                                                                                                                                          |
| [**Eappeerinvokeinteractiveui**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeinteractiveui)                                          | Löst ein benutzerdefiniertes Dialogfeld für die interaktive Benutzeroberfläche für die EAP-Methode auf dem Client aus.                                                                                                                                                                              |
| [**Eappeerquerykredentialinputfields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields)                            | Definiert die Implementierung einer EAP-Methoden spezifischen Funktion, die die Eingabefelder für die EAP-Anmelde Informationen für die einmalige Anmeldung (Single Sign-on, SSO) für diese EAP-Methode abruft.                                                                                                              |
| [**Eappeerqueryinteractiveuiinputfields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)                      | Definiert die Implementierung einer EAP-Supplicant-Funktion, die die Eingabefelder für interaktive Benutzeroberflächen Komponenten abruft, um Sie für den Supplicant zu erhöhen.                                                                                                     |
| [**Eappeerqueryuiblobfrominteractiveuiinputfields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuiblobfrominteractiveuiinputfields)  | Konvertiert Benutzerinformationen in ein benutzerblob, das von EAPHost-Lauf Zeitfunktionen verwendet werden kann.                                                                                                                                                                   |
| [**Eappeerqueryuserblobfromkredentialinputfields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) | Definiert die Implementierung einer EAP-Methoden spezifischen Funktion, die ein EAP-Benutzer Anmelde Informations-BLOB aus einer [**EAP- \_ config- \_ Eingabe \_ Feld \_ Array**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) -Struktur generiert, die Anmelde Informationsdaten enthält, die von einem Supplicant-Benutzer bereitgestellt werden. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[EAPHost-Peer Methode Run-Time-Funktionen](eaphost-peer-method-run-time-functions.md)
</dt> </dl>

 

 




