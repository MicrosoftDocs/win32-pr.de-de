---
title: MPNOTIFY-Enumeration (MpClient.h)
description: Mögliche Rückrufbenachrichtigungen.
ms.assetid: CCD0CD89-2C6E-453F-9437-E6ED87AD9F29
keywords:
- Funktionen der MPNOTIFY-Enumerationsumgebung Windows Legacyumgebung
- PMPNOTIFY-Enumerationszeiger Legacy Windows Umgebungsfeatures
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
ms.openlocfilehash: ed62a9f868aa39cbc0cfc7702afc99849005a22106892696eca857ffb20673af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747788"
---
# <a name="mpnotify-enumeration"></a>MPNOTIFY-Enumeration

Mögliche Rückrufbenachrichtigungen.

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

<span id="MPNOTIFY_NONE"></span><span id="mpnotify_none"></span>**MPNOTIFY \_ NONE**
</dt> <dd></dd> <dt>

<span id="MPNOTIFY_CALL_START"></span><span id="mpnotify_call_start"></span>**MPNOTIFY \_ CALL \_ START**
</dt> <dd>

Start des Benachrichtigungsaufrufs.

</dd> <dt>

<span id="MPNOTIFY_CALL_COMPLETE"></span><span id="mpnotify_call_complete"></span>**MPNOTIFY \_ CALL \_ COMPLETE**
</dt> <dd>

Benachrichtigungsaufruf abgeschlossen.

</dd> <dt>

<span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span>**INTERNER \_ MPNOTIFY-FEHLER \_**
</dt> <dd>

Allgemeiner interner Fehler.

</dd> <dt>

<span id="MPNOTIFY_STATUS_SERVICE_START"></span><span id="mpnotify_status_service_start"></span>**MPNOTIFY \_ STATUS \_ SERVICE \_ START**
</dt> <dd>

Der Schutzdienst für Schadsoftware wurde gestartet.

</dd> <dt>

<span id="MPNOTIFY_STATUS_SERVICE_RUNNING"></span><span id="mpnotify_status_service_running"></span>**MPNOTIFY \_ STATUS SERVICE RUNNING (MPNOTIFY-STATUSDIENST WIRD \_ \_ AUSGEFÜHRT)**
</dt> <dd>

Der Schutzdienst für Schadsoftware wird ausgeführt.

</dd> <dt>

<span id="MPNOTIFY_STATUS_SERVICE_STOP"></span><span id="mpnotify_status_service_stop"></span>**MPNOTIFY \_ STATUS \_ SERVICE \_ STOP**
</dt> <dd>

Der Schutzdienst für Schadsoftware wurde beendet.

</dd> <dt>

<span id="MPNOTIFY_STATUS_COMPONENT"></span><span id="mpnotify_status_component"></span>**\_MPNOTIFY-STATUSKOMPONENTE \_**
</dt> <dd>

Der Aktivierungs-/Deaktivierungsstatus einer bestimmten Komponente.

</dd> <dt>

<span id="MPNOTIFY_STATUS_CHANGE"></span><span id="mpnotify_status_change"></span>**\_MPNOTIFY-STATUSÄNDERUNG \_**
</dt> <dd>

Der Allgemeine Produktstatus hat sich geändert. Rufen [**Sie MpManagerStatusQueryEx auf,**](mpmanagerstatusqueryex.md) um den aktuellen Status abzurufen.

</dd> <dt>

<span id="MPNOTIFY_STATUS_COMPONENT_CONFIGURATION"></span><span id="mpnotify_status_component_configuration"></span>**KONFIGURATION DER \_ \_ MPNOTIFY-STATUSKOMPONENTE \_**
</dt> <dd>

Eine bestimmte Komponente hat die Konfiguration geändert.

</dd> <dt>

<span id="MPNOTIFY_STATUS_EXPIRATION_CHANGE"></span><span id="mpnotify_status_expiration_change"></span>**MPNOTIFY \_ STATUS \_ EXPIRATION \_ CHANGE**
</dt> <dd>

Der Produktablaufstatus wurde geändert.

</dd> <dt>

<span id="MPNOTIFY_STATUS_OFFLINE_SCAN_CHANGE"></span><span id="mpnotify_status_offline_scan_change"></span>**ÄNDERUNG DES \_ \_ MPNOTIFY-STATUS \_ \_ OFFLINESCANS**
</dt> <dd>

Der erforderliche Zustand der Offlineprüfung wurde geändert.

