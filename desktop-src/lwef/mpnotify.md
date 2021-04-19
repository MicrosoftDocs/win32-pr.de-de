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
# <a name="mpnotify-enumeration"></a>Mpnotify-Enumeration

Mögliche Rückruf Benachrichtigungen.

## <a name="syntax"></a>Syntax


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



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="MPNOTIFY_NONE"></span><span id="mpnotify_none"></span>**mpnotify \_ None**
</dt> <dd></dd> <dt>

<span id="MPNOTIFY_CALL_START"></span><span id="mpnotify_call_start"></span>**mpnotify- \_ Anrufe \_ starten**
</dt> <dd>

Der Benachrichtigungs Rückruf wird gestartet.

</dd> <dt>

<span id="MPNOTIFY_CALL_COMPLETE"></span><span id="mpnotify_call_complete"></span>**mpnotify- \_ Rückruf ist \_ beendet**
</dt> <dd>

Der Benachrichtigungs Rückruf wurde abgeschlossen.

</dd> <dt>

<span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span>**Interner mpnotify- \_ \_ Fehler**
</dt> <dd>

Allgemeiner interner Fehler.

</dd> <dt>

<span id="MPNOTIFY_STATUS_SERVICE_START"></span><span id="mpnotify_status_service_start"></span>**mpnotify- \_ Status \_ Dienst \_ starten**
</dt> <dd>

Der Malware Schutzdienst wurde gestartet.

</dd> <dt>

<span id="MPNOTIFY_STATUS_SERVICE_RUNNING"></span><span id="mpnotify_status_service_running"></span>**mpnotify- \_ Status \_ Dienst wird \_ ausgeführt**
</dt> <dd>

Der Malware Schutzdienst wird ausgeführt.

</dd> <dt>

<span id="MPNOTIFY_STATUS_SERVICE_STOP"></span><span id="mpnotify_status_service_stop"></span>**mpnotify- \_ Status \_ Dienst \_ beendet**
</dt> <dd>

Der Malware Schutzdienst wurde beendet.

</dd> <dt>

<span id="MPNOTIFY_STATUS_COMPONENT"></span><span id="mpnotify_status_component"></span>**mpnotify- \_ Status \_ Komponente**
</dt> <dd>

Bestimmte Komponenten aktivieren/deaktivieren Sie den Status.

</dd> <dt>

<span id="MPNOTIFY_STATUS_CHANGE"></span><span id="mpnotify_status_change"></span>**mpnotify- \_ Status \_ Änderung**
</dt> <dd>

Der Gesamtprodukt Status hat sich geändert. Rufen Sie [**mpmanagerstatusqueryex**](mpmanagerstatusqueryex.md) auf, um den aktuellen Status abzurufen.

</dd> <dt>

<span id="MPNOTIFY_STATUS_COMPONENT_CONFIGURATION"></span><span id="mpnotify_status_component_configuration"></span>**mpnotify- \_ Status \_ Komponenten \_ Konfiguration**
</dt> <dd>

Eine bestimmte Komponente hat die Konfiguration geändert.

</dd> <dt>

<span id="MPNOTIFY_STATUS_EXPIRATION_CHANGE"></span><span id="mpnotify_status_expiration_change"></span>**mpnotify- \_ Status \_ Ablauf \_ Änderung**
</dt> <dd>

Der Produktablauf Status hat sich geändert.

</dd> <dt>

<span id="MPNOTIFY_STATUS_OFFLINE_SCAN_CHANGE"></span><span id="mpnotify_status_offline_scan_change"></span>**mpnotify- \_ Status- \_ Offline \_ Scan \_ Änderung**
</dt> <dd>

Der Status der Offline Überprüfung wurde geändert.

</dd> <dt>

<span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span>**mpnotify- \_ Scan \_ Start**
</dt> <dd>

Scan Vorgang gestartet.

</dd> <dt>

<span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span>**mpnotify- \_ Scan \_ angehalten**
</dt> <dd>

Scan angehalten.

</dd> <dt>

