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
# <a name="eap-related-error-and-information-constants"></a><span data-ttu-id="61262-103">EAP-bezogene Fehler-und Informations Konstanten</span><span class="sxs-lookup"><span data-stu-id="61262-103">EAP Related Error and Information Constants</span></span>

<span data-ttu-id="61262-104">Einzelne Gruppen von EAP-bezogenen Fehlern und Informations Konstanten, die allen EAPHost-API-Technologien gemeinsam sind.</span><span class="sxs-lookup"><span data-stu-id="61262-104">Individual groups of EAP related error and information constants common to all EAPHost API technologies.</span></span>

<dl> <dt>

<span data-ttu-id="61262-105"><span id="EAP_E_EAPHOST_FIRST"></span><span id="eap_e_eaphost_first"></span>**EAP \_ E \_ EAPHost \_ zuerst**</span><span class="sxs-lookup"><span data-stu-id="61262-105"><span id="EAP_E_EAPHOST_FIRST"></span><span id="eap_e_eaphost_first"></span>**EAP\_E\_EAPHOST\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-106">0x80420000l</span><span class="sxs-lookup"><span data-stu-id="61262-106">0x80420000L</span></span>
</dt> <dt>



<span data-ttu-id="61262-107">Definiert die Grenze von Fehlerberichten. Alle EAPHost-bezogenen Fehler treten zwischen **EAP \_ e \_ EAPHost \_ First** und **EAP \_ e \_ EAPHost \_ Last** auf.</span><span class="sxs-lookup"><span data-stu-id="61262-107">Defines the boundary of error reports; any EAPHost related error will occur between **EAP\_E\_EAPHOST\_FIRST** and **EAP\_E\_EAPHOST\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-108"><span id="EAP_E_EAPHOST_LAST___"></span><span id="eap_e_eaphost_last___"></span>**EAP \_ E \_ EAPHost \_ zuletzt**</span><span class="sxs-lookup"><span data-stu-id="61262-108"><span id="EAP_E_EAPHOST_LAST___"></span><span id="eap_e_eaphost_last___"></span>**EAP\_E\_EAPHOST\_LAST**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-109">0x804200ffl</span><span class="sxs-lookup"><span data-stu-id="61262-109">0x804200FFL</span></span>
</dt> <dt>



<span data-ttu-id="61262-110">Definiert die Grenze von Fehlerberichten. Alle EAPHost-bezogenen Fehler treten zwischen **EAP \_ e \_ EAPHost \_ First** und **EAP \_ e \_ EAPHost \_ Last** auf.</span><span class="sxs-lookup"><span data-stu-id="61262-110">Defines the boundary of error reports; any EAPHost related error will occur between **EAP\_E\_EAPHOST\_FIRST** and **EAP\_E\_EAPHOST\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-111"><span id="EAP_I_EAPHOST_FIRST_"></span><span id="eap_i_eaphost_first_"></span>**EAP \_ I \_ EAPHost \_ zuerst**</span><span class="sxs-lookup"><span data-stu-id="61262-111"><span id="EAP_I_EAPHOST_FIRST_"></span><span id="eap_i_eaphost_first_"></span>**EAP\_I\_EAPHOST\_FIRST**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-112">0x80420000l</span><span class="sxs-lookup"><span data-stu-id="61262-112">0x80420000L</span></span>
</dt> <dt>



<span data-ttu-id="61262-113">Definiert die Grenze von Informationsberichten. alle mit EAPHost verknüpften Informations Ereignisprotokollierung treten zwischen **EAP \_ i \_ EAPHost \_ First** und **EAP \_ i \_ EAPHost \_ Last** auf.</span><span class="sxs-lookup"><span data-stu-id="61262-113">Defines the boundary of information reports; any EAPHost related informational event logging will occur between **EAP\_I\_EAPHOST\_FIRST** and **EAP\_I\_EAPHOST\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-114"><span id="EAP_I_EAPHOST_LAST"></span><span id="eap_i_eaphost_last"></span>**EAP \_ I \_ EAPHost \_ Last**</span><span class="sxs-lookup"><span data-stu-id="61262-114"><span id="EAP_I_EAPHOST_LAST"></span><span id="eap_i_eaphost_last"></span>**EAP\_I\_EAPHOST\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-115">0x804200ffl</span><span class="sxs-lookup"><span data-stu-id="61262-115">0x804200FFL</span></span>
</dt> <dt>



<span data-ttu-id="61262-116">Definiert die Grenze von Informationsberichten. alle mit EAPHost verknüpften Informations Ereignisprotokollierung treten zwischen **EAP \_ i \_ EAPHost \_ First** und **EAP \_ i \_ EAPHost \_ Last** auf.</span><span class="sxs-lookup"><span data-stu-id="61262-116">Defines the boundary of information reports; any EAPHost related informational event logging will occur between **EAP\_I\_EAPHOST\_FIRST** and **EAP\_I\_EAPHOST\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-117"><span id="EAP_E_CERT_STORE_INACCESSIBLE"></span><span id="eap_e_cert_store_inaccessible"></span>**EAP \_ E- \_ Zertifikat \_ Speicher nicht \_ zugänglich**</span><span class="sxs-lookup"><span data-stu-id="61262-117"><span id="EAP_E_CERT_STORE_INACCESSIBLE"></span><span id="eap_e_cert_store_inaccessible"></span>**EAP\_E\_CERT\_STORE\_INACCESSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-118">0x80420011</span><span class="sxs-lookup"><span data-stu-id="61262-118">0x80420011</span></span>
</dt> <dt>



