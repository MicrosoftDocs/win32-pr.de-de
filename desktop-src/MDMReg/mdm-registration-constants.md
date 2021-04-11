---
title: MDM-Registrierungsfehler Werte (mdmregistration. h)
description: Die folgenden Fehler Werte sind bei der MDM-Registrierung.
ms.assetid: 1f42ed5e-e221-47ec-a019-ed06c05d55d0
topic_type:
- apiref
api_name:
- E_DATATYPE_MISMATCH
- MREGISTER_E_DEVICE_MESSAGE_FORMAT_ERROR
- MENROLL_E_DEVICE_MESSAGE_FORMAT_ERROR
- MREGISTER_E_DEVICE_AUTHENTICATION_ERROR
- MENROLL_E_DEVICE_AUTHENTICATION_ERROR
- MREGISTER_E_DEVICE_AUTHORIZATION_ERROR
- MENROLL_E_DEVICE_AUTHORIZATION_ERROR
- MREGISTER_E_DEVICE_CERTIFCATEREQUEST_ERROR
- MENROLL_E_DEVICE_CERTIFCATEREQUEST_ERROR
- MREGISTER_E_DEVICE_CONFIGMGRSERVER_ERROR
- MENROLL_E_DEVICE_CONFIGMGRSERVER_ERROR
- MREGISTER_E_DEVICE_INTERNALSERVICE_ERROR
- MENROLL_E_DEVICE_INTERNALSERVICE_ERROR
- MREGISTER_E_DEVICE_INVALIDSECURITY_ERROR
- MENROLL_E_DEVICE_INVALIDSECURITY_ERROR
- MREGISTER_E_DEVICE_UNKNOWN_ERROR
- MENROLL_E_DEVICE_UNKNOWN_ERROR
- MREGISTER_E_REGISTRATION_IN_PROGRESS
- MENROLL_E_ENROLLMENT_IN_PROGRESS
- MREGISTER_E_DEVICE_ALREADY_REGISTERED
- MENROLL_E_DEVICE_ALREADY_ENROLLED
- MREGISTER_E_DEVICE_NOT_REGISTERED
- MENROLL_E_DEVICE_NOT_ENROLLED
- MREGISTER_E_DISCOVERY_REDIRECTED
- MREGISTER_E_DEVICE_NOT_AD_REGISTERED_ERROR
- MENROLL_E_DISCOVERY_SEC_CERT_DATE_INVALID
- MREGISTER_E_DISCOVERY_FAILED
- MENROLL_E_PASSWORD_NEEDED
- MENROLL_E_WAB_ERROR
- MENROLL_E_CONNECTIVITY
- MENROLL_S_ENROLLMENT_SUSPENDED
- MENROLL_E_INVALIDSSLCERT
- MENROLL_E_DEVICECAPREACHED
- MENROLL_E_DEVICENOTSUPPORTED
- MENROLL_E_NOTSUPPORTED
- MREGISTER_E_NOTELIGIBLETORENEW
- MENROLL_E_INMAINTENANCE
- MENROLL_E_USERLICENSE
- MENROLL_E_ENROLLMENTDATAINVALID
- MENROLL_E_INSECUREREDIRECT
- MENROLL_E_PLATFORM_WRONG_STATE
- MENROLL_E_PLATFORM_LICENSE_ERROR
- MENROLL_E_PLATFORM_UNKNOWN_ERROR
- MENROLL_E_PROV_CSP_CERTSTORE
- MENROLL_E_PROV_CSP_W7
- MENROLL_E_PROV_CSP_DMCLIENT
- MENROLL_E_PROV_CSP_PFW
- MENROLL_E_PROV_CSP_MISC
- MENROLL_E_PROV_UNKNOWN
- MENROLL_E_PROV_SSLCERTNOTFOUND
- MENROLL_E_PROV_CSP_APPMGMT
- MENROLL_E_DEVICE_MANAGEMENT_BLOCKED
- MENROLL_E_CERTPOLICY_PRIVATEKEYCREATION_FAILED
- MENROLL_E_CERTAUTH_FAILED_TO_FIND_CERT
- MENROLL_E_EMPTY_MESSAGE
- MENROLL_E_USER_CANCELED
- MENROLL_E_MDM_NOT_CONFIGURED
api_location:
- MDMRegistration.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28c21732a102b052d4be51cbbbf5627e42cc487
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040686"
---
# <a name="mdm-registration-error-values"></a>MDM-Registrierungsfehler Werte

