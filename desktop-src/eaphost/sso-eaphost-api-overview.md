---
title: Übersicht über die SSO EAPHost-API
description: Bietet eine Übersicht über die EAPHost-APIs, die einmaliges Anmelden (Single Sign-On, SSO) unterstützen.
ms.assetid: 3c01d10a-9098-4965-8983-c7f65be31884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a38c6dd35dd2506f8aa26412b09db0f9c9951241bd0f017ed5e55d7f5484b86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118085874"
---
# <a name="sso-eaphost-api-overview"></a>Übersicht über die SSO EAPHost-API

Dieses Thema bietet eine Übersicht über die EAPHost-APIs, die einmaliges Anmelden (Single Sign-On, SSO) unterstützen. Spezifische SSO-Szenarien finden Sie unter [SSO EAPHost Scenarios](why-eaphost-sso.md).

## <a name="eaphost-enumerations"></a>EAPHost-Enumerationen

Die folgenden Enumerationen unterstützen SSO.



| Name                                                                    | Zweck                                                                                      |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**\_ \_ EAP-KONFIGURATIONSEINGABEFELDTYP \_ \_**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_config_input_field_type)  | Definiert eine Reihe möglicher Eingabefeldtypen, die beim Abfragen von Benutzeranmeldeinformationen verfügbar sind.    |
| [**\_EAP INTERACTIVE \_ \_ \_ UI-DATENTYP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_config_input_field_type) | Gibt die Typen interaktiver Benutzeroberflächenkontextdaten an, die für bestimmte API-Aufrufe bereitgestellt werden. |



 

## <a name="eaphost-structures"></a>EAPHost-Strukturen

Die folgenden Datenstrukturen unterstützen SSO.



| Name                                                                     | Zweck                                                                                                                                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ EAP-KONFIGURATIONSEINGABEFELDDATEN \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data)   | Enthält die Daten, die einem einzelnen Eingabefeld zugeordnet sind.                                                                                                                         |
| [**EAP \_ CONFIG \_ INPUT \_ FIELD \_ ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) | Enthält eine Reihe von [**EAP \_ CONFIG \_ INPUT FIELD \_ \_ DATA-Strukturen,**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) die zusammen die vom Benutzer abgerufenen Benutzereingabefelddaten enthalten. |
| [**EAP \_ INTERACTIVE \_ UI \_ DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)            | Enthält Konfigurationsinformationen für interaktive Benutzeroberflächenkomponenten, die bei einer EAP-Supplizierung ausgelöst werden.                                                                                   |
| [**EAP \_ CRED \_ REQ**](eap-cred-req.md)                                   | Enthält sowohl die alten als auch die neuen EAP-Anmeldeinformationen für Anmeldeinformationsänderungsvorgänge.                                                                                               |
| [**EAP \_ CRED \_ RESP**](eap-cred-resp.md)                                 | Enthält sowohl die alten als auch die neuen EAP-Anmeldeinformationen für Anmeldeinformationsänderungsvorgänge.                                                                                               |
| [**EAP \_ CRED \_ EXPIRY \_ REQ**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)                    | Enthält sowohl die alten als auch die neuen EAP-Anmeldeinformationen für Anmeldeinformationsablaufvorgänge.                                                                                                 |
| [**EAP \_ CRED \_ EXPIRY \_ RESP**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))              | Enthält sowohl die alten als auch die neuen EAP-Anmeldeinformationen für Anmeldeinformationsablaufvorgänge.                                                                                                 |



 

## <a name="eaphost-peer-supplicant-apis"></a>EAPHost-Peer-APIs (Suppli suppli suppli über)

Die folgenden unterstützenden Funktionen unterstützen SSO.

Die Funktionen [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields) und [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) gelten ausschließlich für einmaliges Anmelden.



| Name                                                                                                             | Zweck                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | Aufgerufene Reihenfolge |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields)                     | Ruft die Eingabefelder für interaktive UI-Komponenten ab, die auf der Supplizierung ausgelöst werden sollen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | 4            |
| [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)                           | Ermöglicht dem Benutzer, zu bestimmen, welche Art von Anmeldeinformationen von den Methoden zum Durchführen der Authentifizierung in einem SSO-Szenario benötigt werden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | 1            |
| [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields) | Konvertiert Benutzerinformationen in ein Benutzer-BLOB, das von EAPHost-Laufzeitfunktionen genutzt werden kann.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | 5            |
| [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields)   | Ruft ein Blob für Anmeldeinformationen ab, mit dem die Authentifizierung anhand von Benutzereingaben gestartet werden kann, die von der SSO-Benutzeroberfläche empfangen wurden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 2            |
| [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)                                                       | Die Suppliplizierung verwendet das **EAP \_ FLAG PRE \_ \_ LOGON-Flag,** um anzugeben, dass EAPHost SSO bereitstellen soll. Wenn der Aktionscode [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) zurückgegeben wird, ruft EAPHost [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)auf und ruft dann [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields) auf.<br/> Wenn der [Aktionscode EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) nicht zurückgegeben wird, fährt EAPHost mit der regulären, nicht SSO-Aufrufsequenz fort. Weitere Informationen finden Sie unter [Suppli api call sequence (Api-Aufrufsequenz für Supplipli suppliplizieren).](supplicant-api-call-sequence.md)<br/> | 3            |



 

## <a name="eaphost-peer-method-apis"></a>EAPHost-Peermethoden-APIs

Die folgenden Peerfunktionen unterstützen SSO.

Die Funktionen [**EapPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields) und [**EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) gelten ausschließlich für einmaliges Anmelden.



| Name                                                                                                      | Zweck                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Aufgerufene Reihenfolge |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)                      | Definiert die Implementierung einer EAP-Methoden-API, die die Eingabefelder für interaktive UI-Komponenten bereitstellt, die auf der Supplizierung ausgelöst werden sollen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | 4            |
| [**EapPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields)                            | Definiert die Implementierung einer EAP-methodenspezifischen Funktion, die die Eingabefelder für EAP-SSO-Anmeldeinformationen für diese EAP-Methode erhält.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | 1            |
| [**EapPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuiblobfrominteractiveuiinputfields)  | Konvertiert Benutzerinformationen in ein Benutzer-BLOB, das von EAPHost-Laufzeitfunktionen genutzt werden kann.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | 5            |
| [**EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) | Definiert die Implementierung einer EAP-Methodenfunktion, die die Benutzer-BLOB-Daten erhält, die von der interaktiven SSO-Benutzeroberfläche bereitgestellt werden, die auf der Supplizierung ausgelöst wird.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | 2            |
| [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession)                                                        | Das **Flag EAP \_ FLAG PRE \_ \_ LOGON** gibt an, dass EAPHost SSO bereitstellen soll. Wenn der **Aktionscode EapPeerResponseInvokeUI** in einem SSO-Szenario zurückgegeben wird, ruft EAPHost [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)auf und ruft dann [**EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) auf.<br/> Wenn der **EapPeerResponseInvokeUI-Aktionscode** nicht zurückgegeben wird, fährt EAPHost mit der regulären, nicht SSO-Aufrufsequenz fort. Weitere Informationen finden Sie unter Aufrufsequenz der [Peermethoden-API.](peer-method-api-call-sequence.md)<br/> | 3            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[SSO und PLAP](understanding-sso-and-plap.md)
</dt> <dt>

[SSO EAPHost-Szenarien](why-eaphost-sso.md)
</dt> </dl>

 

