---
title: Konfigurationsfunktionen der EAPHost-Peermethode
description: Erfahren Sie mehr über EAPHost-Peermethode-Konfigurationsfunktionen. Sehen Sie sich eine Liste der Konfigurationsfunktionen an, und zeigen Sie zusätzliche verfügbare Ressourcen an.
ms.assetid: ba5c90b2-5185-4810-84a2-d08e62e8105c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 355784647be6c6e13d4110303d544670e80ce09e7f9f99be02b662205e8ead82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785195"
---
# <a name="eaphost-peer-method-configuration-functions"></a>Konfigurationsfunktionen der EAPHost-Peermethode

Die Konfigurationsfunktionen der EAP-Peermethode-API lauten wie folgt.



| Funktion                                                                                                  | Beschreibung                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapPeerConfigBlob2Xml**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerconfigblob2xml)                                                    | Konvertiert das Konfigurationsblob in XML.                                                                                                                                                                                                                          |
| [**EapPeerConfigXml2Blob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerconfigxml2blob)                                                    | Konvertiert XML in das Konfigurationsblob.                                                                                                                                                                                                                        |
| [**EapPeerCredentialsXml2Blob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeercredentialsxml2blob)                                          | Konvertiert XML-Anmeldeinformationen in ein BLOB.                                                                                                                                                                                                                            |
| [**EapPeerFreeErrorMemory**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory)                                                  | Gibt den von EapHost-Peer-APIs zurückgegebenen EAP-fehlerspezifischen Arbeitsspeicher frei.                                                                                                                                                                                               |
| [**EapPeerFreeMemory**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreememory)                                                            | Gibt den von den OUT-Parametern der EAP-Methode zugewiesenen Arbeitsspeicher frei.                                                                                                                                                                                                      |
| [**EapPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeconfigui)                                                    | Löst das Benutzeroberflächendialogfeld für die spezifische Verbindungskonfiguration der EAP-Methode auf dem Client aus.                                                                                                                                                                   |
| [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui)                                                | Löst ein benutzerdefiniertes interaktives Benutzeroberflächendialogfeld aus, um Benutzeridentitätsinformationen für die EAP-Methode auf dem Client zu erhalten.                                                                                                                                          |
| [**EapPeerInvokeInteractiveUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeinteractiveui)                                          | Löst ein benutzerdefiniertes interaktives Benutzeroberflächendialogfeld für die EAP-Methode auf dem Client aus.                                                                                                                                                                              |
| [**EapPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields)                            | Definiert die Implementierung einer EAP-methodenspezifischen Funktion, die die Eingabefelder für die EAP-Anmeldeinformationen für einmaliges Anmelden (Single Sign-On, SSO) für diese EAP-Methode erhält.                                                                                                              |
| [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)                      | Definiert die Implementierung einer EAP-Supplicant-Funktion, die die Eingabefelder für interaktive Benutzeroberflächenkomponenten erhält, die auf dem Supplicant auslösung.                                                                                                     |
| [**EapPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuiblobfrominteractiveuiinputfields)  | Konvertiert Benutzerinformationen in ein Benutzerblob, das von EAPHost-Laufzeitfunktionen verwendet werden kann.                                                                                                                                                                   |
| [**EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) | Definiert die Implementierung einer EAP-methodenspezifischen Funktion, die ein EAP-Benutzer-Anmeldeinformationsblob aus einer [**EAP \_ CONFIG \_ INPUT FIELD \_ \_ ARRAY-Struktur**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) generiert, die von einem supplicant-Benutzer bereitgestellte Anmeldeinformationsdaten enthält. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[EAPHost-Peermethode Run-Time Functions](eaphost-peer-method-run-time-functions.md)
</dt> </dl>

 

 