<span data-ttu-id="61262-119">Weder der Authentifikator noch der Peer können auf den Zertifikat Speicher zugreifen.</span><span class="sxs-lookup"><span data-stu-id="61262-119">Neither the authenticator or peer can access the certificate store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-120"><span id="EAP_E_EAPHOST_METHOD_NOT_INSTALLED"></span><span id="eap_e_eaphost_method_not_installed"></span>**EAP \_ E \_ EAPHost- \_ Methode \_ nicht \_ installiert**</span><span class="sxs-lookup"><span data-stu-id="61262-120"><span id="EAP_E_EAPHOST_METHOD_NOT_INSTALLED"></span><span id="eap_e_eaphost_method_not_installed"></span>**EAP\_E\_EAPHOST\_METHOD\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-121">0x80420011</span><span class="sxs-lookup"><span data-stu-id="61262-121">0x80420011</span></span>
</dt> <dt>



<span data-ttu-id="61262-122">Die angeforderte EAP-Methode ist nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="61262-122">The requested EAP method is not installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-123"><span id="EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET"></span><span id="eap_e_eaphost_thirdparty_method_host_reset"></span>**EAP \_ E \_ EAPHost \_ thirdparty- \_ Methoden \_ Host \_ Reset**</span><span class="sxs-lookup"><span data-stu-id="61262-123"><span id="EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET"></span><span id="eap_e_eaphost_thirdparty_method_host_reset"></span>**EAP\_E\_EAPHOST\_THIRDPARTY\_METHOD\_HOST\_RESET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-124">0x80420012</span><span class="sxs-lookup"><span data-stu-id="61262-124">0x80420012</span></span>
</dt> <dt>



<span data-ttu-id="61262-125">Der Host der Drittanbieter Methode antwortet nicht und wurde automatisch neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="61262-125">The host of the third party method is not responding and was restarted automatically.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-126"><span id="EAP_E_EAPHOST_EAPQEC_INACCESSIBLE"></span><span id="eap_e_eaphost_eapqec_inaccessible"></span>**EAP \_ E \_ EAPHost \_ eapqec nicht \_ zugänglich**</span><span class="sxs-lookup"><span data-stu-id="61262-126"><span id="EAP_E_EAPHOST_EAPQEC_INACCESSIBLE"></span><span id="eap_e_eaphost_eapqec_inaccessible"></span>**EAP\_E\_EAPHOST\_EAPQEC\_INACCESSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-127">0x80420013</span><span class="sxs-lookup"><span data-stu-id="61262-127">0x80420013</span></span>
</dt> <dt>



<span data-ttu-id="61262-128">EAPHost kann nicht mit dem EAP- [Quarantäne](/windows/desktop/NAP/nap-client-architecture) Erzwingungs Client (QEC) auf einem NAP-fähigen Client ( [Network Access Protection, Netzwerk Zugriffsschutz](/windows/desktop/NAP/network-access-protection-start-page) ) kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="61262-128">EAPHost not able to communicate with EAP [quarantine enforcement client](/windows/desktop/NAP/nap-client-architecture) (QEC) on a [Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page) (NAP) enabled client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-129"><span id="EAP_E_EAPHOST_IDENTITY_UNKNOWN"></span><span id="eap_e_eaphost_identity_unknown"></span>**EAP \_ E \_ EAPHost- \_ Identität \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="61262-129"><span id="EAP_E_EAPHOST_IDENTITY_UNKNOWN"></span><span id="eap_e_eaphost_identity_unknown"></span>**EAP\_E\_EAPHOST\_IDENTITY\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-130">0x80420014</span><span class="sxs-lookup"><span data-stu-id="61262-130">0x80420014</span></span>
</dt> <dt>



<span data-ttu-id="61262-131">EAPHost gibt diesen Fehler zurück, wenn der Authentifikator die Authentifizierung fehlschlägt, nachdem die Peer Identität übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="61262-131">EAPHost returns this error if the authenticator fails the authentication after the peer identity was submitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-132"><span id="EAP_E_AUTHENTICATION_FAILED"></span><span id="eap_e_authentication_failed"></span>**EAP \_ E- \_ Authentifizierung \_ fehlgeschlagen**</span><span class="sxs-lookup"><span data-stu-id="61262-132"><span id="EAP_E_AUTHENTICATION_FAILED"></span><span id="eap_e_authentication_failed"></span>**EAP\_E\_AUTHENTICATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-133">0x80420015</span><span class="sxs-lookup"><span data-stu-id="61262-133">0x80420015</span></span> 
</dt> <dt>



<span data-ttu-id="61262-134">EAPHost gibt diesen Fehler bei Authentifizierungs Fehlern zurück.</span><span class="sxs-lookup"><span data-stu-id="61262-134">EAPHost returns this error on authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-135"><span id="EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED"></span><span id="eap_i_eaphost_eap_negotiation_failed"></span>**EAP \_ I \_ EAPHost- \_ EAP- \_ Aushandlung \_ fehlgeschlagen**</span><span class="sxs-lookup"><span data-stu-id="61262-135"><span id="EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED"></span><span id="eap_i_eaphost_eap_negotiation_failed"></span>**EAP\_I\_EAPHOST\_EAP\_NEGOTIATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-136">0x40420016</span><span class="sxs-lookup"><span data-stu-id="61262-136">0x40420016</span></span>
</dt> <dt>



<span data-ttu-id="61262-137">EAPHost protokolliert dieses Informations Ereignis, wenn der Client und der Server nicht mit kompatiblen EAP-Typen konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="61262-137">EAPHost logs this information event when the client and server aren't configured with compatible EAP types.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-138"><span id="EAP_E_EAPHOST_METHOD_INVALID_PACKET"></span><span id="eap_e_eaphost_method_invalid_packet"></span>**EAP \_ E \_ EAPHost- \_ Methode \_ ungültiges \_ Paket**</span><span class="sxs-lookup"><span data-stu-id="61262-138"><span id="EAP_E_EAPHOST_METHOD_INVALID_PACKET"></span><span id="eap_e_eaphost_method_invalid_packet"></span>**EAP\_E\_EAPHOST\_METHOD\_INVALID\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-139">0x80420017</span><span class="sxs-lookup"><span data-stu-id="61262-139">0x80420017</span></span>
</dt> <dt>



