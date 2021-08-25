---
title: MPTHREAT_INFO -Struktur (MpClient.h)
description: Enthält Informationen zu einer Bedrohung.
ms.assetid: ED2A0BDB-0E7C-479D-ADA1-95B9A259F57E
keywords:
- MPTHREAT_INFO struktur Legacy Windows Umgebungsfeatures
- PMPTHREAT_INFO strukturzeiger Legacy-Windows-Umgebungsfeatures
topic_type:
- apiref
api_name:
- MPTHREAT_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7be9b1f38a2771d7c6e4831e7716552de34492b30429084f3e087e0a3b49602
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943920"
---
# <a name="mpthreat_info-structure"></a>MPTHREAT \_ INFO-Struktur

Enthält Informationen zu einer Bedrohung.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPTHREAT_INFO {
  MPTHREAT_ID           ThreatID;
  GUID                  DetectionID;
  MP_MIDL_STRING LPWSTR Name;
  MPTHREAT_TYPE         ThreatType;
  MPTHREAT_SEVERITY     ThreatCriticality;
  MPTHREAT_CATEGORY     ThreatCategory;
  DWORD                 ThreatShortDescriptionID;
  DWORD                 ThreatAdviseDescriptionID;
  MPTHREAT_STATUS       ThreatStatus;
  DWORD                 SuggestedActionCount;
  MPTHREAT_ACTION       SuggestedActionArray[MP_MAX_SUGGESTIONS];
  DWORD                 ResourceCount;
  PMPRESOURCE_INFO      *ResourceList[ResourceCount];
  ULARGE_INTEGER        ThreatStatusTime;
  HRESULT               ThreatStatusCode;
  MPTHREAT_DETECTION    ThreatDetection;
  GUID                  QuarantineGuid;
  MPEXECUTION_STATUS    ExecutionStatus;
  union {
    PMPTHREAT_INFOEX_UNUSED   pKnownBad;
    PMPTHREAT_INFOEX_BEHAVIOR pBehavior;
    PMPTHREAT_INFOEX_UNUSED   pUnknown;
    PMPTHREAT_INFOEX_UNUSED   pKnownGood;
    PMPTHREAT_INFOEX_NIS      pNis;
  } Data;
  MPDETECTION_STATE     State;
  MP_MIDL_STRING LPWSTR DetectionUser;
  MPSOURCE              DetectionSource;
  MP_MIDL_STRING LPWSTR ProcessName;
  MPDETECTION_ORIGIN    DetectionOrigin;
  DWORD                 reserved1;
  ULARGE_INTEGER        DetectionTime;
  MPEXECUTION_STATUS    PreExecutionStatus;
  ULARGE_INTEGER        RemediationTime;
  MPEXECUTION_STATUS    PostExecutionStatus;
  BOOL                  CriticalFailure;
  DWORD                 NonCriticalReason;
  MP_MIDL_STRING LPWSTR RemediationUser;
  DWORD                 RemediationResourceCount;
  PMPRESOURCE_INFO      RemediationResourceList[RemediationResourceCount];
  BOOL                  FailureResolved;
  MPRESOLVED_REASON     ResolvedReason;
  DWORD                 AdditionalActions;
  DWORD                 ResolvedActions;
  DWORD                 dwThreatStatusFlag;
} MPTHREAT_INFO, *PMPTHREAT_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**ThreatID**
</dt> <dd>

Typ: **MPTHREAT-ID \_**

</dd> <dd>

Bedrohungsbezeichner. Oberes Bit wird festgelegt, um Bedrohungen im Zusammenhang mit Antivirensoftware zu identifizieren.

</dd> <dt>

**DetectionID**
</dt> <dd>

Typ: **GUID**

</dd> <dd>

Erkennungs-ID.

</dd> <dt>

**Name**
</dt> <dd>

Typ: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Bedrohungsname.

</dd> <dt>

**ThreatType**
</dt> <dd>

Typ: **[ **MPTHREAT \_ TYPE**](mpthreat-type.md)**

</dd> <dd>

Bedrohungstyp. Wird verwendet, um zwischen verschiedenen Bedrohungstypen zu unterscheiden, z. B. als "schlecht", "unbekannt" oder "bekannt gut". Siehe [**MPTHREAT \_ TYPE**](mpthreat-type.md).

