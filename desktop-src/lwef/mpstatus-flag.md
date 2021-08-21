---
title: MPSTATUS_FLAG-Enumeration (MpClient.h)
description: Mögliche allgemeine Produktstatus-Bitflags.
ms.assetid: BF2E6506-E76A-4785-8E91-99937B413548
keywords:
- MPSTATUS_FLAG-Enumeration– Legacy-Windows-Umgebungsfeatures
- PMPSTATUS_FLAG-Enumerationszeiger Legacy Windows-Umgebungsfeatures
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
ms.openlocfilehash: 4d850f0e8de9a3b0ed18a1a1353dfdef40d41bcb1ce4d17265ec245e82ba73f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747034"
---
# <a name="mpstatus_flag-enumeration"></a>MPSTATUS \_ FLAG-Enumeration

Mögliche allgemeine Produktstatus-Bitflags.

## <a name="syntax"></a>Syntax


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



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="MP_STATUS_FLAG_NONE"></span><span id="mp_status_flag_none"></span>**MP \_ STATUS \_ FLAG \_ NONE**
</dt> <dd>

Es sind keine Statusflags festgelegt (nicht initialisierter Zustand).

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_UNAVAILABLE"></span><span id="mp_status_flag_service_unavailable"></span>**\_ \_ MP-STATUSFLAGDIENST \_ \_ NICHT VERFÜGBAR**
</dt> <dd>

Dienst wird nicht ausgeführt.

</dd> <dt>

<span id="MP_STATUS_FLAG_MPENGINE_UNAVAILABLE"></span><span id="mp_status_flag_mpengine_unavailable"></span>**\_ \_ MP-STATUSFLAG \_ MPENGINE \_ NICHT VERFÜGBAR**
</dt> <dd>

Der Dienst wurde ohne Schadsoftwareschutz-Engine gestartet.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_FULLSCAN_REQUIRED"></span><span id="mp_status_flag_threat_fullscan_required"></span>**\_ \_ MP-STATUSFLAG \_ BEDROHUNG \_ FULLSCAN \_ ERFORDERLICH**
</dt> <dd>

Ausstehende vollständige Überprüfung aufgrund einer Bedrohungsaktion.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_REBOOT_REQUIRED"></span><span id="mp_status_flag_threat_reboot_required"></span>**\_ \_ MP-STATUSFLAG \_ \_ BEDROHUNGSNEUSTART \_ ERFORDERLICH**
</dt> <dd>

Ausstehender Neustart aufgrund einer Bedrohungsaktion.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_MANUAL_STEPS_REQUIRED"></span><span id="mp_status_flag_threat_manual_steps_required"></span>**MANUELLE SCHRITTE FÜR DAS \_ MP-STATUSFLAG \_ \_ \_ \_ "BEDROHUNG" \_ ERFORDERLICH**
</dt> <dd>

Ausstehende manuelle Schritte aufgrund einer Bedrohungsaktion.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_AV_SIGNATURE"></span><span id="mp_status_flag_due_av_signature"></span>**\_ \_ MP-STATUSFLAG \_ DUE AV \_ \_ SIGNATURE**
</dt> <dd>

Antivirussignaturen sind veraltet.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_AS_SIGNATURE"></span><span id="mp_status_flag_due_as_signature"></span>**\_ \_ MP-STATUSFLAG \_ ALS \_ SIGNATUR FÄLLIG \_**
</dt> <dd>

Antispyware-Signaturen sind veraltet.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_QUICK_SCAN"></span><span id="mp_status_flag_due_quick_scan"></span>**MP \_ STATUS \_ FLAG \_ DUE \_ QUICK \_ SCAN**
</dt> <dd>

Für einen bestimmten Zeitraum wurde keine Schnellüberprüfung durchgeführt.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_FULL_SCAN"></span><span id="mp_status_flag_due_full_scan"></span>**MP \_ STATUS \_ FLAG \_ DUE \_ FULL \_ SCAN**
</dt> <dd>

Für einen bestimmten Zeitraum wurde keine vollständige Überprüfung durchgeführt.

</dd> <dt>

<span id="MP_STATUS_FLAG_INPROGRESS_SYSTEM_SCAN"></span><span id="mp_status_flag_inprogress_system_scan"></span>**MP \_ STATUS \_ FLAG \_ INPROGRESS \_ SYSTEM \_ SCAN**
</dt> <dd>

Vom System initiierte Überprüfung wird ausgeführt.

</dd> <dt>

<span id="MP_STATUS_FLAG_INPROGRESS_ROUTINE_CLEANING"></span><span id="mp_status_flag_inprogress_routine_cleaning"></span>**MP \_ STATUS \_ FLAG \_ INPROGRESS \_ ROUTINE \_ CLEANING**
</dt> <dd>