<span data-ttu-id="61262-140">Eine EAP-Methode hat ein EAP-Paket empfangen, das nicht verarbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="61262-140">An EAP method received an EAP packet that cannot be processed.</span></span> <span data-ttu-id="61262-141">Ein anderer Name für die **EAP \_ E \_ EAPHost- \_ Methode " \_ ungültiges \_ Paket** " ist das **EAP- \_ \_ ungültige \_ Paket**.</span><span class="sxs-lookup"><span data-stu-id="61262-141">Another name for **EAP\_E\_EAPHOST\_METHOD\_INVALID\_PACKET** is **EAP\_METHOD\_INVALID\_PACKET**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-142"><span id="EAP_E_EAPHOST_REMOTE_INVALID_PACKET"></span><span id="eap_e_eaphost_remote_invalid_packet"></span>**EAP \_ E \_ EAPHost- \_ Remote \_ ungültiges \_ Paket**</span><span class="sxs-lookup"><span data-stu-id="61262-142"><span id="EAP_E_EAPHOST_REMOTE_INVALID_PACKET"></span><span id="eap_e_eaphost_remote_invalid_packet"></span>**EAP\_E\_EAPHOST\_REMOTE\_INVALID\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-143">0x80420018</span><span class="sxs-lookup"><span data-stu-id="61262-143">0x80420018</span></span>
</dt> <dt>



<span data-ttu-id="61262-144">EAPHost hat ein Paket empfangen, das nicht verarbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="61262-144">EAPHost received a packet that cannot be processed.</span></span> <span data-ttu-id="61262-145">Ein anderer Name für das **\_ \_ \_ Remote ungültige EAP \_ E \_ EAPHost-Paket** ist ein **Ungültiges EAP- \_ \_ Paket**.</span><span class="sxs-lookup"><span data-stu-id="61262-145">Another name for **EAP\_E\_EAPHOST\_REMOTE\_INVALID\_PACKET** is **EAP\_INVALID\_PACKET**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-146"><span id="EAP_E_EAPHOST_XML_MALFORMED_"></span><span id="eap_e_eaphost_xml_malformed_"></span>**EAP \_ E \_ EAPHost- \_ XML \_ falsch formatiert**</span><span class="sxs-lookup"><span data-stu-id="61262-146"><span id="EAP_E_EAPHOST_XML_MALFORMED_"></span><span id="eap_e_eaphost_xml_malformed_"></span>**EAP\_E\_EAPHOST\_XML\_MALFORMED**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-147">0x80420019</span><span class="sxs-lookup"><span data-stu-id="61262-147">0x80420019</span></span>
</dt> <dt>



<span data-ttu-id="61262-148">Fehler bei der Überprüfung des EAPHost-Konfigurations Schemas.</span><span class="sxs-lookup"><span data-stu-id="61262-148">The EAPHost configuration schema validation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-149"><span id="EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO"></span><span id="eap_e_method_config_does_not_support_sso"></span>**die EAP \_ E- \_ Methoden \_ Konfiguration \_ \_ \_ unterstützt \_ SSO nicht.**</span><span class="sxs-lookup"><span data-stu-id="61262-149"><span id="EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO"></span><span id="eap_e_method_config_does_not_support_sso"></span>**EAP\_E\_METHOD\_CONFIG\_DOES\_NOT\_SUPPORT\_SSO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-150">0x8042001a</span><span class="sxs-lookup"><span data-stu-id="61262-150">0x8042001A</span></span>
</dt> <dt>



<span data-ttu-id="61262-151">Windows 7 oder höher: die EAP-Methode bietet keine Unterstützung für einmaliges Anmelden (Single Sign on, SSO) für die angegebene Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="61262-151">Windows 7 or later: The EAP method does not support single sign on (SSO) for the provided configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-152"><span id="EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED"></span><span id="eap_e_eaphost_method_operation_not_supported"></span>**der EAP \_ E \_ EAPHost- \_ Methoden \_ Vorgang \_ \_ wird nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="61262-152"><span id="EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED"></span><span id="eap_e_eaphost_method_operation_not_supported"></span>**EAP\_E\_EAPHOST\_METHOD\_OPERATION\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-153">0x80420020</span><span class="sxs-lookup"><span data-stu-id="61262-153">0x80420020</span></span>
</dt> <dt>



<span data-ttu-id="61262-154">EAPHost gibt diesen Fehler zurück, wenn eine konfigurierte EAP-Methode einen angeforderten Vorgang nicht unterstützt (Prozedur aufzurufen).</span><span class="sxs-lookup"><span data-stu-id="61262-154">EAPHost returns this error when a configured EAP method does not support a requested operation (procedure call).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-155"><span id="EAP_E_USER_FIRST"></span><span id="eap_e_user_first"></span>**EAP \_ E- \_ Benutzer \_ zuerst**</span><span class="sxs-lookup"><span data-stu-id="61262-155"><span id="EAP_E_USER_FIRST"></span><span id="eap_e_user_first"></span>**EAP\_E\_USER\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-156">0x80420100l</span><span class="sxs-lookup"><span data-stu-id="61262-156">0x80420100L</span></span>
</dt> <dt>



<span data-ttu-id="61262-157">Definiert die Grenze von Fehlerberichten. alle Benutzer bezogenen Fehler treten zwischen **EAP \_ e \_ User \_ First** und **EAP \_ e \_ User \_ Last** auf.</span><span class="sxs-lookup"><span data-stu-id="61262-157">Defines the boundary of error reports; any user related error will occur between **EAP\_E\_USER\_FIRST** and **EAP\_E\_USER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-158"><span id="EAP_E_USER_LAST_"></span><span id="eap_e_user_last_"></span>**EAP \_ E- \_ Benutzer \_ Letzte**</span><span class="sxs-lookup"><span data-stu-id="61262-158"><span id="EAP_E_USER_LAST_"></span><span id="eap_e_user_last_"></span>**EAP\_E\_USER\_LAST**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-159">0x804201ffl</span><span class="sxs-lookup"><span data-stu-id="61262-159">0x804201FFL</span></span>
</dt> <dt>