</dd> <dt>

**ThreatCriticality**
</dt> <dd>

Typ: **[ **MPTHREAT \_ SEVERITY**](mpthreat-severity.md)**

</dd> <dd>

Bedrohungskritischität. Weitere Informationen [**finden Sie unter MPTHREAT \_ SEVERITY (MPTHREAT-SCHWEREGRAD).**](mpthreat-severity.md)

</dd> <dt>

**ThreatCategory**
</dt> <dd>

Typ: **[ **MPTHREAT \_ CATEGORY**](mpthreat-category.md)**

</dd> <dd>

Bedrohungskategorie, z. B. ein Trojaner oder ein Keylogger. Siehe [**MPTHREAT \_ CATEGORY**](mpthreat-category.md).

</dd> <dt>

**ThreatShortDescriptionID**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Kurzbeschreibungs-ID der Bedrohung.

</dd> <dt>

**ThreatAdviseDescriptionID**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Beschreibungs-ID der Bedrohungsbeschreibung.

</dd> <dt>

**ThreatStatus**
</dt> <dd>

Typ: **[ **MPTHREAT \_ STATUS**](mpthreat-status.md)**

</dd> <dd>

Bedrohungsstatus, z. B. erkannt, bereinigt oder unter Quarantäne gestellt. Weitere Informationen [**finden Sie unter MPTHREAT \_ STATUS**](mpthreat-status.md).

</dd> <dt>

**SuggestedActionCount**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Anzahl der vorgeschlagenen Aktionen in **SuggestedActionArray**.

</dd> <dt>

**SuggestedActionArray**
</dt> <dd>

Typ: **[**MPTHREAT \_ ACTION MP**](mpthreat-action.md) \[ MAX \_ \_ SUGGESTIONS\]**

</dd> <dd>

Array von vorgeschlagenen Aktionen. Siehe [**MPTHREAT \_ ACTION**](mpthreat-action.md).

</dd> <dt>

**ResourceCount**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Anzahl der Ressourcen in **ResourceList**.

</dd> <dt>

**ResourceList**
</dt> <dd>

Typ: **PMPRESOURCE \_ INFO \***

</dd> <dd>

Liste der Ressourcen, die mit der Bedrohung identifiziert wurden. Weitere Informationen [**finden Sie unter MPRESOURCE \_ INFO**](mpresource-info.md).

</dd> <dt>

**ThreatStatusTime**
</dt> <dd>

Typ: **ULARGE \_ INTEGER**

</dd> <dd>

Zeitpunkt der letzten Änderung des Bedrohungsstatus.

</dd> <dt>

**ThreatStatusCode**
</dt> <dd>

Typ: **HRESULT**

</dd> <dd>

Statuscode, der dem Bedrohungsstatus zugeordnet ist.

</dd> <dt>

**ThreatDetection**
</dt> <dd>

Typ: **[ **MPTHREAT \_ DETECTION**](mpthreat-detection.md)**

</dd> <dd>

Bedrohungserkennungstyp, z. B. konkrete, verdächtige oder generische Bedrohungen. Weitere Informationen [**finden Sie unter MPTHREAT DETECTION ( MPTHREAT-ERKENNUNG). \_**](mpthreat-detection.md)

</dd> <dt>

**QuarantineGuid**
</dt> <dd>

Typ: **GUID**

</dd> <dd>

Quarantäne-GUID.

</dd> <dt>

**ExecutionStatus**
</dt> <dd>

Typ: **[ **MPEXECUTION \_ STATUS**](mpexecution-status.md)**

</dd> <dd>

Ausführungsstatus der Bedrohung, z. B. nicht bekannt, blockiert oder aktiv. Weitere Informationen [**finden Sie unter MPEXECUTION \_ STATUS**](mpexecution-status.md).

</dd> <dt>

**Daten**
</dt> <dd>

Zusätzliche Informationen. Der Zeiger auf die entsprechende Struktur hängt vom Wert von **ThreatType ab.**

<dl> <dt>

**pKnownBad**
</dt> <dd>

Typ: **PMPTHREAT \_ INFOEX \_ NICHT VERWENDET**

