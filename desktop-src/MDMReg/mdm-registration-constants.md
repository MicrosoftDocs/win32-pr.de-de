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
# <a name="mdm-registration-error-values"></a><span data-ttu-id="2cc1e-103">MDM-Registrierungsfehler Werte</span><span class="sxs-lookup"><span data-stu-id="2cc1e-103">MDM Registration Error Values</span></span>

<span data-ttu-id="2cc1e-104">Die folgenden Fehler Werte sind bei der MDM-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-104">The following error values are with MDM Registration.</span></span>

<dl> <dt>

<span data-ttu-id="2cc1e-105"><span id="E_DATATYPE_MISMATCH"></span><span id="e_datatype_mismatch"></span>**E \_ DataType-Konflikt \_**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-105"><span id="E_DATATYPE_MISMATCH"></span><span id="e_datatype_mismatch"></span>**E\_DATATYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-106">0x8007065d</span><span class="sxs-lookup"><span data-stu-id="2cc1e-106">0x8007065d</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-107">Der Datentyp stimmt nicht mit dem erwarteten Datentyp.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-107">The datatype does not match the expected datatype.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-108"><span id="MREGISTER_E_DEVICE_MESSAGE_FORMAT_ERROR"></span><span id="mregister_e_device_message_format_error"></span>**MRegister \_ E \_ Geräte \_ Nachrichten \_ Format \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-108"><span id="MREGISTER_E_DEVICE_MESSAGE_FORMAT_ERROR"></span><span id="mregister_e_device_message_format_error"></span>**MREGISTER\_E\_DEVICE\_MESSAGE\_FORMAT\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-109">0x80190001</span><span class="sxs-lookup"><span data-stu-id="2cc1e-109">0x80190001</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-110">Ungültiges Schema, Nachrichten Formatierungs Fehler vom Server.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-110">Invalid Schema, Message Format Error from server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-111"><span id="MENROLL_E_DEVICE_MESSAGE_FORMAT_ERROR"></span><span id="menroll_e_device_message_format_error"></span>**Fehler für "menroll \_ E \_ Device \_ Message \_ Format \_ "**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-111"><span id="MENROLL_E_DEVICE_MESSAGE_FORMAT_ERROR"></span><span id="menroll_e_device_message_format_error"></span>**MENROLL\_E\_DEVICE\_MESSAGE\_FORMAT\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-112">0x80180001</span><span class="sxs-lookup"><span data-stu-id="2cc1e-112">0x80180001</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-113">Ungültiges Schema, Nachrichten Formatierungs Fehler vom Server.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-113">Invalid Schema , Message Format Error from server.</span></span>

<span data-ttu-id="2cc1e-114">**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-114">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-115"><span id="MREGISTER_E_DEVICE_AUTHENTICATION_ERROR"></span><span id="mregister_e_device_authentication_error"></span>**MRegister \_ E \_ Geräte \_ Authentifizierungs \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-115"><span id="MREGISTER_E_DEVICE_AUTHENTICATION_ERROR"></span><span id="mregister_e_device_authentication_error"></span>**MREGISTER\_E\_DEVICE\_AUTHENTICATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-116">0x80190002</span><span class="sxs-lookup"><span data-stu-id="2cc1e-116">0x80190002</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-117">Der Benutzer konnte vom Server nicht authentifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-117">Server failed to authenticate the user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-118"><span id="MENROLL_E_DEVICE_AUTHENTICATION_ERROR"></span><span id="menroll_e_device_authentication_error"></span>**Fehler beim Registrieren der \_ \_ Geräte \_ Authentifizierung \_ .**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-118"><span id="MENROLL_E_DEVICE_AUTHENTICATION_ERROR"></span><span id="menroll_e_device_authentication_error"></span>**MENROLL\_E\_DEVICE\_AUTHENTICATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-119">0x80180002</span><span class="sxs-lookup"><span data-stu-id="2cc1e-119">0x80180002</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-120">Der Benutzer konnte vom Server nicht authentifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-120">Server failed to authenticate the user.</span></span>

<span data-ttu-id="2cc1e-121">**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-121">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-122"><span id="MREGISTER_E_DEVICE_AUTHORIZATION_ERROR"></span><span id="mregister_e_device_authorization_error"></span>**MRegister \_ E \_ Geräte \_ Autorisierungs \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-122"><span id="MREGISTER_E_DEVICE_AUTHORIZATION_ERROR"></span><span id="mregister_e_device_authorization_error"></span>**MREGISTER\_E\_DEVICE\_AUTHORIZATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-123">0x80190003</span><span class="sxs-lookup"><span data-stu-id="2cc1e-123">0x80190003</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-124">Der Benutzer ist nicht autorisiert, sich anzumelden.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-124">The user is not authorized to enroll.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-125"><span id="MENROLL_E_DEVICE_AUTHORIZATION_ERROR"></span><span id="menroll_e_device_authorization_error"></span>**menroll \_ E \_ Geräte \_ Autorisierungs \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-125"><span id="MENROLL_E_DEVICE_AUTHORIZATION_ERROR"></span><span id="menroll_e_device_authorization_error"></span>**MENROLL\_E\_DEVICE\_AUTHORIZATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-126">0x80180003</span><span class="sxs-lookup"><span data-stu-id="2cc1e-126">0x80180003</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-127">Der Benutzer ist nicht autorisiert, sich anzumelden.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-127">The user is not authorized to enroll.</span></span>