<span data-ttu-id="61262-160">Definiert die Grenze von Fehlerberichten. alle Benutzer bezogenen Fehler treten zwischen **EAP \_ e \_ User \_ First** und **EAP \_ e \_ User \_ Last** auf.</span><span class="sxs-lookup"><span data-stu-id="61262-160">Defines the boundary of error reports; any user related error will occur between **EAP\_E\_USER\_FIRST** and **EAP\_E\_USER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-161"><span id="EAP_I_USER_FIRST"></span><span id="eap_i_user_first"></span>**EAP \_ I- \_ Benutzer \_ zuerst**</span><span class="sxs-lookup"><span data-stu-id="61262-161"><span id="EAP_I_USER_FIRST"></span><span id="eap_i_user_first"></span>**EAP\_I\_USER\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-162">0x40420100l</span><span class="sxs-lookup"><span data-stu-id="61262-162">0x40420100L</span></span>
</dt> <dt>



<span data-ttu-id="61262-163">Definiert die Grenze von Informationsberichten. alle EAP-bezogenen Protokolle für Informations Ereignisse werden zwischen **EAP \_ i \_ User \_ First** und **EAP \_ i \_ User \_ Last** ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="61262-163">Defines the boundary of information reports; any EAP related informational event logging will occur between **EAP\_I\_USER\_FIRST** and **EAP\_I\_USER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-164"><span id="EAP_I_USER_LAST"></span><span id="eap_i_user_last"></span>**EAP \_ I- \_ Benutzer \_ Letzte**</span><span class="sxs-lookup"><span data-stu-id="61262-164"><span id="EAP_I_USER_LAST"></span><span id="eap_i_user_last"></span>**EAP\_I\_USER\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-165">0x404201ffl</span><span class="sxs-lookup"><span data-stu-id="61262-165">0x404201FFL</span></span>
</dt> <dt>



<span data-ttu-id="61262-166">Definiert die Grenze von Informationsberichten. alle EAP-bezogenen Protokolle für Informations Ereignisse werden zwischen **EAP \_ i \_ User \_ First** und **EAP \_ i \_ User \_ Last** ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="61262-166">Defines the boundary of information reports; any EAP related informational event logging will occur between **EAP\_I\_USER\_FIRST** and **EAP\_I\_USER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-167"><span id="EAP_E_USER_CERT_NOT_FOUND"></span><span id="eap_e_user_cert_not_found"></span>**EAP \_ E- \_ Benutzer \_ Zertifikat \_ nicht \_ gefunden**</span><span class="sxs-lookup"><span data-stu-id="61262-167"><span id="EAP_E_USER_CERT_NOT_FOUND"></span><span id="eap_e_user_cert_not_found"></span>**EAP\_E\_USER\_CERT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-168">0x80420100</span><span class="sxs-lookup"><span data-stu-id="61262-168">0x80420100</span></span>
</dt> <dt>



<span data-ttu-id="61262-169">EAPHost konnte kein Benutzerzertifikat für die Authentifizierung finden.</span><span class="sxs-lookup"><span data-stu-id="61262-169">EAPHost could not find a user certificate for authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-170"><span id="EAP_E_USER_CERT_INVALID"></span><span id="eap_e_user_cert_invalid"></span>**EAP \_ E- \_ Benutzer \_ Zertifikat \_ ungültig**</span><span class="sxs-lookup"><span data-stu-id="61262-170"><span id="EAP_E_USER_CERT_INVALID"></span><span id="eap_e_user_cert_invalid"></span>**EAP\_E\_USER\_CERT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-171">0x80420101</span><span class="sxs-lookup"><span data-stu-id="61262-171">0x80420101</span></span>
</dt> <dt>



<span data-ttu-id="61262-172">Das Benutzerzertifikat, das für die Authentifizierung verwendet wird, verfügt nicht über die richtige erweiterte Schlüssel Verwendung (EKU).</span><span class="sxs-lookup"><span data-stu-id="61262-172">The user certificate being user for authentication does not have proper extended key usage (EKU) set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-173"><span id="EAP_E_USER_CERT_EXPIRED"></span><span id="eap_e_user_cert_expired"></span>**EAP \_ E- \_ Benutzer \_ Zertifikat \_ abgelaufen**</span><span class="sxs-lookup"><span data-stu-id="61262-173"><span id="EAP_E_USER_CERT_EXPIRED"></span><span id="eap_e_user_cert_expired"></span>**EAP\_E\_USER\_CERT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-174">0x80420102</span><span class="sxs-lookup"><span data-stu-id="61262-174">0x80420102</span></span>
</dt> <dt>



<span data-ttu-id="61262-175">EAPHost hat ein abgelaufenes Benutzerzertifikat gefunden.</span><span class="sxs-lookup"><span data-stu-id="61262-175">EAPhost found an expired user certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-176"><span id="EAP_E_USER_CERT_REVOKED"></span><span id="eap_e_user_cert_revoked"></span>**EAP \_ E- \_ Benutzer \_ Zertifikat \_ gesperrt**</span><span class="sxs-lookup"><span data-stu-id="61262-176"><span id="EAP_E_USER_CERT_REVOKED"></span><span id="eap_e_user_cert_revoked"></span>**EAP\_E\_USER\_CERT\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-177">0x80420103</span><span class="sxs-lookup"><span data-stu-id="61262-177">0x80420103</span></span>
</dt> <dt>



