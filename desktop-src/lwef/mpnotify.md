---
title: Mpnotify-Enumeration (mpclient. h)
description: Mögliche Rückruf Benachrichtigungen.
ms.assetid: CCD0CD89-2C6E-453F-9437-E6ED87AD9F29
keywords:
- Mpnotify-Enumeration Legacy-Windows-Umgebungs Features
- Pmpnotify-enumerationszeiger ältere Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPNOTIFY
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afa0eeb6cb1d610f28cc82f578617f7bd71cf886
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342223"
---
# <a name="mpnotify-enumeration"></a><span data-ttu-id="f29d1-105">Mpnotify-Enumeration</span><span class="sxs-lookup"><span data-stu-id="f29d1-105">MPNOTIFY enumeration</span></span>

<span data-ttu-id="f29d1-106">Mögliche Rückruf Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="f29d1-106">Possible callback notifications.</span></span>

## <a name="syntax"></a><span data-ttu-id="f29d1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f29d1-107">Syntax</span></span>


```C++
typedef enum tagMPNOTIFY { 
  MPNOTIFY_NONE,
  MPNOTIFY_CALL_START,
  MPNOTIFY_CALL_COMPLETE,
  MPNOTIFY_INTERNAL_FAILURE,
  MPNOTIFY_STATUS_SERVICE_START,
  MPNOTIFY_STATUS_SERVICE_RUNNING,
  MPNOTIFY_STATUS_SERVICE_STOP,
  MPNOTIFY_STATUS_COMPONENT,
  MPNOTIFY_STATUS_CHANGE,
  MPNOTIFY_STATUS_COMPONENT_CONFIGURATION,
  MPNOTIFY_STATUS_EXPIRATION_CHANGE,
  MPNOTIFY_STATUS_OFFLINE_SCAN_CHANGE,
  MPNOTIFY_SCAN_START,
  MPNOTIFY_SCAN_PAUSED,
  MPNOTIFY_SCAN_RESUMED,
  MPNOTIFY_SCAN_CANCEL,
  MPNOTIFY_SCAN_COMPLETE,
  MPNOTIFY_SCAN_PROGRESS,
  MPNOTIFY_SCAN_ERROR,
  MPNOTIFY_SCAN_INFECTED,
  MPNOTIFY_SCAN_MEMORYSTART,
  MPNOTIFY_SCAN_MEMORYCOMPLETE,
  MPNOTIFY_SCAN_SFC_BUILD_START,
  MPNOTIFY_SCAN_SFC_BUILD_COMPLETE,
  MPNOTIFY_SCAN_FASTPATH_START,
  MPNOTIFY_SCAN_FASTPATH_COMPLETE,
  MPNOTIFY_SCAN_FASTPATH_PROGRESS,
  MPNOTIFY_CLEAN_START,
  MPNOTIFY_CLEAN_COMPLETE,
  MPNOTIFY_CLEAN_RESTOREPOINT_START,
  MPNOTIFY_CLEAN_RESTOREPOINT_SUCCEEDED,
  MPNOTIFY_CLEAN_RESTOREPOINT_FAILED,
  MPNOTIFY_CLEAN_THREAT_START,
  MPNOTIFY_CLEAN_THREAT_SUCCEEDED,
  MPNOTIFY_CLEAN_THREAT_FAILED,
  MPNOTIFY_CLEAN_RESOURCE_SUCCEEDED,
  MPNOTIFY_CLEAN_RESOURCE_FAILED,
  MPNOTIFY_CLEAN_THREAT_COMPLETE,
  MPNOTIFY_PRECHECK_START,
  MPNOTIFY_PRECHECK_COMPLETE,
  MPNOTIFY_PRECHECK_RESOURCE_BLOCKED,
  MPNOTIFY_THREAT_DETECTED,
  MPNOTIFY_THREAT_MODIFIED,
  MPNOTIFY_THREAT_CLEAN_SUCCEEDED,
  MPNOTIFY_THREAT_CLEAN_FAILED,
  MPNOTIFY_THREAT_ABANDONED,
  MPNOTIFY_THREAT_CLEAN_EVENT_START,
  MPNOTIFY_THREAT_CLEAN_EVENT_COMPLETE,
  MPNOTIFY_SIGUPDATE_START,
  MPNOTIFY_SIGUPDATE_SEARCH_START,
  MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE,
  MPNOTIFY_SIGUPDATE_SOFTWARE_UPDATE_AVAILABLE,
  MPNOTIFY_SIGUPDATE_DOWNLOAD_START,
  MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS,
  MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE,
  MPNOTIFY_SIGUPDATE_INSTALL_START,
  MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS,
  MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE,
  MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED,
  MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED,
  MPNOTIFY_SIGUPDATE_COMPLETE,
  MPNOTIFY_SAMPLE_START,
  MPNOTIFY_SAMPLE_COMPLETE,
  MPNOTIFY_SAMPLE_ITEM_START,
  MPNOTIFY_SAMPLE_ITEM_SUCCEEDED,
  MPNOTIFY_SAMPLE_ITEM_FAILED,
  MPNOTIFY_RESERVED_DATA,
  MPNOTIFY_FASTPATH_SIG_ADDED,
  MPNOTIFY_FASTPATH_SIG_REMOVED,
  MPNOTIFY_NIS_PRIVATE,
  MPNOTIFY_HEALTH_CHANGE,
  MPNOTIFY_HEALTH_RECOVERY,
  MPNOTIFY_HEALTH_START,
  MPNOTIFY_ENDOFLIFE_CHANGE,
  MPNOTIFY_MALWARETOAST_DATA
} MPNOTIFY, *PMPNOTIFY;
```