<span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span>**mpnotify-Scan wird fortgesetzt \_ \_**
</dt> <dd>

Überprüfung fortgesetzt.

</dd> <dt>

<span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span>**mpnotify- \_ Scan \_ Abbruch**
</dt> <dd>

Scan abgebrochen.

</dd> <dt>

<span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span>**mpnotify- \_ Scan ist \_ beendet**
</dt> <dd>

Überprüfung abgeschlossen.

</dd> <dt>

<span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span>**mpnotify- \_ Scan Status \_**
</dt> <dd>

Status Benachrichtigung für die zu überprüfende Ressource.

</dd> <dt>

<span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span>**mpnotify- \_ Scan \_ Fehler**
</dt> <dd>

Fehler beim Scannen einer bestimmten Ressource. Der Scan Vorgang wird trotzdem fortgesetzt.

</dd> <dt>

<span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span>**mpnotify- \_ Scan \_ infiziert**
</dt> <dd>

Der Scan hat eine infizierte Ressource gefunden.

</dd> <dt>

<span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span>**mpnotify- \_ Scan \_ memorystart**
</dt> <dd>

Der Scan Vorgang zum Benachrichtigen des Speicher Scan Teils der Systemüberprüfung wurde gestartet.

</dd> <dt>

<span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span>**mpnotify- \_ Scan \_ memorycomplete**
</dt> <dd>

Der Scan Vorgang zum Benachrichtigen des Speicher Scan Teils der Systemüberprüfung wurde abgeschlossen.

</dd> <dt>

<span id="MPNOTIFY_SCAN_SFC_BUILD_START"></span><span id="mpnotify_scan_sfc_build_start"></span>**mpnotify- \_ Scan für \_ sfc- \_ Build \_ starten**
</dt> <dd>

Der Überprüfungs Fortschritt zum Benachrichtigen des SFC-buildteils wurde gestartet.

</dd> <dt>

<span id="MPNOTIFY_SCAN_SFC_BUILD_COMPLETE"></span><span id="mpnotify_scan_sfc_build_complete"></span>**mpnotify- \_ Scan, \_ sfc-Build wurde \_ \_ beendet**
</dt> <dd>

Der Scan Vorgang zum Benachrichtigen des SFC-buildteils wurde abgeschlossen.

</dd> <dt>

<span id="MPNOTIFY_SCAN_FASTPATH_START"></span><span id="mpnotify_scan_fastpath_start"></span>**mpnotify-Überprüfung \_ \_ FastPath \_ starten**
</dt> <dd>

Der Scan Vorgang von FastPath SpyNet wurde gestartet.

</dd> <dt>

<span id="MPNOTIFY_SCAN_FASTPATH_COMPLETE"></span><span id="mpnotify_scan_fastpath_complete"></span>**mpnotify- \_ Scan für \_ FastPath ist \_ beendet**
</dt> <dd>

Das Überprüfen von FastPath SpyNet wurde beendet.

</dd> <dt>

<span id="MPNOTIFY_SCAN_FASTPATH_PROGRESS"></span><span id="mpnotify_scan_fastpath_progress"></span>**mpnotify-Vorgang zum durch \_ Suchen von \_ FastPath \_**
</dt> <dd>

Status Benachrichtigung für FastPath-repper, intern verwendet und in den **mpnotify- \_ Scan \_** Status für extern konvertiert.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_START"></span><span id="mpnotify_clean_start"></span>**Löschen von mpnotify- \_ Bereinigung \_**
</dt> <dd>

Reinigung wurde gestartet.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_COMPLETE"></span><span id="mpnotify_clean_complete"></span>**Löschen von mpnotify- \_ Bereinigung \_**
</dt> <dd>

Reinigung abgeschlossen.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESTOREPOINT_START"></span><span id="mpnotify_clean_restorepoint_start"></span>**mpnotify \_ Clean \_ RestorePoint \_ Start**
</dt> <dd>

Die Erstellung eines System Wiederherstellungs Punkts wurde gestartet.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESTOREPOINT_SUCCEEDED"></span><span id="mpnotify_clean_restorepoint_succeeded"></span>**mpnotify \_ Clean \_ RestorePoint \_ erfolgreich**
</dt> <dd>

