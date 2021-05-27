---
title: Fehlerwerte für die MDM-Registrierung (MDMRegistration.h)
description: Die folgenden Fehlerwerte gelten für die MDM-Registrierung.
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
ms.openlocfilehash: cb62977a48400866e9fa8829696c884e58e54325
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548985"
---
# <a name="mdm-registration-error-values"></a>Fehlerwerte für die MDM-Registrierung

Die folgenden Fehlerwerte gelten für die MDM-Registrierung.

<dl> <dt>

<span id="E_DATATYPE_MISMATCH"></span><span id="e_datatype_mismatch"></span>**\_ \_ E-DATENTYPKONFLIKT**
</dt> <dd> <dl> <dt>

0x8007065d
</dt> <dt>



Der Datentyp passt nicht zum erwarteten Datentyp.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_MESSAGE_FORMAT_ERROR"></span><span id="mregister_e_device_message_format_error"></span>**MREGISTER \_ E \_ DEVICE \_ MESSAGE \_ FORMAT \_ ERROR**
</dt> <dd> <dl> <dt>

0x80190001
</dt> <dt>



Ungültiges Schema, Meldungsformatfehler vom Server.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_MESSAGE_FORMAT_ERROR"></span><span id="menroll_e_device_message_format_error"></span>**MENROLL \_ E \_ DEVICE \_ MESSAGE \_ FORMAT \_ ERROR**
</dt> <dd> <dl> <dt>

0x80180001
</dt> <dt>



Ungültiges Schema, Meldungsformatfehler vom Server.

**Windows 8.1:** Diese Konstante ist nicht verfügbar, bevor Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_AUTHENTICATION_ERROR"></span><span id="mregister_e_device_authentication_error"></span>**MREGISTER \_ E DEVICE AUTHENTICATION ERROR (MREGISTER \_ E-GERÄTEAUTHENTIFIZIERUNGSFEHLER) \_ \_**
</dt> <dd> <dl> <dt>

0x80190002
</dt> <dt>



Der Server konnte den Benutzer nicht authentifizieren.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_AUTHENTICATION_ERROR"></span><span id="menroll_e_device_authentication_error"></span>**MENROLL \_ E \_ DEVICE \_ AUTHENTICATION \_ ERROR**
</dt> <dd> <dl> <dt>

0x80180002
</dt> <dt>



Der Server konnte den Benutzer nicht authentifizieren.

**Windows 8.1:** Diese Konstante ist nicht verfügbar, bevor Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_AUTHORIZATION_ERROR"></span><span id="mregister_e_device_authorization_error"></span>**MREGISTER \_ E \_ DEVICE \_ AUTHORIZATION \_ ERROR**
</dt> <dd> <dl> <dt>

0x80190003
</dt> <dt>



Der Benutzer ist nicht für die Registrierung autorisiert.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_AUTHORIZATION_ERROR"></span><span id="menroll_e_device_authorization_error"></span>**MENROLL \_ \_ E-GERÄTEAUTORISIERUNGSFEHLER \_ \_**
</dt> <dd> <dl> <dt>

0x80180003
</dt> <dt>



Der Benutzer ist nicht für die Registrierung autorisiert.

**Windows 8.1:** Diese Konstante ist vor Windows 10 nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_CERTIFCATEREQUEST_ERROR"></span><span id="mregister_e_device_certifcaterequest_error"></span>**MREGISTER \_ E \_ DEVICE \_ CERTIFCATEREQUEST \_ ERROR**
</dt> <dd> <dl> <dt>

0x80190004
</dt> <dt>



Der Benutzer hat keine Berechtigung für die Zertifikatvorlage, oder die Zertifizierungsstelle ist nicht erreichbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_CERTIFCATEREQUEST_ERROR"></span><span id="menroll_e_device_certifcaterequest_error"></span>**MENROLL \_ E \_ DEVICE \_ CERTIFCATEREQUEST \_ ERROR**
</dt> <dd> <dl> <dt>

0x80180004
</dt> <dt>



Der Benutzer hat keine Berechtigung für die Zertifikatvorlage, oder die Zertifizierungsstelle ist nicht erreichbar.

