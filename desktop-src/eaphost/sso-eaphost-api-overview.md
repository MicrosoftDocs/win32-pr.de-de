---
title: SSO-EAPHost-API (Übersicht)
description: Bietet eine Übersicht über die EAPHost-APIs, die einmaliges Anmelden (Single-Sign-on, SSO) unterstützen.
ms.assetid: 3c01d10a-9098-4965-8983-c7f65be31884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3c047205946293c2116c1ab3537ad4d9250857d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038941"
---
# <a name="sso-eaphost-api-overview"></a>SSO-EAPHost-API (Übersicht)

Dieses Thema enthält eine Übersicht über die EAPHost-APIs, die einmaliges Anmelden (Single-Sign-on, SSO) unterstützen. Informationen zu bestimmten SSO-Szenarien finden Sie unter [SSO-EAPHost-Szenarios](why-eaphost-sso.md).

## <a name="eaphost-enumerations"></a>EAPHost-Enumerationen

Die folgenden Enumerationen unterstützen SSO.



| Name                                                                    | Zweck                                                                                      |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**\_ \_ Eingabe \_ \_ Feldtyp der EAP-Konfiguration**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_config_input_field_type)  | Definiert einen Satz möglicher Eingabefeld Typen, die beim Abfragen von Benutzer Anmelde Informationen verfügbar sind.    |
| [**interaktiver EAP- \_ \_ UI- \_ \_ Datentyp**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_config_input_field_type) | Gibt die Typen von interaktiven UI-Kontext Daten an, die für bestimmte Supplicant API-Aufrufe bereitgestellt werden. |



 

## <a name="eaphost-structures"></a>EAPHost-Strukturen

Die folgenden Datenstrukturen unterstützen einmaliges Anmelden (SSO).



| Name                                                                     | Zweck                                                                                                                                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ Eingabe \_ Feld \_ Daten der EAP-Konfiguration**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data)   | Enthält die Daten, die einem einzelnen Eingabefeld zugeordnet sind.                                                                                                                         |
| [**\_ \_ Eingabe \_ Feld \_ Array der EAP-Konfiguration**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) | Enthält einen Satz von [**Datenstrukturen der EAP- \_ Konfigurations \_ Eingabe \_ Felder \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) , die zusammen die Benutzereingabe Feld Daten enthalten, die vom Benutzer abgerufen werden. |
| [**interaktive EAP- \_ \_ Benutzeroberflächen \_ Daten**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)            | Enthält Konfigurationsinformationen für interaktive Benutzeroberflächen Komponenten, die auf einem EAP-Supplicant ausgelöst werden.                                                                                   |
| [**EAP- \_ Kred- \_ req**](eap-cred-req.md)                                   | Enthält sowohl die alten als auch die neuen EAP-Anmelde Informationen für einen Vorgang zum Ändern von Anmelde Informationen.                                                                                               |
| [**EAP-Benutzer \_ -e/a \_**](eap-cred-resp.md)                                 | Enthält sowohl die alten als auch die neuen EAP-Anmelde Informationen für einen Vorgang zum Ändern von Anmelde Informationen.                                                                                               |
| [**EAP- \_ \_ ablaufungsablauf- \_ req**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)                    | Enthält sowohl die alten als auch die neuen EAP-Anmelde Informationen für Ablauf Vorgänge für Anmelde Informationen.                                                                                                 |
| [**EAP- \_ \_ Ablaufs Ablauf (e) \_**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))              | Enthält sowohl die alten als auch die neuen EAP-Anmelde Informationen für Ablauf Vorgänge für Anmelde Informationen.                                                                                                 |



 

## <a name="eaphost-peer-supplicant-apis"></a>EAPHost-Peer-APIs (Supplicant)

Die folgenden Supplicant-Funktionen unterstützen SSO.

Die [**eaphostpeer-querykredentialinputfields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields) -und [**eaphostpeer-queryuserblobfromkredentialinputfields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) -Funktionen sind exklusiv für SSO.