<span data-ttu-id="2cc1e-128">**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-128">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-129"><span id="MREGISTER_E_DEVICE_CERTIFCATEREQUEST_ERROR"></span><span id="mregister_e_device_certifcaterequest_error"></span>**MRegister \_ E \_ Gerät \_ certifcaterequest- \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-129"><span id="MREGISTER_E_DEVICE_CERTIFCATEREQUEST_ERROR"></span><span id="mregister_e_device_certifcaterequest_error"></span>**MREGISTER\_E\_DEVICE\_CERTIFCATEREQUEST\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-130">0x80190004</span><span class="sxs-lookup"><span data-stu-id="2cc1e-130">0x80190004</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-131">Der Benutzer hat keine Berechtigung für die Zertifikat Vorlage, oder die Zertifizierungsstelle ist nicht erreichbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-131">The user has no permission for the certificate template or the certificate authority is unreachable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-132"><span id="MENROLL_E_DEVICE_CERTIFCATEREQUEST_ERROR"></span><span id="menroll_e_device_certifcaterequest_error"></span>**"menroll \_ E" \_ \_ certifcaterequest- \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-132"><span id="MENROLL_E_DEVICE_CERTIFCATEREQUEST_ERROR"></span><span id="menroll_e_device_certifcaterequest_error"></span>**MENROLL\_E\_DEVICE\_CERTIFCATEREQUEST\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-133">0x80180004</span><span class="sxs-lookup"><span data-stu-id="2cc1e-133">0x80180004</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-134">Der Benutzer hat keine Berechtigung für die Zertifikat Vorlage, oder die Zertifizierungsstelle ist nicht erreichbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-134">The user has no permission for the certificate template or the certificate authority is unreachable.</span></span>

<span data-ttu-id="2cc1e-135">**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-135">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-136"><span id="MREGISTER_E_DEVICE_CONFIGMGRSERVER_ERROR"></span><span id="mregister_e_device_configmgrserver_error"></span>**MRegister \_ E \_ Gerät \_ configmgrserver \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-136"><span id="MREGISTER_E_DEVICE_CONFIGMGRSERVER_ERROR"></span><span id="mregister_e_device_configmgrserver_error"></span>**MREGISTER\_E\_DEVICE\_CONFIGMGRSERVER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-137">0x80190005</span><span class="sxs-lookup"><span data-stu-id="2cc1e-137">0x80190005</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-138">Beim Management Server ist ein Fehler aufgetreten, z. b. ein Datenbankzugriffs Fehler.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-138">There was a failure at the management server, such as a database access error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-139"><span id="MENROLL_E_DEVICE_CONFIGMGRSERVER_ERROR"></span><span id="menroll_e_device_configmgrserver_error"></span>**\_ \_ \_ configmgrserver-Fehler bei "menroll E" \_**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-139"><span id="MENROLL_E_DEVICE_CONFIGMGRSERVER_ERROR"></span><span id="menroll_e_device_configmgrserver_error"></span>**MENROLL\_E\_DEVICE\_CONFIGMGRSERVER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-140">0x80180005</span><span class="sxs-lookup"><span data-stu-id="2cc1e-140">0x80180005</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-141">Beim Management Server ist ein Fehler aufgetreten, z. b. ein Datenbankzugriffs Fehler.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-141">There was a failure at the management server, such as a database access error.</span></span>

<span data-ttu-id="2cc1e-142">**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-142">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-143"><span id="MREGISTER_E_DEVICE_INTERNALSERVICE_ERROR"></span><span id="mregister_e_device_internalservice_error"></span>**Fehler im \_ \_ \_ internalservice für MRegister E-Geräte \_**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-143"><span id="MREGISTER_E_DEVICE_INTERNALSERVICE_ERROR"></span><span id="mregister_e_device_internalservice_error"></span>**MREGISTER\_E\_DEVICE\_INTERNALSERVICE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-144">0x80190006</span><span class="sxs-lookup"><span data-stu-id="2cc1e-144">0x80190006</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-145">Auf dem Server ist eine nicht behandelte Ausnahme aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-145">There was an unhandled exception on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-146"><span id="MENROLL_E_DEVICE_INTERNALSERVICE_ERROR"></span><span id="menroll_e_device_internalservice_error"></span>**Fehler bei "menroll \_ E" \_ \_ internalservice \_**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-146"><span id="MENROLL_E_DEVICE_INTERNALSERVICE_ERROR"></span><span id="menroll_e_device_internalservice_error"></span>**MENROLL\_E\_DEVICE\_INTERNALSERVICE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-147">0x80180006</span><span class="sxs-lookup"><span data-stu-id="2cc1e-147">0x80180006</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-148">Auf dem Server ist eine nicht behandelte Ausnahme aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-148">There was an unhandled exception on the server.</span></span>

<span data-ttu-id="2cc1e-149">**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-149">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-150"><span id="MREGISTER_E_DEVICE_INVALIDSECURITY_ERROR"></span><span id="mregister_e_device_invalidsecurity_error"></span>**MRegister \_ E \_ Geräte \_ invalidsecurity- \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-150"><span id="MREGISTER_E_DEVICE_INVALIDSECURITY_ERROR"></span><span id="mregister_e_device_invalidsecurity_error"></span>**MREGISTER\_E\_DEVICE\_INVALIDSECURITY\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-151">0x80190007</span><span class="sxs-lookup"><span data-stu-id="2cc1e-151">0x80190007</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-152">Auf dem Server ist eine nicht behandelte Ausnahme aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-152">There was an unhandled exception on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-153"><span id="MENROLL_E_DEVICE_INVALIDSECURITY_ERROR"></span><span id="menroll_e_device_invalidsecurity_error"></span>**Fehler bei "menroll \_ E \_ Device \_ invalidsecurity" \_**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-153"><span id="MENROLL_E_DEVICE_INVALIDSECURITY_ERROR"></span><span id="menroll_e_device_invalidsecurity_error"></span>**MENROLL\_E\_DEVICE\_INVALIDSECURITY\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-154">0x80180007</span><span class="sxs-lookup"><span data-stu-id="2cc1e-154">0x80180007</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-155">Auf dem Server ist eine nicht behandelte Ausnahme aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-155">There was an unhandled exception on the server.</span></span>

