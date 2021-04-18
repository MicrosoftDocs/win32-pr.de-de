---
title: MPSTATUS_FLAG-Enumeration (mpclient. h)
description: Mögliche allgemeine Bitflags für den Produktstatus.
ms.assetid: BF2E6506-E76A-4785-8E91-99937B413548
keywords:
- MPSTATUS_FLAG-Enumerationsfunktionen der Legacy-Windows-Umgebung
- PMPSTATUS_FLAG enumerationszeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPSTATUS_FLAG
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c7175980c09c63938be04626091c31b53335756
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340583"
---
# <a name="mpstatus_flag-enumeration"></a><span data-ttu-id="d4fa3-105">Mpstatusflag- \_ Enumeration</span><span class="sxs-lookup"><span data-stu-id="d4fa3-105">MPSTATUS\_FLAG enumeration</span></span>

<span data-ttu-id="d4fa3-106">Mögliche allgemeine Bitflags für den Produktstatus.</span><span class="sxs-lookup"><span data-stu-id="d4fa3-106">Possible overall product status bit flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4fa3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4fa3-107">Syntax</span></span>


```C++
typedef enum tagMPSTATUS_FLAG { 
  MP_STATUS_FLAG_NONE                           = 0,
  MP_STATUS_FLAG_SERVICE_UNAVAILABLE            = 1 << 0,
  MP_STATUS_FLAG_MPENGINE_UNAVAILABLE           = 1 << 1,
  MP_STATUS_FLAG_THREAT_FULLSCAN_REQUIRED       = 1 << 2,
  MP_STATUS_FLAG_THREAT_REBOOT_REQUIRED         = 1 << 3,
  MP_STATUS_FLAG_THREAT_MANUAL_STEPS_REQUIRED   = 1 << 4,
  MP_STATUS_FLAG_DUE_AV_SIGNATURE               = 1 << 5,
  MP_STATUS_FLAG_DUE_AS_SIGNATURE               = 1 << 6,
  MP_STATUS_FLAG_DUE_QUICK_SCAN                 = 1 << 7,
  MP_STATUS_FLAG_DUE_FULL_SCAN                  = 1 << 8,
  MP_STATUS_FLAG_INPROGRESS_SYSTEM_SCAN         = 1 << 9,
  MP_STATUS_FLAG_INPROGRESS_ROUTINE_CLEANING    = 1 << 10,
  MP_STATUS_FLAG_DUE_SAMPLES                    = 1 << 11,
  MP_STATUS_FLAG_EVALUATION_MODE                = 1 << 12,
  MP_STATUS_FLAG_NONGENUINE                     = 1 << 13,
  MP_STATUS_FLAG_PRODUCT_EXPIRED                = 1 << 14,
  MP_STATUS_FLAG_THREAT_CALLISTO_REQUIRED       = 1 << 15,
  MP_STATUS_FLAG_SERVICE_ON_SYSTEM_SHUTDOWN     = 1 << 16,
  MP_STATUS_FLAG_SERVICE_CRITICAL_FAILURE       = 1 << 17,
  MP_STATUS_FLAG_SERVICE_NON_CRITICAL_FAILURE   = 1 << 18,
  MP_STATUS_FLAG_HEALTH_INITIALIZED             = 1 << 19,
  MP_STATUS_FLAG_DUE_PLATFORM_UPDATE            = 1 << 20,
  MP_STATUS_FLAG_INPROGRESS_PLATFORM_UPDATE     = 1 << 21,
  MP_STATUS_FLAG_PLATFORM_ABOUT_TO_BE_OUTDATED  = 1 << 22,
  MP_STATUS_FLAG_END_OF_LIFE                    = 1 << 23,
  MP_STATUS_FLAG_MAX                            = 1 << 23,
  MP_STATUS_FLAG_ALL                            = (1 << 24)-1
} MPSTATUS_FLAG, *PMPSTATUS_FLAG;
```



## <a name="constants"></a><span data-ttu-id="d4fa3-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="d4fa3-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d4fa3-109"><span id="MP_STATUS_FLAG_NONE"></span><span id="mp_status_flag_none"></span>**MP \_ - \_ Statusflag \_ None**</span><span class="sxs-lookup"><span data-stu-id="d4fa3-109"><span id="MP_STATUS_FLAG_NONE"></span><span id="mp_status_flag_none"></span>**MP\_STATUS\_FLAG\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="d4fa3-110">Es wurden keine Statusflags festgelegt (nicht initialisierter Zustand).</span><span class="sxs-lookup"><span data-stu-id="d4fa3-110">No status flags set (non-initialized state).</span></span>