</dd> <dt>

<span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span>**MPNOTIFY \_ SCAN \_ START**
</dt> <dd>

Die Überprüfung wurde gestartet.

</dd> <dt>

<span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span>**\_MPNOTIFY-ÜBERPRÜFUNG \_ ANGEHALTEN**
</dt> <dd>

Überprüfung angehalten.

</dd> <dt>

<span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span>**\_MPNOTIFY-ÜBERPRÜFUNG \_ FORTGESETZT**
</dt> <dd>

Überprüfung fortgesetzt.

</dd> <dt>

<span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span>**MPNOTIFY \_ SCAN \_ CANCEL**
</dt> <dd>

Überprüfung abgebrochen.

</dd> <dt>

<span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span>**MPNOTIFY \_ SCAN \_ COMPLETE**
</dt> <dd>

Überprüfung abgeschlossen.

</dd> <dt>

<span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span>**\_MPNOTIFY-ÜBERPRÜFUNGSFORTSCHRITT \_**
</dt> <dd>

Statusbenachrichtigung für die spezifische Ressource, die überprüft wird.

</dd> <dt>

<span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span>**\_MPNOTIFY-SCANFEHLER \_**
</dt> <dd>

Fehler beim Überprüfen einer bestimmten Ressource. Die Überprüfung wird weiterhin fortgesetzt.

</dd> <dt>

<span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span>**MPNOTIFY \_ SCAN \_ INFECTED**
</dt> <dd>

Scan hat eine infizierte Ressource gefunden.

</dd> <dt>

<span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span>**MPNOTIFY \_ SCAN \_ MEMORYSTART**
</dt> <dd>

Überprüfungsfortschritt, um den Arbeitsspeicherscanteil der Systemprüfung zu benachrichtigen, wurde gestartet.

</dd> <dt>

<span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span>**MPNOTIFY \_ SCAN \_ MEMORYCOMPLETE**
</dt> <dd>

Überprüfungsfortschritt, um den Speicherscanteil des Systemscans zu benachrichtigen, wurde abgeschlossen.

</dd> <dt>

<span id="MPNOTIFY_SCAN_SFC_BUILD_START"></span><span id="mpnotify_scan_sfc_build_start"></span>**MPNOTIFY \_ SCAN \_ SFC \_ BUILD \_ START**
</dt> <dd>

Überprüfungsfortschritt zur Benachrichtigung, dass der Sfc-Buildteil gestartet wurde.

</dd> <dt>

<span id="MPNOTIFY_SCAN_SFC_BUILD_COMPLETE"></span><span id="mpnotify_scan_sfc_build_complete"></span>**MPNOTIFY \_ SCAN \_ SFC \_ BUILD \_ COMPLETE**
</dt> <dd>

Überprüfungsfortschritt zur Benachrichtigung, dass der Sfc-Buildteil abgeschlossen wurde.

</dd> <dt>

<span id="MPNOTIFY_SCAN_FASTPATH_START"></span><span id="mpnotify_scan_fastpath_start"></span>**MPNOTIFY \_ SCAN \_ FASTPATH \_ START**
</dt> <dd>

Scan fastpath spynet hat begonnen.

</dd> <dt>

<span id="MPNOTIFY_SCAN_FASTPATH_COMPLETE"></span><span id="mpnotify_scan_fastpath_complete"></span>**MPNOTIFY \_ SCAN \_ FASTPATH \_ COMPLETE**
</dt> <dd>

Scan fastpath spynet wurde beendet.

</dd> <dt>

<span id="MPNOTIFY_SCAN_FASTPATH_PROGRESS"></span><span id="mpnotify_scan_fastpath_progress"></span>**MPNOTIFY \_ SCAN \_ FASTPATH \_ PROGRESS**
</dt> <dd>

Statusbenachrichtigung für fastpath-Neuscans, intern verwendet und für external in **MPNOTIFY \_ SCAN \_ PROGRESS** konvertiert.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_START"></span><span id="mpnotify_clean_start"></span>**MPNOTIFY \_ CLEAN \_ START**
</dt> <dd>

Die Bereinigung wurde gestartet.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_COMPLETE"></span><span id="mpnotify_clean_complete"></span>**MPNOTIFY \_ CLEAN \_ COMPLETE**
</dt> <dd>