<span data-ttu-id="2cc1e-156">**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-156">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-157"><span id="MREGISTER_E_DEVICE_UNKNOWN_ERROR"></span><span id="mregister_e_device_unknown_error"></span>**\_ \_ \_ unbekannter \_ Fehler bei MRegister E-Gerät**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-157"><span id="MREGISTER_E_DEVICE_UNKNOWN_ERROR"></span><span id="mregister_e_device_unknown_error"></span>**MREGISTER\_E\_DEVICE\_UNKNOWN\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-158">0x80190008</span><span class="sxs-lookup"><span data-stu-id="2cc1e-158">0x80190008</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-159">Unbekannter Server Fehler.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-159">Unknown server error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-160"><span id="MENROLL_E_DEVICE_UNKNOWN_ERROR"></span><span id="menroll_e_device_unknown_error"></span>**\_ \_ \_ unbekannter \_ Fehler bei "menroll E".**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-160"><span id="MENROLL_E_DEVICE_UNKNOWN_ERROR"></span><span id="menroll_e_device_unknown_error"></span>**MENROLL\_E\_DEVICE\_UNKNOWN\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-161">0x80180008</span><span class="sxs-lookup"><span data-stu-id="2cc1e-161">0x80180008</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-162">Unbekannter Server Fehler.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-162">Unknown server error.</span></span>

<span data-ttu-id="2cc1e-163">**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-163">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-164"><span id="MREGISTER_E_REGISTRATION_IN_PROGRESS"></span><span id="mregister_e_registration_in_progress"></span>**MRegister \_ E \_ Registrierung \_ wird \_ ausgeführt**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-164"><span id="MREGISTER_E_REGISTRATION_IN_PROGRESS"></span><span id="mregister_e_registration_in_progress"></span>**MREGISTER\_E\_REGISTRATION\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-165">0x80190009</span><span class="sxs-lookup"><span data-stu-id="2cc1e-165">0x80190009</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-166">Zurzeit wird ein weiterer Registrierungsvorgang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-166">Another enrollment operation is currently underway.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-167"><span id="MENROLL_E_ENROLLMENT_IN_PROGRESS"></span><span id="menroll_e_enrollment_in_progress"></span>**die Registrierung für die Registrierung wird durchgeführt. \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-167"><span id="MENROLL_E_ENROLLMENT_IN_PROGRESS"></span><span id="menroll_e_enrollment_in_progress"></span>**MENROLL\_E\_ENROLLMENT\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-168">0x80180009</span><span class="sxs-lookup"><span data-stu-id="2cc1e-168">0x80180009</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-169">Zurzeit wird ein weiterer Registrierungsvorgang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-169">Another enrollment operation is currently underway.</span></span>

<span data-ttu-id="2cc1e-170">**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-170">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-171"><span id="MREGISTER_E_DEVICE_ALREADY_REGISTERED"></span><span id="mregister_e_device_already_registered"></span>**MRegister \_ E \_ Gerät \_ bereits \_ registriert**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-171"><span id="MREGISTER_E_DEVICE_ALREADY_REGISTERED"></span><span id="mregister_e_device_already_registered"></span>**MREGISTER\_E\_DEVICE\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-172">0x8019000a</span><span class="sxs-lookup"><span data-stu-id="2cc1e-172">0x8019000A</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-173">Nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-173">No longer used.</span></span>

<span data-ttu-id="2cc1e-174">**Windows 8.1:** Das Gerät ist bereits registriert.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-174">**Windows 8.1:** The device is already enrolled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-175"><span id="MENROLL_E_DEVICE_ALREADY_ENROLLED"></span><span id="menroll_e_device_already_enrolled"></span>**Das \_ Gerät ist \_ \_ bereits \_ registriert.**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-175"><span id="MENROLL_E_DEVICE_ALREADY_ENROLLED"></span><span id="menroll_e_device_already_enrolled"></span>**MENROLL\_E\_DEVICE\_ALREADY\_ENROLLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-176">0x8018000a</span><span class="sxs-lookup"><span data-stu-id="2cc1e-176">0x8018000A</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-177">Das Gerät ist bereits registriert.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-177">The device is already enrolled.</span></span>

<span data-ttu-id="2cc1e-178">**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-178">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-179"><span id="MREGISTER_E_DEVICE_NOT_REGISTERED"></span><span id="mregister_e_device_not_registered"></span>**MRegister \_ E \_ Gerät \_ nicht \_ registriert**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-179"><span id="MREGISTER_E_DEVICE_NOT_REGISTERED"></span><span id="mregister_e_device_not_registered"></span>**MREGISTER\_E\_DEVICE\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-180">0x8019000b</span><span class="sxs-lookup"><span data-stu-id="2cc1e-180">0x8019000B</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-181">Nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-181">No longer used.</span></span>

<span data-ttu-id="2cc1e-182">**Windows 8.1:** Das Gerät ist nicht registriert.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-182">**Windows 8.1:** The device is not enrolled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-183"><span id="MENROLL_E_DEVICE_NOT_ENROLLED"></span><span id="menroll_e_device_not_enrolled"></span>**menroll \_ E \_ Gerät \_ nicht \_ registriert**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-183"><span id="MENROLL_E_DEVICE_NOT_ENROLLED"></span><span id="menroll_e_device_not_enrolled"></span>**MENROLL\_E\_DEVICE\_NOT\_ENROLLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-184">0x8018000b</span><span class="sxs-lookup"><span data-stu-id="2cc1e-184">0x8018000B</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-185">Das Gerät ist nicht registriert.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-185">The device is not enrolled.</span></span>