Die folgenden Fehler Werte sind bei der MDM-Registrierung.

<dl> <dt>

<span id="E_DATATYPE_MISMATCH"></span><span id="e_datatype_mismatch"></span>**E \_ DataType-Konflikt \_**
</dt> <dd> <dl> <dt>

0x8007065d
</dt> <dt>



Der Datentyp stimmt nicht mit dem erwarteten Datentyp.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_MESSAGE_FORMAT_ERROR"></span><span id="mregister_e_device_message_format_error"></span>**MRegister \_ E \_ Geräte \_ Nachrichten \_ Format \_ Fehler**
</dt> <dd> <dl> <dt>

0x80190001
</dt> <dt>



Ungültiges Schema, Nachrichten Formatierungs Fehler vom Server.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_MESSAGE_FORMAT_ERROR"></span><span id="menroll_e_device_message_format_error"></span>**Fehler für "menroll \_ E \_ Device \_ Message \_ Format \_ "**
</dt> <dd> <dl> <dt>

0x80180001
</dt> <dt>



Ungültiges Schema, Nachrichten Formatierungs Fehler vom Server.

**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_AUTHENTICATION_ERROR"></span><span id="mregister_e_device_authentication_error"></span>**MRegister \_ E \_ Geräte \_ Authentifizierungs \_ Fehler**
</dt> <dd> <dl> <dt>

0x80190002
</dt> <dt>



Der Benutzer konnte vom Server nicht authentifiziert werden.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_AUTHENTICATION_ERROR"></span><span id="menroll_e_device_authentication_error"></span>**Fehler beim Registrieren der \_ \_ Geräte \_ Authentifizierung \_ .**
</dt> <dd> <dl> <dt>

0x80180002
</dt> <dt>



Der Benutzer konnte vom Server nicht authentifiziert werden.

**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_AUTHORIZATION_ERROR"></span><span id="mregister_e_device_authorization_error"></span>**MRegister \_ E \_ Geräte \_ Autorisierungs \_ Fehler**
</dt> <dd> <dl> <dt>

0x80190003
</dt> <dt>



Der Benutzer ist nicht autorisiert, sich anzumelden.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_AUTHORIZATION_ERROR"></span><span id="menroll_e_device_authorization_error"></span>**menroll \_ E \_ Geräte \_ Autorisierungs \_ Fehler**
</dt> <dd> <dl> <dt>

0x80180003
</dt> <dt>



Der Benutzer ist nicht autorisiert, sich anzumelden.

**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_CERTIFCATEREQUEST_ERROR"></span><span id="mregister_e_device_certifcaterequest_error"></span>**MRegister \_ E \_ Gerät \_ certifcaterequest- \_ Fehler**
</dt> <dd> <dl> <dt>

0x80190004
</dt> <dt>



Der Benutzer hat keine Berechtigung für die Zertifikat Vorlage, oder die Zertifizierungsstelle ist nicht erreichbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_CERTIFCATEREQUEST_ERROR"></span><span id="menroll_e_device_certifcaterequest_error"></span>**"menroll \_ E" \_ \_ certifcaterequest- \_ Fehler**
</dt> <dd> <dl> <dt>

0x80180004
</dt> <dt>



Der Benutzer hat keine Berechtigung für die Zertifikat Vorlage, oder die Zertifizierungsstelle ist nicht erreichbar.

**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_CONFIGMGRSERVER_ERROR"></span><span id="mregister_e_device_configmgrserver_error"></span>**MRegister \_ E \_ Gerät \_ configmgrserver \_ Fehler**
</dt> <dd> <dl> <dt>

0x80190005
</dt> <dt>



Beim Management Server ist ein Fehler aufgetreten, z. b. ein Datenbankzugriffs Fehler.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_CONFIGMGRSERVER_ERROR"></span><span id="menroll_e_device_configmgrserver_error"></span>**\_ \_ \_ configmgrserver-Fehler bei "menroll E" \_**
</dt> <dd> <dl> <dt>

0x80180005
</dt> <dt>



Beim Management Server ist ein Fehler aufgetreten, z. b. ein Datenbankzugriffs Fehler.

**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_INTERNALSERVICE_ERROR"></span><span id="mregister_e_device_internalservice_error"></span>**Fehler im \_ \_ \_ internalservice für MRegister E-Geräte \_**
</dt> <dd> <dl> <dt>

