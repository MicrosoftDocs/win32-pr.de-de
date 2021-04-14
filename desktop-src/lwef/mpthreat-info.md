---
title: MPTHREAT_INFO Struktur (mpclient. h)
description: Enthält Informationen zu einer Bedrohung.
ms.assetid: ED2A0BDB-0E7C-479D-ADA1-95B9A259F57E
keywords:
- MPTHREAT_INFO Struktur Funktionen der Legacy-Windows-Umgebung
- PMPTHREAT_INFO Struktur Zeiger Legacy-Windows-Umgebungs Features
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
ms.openlocfilehash: dfa850a4293006a2f4b107a3f2579fdc14c1ea6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478738"
---
# <a name="mpthreat_info-structure"></a>Mpthreat- \_ Informationsstruktur

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

**Threatid**
</dt> <dd>

Typ: **mpthreat- \_ ID**

</dd> <dd>

Bedrohungs Bezeichner. Das obere Bit ist festgelegt, um antivirenbezogene Bedrohungen zu identifizieren.

</dd> <dt>

**Detectionid**
</dt> <dd>

Typ: **GUID**

</dd> <dd>

Erkennungs-ID.

</dd> <dt>

**Name**
</dt> <dd>

Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**

</dd> <dd>

Bedrohungs Name.

</dd> <dt>

**Typ**
</dt> <dd>

Typ: **[ **mpthreat- \_ Typ**](mpthreat-type.md)**

</dd> <dd>

Bedrohungstyp. Wird zur Unterscheidung zwischen unterschiedlichen Bedrohungs Typen verwendet, wie z. b. bekanntermaßen "schlecht", "unbekannt" Siehe [**mpthreat- \_ Typ**](mpthreat-type.md).

</dd> <dt>

**Gefährlichkeit**
</dt> <dd>

Typ: **[ **mpthreat- \_ Schweregrad**](mpthreat-severity.md)**

</dd> <dd>

Bedrohungs Gefahr. Siehe [**mpthreat- \_ Schweregrad**](mpthreat-severity.md).

</dd> <dt>

**ThreatCategory**
</dt> <dd>

Typ: **[ **mpthreat- \_ Kategorie**](mpthreat-category.md)**

</dd> <dd>

Bedrohungs Kategorie, z. b. ein Trojaner oder eine Keylogger. Siehe [**mpthreat- \_ Kategorie**](mpthreat-category.md).

</dd> <dt>

**"Bedrohlich shortdescriptionid"**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

ID der Bedrohungs Kurzbeschreibung.

</dd> <dt>

**"Bedrohlich advimendescriptionid"**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

ID der Bedrohungs Empfehlung.

</dd> <dt>

**ThreatStatus**
</dt> <dd>

Typ: **[ **mpthreat- \_ Status**](mpthreat-status.md)**

</dd> <dd>

Bedrohungs Status, z. b. erkannt, bereinigt oder unter Quarantäne. Siehe [**mpthreat- \_ Status**](mpthreat-status.md).

</dd> <dt>

**Vorschlags stedactioncount**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Anzahl der vorgeschlagenen Aktionen in "Vorschlags **stedactionarray**".

</dd> <dt>

**Vorschlag**
</dt> <dd>

Typ: **[**mpthreat \_ Action**](mpthreat-action.md) \[ MP \_ Maximale \_ Vorschläge\]**

</dd> <dd>

Array von vorgeschlagenen Aktionen. Siehe [**mpthreat- \_ Aktion**](mpthreat-action.md).

</dd> <dt>

**ResourceCount**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Anzahl der Ressourcen in **resourceList**.

</dd> <dt>

**ResourceList**
</dt> <dd>

Typ: **pmpresource \_ Info \** _

</dd> <dd>

Liste der mit der Bedrohung identifizierten Ressourcen. Weitere Informationen finden Sie unter [_ *mpresource- \_ Informationen* *](mpresource-info.md).

</dd> <dt>

**Bedrohung**
</dt> <dd>

Typ: **ularge \_ Integer**

</dd> <dd>

Zeitpunkt, zu dem der Bedrohungs Status zuletzt geändert wurde.

</dd> <dt>

**"Bedrohlich Statuscode"**
</dt> <dd>

Typ: **HRESULT**

</dd> <dd>

Statuscode, der mit dem Bedrohungs Status verknüpft ist.

</dd> <dt>

**Erkennung**
</dt> <dd>

Typ: **[ **mpthreat- \_ Erkennung**](mpthreat-detection.md)**

</dd> <dd>