<span data-ttu-id="2cc1e-186">**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-186">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-187"><span id="MREGISTER_E_DISCOVERY_REDIRECTED"></span><span id="mregister_e_discovery_redirected"></span>**MRegister \_ E-Ermittlung \_ \_ umgeleitet**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-187"><span id="MREGISTER_E_DISCOVERY_REDIRECTED"></span><span id="mregister_e_discovery_redirected"></span>**MREGISTER\_E\_DISCOVERY\_REDIRECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-188">0x8019000c</span><span class="sxs-lookup"><span data-stu-id="2cc1e-188">0x8019000C</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-189">Nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-189">No longer used.</span></span>

<span data-ttu-id="2cc1e-190">**Windows 8.1:** Die Umleitung ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-190">**Windows 8.1:** Redirection is needed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-191"><span id="MREGISTER_E_DEVICE_NOT_AD_REGISTERED_ERROR"></span><span id="mregister_e_device_not_ad_registered_error"></span>**Fehler beim Registrieren des Registrierungs \_ \_ Geräts E \_ nicht \_ AD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-191"><span id="MREGISTER_E_DEVICE_NOT_AD_REGISTERED_ERROR"></span><span id="mregister_e_device_not_ad_registered_error"></span>**MREGISTER\_E\_DEVICE\_NOT\_AD\_REGISTERED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-192">0x8019000d</span><span class="sxs-lookup"><span data-stu-id="2cc1e-192">0x8019000D</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-193">Nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-193">No longer used.</span></span>

<span data-ttu-id="2cc1e-194">**Windows 8.1:** Das Gerät ist nicht bei Active Directory registriert.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-194">**Windows 8.1:** The device is not registered with Active Directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-195"><span id="MENROLL_E_DISCOVERY_SEC_CERT_DATE_INVALID"></span><span id="menroll_e_discovery_sec_cert_date_invalid"></span>**"menroll \_ E \_ Discovery sec"- \_ Zertifikat ist \_ \_ \_ ungültig.**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-195"><span id="MENROLL_E_DISCOVERY_SEC_CERT_DATE_INVALID"></span><span id="menroll_e_discovery_sec_cert_date_invalid"></span>**MENROLL\_E\_DISCOVERY\_SEC\_CERT\_DATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-196">0x8018000d</span><span class="sxs-lookup"><span data-stu-id="2cc1e-196">0x8018000D</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-197">Während der Ermittlung war das Datum des Zertifikats "Sek." ungültig.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-197">During discovery the sec cert date was invalid.</span></span>

<span data-ttu-id="2cc1e-198">**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-198">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-199"><span id="MREGISTER_E_DISCOVERY_FAILED"></span><span id="mregister_e_discovery_failed"></span>**MRegister-E-Ermittlung \_ \_ \_ fehlgeschlagen**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-199"><span id="MREGISTER_E_DISCOVERY_FAILED"></span><span id="mregister_e_discovery_failed"></span>**MREGISTER\_E\_DISCOVERY\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-200">0x8019000e</span><span class="sxs-lookup"><span data-stu-id="2cc1e-200">0x8019000E</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-201">Nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-201">No longer used.</span></span>

<span data-ttu-id="2cc1e-202">**Windows 8.1:** Fehler bei der Ermittlung. die Umleitung ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-202">**Windows 8.1:** Discovery failed; redirection is needed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-203"><span id="MENROLL_E_PASSWORD_NEEDED"></span><span id="menroll_e_password_needed"></span>**\_ \_ Kennwort für Kennwort \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-203"><span id="MENROLL_E_PASSWORD_NEEDED"></span><span id="menroll_e_password_needed"></span>**MENROLL\_E\_PASSWORD\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-204">0x8018000e</span><span class="sxs-lookup"><span data-stu-id="2cc1e-204">0x8018000E</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-205">Ein Kennwort ist erforderlich, wurde jedoch nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-205">A password is needed, but was not supplied.</span></span>

<span data-ttu-id="2cc1e-206">**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-206">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-207"><span id="MENROLL_E_WAB_ERROR"></span><span id="menroll_e_wab_error"></span>**Fehler "menroll \_ E \_ WAB" \_**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-207"><span id="MENROLL_E_WAB_ERROR"></span><span id="menroll_e_wab_error"></span>**MENROLL\_E\_WAB\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-208">0x8018000f</span><span class="sxs-lookup"><span data-stu-id="2cc1e-208">0x8018000F</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-209">Fehler bei der WAB-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-209">An error occurred during WAB enrollment.</span></span>

<span data-ttu-id="2cc1e-210">**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-210">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-211"><span id="MENROLL_E_CONNECTIVITY"></span><span id="menroll_e_connectivity"></span>**menroll \_ E \_ Konnektivität**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-211"><span id="MENROLL_E_CONNECTIVITY"></span><span id="menroll_e_connectivity"></span>**MENROLL\_E\_CONNECTIVITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-212">0x80180010</span><span class="sxs-lookup"><span data-stu-id="2cc1e-212">0x80180010</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-213">Ein Netzwerkfehler ist aufgetreten, z. b. DNS oder ein Netzwerk Timeout.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-213">A network error occurred, such as DNS or a network timeout.</span></span>

<span data-ttu-id="2cc1e-214">**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-214">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-215"><span id="MENROLL_S_ENROLLMENT_SUSPENDED"></span><span id="menroll_s_enrollment_suspended"></span>**die Registrierung der \_ menrolls wurde \_ \_ unterbrochen.**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-215"><span id="MENROLL_S_ENROLLMENT_SUSPENDED"></span><span id="menroll_s_enrollment_suspended"></span>**MENROLL\_S\_ENROLLMENT\_SUSPENDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-216">0x00180011</span><span class="sxs-lookup"><span data-stu-id="2cc1e-216">0x00180011</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-217">Die Registrierung wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-217">Enrollment was suspended.</span></span> <span data-ttu-id="2cc1e-218">Wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-218">No longer supported.</span></span>

