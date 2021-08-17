---
title: MPSCAN_RESULT-Struktur (MpClient.h)
description: Die Ergebnisse einer Überprüfung.
ms.assetid: 9031A371-092A-4175-BE1D-90442A5BED2D
keywords:
- MPSCAN_RESULT struktur legacy Windows Environment Features (Legacy-Windows-Umgebungsfeatures)
- PMPSCAN_RESULT Strukturzeiger Legacy Windows Umgebungsfeatures
topic_type:
- apiref
api_name:
- MPSCAN_RESULT
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a41efd40529976d4b7fe639c4907729ed39ae261f5ac644faf1a36e1a213a97e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747151"
---
# <a name="mpscan_result-structure"></a>MPSCAN \_ RESULT-Struktur

Die Ergebnisse einer Überprüfung.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPSCAN_RESULT {
  MPSCAN_TYPE      ScanType;
  MPSOURCE         Source;
  GUID             ScanGuid;
  ULARGE_INTEGER   StartTime;
  ULARGE_INTEGER   EndTime;
  MPTHREAT_STATS   ThreatStats;
  MPRESOURCE_STATS ResourceStats;
  ULONGLONG        SignatureVersion;
} MPSCAN_RESULT, *PMPSCAN_RESULT;
```



## <a name="members"></a>Member

<dl> <dt>

**ScanType**
</dt> <dd>

Typ: **[ **\_ MPSCAN-TYP**](mpscan-type.md)**

</dd> <dd>

Scantyp. Siehe [**\_ MPSCAN-TYP.**](mpscan-type.md)

</dd> <dt>

**Quelle**
</dt> <dd>

Typ: **[ **MPSOURCE**](mpsource.md)**

</dd> <dd>

Scanquelle, z. B. vom Benutzer oder vom System initiiert. Siehe [**MPSOURCE**](mpsource.md).

</dd> <dt>

**ScanGuid**
</dt> <dd>

Typ: **GUID**

</dd> <dd>

Überprüfungsbezeichner.

</dd> <dt>

**StartTime**
</dt> <dd>

Typ: **ULARGE \_ INTEGER**

</dd> <dd>

Startzeit der Überprüfung.

</dd> <dt>

**EndTime**
</dt> <dd>

Typ: **ULARGE \_ INTEGER**

</dd> <dd>

Endzeit der Überprüfung.

</dd> <dt>

**ThreatStats**
</dt> <dd>

Typ: **[ **MPTHREAT \_ STATS**](mpthreat-stats.md)**

</dd> <dd>

Bedrohungsbezogene Statistiken. Siehe [**MPTHREAT \_ STATS**](mpthreat-stats.md).

</dd> <dt>

**ResourceStats**
</dt> <dd>

Typ: **[ **MPRESOURCE \_ STATS**](mpresource-stats.md)**

</dd> <dd>

Ressourcenbezogene Statistiken. Weitere Informationen finden Sie [**unter MPRESOURCE-STATISTIKEN. \_**](mpresource-stats.md)

</dd> <dt>

**SignatureVersion**
</dt> <dd>

Typ: **ULONGLONG**

</dd> <dd>

Version der Signatur, die für die Überprüfung verwendet wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_MPRESOURCE-STATISTIKEN**](mpresource-stats.md)
</dt> <dt>

[**\_MPSCAN-TYP**](mpscan-type.md)
</dt> <dt>

[**MPSOURCE**](mpsource.md)
</dt> <dt>

[**\_MPTHREAT-STATISTIKEN**](mpthreat-stats.md)
</dt> </dl>

 

 





