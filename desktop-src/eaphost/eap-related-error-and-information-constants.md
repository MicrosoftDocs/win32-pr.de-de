---
title: EAP-bezogene Fehler-und Informations Konstanten (EAPHost RoR. h)
description: Einzelne Gruppen von EAP-bezogenen Fehlern und Informations Konstanten, die allen EAPHost-API-Technologien gemeinsam sind.
ms.assetid: 081b7a72-abe3-4cbb-9b6c-07bb6717fbfe
topic_type:
- apiref
api_name:
- EAP_E_EAPHOST_FIRST
- EAP_E_EAPHOST_LAST
- EAP_I_EAPHOST_FIRST
- EAP_I_EAPHOST_LAST
- EAP_E_CERT_STORE_INACCESSIBLE
- EAP_E_EAPHOST_METHOD_NOT_INSTALLED
- EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET
- EAP_E_EAPHOST_EAPQEC_INACCESSIBLE
- EAP_E_EAPHOST_IDENTITY_UNKNOWN
- EAP_E_AUTHENTICATION_FAILED
- EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED
- EAP_E_EAPHOST_METHOD_INVALID_PACKET
- EAP_E_EAPHOST_REMOTE_INVALID_PACKET
- EAP_E_EAPHOST_XML_MALFORMED
- EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO
- EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED
- EAP_E_USER_FIRST
- EAP_E_USER_LAST
- EAP_I_USER_FIRST
- EAP_I_USER_LAST
- EAP_E_USER_CERT_NOT_FOUND
- EAP_E_USER_CERT_INVALID
- EAP_E_USER_CERT_EXPIRED
- EAP_E_USER_CERT_REVOKED
- EAP_E_USER_CERT_OTHER_ERROR
- EAP_E_USER_CERT_REJECTED
- EAP_I_USER_ACCOUNT_OTHER_ERROR
- EAP_E_USER_CREDENTIALS_REJECTED
- EAP_E_USER_NAME_PASSWORD_REJECTED
- EAP_E_NO_SMART_CARD_READER
- EAP_E_SERVER_FIRST
- EAP_E_SERVER_LAST
- EAP_E_SERVER_CERT_NOT_FOUND
- EAP_E_SERVER_CERT_INVALID
- EAP_E_SERVER_CERT_EXPIRED
- EAP_E_SERVER_CERT_REVOKED
- EAP_E_SERVER_CERT_OTHER_ERROR
- EAP_E_USER_ROOT_CERT_FIRST
- EAP_E_USER_ROOT_CERT_LAST
- EAP_E_USER_ROOT_CERT_NOT_FOUND
- EAP_E_USER_ROOT_CERT_INVALID
- EAP_E_USER_ROOT_CERT_EXPIRED
- EAP_E_SERVER_ROOT_CERT_FIRST
- EAP_E_SERVER_ROOT_CERT_LAST
- EAP_E_SERVER_ROOT_CERT_NOT_FOUND
- EAP_E_SERVER_ROOT_CERT_INVALID
- EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED
api_location:
- eaphosterror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bd7b829cd4c5ba550fd88242ffb8c34572648d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040698"
---
# <a name="eap-related-error-and-information-constants"></a>EAP-bezogene Fehler-und Informations Konstanten

Einzelne Gruppen von EAP-bezogenen Fehlern und Informations Konstanten, die allen EAPHost-API-Technologien gemeinsam sind.

<dl> <dt>

<span id="EAP_E_EAPHOST_FIRST"></span><span id="eap_e_eaphost_first"></span>**EAP \_ E \_ EAPHost \_ zuerst**
</dt> <dd> <dl> <dt>

0x80420000l
</dt> <dt>



Definiert die Grenze von Fehlerberichten. Alle EAPHost-bezogenen Fehler treten zwischen **EAP \_ e \_ EAPHost \_ First** und **EAP \_ e \_ EAPHost \_ Last** auf.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_LAST___"></span><span id="eap_e_eaphost_last___"></span>**EAP \_ E \_ EAPHost \_ zuletzt** 
</dt> <dd> <dl> <dt>

0x804200ffl
</dt> <dt>



