---
title: EAP-bezogene Fehler- und Informationskonstanten (Eaphosterror.h)
description: Einzelne Gruppen von EAP-bezogenen Fehler- und Informationskonstanten, die allen EAPHost-API-Technologien gemeinsam sind.
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
ms.openlocfilehash: bc4140444d1b5c3ae99c90c2447e165a4143b042dcc7567104e4b5f0063b645b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984240"
---
# <a name="eap-related-error-and-information-constants"></a>EAP-bezogene Fehler- und Informationskonstanten

Einzelne Gruppen von EAP-bezogenen Fehler- und Informationskonstanten, die allen EAPHost-API-Technologien gemeinsam sind.

<dl> <dt>

<span id="EAP_E_EAPHOST_FIRST"></span><span id="eap_e_eaphost_first"></span>**EAP \_ E \_ EAPHOST \_ FIRST**
</dt> <dd> <dl> <dt>

0x80420000L
</dt> <dt>



Definiert die Grenze von Fehlerberichten. Jeder EAPHost-bezogene Fehler tritt zwischen **EAP \_ E \_ EAPHOST \_ FIRST** und **EAP \_ E \_ EAPHOST \_ LAST** auf.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_LAST___"></span><span id="eap_e_eaphost_last___"></span>**EAP \_ E \_ EAPHOST \_ LAST** 
</dt> <dd> <dl> <dt>

0x804200FFL
</dt> <dt>



Definiert die Grenze von Fehlerberichten. Jeder EAPHost-bezogene Fehler tritt zwischen **EAP \_ E \_ EAPHOST \_ FIRST** und **EAP \_ E \_ EAPHOST \_ LAST** auf.


</dt> </dl> </dd> <dt>

<span id="EAP_I_EAPHOST_FIRST_"></span><span id="eap_i_eaphost_first_"></span>**EAP \_ I \_ EAPHOST \_ FIRST** 
</dt> <dd> <dl> <dt>

0x80420000L
</dt> <dt>



Definiert die Grenze von Informationsberichten. jede EAPHost-bezogene Informationsereignisprotokollierung erfolgt zwischen **EAP \_ I \_ EAPHOST \_ FIRST** und **EAP \_ I \_ EAPHOST \_ LAST**.


</dt> </dl> </dd> <dt>

<span id="EAP_I_EAPHOST_LAST"></span><span id="eap_i_eaphost_last"></span>**EAP \_ I \_ EAPHOST \_ LAST**
</dt> <dd> <dl> <dt>

0x804200FFL
</dt> <dt>



Definiert die Grenze von Informationsberichten. jede EAPHost-bezogene Informationsereignisprotokollierung erfolgt zwischen **EAP \_ I \_ EAPHOST \_ FIRST** und **EAP \_ I \_ EAPHOST \_ LAST**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_CERT_STORE_INACCESSIBLE"></span><span id="eap_e_cert_store_inaccessible"></span>**\_ \_ \_ EAP-E-ZERTIFIKATSPEICHER \_ NICHT ZUGÄNGLICH**
</dt> <dd> <dl> <dt>

0x80420011
</dt> <dt>



Weder der Authentifikator noch der Peer kann auf den Zertifikatspeicher zugreifen.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_METHOD_NOT_INSTALLED"></span><span id="eap_e_eaphost_method_not_installed"></span>**EAP \_ E \_ EAPHOST-METHODE \_ NICHT \_ \_ INSTALLIERT**
</dt> <dd> <dl> <dt>

0x80420011
</dt> <dt>



Die angeforderte EAP-Methode ist nicht installiert.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET"></span><span id="eap_e_eaphost_thirdparty_method_host_reset"></span>**EAP \_ E \_ EAPHOST \_ THIRDPARTY \_ METHOD \_ HOST \_ RESET**
</dt> <dd> <dl> <dt>

0x80420012
</dt> <dt>



Der Host der Drittanbietermethode reagiert nicht und wurde automatisch neu gestartet.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_EAPQEC_INACCESSIBLE"></span><span id="eap_e_eaphost_eapqec_inaccessible"></span>**EAP \_ E \_ EAPHOST \_ EAPQEC \_ NICHT ZUGÄNGLICH**
</dt> <dd> <dl> <dt>

0x80420013
</dt> <dt>