Der System Wiederherstellungspunkt wurde erfolgreich erstellt.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESTOREPOINT_FAILED"></span><span id="mpnotify_clean_restorepoint_failed"></span>**Fehler beim \_ Bereinigen von Clean \_ RestorePoint. \_**
</dt> <dd>

Fehler beim Erstellen des System Wiederherstellungs Punkts.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_START"></span><span id="mpnotify_clean_threat_start"></span>**mpnotify \_ Clean \_ Threat \_ Start**
</dt> <dd>

Die Bereinigung wird für eine bestimmte Bedrohung gestartet.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_SUCCEEDED"></span><span id="mpnotify_clean_threat_succeeded"></span>**mpnotify- \_ Bereinigung \_ \_ erfolgreich**
</dt> <dd>

Die Bereinigung ist für eine bestimmte Bedrohung erfolgreich.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_FAILED"></span><span id="mpnotify_clean_threat_failed"></span>**Fehler beim \_ Bereinigen der Bereinigung \_ \_**
</dt> <dd>

Fehler beim Bereinigen für eine bestimmte Bedrohung. **Fehler \_ Der Fehlercode "MP- \_ Bedrohung \_ nicht \_ gefunden** " zeigt an, dass die Bedrohung nicht gefunden wurde (und kein Fehler beim Bereinigen aufgetreten ist).

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESOURCE_SUCCEEDED"></span><span id="mpnotify_clean_resource_succeeded"></span>**mpnotify- \_ Clean- \_ Ressource \_ erfolgreich**
</dt> <dd>

Die Bereinigung für eine bestimmte Ressource war erfolgreich.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESOURCE_FAILED"></span><span id="mpnotify_clean_resource_failed"></span>**Fehler beim Löschen der mpnotify- \_ \_ Ressource \_**
</dt> <dd>

Fehler beim Bereinigen für eine bestimmte Ressource.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_COMPLETE"></span><span id="mpnotify_clean_threat_complete"></span>**mpnotify \_ Clean \_ Threat \_ Complete**
</dt> <dd>

Die Bereinigung wurde für eine bestimmte Bedrohung abgeschlossen.

</dd> <dt>

<span id="MPNOTIFY_PRECHECK_START"></span><span id="mpnotify_precheck_start"></span>**mpnotify- \_ vorab Überprüfung \_ starten**
</dt> <dd>

Clean Vorüberprüfung wurde gestartet.

</dd> <dt>

<span id="MPNOTIFY_PRECHECK_COMPLETE"></span><span id="mpnotify_precheck_complete"></span>**mpnotify- \_ vorab Überprüfung ist \_ beendet**
</dt> <dd>

Die Clean-Vorprüfung ist abgeschlossen.

</dd> <dt>

<span id="MPNOTIFY_PRECHECK_RESOURCE_BLOCKED"></span><span id="mpnotify_precheck_resource_blocked"></span>**mpnotify- \_ Precheck- \_ Ressource \_ blockiert**
</dt> <dd>

Clean Vorüberprüfung hat blockierte Ressource erkannt.

</dd> <dt>

<span id="MPNOTIFY_THREAT_DETECTED"></span><span id="mpnotify_threat_detected"></span>**mpnotify- \_ Bedrohung \_ erkannt**
</dt> <dd>

Neue Bedrohung im System erkannt.

</dd> <dt>

<span id="MPNOTIFY_THREAT_MODIFIED"></span><span id="mpnotify_threat_modified"></span>**mpnotify- \_ Bedrohung \_ geändert**
</dt> <dd>

Die Bedrohungs Informationen wurden geändert. Beispielsweise wurde eine neue Ressource hinzugefügt.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_SUCCEEDED"></span><span id="mpnotify_threat_clean_succeeded"></span>**mpnotify- \_ Bedrohungs \_ Bereinigung \_ erfolgreich**
</dt> <dd>