<span data-ttu-id="61262-178">Das Benutzerzertifikat, das für die Authentifizierung verwendet wird, wurde gesperrt.</span><span class="sxs-lookup"><span data-stu-id="61262-178">The user certificate being used for authentication has been revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-179"><span id="EAP_E_USER_CERT_OTHER_ERROR"></span><span id="eap_e_user_cert_other_error"></span>**Fehler beim EAP \_ E- \_ Benutzer \_ Zertifikat \_ \_ .**</span><span class="sxs-lookup"><span data-stu-id="61262-179"><span id="EAP_E_USER_CERT_OTHER_ERROR"></span><span id="eap_e_user_cert_other_error"></span>**EAP\_E\_USER\_CERT\_OTHER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-180">0x80420104</span><span class="sxs-lookup"><span data-stu-id="61262-180">0x80420104</span></span>
</dt> <dt>



<span data-ttu-id="61262-181">Ein unbekannter Fehler ist aufgetreten, wenn die Benutzer Zertifizierung für die Authentifizierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="61262-181">An unknown error occurred with the user certification being used for authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-182"><span id="EAP_E_USER_CERT_REJECTED_"></span><span id="eap_e_user_cert_rejected_"></span>**EAP \_ E- \_ Benutzer \_ Zertifikat \_ abgelehnt**</span><span class="sxs-lookup"><span data-stu-id="61262-182"><span id="EAP_E_USER_CERT_REJECTED_"></span><span id="eap_e_user_cert_rejected_"></span>**EAP\_E\_USER\_CERT\_REJECTED**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-183">0x80420105</span><span class="sxs-lookup"><span data-stu-id="61262-183">0x80420105</span></span>
</dt> <dt>



<span data-ttu-id="61262-184">Der Authentifikator hat die Benutzer Zertifizierung abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="61262-184">The authenticator rejected the user certification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-185"><span id="EAP_I_USER_ACCOUNT_OTHER_ERROR"></span><span id="eap_i_user_account_other_error"></span>**anderer EAP- \_ \_ Benutzer \_ Konto \_ \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="61262-185"><span id="EAP_I_USER_ACCOUNT_OTHER_ERROR"></span><span id="eap_i_user_account_other_error"></span>**EAP\_I\_USER\_ACCOUNT\_OTHER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-186">0x40420110</span><span class="sxs-lookup"><span data-stu-id="61262-186">0x40420110</span></span>
</dt> <dt>



<span data-ttu-id="61262-187">Nach einem Identitäts Austausch wurde ein EAP-Fehler empfangen, der die Wahrscheinlichkeit eines Problems mit dem Konto des authentifizier enden Benutzers angibt.</span><span class="sxs-lookup"><span data-stu-id="61262-187">An EAP failure was received after an identity exchange, indicating the likelihood of a problem with the authenticating user's account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-188"><span id="EAP_E_USER_CREDENTIALS_REJECTED"></span><span id="eap_e_user_credentials_rejected"></span>**EAP \_ E- \_ Benutzer \_ Anmelde Informationen \_ abgelehnt**</span><span class="sxs-lookup"><span data-stu-id="61262-188"><span id="EAP_E_USER_CREDENTIALS_REJECTED"></span><span id="eap_e_user_credentials_rejected"></span>**EAP\_E\_USER\_CREDENTIALS\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-189">0x80420111</span><span class="sxs-lookup"><span data-stu-id="61262-189">0x80420111</span></span>
</dt> <dt>



<span data-ttu-id="61262-190">Der Authentifikator hat die Benutzer Anmelde Informationen für die Authentifizierung abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="61262-190">The authenticator rejected user credentials for authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-191"><span id="EAP_E_USER_NAME_PASSWORD_REJECTED"></span><span id="eap_e_user_name_password_rejected"></span>**Kennwort für EAP \_ E- \_ Benutzer \_ Name \_ \_ abgelehnt**</span><span class="sxs-lookup"><span data-stu-id="61262-191"><span id="EAP_E_USER_NAME_PASSWORD_REJECTED"></span><span id="eap_e_user_name_password_rejected"></span>**EAP\_E\_USER\_NAME\_PASSWORD\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-192">0x80420112</span><span class="sxs-lookup"><span data-stu-id="61262-192">0x80420112</span></span>
</dt> <dt>



<span data-ttu-id="61262-193">Windows 7 oder höher: Fehler bei der Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="61262-193">Windows 7 or later: Authentication failed.</span></span> <span data-ttu-id="61262-194">Der Authentifikator hat die Anmelde Informationen des Benutzers abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="61262-194">The authenticator rejected the user credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-195"><span id="EAP_E_NO_SMART_CARD_READER"></span><span id="eap_e_no_smart_card_reader"></span>**EAP \_ E \_ kein \_ \_ \_ Smartcardleser**</span><span class="sxs-lookup"><span data-stu-id="61262-195"><span id="EAP_E_NO_SMART_CARD_READER"></span><span id="eap_e_no_smart_card_reader"></span>**EAP\_E\_NO\_SMART\_CARD\_READER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-196">0x80420113</span><span class="sxs-lookup"><span data-stu-id="61262-196">0x80420113</span></span>
</dt> <dt>



<span data-ttu-id="61262-197">Windows 7 oder höher: Es wurde kein Smartcardleser gefunden.</span><span class="sxs-lookup"><span data-stu-id="61262-197">Windows 7 or later: No smart card reader found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-198"><span id="EAP_E_SERVER_FIRST"></span><span id="eap_e_server_first"></span>**EAP \_ E \_ Server \_ First**</span><span class="sxs-lookup"><span data-stu-id="61262-198"><span id="EAP_E_SERVER_FIRST"></span><span id="eap_e_server_first"></span>**EAP\_E\_SERVER\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-199">0x80420200l</span><span class="sxs-lookup"><span data-stu-id="61262-199">0x80420200L</span></span>
</dt> <dt>