**Windows 8.1:** Diese Konstante ist vor Windows 10 nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_CONFIGMGRSERVER_ERROR"></span><span id="mregister_e_device_configmgrserver_error"></span>**MREGISTER \_ E \_ DEVICE \_ CONFIGMGRSERVER \_ ERROR**
</dt> <dd> <dl> <dt>

0x80190005
</dt> <dt>



Auf dem Verwaltungsserver ist ein Fehler aufgetreten, z. B. ein Datenbankzugriffsfehler.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_CONFIGMGRSERVER_ERROR"></span><span id="menroll_e_device_configmgrserver_error"></span>**MENROLL \_ E \_ DEVICE \_ CONFIGMGRSERVER \_ ERROR**
</dt> <dd> <dl> <dt>

0x80180005
</dt> <dt>



Auf dem Verwaltungsserver ist ein Fehler aufgetreten, z. B. ein Datenbankzugriffsfehler.

**Windows 8.1:** Diese Konstante ist nicht verfügbar, bevor Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_INTERNALSERVICE_ERROR"></span><span id="mregister_e_device_internalservice_error"></span>**MREGISTER \_ E \_ DEVICE \_ INTERNALSERVICE \_ ERROR**
</dt> <dd> <dl> <dt>

0x80190006
</dt> <dt>



Es gab eine nicht behandelte Ausnahme auf dem Server.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_INTERNALSERVICE_ERROR"></span><span id="menroll_e_device_internalservice_error"></span>**MENROLL \_ E \_ DEVICE \_ INTERNALSERVICE \_ ERROR**
</dt> <dd> <dl> <dt>

0x80180006
</dt> <dt>



Auf dem Server ist eine nicht behandelte Ausnahme vorgehanden.

**Windows 8.1:** Diese Konstante ist nicht verfügbar, bevor Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_INVALIDSECURITY_ERROR"></span><span id="mregister_e_device_invalidsecurity_error"></span>**MREGISTER \_ E \_ DEVICE \_ INVALIDSECURITY \_ ERROR**
</dt> <dd> <dl> <dt>

0x80190007
</dt> <dt>



Es gab eine nicht behandelte Ausnahme auf dem Server.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_INVALIDSECURITY_ERROR"></span><span id="menroll_e_device_invalidsecurity_error"></span>**MENROLL \_ E \_ DEVICE \_ INVALIDSECURITY \_ ERROR**
</dt> <dd> <dl> <dt>

0x80180007
</dt> <dt>



Es gab eine nicht behandelte Ausnahme auf dem Server.

**Windows 8.1:** Diese Konstante ist nicht verfügbar, bevor Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_UNKNOWN_ERROR"></span><span id="mregister_e_device_unknown_error"></span>**MREGISTER \_ E \_ DEVICE \_ UNKNOWN \_ ERROR**
</dt> <dd> <dl> <dt>

0x80190008
</dt> <dt>



Unbekannter Serverfehler.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_UNKNOWN_ERROR"></span><span id="menroll_e_device_unknown_error"></span>**MENROLL \_ E \_ DEVICE \_ UNKNOWN \_ ERROR**
</dt> <dd> <dl> <dt>

0x80180008
</dt> <dt>



Unbekannter Serverfehler.

**Windows 8.1:** Diese Konstante ist vor Windows 10 nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_REGISTRATION_IN_PROGRESS"></span><span id="mregister_e_registration_in_progress"></span>**MREGISTER \_ E REGISTRATION IN \_ \_ \_ BEARBEITUNG**
</dt> <dd> <dl> <dt>

0x80190009
</dt> <dt>



Derzeit wird ein weiterer Registrierungsvorgang durchgeführt.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_ENROLLMENT_IN_PROGRESS"></span><span id="menroll_e_enrollment_in_progress"></span>**MENROLL \_ E \_ ENROLLMENT \_ IN \_ PROGRESS**
</dt> <dd> <dl> <dt>

0x80180009
</dt> <dt>



Derzeit wird ein weiterer Registrierungsvorgang durchgeführt.

**Windows 8.1:** Diese Konstante ist vor Windows 10 nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_ALREADY_REGISTERED"></span><span id="mregister_e_device_already_registered"></span>**MREGISTER \_ E \_ DEVICE \_ ALREADY \_ REGISTERED**
</dt> <dd> <dl> <dt>

0x8019000A
</dt> <dt>