0x80190006
</dt> <dt>



Auf dem Server ist eine nicht behandelte Ausnahme aufgetreten.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_INTERNALSERVICE_ERROR"></span><span id="menroll_e_device_internalservice_error"></span>**Fehler bei "menroll \_ E" \_ \_ internalservice \_**
</dt> <dd> <dl> <dt>

0x80180006
</dt> <dt>



Auf dem Server ist eine nicht behandelte Ausnahme aufgetreten.

**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_INVALIDSECURITY_ERROR"></span><span id="mregister_e_device_invalidsecurity_error"></span>**MRegister \_ E \_ Geräte \_ invalidsecurity- \_ Fehler**
</dt> <dd> <dl> <dt>

0x80190007
</dt> <dt>



Auf dem Server ist eine nicht behandelte Ausnahme aufgetreten.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_INVALIDSECURITY_ERROR"></span><span id="menroll_e_device_invalidsecurity_error"></span>**Fehler bei "menroll \_ E \_ Device \_ invalidsecurity" \_**
</dt> <dd> <dl> <dt>

0x80180007
</dt> <dt>



Auf dem Server ist eine nicht behandelte Ausnahme aufgetreten.

**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_UNKNOWN_ERROR"></span><span id="mregister_e_device_unknown_error"></span>**\_ \_ \_ unbekannter \_ Fehler bei MRegister E-Gerät**
</dt> <dd> <dl> <dt>

0x80190008
</dt> <dt>



Unbekannter Server Fehler.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_UNKNOWN_ERROR"></span><span id="menroll_e_device_unknown_error"></span>**\_ \_ \_ unbekannter \_ Fehler bei "menroll E".**
</dt> <dd> <dl> <dt>

0x80180008
</dt> <dt>



Unbekannter Server Fehler.

**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_REGISTRATION_IN_PROGRESS"></span><span id="mregister_e_registration_in_progress"></span>**MRegister \_ E \_ Registrierung \_ wird \_ ausgeführt**
</dt> <dd> <dl> <dt>

0x80190009
</dt> <dt>



Zurzeit wird ein weiterer Registrierungsvorgang ausgeführt.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_ENROLLMENT_IN_PROGRESS"></span><span id="menroll_e_enrollment_in_progress"></span>**die Registrierung für die Registrierung wird durchgeführt. \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

0x80180009
</dt> <dt>



Zurzeit wird ein weiterer Registrierungsvorgang ausgeführt.

**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_ALREADY_REGISTERED"></span><span id="mregister_e_device_already_registered"></span>**MRegister \_ E \_ Gerät \_ bereits \_ registriert**
</dt> <dd> <dl> <dt>

0x8019000a
</dt> <dt>



Nicht mehr verwendet.

**Windows 8.1:** Das Gerät ist bereits registriert.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_ALREADY_ENROLLED"></span><span id="menroll_e_device_already_enrolled"></span>**Das \_ Gerät ist \_ \_ bereits \_ registriert.**
</dt> <dd> <dl> <dt>

0x8018000a
</dt> <dt>



Das Gerät ist bereits registriert.

**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_NOT_REGISTERED"></span><span id="mregister_e_device_not_registered"></span>**MRegister \_ E \_ Gerät \_ nicht \_ registriert**
</dt> <dd> <dl> <dt>

0x8019000b
</dt> <dt>



Nicht mehr verwendet.

**Windows 8.1:** Das Gerät ist nicht registriert.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_NOT_ENROLLED"></span><span id="menroll_e_device_not_enrolled"></span>**menroll \_ E \_ Gerät \_ nicht \_ registriert**
</dt> <dd> <dl> <dt>

0x8018000b
</dt> <dt>



Das Gerät ist nicht registriert.

**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DISCOVERY_REDIRECTED"></span><span id="mregister_e_discovery_redirected"></span>**MRegister \_ E-Ermittlung \_ \_ umgeleitet**
</dt> <dd> <dl> <dt>

0x8019000c
</dt> <dt>



Nicht mehr verwendet.

**Windows 8.1:** Die Umleitung ist erforderlich.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_NOT_AD_REGISTERED_ERROR"></span><span id="mregister_e_device_not_ad_registered_error"></span>**Fehler beim Registrieren des Registrierungs \_ \_ Geräts E \_ nicht \_ AD \_ \_**
</dt> <dd> <dl> <dt>