Definiert die Grenze von Fehlerberichten. Alle EAPHost-bezogenen Fehler treten zwischen **EAP \_ e \_ EAPHost \_ First** und **EAP \_ e \_ EAPHost \_ Last** auf.


</dt> </dl> </dd> <dt>

<span id="EAP_I_EAPHOST_FIRST_"></span><span id="eap_i_eaphost_first_"></span>**EAP \_ I \_ EAPHost \_ zuerst** 
</dt> <dd> <dl> <dt>

0x80420000l
</dt> <dt>



Definiert die Grenze von Informationsberichten. alle mit EAPHost verknüpften Informations Ereignisprotokollierung treten zwischen **EAP \_ i \_ EAPHost \_ First** und **EAP \_ i \_ EAPHost \_ Last** auf.


</dt> </dl> </dd> <dt>

<span id="EAP_I_EAPHOST_LAST"></span><span id="eap_i_eaphost_last"></span>**EAP \_ I \_ EAPHost \_ Last**
</dt> <dd> <dl> <dt>

0x804200ffl
</dt> <dt>



Definiert die Grenze von Informationsberichten. alle mit EAPHost verknüpften Informations Ereignisprotokollierung treten zwischen **EAP \_ i \_ EAPHost \_ First** und **EAP \_ i \_ EAPHost \_ Last** auf.


</dt> </dl> </dd> <dt>

<span id="EAP_E_CERT_STORE_INACCESSIBLE"></span><span id="eap_e_cert_store_inaccessible"></span>**EAP \_ E- \_ Zertifikat \_ Speicher nicht \_ zugänglich**
</dt> <dd> <dl> <dt>

0x80420011
</dt> <dt>



Weder der Authentifikator noch der Peer können auf den Zertifikat Speicher zugreifen.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_METHOD_NOT_INSTALLED"></span><span id="eap_e_eaphost_method_not_installed"></span>**EAP \_ E \_ EAPHost- \_ Methode \_ nicht \_ installiert**
</dt> <dd> <dl> <dt>

0x80420011
</dt> <dt>



Die angeforderte EAP-Methode ist nicht installiert.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET"></span><span id="eap_e_eaphost_thirdparty_method_host_reset"></span>**EAP \_ E \_ EAPHost \_ thirdparty- \_ Methoden \_ Host \_ Reset**
</dt> <dd> <dl> <dt>

0x80420012
</dt> <dt>



Der Host der Drittanbieter Methode antwortet nicht und wurde automatisch neu gestartet.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_EAPQEC_INACCESSIBLE"></span><span id="eap_e_eaphost_eapqec_inaccessible"></span>**EAP \_ E \_ EAPHost \_ eapqec nicht \_ zugänglich**
</dt> <dd> <dl> <dt>

0x80420013
</dt> <dt>



EAPHost kann nicht mit dem EAP- [Quarantäne](/windows/desktop/NAP/nap-client-architecture) Erzwingungs Client (QEC) auf einem NAP-fähigen Client ( [Network Access Protection, Netzwerk Zugriffsschutz](/windows/desktop/NAP/network-access-protection-start-page) ) kommunizieren.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_IDENTITY_UNKNOWN"></span><span id="eap_e_eaphost_identity_unknown"></span>**EAP \_ E \_ EAPHost- \_ Identität \_ unbekannt**
</dt> <dd> <dl> <dt>

0x80420014
</dt> <dt>



EAPHost gibt diesen Fehler zurück, wenn der Authentifikator die Authentifizierung fehlschlägt, nachdem die Peer Identität übermittelt wurde.


</dt> </dl> </dd> <dt>

<span id="EAP_E_AUTHENTICATION_FAILED"></span><span id="eap_e_authentication_failed"></span>**EAP \_ E- \_ Authentifizierung \_ fehlgeschlagen**
</dt> <dd> <dl> <dt>

0x80420015 
</dt> <dt>



EAPHost gibt diesen Fehler bei Authentifizierungs Fehlern zurück.


</dt> </dl> </dd> <dt>