</dd> <dt>

<span data-ttu-id="d4fa3-111"><span id="MP_STATUS_FLAG_SERVICE_UNAVAILABLE"></span><span id="mp_status_flag_service_unavailable"></span>**MP \_ - \_ statusflagdienst nicht \_ \_ verfügbar**</span><span class="sxs-lookup"><span data-stu-id="d4fa3-111"><span id="MP_STATUS_FLAG_SERVICE_UNAVAILABLE"></span><span id="mp_status_flag_service_unavailable"></span>**MP\_STATUS\_FLAG\_SERVICE\_UNAVAILABLE**</span></span>
</dt> <dd>

<span data-ttu-id="d4fa3-112">Der Dienst wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4fa3-112">Service not running.</span></span>

</dd> <dt>

<span data-ttu-id="d4fa3-113"><span id="MP_STATUS_FLAG_MPENGINE_UNAVAILABLE"></span><span id="mp_status_flag_mpengine_unavailable"></span>**MP- \_ Status \_ Flag " \_ mpengine nicht \_ verfügbar"**</span><span class="sxs-lookup"><span data-stu-id="d4fa3-113"><span id="MP_STATUS_FLAG_MPENGINE_UNAVAILABLE"></span><span id="mp_status_flag_mpengine_unavailable"></span>**MP\_STATUS\_FLAG\_MPENGINE\_UNAVAILABLE**</span></span>
</dt> <dd>

<span data-ttu-id="d4fa3-114">Der Dienst wurde ohne Malware Schutz Modul gestartet.</span><span class="sxs-lookup"><span data-stu-id="d4fa3-114">Service started without any malware protection engine.</span></span>

</dd> <dt>

<span data-ttu-id="d4fa3-115"><span id="MP_STATUS_FLAG_THREAT_FULLSCAN_REQUIRED"></span><span id="mp_status_flag_threat_fullscan_required"></span>**MP \_ - \_ Statusflag \_ Threat \_ FULLSCAN \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d4fa3-115"><span id="MP_STATUS_FLAG_THREAT_FULLSCAN_REQUIRED"></span><span id="mp_status_flag_threat_fullscan_required"></span>**MP\_STATUS\_FLAG\_THREAT\_FULLSCAN\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="d4fa3-116">Ausstehende vollständige Überprüfung aufgrund von Bedrohungs Aktion.</span><span class="sxs-lookup"><span data-stu-id="d4fa3-116">Pending full scan due to threat action.</span></span>

</dd> <dt>

<span data-ttu-id="d4fa3-117"><span id="MP_STATUS_FLAG_THREAT_REBOOT_REQUIRED"></span><span id="mp_status_flag_threat_reboot_required"></span>**MP \_ - \_ Statusflag für \_ Bedrohungs \_ Neustart \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d4fa3-117"><span id="MP_STATUS_FLAG_THREAT_REBOOT_REQUIRED"></span><span id="mp_status_flag_threat_reboot_required"></span>**MP\_STATUS\_FLAG\_THREAT\_REBOOT\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="d4fa3-118">Neustart aufgrund einer Bedrohungs Aktion steht aus.</span><span class="sxs-lookup"><span data-stu-id="d4fa3-118">Pending reboot due to threat action.</span></span>

</dd> <dt>

<span data-ttu-id="d4fa3-119"><span id="MP_STATUS_FLAG_THREAT_MANUAL_STEPS_REQUIRED"></span><span id="mp_status_flag_threat_manual_steps_required"></span>**MP \_ - \_ Statusflag, \_ \_ Manuelle \_ Schritte \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d4fa3-119"><span id="MP_STATUS_FLAG_THREAT_MANUAL_STEPS_REQUIRED"></span><span id="mp_status_flag_threat_manual_steps_required"></span>**MP\_STATUS\_FLAG\_THREAT\_MANUAL\_STEPS\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="d4fa3-120">Ausstehende manuelle Schritte aufgrund von Bedrohungs Aktionen.</span><span class="sxs-lookup"><span data-stu-id="d4fa3-120">Pending manual steps due to threat action.</span></span>