0x8019000d
</dt> <dt>



Nicht mehr verwendet.

**Windows 8.1:** Das Gerät ist nicht bei Active Directory registriert.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DISCOVERY_SEC_CERT_DATE_INVALID"></span><span id="menroll_e_discovery_sec_cert_date_invalid"></span>**"menroll \_ E \_ Discovery sec"- \_ Zertifikat ist \_ \_ \_ ungültig.**
</dt> <dd> <dl> <dt>

0x8018000d
</dt> <dt>



Während der Ermittlung war das Datum des Zertifikats "Sek." ungültig.

**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DISCOVERY_FAILED"></span><span id="mregister_e_discovery_failed"></span>**MRegister-E-Ermittlung \_ \_ \_ fehlgeschlagen**
</dt> <dd> <dl> <dt>

0x8019000e
</dt> <dt>



Nicht mehr verwendet.

**Windows 8.1:** Fehler bei der Ermittlung. die Umleitung ist erforderlich.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PASSWORD_NEEDED"></span><span id="menroll_e_password_needed"></span>**\_ \_ Kennwort für Kennwort \_ erforderlich**
</dt> <dd> <dl> <dt>

0x8018000e
</dt> <dt>



Ein Kennwort ist erforderlich, wurde jedoch nicht angegeben.

**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_WAB_ERROR"></span><span id="menroll_e_wab_error"></span>**Fehler "menroll \_ E \_ WAB" \_**
</dt> <dd> <dl> <dt>

0x8018000f
</dt> <dt>



Fehler bei der WAB-Registrierung.

**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_CONNECTIVITY"></span><span id="menroll_e_connectivity"></span>**menroll \_ E \_ Konnektivität**
</dt> <dd> <dl> <dt>

0x80180010
</dt> <dt>



Ein Netzwerkfehler ist aufgetreten, z. b. DNS oder ein Netzwerk Timeout.

**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_S_ENROLLMENT_SUSPENDED"></span><span id="menroll_s_enrollment_suspended"></span>**die Registrierung der \_ menrolls wurde \_ \_ unterbrochen.**
</dt> <dd> <dl> <dt>

0x00180011
</dt> <dt>



Die Registrierung wurde angehalten. Wird nicht mehr unterstützt.

**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_INVALIDSSLCERT"></span><span id="menroll_e_invalidsslcert"></span>**menroll \_ E \_ invalidsslcert**
</dt> <dd> <dl> <dt>

0x80180012
</dt> <dt>



Das SSL-Zertifikat war ungültig.

**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICECAPREACHED"></span><span id="menroll_e_devicecapreached"></span>**menroll E Geräte-App-Limit \_ \_ erreicht**
</dt> <dd> <dl> <dt>

0x80180013
</dt> <dt>



Der Benutzer hat bereits zu viele Geräte registriert. Löschen Sie alte, oder heben Sie die Registrierung auf, um diesen Fehler zu beheben Beachten Sie, dass der Benutzer diesen Fehler ohne Administrator Unterstützung beheben kann.

**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICENOTSUPPORTED"></span><span id="menroll_e_devicenotsupported"></span>**menroll \_ E \_ devicenotsupported**
</dt> <dd> <dl> <dt>

Nummer 0x80180014
</dt> <dt>



Eine bestimmte Plattform (z. b. Windows) oder die Version wird nicht unterstützt. Die allgemeine Behebung dieses Fehlers besteht darin, das Gerät zu aktualisieren.

**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_NOTSUPPORTED"></span><span id="menroll_e_notsupported"></span>**menroll \_ E \_ NotSupported**
</dt> <dd> <dl> <dt>

0x80180015
</dt> <dt>



Die Verwaltung mobiler Geräte wird für dieses Gerät in der Regel nicht unterstützt. der Benutzer kann den Administrator anrufen, aber es ist unwahrscheinlich, dass dieses Problem behoben wird.

**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_NOTELIGIBLETORENEW"></span><span id="mregister_e_noteligibletorenew"></span>**MRegister \_ E \_ noteligibletor**
</dt> <dd> <dl> <dt>

0x80180016
</dt> <dt>



Das Gerät versucht, eine Erneuerung durchzusetzen, aber der Server hat die Anforderung abgelehnt. Prüfen Sie die Uhrzeit auf dem Gerät. Der Benutzer kann diesen Fehler ggf. beheben, indem er sich erneut anmelden.