</dd> <dd>

Wenn **ThreatType**  ==  **MPTHREAT \_ TYPE \_ KNOWNBAD**. Weitere Informationen [**finden Sie unter MPTHREAT \_ INFOEX \_ UNUSED**](mpthreat-infoex-unused.md).

</dd> <dt>

**pBehavior**
</dt> <dd>

Typ: **PMPTHREAT \_ INFOEX \_ BEHAVIOR**

</dd> <dd>

Wenn **ThreatType**  ==  **MPTHREAT \_ TYPE BEHAVIOR \_ .** Siehe [**MPTHREAT INFOEX BEHAVIOR (MPTHREAT \_ \_ INFOEX-VERHALTEN).**](mpthreat-infoex-behavior.md)

</dd> <dt>

**pUnknown**
</dt> <dd>

Typ: **PMPTHREAT \_ INFOEX \_ NICHT VERWENDET**

</dd> <dd>

Wenn **ThreatType**  ==  **MPTHREAT \_ TYPE UNKNOWN \_ ist.** Weitere Informationen [**finden Sie unter MPTHREAT \_ INFOEX \_ UNUSED**](mpthreat-infoex-unused.md).

</dd> <dt>

**pKnownGood**
</dt> <dd>

Typ: **PMPTHREAT \_ INFOEX \_ NICHT VERWENDET**

</dd> <dd>

When **ThreatType** == MPTHREAT \_ TYPE \_ KNOWNGOOD. Weitere Informationen [**finden Sie unter MPTHREAT \_ INFOEX \_ UNUSED**](mpthreat-infoex-unused.md).

</dd> <dt>

**pNis**
</dt> <dd>

Typ: **PMPTHREAT \_ INFOEX \_ NIS**

</dd> <dd>

Wenn **ThreatType**  ==  **MPTHREAT \_ TYPE \_ NIS.** Weitere Informationen [**finden Sie unter MPTHREAT \_ INFOEX \_ NIS**](mpthreat-infoex-nis.md).

</dd> </dl> </dd> <dt>

**State**
</dt> <dd>

Typ: **[ **MPDETECTION \_ STATE**](mpdetection-state.md)**

</dd> <dd>

Der aktuelle Status der Erkennung. Weitere Informationen [**finden Sie unter MPDETECTION \_ STATE**](mpdetection-state.md).

</dd> <dt>

**DetectionUser**
</dt> <dd>

Typ: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Der der Erkennung zugeordnete Benutzer im Format "Domäne/Benutzer".

</dd> <dt>

**DetectionSource**
</dt> <dd>

Typ: **[ **MPSOURCE**](mpsource.md)**

</dd> <dd>

Die Quelle der Erkennung. Siehe [**MPSOURCE**](mpsource.md).

</dd> <dt>

**ProcessName**
</dt> <dd>

Typ: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Prozessname, der der Erkennung zugeordnet ist.

</dd> <dt>

**DetectionOrigin**
</dt> <dd>

Typ: **[ **MPDETECTION \_ ORIGIN**](mpdetection-origin.md)**

</dd> <dd>

Der Ursprung der Erkennung, z. B. lokal oder netzwerk. Siehe [**MPDETECTION \_ ORIGIN**](mpdetection-origin.md).

</dd> <dt>

**reserviert1**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Reservierte Metadaten zur Erkennung.

</dd> <dt>

**DetectionTime**
</dt> <dd>

Typ: **ULARGE \_ INTEGER**

</dd> <dd>

Der Zeitpunkt der ersten Erkennung.

</dd> <dt>

**PreExecutionStatus**
</dt> <dd>

Typ: **[ **MPEXECUTION \_ STATUS**](mpexecution-status.md)**

</dd> <dd>

Ausführungsstatus direkt vor der Wiederherstellung. Siehe [**MPEXECUTION \_ STATUS**](mpexecution-status.md).

</dd> <dt>

**RemediationTime**
</dt> <dd>

Typ: **ULARGE \_ INTEGER**

</dd> <dd>

Die Zeit, zu der die Wiederherstellung aufgetreten ist.

</dd> <dt>

**PostExecutionStatus**
</dt> <dd>

Typ: **[ **MPEXECUTION \_ STATUS**](mpexecution-status.md)**