<span data-ttu-id="2cc1e-219">**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-219">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-220"><span id="MENROLL_E_INVALIDSSLCERT"></span><span id="menroll_e_invalidsslcert"></span>**menroll \_ E \_ invalidsslcert**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-220"><span id="MENROLL_E_INVALIDSSLCERT"></span><span id="menroll_e_invalidsslcert"></span>**MENROLL\_E\_INVALIDSSLCERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-221">0x80180012</span><span class="sxs-lookup"><span data-stu-id="2cc1e-221">0x80180012</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-222">Das SSL-Zertifikat war ungültig.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-222">The SSL cert was not valid.</span></span>

<span data-ttu-id="2cc1e-223">**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-223">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-224"><span id="MENROLL_E_DEVICECAPREACHED"></span><span id="menroll_e_devicecapreached"></span>**menroll E Geräte-App-Limit \_ \_ erreicht**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-224"><span id="MENROLL_E_DEVICECAPREACHED"></span><span id="menroll_e_devicecapreached"></span>**MENROLL\_E\_DEVICECAPREACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-225">0x80180013</span><span class="sxs-lookup"><span data-stu-id="2cc1e-225">0x80180013</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-226">Der Benutzer hat bereits zu viele Geräte registriert.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-226">The user has already enrolled too many devices.</span></span> <span data-ttu-id="2cc1e-227">Löschen Sie alte, oder heben Sie die Registrierung auf, um diesen Fehler zu beheben</span><span class="sxs-lookup"><span data-stu-id="2cc1e-227">Delete or unenroll old ones to fix this error.</span></span> <span data-ttu-id="2cc1e-228">Beachten Sie, dass der Benutzer diesen Fehler ohne Administrator Unterstützung beheben kann.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-228">Note that the user can resolve this error without admin assistance.</span></span>

<span data-ttu-id="2cc1e-229">**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-229">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-230"><span id="MENROLL_E_DEVICENOTSUPPORTED"></span><span id="menroll_e_devicenotsupported"></span>**menroll \_ E \_ devicenotsupported**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-230"><span id="MENROLL_E_DEVICENOTSUPPORTED"></span><span id="menroll_e_devicenotsupported"></span>**MENROLL\_E\_DEVICENOTSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-231">Nummer 0x80180014</span><span class="sxs-lookup"><span data-stu-id="2cc1e-231">0x80180014</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-232">Eine bestimmte Plattform (z. b. Windows) oder die Version wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-232">A specific platform (e.g. Windows) or version is not supported.</span></span> <span data-ttu-id="2cc1e-233">Die allgemeine Behebung dieses Fehlers besteht darin, das Gerät zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-233">The general fix for this error is to upgrade the device.</span></span>

<span data-ttu-id="2cc1e-234">**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-234">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-235"><span id="MENROLL_E_NOTSUPPORTED"></span><span id="menroll_e_notsupported"></span>**menroll \_ E \_ NotSupported**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-235"><span id="MENROLL_E_NOTSUPPORTED"></span><span id="menroll_e_notsupported"></span>**MENROLL\_E\_NOTSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-236">0x80180015</span><span class="sxs-lookup"><span data-stu-id="2cc1e-236">0x80180015</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-237">Die Verwaltung mobiler Geräte wird für dieses Gerät in der Regel nicht unterstützt. der Benutzer kann den Administrator anrufen, aber es ist unwahrscheinlich, dass dieses Problem behoben wird.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-237">Mobile device management is generally not supported for this device - the user may call the admin, but will be unlikely to resolve this issue.</span></span>

<span data-ttu-id="2cc1e-238">**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-238">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-239"><span id="MREGISTER_E_NOTELIGIBLETORENEW"></span><span id="mregister_e_noteligibletorenew"></span>**MRegister \_ E \_ noteligibletor**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-239"><span id="MREGISTER_E_NOTELIGIBLETORENEW"></span><span id="mregister_e_noteligibletorenew"></span>**MREGISTER\_E\_NOTELIGIBLETORENEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-240">0x80180016</span><span class="sxs-lookup"><span data-stu-id="2cc1e-240">0x80180016</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-241">Das Gerät versucht, eine Erneuerung durchzusetzen, aber der Server hat die Anforderung abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-241">The device is attempting to renew, but the server rejected the request.</span></span> <span data-ttu-id="2cc1e-242">Prüfen Sie die Uhrzeit auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-242">Check time on device.</span></span> <span data-ttu-id="2cc1e-243">Der Benutzer kann diesen Fehler ggf. beheben, indem er sich erneut anmelden.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-243">The user may be able to resolve this error by re-enrolling.</span></span>

<span data-ttu-id="2cc1e-244">**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-244">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-245"><span id="MENROLL_E_INMAINTENANCE"></span><span id="menroll_e_inmaintenance"></span>**menroll \_ E \_ inmaintenance**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-245"><span id="MENROLL_E_INMAINTENANCE"></span><span id="menroll_e_inmaintenance"></span>**MENROLL\_E\_INMAINTENANCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-246">0x80180017</span><span class="sxs-lookup"><span data-stu-id="2cc1e-246">0x80180017</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-247">Das Konto befindet sich im Wartungsmodus. versuchen Sie es später erneut.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-247">Account is in maintenance; retry later.</span></span> <span data-ttu-id="2cc1e-248">Der Benutzer kann den Vorgang später wiederholen.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-248">The user can retry later.</span></span> <span data-ttu-id="2cc1e-249">Der Benutzer kann jedoch den Administrator anrufen, um den Wartungs Zeitplan zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-249">However, the user may choose to call the admin to determine the maintenance schedule.</span></span>

<span data-ttu-id="2cc1e-250">**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-250">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-251"><span id="MENROLL_E_USERLICENSE"></span><span id="menroll_e_userlicense"></span>**menroll \_ E \_ userlicense**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-251"><span id="MENROLL_E_USERLICENSE"></span><span id="menroll_e_userlicense"></span>**MENROLL\_E\_USERLICENSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-252">0x80180018</span><span class="sxs-lookup"><span data-stu-id="2cc1e-252">0x80180018</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-253">Die Lizenz des Benutzers befindet sich in einem ungültigen Zustand, der die Registrierung blockiert. der Benutzer muss den Administrator anrufen.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-253">The license of user is in bad state blocking enrollment; the user will need to call the admin.</span></span>

