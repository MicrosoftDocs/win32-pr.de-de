---
title: NAP-Fehler Konstanten (Winerror. h)
description: Die folgenden NAP-Fehler Konstanten werden in WinError. h definiert.
ms.assetid: b2fba990-75d9-4153-8058-c01e97700d00
topic_type:
- apiref
api_name:
- NAP_E_INVALID_PACKET
- NAP_E_MISSING_SOH
- NAP_E_CONFLICTING_ID
- NAP_E_NO_CACHED_SOH
- NAP_E_STILL_BOUND
- NAP_E_NOT_REGISTERED
- NAP_E_NOT_INITIALIZED
- NAP_E_MISMATCHED_ID
- NAP_E_NOT_PENDING
- NAP_E_ID_NOT_FOUND
- NAP_E_MAXSIZE_TOO_SMALL
- NAP_E_SERVICE_NOT_RUNNING
- NAP_S_CERT_ALREADY_PRESENT
- NAP_E_ENTITY_DISABLED
- NAP_E_NETSH_GROUPPOLICY_ERROR
- NAP_E_TOO_MANY_CALLS
- NAP_E_SHV_CONFIG_EXISTED
- NAP_E_SHV_CONFIG_NOT_FOUND
- NAP_E_SHV_TIMEOUT
api_location:
- WinError.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b871d6f00174f05ab580aad54395851fa70af877
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956964"
---
# <a name="nap-error-constants"></a><span data-ttu-id="c2c06-103">NAP-Fehler Konstanten</span><span class="sxs-lookup"><span data-stu-id="c2c06-103">NAP Error Constants</span></span>

> [!Note]  
> <span data-ttu-id="c2c06-104">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c2c06-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c2c06-105">Die folgenden NAP-Fehler Konstanten werden in WinError. h definiert.</span><span class="sxs-lookup"><span data-stu-id="c2c06-105">The following NAP error constants are defined in WinError.h.</span></span>

<dl> <dt>

<span data-ttu-id="c2c06-106"><span id="NAP_E_INVALID_PACKET"></span><span id="nap_e_invalid_packet"></span>**\_ \_ Ungültiges NAP- \_ Paket**</span><span class="sxs-lookup"><span data-stu-id="c2c06-106"><span id="NAP_E_INVALID_PACKET"></span><span id="nap_e_invalid_packet"></span>**NAP\_E\_INVALID\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2c06-107">\_HRESULT- \_ typedef \_ (0x80270001l)</span><span class="sxs-lookup"><span data-stu-id="c2c06-107">\_HRESULT\_TYPEDEF\_(0x80270001L)</span></span>
</dt> <dt>



<span data-ttu-id="c2c06-108">Das NAP- [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) -Paket ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c2c06-108">The NAP [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c2c06-109"><span id="NAP_E_MISSING_SOH"></span><span id="nap_e_missing_soh"></span>**NAP \_ E \_ fehlt \_ SoH**</span><span class="sxs-lookup"><span data-stu-id="c2c06-109"><span id="NAP_E_MISSING_SOH"></span><span id="nap_e_missing_soh"></span>**NAP\_E\_MISSING\_SOH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2c06-110">\_HRESULT- \_ typedef \_ (0x80270002l)</span><span class="sxs-lookup"><span data-stu-id="c2c06-110">\_HRESULT\_TYPEDEF\_(0x80270002L)</span></span>
</dt> <dt>