</dd> <dd>

Ausführungsstatus nach der Wiederherstellung. Siehe [**MPEXECUTION \_ STATUS**](mpexecution-status.md).

</dd> <dt>

**CriticalFailure**
</dt> <dd>

Typ: **BOOL**

</dd> <dd>

True, wenn der Wiederherstellungsfehler kritisch war.

</dd> <dt>

**NonCriticalReason**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Der Grund für den Fehler bei der Wiederherstellung ist nicht kritisch. Dies wird in Zukunft nicht garantiert.

</dd> <dt>

**RemediationUser**
</dt> <dd>

Typ: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Benutzer, der die Wiederherstellung angefordert hat, im Format "Domäne/Benutzer".

</dd> <dt>

**RemediationResourceCount**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Anzahl der Ressourcen in **RemediationResourceList**.

</dd> <dt>

**RemediationResourceList**
</dt> <dd>

Typ: **PMPRESOURCE \_ INFO \[ RemediationResourceCount \]**

</dd> <dd>

Liste der Ressourcen, bei denen während der Wiederherstellung ein Fehler aufgetreten ist. Weitere Informationen finden Sie unter [**MPRESOURCE \_ INFO**](mpresource-info.md).

</dd> <dt>

**Fehler Behoben**
</dt> <dd>

Typ: **BOOL**

</dd> <dd>

True, wenn ein Wiederherstellungsfehler behoben wurde. Dadurch wird der Bucket entweder in "Abgeschlossen" oder in eine zusätzliche Aktion verschoben.

</dd> <dt>

**ResolvedReason**
</dt> <dd>

Typ: **[ **MPRESOLVED \_ REASON**](mpresolved-reason.md)**

</dd> <dd>

Ursache für behebungsfehler. Dies ist der Grund, warum die Erkennung von "Failed" in "Additional Action" verschoben oder abgeschlossen wurde. Weitere Informationen finden Sie unter [**MPRESOLVED \_ REASON**](mpresolved-reason.md).

</dd> <dt>

**AdditionalActions**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Sind zusätzliche Aktionen erforderlich.

</dd> <dt>

**ResolvedActions**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Alle zusätzlichen Aktionen, die ausgeführt wurden.

</dd> <dt>

**dwThreatStatusFlag**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Fügen Sie zusätzliche Informationen zur Bedrohungserkennung hinzu.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MpFreeMemory**](mpfreememory.md)
</dt> <dt>

[**MpThreatEnumerate**](mpthreatenumerate.md)
</dt> <dt>

[**MpThreatQuery**](mpthreatquery.md)
</dt> <dt>

[**MPDETECTION \_ ORIGIN**](mpdetection-origin.md)
</dt> <dt>

[**\_MPDETECTION-ZUSTAND**](mpdetection-state.md)
</dt> <dt>

[**MPEXECUTION-STATUS \_**](mpexecution-status.md)
</dt> <dt>

[**MPRESOLVED \_ REASON**](mpresolved-reason.md)
</dt> <dt>

[**\_MPRESOURCE-INFORMATIONEN**](mpresource-info.md)
</dt> <dt>

[**MPSOURCE**](mpsource.md)
</dt> <dt>

[**\_MPTHREAT-AKTION**](mpthreat-action.md)
</dt> <dt>

[**MPTHREAT \_ CATEGORY**](mpthreat-category.md)
</dt> <dt>

[**\_MPTHREAT-ERKENNUNG**](mpthreat-detection.md)
</dt> <dt>

[**MPTHREAT \_ \_ INFOEX-VERHALTEN**](mpthreat-infoex-behavior.md)
</dt> <dt>

[**MPTHREAT \_ INFOEX \_ NIS**](mpthreat-infoex-nis.md)
</dt> <dt>

[**MPTHREAT \_ INFOEX \_ UNUSED**](mpthreat-infoex-unused.md)
</dt> <dt>

[**\_MPTHREAT-SCHWEREGRAD**](mpthreat-severity.md)
</dt> <dt>

[**\_MPTHREAT-STATUS**](mpthreat-status.md)
</dt> <dt>

[**\_MPTHREAT-TYP**](mpthreat-type.md)
</dt> </dl>

 

 