<span data-ttu-id="2cc1e-254">**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-254">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-255"><span id="MENROLL_E_ENROLLMENTDATAINVALID"></span><span id="menroll_e_enrollmentdatainvalid"></span>**menroll \_ E \_ anmelmentdatainvalid**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-255"><span id="MENROLL_E_ENROLLMENTDATAINVALID"></span><span id="menroll_e_enrollmentdatainvalid"></span>**MENROLL\_E\_ENROLLMENTDATAINVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-256">0x80180019</span><span class="sxs-lookup"><span data-stu-id="2cc1e-256">0x80180019</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-257">Der Server hat die Registrierungsdaten abgelehnt. der Server ist möglicherweise nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-257">The server rejected the Enrollment Data; the server may not be configured correctly.</span></span>

<span data-ttu-id="2cc1e-258">**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-258">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-259"><span id="MENROLL_E_INSECUREREDIRECT"></span><span id="menroll_e_insecureredirect"></span>**menroll \_ E \_ insecureredirect**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-259"><span id="MENROLL_E_INSECUREREDIRECT"></span><span id="menroll_e_insecureredirect"></span>**MENROLL\_E\_INSECUREREDIRECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-260">0x8018001a</span><span class="sxs-lookup"><span data-stu-id="2cc1e-260">0x8018001A</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-261">Der Server hat http anstelle von HTTPS angefordert, aber es wurde nicht akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-261">The server requested HTTP rather than HTTPS but it was not accepted.</span></span>

<span data-ttu-id="2cc1e-262">**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-262">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-263"><span id="MENROLL_E_PLATFORM_WRONG_STATE"></span><span id="menroll_e_platform_wrong_state"></span>**\_ \_ \_ falscher Status der unplattform \_**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-263"><span id="MENROLL_E_PLATFORM_WRONG_STATE"></span><span id="menroll_e_platform_wrong_state"></span>**MENROLL\_E\_PLATFORM\_WRONG\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-264">0x8018001b</span><span class="sxs-lookup"><span data-stu-id="2cc1e-264">0x8018001B</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-265">Es wurde versucht, das gleiche Gerät zweimal zu registrieren oder die Registrierung eines unbekannten Geräts aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-265">An invalid operation was attempted, such trying to enroll the same device twice or unenroll an unknown device.</span></span>

<span data-ttu-id="2cc1e-266">**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-266">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-267"><span id="MENROLL_E_PLATFORM_LICENSE_ERROR"></span><span id="menroll_e_platform_license_error"></span>**Fehler bei der menrollout \_ E \_ Platform- \_ Lizenz \_**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-267"><span id="MENROLL_E_PLATFORM_LICENSE_ERROR"></span><span id="menroll_e_platform_license_error"></span>**MENROLL\_E\_PLATFORM\_LICENSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-268">0x8018001c</span><span class="sxs-lookup"><span data-stu-id="2cc1e-268">0x8018001C</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-269">Dieser registriungstyp wird von der auf dem Client installierten Windows-Version nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-269">The version of Windows installed on the client does not support this enrollment type.</span></span>

<span data-ttu-id="2cc1e-270">**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-270">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-271"><span id="MENROLL_E_PLATFORM_UNKNOWN_ERROR"></span><span id="menroll_e_platform_unknown_error"></span>**Unbekannter Fehler bei "menroll \_ E \_ Platform" \_ . \_**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-271"><span id="MENROLL_E_PLATFORM_UNKNOWN_ERROR"></span><span id="menroll_e_platform_unknown_error"></span>**MENROLL\_E\_PLATFORM\_UNKNOWN\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-272">0x8018001d</span><span class="sxs-lookup"><span data-stu-id="2cc1e-272">0x8018001D</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-273">Auf dem Client ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-273">An unknown error occurred on the client.</span></span>

<span data-ttu-id="2cc1e-274">**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-274">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-275"><span id="MENROLL_E_PROV_CSP_CERTSTORE"></span><span id="menroll_e_prov_csp_certstore"></span>**menroll \_ E \_ Prov \_ CSP \_ certstore**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-275"><span id="MENROLL_E_PROV_CSP_CERTSTORE"></span><span id="menroll_e_prov_csp_certstore"></span>**MENROLL\_E\_PROV\_CSP\_CERTSTORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-276">0x8018001e</span><span class="sxs-lookup"><span data-stu-id="2cc1e-276">0x8018001E</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-277">Fehler bei der Bereitstellung im Zertifikat Speicher-CSP.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-277">Provisioning failed in the certificate store CSP.</span></span>

<span data-ttu-id="2cc1e-278">**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-278">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-279"><span id="MENROLL_E_PROV_CSP_W7"></span><span id="menroll_e_prov_csp_w7"></span>**Menroll \_ E \_ Prov \_ CSP \_ W7**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-279"><span id="MENROLL_E_PROV_CSP_W7"></span><span id="menroll_e_prov_csp_w7"></span>**MENROLL\_E\_PROV\_CSP\_W7**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-280">0x8018001f</span><span class="sxs-lookup"><span data-stu-id="2cc1e-280">0x8018001F</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-281">Fehler bei der Bereitstellung in einem W7/dmacc-cpp.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-281">Provisioning failed in a W7/DMAcc CPP.</span></span>