**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_INMAINTENANCE"></span><span id="menroll_e_inmaintenance"></span>**menroll \_ E \_ inmaintenance**
</dt> <dd> <dl> <dt>

0x80180017
</dt> <dt>



Das Konto befindet sich im Wartungsmodus. versuchen Sie es später erneut. Der Benutzer kann den Vorgang später wiederholen. Der Benutzer kann jedoch den Administrator anrufen, um den Wartungs Zeitplan zu bestimmen.

**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_USERLICENSE"></span><span id="menroll_e_userlicense"></span>**menroll \_ E \_ userlicense**
</dt> <dd> <dl> <dt>

0x80180018
</dt> <dt>



Die Lizenz des Benutzers befindet sich in einem ungültigen Zustand, der die Registrierung blockiert. der Benutzer muss den Administrator anrufen.

**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_ENROLLMENTDATAINVALID"></span><span id="menroll_e_enrollmentdatainvalid"></span>**menroll \_ E \_ anmelmentdatainvalid**
</dt> <dd> <dl> <dt>

0x80180019
</dt> <dt>



Der Server hat die Registrierungsdaten abgelehnt. der Server ist möglicherweise nicht ordnungsgemäß konfiguriert.

**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_INSECUREREDIRECT"></span><span id="menroll_e_insecureredirect"></span>**menroll \_ E \_ insecureredirect**
</dt> <dd> <dl> <dt>

0x8018001a
</dt> <dt>



Der Server hat http anstelle von HTTPS angefordert, aber es wurde nicht akzeptiert.

**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PLATFORM_WRONG_STATE"></span><span id="menroll_e_platform_wrong_state"></span>**\_ \_ \_ falscher Status der unplattform \_**
</dt> <dd> <dl> <dt>

0x8018001b
</dt> <dt>



Es wurde versucht, das gleiche Gerät zweimal zu registrieren oder die Registrierung eines unbekannten Geräts aufzuheben.

**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PLATFORM_LICENSE_ERROR"></span><span id="menroll_e_platform_license_error"></span>**Fehler bei der menrollout \_ E \_ Platform- \_ Lizenz \_**
</dt> <dd> <dl> <dt>

0x8018001c
</dt> <dt>



Dieser registriungstyp wird von der auf dem Client installierten Windows-Version nicht unterstützt.

**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PLATFORM_UNKNOWN_ERROR"></span><span id="menroll_e_platform_unknown_error"></span>**Unbekannter Fehler bei "menroll \_ E \_ Platform" \_ . \_**
</dt> <dd> <dl> <dt>

0x8018001d
</dt> <dt>



Auf dem Client ist ein unbekannter Fehler aufgetreten.

**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_CERTSTORE"></span><span id="menroll_e_prov_csp_certstore"></span>**menroll \_ E \_ Prov \_ CSP \_ certstore**
</dt> <dd> <dl> <dt>

0x8018001e
</dt> <dt>



Fehler bei der Bereitstellung im Zertifikat Speicher-CSP.

**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_W7"></span><span id="menroll_e_prov_csp_w7"></span>**Menroll \_ E \_ Prov \_ CSP \_ W7**
</dt> <dd> <dl> <dt>

0x8018001f
</dt> <dt>



Fehler bei der Bereitstellung in einem W7/dmacc-cpp.

**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_DMCLIENT"></span><span id="menroll_e_prov_csp_dmclient"></span>**ENROLL \_ E \_ Prov \_ CSP \_ dmclient**
</dt> <dd> <dl> <dt>

0x80180020
</dt> <dt>



Fehler bei der Bereitstellung in einem DM-Client-CSP.

**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_PFW"></span><span id="menroll_e_prov_csp_pfw"></span>**menroll \_ E \_ Prov \_ CSP \_ PFW**
</dt> <dd> <dl> <dt>

0x80180021
</dt> <dt>



Fehler bei der Bereitstellung in einem Passport for Work-CSP.

**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_MISC"></span><span id="menroll_e_prov_csp_misc"></span>**menroll \_ E \_ Prov \_ CSP \_ misc**
</dt> <dd> <dl> <dt>

0x80180022
</dt> <dt>



Fehler bei der Bereitstellung in einem CSP, der oben nicht aufgeführt ist.