Bedrohungs Erkennungs Typen, z. b. konkret, verdächtig oder generisch. Siehe [**mpthreat- \_ Erkennung**](mpthreat-detection.md).

</dd> <dt>

**Quarantäne-GUID**
</dt> <dd>

Typ: **GUID**

</dd> <dd>

Quarantäne-GUID.

</dd> <dt>

**ExecutionStatus**
</dt> <dd>

Typ: **[ **mpexecution- \_ Status**](mpexecution-status.md)**

</dd> <dd>

Ausführungs Status der Bedrohung, z. b. nicht bekannt, blockiert oder aktiv. Siehe [**mpexecution- \_ Status**](mpexecution-status.md).

</dd> <dt>

**Daten**
</dt> <dd>

Weitere Informationen. Der Zeiger auf die entsprechende-Struktur hängt vom Wert von "- **Typ**" ab.

<dl> <dt>

**pknownbad**
</dt> <dd>

Typ: **pmpthreat \_ INFOEX nicht \_ verwendet**

</dd> <dd>

Wenn der **Typ**  ==  **mpthreat den \_ Typ \_ knownbad** hat. Weitere Informationen finden Sie unter [**mpthreat \_ INFOEX nicht \_ verwendet**](mpthreat-infoex-unused.md).

</dd> <dt>

**pbehavior**
</dt> <dd>

Typ: **pmpthreat \_ INFOEX- \_ Verhalten**

</dd> <dd>

Wenn der **Typ**  ==  **mpthreat \_ Type \_ Verhalten** hat. Siehe [**mpthreat \_ INFOEX- \_ Verhalten**](mpthreat-infoex-behavior.md).

</dd> <dt>

**pUnknown**
</dt> <dd>

Typ: **pmpthreat \_ INFOEX nicht \_ verwendet**

</dd> <dd>

Wenn **der Typ**  ==  **mpthreat \_ Type \_ unbekannt** ist. Weitere Informationen finden Sie unter [**mpthreat \_ INFOEX nicht \_ verwendet**](mpthreat-infoex-unused.md).

</dd> <dt>

**pknowngood**
</dt> <dd>

Typ: **pmpthreat \_ INFOEX nicht \_ verwendet**

</dd> <dd>

Wenn **gefährtype** = = mpthreat \_ Type \_ knowngood ist. Weitere Informationen finden Sie unter [**mpthreat \_ INFOEX nicht \_ verwendet**](mpthreat-infoex-unused.md).

</dd> <dt>

**pnis**
</dt> <dd>

Typ: **pmpthreat \_ INFOEX \_ NIS**

</dd> <dd>

Wenn der **Typ**  ==  **mpthreat \_ Type \_ NIS** ist. Weitere Informationen finden Sie unter [**mpthreat \_ INFOEX \_ NIS**](mpthreat-infoex-nis.md).

</dd> </dl> </dd> <dt>

**State**
</dt> <dd>

Typ: **[ **mperkennungs- \_ Status**](mpdetection-state.md)**

</dd> <dd>

Der aktuelle Zustand der Erkennung. Siehe [**mperkennungs- \_ Status**](mpdetection-state.md).

</dd> <dt>

**Erkenctionuser**
</dt> <dd>

Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**

</dd> <dd>

Der Benutzer, der der Erkennung zugeordnet ist, im Format "Domäne/Benutzer".

</dd> <dt>

**Detectionsource**
</dt> <dd>

Typ: **[ **mpsource**](mpsource.md)**

</dd> <dd>

Die Quelle der Erkennung. Siehe [**mpsource**](mpsource.md).

</dd> <dt>

**ProcessName**
</dt> <dd>

Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**

</dd> <dd>

Der Prozess Name, der der Erkennung zugeordnet ist.

</dd> <dt>

**Detectionorigin**
</dt> <dd>

Typ: **[ **mperkennungs- \_ Ursprung**](mpdetection-origin.md)**

</dd> <dd>

Der Ursprung der Erkennung, z. b. local oder Network. Siehe [**mperkennungs- \_ Ursprung**](mpdetection-origin.md).

</dd> <dt>

**"reserved1"**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Reservierte Metadaten zur Erkennung.

</dd> <dt>

**Erkenctiontime**
</dt> <dd>

Typ: **ularge \_ Integer**

</dd> <dd>

Der Zeitpunkt der ersten Erkennung.

</dd> <dt>

**Preexecutionstatus**
</dt> <dd>

Typ: **[ **mpexecution- \_ Status**](mpexecution-status.md)**

</dd> <dd>