Nicht mehr verwendet.

**Windows 8.1:** Das Gerät ist bereits registriert.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_ALREADY_ENROLLED"></span><span id="menroll_e_device_already_enrolled"></span>**MENROLL \_ \_ E-GERÄT \_ BEREITS \_ REGISTRIERT**
</dt> <dd> <dl> <dt>

0x8018000A
</dt> <dt>



Das Gerät ist bereits registriert.

**Windows 8.1:** Diese Konstante ist vor Windows 10 nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_NOT_REGISTERED"></span><span id="mregister_e_device_not_registered"></span>**MREGISTER \_ E \_ DEVICE \_ NOT \_ REGISTERED**
</dt> <dd> <dl> <dt>

0x8019000B
</dt> <dt>



Nicht mehr verwendet.

**Windows 8.1:** Das Gerät ist nicht registriert.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_NOT_ENROLLED"></span><span id="menroll_e_device_not_enrolled"></span>**MENROLL \_ \_ E-GERÄT \_ NICHT \_ REGISTRIERT**
</dt> <dd> <dl> <dt>

0x8018000B
</dt> <dt>



Das Gerät ist nicht registriert.

**Windows 8.1:** Diese Konstante ist nicht verfügbar, bevor Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DISCOVERY_REDIRECTED"></span><span id="mregister_e_discovery_redirected"></span>**MREGISTER \_ E \_ DISCOVERY \_ REDIRECTED**
</dt> <dd> <dl> <dt>

0x8019000C
</dt> <dt>



Nicht mehr verwendet.

**Windows 8.1:** Eine Umleitung ist erforderlich.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_NOT_AD_REGISTERED_ERROR"></span><span id="mregister_e_device_not_ad_registered_error"></span>**MREGISTER \_ E \_ DEVICE \_ NOT \_ AD \_ REGISTERED \_ ERROR**
</dt> <dd> <dl> <dt>

0x8019000D
</dt> <dt>



Nicht mehr verwendet.

**Windows 8.1:** Das Gerät ist nicht bei Active Directory registriert.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DISCOVERY_SEC_CERT_DATE_INVALID"></span><span id="menroll_e_discovery_sec_cert_date_invalid"></span>**MENROLL \_ E \_ DISCOVERY \_ SEC \_ CERT \_ DATE \_ INVALID**
</dt> <dd> <dl> <dt>

0x8018000D
</dt> <dt>



Während der Ermittlung war das Datum des Sec-Zertifikats ungültig.

**Windows 8.1:** Diese Konstante ist nicht verfügbar, bevor Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DISCOVERY_FAILED"></span><span id="mregister_e_discovery_failed"></span>**FEHLER BEI DER \_ MREGISTER \_ \_ E-ERMITTLUNG**
</dt> <dd> <dl> <dt>

0x8019000E
</dt> <dt>



Nicht mehr verwendet.

**Windows 8.1:** Fehler bei der Ermittlung; -Umleitung ist erforderlich.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PASSWORD_NEEDED"></span><span id="menroll_e_password_needed"></span>**MENROLL \_ E \_ PASSWORD \_ NEEDED**
</dt> <dd> <dl> <dt>

0x8018000E
</dt> <dt>



Ein Kennwort ist erforderlich, wurde aber nicht angegeben.

**Windows 8.1:** Diese Konstante ist nicht verfügbar, bevor Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_WAB_ERROR"></span><span id="menroll_e_wab_error"></span>**MENROLL \_ E \_ WAB-FEHLER \_**
</dt> <dd> <dl> <dt>

0x8018000F
</dt> <dt>



Fehler bei der WAB-Registrierung.

**Windows 8.1:** Diese Konstante ist vor Windows 10 nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_CONNECTIVITY"></span><span id="menroll_e_connectivity"></span>**MENROLL \_ E \_ CONNECTIVITY**
</dt> <dd> <dl> <dt>

0x80180010
</dt> <dt>



Ein Netzwerkfehler ist aufgetreten, z. B. DNS oder ein Netzwerktimeout.

**Windows 8.1:** Diese Konstante ist vor Windows 10 nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_S_ENROLLMENT_SUSPENDED"></span><span id="menroll_s_enrollment_suspended"></span>**MENROLL \_ S \_ ENROLLMENT \_ SUSPENDED**
</dt> <dd> <dl> <dt>