<span data-ttu-id="c2c06-111">Im NAP-Paket fehlte ein [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="c2c06-111">An [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) was missing from the NAP packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c2c06-112"><span id="NAP_E_CONFLICTING_ID"></span><span id="nap_e_conflicting_id"></span>**in \_ \_ Konflikt stehende \_ ID für NAP**</span><span class="sxs-lookup"><span data-stu-id="c2c06-112"><span id="NAP_E_CONFLICTING_ID"></span><span id="nap_e_conflicting_id"></span>**NAP\_E\_CONFLICTING\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2c06-113">\_HRESULT- \_ typedef \_ (0x80270003l)</span><span class="sxs-lookup"><span data-stu-id="c2c06-113">\_HRESULT\_TYPEDEF\_(0x80270003L)</span></span>
</dt> <dt>



<span data-ttu-id="c2c06-114">Die Entitäts-ID steht in Konflikt mit einer bereits registrierten Entitäts-ID.</span><span class="sxs-lookup"><span data-stu-id="c2c06-114">The entity ID conflicts with an already-registered entity ID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c2c06-115"><span id="NAP_E_NO_CACHED_SOH"></span><span id="nap_e_no_cached_soh"></span>**NAP \_ E \_ kein \_ zwischengespeichertes \_ SoH**</span><span class="sxs-lookup"><span data-stu-id="c2c06-115"><span id="NAP_E_NO_CACHED_SOH"></span><span id="nap_e_no_cached_soh"></span>**NAP\_E\_NO\_CACHED\_SOH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2c06-116">\_HRESULT- \_ typedef \_ (0x80270004l)</span><span class="sxs-lookup"><span data-stu-id="c2c06-116">\_HRESULT\_TYPEDEF\_(0x80270004L)</span></span>
</dt> <dt>



<span data-ttu-id="c2c06-117">Es ist kein zwischengespeichertes [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c2c06-117">No cached [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) is present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c2c06-118"><span id="NAP_E_STILL_BOUND"></span><span id="nap_e_still_bound"></span>**NAP \_ E \_ trotzdem \_ gebunden**</span><span class="sxs-lookup"><span data-stu-id="c2c06-118"><span id="NAP_E_STILL_BOUND"></span><span id="nap_e_still_bound"></span>**NAP\_E\_STILL\_BOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2c06-119">\_HRESULT- \_ typedef \_ (0x80270005l)</span><span class="sxs-lookup"><span data-stu-id="c2c06-119">\_HRESULT\_TYPEDEF\_(0x80270005L)</span></span>
</dt> <dt>



<span data-ttu-id="c2c06-120">Die Entität ist weiterhin an das NAP-System gebunden.</span><span class="sxs-lookup"><span data-stu-id="c2c06-120">The entity is still bound to the NAP system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c2c06-121"><span id="NAP_E_NOT_REGISTERED"></span><span id="nap_e_not_registered"></span>**NAP \_ E \_ nicht \_ registriert**</span><span class="sxs-lookup"><span data-stu-id="c2c06-121"><span id="NAP_E_NOT_REGISTERED"></span><span id="nap_e_not_registered"></span>**NAP\_E\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2c06-122">\_HRESULT- \_ typedef \_ (0x80270006l)</span><span class="sxs-lookup"><span data-stu-id="c2c06-122">\_HRESULT\_TYPEDEF\_(0x80270006L)</span></span>
</dt> <dt>



<span data-ttu-id="c2c06-123">Die Entität ist nicht beim NAP-System registriert.</span><span class="sxs-lookup"><span data-stu-id="c2c06-123">The entity is not registered with the NAP system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c2c06-124"><span id="NAP_E_NOT_INITIALIZED"></span><span id="nap_e_not_initialized"></span>**NAP \_ E \_ nicht \_ Initialisiert**</span><span class="sxs-lookup"><span data-stu-id="c2c06-124"><span id="NAP_E_NOT_INITIALIZED"></span><span id="nap_e_not_initialized"></span>**NAP\_E\_NOT\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2c06-125">\_HRESULT- \_ typedef \_ (0x80270007l)</span><span class="sxs-lookup"><span data-stu-id="c2c06-125">\_HRESULT\_TYPEDEF\_(0x80270007L)</span></span>
</dt> <dt>



<span data-ttu-id="c2c06-126">Die Entität ist nicht mit dem NAP-System initialisiert.</span><span class="sxs-lookup"><span data-stu-id="c2c06-126">The entity is not initialized with the NAP system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c2c06-127"><span id="NAP_E_MISMATCHED_ID"></span><span id="nap_e_mismatched_id"></span>**nicht \_ \_ übereinstimmende NAP- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="c2c06-127"><span id="NAP_E_MISMATCHED_ID"></span><span id="nap_e_mismatched_id"></span>**NAP\_E\_MISMATCHED\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2c06-128">\_HRESULT- \_ typedef \_ (0x80270008l)</span><span class="sxs-lookup"><span data-stu-id="c2c06-128">\_HRESULT\_TYPEDEF\_(0x80270008L)</span></span>
</dt> <dt>



<span data-ttu-id="c2c06-129">Die Korrelations-IDs in der [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) -Anforderung und **SoH** -Antwort stimmen nicht ab.</span><span class="sxs-lookup"><span data-stu-id="c2c06-129">The correlation IDs in the [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) request and **SoH** response do not match up.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c2c06-130"><span id="NAP_E_NOT_PENDING"></span><span id="nap_e_not_pending"></span>**NAP \_ E \_ nicht \_ Ausstehend**</span><span class="sxs-lookup"><span data-stu-id="c2c06-130"><span id="NAP_E_NOT_PENDING"></span><span id="nap_e_not_pending"></span>**NAP\_E\_NOT\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2c06-131">\_HRESULT- \_ typedef \_ (0x80270009l)</span><span class="sxs-lookup"><span data-stu-id="c2c06-131">\_HRESULT\_TYPEDEF\_(0x80270009L)</span></span>
</dt> <dt>



<span data-ttu-id="c2c06-132">Der Abschluss wurde für eine Anforderung angegeben, die derzeit nicht aussteht.</span><span class="sxs-lookup"><span data-stu-id="c2c06-132">Completion was indicated on a request that is not currently pending.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c2c06-133"><span id="NAP_E_ID_NOT_FOUND"></span><span id="nap_e_id_not_found"></span>**NAP- \_ E- \_ ID \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="c2c06-133"><span id="NAP_E_ID_NOT_FOUND"></span><span id="nap_e_id_not_found"></span>**NAP\_E\_ID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2c06-134">\_HRESULT- \_ typedef \_ (0x8027000al)</span><span class="sxs-lookup"><span data-stu-id="c2c06-134">\_HRESULT\_TYPEDEF\_(0x8027000AL)</span></span>
</dt> <dt>



<span data-ttu-id="c2c06-135">Die ID der NAP-Komponente wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="c2c06-135">The NAP component's ID was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c2c06-136"><span id="NAP_E_MAXSIZE_TOO_SMALL"></span><span id="nap_e_maxsize_too_small"></span>**NAP \_ E \_ MaxSize \_ zu \_ klein**</span><span class="sxs-lookup"><span data-stu-id="c2c06-136"><span id="NAP_E_MAXSIZE_TOO_SMALL"></span><span id="nap_e_maxsize_too_small"></span>**NAP\_E\_MAXSIZE\_TOO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2c06-137">\_HRESULT- \_ typedef \_ (0x8027000bl)</span><span class="sxs-lookup"><span data-stu-id="c2c06-137">\_HRESULT\_TYPEDEF\_(0x8027000BL)</span></span>
</dt> <dt>



<span data-ttu-id="c2c06-138">Die maximale Größe der Verbindung ist zu klein für ein SoH-Paket.</span><span class="sxs-lookup"><span data-stu-id="c2c06-138">The maximum size of the connection is too small for an SoH packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c2c06-139"><span id="NAP_E_SERVICE_NOT_RUNNING"></span><span id="nap_e_service_not_running"></span>**NAP- \_ E- \_ Dienst wird \_ nicht \_ ausgeführt**</span><span class="sxs-lookup"><span data-stu-id="c2c06-139"><span id="NAP_E_SERVICE_NOT_RUNNING"></span><span id="nap_e_service_not_running"></span>**NAP\_E\_SERVICE\_NOT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2c06-140">\_HRESULT- \_ typedef \_ (0x8027000cl)</span><span class="sxs-lookup"><span data-stu-id="c2c06-140">\_HRESULT\_TYPEDEF\_(0x8027000CL)</span></span>
</dt> <dt>



<span data-ttu-id="c2c06-141">Der NAPAgent-Dienst wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2c06-141">The NapAgent service is not running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c2c06-142"><span id="NAP_S_CERT_ALREADY_PRESENT"></span><span id="nap_s_cert_already_present"></span>**das NAP- \_ \_ Zertifikat ist \_ bereits \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="c2c06-142"><span id="NAP_S_CERT_ALREADY_PRESENT"></span><span id="nap_s_cert_already_present"></span>**NAP\_S\_CERT\_ALREADY\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2c06-143">\_HRESULT- \_ typedef \_ (0x0027000dl)</span><span class="sxs-lookup"><span data-stu-id="c2c06-143">\_HRESULT\_TYPEDEF\_(0x0027000DL)</span></span> 
</dt> <dt>



<span data-ttu-id="c2c06-144">Im Zertifikat Speicher ist bereits ein Zertifikat vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c2c06-144">A certificate is already present in the certificate store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c2c06-145"><span id="NAP_E_ENTITY_DISABLED"></span><span id="nap_e_entity_disabled"></span>**NAP- \_ E- \_ Entität \_ deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="c2c06-145"><span id="NAP_E_ENTITY_DISABLED"></span><span id="nap_e_entity_disabled"></span>**NAP\_E\_ENTITY\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2c06-146">\_HRESULT- \_ typedef \_ (0x8027000el)</span><span class="sxs-lookup"><span data-stu-id="c2c06-146">\_HRESULT\_TYPEDEF\_(0x8027000EL)</span></span>
</dt> <dt>



<span data-ttu-id="c2c06-147">Die Entität ist mit dem NAPAgent-Dienst deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c2c06-147">The entity is disabled with the NapAgent service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c2c06-148"><span id="NAP_E_NETSH_GROUPPOLICY_ERROR"></span><span id="nap_e_netsh_grouppolicy_error"></span>**NAP \_ E \_ netsh \_ GroupPolicy- \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="c2c06-148"><span id="NAP_E_NETSH_GROUPPOLICY_ERROR"></span><span id="nap_e_netsh_grouppolicy_error"></span>**NAP\_E\_NETSH\_GROUPPOLICY\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2c06-149">\_HRESULT- \_ typedef \_ (0x8027000fl)</span><span class="sxs-lookup"><span data-stu-id="c2c06-149">\_HRESULT\_TYPEDEF\_(0x8027000FL)</span></span>
</dt> <dt>



<span data-ttu-id="c2c06-150">Gruppenrichtlinie ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="c2c06-150">Group Policy is not configured.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c2c06-151"><span id="NAP_E_TOO_MANY_CALLS"></span><span id="nap_e_too_many_calls"></span>**NAP- \_ E \_ zu \_ viele \_ Aufrufe**</span><span class="sxs-lookup"><span data-stu-id="c2c06-151"><span id="NAP_E_TOO_MANY_CALLS"></span><span id="nap_e_too_many_calls"></span>**NAP\_E\_TOO\_MANY\_CALLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2c06-152">\_HRESULT- \_ typedef \_ (0x80270010l)</span><span class="sxs-lookup"><span data-stu-id="c2c06-152">\_HRESULT\_TYPEDEF\_(0x80270010L)</span></span>
</dt> <dt>



<span data-ttu-id="c2c06-153">Zu viele gleichzeitige Aufrufe.</span><span class="sxs-lookup"><span data-stu-id="c2c06-153">Too many simultaneous calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c2c06-154"><span id="NAP_E_SHV_CONFIG_EXISTED"></span><span id="nap_e_shv_config_existed"></span>**NAP- \_ E- \_ SHV- \_ Konfiguration \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="c2c06-154"><span id="NAP_E_SHV_CONFIG_EXISTED"></span><span id="nap_e_shv_config_existed"></span>**NAP\_E\_SHV\_CONFIG\_EXISTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2c06-155">\_HRESULT- \_ typedef \_ (0x80270011l)</span><span class="sxs-lookup"><span data-stu-id="c2c06-155">\_HRESULT\_TYPEDEF\_(0x80270011L)</span></span>
</dt> <dt>



<span data-ttu-id="c2c06-156">Die SHV-Konfiguration ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c2c06-156">SHV configuration already exists.</span></span>

> [!Note]  
> <span data-ttu-id="c2c06-157">Unterstützt in Windows 7 oder höher.</span><span class="sxs-lookup"><span data-stu-id="c2c06-157">Supported in Windows 7 or later.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="c2c06-158"><span id="NAP_E_SHV_CONFIG_NOT_FOUND"></span><span id="nap_e_shv_config_not_found"></span>**NAP- \_ E- \_ SHV- \_ Konfiguration \_ nicht \_ gefunden**</span><span class="sxs-lookup"><span data-stu-id="c2c06-158"><span id="NAP_E_SHV_CONFIG_NOT_FOUND"></span><span id="nap_e_shv_config_not_found"></span>**NAP\_E\_SHV\_CONFIG\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2c06-159">\_HRESULT- \_ typedef \_ (0x80270012l)</span><span class="sxs-lookup"><span data-stu-id="c2c06-159">\_HRESULT\_TYPEDEF\_(0x80270012L)</span></span>
</dt> <dt>



<span data-ttu-id="c2c06-160">Die SHV-Konfiguration wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="c2c06-160">SHV configuration is not found.</span></span>

> [!Note]  
> <span data-ttu-id="c2c06-161">Unterstützt in Windows 7 oder höher.</span><span class="sxs-lookup"><span data-stu-id="c2c06-161">Supported in Windows 7 or later.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="c2c06-162"><span id="NAP_E_SHV_TIMEOUT"></span><span id="nap_e_shv_timeout"></span>**NAP- \_ E- \_ SHV- \_ Timeout**</span><span class="sxs-lookup"><span data-stu-id="c2c06-162"><span id="NAP_E_SHV_TIMEOUT"></span><span id="nap_e_shv_timeout"></span>**NAP\_E\_SHV\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2c06-163">\_HRESULT- \_ typedef \_ (0x80270013l)</span><span class="sxs-lookup"><span data-stu-id="c2c06-163">\_HRESULT\_TYPEDEF\_(0x80270013L)</span></span>
</dt> <dt>



<span data-ttu-id="c2c06-164">Bei SHV ist für die Anforderung ein Timeout aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="c2c06-164">SHV timed out on the request.</span></span>

> [!Note]  
> <span data-ttu-id="c2c06-165">Unterstützt in Windows 7 oder höher.</span><span class="sxs-lookup"><span data-stu-id="c2c06-165">Supported in Windows 7 or later.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c2c06-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2c06-166">Requirements</span></span>



| <span data-ttu-id="c2c06-167">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2c06-167">Requirement</span></span> | <span data-ttu-id="c2c06-168">Wert</span><span class="sxs-lookup"><span data-stu-id="c2c06-168">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c2c06-169">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2c06-169">Minimum supported client</span></span><br/> | <span data-ttu-id="c2c06-170">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2c06-170">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c2c06-171">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2c06-171">Minimum supported server</span></span><br/> | <span data-ttu-id="c2c06-172">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2c06-172">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c2c06-173">Header</span><span class="sxs-lookup"><span data-stu-id="c2c06-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2c06-174"><dt>Winerror. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2c06-174"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2c06-175">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2c06-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2c06-176">**NAP-Konstanten**</span><span class="sxs-lookup"><span data-stu-id="c2c06-176">**NAP Constants**</span></span>](nap-constants.md)
</dt> </dl>

 

 