Ausführungs Status direkt vor der Wiederherstellung. Siehe [**mpexecution- \_ Status**](mpexecution-status.md).

</dd> <dt>

**Wiederbehebe Zeit**
</dt> <dd>

Typ: **ularge \_ Integer**

</dd> <dd>

Die Zeit für die Wiederherstellung.

</dd> <dt>

**Postexecutionstatus**
</dt> <dd>

Typ: **[ **mpexecution- \_ Status**](mpexecution-status.md)**

</dd> <dd>

Ausführungs Status nach der Wiederherstellung. Siehe [**mpexecution- \_ Status**](mpexecution-status.md).

</dd> <dt>

**CriticalFailure**
</dt> <dd>

Typ: **bool**

</dd> <dd>

True, wenn der Wiederherstellungs Fehler kritisch war.

</dd> <dt>

**Nicht criticalreason**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Der Grund für den Fehler bei der Wiederherstellung ist nicht wichtig. Dies wird in Zukunft nicht garantiert unterstützt.

</dd> <dt>

**Wiederbeheationuser**
</dt> <dd>

Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**

</dd> <dd>

Der Benutzer, der die Wiederherstellung angefordert hat, im Format Domäne/Benutzer.

</dd> <dt>

**Wiederbeheationresourcecount**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Anzahl der Ressourcen in der **wiederbehebe**-Ressourcen Liste.

</dd> <dt>

**Wiederherstellung von wiedersourcelist**
</dt> <dd>

Typ: **pmpresource \_ Info \[ wiederbeheationresourcecount \]**

</dd> <dd>

Liste der Ressourcen, die während der Wiederherstellung nicht erfolgreich waren Informationen finden Sie unter [**mpresource- \_ Informationen**](mpresource-info.md).

</dd> <dt>

**Failureresolved**
</dt> <dd>

Typ: **bool**

</dd> <dd>

True, wenn der Wiederherstellungs Fehler behoben wurde. Dadurch wird der Bucket entweder auf Complete oder eine zusätzliche Aktion verschoben.

</dd> <dt>

**Resolvedreason**
</dt> <dd>

Typ: **[ **mpregelöste \_ Ursache**](mpresolved-reason.md)**

</dd> <dd>

Der Grund für die Behebung des Fehlers bei der Wiederherstellung. Dies ist der Grund, warum die Erkennung von nicht zu weiteren Aktionen verschoben wurde oder abgeschlossen wurde. Weitere Informationen finden Sie unter [**mpregelöste \_ reason**](mpresolved-reason.md).

</dd> <dt>

**Additionalactions**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Sind zusätzliche Aktionen erforderlich.

</dd> <dt>

**Resolvedactions**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Alle weiteren Aktionen, die ausgeführt wurden.

</dd> <dt>

**dwbilistatusflag**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Zusätzliche Informationen zur Bedrohungserkennung.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mpfrememory**](mpfreememory.md)
</dt> <dt>

[**Mpzerenumerate**](mpthreatenumerate.md)
</dt> <dt>

[**Mpbedrohlich Query**](mpthreatquery.md)
</dt> <dt>

[**mperkennungs- \_ Ursprung**](mpdetection-origin.md)
</dt> <dt>

[**mperkennungs- \_ Status**](mpdetection-state.md)
</dt> <dt>

[**mpexecution- \_ Status**](mpexecution-status.md)
</dt> <dt>

[**mpregelösten \_ Grund**](mpresolved-reason.md)
</dt> <dt>

[**mpresource- \_ Informationen**](mpresource-info.md)
</dt> <dt>

[**Mpsource**](mpsource.md)
</dt> <dt>

[**mpthreat- \_ Aktion**](mpthreat-action.md)
</dt> <dt>

[**mpthreat- \_ Kategorie**](mpthreat-category.md)
</dt> <dt>

[**mpthreat- \_ Erkennung**](mpthreat-detection.md)
</dt> <dt>

[**mpthreat- \_ INFOEX- \_ Verhalten**](mpthreat-infoex-behavior.md)
</dt> <dt>

[**mpthreat \_ INFOEX \_ NIS**](mpthreat-infoex-nis.md)
</dt> <dt>

[**mpthreat \_ INFOEX nicht \_ verwendet**](mpthreat-infoex-unused.md)
</dt> <dt>

[**mpthreat- \_ Schweregrad**](mpthreat-severity.md)
</dt> <dt>

[**mpthreat- \_ Status**](mpthreat-status.md)
</dt> <dt>

[**mpthreat- \_ Typ**](mpthreat-type.md)
</dt> </dl>

 

 