EAPHost kann nicht mit dem [EAP-Quarantäneerzwingungsclient](/windows/desktop/NAP/nap-client-architecture) (QEC) auf einem NAP-fähigen Client [(Network Access Protection)](/windows/desktop/NAP/network-access-protection-start-page) kommunizieren.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_IDENTITY_UNKNOWN"></span><span id="eap_e_eaphost_identity_unknown"></span>**EAP \_ E \_ EAPHOST \_ IDENTITY \_ UNKNOWN**
</dt> <dd> <dl> <dt>

0x80420014
</dt> <dt>



EAPHost gibt diesen Fehler zurück, wenn der Authentifikator die Authentifizierung nach übermittlung der Peeridentität fehlschlägt.


</dt> </dl> </dd> <dt>

<span id="EAP_E_AUTHENTICATION_FAILED"></span><span id="eap_e_authentication_failed"></span>**\_ \_ EAP-E-AUTHENTIFIZIERUNG \_ FEHLGESCHLAGEN**
</dt> <dd> <dl> <dt>

0x80420015 
</dt> <dt>



EAPHost gibt diesen Fehler bei einem Authentifizierungsfehler zurück.


</dt> </dl> </dd> <dt>

<span id="EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED"></span><span id="eap_i_eaphost_eap_negotiation_failed"></span>**\_EAP I \_ EAPHOST \_ EAP NEGOTIATION FAILED (EAP I EAPHOST-EAP-AUSHANDLUNG \_ \_ FEHLGESCHLAGEN)**
</dt> <dd> <dl> <dt>

0x40420016
</dt> <dt>



EAPHost protokolliert dieses Informationsereignis, wenn Client und Server nicht mit kompatiblen EAP-Typen konfiguriert sind.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_METHOD_INVALID_PACKET"></span><span id="eap_e_eaphost_method_invalid_packet"></span>**EAP \_ E \_ EAPHOST-METHODE \_ \_ \_ UNGÜLTIGES PAKET**
</dt> <dd> <dl> <dt>

0x80420017
</dt> <dt>



Eine EAP-Methode hat ein EAP-Paket empfangen, das nicht verarbeitet werden kann. Ein anderer Name für **EAP \_ E \_ EAPHOST \_ METHOD INVALID \_ \_ PACKET** ist **EAP METHOD INVALID \_ \_ \_ PACKET**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_REMOTE_INVALID_PACKET"></span><span id="eap_e_eaphost_remote_invalid_packet"></span>**EAP \_ E \_ EAPHOST \_ REMOTE \_ INVALID \_ PACKET**
</dt> <dd> <dl> <dt>

0x80420018
</dt> <dt>



EAPHost hat ein Paket empfangen, das nicht verarbeitet werden kann. Ein anderer Name für **EAP \_ E \_ EAPHOST \_ REMOTE INVALID \_ \_ PACKET** ist **EAP INVALID \_ \_ PACKET**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_XML_MALFORMED_"></span><span id="eap_e_eaphost_xml_malformed_"></span>**EAP \_ E \_ EAPHOST \_ XML \_ MALFORMED** 
</dt> <dd> <dl> <dt>

0x80420019
</dt> <dt>



Fehler bei der Validierung des EAPHost-Konfigurationsschemas.


</dt> </dl> </dd> <dt>

<span id="EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO"></span><span id="eap_e_method_config_does_not_support_sso"></span>**EAP \_ \_ E-METHODENKONFIGURATION \_ \_ UNTERSTÜTZT KEIN \_ \_ \_ EINMALIGES ANMELDEN.**
</dt> <dd> <dl> <dt>

0x8042001A
</dt> <dt>



Windows 7 oder höher: Die EAP-Methode unterstützt das einmalige Anmelden (Single Sign On, SSO) für die bereitgestellte Konfiguration nicht.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED"></span><span id="eap_e_eaphost_method_operation_not_supported"></span>**\_EAP E \_ EAPHOST-METHODENVORGANG \_ WIRD NICHT \_ \_ \_ UNTERSTÜTZT**
</dt> <dd> <dl> <dt>

0x80420020
</dt> <dt>



EAPHost gibt diesen Fehler zurück, wenn eine konfigurierte EAP-Methode einen angeforderten Vorgang nicht unterstützt (Prozeduraufruf).


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_FIRST"></span><span id="eap_e_user_first"></span>**EAP \_ E \_ USER \_ FIRST**
</dt> <dd> <dl> <dt>

0x80420100L
</dt> <dt>