## <a name="constants"></a><span data-ttu-id="f29d1-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="f29d1-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f29d1-109"><span id="MPNOTIFY_NONE"></span><span id="mpnotify_none"></span>**mpnotify \_ None**</span><span class="sxs-lookup"><span data-stu-id="f29d1-109"><span id="MPNOTIFY_NONE"></span><span id="mpnotify_none"></span>**MPNOTIFY\_NONE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f29d1-110"><span id="MPNOTIFY_CALL_START"></span><span id="mpnotify_call_start"></span>**mpnotify- \_ Anrufe \_ starten**</span><span class="sxs-lookup"><span data-stu-id="f29d1-110"><span id="MPNOTIFY_CALL_START"></span><span id="mpnotify_call_start"></span>**MPNOTIFY\_CALL\_START**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-111">Der Benachrichtigungs Rückruf wird gestartet.</span><span class="sxs-lookup"><span data-stu-id="f29d1-111">Notification call start.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-112"><span id="MPNOTIFY_CALL_COMPLETE"></span><span id="mpnotify_call_complete"></span>**mpnotify- \_ Rückruf ist \_ beendet**</span><span class="sxs-lookup"><span data-stu-id="f29d1-112"><span id="MPNOTIFY_CALL_COMPLETE"></span><span id="mpnotify_call_complete"></span>**MPNOTIFY\_CALL\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-113">Der Benachrichtigungs Rückruf wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="f29d1-113">Notification call completed.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-114"><span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span>**Interner mpnotify- \_ \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="f29d1-114"><span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span>**MPNOTIFY\_INTERNAL\_FAILURE**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-115">Allgemeiner interner Fehler.</span><span class="sxs-lookup"><span data-stu-id="f29d1-115">Generic internal failure.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-116"><span id="MPNOTIFY_STATUS_SERVICE_START"></span><span id="mpnotify_status_service_start"></span>**mpnotify- \_ Status \_ Dienst \_ starten**</span><span class="sxs-lookup"><span data-stu-id="f29d1-116"><span id="MPNOTIFY_STATUS_SERVICE_START"></span><span id="mpnotify_status_service_start"></span>**MPNOTIFY\_STATUS\_SERVICE\_START**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-117">Der Malware Schutzdienst wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="f29d1-117">Malware protection service has started.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-118"><span id="MPNOTIFY_STATUS_SERVICE_RUNNING"></span><span id="mpnotify_status_service_running"></span>**mpnotify- \_ Status \_ Dienst wird \_ ausgeführt**</span><span class="sxs-lookup"><span data-stu-id="f29d1-118"><span id="MPNOTIFY_STATUS_SERVICE_RUNNING"></span><span id="mpnotify_status_service_running"></span>**MPNOTIFY\_STATUS\_SERVICE\_RUNNING**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-119">Der Malware Schutzdienst wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f29d1-119">Malware protection service is running.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-120"><span id="MPNOTIFY_STATUS_SERVICE_STOP"></span><span id="mpnotify_status_service_stop"></span>**mpnotify- \_ Status \_ Dienst \_ beendet**</span><span class="sxs-lookup"><span data-stu-id="f29d1-120"><span id="MPNOTIFY_STATUS_SERVICE_STOP"></span><span id="mpnotify_status_service_stop"></span>**MPNOTIFY\_STATUS\_SERVICE\_STOP**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-121">Der Malware Schutzdienst wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="f29d1-121">Malware protection service has stopped.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-122"><span id="MPNOTIFY_STATUS_COMPONENT"></span><span id="mpnotify_status_component"></span>**mpnotify- \_ Status \_ Komponente**</span><span class="sxs-lookup"><span data-stu-id="f29d1-122"><span id="MPNOTIFY_STATUS_COMPONENT"></span><span id="mpnotify_status_component"></span>**MPNOTIFY\_STATUS\_COMPONENT**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-123">Bestimmte Komponenten aktivieren/deaktivieren Sie den Status.</span><span class="sxs-lookup"><span data-stu-id="f29d1-123">Particular component enable/disable status.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-124"><span id="MPNOTIFY_STATUS_CHANGE"></span><span id="mpnotify_status_change"></span>**mpnotify- \_ Status \_ Änderung**</span><span class="sxs-lookup"><span data-stu-id="f29d1-124"><span id="MPNOTIFY_STATUS_CHANGE"></span><span id="mpnotify_status_change"></span>**MPNOTIFY\_STATUS\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-125">Der Gesamtprodukt Status hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="f29d1-125">Overall product status has changed.</span></span> <span data-ttu-id="f29d1-126">Rufen Sie [**mpmanagerstatusqueryex**](mpmanagerstatusqueryex.md) auf, um den aktuellen Status abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f29d1-126">Call [**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md) to obtain the current status.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-127"><span id="MPNOTIFY_STATUS_COMPONENT_CONFIGURATION"></span><span id="mpnotify_status_component_configuration"></span>**mpnotify- \_ Status \_ Komponenten \_ Konfiguration**</span><span class="sxs-lookup"><span data-stu-id="f29d1-127"><span id="MPNOTIFY_STATUS_COMPONENT_CONFIGURATION"></span><span id="mpnotify_status_component_configuration"></span>**MPNOTIFY\_STATUS\_COMPONENT\_CONFIGURATION**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-128">Eine bestimmte Komponente hat die Konfiguration geändert.</span><span class="sxs-lookup"><span data-stu-id="f29d1-128">A particular component has changed configuration.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-129"><span id="MPNOTIFY_STATUS_EXPIRATION_CHANGE"></span><span id="mpnotify_status_expiration_change"></span>**mpnotify- \_ Status \_ Ablauf \_ Änderung**</span><span class="sxs-lookup"><span data-stu-id="f29d1-129"><span id="MPNOTIFY_STATUS_EXPIRATION_CHANGE"></span><span id="mpnotify_status_expiration_change"></span>**MPNOTIFY\_STATUS\_EXPIRATION\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-130">Der Produktablauf Status hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="f29d1-130">Product expiration status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-131"><span id="MPNOTIFY_STATUS_OFFLINE_SCAN_CHANGE"></span><span id="mpnotify_status_offline_scan_change"></span>**mpnotify- \_ Status- \_ Offline \_ Scan \_ Änderung**</span><span class="sxs-lookup"><span data-stu-id="f29d1-131"><span id="MPNOTIFY_STATUS_OFFLINE_SCAN_CHANGE"></span><span id="mpnotify_status_offline_scan_change"></span>**MPNOTIFY\_STATUS\_OFFLINE\_SCAN\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-132">Der Status der Offline Überprüfung wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="f29d1-132">Offline scan required state changed.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-133"><span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span>**mpnotify- \_ Scan \_ Start**</span><span class="sxs-lookup"><span data-stu-id="f29d1-133"><span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span>**MPNOTIFY\_SCAN\_START**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-134">Scan Vorgang gestartet.</span><span class="sxs-lookup"><span data-stu-id="f29d1-134">Scan started.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-135"><span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span>**mpnotify- \_ Scan \_ angehalten**</span><span class="sxs-lookup"><span data-stu-id="f29d1-135"><span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span>**MPNOTIFY\_SCAN\_PAUSED**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-136">Scan angehalten.</span><span class="sxs-lookup"><span data-stu-id="f29d1-136">Scan paused.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-137"><span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span>**mpnotify-Scan wird fortgesetzt \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f29d1-137"><span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span>**MPNOTIFY\_SCAN\_RESUMED**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-138">Überprüfung fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="f29d1-138">scan resumed.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-139"><span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span>**mpnotify- \_ Scan \_ Abbruch**</span><span class="sxs-lookup"><span data-stu-id="f29d1-139"><span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span>**MPNOTIFY\_SCAN\_CANCEL**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-140">Scan abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="f29d1-140">Scan cancelled.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-141"><span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span>**mpnotify- \_ Scan ist \_ beendet**</span><span class="sxs-lookup"><span data-stu-id="f29d1-141"><span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span>**MPNOTIFY\_SCAN\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-142">Überprüfung abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="f29d1-142">Scan completed.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-143"><span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span>**mpnotify- \_ Scan Status \_**</span><span class="sxs-lookup"><span data-stu-id="f29d1-143"><span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span>**MPNOTIFY\_SCAN\_PROGRESS**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-144">Status Benachrichtigung für die zu überprüfende Ressource.</span><span class="sxs-lookup"><span data-stu-id="f29d1-144">Progress notification for the specific resource being scanned.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-145"><span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span>**mpnotify- \_ Scan \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="f29d1-145"><span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span>**MPNOTIFY\_SCAN\_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-146">Fehler beim Scannen einer bestimmten Ressource.</span><span class="sxs-lookup"><span data-stu-id="f29d1-146">Failure to scan a particular resource.</span></span> <span data-ttu-id="f29d1-147">Der Scan Vorgang wird trotzdem fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="f29d1-147">Scan will still continue.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-148"><span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span>**mpnotify- \_ Scan \_ infiziert**</span><span class="sxs-lookup"><span data-stu-id="f29d1-148"><span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span>**MPNOTIFY\_SCAN\_INFECTED**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-149">Der Scan hat eine infizierte Ressource gefunden.</span><span class="sxs-lookup"><span data-stu-id="f29d1-149">Scan found an infected resource.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-150"><span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span>**mpnotify- \_ Scan \_ memorystart**</span><span class="sxs-lookup"><span data-stu-id="f29d1-150"><span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span>**MPNOTIFY\_SCAN\_MEMORYSTART**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-151">Der Scan Vorgang zum Benachrichtigen des Speicher Scan Teils der Systemüberprüfung wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="f29d1-151">Scan progress to notify memory scan portion of the system scan has started.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-152"><span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span>**mpnotify- \_ Scan \_ memorycomplete**</span><span class="sxs-lookup"><span data-stu-id="f29d1-152"><span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span>**MPNOTIFY\_SCAN\_MEMORYCOMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-153">Der Scan Vorgang zum Benachrichtigen des Speicher Scan Teils der Systemüberprüfung wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="f29d1-153">Scan progress to notify memory scan portion of the system scan has completed.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-154"><span id="MPNOTIFY_SCAN_SFC_BUILD_START"></span><span id="mpnotify_scan_sfc_build_start"></span>**mpnotify- \_ Scan für \_ sfc- \_ Build \_ starten**</span><span class="sxs-lookup"><span data-stu-id="f29d1-154"><span id="MPNOTIFY_SCAN_SFC_BUILD_START"></span><span id="mpnotify_scan_sfc_build_start"></span>**MPNOTIFY\_SCAN\_SFC\_BUILD\_START**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-155">Der Überprüfungs Fortschritt zum Benachrichtigen des SFC-buildteils wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="f29d1-155">Scan progress to notify sfc build portion has started.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-156"><span id="MPNOTIFY_SCAN_SFC_BUILD_COMPLETE"></span><span id="mpnotify_scan_sfc_build_complete"></span>**mpnotify- \_ Scan, \_ sfc-Build wurde \_ \_ beendet**</span><span class="sxs-lookup"><span data-stu-id="f29d1-156"><span id="MPNOTIFY_SCAN_SFC_BUILD_COMPLETE"></span><span id="mpnotify_scan_sfc_build_complete"></span>**MPNOTIFY\_SCAN\_SFC\_BUILD\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-157">Der Scan Vorgang zum Benachrichtigen des SFC-buildteils wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="f29d1-157">Scan progress to notify sfc build portion has completed.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-158"><span id="MPNOTIFY_SCAN_FASTPATH_START"></span><span id="mpnotify_scan_fastpath_start"></span>**mpnotify-Überprüfung \_ \_ FastPath \_ starten**</span><span class="sxs-lookup"><span data-stu-id="f29d1-158"><span id="MPNOTIFY_SCAN_FASTPATH_START"></span><span id="mpnotify_scan_fastpath_start"></span>**MPNOTIFY\_SCAN\_FASTPATH\_START**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-159">Der Scan Vorgang von FastPath SpyNet wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="f29d1-159">Scan fastpath spynet has begun.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-160"><span id="MPNOTIFY_SCAN_FASTPATH_COMPLETE"></span><span id="mpnotify_scan_fastpath_complete"></span>**mpnotify- \_ Scan für \_ FastPath ist \_ beendet**</span><span class="sxs-lookup"><span data-stu-id="f29d1-160"><span id="MPNOTIFY_SCAN_FASTPATH_COMPLETE"></span><span id="mpnotify_scan_fastpath_complete"></span>**MPNOTIFY\_SCAN\_FASTPATH\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-161">Das Überprüfen von FastPath SpyNet wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="f29d1-161">Scan fastpath spynet has ended.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-162"><span id="MPNOTIFY_SCAN_FASTPATH_PROGRESS"></span><span id="mpnotify_scan_fastpath_progress"></span>**mpnotify-Vorgang zum durch \_ Suchen von \_ FastPath \_**</span><span class="sxs-lookup"><span data-stu-id="f29d1-162"><span id="MPNOTIFY_SCAN_FASTPATH_PROGRESS"></span><span id="mpnotify_scan_fastpath_progress"></span>**MPNOTIFY\_SCAN\_FASTPATH\_PROGRESS**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-163">Status Benachrichtigung für FastPath-repper, intern verwendet und in den **mpnotify- \_ Scan \_** Status für extern konvertiert.</span><span class="sxs-lookup"><span data-stu-id="f29d1-163">Progress notification for fastpath rescans, used internally and converted to **MPNOTIFY\_SCAN\_PROGRESS** for external.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-164"><span id="MPNOTIFY_CLEAN_START"></span><span id="mpnotify_clean_start"></span>**Löschen von mpnotify- \_ Bereinigung \_**</span><span class="sxs-lookup"><span data-stu-id="f29d1-164"><span id="MPNOTIFY_CLEAN_START"></span><span id="mpnotify_clean_start"></span>**MPNOTIFY\_CLEAN\_START**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-165">Reinigung wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="f29d1-165">Cleaning started.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-166"><span id="MPNOTIFY_CLEAN_COMPLETE"></span><span id="mpnotify_clean_complete"></span>**Löschen von mpnotify- \_ Bereinigung \_**</span><span class="sxs-lookup"><span data-stu-id="f29d1-166"><span id="MPNOTIFY_CLEAN_COMPLETE"></span><span id="mpnotify_clean_complete"></span>**MPNOTIFY\_CLEAN\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-167">Reinigung abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="f29d1-167">Cleaning completed.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-168"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_START"></span><span id="mpnotify_clean_restorepoint_start"></span>**mpnotify \_ Clean \_ RestorePoint \_ Start**</span><span class="sxs-lookup"><span data-stu-id="f29d1-168"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_START"></span><span id="mpnotify_clean_restorepoint_start"></span>**MPNOTIFY\_CLEAN\_RESTOREPOINT\_START**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-169">Die Erstellung eines System Wiederherstellungs Punkts wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="f29d1-169">Started to create a system restore point.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-170"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_SUCCEEDED"></span><span id="mpnotify_clean_restorepoint_succeeded"></span>**mpnotify \_ Clean \_ RestorePoint \_ erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="f29d1-170"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_SUCCEEDED"></span><span id="mpnotify_clean_restorepoint_succeeded"></span>**MPNOTIFY\_CLEAN\_RESTOREPOINT\_SUCCEEDED**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-171">Der System Wiederherstellungspunkt wurde erfolgreich erstellt.</span><span class="sxs-lookup"><span data-stu-id="f29d1-171">System restore point successfully created.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-172"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_FAILED"></span><span id="mpnotify_clean_restorepoint_failed"></span>**Fehler beim \_ Bereinigen von Clean \_ RestorePoint. \_**</span><span class="sxs-lookup"><span data-stu-id="f29d1-172"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_FAILED"></span><span id="mpnotify_clean_restorepoint_failed"></span>**MPNOTIFY\_CLEAN\_RESTOREPOINT\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-173">Fehler beim Erstellen des System Wiederherstellungs Punkts.</span><span class="sxs-lookup"><span data-stu-id="f29d1-173">System restore point creation failed.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-174"><span id="MPNOTIFY_CLEAN_THREAT_START"></span><span id="mpnotify_clean_threat_start"></span>**mpnotify \_ Clean \_ Threat \_ Start**</span><span class="sxs-lookup"><span data-stu-id="f29d1-174"><span id="MPNOTIFY_CLEAN_THREAT_START"></span><span id="mpnotify_clean_threat_start"></span>**MPNOTIFY\_CLEAN\_THREAT\_START**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-175">Die Bereinigung wird für eine bestimmte Bedrohung gestartet.</span><span class="sxs-lookup"><span data-stu-id="f29d1-175">Cleaning is started for a particular threat.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-176"><span id="MPNOTIFY_CLEAN_THREAT_SUCCEEDED"></span><span id="mpnotify_clean_threat_succeeded"></span>**mpnotify- \_ Bereinigung \_ \_ erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="f29d1-176"><span id="MPNOTIFY_CLEAN_THREAT_SUCCEEDED"></span><span id="mpnotify_clean_threat_succeeded"></span>**MPNOTIFY\_CLEAN\_THREAT\_SUCCEEDED**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-177">Die Bereinigung ist für eine bestimmte Bedrohung erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f29d1-177">Cleaning is succeeded for a particular threat.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-178"><span id="MPNOTIFY_CLEAN_THREAT_FAILED"></span><span id="mpnotify_clean_threat_failed"></span>**Fehler beim \_ Bereinigen der Bereinigung \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f29d1-178"><span id="MPNOTIFY_CLEAN_THREAT_FAILED"></span><span id="mpnotify_clean_threat_failed"></span>**MPNOTIFY\_CLEAN\_THREAT\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-179">Fehler beim Bereinigen für eine bestimmte Bedrohung.</span><span class="sxs-lookup"><span data-stu-id="f29d1-179">Cleaning has failed for a particular threat.</span></span> <span data-ttu-id="f29d1-180">**Fehler \_ Der Fehlercode "MP- \_ Bedrohung \_ nicht \_ gefunden** " zeigt an, dass die Bedrohung nicht gefunden wurde (und kein Fehler beim Bereinigen aufgetreten ist).</span><span class="sxs-lookup"><span data-stu-id="f29d1-180">**ERROR\_MP\_THREAT\_NOT\_FOUND** error code indicates that the threat was not found (and was not a failure to clean).</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-181"><span id="MPNOTIFY_CLEAN_RESOURCE_SUCCEEDED"></span><span id="mpnotify_clean_resource_succeeded"></span>**mpnotify- \_ Clean- \_ Ressource \_ erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="f29d1-181"><span id="MPNOTIFY_CLEAN_RESOURCE_SUCCEEDED"></span><span id="mpnotify_clean_resource_succeeded"></span>**MPNOTIFY\_CLEAN\_RESOURCE\_SUCCEEDED**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-182">Die Bereinigung für eine bestimmte Ressource war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f29d1-182">Cleaning is succeeded for a particular resource.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-183"><span id="MPNOTIFY_CLEAN_RESOURCE_FAILED"></span><span id="mpnotify_clean_resource_failed"></span>**Fehler beim Löschen der mpnotify- \_ \_ Ressource \_**</span><span class="sxs-lookup"><span data-stu-id="f29d1-183"><span id="MPNOTIFY_CLEAN_RESOURCE_FAILED"></span><span id="mpnotify_clean_resource_failed"></span>**MPNOTIFY\_CLEAN\_RESOURCE\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-184">Fehler beim Bereinigen für eine bestimmte Ressource.</span><span class="sxs-lookup"><span data-stu-id="f29d1-184">Cleaning has failed for a particular resource.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-185"><span id="MPNOTIFY_CLEAN_THREAT_COMPLETE"></span><span id="mpnotify_clean_threat_complete"></span>**mpnotify \_ Clean \_ Threat \_ Complete**</span><span class="sxs-lookup"><span data-stu-id="f29d1-185"><span id="MPNOTIFY_CLEAN_THREAT_COMPLETE"></span><span id="mpnotify_clean_threat_complete"></span>**MPNOTIFY\_CLEAN\_THREAT\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-186">Die Bereinigung wurde für eine bestimmte Bedrohung abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="f29d1-186">Cleaning has completed for a particular threat.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-187"><span id="MPNOTIFY_PRECHECK_START"></span><span id="mpnotify_precheck_start"></span>**mpnotify- \_ vorab Überprüfung \_ starten**</span><span class="sxs-lookup"><span data-stu-id="f29d1-187"><span id="MPNOTIFY_PRECHECK_START"></span><span id="mpnotify_precheck_start"></span>**MPNOTIFY\_PRECHECK\_START**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-188">Clean Vorüberprüfung wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="f29d1-188">Clean precheck started.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-189"><span id="MPNOTIFY_PRECHECK_COMPLETE"></span><span id="mpnotify_precheck_complete"></span>**mpnotify- \_ vorab Überprüfung ist \_ beendet**</span><span class="sxs-lookup"><span data-stu-id="f29d1-189"><span id="MPNOTIFY_PRECHECK_COMPLETE"></span><span id="mpnotify_precheck_complete"></span>**MPNOTIFY\_PRECHECK\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-190">Die Clean-Vorprüfung ist abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="f29d1-190">Clean precheck completed.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-191"><span id="MPNOTIFY_PRECHECK_RESOURCE_BLOCKED"></span><span id="mpnotify_precheck_resource_blocked"></span>**mpnotify- \_ Precheck- \_ Ressource \_ blockiert**</span><span class="sxs-lookup"><span data-stu-id="f29d1-191"><span id="MPNOTIFY_PRECHECK_RESOURCE_BLOCKED"></span><span id="mpnotify_precheck_resource_blocked"></span>**MPNOTIFY\_PRECHECK\_RESOURCE\_BLOCKED**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-192">Clean Vorüberprüfung hat blockierte Ressource erkannt.</span><span class="sxs-lookup"><span data-stu-id="f29d1-192">Clean precheck detected blocked resource.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-193"><span id="MPNOTIFY_THREAT_DETECTED"></span><span id="mpnotify_threat_detected"></span>**mpnotify- \_ Bedrohung \_ erkannt**</span><span class="sxs-lookup"><span data-stu-id="f29d1-193"><span id="MPNOTIFY_THREAT_DETECTED"></span><span id="mpnotify_threat_detected"></span>**MPNOTIFY\_THREAT\_DETECTED**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-194">Neue Bedrohung im System erkannt.</span><span class="sxs-lookup"><span data-stu-id="f29d1-194">New threat detected in system.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-195"><span id="MPNOTIFY_THREAT_MODIFIED"></span><span id="mpnotify_threat_modified"></span>**mpnotify- \_ Bedrohung \_ geändert**</span><span class="sxs-lookup"><span data-stu-id="f29d1-195"><span id="MPNOTIFY_THREAT_MODIFIED"></span><span id="mpnotify_threat_modified"></span>**MPNOTIFY\_THREAT\_MODIFIED**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-196">Die Bedrohungs Informationen wurden geändert.</span><span class="sxs-lookup"><span data-stu-id="f29d1-196">Threat information modified.</span></span> <span data-ttu-id="f29d1-197">Beispielsweise wurde eine neue Ressource hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f29d1-197">For example, a new resource was added.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-198"><span id="MPNOTIFY_THREAT_CLEAN_SUCCEEDED"></span><span id="mpnotify_threat_clean_succeeded"></span>**mpnotify- \_ Bedrohungs \_ Bereinigung \_ erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="f29d1-198"><span id="MPNOTIFY_THREAT_CLEAN_SUCCEEDED"></span><span id="mpnotify_threat_clean_succeeded"></span>**MPNOTIFY\_THREAT\_CLEAN\_SUCCEEDED**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-199">Die Bereinigungs Aktion war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f29d1-199">Cleaning action succeeded for a threat.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-200"><span id="MPNOTIFY_THREAT_CLEAN_FAILED"></span><span id="mpnotify_threat_clean_failed"></span>**mpnotify-Fehler beim \_ \_ Bereinigen \_**</span><span class="sxs-lookup"><span data-stu-id="f29d1-200"><span id="MPNOTIFY_THREAT_CLEAN_FAILED"></span><span id="mpnotify_threat_clean_failed"></span>**MPNOTIFY\_THREAT\_CLEAN\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-201">Fehler beim Bereinigungs Vorgang für eine Bedrohung.</span><span class="sxs-lookup"><span data-stu-id="f29d1-201">Cleaning action failed for a threat.</span></span> <span data-ttu-id="f29d1-202">**Fehler \_ Der Fehlercode "MP- \_ Bedrohung \_ nicht \_ gefunden** " zeigt an, dass die Bedrohung nicht gefunden wurde (und kein Fehler beim Bereinigen aufgetreten ist).</span><span class="sxs-lookup"><span data-stu-id="f29d1-202">**ERROR\_MP\_THREAT\_NOT\_FOUND** error code indicates that the threat was not found (and was not a failure to clean).</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-203"><span id="MPNOTIFY_THREAT_ABANDONED"></span><span id="mpnotify_threat_abandoned"></span>**mpnotify- \_ Bedrohung \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="f29d1-203"><span id="MPNOTIFY_THREAT_ABANDONED"></span><span id="mpnotify_threat_abandoned"></span>**MPNOTIFY\_THREAT\_ABANDONED**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-204">Es ist keine Wiederherstellung aufgetreten, bevor der Dienst angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="f29d1-204">No remediation occurred before the service was stopped.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-205"><span id="MPNOTIFY_THREAT_CLEAN_EVENT_START"></span><span id="mpnotify_threat_clean_event_start"></span>**mpnotify \_ Threat \_ Clean- \_ Ereignis \_ starten**</span><span class="sxs-lookup"><span data-stu-id="f29d1-205"><span id="MPNOTIFY_THREAT_CLEAN_EVENT_START"></span><span id="mpnotify_threat_clean_event_start"></span>**MPNOTIFY\_THREAT\_CLEAN\_EVENT\_START**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-206">Eine Reinigungsaktion wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="f29d1-206">A cleaning action has been started.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-207"><span id="MPNOTIFY_THREAT_CLEAN_EVENT_COMPLETE"></span><span id="mpnotify_threat_clean_event_complete"></span>**mpnotify \_ Threat \_ Clean- \_ Ereignis wurde \_ beendet.**</span><span class="sxs-lookup"><span data-stu-id="f29d1-207"><span id="MPNOTIFY_THREAT_CLEAN_EVENT_COMPLETE"></span><span id="mpnotify_threat_clean_event_complete"></span>**MPNOTIFY\_THREAT\_CLEAN\_EVENT\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-208">Eine Reinigungsaktion wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="f29d1-208">A cleaning action has ended.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-209"><span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span>**mpnotify \_ sigupdate \_ Start**</span><span class="sxs-lookup"><span data-stu-id="f29d1-209"><span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span>**MPNOTIFY\_SIGUPDATE\_START**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-210">Das Signatur Update wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="f29d1-210">Signature update started.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-211"><span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span>**mpnotify \_ sigupdate- \_ Suche \_ starten**</span><span class="sxs-lookup"><span data-stu-id="f29d1-211"><span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span>**MPNOTIFY\_SIGUPDATE\_SEARCH\_START**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-212">Suche nach Updates gestartet.</span><span class="sxs-lookup"><span data-stu-id="f29d1-212">Search for updates started.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-213"><span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span>**mpnotify \_ sigupdate- \_ Suche ist \_ beendet**</span><span class="sxs-lookup"><span data-stu-id="f29d1-213"><span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span>**MPNOTIFY\_SIGUPDATE\_SEARCH\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-214">Suche nach Updates wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="f29d1-214">Search for updates completed.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-215"><span id="MPNOTIFY_SIGUPDATE_SOFTWARE_UPDATE_AVAILABLE"></span><span id="mpnotify_sigupdate_software_update_available"></span>**mpnotify- \_ sigupdate- \_ Software \_ Update \_ verfügbar**</span><span class="sxs-lookup"><span data-stu-id="f29d1-215"><span id="MPNOTIFY_SIGUPDATE_SOFTWARE_UPDATE_AVAILABLE"></span><span id="mpnotify_sigupdate_software_update_available"></span>**MPNOTIFY\_SIGUPDATE\_SOFTWARE\_UPDATE\_AVAILABLE**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-216">Das Software Update ist verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f29d1-216">Software update available.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-217"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span>**mpnotify \_ sigupdate \_ Download \_ starten**</span><span class="sxs-lookup"><span data-stu-id="f29d1-217"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_START**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-218">Der Download wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="f29d1-218">Download started.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-219"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span>**mpnotify \_ sigupdate- \_ Download \_ Fortschritt**</span><span class="sxs-lookup"><span data-stu-id="f29d1-219"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_PROGRESS**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-220">Der Download wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f29d1-220">Download in progress.</span></span> <span data-ttu-id="f29d1-221">Rückruf Daten enthalten den Fortschritt.</span><span class="sxs-lookup"><span data-stu-id="f29d1-221">Callback data contains progress.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-222"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span>**mpnotify \_ sigupdate- \_ Download ist \_ fertiggestellt.**</span><span class="sxs-lookup"><span data-stu-id="f29d1-222"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-223">Download abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="f29d1-223">Download completed.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-224"><span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span>**mpnotify \_ sigupdate \_ Installation \_ starten**</span><span class="sxs-lookup"><span data-stu-id="f29d1-224"><span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span>**MPNOTIFY\_SIGUPDATE\_INSTALL\_START**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-225">Die Installation wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="f29d1-225">Installation started.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-226"><span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span>**mpnotify \_ sigupdate- \_ Installations \_ Fortschritt**</span><span class="sxs-lookup"><span data-stu-id="f29d1-226"><span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span>**MPNOTIFY\_SIGUPDATE\_INSTALL\_PROGRESS**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-227">Installation wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f29d1-227">Installation in progress.</span></span> <span data-ttu-id="f29d1-228">Rückruf Daten enthalten den Fortschritt.</span><span class="sxs-lookup"><span data-stu-id="f29d1-228">Callback data contains progress.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-229"><span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span>**mpnotify \_ sigupdate- \_ Installation ist \_ fertiggestellt.**</span><span class="sxs-lookup"><span data-stu-id="f29d1-229"><span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span>**MPNOTIFY\_SIGUPDATE\_INSTALL\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-230">Die Installation ist beendet.</span><span class="sxs-lookup"><span data-stu-id="f29d1-230">Installation complete.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-231"><span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span>**mpnotify- \_ sigupdate- \_ Neustart \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="f29d1-231"><span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span>**MPNOTIFY\_SIGUPDATE\_REBOOT\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-232">Das Update erfordert einen Neustart.</span><span class="sxs-lookup"><span data-stu-id="f29d1-232">Update requires reboot.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-233"><span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span>**mpnotify \_ sigupdate- \_ Anforderung \_ verarbeitet**</span><span class="sxs-lookup"><span data-stu-id="f29d1-233"><span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span>**MPNOTIFY\_SIGUPDATE\_REQUEST\_PROCESSED**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-234">Der Dienst hat eine Signatur Aktualisierungs Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="f29d1-234">Service processed a signature update request.</span></span> <span data-ttu-id="f29d1-235">Fehler oder Erfolg wird von **HRESULT** in den Rückruf Daten angegeben.</span><span class="sxs-lookup"><span data-stu-id="f29d1-235">Failure or success is indicated by **hResult** in the callback data.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-236"><span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span>**mpnotify \_ sigupdate ist fertiggestellt. \_**</span><span class="sxs-lookup"><span data-stu-id="f29d1-236"><span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span>**MPNOTIFY\_SIGUPDATE\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-237">Das Update wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="f29d1-237">Update complete.</span></span> <span data-ttu-id="f29d1-238">**S \_** Der Status false gibt an, dass keine Updates erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="f29d1-238">**S\_FALSE** status indicates that no updates were needed.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-239"><span id="MPNOTIFY_SAMPLE_START"></span><span id="mpnotify_sample_start"></span>**mpnotify- \_ Beispiel \_ Start**</span><span class="sxs-lookup"><span data-stu-id="f29d1-239"><span id="MPNOTIFY_SAMPLE_START"></span><span id="mpnotify_sample_start"></span>**MPNOTIFY\_SAMPLE\_START**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-240">Die Beispiel Übermittlung wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="f29d1-240">Sample submission started.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-241"><span id="MPNOTIFY_SAMPLE_COMPLETE"></span><span id="mpnotify_sample_complete"></span>**mpnotify- \_ Beispiel ist \_ fertiggestellt**</span><span class="sxs-lookup"><span data-stu-id="f29d1-241"><span id="MPNOTIFY_SAMPLE_COMPLETE"></span><span id="mpnotify_sample_complete"></span>**MPNOTIFY\_SAMPLE\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-242">Die Beispiel Übermittlung wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="f29d1-242">Sample submission completed.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-243"><span id="MPNOTIFY_SAMPLE_ITEM_START"></span><span id="mpnotify_sample_item_start"></span>**mpnotify- \_ Beispiel \_ Element \_ Anfang**</span><span class="sxs-lookup"><span data-stu-id="f29d1-243"><span id="MPNOTIFY_SAMPLE_ITEM_START"></span><span id="mpnotify_sample_item_start"></span>**MPNOTIFY\_SAMPLE\_ITEM\_START**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-244">Eine bestimmte Beispiel Element Übermittlung wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="f29d1-244">Specific sample item submission started.</span></span> <span data-ttu-id="f29d1-245">Der Beispiel Index für Elemente ist in [**mpsample- \_ Daten**](mpsample-data.md)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f29d1-245">Sample item index is available in [**MPSAMPLE\_DATA**](mpsample-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-246"><span id="MPNOTIFY_SAMPLE_ITEM_SUCCEEDED"></span><span id="mpnotify_sample_item_succeeded"></span>**mpnotify- \_ Beispiel \_ Element \_ erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="f29d1-246"><span id="MPNOTIFY_SAMPLE_ITEM_SUCCEEDED"></span><span id="mpnotify_sample_item_succeeded"></span>**MPNOTIFY\_SAMPLE\_ITEM\_SUCCEEDED**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-247">Eine bestimmte Beispiel Element Übermittlung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f29d1-247">Specific sample item submission succeeded.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-248"><span id="MPNOTIFY_SAMPLE_ITEM_FAILED"></span><span id="mpnotify_sample_item_failed"></span>**Fehler beim mpnotify- \_ Beispiel \_ Element. \_**</span><span class="sxs-lookup"><span data-stu-id="f29d1-248"><span id="MPNOTIFY_SAMPLE_ITEM_FAILED"></span><span id="mpnotify_sample_item_failed"></span>**MPNOTIFY\_SAMPLE\_ITEM\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-249">Fehler beim Einreichen eines bestimmten Beispiel Elements.</span><span class="sxs-lookup"><span data-stu-id="f29d1-249">Specific sample item submission failed.</span></span> <span data-ttu-id="f29d1-250">Der Fehlercode ist in [**mpcallback- \_ Daten**](mpcallback-data.md)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f29d1-250">Error code is available in [**MPCALLBACK\_DATA**](mpcallback-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-251"><span id="MPNOTIFY_RESERVED_DATA"></span><span id="mpnotify_reserved_data"></span>**\_reservierte Daten für mpnotify \_**</span><span class="sxs-lookup"><span data-stu-id="f29d1-251"><span id="MPNOTIFY_RESERVED_DATA"></span><span id="mpnotify_reserved_data"></span>**MPNOTIFY\_RESERVED\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-252">Interne reservierte Daten.</span><span class="sxs-lookup"><span data-stu-id="f29d1-252">Internal reserved data.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-253"><span id="MPNOTIFY_FASTPATH_SIG_ADDED"></span><span id="mpnotify_fastpath_sig_added"></span>**mpnotify \_ FastPath \_ sig \_ hinzugefügt**</span><span class="sxs-lookup"><span data-stu-id="f29d1-253"><span id="MPNOTIFY_FASTPATH_SIG_ADDED"></span><span id="mpnotify_fastpath_sig_added"></span>**MPNOTIFY\_FASTPATH\_SIG\_ADDED**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-254">Eine FastPath-Signatur hat eine Signatur entweder hinzugefügt oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="f29d1-254">A Fastpath signature has either added or disabled a signature.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-255"><span id="MPNOTIFY_FASTPATH_SIG_REMOVED"></span><span id="mpnotify_fastpath_sig_removed"></span>**mpnotify \_ FastPath \_ sig \_ entfernt**</span><span class="sxs-lookup"><span data-stu-id="f29d1-255"><span id="MPNOTIFY_FASTPATH_SIG_REMOVED"></span><span id="mpnotify_fastpath_sig_removed"></span>**MPNOTIFY\_FASTPATH\_SIG\_REMOVED**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-256">Eine FastPath-Signatur wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="f29d1-256">A FastPath signature has been removed.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-257"><span id="MPNOTIFY_NIS_PRIVATE"></span><span id="mpnotify_nis_private"></span>**mpnotify \_ NIS \_ private**</span><span class="sxs-lookup"><span data-stu-id="f29d1-257"><span id="MPNOTIFY_NIS_PRIVATE"></span><span id="mpnotify_nis_private"></span>**MPNOTIFY\_NIS\_PRIVATE**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-258">Private NIS-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="f29d1-258">NIS private notifcations.</span></span> <span data-ttu-id="f29d1-259">Hierfür sollten keine Partner registriert werden.</span><span class="sxs-lookup"><span data-stu-id="f29d1-259">No partners should register for this.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-260"><span id="MPNOTIFY_HEALTH_CHANGE"></span><span id="mpnotify_health_change"></span>**mpnotify-Integritäts \_ \_ Änderung**</span><span class="sxs-lookup"><span data-stu-id="f29d1-260"><span id="MPNOTIFY_HEALTH_CHANGE"></span><span id="mpnotify_health_change"></span>**MPNOTIFY\_HEALTH\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-261">Der am-Dienst hat einen neuen Status eingegeben.</span><span class="sxs-lookup"><span data-stu-id="f29d1-261">The AM service has entered a new state.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-262"><span id="MPNOTIFY_HEALTH_RECOVERY"></span><span id="mpnotify_health_recovery"></span>**mpnotify-Integritäts \_ \_ Wiederherstellung**</span><span class="sxs-lookup"><span data-stu-id="f29d1-262"><span id="MPNOTIFY_HEALTH_RECOVERY"></span><span id="mpnotify_health_recovery"></span>**MPNOTIFY\_HEALTH\_RECOVERY**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-263">Der am-Dienst wurde nach einem-Zustand wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="f29d1-263">The AM service has recovered from a state.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-264"><span id="MPNOTIFY_HEALTH_START"></span><span id="mpnotify_health_start"></span>**mpnotify-Integritäts \_ \_ Beginn**</span><span class="sxs-lookup"><span data-stu-id="f29d1-264"><span id="MPNOTIFY_HEALTH_START"></span><span id="mpnotify_health_start"></span>**MPNOTIFY\_HEALTH\_START**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-265">Der am-Dienst hat den Zustand des Systems initialisiert.</span><span class="sxs-lookup"><span data-stu-id="f29d1-265">The AM service has initialized the health of the system.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-266"><span id="MPNOTIFY_ENDOFLIFE_CHANGE"></span><span id="mpnotify_endoflife_change"></span>**Änderung der \_ Endo-Life-Änderung in mpnotify \_**</span><span class="sxs-lookup"><span data-stu-id="f29d1-266"><span id="MPNOTIFY_ENDOFLIFE_CHANGE"></span><span id="mpnotify_endoflife_change"></span>**MPNOTIFY\_ENDOFLIFE\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-267">Die Ablaufdatums Angaben für den am-Dienst haben sich geändert.</span><span class="sxs-lookup"><span data-stu-id="f29d1-267">The "End Of Life" expiry dates for the AM service have changed.</span></span>