<span id="EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED"></span><span id="eap_i_eaphost_eap_negotiation_failed"></span>**EAP \_ I \_ EAPHost- \_ EAP- \_ Aushandlung \_ fehlgeschlagen**
</dt> <dd> <dl> <dt>

0x40420016
</dt> <dt>



EAPHost protokolliert dieses Informations Ereignis, wenn der Client und der Server nicht mit kompatiblen EAP-Typen konfiguriert sind.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_METHOD_INVALID_PACKET"></span><span id="eap_e_eaphost_method_invalid_packet"></span>**EAP \_ E \_ EAPHost- \_ Methode \_ ungültiges \_ Paket**
</dt> <dd> <dl> <dt>

0x80420017
</dt> <dt>



Eine EAP-Methode hat ein EAP-Paket empfangen, das nicht verarbeitet werden kann. Ein anderer Name für die **EAP \_ E \_ EAPHost- \_ Methode " \_ ungültiges \_ Paket** " ist das **EAP- \_ \_ ungültige \_ Paket**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_REMOTE_INVALID_PACKET"></span><span id="eap_e_eaphost_remote_invalid_packet"></span>**EAP \_ E \_ EAPHost- \_ Remote \_ ungültiges \_ Paket**
</dt> <dd> <dl> <dt>

0x80420018
</dt> <dt>



EAPHost hat ein Paket empfangen, das nicht verarbeitet werden kann. Ein anderer Name für das **\_ \_ \_ Remote ungültige EAP \_ E \_ EAPHost-Paket** ist ein **Ungültiges EAP- \_ \_ Paket**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_XML_MALFORMED_"></span><span id="eap_e_eaphost_xml_malformed_"></span>**EAP \_ E \_ EAPHost- \_ XML \_ falsch formatiert** 
</dt> <dd> <dl> <dt>

0x80420019
</dt> <dt>



Fehler bei der Überprüfung des EAPHost-Konfigurations Schemas.


</dt> </dl> </dd> <dt>

<span id="EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO"></span><span id="eap_e_method_config_does_not_support_sso"></span>**die EAP \_ E- \_ Methoden \_ Konfiguration \_ \_ \_ unterstützt \_ SSO nicht.**
</dt> <dd> <dl> <dt>

0x8042001a
</dt> <dt>



Windows 7 oder höher: die EAP-Methode bietet keine Unterstützung für einmaliges Anmelden (Single Sign on, SSO) für die angegebene Konfiguration.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED"></span><span id="eap_e_eaphost_method_operation_not_supported"></span>**der EAP \_ E \_ EAPHost- \_ Methoden \_ Vorgang \_ \_ wird nicht unterstützt.**
</dt> <dd> <dl> <dt>

0x80420020
</dt> <dt>



EAPHost gibt diesen Fehler zurück, wenn eine konfigurierte EAP-Methode einen angeforderten Vorgang nicht unterstützt (Prozedur aufzurufen).


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_FIRST"></span><span id="eap_e_user_first"></span>**EAP \_ E- \_ Benutzer \_ zuerst**
</dt> <dd> <dl> <dt>

0x80420100l
</dt> <dt>



Definiert die Grenze von Fehlerberichten. alle Benutzer bezogenen Fehler treten zwischen **EAP \_ e \_ User \_ First** und **EAP \_ e \_ User \_ Last** auf.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_LAST_"></span><span id="eap_e_user_last_"></span>**EAP \_ E- \_ Benutzer \_ Letzte** 
</dt> <dd> <dl> <dt>

0x804201ffl
</dt> <dt>



Definiert die Grenze von Fehlerberichten. alle Benutzer bezogenen Fehler treten zwischen **EAP \_ e \_ User \_ First** und **EAP \_ e \_ User \_ Last** auf.


</dt> </dl> </dd> <dt>

<span id="EAP_I_USER_FIRST"></span><span id="eap_i_user_first"></span>**EAP \_ I- \_ Benutzer \_ zuerst**
</dt> <dd> <dl> <dt>

0x40420100l
</dt> <dt>



Definiert die Grenze von Informationsberichten. alle EAP-bezogenen Protokolle für Informations Ereignisse werden zwischen **EAP \_ i \_ User \_ First** und **EAP \_ i \_ User \_ Last** ausgeführt.