0x00180011
</dt> <dt>



Die Registrierung wurde angehalten. Wird nicht mehr unterstützt.

**Windows 8.1:** Diese Konstante ist vor Windows 10 nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_INVALIDSSLCERT"></span><span id="menroll_e_invalidsslcert"></span>**MENROLL \_ E \_ INVALIDSSLCERT**
</dt> <dd> <dl> <dt>

0x80180012
</dt> <dt>



Das SSL-Zertifikat war ungültig.

**Windows 8.1:** Diese Konstante ist vor Windows 10 nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICECAPREACHED"></span><span id="menroll_e_devicecapreached"></span>**MENROLL \_ E \_ DEVICECAPREACHED**
</dt> <dd> <dl> <dt>

0x80180013
</dt> <dt>



Der Benutzer hat bereits zu viele Geräte registriert. Löschen Sie alte, oder entfernen Sie die Registrierung, um diesen Fehler zu beheben. Beachten Sie, dass der Benutzer diesen Fehler ohne Administratorunterstützung beheben kann.

**Windows 8.1:** Diese Konstante ist nicht verfügbar, bevor Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICENOTSUPPORTED"></span><span id="menroll_e_devicenotsupported"></span>**MENROLL \_ E \_ DEVICENOTSUPPORTED**
</dt> <dd> <dl> <dt>

0x80180014
</dt> <dt>



Eine bestimmte Plattform (z. B. Windows) oder Version wird nicht unterstützt. Die allgemeine Fehlerbehebung für diesen Fehler besteht im Upgrade des Geräts.

**Windows 8.1:** Diese Konstante ist nicht verfügbar, bevor Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_NOTSUPPORTED"></span><span id="menroll_e_notsupported"></span>**MENROLL \_ E \_ NOTSUPPORTED**
</dt> <dd> <dl> <dt>

0x80180015
</dt> <dt>



Die Verwaltung mobiler Geräte wird für dieses Gerät im Allgemeinen nicht unterstützt. Der Benutzer kann den Administrator anrufen, wird dieses Problem jedoch wahrscheinlich nicht beheben.

**Windows 8.1:** Diese Konstante ist nicht verfügbar, bevor Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_NOTELIGIBLETORENEW"></span><span id="mregister_e_noteligibletorenew"></span>**MREGISTER \_ E \_ NOTELIGIBLETORENEW**
</dt> <dd> <dl> <dt>

0x80180016
</dt> <dt>



Das Gerät versucht zu erneuern, aber der Server hat die Anforderung abgelehnt. Überprüfen Sie die Zeit auf dem Gerät. Der Benutzer kann diesen Fehler möglicherweise beheben, indem er sich erneut registriert.

**Windows 8.1:** Diese Konstante ist nicht verfügbar, bevor Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_INMAINTENANCE"></span><span id="menroll_e_inmaintenance"></span>**MENROLL \_ E \_ INMAINTENANCE**
</dt> <dd> <dl> <dt>

0x80180017
</dt> <dt>



Das Konto befindet sich in Wartung; Wiederholen Sie den Vorgang später. Der Benutzer kann den Vorgang später wiederholen. Der Benutzer kann jedoch den Administrator aufrufen, um den Wartungszeitplan zu bestimmen.

**Windows 8.1:** Diese Konstante ist vor Windows 10 nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_USERLICENSE"></span><span id="menroll_e_userlicense"></span>**MENROLL \_ E \_ USERLICENSE**
</dt> <dd> <dl> <dt>

0x80180018
</dt> <dt>



Die Lizenz des Benutzers befindet sich in einem ungültigen Zustand und blockiert die Registrierung. der Benutzer muss den Administrator aufrufen.

**Windows 8.1:** Diese Konstante ist vor Windows 10 nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_ENROLLMENTDATAINVALID"></span><span id="menroll_e_enrollmentdatainvalid"></span>**MENROLL \_ E \_ ENROLLMENTDATAINVALID**
</dt> <dd> <dl> <dt>

0x80180019
</dt> <dt>



Der Server hat die Registrierungsdaten abgelehnt. Der Server ist möglicherweise nicht ordnungsgemäß konfiguriert.