</dd> <dt>

<span data-ttu-id="d4fa3-121"><span id="MP_STATUS_FLAG_DUE_AV_SIGNATURE"></span><span id="mp_status_flag_due_av_signature"></span>**MP \_ - \_ Statusflag \_ aufgrund der \_ AV- \_ Signatur**</span><span class="sxs-lookup"><span data-stu-id="d4fa3-121"><span id="MP_STATUS_FLAG_DUE_AV_SIGNATURE"></span><span id="mp_status_flag_due_av_signature"></span>**MP\_STATUS\_FLAG\_DUE\_AV\_SIGNATURE**</span></span>
</dt> <dd>

<span data-ttu-id="d4fa3-122">Antivirensignaturen sind veraltet.</span><span class="sxs-lookup"><span data-stu-id="d4fa3-122">Antivirus signatures out of date.</span></span>

</dd> <dt>

<span data-ttu-id="d4fa3-123"><span id="MP_STATUS_FLAG_DUE_AS_SIGNATURE"></span><span id="mp_status_flag_due_as_signature"></span>**MP \_ - \_ Statusflag \_ aufgrund der \_ \_ Signatur**</span><span class="sxs-lookup"><span data-stu-id="d4fa3-123"><span id="MP_STATUS_FLAG_DUE_AS_SIGNATURE"></span><span id="mp_status_flag_due_as_signature"></span>**MP\_STATUS\_FLAG\_DUE\_AS\_SIGNATURE**</span></span>
</dt> <dd>

<span data-ttu-id="d4fa3-124">Antispywaresignaturen sind veraltet.</span><span class="sxs-lookup"><span data-stu-id="d4fa3-124">Antispyware signatures out of date.</span></span>

</dd> <dt>

<span data-ttu-id="d4fa3-125"><span id="MP_STATUS_FLAG_DUE_QUICK_SCAN"></span><span id="mp_status_flag_due_quick_scan"></span>**MP \_ - \_ Statusflag \_ aufgrund der \_ schnell \_ Überprüfung**</span><span class="sxs-lookup"><span data-stu-id="d4fa3-125"><span id="MP_STATUS_FLAG_DUE_QUICK_SCAN"></span><span id="mp_status_flag_due_quick_scan"></span>**MP\_STATUS\_FLAG\_DUE\_QUICK\_SCAN**</span></span>
</dt> <dd>

<span data-ttu-id="d4fa3-126">Für einen angegebenen Zeitraum ist keine schnell Überprüfung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="d4fa3-126">No quick scan has happened for a specified period.</span></span>

</dd> <dt>

<span data-ttu-id="d4fa3-127"><span id="MP_STATUS_FLAG_DUE_FULL_SCAN"></span><span id="mp_status_flag_due_full_scan"></span>**MP \_ - \_ Statusflag \_ durch \_ vollständige \_ Überprüfung**</span><span class="sxs-lookup"><span data-stu-id="d4fa3-127"><span id="MP_STATUS_FLAG_DUE_FULL_SCAN"></span><span id="mp_status_flag_due_full_scan"></span>**MP\_STATUS\_FLAG\_DUE\_FULL\_SCAN**</span></span>
</dt> <dd>

<span data-ttu-id="d4fa3-128">in einem angegebenen Zeitraum ist keine vollständige Überprüfung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="d4fa3-128">no full scan has happened for a specified period</span></span>

</dd> <dt>

<span data-ttu-id="d4fa3-129"><span id="MP_STATUS_FLAG_INPROGRESS_SYSTEM_SCAN"></span><span id="mp_status_flag_inprogress_system_scan"></span>**MP \_ - \_ Statusflag " \_ InProgress \_ System \_ Scan"**</span><span class="sxs-lookup"><span data-stu-id="d4fa3-129"><span id="MP_STATUS_FLAG_INPROGRESS_SYSTEM_SCAN"></span><span id="mp_status_flag_inprogress_system_scan"></span>**MP\_STATUS\_FLAG\_INPROGRESS\_SYSTEM\_SCAN**</span></span>
</dt> <dd>

<span data-ttu-id="d4fa3-130">Vom System initiierte Überprüfung wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4fa3-130">System-initiated scan in progress.</span></span>

</dd> <dt>