Die Bereinigungs Aktion war erfolgreich.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_FAILED"></span><span id="mpnotify_threat_clean_failed"></span>**mpnotify-Fehler beim \_ \_ Bereinigen \_**
</dt> <dd>

Fehler beim Bereinigungs Vorgang für eine Bedrohung. **Fehler \_ Der Fehlercode "MP- \_ Bedrohung \_ nicht \_ gefunden** " zeigt an, dass die Bedrohung nicht gefunden wurde (und kein Fehler beim Bereinigen aufgetreten ist).

</dd> <dt>

<span id="MPNOTIFY_THREAT_ABANDONED"></span><span id="mpnotify_threat_abandoned"></span>**mpnotify- \_ Bedrohung \_ abgebrochen**
</dt> <dd>

Es ist keine Wiederherstellung aufgetreten, bevor der Dienst angehalten wurde.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_EVENT_START"></span><span id="mpnotify_threat_clean_event_start"></span>**mpnotify \_ Threat \_ Clean- \_ Ereignis \_ starten**
</dt> <dd>

Eine Reinigungsaktion wurde gestartet.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_EVENT_COMPLETE"></span><span id="mpnotify_threat_clean_event_complete"></span>**mpnotify \_ Threat \_ Clean- \_ Ereignis wurde \_ beendet.**
</dt> <dd>

Eine Reinigungsaktion wurde beendet.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span>**mpnotify \_ sigupdate \_ Start**
</dt> <dd>

Das Signatur Update wurde gestartet.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span>**mpnotify \_ sigupdate- \_ Suche \_ starten**
</dt> <dd>

Suche nach Updates gestartet.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span>**mpnotify \_ sigupdate- \_ Suche ist \_ beendet**
</dt> <dd>

Suche nach Updates wurde abgeschlossen.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_SOFTWARE_UPDATE_AVAILABLE"></span><span id="mpnotify_sigupdate_software_update_available"></span>**mpnotify- \_ sigupdate- \_ Software \_ Update \_ verfügbar**
</dt> <dd>

Das Software Update ist verfügbar.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span>**mpnotify \_ sigupdate \_ Download \_ starten**
</dt> <dd>

Der Download wurde gestartet.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span>**mpnotify \_ sigupdate- \_ Download \_ Fortschritt**
</dt> <dd>

Der Download wird ausgeführt. Rückruf Daten enthalten den Fortschritt.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span>**mpnotify \_ sigupdate- \_ Download ist \_ fertiggestellt.**
</dt> <dd>

Download abgeschlossen.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span>**mpnotify \_ sigupdate \_ Installation \_ starten**
</dt> <dd>

Die Installation wurde gestartet.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span>**mpnotify \_ sigupdate- \_ Installations \_ Fortschritt**
</dt> <dd>

Installation wird ausgeführt. Rückruf Daten enthalten den Fortschritt.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span>**mpnotify \_ sigupdate- \_ Installation ist \_ fertiggestellt.**
</dt> <dd>

Die Installation ist beendet.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span>**mpnotify- \_ sigupdate- \_ Neustart \_ erforderlich**
</dt> <dd>

Das Update erfordert einen Neustart.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span>**mpnotify \_ sigupdate- \_ Anforderung \_ verarbeitet**
</dt> <dd>

Der Dienst hat eine Signatur Aktualisierungs Anforderung verarbeitet. Fehler oder Erfolg wird von **HRESULT** in den Rückruf Daten angegeben.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span>**mpnotify \_ sigupdate ist fertiggestellt. \_**
</dt> <dd>

Das Update wurde beendet. **S \_** Der Status false gibt an, dass keine Updates erforderlich sind.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_START"></span><span id="mpnotify_sample_start"></span>**mpnotify- \_ Beispiel \_ Start**
</dt> <dd>

Die Beispiel Übermittlung wurde gestartet.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_COMPLETE"></span><span id="mpnotify_sample_complete"></span>**mpnotify- \_ Beispiel ist \_ fertiggestellt**
</dt> <dd>