Die Bereinigung wurde abgeschlossen.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESTOREPOINT_START"></span><span id="mpnotify_clean_restorepoint_start"></span>**MPNOTIFY \_ CLEAN \_ RESTOREPOINT \_ START**
</dt> <dd>

Die Erstellung eines Systemwiederherstellungspunkts wurde gestartet.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESTOREPOINT_SUCCEEDED"></span><span id="mpnotify_clean_restorepoint_succeeded"></span>**MPNOTIFY \_ CLEAN \_ RESTOREPOINT \_ SUCCEEDED**
</dt> <dd>

Der Systemwiederherstellungspunkt wurde erfolgreich erstellt.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESTOREPOINT_FAILED"></span><span id="mpnotify_clean_restorepoint_failed"></span>**FEHLER BEI MPNOTIFY \_ CLEAN \_ RESTOREPOINT \_**
</dt> <dd>

Fehler beim Erstellen des Systemwiederherstellungspunkts.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_START"></span><span id="mpnotify_clean_threat_start"></span>**MPNOTIFY \_ CLEAN \_ THREAT \_ START**
</dt> <dd>

Die Bereinigung wird für eine bestimmte Bedrohung gestartet.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_SUCCEEDED"></span><span id="mpnotify_clean_threat_succeeded"></span>**MPNOTIFY \_ CLEAN \_ THREAT \_ SUCCEEDED**
</dt> <dd>

Die Bereinigung ist für eine bestimmte Bedrohung erfolgreich.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_FAILED"></span><span id="mpnotify_clean_threat_failed"></span>**FEHLER BEI MPNOTIFY \_ CLEAN \_ THREAT \_**
</dt> <dd>

Die Bereinigung ist für eine bestimmte Bedrohung fehlgeschlagen. **FEHLER \_ Mp \_ THREAT \_ NOT \_ FOUND-Fehlercode** gibt an, dass die Bedrohung nicht gefunden wurde (und kein Fehler bei der Bereinigung war).

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESOURCE_SUCCEEDED"></span><span id="mpnotify_clean_resource_succeeded"></span>**MPNOTIFY \_ CLEAN \_ RESOURCE \_ SUCCEEDED**
</dt> <dd>

Die Bereinigung ist für eine bestimmte Ressource erfolgreich.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESOURCE_FAILED"></span><span id="mpnotify_clean_resource_failed"></span>**FEHLER BEI MPNOTIFY \_ CLEAN \_ RESOURCE \_**
</dt> <dd>

Fehler beim Bereinigen für eine bestimmte Ressource.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_COMPLETE"></span><span id="mpnotify_clean_threat_complete"></span>**MPNOTIFY \_ CLEAN \_ THREAT \_ COMPLETE**
</dt> <dd>

Die Bereinigung wurde für eine bestimmte Bedrohung abgeschlossen.

</dd> <dt>

<span id="MPNOTIFY_PRECHECK_START"></span><span id="mpnotify_precheck_start"></span>**MPNOTIFY \_ PRECHECK \_ START**
</dt> <dd>

Clean precheck started (Vorabprüfung für bereinigte Daten gestartet).

</dd> <dt>

<span id="MPNOTIFY_PRECHECK_COMPLETE"></span><span id="mpnotify_precheck_complete"></span>**MPNOTIFY \_ PRECHECK \_ COMPLETE**
</dt> <dd>

Bereinigte Vorabprüfung abgeschlossen.

</dd> <dt>

<span id="MPNOTIFY_PRECHECK_RESOURCE_BLOCKED"></span><span id="mpnotify_precheck_resource_blocked"></span>**MPNOTIFY \_ PRECHECK \_ RESOURCE \_ BLOCKED**
</dt> <dd>