<span data-ttu-id="2cc1e-282">**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-282">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-283"><span id="MENROLL_E_PROV_CSP_DMCLIENT"></span><span id="menroll_e_prov_csp_dmclient"></span>**ENROLL \_ E \_ Prov \_ CSP \_ dmclient**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-283"><span id="MENROLL_E_PROV_CSP_DMCLIENT"></span><span id="menroll_e_prov_csp_dmclient"></span>**MENROLL\_E\_PROV\_CSP\_DMCLIENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-284">0x80180020</span><span class="sxs-lookup"><span data-stu-id="2cc1e-284">0x80180020</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-285">Fehler bei der Bereitstellung in einem DM-Client-CSP.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-285">Provisioning failed in a DM client CSP.</span></span>

<span data-ttu-id="2cc1e-286">**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-286">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-287"><span id="MENROLL_E_PROV_CSP_PFW"></span><span id="menroll_e_prov_csp_pfw"></span>**menroll \_ E \_ Prov \_ CSP \_ PFW**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-287"><span id="MENROLL_E_PROV_CSP_PFW"></span><span id="menroll_e_prov_csp_pfw"></span>**MENROLL\_E\_PROV\_CSP\_PFW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-288">0x80180021</span><span class="sxs-lookup"><span data-stu-id="2cc1e-288">0x80180021</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-289">Fehler bei der Bereitstellung in einem Passport for Work-CSP.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-289">Provisioning failed in a Passport for Work CSP.</span></span>

<span data-ttu-id="2cc1e-290">**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-290">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-291"><span id="MENROLL_E_PROV_CSP_MISC"></span><span id="menroll_e_prov_csp_misc"></span>**menroll \_ E \_ Prov \_ CSP \_ misc**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-291"><span id="MENROLL_E_PROV_CSP_MISC"></span><span id="menroll_e_prov_csp_misc"></span>**MENROLL\_E\_PROV\_CSP\_MISC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-292">0x80180022</span><span class="sxs-lookup"><span data-stu-id="2cc1e-292">0x80180022</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-293">Fehler bei der Bereitstellung in einem CSP, der oben nicht aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-293">Provisioning failed in a CSP not listed above.</span></span>

<span data-ttu-id="2cc1e-294">**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-294">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-295"><span id="MENROLL_E_PROV_UNKNOWN"></span><span id="menroll_e_prov_unknown"></span>**\_ \_ unbekannte E Prov- \_ Datei**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-295"><span id="MENROLL_E_PROV_UNKNOWN"></span><span id="menroll_e_prov_unknown"></span>**MENROLL\_E\_PROV\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-296">0x80180023</span><span class="sxs-lookup"><span data-stu-id="2cc1e-296">0x80180023</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-297">Fehler bei der Bereitstellung, aber es ist kein bestimmter CSP angegeben.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-297">Provisioning failed, but a specific CSP is not indicated.</span></span>

<span data-ttu-id="2cc1e-298">**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-298">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-299"><span id="MENROLL_E_PROV_SSLCERTNOTFOUND"></span><span id="menroll_e_prov_sslcertnotfound"></span>**menroll \_ E \_ Prov \_ sslcertnotfound**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-299"><span id="MENROLL_E_PROV_SSLCERTNOTFOUND"></span><span id="menroll_e_prov_sslcertnotfound"></span>**MENROLL\_E\_PROV\_SSLCERTNOTFOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-300">0x80180024</span><span class="sxs-lookup"><span data-stu-id="2cc1e-300">0x80180024</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-301">Beim Versuch, den öffentlichen Zertifikat/privaten Schlüssel zu binden, wurde das öffentliche Zertifikat entweder nicht gefunden: beim Versuch, den öffentlichen Zertifikat/privaten Schlüssel zu binden, oder bei der Überprüfung der Nutzlast (möglicherweise auf den falschen Speicher).</span><span class="sxs-lookup"><span data-stu-id="2cc1e-301">When attempting to bind the public cert/private key, the public cert was not found either: when attempting to bind the public cert/private key, or when looking into provisioning payload (perhaps targeting the wrong store).</span></span>

<span data-ttu-id="2cc1e-302">**Windows 8.1:** Diese Konstante ist nicht vor Windows 10 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-302">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-303"><span id="MENROLL_E_PROV_CSP_APPMGMT"></span><span id="menroll_e_prov_csp_appmgmt"></span>**menroll \_ E \_ Prov \_ CSP \_ Appmgmt**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-303"><span id="MENROLL_E_PROV_CSP_APPMGMT"></span><span id="menroll_e_prov_csp_appmgmt"></span>**MENROLL\_E\_PROV\_CSP\_APPMGMT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-304">0x80180025</span><span class="sxs-lookup"><span data-stu-id="2cc1e-304">0x80180025</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-305">Fehler bei der Bereitstellung im enterpritsappmanagement-CSP.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-305">Provisioning failed in the EnterpriseAppManagement CSP.</span></span>

> [!Note]  
> <span data-ttu-id="2cc1e-306">Diese Konstante ist vor Windows 10, Version 1709, nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-306">This constant is not available before Windows 10, version 1709.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-307"><span id="MENROLL_E_DEVICE_MANAGEMENT_BLOCKED"></span><span id="menroll_e_device_management_blocked"></span>**die \_ \_ Geräteverwaltung wurde \_ \_ gesperrt.**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-307"><span id="MENROLL_E_DEVICE_MANAGEMENT_BLOCKED"></span><span id="menroll_e_device_management_blocked"></span>**MENROLL\_E\_DEVICE\_MANAGEMENT\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-308">0x80180026</span><span class="sxs-lookup"><span data-stu-id="2cc1e-308">0x80180026</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-309">Die Verwaltung mobiler Geräte (Mobile Device Management, MDM) wurde blockiert, möglicherweise durch Gruppenrichtlinie oder die Funktion [**setmanagedexternally**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-setmanagedexternally) .</span><span class="sxs-lookup"><span data-stu-id="2cc1e-309">Mobile Device Management (MDM) was blocked, possibly by Group Policy or the [**SetManagedExternally**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-setmanagedexternally) function.</span></span>