</dd> <dt>

<span data-ttu-id="f29d1-268"><span id="MPNOTIFY_MALWARETOAST_DATA"></span><span id="mpnotify_malwaretoast_data"></span>**mpnotify \_ malwarepopup- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="f29d1-268"><span id="MPNOTIFY_MALWARETOAST_DATA"></span><span id="mpnotify_malwaretoast_data"></span>**MPNOTIFY\_MALWARETOAST\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="f29d1-269">Im Dienst "am" ist Schadsoftware aufgetreten, die möglicherweise zu einer Änderung der Änderung des Computers geführt hat.</span><span class="sxs-lookup"><span data-stu-id="f29d1-269">The AM service has encountered malware that might have caused critical settings change in the machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f29d1-270">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f29d1-270">Requirements</span></span>



| <span data-ttu-id="f29d1-271">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f29d1-271">Requirement</span></span> | <span data-ttu-id="f29d1-272">Wert</span><span class="sxs-lookup"><span data-stu-id="f29d1-272">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f29d1-273">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f29d1-273">Minimum supported client</span></span><br/> | <span data-ttu-id="f29d1-274">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f29d1-274">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f29d1-275">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f29d1-275">Minimum supported server</span></span><br/> | <span data-ttu-id="f29d1-276">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f29d1-276">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f29d1-277">Header</span><span class="sxs-lookup"><span data-stu-id="f29d1-277">Header</span></span><br/>                   | <dl> <span data-ttu-id="f29d1-278"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="f29d1-278"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f29d1-279">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f29d1-279">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f29d1-280">**Mpmanagerstatus-QUERYEX**</span><span class="sxs-lookup"><span data-stu-id="f29d1-280">**MpManagerStatusQueryEx**</span></span>](mpmanagerstatusqueryex.md)
</dt> <dt>

[<span data-ttu-id="f29d1-281">**mpcallback- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="f29d1-281">**MPCALLBACK\_DATA**</span></span>](mpcallback-data.md)
</dt> <dt>

[<span data-ttu-id="f29d1-282">**mpsample- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="f29d1-282">**MPSAMPLE\_DATA**</span></span>](mpsample-data.md)
</dt> </dl>

 

 