Definiert die Grenze von Fehlerberichten. Alle benutzerbezogenen Fehler treten zwischen **EAP \_ E USER \_ \_ FIRST** und **EAP E USER \_ \_ \_ LAST** auf.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_LAST_"></span><span id="eap_e_user_last_"></span>**EAP \_ E \_ USER \_ LAST** 
</dt> <dd> <dl> <dt>

0x804201FFL
</dt> <dt>



Definiert die Grenze von Fehlerberichten. Alle benutzerbezogenen Fehler treten zwischen **EAP \_ E USER \_ \_ FIRST** und **EAP E USER \_ \_ \_ LAST** auf.


</dt> </dl> </dd> <dt>

<span id="EAP_I_USER_FIRST"></span><span id="eap_i_user_first"></span>**EAP \_ I \_ USER \_ FIRST**
</dt> <dd> <dl> <dt>

0x40420100L
</dt> <dt>



Definiert die Grenze von Informationsberichten. Alle EAP-bezogenen Informationsereignisprotokollierung erfolgt zwischen **EAP \_ I USER \_ \_ FIRST** und **EAP I USER \_ \_ \_ LAST**.


</dt> </dl> </dd> <dt>

<span id="EAP_I_USER_LAST"></span><span id="eap_i_user_last"></span>**EAP \_ I \_ USER \_ LAST**
</dt> <dd> <dl> <dt>

0x404201FFL
</dt> <dt>



Definiert die Grenze von Informationsberichten. Alle EAP-bezogenen Informationsereignisprotokollierung erfolgt zwischen **EAP \_ I USER \_ \_ FIRST** und **EAP I USER \_ \_ \_ LAST**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_NOT_FOUND"></span><span id="eap_e_user_cert_not_found"></span>**EAP \_ E \_ USER \_ CERT \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

0x80420100
</dt> <dt>



EAPHost konnte kein Benutzerzertifikat für die Authentifizierung finden.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_INVALID"></span><span id="eap_e_user_cert_invalid"></span>**EAP \_ E \_ USER \_ CERT \_ INVALID**
</dt> <dd> <dl> <dt>

0x80420101
</dt> <dt>



Für das Benutzerzertifikat, das für die Authentifizierung verwendet wird, ist keine ordnungsgemäße erweiterte Schlüsselverwendung (Extended Key Usage, EKU) festgelegt.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_EXPIRED"></span><span id="eap_e_user_cert_expired"></span>**EAP \_ E \_ USER \_ CERT \_ EXPIRED**
</dt> <dd> <dl> <dt>

0x80420102
</dt> <dt>



EAPhost hat ein abgelaufenes Benutzerzertifikat gefunden.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_REVOKED"></span><span id="eap_e_user_cert_revoked"></span>**EAP \_ E \_ USER \_ CERT \_ REVOKED**
</dt> <dd> <dl> <dt>

0x80420103
</dt> <dt>



Das für die Authentifizierung verwendete Benutzerzertifikat wurde widerrufen.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_OTHER_ERROR"></span><span id="eap_e_user_cert_other_error"></span>**\_EAP E \_ USER \_ CERT \_ – ANDERER \_ FEHLER**
</dt> <dd> <dl> <dt>

0x80420104
</dt> <dt>



Unbekannter Fehler bei der Benutzerzertifizierung, die für die Authentifizierung verwendet wird.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_REJECTED_"></span><span id="eap_e_user_cert_rejected_"></span>**EAP \_ E \_ USER \_ CERT \_ ABGELEHNT** 
</dt> <dd> <dl> <dt>

0x80420105
</dt> <dt>



Der Authentifikator hat die Benutzerzertifizierung abgelehnt.


</dt> </dl> </dd> <dt>

<span id="EAP_I_USER_ACCOUNT_OTHER_ERROR"></span><span id="eap_i_user_account_other_error"></span>**EAP \_ I \_ USER \_ ACCOUNT \_ OTHER \_ ERROR**
</dt> <dd> <dl> <dt>

0x40420110
</dt> <dt>



Nach einem Identitätsaustausch wurde ein EAP-Fehler empfangen, der die Wahrscheinlichkeit eines Problems mit dem Authentifizieren des Benutzerkontos angibt.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CREDENTIALS_REJECTED"></span><span id="eap_e_user_credentials_rejected"></span>**EAP \_ E USER CREDENTIALS REJECTED (EAP-E-BENUTZERANMELDEINFORMATIONEN \_ \_ \_ ABGELEHNT)**
</dt> <dd> <dl> <dt>