<span data-ttu-id="61262-200">Definiert die Grenze von Fehlerberichten. alle Server bezogenen Fehler werden zwischen **EAP \_ e \_ Server \_ First** und **EAP \_ e \_ Server \_ Last** auftreten.</span><span class="sxs-lookup"><span data-stu-id="61262-200">Defines the boundary of error reports; any server related error will occur between **EAP\_E\_SERVER\_FIRST** and **EAP\_E\_SERVER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-201"><span id="EAP_E_SERVER_LAST"></span><span id="eap_e_server_last"></span>**EAP \_ E- \_ Server \_ zuletzt**</span><span class="sxs-lookup"><span data-stu-id="61262-201"><span id="EAP_E_SERVER_LAST"></span><span id="eap_e_server_last"></span>**EAP\_E\_SERVER\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-202">0x804202ffl</span><span class="sxs-lookup"><span data-stu-id="61262-202">0x804202FFL</span></span>
</dt> <dt>



<span data-ttu-id="61262-203">Definiert die Grenze von Fehlerberichten. alle Server bezogenen Fehler werden zwischen **EAP \_ e \_ Server \_ First** und **EAP \_ e \_ Server \_ Last** auftreten.</span><span class="sxs-lookup"><span data-stu-id="61262-203">Defines the boundary of error reports; any server related error will occur between **EAP\_E\_SERVER\_FIRST** and **EAP\_E\_SERVER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-204"><span id="EAP_E_SERVER_CERT_NOT_FOUND"></span><span id="eap_e_server_cert_not_found"></span>**EAP \_ E- \_ Server- \_ CERT \_ nicht \_ gefunden**</span><span class="sxs-lookup"><span data-stu-id="61262-204"><span id="EAP_E_SERVER_CERT_NOT_FOUND"></span><span id="eap_e_server_cert_not_found"></span>**EAP\_E\_SERVER\_CERT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-205">0x80420200</span><span class="sxs-lookup"><span data-stu-id="61262-205">0x80420200</span></span>
</dt> <dt>



<span data-ttu-id="61262-206">EAPHost konnte das Serverzertifikat für die Authentifizierung nicht finden.</span><span class="sxs-lookup"><span data-stu-id="61262-206">EAPHost could not find the server certificate for authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-207"><span id="EAP_E_SERVER_CERT_INVALID"></span><span id="eap_e_server_cert_invalid"></span>**EAP \_ E- \_ Server \_ Zertifikat \_ ungültig**</span><span class="sxs-lookup"><span data-stu-id="61262-207"><span id="EAP_E_SERVER_CERT_INVALID"></span><span id="eap_e_server_cert_invalid"></span>**EAP\_E\_SERVER\_CERT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-208">0x80420201</span><span class="sxs-lookup"><span data-stu-id="61262-208">0x80420201</span></span>
</dt> <dt>



<span data-ttu-id="61262-209">Das Serverzertifikat, das als Benutzer für die Authentifizierung dient, verfügt über keinen geeigneten EKU-Satz (Extended Key Usage).</span><span class="sxs-lookup"><span data-stu-id="61262-209">The server certificate being user for authentication does not have a proper extended key usage (EKU) set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-210"><span id="EAP_E_SERVER_CERT_EXPIRED"></span><span id="eap_e_server_cert_expired"></span>**EAP \_ E \_ Server- \_ Zertifikat \_ abgelaufen**</span><span class="sxs-lookup"><span data-stu-id="61262-210"><span id="EAP_E_SERVER_CERT_EXPIRED"></span><span id="eap_e_server_cert_expired"></span>**EAP\_E\_SERVER\_CERT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-211">0x80420202</span><span class="sxs-lookup"><span data-stu-id="61262-211">0x80420202</span></span>
</dt> <dt>



<span data-ttu-id="61262-212">EAPHost hat ein abgelaufenes Serverzertifikat gefunden.</span><span class="sxs-lookup"><span data-stu-id="61262-212">EAPhost found an expired server certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-213"><span id="EAP_E_SERVER_CERT_REVOKED"></span><span id="eap_e_server_cert_revoked"></span>**EAP \_ E- \_ Server \_ Zertifikat \_ gesperrt**</span><span class="sxs-lookup"><span data-stu-id="61262-213"><span id="EAP_E_SERVER_CERT_REVOKED"></span><span id="eap_e_server_cert_revoked"></span>**EAP\_E\_SERVER\_CERT\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-214">0x80420203</span><span class="sxs-lookup"><span data-stu-id="61262-214">0x80420203</span></span>
</dt> <dt>



<span data-ttu-id="61262-215">Das Serverzertifikat, das für die Authentifizierung verwendet wird, wurde gesperrt.</span><span class="sxs-lookup"><span data-stu-id="61262-215">The server certificate being used for authentication has been revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-216"><span id="EAP_E_SERVER_CERT_OTHER_ERROR"></span><span id="eap_e_server_cert_other_error"></span>**anderer EAP \_ E-Server- \_ CERT- \_ \_ \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="61262-216"><span id="EAP_E_SERVER_CERT_OTHER_ERROR"></span><span id="eap_e_server_cert_other_error"></span>**EAP\_E\_SERVER\_CERT\_OTHER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-217">0x80420204</span><span class="sxs-lookup"><span data-stu-id="61262-217">0x80420204</span></span>
</dt> <dt>



<span data-ttu-id="61262-218">Unbekannter Fehler beim Serverzertifikat.</span><span class="sxs-lookup"><span data-stu-id="61262-218">An unknown error occurred with the server certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-219"><span id="EAP_E_USER_ROOT_CERT_FIRST"></span><span id="eap_e_user_root_cert_first"></span>**EAP \_ E- \_ Benutzer Stamm \_ \_ Zertifikat \_ zuerst**</span><span class="sxs-lookup"><span data-stu-id="61262-219"><span id="EAP_E_USER_ROOT_CERT_FIRST"></span><span id="eap_e_user_root_cert_first"></span>**EAP\_E\_USER\_ROOT\_CERT\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-220">0x80420300l</span><span class="sxs-lookup"><span data-stu-id="61262-220">0x80420300L</span></span>
</dt> <dt>