<span data-ttu-id="d4fa3-131"><span id="MP_STATUS_FLAG_INPROGRESS_ROUTINE_CLEANING"></span><span id="mp_status_flag_inprogress_routine_cleaning"></span>**MP \_ - \_ Statusflag " \_ InProgress- \_ Routine \_ Reinigung"**</span><span class="sxs-lookup"><span data-stu-id="d4fa3-131"><span id="MP_STATUS_FLAG_INPROGRESS_ROUTINE_CLEANING"></span><span id="mp_status_flag_inprogress_routine_cleaning"></span>**MP\_STATUS\_FLAG\_INPROGRESS\_ROUTINE\_CLEANING**</span></span>
</dt> <dd>

<span data-ttu-id="d4fa3-132">Vom System initiierte Bereinigung wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4fa3-132">System-initiated clean in progress.</span></span>

</dd> <dt>

<span data-ttu-id="d4fa3-133"><span id="MP_STATUS_FLAG_DUE_SAMPLES"></span><span id="mp_status_flag_due_samples"></span>**Verwaltungs Beispiele für MP- \_ \_ Statusflags \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d4fa3-133"><span id="MP_STATUS_FLAG_DUE_SAMPLES"></span><span id="mp_status_flag_due_samples"></span>**MP\_STATUS\_FLAG\_DUE\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="d4fa3-134">Es sind Beispiele für ausstehende Übermittlung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d4fa3-134">There are samples pending submission.</span></span>

</dd> <dt>

<span data-ttu-id="d4fa3-135"><span id="MP_STATUS_FLAG_EVALUATION_MODE"></span><span id="mp_status_flag_evaluation_mode"></span>**Bewertungsmodus für MP- \_ \_ Statusflag \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d4fa3-135"><span id="MP_STATUS_FLAG_EVALUATION_MODE"></span><span id="mp_status_flag_evaluation_mode"></span>**MP\_STATUS\_FLAG\_EVALUATION\_MODE**</span></span>
</dt> <dd>

<span data-ttu-id="d4fa3-136">Das Produkt wird im Auswertungsmodus ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4fa3-136">Product is running in evaluation mode.</span></span>

</dd> <dt>

<span data-ttu-id="d4fa3-137"><span id="MP_STATUS_FLAG_NONGENUINE"></span><span id="mp_status_flag_nongenuine"></span>**MP \_ - \_ Statusflag \_ nicht Original**</span><span class="sxs-lookup"><span data-stu-id="d4fa3-137"><span id="MP_STATUS_FLAG_NONGENUINE"></span><span id="mp_status_flag_nongenuine"></span>**MP\_STATUS\_FLAG\_NONGENUINE**</span></span>
</dt> <dd>

<span data-ttu-id="d4fa3-138">Das Produkt wird im nicht Original-Windows-Modus ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4fa3-138">Product is running in non-genuine Windows mode.</span></span>

</dd> <dt>

<span data-ttu-id="d4fa3-139"><span id="MP_STATUS_FLAG_PRODUCT_EXPIRED"></span><span id="mp_status_flag_product_expired"></span>**MP \_ - \_ Statusflag ist \_ \_ abgelaufen.**</span><span class="sxs-lookup"><span data-stu-id="d4fa3-139"><span id="MP_STATUS_FLAG_PRODUCT_EXPIRED"></span><span id="mp_status_flag_product_expired"></span>**MP\_STATUS\_FLAG\_PRODUCT\_EXPIRED**</span></span>
</dt> <dd>

<span data-ttu-id="d4fa3-140">Das Produkt ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="d4fa3-140">Product expired.</span></span>

</dd> <dt>

<span data-ttu-id="d4fa3-141"><span id="MP_STATUS_FLAG_THREAT_CALLISTO_REQUIRED"></span><span id="mp_status_flag_threat_callisto_required"></span>**MP \_ - \_ Statusflag \_ Threat \_ Callisto \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d4fa3-141"><span id="MP_STATUS_FLAG_THREAT_CALLISTO_REQUIRED"></span><span id="mp_status_flag_threat_callisto_required"></span>**MP\_STATUS\_FLAG\_THREAT\_CALLISTO\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="d4fa3-142">Callisto-Offline Überprüfung ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d4fa3-142">Callisto off-line scan required.</span></span>

</dd> <dt>