</dt> </dl> </dd> <dt>

<span id="EAP_I_USER_LAST"></span><span id="eap_i_user_last"></span>**EAP \_ I- \_ Benutzer \_ Letzte**
</dt> <dd> <dl> <dt>

0x404201ffl
</dt> <dt>



Definiert die Grenze von Informationsberichten. alle EAP-bezogenen Protokolle für Informations Ereignisse werden zwischen **EAP \_ i \_ User \_ First** und **EAP \_ i \_ User \_ Last** ausgeführt.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_NOT_FOUND"></span><span id="eap_e_user_cert_not_found"></span>**EAP \_ E- \_ Benutzer \_ Zertifikat \_ nicht \_ gefunden**
</dt> <dd> <dl> <dt>

0x80420100
</dt> <dt>



EAPHost konnte kein Benutzerzertifikat für die Authentifizierung finden.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_INVALID"></span><span id="eap_e_user_cert_invalid"></span>**EAP \_ E- \_ Benutzer \_ Zertifikat \_ ungültig**
</dt> <dd> <dl> <dt>

0x80420101
</dt> <dt>



Das Benutzerzertifikat, das für die Authentifizierung verwendet wird, verfügt nicht über die richtige erweiterte Schlüssel Verwendung (EKU).


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_EXPIRED"></span><span id="eap_e_user_cert_expired"></span>**EAP \_ E- \_ Benutzer \_ Zertifikat \_ abgelaufen**
</dt> <dd> <dl> <dt>

0x80420102
</dt> <dt>



EAPHost hat ein abgelaufenes Benutzerzertifikat gefunden.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_REVOKED"></span><span id="eap_e_user_cert_revoked"></span>**EAP \_ E- \_ Benutzer \_ Zertifikat \_ gesperrt**
</dt> <dd> <dl> <dt>

0x80420103
</dt> <dt>



Das Benutzerzertifikat, das für die Authentifizierung verwendet wird, wurde gesperrt.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_OTHER_ERROR"></span><span id="eap_e_user_cert_other_error"></span>**Fehler beim EAP \_ E- \_ Benutzer \_ Zertifikat \_ \_ .**
</dt> <dd> <dl> <dt>

0x80420104
</dt> <dt>



Ein unbekannter Fehler ist aufgetreten, wenn die Benutzer Zertifizierung für die Authentifizierung verwendet wird.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_REJECTED_"></span><span id="eap_e_user_cert_rejected_"></span>**EAP \_ E- \_ Benutzer \_ Zertifikat \_ abgelehnt** 
</dt> <dd> <dl> <dt>

0x80420105
</dt> <dt>



Der Authentifikator hat die Benutzer Zertifizierung abgelehnt.


</dt> </dl> </dd> <dt>

<span id="EAP_I_USER_ACCOUNT_OTHER_ERROR"></span><span id="eap_i_user_account_other_error"></span>**anderer EAP- \_ \_ Benutzer \_ Konto \_ \_ Fehler**
</dt> <dd> <dl> <dt>

0x40420110
</dt> <dt>



Nach einem Identitäts Austausch wurde ein EAP-Fehler empfangen, der die Wahrscheinlichkeit eines Problems mit dem Konto des authentifizier enden Benutzers angibt.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CREDENTIALS_REJECTED"></span><span id="eap_e_user_credentials_rejected"></span>**EAP \_ E- \_ Benutzer \_ Anmelde Informationen \_ abgelehnt**
</dt> <dd> <dl> <dt>

0x80420111
</dt> <dt>



Der Authentifikator hat die Benutzer Anmelde Informationen für die Authentifizierung abgelehnt.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_NAME_PASSWORD_REJECTED"></span><span id="eap_e_user_name_password_rejected"></span>**Kennwort für EAP \_ E- \_ Benutzer \_ Name \_ \_ abgelehnt**
</dt> <dd> <dl> <dt>

0x80420112
</dt> <dt>



Windows 7 oder höher: Fehler bei der Authentifizierung. Der Authentifikator hat die Anmelde Informationen des Benutzers abgelehnt.


</dt> </dl> </dd> <dt>