<span data-ttu-id="61262-221">Definiert die Grenze von Fehlerberichten. alle Fehler im Zusammenhang mit dem Benutzer Stamm Zertifikat treten zuerst zwischen dem **EAP e-Benutzer Stamm Zertifikat \_ \_ \_ \_ \_ First** und dem **EAP \_ e- \_ Benutzer \_ \_ \_** Stamm Zertifikat auf.</span><span class="sxs-lookup"><span data-stu-id="61262-221">Defines the boundary of error reports; any user root certificate related error will occur between **EAP\_E\_USER\_ROOT\_CERT\_FIRST** and **EAP\_E\_USER\_ROOT\_CERT\_FIRST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-222"><span id="EAP_E_USER_ROOT_CERT_LAST"></span><span id="eap_e_user_root_cert_last"></span>**EAP \_ E- \_ Benutzer Stamm \_ \_ Zertifikat \_ zuletzt**</span><span class="sxs-lookup"><span data-stu-id="61262-222"><span id="EAP_E_USER_ROOT_CERT_LAST"></span><span id="eap_e_user_root_cert_last"></span>**EAP\_E\_USER\_ROOT\_CERT\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-223">0x804203ffl</span><span class="sxs-lookup"><span data-stu-id="61262-223">0x804203FFL</span></span>
</dt> <dt>



<span data-ttu-id="61262-224">Definiert die Grenze von Fehlerberichten. alle Fehler im Zusammenhang mit dem Benutzer Stamm Zertifikat treten zuerst zwischen dem **EAP e-Benutzer Stamm Zertifikat \_ \_ \_ \_ \_ First** und dem **EAP \_ e- \_ Benutzer \_ \_ \_** Stamm Zertifikat auf.</span><span class="sxs-lookup"><span data-stu-id="61262-224">Defines the boundary of error reports; any user root certificate related error will occur between **EAP\_E\_USER\_ROOT\_CERT\_FIRST** and **EAP\_E\_USER\_ROOT\_CERT\_FIRST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-225"><span id="EAP_E_USER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_user_root_cert_not_found"></span>**EAP \_ E-Stamm \_ Zertifikat für Benutzer \_ \_ \_ nicht \_ gefunden**</span><span class="sxs-lookup"><span data-stu-id="61262-225"><span id="EAP_E_USER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_user_root_cert_not_found"></span>**EAP\_E\_USER\_ROOT\_CERT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-226">0x80420300</span><span class="sxs-lookup"><span data-stu-id="61262-226">0x80420300</span></span>
</dt> <dt>



<span data-ttu-id="61262-227">EAPHost konnte kein Zertifikat in einem vertrauenswürdigen Stamm Zertifikat Speicher für die Validierung der Benutzer Zertifizierungsstelle finden.</span><span class="sxs-lookup"><span data-stu-id="61262-227">EAPHost could not find a certificate in a trusted root certificate store for user certification validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-228"><span id="EAP_E_USER_ROOT_CERT_INVALID"></span><span id="eap_e_user_root_cert_invalid"></span>**EAP \_ E-Stamm \_ Zertifikat für Benutzer \_ \_ \_ ungültig**</span><span class="sxs-lookup"><span data-stu-id="61262-228"><span id="EAP_E_USER_ROOT_CERT_INVALID"></span><span id="eap_e_user_root_cert_invalid"></span>**EAP\_E\_USER\_ROOT\_CERT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-229">0x80420301</span><span class="sxs-lookup"><span data-stu-id="61262-229">0x80420301</span></span>
</dt> <dt>



<span data-ttu-id="61262-230">Die Authentifizierung ist fehlgeschlagen, weil das für dieses Netzwerk verwendete Stamm Zertifikat ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="61262-230">The authentication failed because the root certificate used for this network is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-231"><span id="EAP_E_USER_ROOT_CERT_EXPIRED"></span><span id="eap_e_user_root_cert_expired"></span>**EAP \_ E-Stamm \_ Zertifikat für Benutzer \_ \_ \_ abgelaufen**</span><span class="sxs-lookup"><span data-stu-id="61262-231"><span id="EAP_E_USER_ROOT_CERT_EXPIRED"></span><span id="eap_e_user_root_cert_expired"></span>**EAP\_E\_USER\_ROOT\_CERT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-232">0x80420302</span><span class="sxs-lookup"><span data-stu-id="61262-232">0x80420302</span></span>
</dt> <dt>



<span data-ttu-id="61262-233">Das für die Validierung des Benutzer Zertifikats erforderliche vertrauenswürdige Stamm Zertifikat ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="61262-233">The trusted root certificate needed for user certificate validation has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-234"><span id="EAP_E_SERVER_ROOT_CERT_FIRST"></span><span id="eap_e_server_root_cert_first"></span>**EAP-E-Server-Stamm \_ \_ \_ \_ Zertifikat \_ zuerst**</span><span class="sxs-lookup"><span data-stu-id="61262-234"><span id="EAP_E_SERVER_ROOT_CERT_FIRST"></span><span id="eap_e_server_root_cert_first"></span>**EAP\_E\_SERVER\_ROOT\_CERT\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-235">0x80420400l</span><span class="sxs-lookup"><span data-stu-id="61262-235">0x80420400L</span></span>
</dt> <dt>



<span data-ttu-id="61262-236">Definiert die Grenze von Fehlerberichten. alle Fehler im Zusammenhang mit dem Server Stamm Zertifikat treten zuerst zwischen **EAP \_ e \_ Server \_ root \_ CERT \_ First** und **EAP \_ e \_ Server \_ root \_ CERT \_** auf.</span><span class="sxs-lookup"><span data-stu-id="61262-236">Defines the boundary of error reports; any server root certificate related error will occur between **EAP\_E\_SERVER\_ROOT\_CERT\_FIRST** and **EAP\_E\_SERVER\_ROOT\_CERT\_FIRST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-237"><span id="EAP_E_SERVER_ROOT_CERT_LAST"></span><span id="eap_e_server_root_cert_last"></span>**EAP \_ E-Server-Stamm \_ \_ \_ Zertifikat \_ zuletzt**</span><span class="sxs-lookup"><span data-stu-id="61262-237"><span id="EAP_E_SERVER_ROOT_CERT_LAST"></span><span id="eap_e_server_root_cert_last"></span>**EAP\_E\_SERVER\_ROOT\_CERT\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-238">0x804204ffl</span><span class="sxs-lookup"><span data-stu-id="61262-238">0x804204FFL</span></span>
</dt> <dt>