| Name                                                                                                             | Zweck                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | Aufgerufene Reihenfolge |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [**Eaphostpeer-queryinteractiveuiinputfields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields)                     | Ruft die Eingabefelder für interaktive UI-Komponenten ab, die für den Supplicant ausgelöst werden sollen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | 4            |
| [**Eaphostpeer-querykredentialinputfields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)                           | Ermöglicht es dem Benutzer zu ermitteln, welche Art von Anmelde Informationen von den Methoden zum Durchführen der Authentifizierung in einem SSO-Szenario benötigt werden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | 1            |
| [**Eaphostpeer-queryuiblobfrominteractiveuiinputfields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields) | Konvertiert Benutzerinformationen in ein benutzerblob, das von EAPHost-Lauf Zeitfunktionen verwendet werden kann.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | 5            |
| [**Eaphostpeer-queryuserblobfromkredentialinputfields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields)   | Ruft ein Anmelde Informations-BLOB ab, das zum Starten der Authentifizierung von Benutzereingaben verwendet werden kann, die von der SSO-Benutzeroberfläche empfangen werden                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 2            |
| [**Eaphosteterbeginsession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)                                                       | Der Supplicant verwendet das **EAP- \_ Flag " \_ Pre \_ Logon** ", um anzugeben, dass EAPHost SSO bereitstellen soll. Wenn der [eaphosteterresponseinvokeui](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) -Aktions Code zurückgegeben wird, ruft EAPHost [**eappeerqueryinteractiveuiinputfields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)auf und ruft dann [**eaphostpeer-queryuiblobfrominteractiveuiinputfields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields) auf.<br/> Wenn der [eaphosteterresponseinvokeui](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) -Aktions Code nicht zurückgegeben wird, fährt EAPHost mit der regulären, nicht-SSO-aufrufssequenz fort. Weitere Informationen finden Sie unter [Supplicant API-Rückruf Sequenz](supplicant-api-call-sequence.md).<br/> | 3            |



 

## <a name="eaphost-peer-method-apis"></a>EAPHost-Peer Methoden-APIs

Die folgenden Peer Funktionen unterstützen einmaliges Anmelden (SSO).

Die Funktionen [**eappeerquerykredentialinputfields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields) und [**eappeerqueryuserblobfromkredentialinputfields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) sind exklusiv für einmaliges Anmelden (SSO).



| Name                                                                                                      | Zweck                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Aufgerufene Reihenfolge |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [**Eappeerqueryinteractiveuiinputfields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)                      | Definiert die Implementierung einer EAP-Methoden-API, die die Eingabefelder für interaktive Benutzeroberflächen Komponenten bereitstellt, die für den Supplicant ausgelöst werden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | 4            |
| [**Eappeerquerykredentialinputfields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields)                            | Definiert die Implementierung einer EAP-Methoden spezifischen Funktion, die die Eingabefelder der EAP-SSO-Anmelde Informationen für diese EAP-Methode abruft.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | 1            |
| [**Eappeerqueryuiblobfrominteractiveuiinputfields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuiblobfrominteractiveuiinputfields)  | Konvertiert Benutzerinformationen in ein benutzerblob, das von EAPHost-Lauf Zeitfunktionen verwendet werden kann.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | 5            |
| [**Eappeerqueryuserblobfromkredentialinputfields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) | Definiert die Implementierung einer EAP-Methoden Funktion, mit der die Benutzer-BLOB-Daten abgerufen werden, die von der interaktiven SSO-Benutzeroberfläche für den Supplicant ausgelöst werden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | 2            |
| [**Eappeerbeginsession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession)                                                        | Das Flag für das **EAP- \_ Flag \_ vor der \_ Anmeldung** gibt an, dass EAPHost SSO bereitstellen soll. Wenn in einem SSO-Szenario der **eappeerresponseinvokeui** -Aktions Code zurückgegeben wird, ruft EAPHost [**eappeerqueryinteractiveuiinputfields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)auf und ruft dann [**eappeerqueryuserblobfromkredentialinputfields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) auf.<br/> Wenn der Aktions Code **eappeerresponseinvokeui** nicht zurückgegeben wird, fährt EAPHost mit der regulären, nicht SSO-aufrufssequenz fort. Weitere Informationen finden Sie unter [Peer Method API-Rückruf Sequenz](peer-method-api-call-sequence.md).<br/> | 3            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[SSO und PLAP](understanding-sso-and-plap.md)
</dt> <dt>

[SSO-EAPHost-Szenarios](why-eaphost-sso.md)
</dt> </dl>

 