Systeminitiierte Bereinigung wird ausgeführt.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_SAMPLES"></span><span id="mp_status_flag_due_samples"></span>**MP \_ STATUS \_ FLAG \_ DUE \_ SAMPLES**
</dt> <dd>

Es stehen Beispiele für die Übermittlung aus.

</dd> <dt>

<span id="MP_STATUS_FLAG_EVALUATION_MODE"></span><span id="mp_status_flag_evaluation_mode"></span>**\_ \_ AUSWERTUNGSMODUS DES MP-STATUSFLAGS \_ \_**
</dt> <dd>

Das Produkt wird im Auswertungsmodus ausgeführt.

</dd> <dt>

<span id="MP_STATUS_FLAG_NONGENUINE"></span><span id="mp_status_flag_nongenuine"></span>**MP \_ STATUS \_ FLAG \_ NONGENUINE**
</dt> <dd>

Das Produkt wird im Nicht-Originalmodus Windows ausgeführt.

</dd> <dt>

<span id="MP_STATUS_FLAG_PRODUCT_EXPIRED"></span><span id="mp_status_flag_product_expired"></span>**\_ \_ MP-STATUSFLAG \_ PRODUKT \_ ABGELAUFEN**
</dt> <dd>

Das Produkt ist abgelaufen.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_CALLISTO_REQUIRED"></span><span id="mp_status_flag_threat_callisto_required"></span>**MP \_ STATUS \_ FLAG \_ THREAT \_ CALLISTO \_ REQUIRED**
</dt> <dd>

Callisto-Off-Line-Scan erforderlich.

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_ON_SYSTEM_SHUTDOWN"></span><span id="mp_status_flag_service_on_system_shutdown"></span>**\_ \_ MP-STATUSFLAGDIENST \_ \_ BEIM \_ HERUNTERFAHREN DES SYSTEMS \_**
</dt> <dd>

Der Dienst wird im Rahmen des Herunterfahrens des Systems heruntergefahren.

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_critical_failure"></span>**FEHLER \_ BEIM MP-STATUSFLAG \_ \_ \_ "DIENSTKRITISCH" \_**
</dt> <dd>

Fehler bei der Bedrohungsbehebung.

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_NON_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_non_critical_failure"></span>**FEHLER BEIM \_ MP-STATUSFLAGDIENST \_ \_ NICHT \_ \_ KRITISCH \_**
</dt> <dd>

Fehler bei der Wiederherstellung von Bedrohungen nicht kritisch.

</dd> <dt>

<span id="MP_STATUS_FLAG_HEALTH_INITIALIZED"></span><span id="mp_status_flag_health_initialized"></span>**INTEGRITÄT DES \_ MP-STATUSFLAGS \_ \_ \_ INITIALISIERT**
</dt> <dd>

Es sind keine Statusflags festgelegt (gut initialisierter Zustand).

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_PLATFORM_UPDATE"></span><span id="mp_status_flag_due_platform_update"></span>**MP \_ STATUS \_ FLAG \_ DUE \_ PLATFORM \_ UPDATE**
</dt> <dd>

Die Plattform ist veraltet.

</dd> <dt>

<span id="MP_STATUS_FLAG_INPROGRESS_PLATFORM_UPDATE"></span><span id="mp_status_flag_inprogress_platform_update"></span>**MP \_ STATUS \_ FLAG \_ INPROGRESS \_ PLATFORM \_ UPDATE**
</dt> <dd>

Das Plattformupdate wird ausgeführt.

</dd> <dt>

<span id="MP_STATUS_FLAG_PLATFORM_ABOUT_TO_BE_OUTDATED"></span><span id="mp_status_flag_platform_about_to_be_outdated"></span>**MP \_ STATUS FLAG PLATFORM ABOUT TO BE OUTDATED (MP-STATUSFLAGPLATTFORM \_ IST \_ \_ \_ \_ \_ VERALTET)**
</dt> <dd>

Die Plattform ist veraltet.

</dd> <dt>

<span id="MP_STATUS_FLAG_END_OF_LIFE"></span><span id="mp_status_flag_end_of_life"></span>**MP \_ STATUS \_ FLAG \_ END \_ OF \_ LIFE**
</dt> <dd>

Die Signatur oder das Ende der Lebensdauer der Plattform ist abgelaufen oder steht aus.

</dd> <dt>

<span id="MP_STATUS_FLAG_MAX"></span><span id="mp_status_flag_max"></span>**MP \_ STATUS \_ FLAG \_ MAX**
</dt> <dd>

Maximal gültiges Flag.

</dd> <dt>

<span id="MP_STATUS_FLAG_ALL"></span><span id="mp_status_flag_all"></span>**MP \_ STATUS \_ FLAG \_ ALL**
</dt> <dd>

Maximalwert möglich.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