<span data-ttu-id="61262-239">Definiert die Grenze von Fehlerberichten. alle Fehler im Zusammenhang mit dem Server Stamm Zertifikat treten zuerst zwischen **EAP \_ e \_ Server \_ root \_ CERT \_ First** und **EAP \_ e \_ Server \_ root \_ CERT \_** auf.</span><span class="sxs-lookup"><span data-stu-id="61262-239">Defines the boundary of error reports; any server root certificate related error will occur between **EAP\_E\_SERVER\_ROOT\_CERT\_FIRST** and **EAP\_E\_SERVER\_ROOT\_CERT\_FIRST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-240"><span id="EAP_E_SERVER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_server_root_cert_not_found"></span>**Das EAP \_ E- \_ Server Stamm Zertifikat wurde \_ \_ \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="61262-240"><span id="EAP_E_SERVER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_server_root_cert_not_found"></span>**EAP\_E\_SERVER\_ROOT\_CERT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-241">0x80420400</span><span class="sxs-lookup"><span data-stu-id="61262-241">0x80420400</span></span>
</dt> <dt>



<span data-ttu-id="61262-242">EAPHost konnte kein Stamm Zertifikat in einem vertrauenswürdigen Stamm Zertifikat Speicher für die Überprüfung der Server Zertifizierung finden.</span><span class="sxs-lookup"><span data-stu-id="61262-242">EAPHost could not find a root certificate in a trusted root certificate store for the server certification validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-243"><span id="EAP_E_SERVER_ROOT_CERT_INVALID__________"></span><span id="eap_e_server_root_cert_invalid__________"></span>**EAP \_ E \_ Server \_ root- \_ Zertifikat \_ ungültig**</span><span class="sxs-lookup"><span data-stu-id="61262-243"><span id="EAP_E_SERVER_ROOT_CERT_INVALID__________"></span><span id="eap_e_server_root_cert_invalid__________"></span>**EAP\_E\_SERVER\_ROOT\_CERT\_INVALID**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-244">0x80420401</span><span class="sxs-lookup"><span data-stu-id="61262-244">0x80420401</span></span>
</dt> <dt>



<span data-ttu-id="61262-245">Die Authentifizierung ist fehlgeschlagen, weil das für dieses Netzwerk auf dem Server Computer erforderliche Serverzertifikat ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="61262-245">The authentication failed because the server certificate required for this network on the server computer is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61262-246"><span id="EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED"></span><span id="eap_e_server_root_cert_name_required"></span>**der EAP \_ E- \_ Server Stamm \_ \_ Zertifikat Name ist \_ \_ erforderlich.**</span><span class="sxs-lookup"><span data-stu-id="61262-246"><span id="EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED"></span><span id="eap_e_server_root_cert_name_required"></span>**EAP\_E\_SERVER\_ROOT\_CERT\_NAME\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61262-247">0x80420406</span><span class="sxs-lookup"><span data-stu-id="61262-247">0x80420406</span></span>
</dt> <dt>



<span data-ttu-id="61262-248">Die Authentifizierung ist fehlgeschlagen, weil für das Zertifikat auf dem Server Computer kein Servername angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="61262-248">The authentication failed because the certificate on the server computer does not have a server name specified.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="61262-249">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61262-249">Remarks</span></span>

<span data-ttu-id="61262-250">Für bestimmte Fehler gibt es alternative Namen:</span><span class="sxs-lookup"><span data-stu-id="61262-250">There are alternate names for certain errors:</span></span>

-   <span data-ttu-id="61262-251">Ein anderer Name für die **EAP \_ E \_ EAPHost- \_ Methode " \_ ungültiges \_ Paket** " ist das **EAP- \_ \_ ungültige \_ Paket**.</span><span class="sxs-lookup"><span data-stu-id="61262-251">Another name for **EAP\_E\_EAPHOST\_METHOD\_INVALID\_PACKET** is **EAP\_METHOD\_INVALID\_PACKET**.</span></span>
-   <span data-ttu-id="61262-252">Ein anderer Name für das **\_ \_ \_ Remote ungültige EAP \_ E \_ EAPHost-Paket** ist ein **Ungültiges EAP- \_ \_ Paket**.</span><span class="sxs-lookup"><span data-stu-id="61262-252">Another name for **EAP\_E\_EAPHOST\_REMOTE\_INVALID\_PACKET** is **EAP\_INVALID\_PACKET**.</span></span>

## <a name="requirements"></a><span data-ttu-id="61262-253">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61262-253">Requirements</span></span>



| <span data-ttu-id="61262-254">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61262-254">Requirement</span></span> | <span data-ttu-id="61262-255">Wert</span><span class="sxs-lookup"><span data-stu-id="61262-255">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="61262-256">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="61262-256">Minimum supported client</span></span><br/> | <span data-ttu-id="61262-257">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="61262-257">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="61262-258">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="61262-258">Minimum supported server</span></span><br/> | <span data-ttu-id="61262-259">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="61262-259">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="61262-260">Header</span><span class="sxs-lookup"><span data-stu-id="61262-260">Header</span></span><br/>                   | <dl> <span data-ttu-id="61262-261"><dt>EAPHost RoR. h</dt></span><span class="sxs-lookup"><span data-stu-id="61262-261"><dt>Eaphosterror.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61262-262">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61262-262">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61262-263">Allgemeine EAPHost-Konstanten</span><span class="sxs-lookup"><span data-stu-id="61262-263">Common EAPHost Constants</span></span>](common-eap-host-error-constants.md)
</dt> </dl>

 