0x80420111
</dt> <dt>



Der Authentifikator hat Benutzeranmeldeinformationen für die Authentifizierung abgelehnt.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_NAME_PASSWORD_REJECTED"></span><span id="eap_e_user_name_password_rejected"></span>**EAP \_ E \_ USER \_ NAME \_ PASSWORD \_ REJECTED**
</dt> <dd> <dl> <dt>

0x80420112
</dt> <dt>



Windows 7 oder höher: Fehler bei der Authentifizierung. Der Authentifikator hat die Benutzeranmeldeinformationen abgelehnt.


</dt> </dl> </dd> <dt>

<span id="EAP_E_NO_SMART_CARD_READER"></span><span id="eap_e_no_smart_card_reader"></span>**EAP \_ E \_ NO \_ SMART \_ CARD \_ READER**
</dt> <dd> <dl> <dt>

0x80420113
</dt> <dt>



Windows 7 oder höher: Kein Smartcardleser gefunden.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_FIRST"></span><span id="eap_e_server_first"></span>**EAP \_ E \_ SERVER \_ FIRST**
</dt> <dd> <dl> <dt>

0x80420200L
</dt> <dt>



Definiert die Grenze von Fehlerberichten. Alle serverbezogenen Fehler treten zwischen **EAP \_ E SERVER \_ \_ FIRST** und **EAP E SERVER \_ \_ \_ LAST** auf.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_LAST"></span><span id="eap_e_server_last"></span>**EAP \_ E \_ SERVER \_ LAST**
</dt> <dd> <dl> <dt>

0x804202FFL
</dt> <dt>



Definiert die Grenze von Fehlerberichten. Serverbezogene Fehler treten zwischen **EAP \_ E SERVER \_ \_ FIRST** und **EAP E SERVER LAST \_ \_ \_ auf.**


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_NOT_FOUND"></span><span id="eap_e_server_cert_not_found"></span>**EAP \_ E \_ SERVER \_ CERT \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

0x80420200
</dt> <dt>



EAPHost konnte das Serverzertifikat für die Authentifizierung nicht finden.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_INVALID"></span><span id="eap_e_server_cert_invalid"></span>**EAP \_ E \_ SERVER \_ CERT \_ INVALID**
</dt> <dd> <dl> <dt>

0x80420201
</dt> <dt>



Für das Serverzertifikat, das benutzer für die Authentifizierung ist, ist keine ordnungsgemäße erweiterte Schlüsselverwendung (Extended Key Usage, EKU) festgelegt.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_EXPIRED"></span><span id="eap_e_server_cert_expired"></span>**EAP \_ E \_ SERVER \_ CERT \_ EXPIRED**
</dt> <dd> <dl> <dt>

0x80420202
</dt> <dt>



EAPhost hat ein abgelaufenes Serverzertifikat gefunden.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_REVOKED"></span><span id="eap_e_server_cert_revoked"></span>**EAP \_ E \_ SERVER \_ CERT \_ WIDERRUFEN**
</dt> <dd> <dl> <dt>

0x80420203
</dt> <dt>



Das für die Authentifizierung verwendete Serverzertifikat wurde widerrufen.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_OTHER_ERROR"></span><span id="eap_e_server_cert_other_error"></span>**EAP \_ E \_ SERVER \_ CERT \_ OTHER \_ ERROR**
</dt> <dd> <dl> <dt>

0x80420204
</dt> <dt>



Beim Serverzertifikat ist ein unbekannter Fehler aufgetreten.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_FIRST"></span><span id="eap_e_user_root_cert_first"></span>**EAP \_ E \_ USER \_ ROOT \_ CERT \_ FIRST**
</dt> <dd> <dl> <dt>

0x80420300L
</dt> <dt>



Definiert die Grenze von Fehlerberichten. Ein Fehler im Zusammenhang mit dem Benutzerstammzertifikat tritt zwischen **EAP \_ E USER \_ ROOT \_ \_ CERT \_ FIRST** und **EAP E USER ROOT \_ \_ \_ \_ CERT FIRST \_ auf.**


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_LAST"></span><span id="eap_e_user_root_cert_last"></span>**EAP \_ E \_ USER \_ ROOT \_ CERT \_ LAST**
</dt> <dd> <dl> <dt>

0x804203FFL
</dt> <dt>