Clean precheck detected blocked resource. (Bereinigte Vorabprüfung erkannte blockierte Ressource.

</dd> <dt>

<span id="MPNOTIFY_THREAT_DETECTED"></span><span id="mpnotify_threat_detected"></span>**\_MPNOTIFY-BEDROHUNG \_ ERKANNT**
</dt> <dd>

Neue Bedrohung im System erkannt.

</dd> <dt>

<span id="MPNOTIFY_THREAT_MODIFIED"></span><span id="mpnotify_threat_modified"></span>**MPNOTIFY \_ THREAT \_ MODIFIED**
</dt> <dd>

Geänderte Bedrohungsinformationen. Beispielsweise wurde eine neue Ressource hinzugefügt.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_SUCCEEDED"></span><span id="mpnotify_threat_clean_succeeded"></span>**MPNOTIFY \_ THREAT \_ CLEAN \_ SUCCEEDED**
</dt> <dd>

Die Bereinigungsaktion war für eine Bedrohung erfolgreich.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_FAILED"></span><span id="mpnotify_threat_clean_failed"></span>**FEHLER BEI DER \_ MPNOTIFY-BEDROHUNGSBEREINIGUNG \_ \_**
</dt> <dd>

Fehler bei der Bereinigungsaktion für eine Bedrohung. **FEHLER \_ MP THREAT NOT FOUND error code (MP \_ THREAT \_ NOT FOUND-Fehlercode) \_** gibt an, dass die Bedrohung nicht gefunden wurde (und kein Fehler beim Bereinigen).

</dd> <dt>

<span id="MPNOTIFY_THREAT_ABANDONED"></span><span id="mpnotify_threat_abandoned"></span>**MPNOTIFY \_ THREAT \_ ABANDONED**
</dt> <dd>

Vor dem Anhalten des Diensts ist keine Wiederherstellung aufgetreten.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_EVENT_START"></span><span id="mpnotify_threat_clean_event_start"></span>**STARTEN DES MPNOTIFY \_ THREAT \_ \_ CLEAN-EREIGNISSES \_**
</dt> <dd>

Eine Bereinigungsaktion wurde gestartet.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_EVENT_COMPLETE"></span><span id="mpnotify_threat_clean_event_complete"></span>**MPNOTIFY \_ THREAT \_ \_ CLEAN-EREIGNIS \_ ABGESCHLOSSEN**
</dt> <dd>

Eine Bereinigungsaktion wurde beendet.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span>**MPNOTIFY \_ SIGUPDATE \_ START**
</dt> <dd>

Signaturaktualisierung gestartet.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span>**MPNOTIFY \_ SIGUPDATE \_ SEARCH \_ START**
</dt> <dd>

Suche nach gestarteten Updates.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span>**MPNOTIFY \_ SIGUPDATE \_ SEARCH \_ COMPLETE**
</dt> <dd>

Suchen Sie nach abgeschlossenen Updates.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_SOFTWARE_UPDATE_AVAILABLE"></span><span id="mpnotify_sigupdate_software_update_available"></span>**MPNOTIFY \_ SIGUPDATE \_ SOFTWARE UPDATE \_ \_ VERFÜGBAR**
</dt> <dd>

Softwareupdate verfügbar.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span>**MPNOTIFY \_ SIGUPDATE \_ DOWNLOAD \_ START**
</dt> <dd>

Download gestartet.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span>**MPNOTIFY \_ \_ SIGUPDATE-DOWNLOADFORTSCHRITT \_**
</dt> <dd>

Der Download wird ausgeführt. Rückrufdaten enthalten den Fortschritt.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span>**MPNOTIFY \_ SIGUPDATE \_ DOWNLOAD \_ ABGESCHLOSSEN**
</dt> <dd>

Download abgeschlossen.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span>**MPNOTIFY \_ SIGUPDATE \_ INSTALL \_ START**
</dt> <dd>

Die Installation wurde gestartet.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span>**MPNOTIFY \_ \_ SIGUPDATE– \_ INSTALLATIONSFORTSCHRITT**
</dt> <dd>

Installation wird ausgeführt. Rückrufdaten enthalten den Fortschritt.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span>**MPNOTIFY \_ SIGUPDATE \_ INSTALL \_ COMPLETE**
</dt> <dd>

Die Installation ist abgeschlossen.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span>**MPNOTIFY \_ SIGUPDATE \_ REBOOT \_ ERFORDERLICH**
</dt> <dd>

Für das Update ist ein Neustart erforderlich.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span>**VERARBEITETE MPNOTIFY \_ \_ SIGUPDATE-ANFORDERUNG \_**
</dt> <dd>

Der Dienst hat eine Signaturaktualisierungsanforderung verarbeitet. Fehler oder Erfolg werden durch **hResult** in den Rückrufdaten angegeben.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span>**MPNOTIFY \_ SIGUPDATE \_ COMPLETE**
</dt> <dd>

Update abgeschlossen. **S \_ DER FALSE-Status** gibt an, dass keine Updates erforderlich waren.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_START"></span><span id="mpnotify_sample_start"></span>**\_MPNOTIFY-BEISPIELSTART \_**
</dt> <dd>

Die Beispielübermittlung wurde gestartet.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_COMPLETE"></span><span id="mpnotify_sample_complete"></span>**\_MPNOTIFY-BEISPIEL \_ ABGESCHLOSSEN**
</dt> <dd>

Die Beispielübermittlung wurde abgeschlossen.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_ITEM_START"></span><span id="mpnotify_sample_item_start"></span>**START DES \_ MPNOTIFY-BEISPIELELEMENTS \_ \_**
</dt> <dd>

Die Übermittlung eines bestimmten Beispielelements wurde gestartet. Der Beispielelementindex ist in [**MPSAMPLE \_ DATA**](mpsample-data.md)verfügbar.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_ITEM_SUCCEEDED"></span><span id="mpnotify_sample_item_succeeded"></span>**\_MPNOTIFY-BEISPIELELEMENT \_ \_ ERFOLGREICH**
</dt> <dd>

Die Übermittlung eines bestimmten Beispielelements war erfolgreich.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_ITEM_FAILED"></span><span id="mpnotify_sample_item_failed"></span>**\_FEHLER BEIM MPNOTIFY-BEISPIELELEMENT \_ \_**
</dt> <dd>

Fehler bei der Übermittlung eines bestimmten Beispielelements. Fehlercode ist in [**MPCALLBACK \_ DATA**](mpcallback-data.md)verfügbar.

</dd> <dt>

<span id="MPNOTIFY_RESERVED_DATA"></span><span id="mpnotify_reserved_data"></span>**RESERVIERTE \_ \_ MPNOTIFY-DATEN**
</dt> <dd>

Interne reservierte Daten.

</dd> <dt>

<span id="MPNOTIFY_FASTPATH_SIG_ADDED"></span><span id="mpnotify_fastpath_sig_added"></span>**MPNOTIFY \_ FASTPATH \_ SIG \_ HINZUGEFÜGT**
</dt> <dd>

Eine Fastpath-Signatur hat eine Signatur hinzugefügt oder deaktiviert.

</dd> <dt>

<span id="MPNOTIFY_FASTPATH_SIG_REMOVED"></span><span id="mpnotify_fastpath_sig_removed"></span>**MPNOTIFY \_ FASTPATH \_ SIG \_ ENTFERNT**
</dt> <dd>

Eine FastPath-Signatur wurde entfernt.

</dd> <dt>

<span id="MPNOTIFY_NIS_PRIVATE"></span><span id="mpnotify_nis_private"></span>**MPNOTIFY \_ NIS \_ PRIVATE**
</dt> <dd>

Private NIS-Notifkationen. Dafür sollten sich keine Partner registrieren.

</dd> <dt>

<span id="MPNOTIFY_HEALTH_CHANGE"></span><span id="mpnotify_health_change"></span>**MPNOTIFY \_ HEALTH \_ CHANGE**
</dt> <dd>

Der AM-Dienst wurde in einen neuen Zustand übergegangen.

</dd> <dt>

<span id="MPNOTIFY_HEALTH_RECOVERY"></span><span id="mpnotify_health_recovery"></span>**MPNOTIFY \_ HEALTH \_ RECOVERY**
</dt> <dd>

Der AM-Dienst wurde aus einem Zustand wiederhergestellt.

</dd> <dt>

<span id="MPNOTIFY_HEALTH_START"></span><span id="mpnotify_health_start"></span>**MPNOTIFY \_ HEALTH \_ START**
</dt> <dd>

Der AM-Dienst hat die Integrität des Systems initialisiert.

</dd> <dt>

<span id="MPNOTIFY_ENDOFLIFE_CHANGE"></span><span id="mpnotify_endoflife_change"></span>**MPNOTIFY \_ ENDOFLIFE \_ CHANGE**
</dt> <dd>

Die Ablaufdatume für den AM-Dienst "End Of Life" wurden geändert.

</dd> <dt>

<span id="MPNOTIFY_MALWARETOAST_DATA"></span><span id="mpnotify_malwaretoast_data"></span>**MPNOTIFY \_ \_ MALWARETOAST-DATEN**
</dt> <dd>

Der AM-Dienst hat Schadsoftware gefunden, die möglicherweise zu einer änderung kritischer Einstellungen auf dem Computer geführt hat.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md)
</dt> <dt>

[**\_MPCALLBACK-DATEN**](mpcallback-data.md)
</dt> <dt>

[**\_MPSAMPLE-DATEN**](mpsample-data.md)
</dt> </dl>

 

 