<span id="EAP_E_NO_SMART_CARD_READER"></span><span id="eap_e_no_smart_card_reader"></span>**EAP \_ E \_ kein \_ \_ \_ Smartcardleser**
</dt> <dd> <dl> <dt>

0x80420113
</dt> <dt>



Windows 7 oder höher: Es wurde kein Smartcardleser gefunden.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_FIRST"></span><span id="eap_e_server_first"></span>**EAP \_ E \_ Server \_ First**
</dt> <dd> <dl> <dt>

0x80420200l
</dt> <dt>



Definiert die Grenze von Fehlerberichten. alle Server bezogenen Fehler werden zwischen **EAP \_ e \_ Server \_ First** und **EAP \_ e \_ Server \_ Last** auftreten.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_LAST"></span><span id="eap_e_server_last"></span>**EAP \_ E- \_ Server \_ zuletzt**
</dt> <dd> <dl> <dt>

0x804202ffl
</dt> <dt>



Definiert die Grenze von Fehlerberichten. alle Server bezogenen Fehler werden zwischen **EAP \_ e \_ Server \_ First** und **EAP \_ e \_ Server \_ Last** auftreten.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_NOT_FOUND"></span><span id="eap_e_server_cert_not_found"></span>**EAP \_ E- \_ Server- \_ CERT \_ nicht \_ gefunden**
</dt> <dd> <dl> <dt>

0x80420200
</dt> <dt>



EAPHost konnte das Serverzertifikat für die Authentifizierung nicht finden.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_INVALID"></span><span id="eap_e_server_cert_invalid"></span>**EAP \_ E- \_ Server \_ Zertifikat \_ ungültig**
</dt> <dd> <dl> <dt>

0x80420201
</dt> <dt>



Das Serverzertifikat, das als Benutzer für die Authentifizierung dient, verfügt über keinen geeigneten EKU-Satz (Extended Key Usage).


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_EXPIRED"></span><span id="eap_e_server_cert_expired"></span>**EAP \_ E \_ Server- \_ Zertifikat \_ abgelaufen**
</dt> <dd> <dl> <dt>

0x80420202
</dt> <dt>



EAPHost hat ein abgelaufenes Serverzertifikat gefunden.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_REVOKED"></span><span id="eap_e_server_cert_revoked"></span>**EAP \_ E- \_ Server \_ Zertifikat \_ gesperrt**
</dt> <dd> <dl> <dt>

0x80420203
</dt> <dt>



Das Serverzertifikat, das für die Authentifizierung verwendet wird, wurde gesperrt.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_OTHER_ERROR"></span><span id="eap_e_server_cert_other_error"></span>**anderer EAP \_ E-Server- \_ CERT- \_ \_ \_ Fehler**
</dt> <dd> <dl> <dt>

0x80420204
</dt> <dt>



Unbekannter Fehler beim Serverzertifikat.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_FIRST"></span><span id="eap_e_user_root_cert_first"></span>**EAP \_ E- \_ Benutzer Stamm \_ \_ Zertifikat \_ zuerst**
</dt> <dd> <dl> <dt>

0x80420300l
</dt> <dt>



Definiert die Grenze von Fehlerberichten. alle Fehler im Zusammenhang mit dem Benutzer Stamm Zertifikat treten zuerst zwischen dem **EAP e-Benutzer Stamm Zertifikat \_ \_ \_ \_ \_ First** und dem **EAP \_ e- \_ Benutzer \_ \_ \_** Stamm Zertifikat auf.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_LAST"></span><span id="eap_e_user_root_cert_last"></span>**EAP \_ E- \_ Benutzer Stamm \_ \_ Zertifikat \_ zuletzt**
</dt> <dd> <dl> <dt>

0x804203ffl
</dt> <dt>



Definiert die Grenze von Fehlerberichten. alle Fehler im Zusammenhang mit dem Benutzer Stamm Zertifikat treten zuerst zwischen dem **EAP e-Benutzer Stamm Zertifikat \_ \_ \_ \_ \_ First** und dem **EAP \_ e- \_ Benutzer \_ \_ \_** Stamm Zertifikat auf.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_user_root_cert_not_found"></span>**EAP \_ E-Stamm \_ Zertifikat für Benutzer \_ \_ \_ nicht \_ gefunden**
</dt> <dd> <dl> <dt>