**Windows 8.1:** Diese Konstante ist vor Windows 10 nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_INSECUREREDIRECT"></span><span id="menroll_e_insecureredirect"></span>**MENROLL \_ E \_ INSECUREREDIRECT**
</dt> <dd> <dl> <dt>

0x8018001A
</dt> <dt>



Der Server hat HTTP anstelle von HTTPS angefordert, aber er wurde nicht akzeptiert.

**Windows 8.1:** Diese Konstante ist vor Windows 10 nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PLATFORM_WRONG_STATE"></span><span id="menroll_e_platform_wrong_state"></span>**MENROLL \_ E \_ PLATFORM \_ WRONG \_ STATE**
</dt> <dd> <dl> <dt>

0x8018001B
</dt> <dt>



Es wurde ein ungültiger Vorgang versucht, z. B. zweimal dasselbe Gerät zu registrieren oder die Registrierung eines unbekannten Geräts zu aufheben.

**Windows 8.1:** Diese Konstante ist vor Windows 10 nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PLATFORM_LICENSE_ERROR"></span><span id="menroll_e_platform_license_error"></span>**MENROLL \_ E \_ PLATFORM \_ LICENSE \_ ERROR**
</dt> <dd> <dl> <dt>

0x8018001C
</dt> <dt>



Die auf dem Client installierte Windows-Version unterstützt diesen Registrierungstyp nicht.

**Windows 8.1:** Diese Konstante ist nicht verfügbar, bevor Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PLATFORM_UNKNOWN_ERROR"></span><span id="menroll_e_platform_unknown_error"></span>**MENROLL \_ E \_ PLATFORM \_ UNKNOWN \_ ERROR**
</dt> <dd> <dl> <dt>

0x8018001D
</dt> <dt>



Auf dem Client ist ein unbekannter Fehler aufgetreten.

**Windows 8.1:** Diese Konstante ist nicht verfügbar, bevor Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_CERTSTORE"></span><span id="menroll_e_prov_csp_certstore"></span>**MENROLL \_ E \_ PROV \_ CSP \_ CERTSTORE**
</dt> <dd> <dl> <dt>

0x8018001E
</dt> <dt>



Fehler bei der Bereitstellung im Zertifikatspeicher-CSP.

**Windows 8.1:** Diese Konstante ist nicht verfügbar, bevor Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_W7"></span><span id="menroll_e_prov_csp_w7"></span>**MENROLL \_ E \_ PROV \_ CSP \_ W7**
</dt> <dd> <dl> <dt>

0x8018001F
</dt> <dt>



Fehler bei der Bereitstellung in einem W7/DMAcc-CPP.

**Windows 8.1:** Diese Konstante ist nicht verfügbar, bevor Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_DMCLIENT"></span><span id="menroll_e_prov_csp_dmclient"></span>**MENROLL \_ E \_ PROV \_ CSP \_ DMCLIENT**
</dt> <dd> <dl> <dt>

0x80180020
</dt> <dt>



Fehler bei der Bereitstellung in einem DM-Client-CSP.

**Windows 8.1:** Diese Konstante ist nicht verfügbar, bevor Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_PFW"></span><span id="menroll_e_prov_csp_pfw"></span>**MENROLL \_ E \_ PROV \_ CSP \_ PFW**
</dt> <dd> <dl> <dt>

0x80180021
</dt> <dt>



Fehler bei der Bereitstellung in einem Passport for Work-CSP.

**Windows 8.1:** Diese Konstante ist vor Windows 10 nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_MISC"></span><span id="menroll_e_prov_csp_misc"></span>**MENROLL \_ E \_ PROV \_ CSP \_ MISC**
</dt> <dd> <dl> <dt>

0x80180022
</dt> <dt>



Fehler bei der Bereitstellung in einem CSP, der oben nicht aufgeführt ist.

**Windows 8.1:** Diese Konstante ist vor Windows 10 nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_UNKNOWN"></span><span id="menroll_e_prov_unknown"></span>**MENROLL \_ E \_ PROV \_ UNKNOWN**
</dt> <dd> <dl> <dt>

0x80180023
</dt> <dt>



Fehler bei der Bereitstellung, aber ein bestimmter CSP ist nicht angegeben.