Definiert die Grenze von Fehlerberichten. Ein Fehler im Zusammenhang mit dem Benutzerstammzertifikat tritt zwischen **EAP \_ E USER \_ ROOT \_ \_ CERT \_ FIRST** und **EAP E USER ROOT \_ \_ \_ \_ CERT FIRST \_ auf.**


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_user_root_cert_not_found"></span>**EAP E USER ROOT CERT NOT FOUND (EAP \_ \_ \_ \_ E-BENUTZERSTAMMZERTIFIKAT \_ NICHT \_ GEFUNDEN)**
</dt> <dd> <dl> <dt>

0x80420300
</dt> <dt>



EAPHost konnte kein Zertifikat in einem vertrauenswürdigen Stammzertifikatspeicher für die Überprüfung der Benutzerzertifizierung finden.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_INVALID"></span><span id="eap_e_user_root_cert_invalid"></span>**EAP \_ E \_ USER \_ ROOT \_ CERT \_ INVALID**
</dt> <dd> <dl> <dt>

0x80420301
</dt> <dt>



Fehler bei der Authentifizierung, weil das für dieses Netzwerk verwendete Stammzertifikat ungültig ist.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_EXPIRED"></span><span id="eap_e_user_root_cert_expired"></span>**EAP \_ E \_ USER \_ ROOT \_ CERT \_ EXPIRED**
</dt> <dd> <dl> <dt>

0x80420302
</dt> <dt>



Das vertrauenswürdige Stammzertifikat, das für die Überprüfung des Benutzerzertifikats erforderlich ist, ist abgelaufen.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_FIRST"></span><span id="eap_e_server_root_cert_first"></span>**EAP \_ E \_ SERVER \_ ROOT \_ CERT \_ FIRST**
</dt> <dd> <dl> <dt>

0x80420400L
</dt> <dt>



Definiert die Begrenzung von Fehlerberichten. Ein serverstammzertifikatbezogener Fehler tritt zwischen **EAP \_ E SERVER \_ ROOT \_ \_ CERT \_ FIRST** und **EAP E SERVER ROOT \_ \_ \_ \_ CERT FIRST \_ auf.**


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_LAST"></span><span id="eap_e_server_root_cert_last"></span>**EAP \_ E \_ SERVER \_ ROOT \_ CERT \_ LAST**
</dt> <dd> <dl> <dt>

0x804204FFL
</dt> <dt>



Definiert die Begrenzung von Fehlerberichten. Ein serverstammzertifikatbezogener Fehler tritt zwischen **EAP \_ E SERVER \_ ROOT \_ \_ CERT \_ FIRST** und **EAP E SERVER ROOT \_ \_ \_ \_ CERT FIRST \_ auf.**


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_server_root_cert_not_found"></span>**EAP \_ E \_ SERVER \_ ROOT \_ CERT \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

0x80420400
</dt> <dt>



EAPHost konnte kein Stammzertifikat in einem vertrauenswürdigen Stammzertifikatspeicher für die Serverzertifizierungsüberprüfung finden.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_INVALID__________"></span><span id="eap_e_server_root_cert_invalid__________"></span>**EAP \_ E \_ SERVER \_ ROOT \_ CERT \_ INVALID** 
</dt> <dd> <dl> <dt>

0x80420401
</dt> <dt>



Fehler bei der Authentifizierung, weil das für dieses Netzwerk auf dem Servercomputer erforderliche Serverzertifikat ungültig ist.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED"></span><span id="eap_e_server_root_cert_name_required"></span>**EAP \_ E \_ SERVER \_ ROOT \_ CERT \_ NAME \_ REQUIRED**
</dt> <dd> <dl> <dt>

0x80420406
</dt> <dt>



Fehler bei der Authentifizierung, weil für das Zertifikat auf dem Servercomputer kein Servername angegeben ist.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Für bestimmte Fehler gibt es alternative Namen:

-   Ein anderer Name für **EAP \_ \_ EAPHOST \_ METHOD INVALID PACKET \_ \_ ist** **EAP METHOD INVALID \_ \_ \_ PACKET**.
-   Ein anderer Name für **EAP \_ \_ EAPHOST \_ REMOTE INVALID PACKET \_ \_ ist** **EAP INVALID \_ \_ PACKET**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                      |
| Header<br/>                   | <dl> <dt>Eaphosterror.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Allgemeine EAPHost-Konstanten](common-eap-host-error-constants.md)
</dt> </dl>

 