0x80420300
</dt> <dt>



EAPHost konnte kein Zertifikat in einem vertrauenswürdigen Stamm Zertifikat Speicher für die Validierung der Benutzer Zertifizierungsstelle finden.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_INVALID"></span><span id="eap_e_user_root_cert_invalid"></span>**EAP \_ E-Stamm \_ Zertifikat für Benutzer \_ \_ \_ ungültig**
</dt> <dd> <dl> <dt>

0x80420301
</dt> <dt>



Die Authentifizierung ist fehlgeschlagen, weil das für dieses Netzwerk verwendete Stamm Zertifikat ungültig ist.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_EXPIRED"></span><span id="eap_e_user_root_cert_expired"></span>**EAP \_ E-Stamm \_ Zertifikat für Benutzer \_ \_ \_ abgelaufen**
</dt> <dd> <dl> <dt>

0x80420302
</dt> <dt>



Das für die Validierung des Benutzer Zertifikats erforderliche vertrauenswürdige Stamm Zertifikat ist abgelaufen.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_FIRST"></span><span id="eap_e_server_root_cert_first"></span>**EAP-E-Server-Stamm \_ \_ \_ \_ Zertifikat \_ zuerst**
</dt> <dd> <dl> <dt>

0x80420400l
</dt> <dt>



Definiert die Grenze von Fehlerberichten. alle Fehler im Zusammenhang mit dem Server Stamm Zertifikat treten zuerst zwischen **EAP \_ e \_ Server \_ root \_ CERT \_ First** und **EAP \_ e \_ Server \_ root \_ CERT \_** auf.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_LAST"></span><span id="eap_e_server_root_cert_last"></span>**EAP \_ E-Server-Stamm \_ \_ \_ Zertifikat \_ zuletzt**
</dt> <dd> <dl> <dt>

0x804204ffl
</dt> <dt>



Definiert die Grenze von Fehlerberichten. alle Fehler im Zusammenhang mit dem Server Stamm Zertifikat treten zuerst zwischen **EAP \_ e \_ Server \_ root \_ CERT \_ First** und **EAP \_ e \_ Server \_ root \_ CERT \_** auf.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_server_root_cert_not_found"></span>**Das EAP \_ E- \_ Server Stamm Zertifikat wurde \_ \_ \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

0x80420400
</dt> <dt>



EAPHost konnte kein Stamm Zertifikat in einem vertrauenswürdigen Stamm Zertifikat Speicher für die Überprüfung der Server Zertifizierung finden.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_INVALID__________"></span><span id="eap_e_server_root_cert_invalid__________"></span>**EAP \_ E \_ Server \_ root- \_ Zertifikat \_ ungültig** 
</dt> <dd> <dl> <dt>

0x80420401
</dt> <dt>



Die Authentifizierung ist fehlgeschlagen, weil das für dieses Netzwerk auf dem Server Computer erforderliche Serverzertifikat ungültig ist.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED"></span><span id="eap_e_server_root_cert_name_required"></span>**der EAP \_ E- \_ Server Stamm \_ \_ Zertifikat Name ist \_ \_ erforderlich.**
</dt> <dd> <dl> <dt>

0x80420406
</dt> <dt>



Die Authentifizierung ist fehlgeschlagen, weil für das Zertifikat auf dem Server Computer kein Servername angegeben ist.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Für bestimmte Fehler gibt es alternative Namen:

-   Ein anderer Name für die **EAP \_ E \_ EAPHost- \_ Methode " \_ ungültiges \_ Paket** " ist das **EAP- \_ \_ ungültige \_ Paket**.
-   Ein anderer Name für das **\_ \_ \_ Remote ungültige EAP \_ E \_ EAPHost-Paket** ist ein **Ungültiges EAP- \_ \_ Paket**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                      |
| Header<br/>                   | <dl> <dt>EAPHost RoR. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine EAPHost-Konstanten](common-eap-host-error-constants.md)
</dt> </dl>

 

