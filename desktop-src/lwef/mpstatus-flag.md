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
# <a name="mpstatus_flag-enumeration"></a>Mpstatusflag- \_ Enumeration

Mögliche allgemeine Bitflags für den Produktstatus.

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

<span id="MP_STATUS_FLAG_NONE"></span><span id="mp_status_flag_none"></span>**MP \_ - \_ Statusflag \_ None**
</dt> <dd>

Es wurden keine Statusflags festgelegt (nicht initialisierter Zustand).

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_UNAVAILABLE"></span><span id="mp_status_flag_service_unavailable"></span>**MP \_ - \_ statusflagdienst nicht \_ \_ verfügbar**
</dt> <dd>

Der Dienst wird nicht ausgeführt.

</dd> <dt>

<span id="MP_STATUS_FLAG_MPENGINE_UNAVAILABLE"></span><span id="mp_status_flag_mpengine_unavailable"></span>**MP- \_ Status \_ Flag " \_ mpengine nicht \_ verfügbar"**
</dt> <dd>

Der Dienst wurde ohne Malware Schutz Modul gestartet.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_FULLSCAN_REQUIRED"></span><span id="mp_status_flag_threat_fullscan_required"></span>**MP \_ - \_ Statusflag \_ Threat \_ FULLSCAN \_ erforderlich**
</dt> <dd>

Ausstehende vollständige Überprüfung aufgrund von Bedrohungs Aktion.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_REBOOT_REQUIRED"></span><span id="mp_status_flag_threat_reboot_required"></span>**MP \_ - \_ Statusflag für \_ Bedrohungs \_ Neustart \_ erforderlich**
</dt> <dd>

Neustart aufgrund einer Bedrohungs Aktion steht aus.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_MANUAL_STEPS_REQUIRED"></span><span id="mp_status_flag_threat_manual_steps_required"></span>**MP \_ - \_ Statusflag, \_ \_ Manuelle \_ Schritte \_ erforderlich**
</dt> <dd>

Ausstehende manuelle Schritte aufgrund von Bedrohungs Aktionen.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_AV_SIGNATURE"></span><span id="mp_status_flag_due_av_signature"></span>**MP \_ - \_ Statusflag \_ aufgrund der \_ AV- \_ Signatur**
</dt> <dd>

Antivirensignaturen sind veraltet.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_AS_SIGNATURE"></span><span id="mp_status_flag_due_as_signature"></span>**MP \_ - \_ Statusflag \_ aufgrund der \_ \_ Signatur**
</dt> <dd>

Antispywaresignaturen sind veraltet.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_QUICK_SCAN"></span><span id="mp_status_flag_due_quick_scan"></span>**MP \_ - \_ Statusflag \_ aufgrund der \_ schnell \_ Überprüfung**
</dt> <dd>

Für einen angegebenen Zeitraum ist keine schnell Überprüfung erfolgt.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_FULL_SCAN"></span><span id="mp_status_flag_due_full_scan"></span>**MP \_ - \_ Statusflag \_ durch \_ vollständige \_ Überprüfung**
</dt> <dd>

in einem angegebenen Zeitraum ist keine vollständige Überprüfung erfolgt.

</dd> <dt>

<span id="MP_STATUS_FLAG_INPROGRESS_SYSTEM_SCAN"></span><span id="mp_status_flag_inprogress_system_scan"></span>**MP \_ - \_ Statusflag " \_ InProgress \_ System \_ Scan"**
</dt> <dd>

Vom System initiierte Überprüfung wird ausgeführt.

</dd> <dt>

<span id="MP_STATUS_FLAG_INPROGRESS_ROUTINE_CLEANING"></span><span id="mp_status_flag_inprogress_routine_cleaning"></span>**MP \_ - \_ Statusflag " \_ InProgress- \_ Routine \_ Reinigung"**
</dt> <dd>

Vom System initiierte Bereinigung wird ausgeführt.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_SAMPLES"></span><span id="mp_status_flag_due_samples"></span>**Verwaltungs Beispiele für MP- \_ \_ Statusflags \_ \_**
</dt> <dd>

Es sind Beispiele für ausstehende Übermittlung vorhanden.