> [!Note]  
> <span data-ttu-id="2cc1e-310">Diese Konstante ist vor Windows 10, Version 1709, nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-310">This constant is not available before Windows 10, version 1709.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-311"><span id="MENROLL_E_CERTPOLICY_PRIVATEKEYCREATION_FAILED"></span><span id="menroll_e_certpolicy_privatekeycreation_failed"></span>**menroll \_ E \_ certpolicy \_ privatekeycreation \_ fehlgeschlagen**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-311"><span id="MENROLL_E_CERTPOLICY_PRIVATEKEYCREATION_FAILED"></span><span id="menroll_e_certpolicy_privatekeycreation_failed"></span>**MENROLL\_E\_CERTPOLICY\_PRIVATEKEYCREATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-312">0x80180027</span><span class="sxs-lookup"><span data-stu-id="2cc1e-312">0x80180027</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-313">Der private Schlüssel konnte nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-313">Failed to create the private key.</span></span>

> [!Note]  
> <span data-ttu-id="2cc1e-314">Diese Konstante ist vor Windows 10, Version 1709, nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-314">This constant is not available before Windows 10, version 1709.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-315"><span id="MENROLL_E_CERTAUTH_FAILED_TO_FIND_CERT"></span><span id="menroll_e_certauth_failed_to_find_cert"></span>**"menroll \_ E \_ certauth" konnte das \_ \_ \_ Zertifikat nicht finden \_ .**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-315"><span id="MENROLL_E_CERTAUTH_FAILED_TO_FIND_CERT"></span><span id="menroll_e_certauth_failed_to_find_cert"></span>**MENROLL\_E\_CERTAUTH\_FAILED\_TO\_FIND\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-316">0x80180028</span><span class="sxs-lookup"><span data-stu-id="2cc1e-316">0x80180028</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-317">Die Zertifikat Authentifizierung wurde angefordert, aber es wurde ein nicht verwendende Zertifikat gefunden.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-317">Certificate Authentication was requested, but failed find a certificate to use.</span></span>

> [!Note]  
> <span data-ttu-id="2cc1e-318">Diese Konstante ist vor Windows 10, Version 1709, nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-318">This constant is not available before Windows 10, version 1709.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-319"><span id="MENROLL_E_EMPTY_MESSAGE"></span><span id="menroll_e_empty_message"></span>**\_ \_ leere \_ Nachricht für "menroll"**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-319"><span id="MENROLL_E_EMPTY_MESSAGE"></span><span id="menroll_e_empty_message"></span>**MENROLL\_E\_EMPTY\_MESSAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-320">0x80180029</span><span class="sxs-lookup"><span data-stu-id="2cc1e-320">0x80180029</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-321">Der Server hat mit HTTP 200 geantwortet, aber die Nachricht war leer.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-321">The server responded with HTTP 200, but the message was empty.</span></span>

> [!Note]  
> <span data-ttu-id="2cc1e-322">Diese Konstante ist vor Windows 10, Version 1709, nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-322">This constant is not available before Windows 10, version 1709.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-323"><span id="MENROLL_E_USER_CANCELED_"></span><span id="menroll_e_user_canceled_"></span>**menroll \_ E \_ Benutzer \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-323"><span id="MENROLL_E_USER_CANCELED_"></span><span id="menroll_e_user_canceled_"></span>**MENROLL\_E\_USER\_CANCELED**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-324">0x80180030</span><span class="sxs-lookup"><span data-stu-id="2cc1e-324">0x80180030</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-325">Der Benutzer hat den Vorgang abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-325">The user canceled the operation.</span></span>

> [!Note]  
> <span data-ttu-id="2cc1e-326">Diese Konstante ist vor Windows 10, Version 1709, nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-326">This constant is not available before Windows 10, version 1709.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cc1e-327"><span id="MENROLL_E_MDM_NOT_CONFIGURED"></span><span id="menroll_e_mdm_not_configured"></span>**menroll \_ E \_ MDM \_ nicht \_ konfiguriert**</span><span class="sxs-lookup"><span data-stu-id="2cc1e-327"><span id="MENROLL_E_MDM_NOT_CONFIGURED"></span><span id="menroll_e_mdm_not_configured"></span>**MENROLL\_E\_MDM\_NOT\_CONFIGURED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc1e-328">0x80180031</span><span class="sxs-lookup"><span data-stu-id="2cc1e-328">0x80180031</span></span>
</dt> <dt>



<span data-ttu-id="2cc1e-329">Die Verwaltung mobiler Geräte (Mobile Device Management, MDM) ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-329">Mobile Device Management (MDM) is not configured.</span></span>

> [!Note]  
> <span data-ttu-id="2cc1e-330">Diese Konstante ist vor Windows 10, Version 1709, nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc1e-330">This constant is not available before Windows 10, version 1709.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2cc1e-331">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2cc1e-331">Requirements</span></span>



| <span data-ttu-id="2cc1e-332">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2cc1e-332">Requirement</span></span> | <span data-ttu-id="2cc1e-333">Wert</span><span class="sxs-lookup"><span data-stu-id="2cc1e-333">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cc1e-334">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2cc1e-334">Minimum supported client</span></span><br/> | <span data-ttu-id="2cc1e-335">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2cc1e-335">Windows 8.1</span></span><br/>                                                                       |
| <span data-ttu-id="2cc1e-336">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2cc1e-336">Minimum supported server</span></span><br/> | <span data-ttu-id="2cc1e-337">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2cc1e-337">None supported</span></span><br/>                                                                    |
| <span data-ttu-id="2cc1e-338">Header</span><span class="sxs-lookup"><span data-stu-id="2cc1e-338">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cc1e-339"><dt>Mdmregistration. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cc1e-339"><dt>MDMRegistration.h</dt></span></span> </dl> |



 

 