**Windows 8.1:** Diese Konstante ist vor Windows 10 nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_SSLCERTNOTFOUND"></span><span id="menroll_e_prov_sslcertnotfound"></span>**MENROLL \_ E \_ PROV \_ SSLCERTNOTFOUND**
</dt> <dd> <dl> <dt>

0x80180024
</dt> <dt>



Beim Versuch, das öffentliche Zertifikat/den privaten Schlüssel zu binden, wurde das öffentliche Zertifikat nicht gefunden: beim Versuch, das öffentliche Zertifikat/den privaten Schlüssel zu binden, oder beim Untersuchen der Bereitstellungsnutzlast (möglicherweise für den falschen Speicher).

**Windows 8.1:** Diese Konstante ist vor Windows 10 nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_APPMGMT"></span><span id="menroll_e_prov_csp_appmgmt"></span>**MENROLL \_ E \_ PROV \_ CSP \_ APPMGMT**
</dt> <dd> <dl> <dt>

0x80180025
</dt> <dt>



Fehler bei der Bereitstellung im EnterpriseAppManagement-CSP.

> [!Note]  
> Diese Konstante ist vor Windows 10 Version 1709 nicht verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_MANAGEMENT_BLOCKED"></span><span id="menroll_e_device_management_blocked"></span>**MENROLL \_ \_ E-GERÄTEVERWALTUNG \_ \_ BLOCKIERT**
</dt> <dd> <dl> <dt>

0x80180026
</dt> <dt>



Mobile Geräteverwaltung (MDM) wurde blockiert, möglicherweise durch Gruppenrichtlinie oder die [**SetManagedExternally-Funktion.**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-setmanagedexternally)

> [!Note]  
> Diese Konstante ist vor Windows 10 Version 1709 nicht verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_CERTPOLICY_PRIVATEKEYCREATION_FAILED"></span><span id="menroll_e_certpolicy_privatekeycreation_failed"></span>**MENROLL \_ E \_ CERTPOLICY \_ PRIVATEKEYCREATION \_ FAILED**
</dt> <dd> <dl> <dt>

0x80180027
</dt> <dt>



Fehler beim Erstellen des privaten Schlüssels.

> [!Note]  
> Diese Konstante ist vor Windows 10 Version 1709 nicht verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_CERTAUTH_FAILED_TO_FIND_CERT"></span><span id="menroll_e_certauth_failed_to_find_cert"></span>**MENROLL E CERTAUTH FAILED TO FIND CERT (MENROLL \_ E \_ CERTAUTH \_ KONNTE \_ \_ \_ CERT NICHT FINDEN)**
</dt> <dd> <dl> <dt>

0x80180028
</dt> <dt>



Die Zertifikatauthentifizierung wurde angefordert, aber es ist ein Fehler beim Suchen eines zu verwendenden Zertifikats fehlgeschlagen.

> [!Note]  
> Diese Konstante ist vor Windows 10 Version 1709 nicht verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_EMPTY_MESSAGE"></span><span id="menroll_e_empty_message"></span>**MENROLL \_ E \_ EMPTY \_ MESSAGE**
</dt> <dd> <dl> <dt>

0x80180029
</dt> <dt>



Der Server hat mit HTTP 200 geantwortet, aber die Nachricht war leer.

> [!Note]  
> Diese Konstante ist vor Windows 10 Version 1709 nicht verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_USER_CANCELED_"></span><span id="menroll_e_user_canceled_"></span>**MENROLL \_ E \_ USER \_ CANCELED** 
</dt> <dd> <dl> <dt>

0x80180030
</dt> <dt>



Der Benutzer hat den Vorgang abgebrochen.

> [!Note]  
> Diese Konstante ist vor Windows 10 Version 1709 nicht verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_MDM_NOT_CONFIGURED"></span><span id="menroll_e_mdm_not_configured"></span>**MENROLL \_ E MDM NICHT \_ \_ \_ KONFIGURIERT**
</dt> <dd> <dl> <dt>

0x80180031
</dt> <dt>



Mobile Geräteverwaltung (MDM) ist nicht konfiguriert.

> [!Note]  
> Diese Konstante ist vor Windows 10 Version 1709 nicht verfügbar.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                    |
| Header<br/>                   | <dl> <dt>MDMRegistration.h</dt> </dl> |



 

 