</dd> <dt>

<span id="MP_STATUS_FLAG_EVALUATION_MODE"></span><span id="mp_status_flag_evaluation_mode"></span>**Bewertungsmodus für MP- \_ \_ Statusflag \_ \_**
</dt> <dd>

Das Produkt wird im Auswertungsmodus ausgeführt.

</dd> <dt>

<span id="MP_STATUS_FLAG_NONGENUINE"></span><span id="mp_status_flag_nongenuine"></span>**MP \_ - \_ Statusflag \_ nicht Original**
</dt> <dd>

Das Produkt wird im nicht Original-Windows-Modus ausgeführt.

</dd> <dt>

<span id="MP_STATUS_FLAG_PRODUCT_EXPIRED"></span><span id="mp_status_flag_product_expired"></span>**MP \_ - \_ Statusflag ist \_ \_ abgelaufen.**
</dt> <dd>

Das Produkt ist abgelaufen.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_CALLISTO_REQUIRED"></span><span id="mp_status_flag_threat_callisto_required"></span>**MP \_ - \_ Statusflag \_ Threat \_ Callisto \_ erforderlich**
</dt> <dd>

Callisto-Offline Überprüfung ist erforderlich.

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_ON_SYSTEM_SHUTDOWN"></span><span id="mp_status_flag_service_on_system_shutdown"></span>**MP \_ - \_ Statusflag- \_ Dienst \_ beim Herunterfahren des \_ Systems \_**
</dt> <dd>

Der Dienst wird im Rahmen des herunter Fahrens des Systems heruntergefahren.

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_critical_failure"></span>**kritischer Fehler des MP- \_ \_ Statusflags \_ \_ \_**
</dt> <dd>

Fehler bei der Bedrohungs Behebung.

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_NON_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_non_critical_failure"></span>**MP \_ - \_ Statusflag- \_ Dienst \_ nicht schwer \_ wiegender \_ Fehler**
</dt> <dd>

Die Bedrohungs Behebung ist nicht kritisch.

</dd> <dt>

<span id="MP_STATUS_FLAG_HEALTH_INITIALIZED"></span><span id="mp_status_flag_health_initialized"></span>**Status des MP- \_ \_ Statusflags \_ \_ Initialisiert**
</dt> <dd>

Es wurden keine Statusflags festgelegt (wohl initialisierter Zustand).

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_PLATFORM_UPDATE"></span><span id="mp_status_flag_due_platform_update"></span>**MP \_ - \_ Statusflag \_ aufgrund der \_ Platt Form \_ Aktualisierung**
</dt> <dd>

Die Plattform ist veraltet.

</dd> <dt>

<span id="MP_STATUS_FLAG_INPROGRESS_PLATFORM_UPDATE"></span><span id="mp_status_flag_inprogress_platform_update"></span>**MP \_ - \_ Statusflag " \_ InProgress \_ Platform \_ Update"**
</dt> <dd>

Das Platt Form Update wird ausgeführt.

</dd> <dt>

<span id="MP_STATUS_FLAG_PLATFORM_ABOUT_TO_BE_OUTDATED"></span><span id="mp_status_flag_platform_about_to_be_outdated"></span>**MP \_ - \_ Statusflag- \_ Plattform ist \_ \_ \_ \_ veraltet**
</dt> <dd>

Die Plattform ist veraltet.

</dd> <dt>

<span id="MP_STATUS_FLAG_END_OF_LIFE"></span><span id="mp_status_flag_end_of_life"></span>**MP \_ - \_ Statusflag- \_ Ende \_ des \_ Lebenszyklus**
</dt> <dd>

Die Signatur oder das Ende der Plattform ist abgelaufen oder steht aus.

</dd> <dt>

<span id="MP_STATUS_FLAG_MAX"></span><span id="mp_status_flag_max"></span>**MP \_ - \_ Statusflag \_ Max**
</dt> <dd>

Maximal gültiges Flag.

</dd> <dt>

<span id="MP_STATUS_FLAG_ALL"></span><span id="mp_status_flag_all"></span>**MP \_ - \_ Statusflag \_ alle**
</dt> <dd>

Maximal möglicher Wert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



 

 