**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_UNKNOWN"></span><span id="menroll_e_prov_unknown"></span>**\_ \_ unbekannte E Prov- \_ Datei**
</dt> <dd> <dl> <dt>

0x80180023
</dt> <dt>



Fehler bei der Bereitstellung, aber es ist kein bestimmter CSP angegeben.

**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_SSLCERTNOTFOUND"></span><span id="menroll_e_prov_sslcertnotfound"></span>**menroll \_ E \_ Prov \_ sslcertnotfound**
</dt> <dd> <dl> <dt>

0x80180024
</dt> <dt>



Beim Versuch, den öffentlichen Zertifikat/privaten Schlüssel zu binden, wurde das öffentliche Zertifikat entweder nicht gefunden: beim Versuch, den öffentlichen Zertifikat/privaten Schlüssel zu binden, oder bei der Überprüfung der Nutzlast (möglicherweise auf den falschen Speicher).

**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_APPMGMT"></span><span id="menroll_e_prov_csp_appmgmt"></span>**menroll \_ E \_ Prov \_ CSP \_ Appmgmt**
</dt> <dd> <dl> <dt>

0x80180025
</dt> <dt>



Fehler bei der Bereitstellung im enterpritsappmanagement-CSP.

> [!Note]  
> Diese Konstante ist vor Windows 10, Version 1709, nicht verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_MANAGEMENT_BLOCKED"></span><span id="menroll_e_device_management_blocked"></span>**die \_ \_ Geräteverwaltung wurde \_ \_ gesperrt.**
</dt> <dd> <dl> <dt>

0x80180026
</dt> <dt>



Die Verwaltung mobiler Geräte (Mobile Device Management, MDM) wurde blockiert, möglicherweise durch Gruppenrichtlinie oder die Funktion [**setmanagedexternally**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-setmanagedexternally) .

> [!Note]  
> Diese Konstante ist vor Windows 10, Version 1709, nicht verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_CERTPOLICY_PRIVATEKEYCREATION_FAILED"></span><span id="menroll_e_certpolicy_privatekeycreation_failed"></span>**menroll \_ E \_ certpolicy \_ privatekeycreation \_ fehlgeschlagen**
</dt> <dd> <dl> <dt>

0x80180027
</dt> <dt>



Der private Schlüssel konnte nicht erstellt werden.

> [!Note]  
> Diese Konstante ist vor Windows 10, Version 1709, nicht verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_CERTAUTH_FAILED_TO_FIND_CERT"></span><span id="menroll_e_certauth_failed_to_find_cert"></span>**"menroll \_ E \_ certauth" konnte das \_ \_ \_ Zertifikat nicht finden \_ .**
</dt> <dd> <dl> <dt>

0x80180028
</dt> <dt>



Die Zertifikat Authentifizierung wurde angefordert, aber es wurde ein nicht verwendende Zertifikat gefunden.

> [!Note]  
> Diese Konstante ist vor Windows 10, Version 1709, nicht verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_EMPTY_MESSAGE"></span><span id="menroll_e_empty_message"></span>**\_ \_ leere \_ Nachricht für "menroll"**
</dt> <dd> <dl> <dt>

0x80180029
</dt> <dt>



Der Server hat mit HTTP 200 geantwortet, aber die Nachricht war leer.

> [!Note]  
> Diese Konstante ist vor Windows 10, Version 1709, nicht verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_USER_CANCELED_"></span><span id="menroll_e_user_canceled_"></span>**menroll \_ E \_ Benutzer \_ abgebrochen** 
</dt> <dd> <dl> <dt>

0x80180030
</dt> <dt>



Der Benutzer hat den Vorgang abgebrochen.

> [!Note]  
> Diese Konstante ist vor Windows 10, Version 1709, nicht verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_MDM_NOT_CONFIGURED"></span><span id="menroll_e_mdm_not_configured"></span>**menroll \_ E \_ MDM \_ nicht \_ konfiguriert**
</dt> <dd> <dl> <dt>

0x80180031
</dt> <dt>



Die Verwaltung mobiler Geräte (Mobile Device Management, MDM) ist nicht konfiguriert.

> [!Note]  
> Diese Konstante ist vor Windows 10, Version 1709, nicht verfügbar.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                    |
| Header<br/>                   | <dl> <dt>Mdmregistration. h</dt> </dl> |



 

 