<span data-ttu-id="d4fa3-143"><span id="MP_STATUS_FLAG_SERVICE_ON_SYSTEM_SHUTDOWN"></span><span id="mp_status_flag_service_on_system_shutdown"></span>**MP \_ - \_ Statusflag- \_ Dienst \_ beim Herunterfahren des \_ Systems \_**</span><span class="sxs-lookup"><span data-stu-id="d4fa3-143"><span id="MP_STATUS_FLAG_SERVICE_ON_SYSTEM_SHUTDOWN"></span><span id="mp_status_flag_service_on_system_shutdown"></span>**MP\_STATUS\_FLAG\_SERVICE\_ON\_SYSTEM\_SHUTDOWN**</span></span>
</dt> <dd>

<span data-ttu-id="d4fa3-144">Der Dienst wird im Rahmen des herunter Fahrens des Systems heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="d4fa3-144">Service is shutting down as part of system shutdown.</span></span>

</dd> <dt>

<span data-ttu-id="d4fa3-145"><span id="MP_STATUS_FLAG_SERVICE_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_critical_failure"></span>**kritischer Fehler des MP- \_ \_ Statusflags \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d4fa3-145"><span id="MP_STATUS_FLAG_SERVICE_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_critical_failure"></span>**MP\_STATUS\_FLAG\_SERVICE\_CRITICAL\_FAILURE**</span></span>
</dt> <dd>

<span data-ttu-id="d4fa3-146">Fehler bei der Bedrohungs Behebung.</span><span class="sxs-lookup"><span data-stu-id="d4fa3-146">Threat remediation failed critically.</span></span>

</dd> <dt>

<span data-ttu-id="d4fa3-147"><span id="MP_STATUS_FLAG_SERVICE_NON_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_non_critical_failure"></span>**MP \_ - \_ Statusflag- \_ Dienst \_ nicht schwer \_ wiegender \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="d4fa3-147"><span id="MP_STATUS_FLAG_SERVICE_NON_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_non_critical_failure"></span>**MP\_STATUS\_FLAG\_SERVICE\_NON\_CRITICAL\_FAILURE**</span></span>
</dt> <dd>

<span data-ttu-id="d4fa3-148">Die Bedrohungs Behebung ist nicht kritisch.</span><span class="sxs-lookup"><span data-stu-id="d4fa3-148">Threat remediation failed non-critically.</span></span>

</dd> <dt>

<span data-ttu-id="d4fa3-149"><span id="MP_STATUS_FLAG_HEALTH_INITIALIZED"></span><span id="mp_status_flag_health_initialized"></span>**Status des MP- \_ \_ Statusflags \_ \_ Initialisiert**</span><span class="sxs-lookup"><span data-stu-id="d4fa3-149"><span id="MP_STATUS_FLAG_HEALTH_INITIALIZED"></span><span id="mp_status_flag_health_initialized"></span>**MP\_STATUS\_FLAG\_HEALTH\_INITIALIZED**</span></span>
</dt> <dd>

<span data-ttu-id="d4fa3-150">Es wurden keine Statusflags festgelegt (wohl initialisierter Zustand).</span><span class="sxs-lookup"><span data-stu-id="d4fa3-150">No status flags set (well-initialized state).</span></span>

</dd> <dt>

<span data-ttu-id="d4fa3-151"><span id="MP_STATUS_FLAG_DUE_PLATFORM_UPDATE"></span><span id="mp_status_flag_due_platform_update"></span>**MP \_ - \_ Statusflag \_ aufgrund der \_ Platt Form \_ Aktualisierung**</span><span class="sxs-lookup"><span data-stu-id="d4fa3-151"><span id="MP_STATUS_FLAG_DUE_PLATFORM_UPDATE"></span><span id="mp_status_flag_due_platform_update"></span>**MP\_STATUS\_FLAG\_DUE\_PLATFORM\_UPDATE**</span></span>
</dt> <dd>

<span data-ttu-id="d4fa3-152">Die Plattform ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="d4fa3-152">The platform is out of date.</span></span>

</dd> <dt>