Die Beispiel Übermittlung wurde abgeschlossen.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_ITEM_START"></span><span id="mpnotify_sample_item_start"></span>**mpnotify- \_ Beispiel \_ Element \_ Anfang**
</dt> <dd>

Eine bestimmte Beispiel Element Übermittlung wurde gestartet. Der Beispiel Index für Elemente ist in [**mpsample- \_ Daten**](mpsample-data.md)verfügbar.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_ITEM_SUCCEEDED"></span><span id="mpnotify_sample_item_succeeded"></span>**mpnotify- \_ Beispiel \_ Element \_ erfolgreich**
</dt> <dd>

Eine bestimmte Beispiel Element Übermittlung war erfolgreich.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_ITEM_FAILED"></span><span id="mpnotify_sample_item_failed"></span>**Fehler beim mpnotify- \_ Beispiel \_ Element. \_**
</dt> <dd>

Fehler beim Einreichen eines bestimmten Beispiel Elements. Der Fehlercode ist in [**mpcallback- \_ Daten**](mpcallback-data.md)verfügbar.

</dd> <dt>

<span id="MPNOTIFY_RESERVED_DATA"></span><span id="mpnotify_reserved_data"></span>**\_reservierte Daten für mpnotify \_**
</dt> <dd>

Interne reservierte Daten.

</dd> <dt>

<span id="MPNOTIFY_FASTPATH_SIG_ADDED"></span><span id="mpnotify_fastpath_sig_added"></span>**mpnotify \_ FastPath \_ sig \_ hinzugefügt**
</dt> <dd>

Eine FastPath-Signatur hat eine Signatur entweder hinzugefügt oder deaktiviert.

</dd> <dt>

<span id="MPNOTIFY_FASTPATH_SIG_REMOVED"></span><span id="mpnotify_fastpath_sig_removed"></span>**mpnotify \_ FastPath \_ sig \_ entfernt**
</dt> <dd>

Eine FastPath-Signatur wurde entfernt.

</dd> <dt>

<span id="MPNOTIFY_NIS_PRIVATE"></span><span id="mpnotify_nis_private"></span>**mpnotify \_ NIS \_ private**
</dt> <dd>

Private NIS-Benachrichtigungen. Hierfür sollten keine Partner registriert werden.

</dd> <dt>

<span id="MPNOTIFY_HEALTH_CHANGE"></span><span id="mpnotify_health_change"></span>**mpnotify-Integritäts \_ \_ Änderung**
</dt> <dd>

Der am-Dienst hat einen neuen Status eingegeben.

</dd> <dt>

<span id="MPNOTIFY_HEALTH_RECOVERY"></span><span id="mpnotify_health_recovery"></span>**mpnotify-Integritäts \_ \_ Wiederherstellung**
</dt> <dd>

Der am-Dienst wurde nach einem-Zustand wieder hergestellt.

</dd> <dt>

<span id="MPNOTIFY_HEALTH_START"></span><span id="mpnotify_health_start"></span>**mpnotify-Integritäts \_ \_ Beginn**
</dt> <dd>

Der am-Dienst hat den Zustand des Systems initialisiert.

</dd> <dt>

<span id="MPNOTIFY_ENDOFLIFE_CHANGE"></span><span id="mpnotify_endoflife_change"></span>**Änderung der \_ Endo-Life-Änderung in mpnotify \_**
</dt> <dd>

Die Ablaufdatums Angaben für den am-Dienst haben sich geändert.

</dd> <dt>

<span id="MPNOTIFY_MALWARETOAST_DATA"></span><span id="mpnotify_malwaretoast_data"></span>**mpnotify \_ malwarepopup- \_ Daten**
</dt> <dd>

Im Dienst "am" ist Schadsoftware aufgetreten, die möglicherweise zu einer Änderung der Änderung des Computers geführt hat.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mpmanagerstatus-QUERYEX**](mpmanagerstatusqueryex.md)
</dt> <dt>

[**mpcallback- \_ Daten**](mpcallback-data.md)
</dt> <dt>

[**mpsample- \_ Daten**](mpsample-data.md)
</dt> </dl>

 

 