<span data-ttu-id="d4fa3-153"><span id="MP_STATUS_FLAG_INPROGRESS_PLATFORM_UPDATE"></span><span id="mp_status_flag_inprogress_platform_update"></span>**MP \_ - \_ Statusflag " \_ InProgress \_ Platform \_ Update"**</span><span class="sxs-lookup"><span data-stu-id="d4fa3-153"><span id="MP_STATUS_FLAG_INPROGRESS_PLATFORM_UPDATE"></span><span id="mp_status_flag_inprogress_platform_update"></span>**MP\_STATUS\_FLAG\_INPROGRESS\_PLATFORM\_UPDATE**</span></span>
</dt> <dd>

<span data-ttu-id="d4fa3-154">Das Platt Form Update wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4fa3-154">Platform update is in progress.</span></span>

</dd> <dt>

<span data-ttu-id="d4fa3-155"><span id="MP_STATUS_FLAG_PLATFORM_ABOUT_TO_BE_OUTDATED"></span><span id="mp_status_flag_platform_about_to_be_outdated"></span>**MP \_ - \_ Statusflag- \_ Plattform ist \_ \_ \_ \_ veraltet**</span><span class="sxs-lookup"><span data-stu-id="d4fa3-155"><span id="MP_STATUS_FLAG_PLATFORM_ABOUT_TO_BE_OUTDATED"></span><span id="mp_status_flag_platform_about_to_be_outdated"></span>**MP\_STATUS\_FLAG\_PLATFORM\_ABOUT\_TO\_BE\_OUTDATED**</span></span>
</dt> <dd>

<span data-ttu-id="d4fa3-156">Die Plattform ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="d4fa3-156">The platform is about to be outdated</span></span>

</dd> <dt>

<span data-ttu-id="d4fa3-157"><span id="MP_STATUS_FLAG_END_OF_LIFE"></span><span id="mp_status_flag_end_of_life"></span>**MP \_ - \_ Statusflag- \_ Ende \_ des \_ Lebenszyklus**</span><span class="sxs-lookup"><span data-stu-id="d4fa3-157"><span id="MP_STATUS_FLAG_END_OF_LIFE"></span><span id="mp_status_flag_end_of_life"></span>**MP\_STATUS\_FLAG\_END\_OF\_LIFE**</span></span>
</dt> <dd>

<span data-ttu-id="d4fa3-158">Die Signatur oder das Ende der Plattform ist abgelaufen oder steht aus.</span><span class="sxs-lookup"><span data-stu-id="d4fa3-158">The signature or platform end of life is past or is pending.</span></span>

</dd> <dt>

<span data-ttu-id="d4fa3-159"><span id="MP_STATUS_FLAG_MAX"></span><span id="mp_status_flag_max"></span>**MP \_ - \_ Statusflag \_ Max**</span><span class="sxs-lookup"><span data-stu-id="d4fa3-159"><span id="MP_STATUS_FLAG_MAX"></span><span id="mp_status_flag_max"></span>**MP\_STATUS\_FLAG\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="d4fa3-160">Maximal gültiges Flag.</span><span class="sxs-lookup"><span data-stu-id="d4fa3-160">Maximum valid flag.</span></span>

</dd> <dt>

<span data-ttu-id="d4fa3-161"><span id="MP_STATUS_FLAG_ALL"></span><span id="mp_status_flag_all"></span>**MP \_ - \_ Statusflag \_ alle**</span><span class="sxs-lookup"><span data-stu-id="d4fa3-161"><span id="MP_STATUS_FLAG_ALL"></span><span id="mp_status_flag_all"></span>**MP\_STATUS\_FLAG\_ALL**</span></span>
</dt> <dd>

<span data-ttu-id="d4fa3-162">Maximal möglicher Wert.</span><span class="sxs-lookup"><span data-stu-id="d4fa3-162">Maximum value possible.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d4fa3-163">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4fa3-163">Requirements</span></span>



| <span data-ttu-id="d4fa3-164">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4fa3-164">Requirement</span></span> | <span data-ttu-id="d4fa3-165">Wert</span><span class="sxs-lookup"><span data-stu-id="d4fa3-165">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d4fa3-166">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d4fa3-166">Minimum supported client</span></span><br/> | <span data-ttu-id="d4fa3-167">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d4fa3-167">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d4fa3-168">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d4fa3-168">Minimum supported server</span></span><br/> | <span data-ttu-id="d4fa3-169">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d4fa3-169">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d4fa3-170">Header</span><span class="sxs-lookup"><span data-stu-id="d4fa3-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4fa3-171"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4fa3-171"><dt>MpClient.h</dt></span></span> </dl> |



 

 





