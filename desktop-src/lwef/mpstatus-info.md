---
title: MPSTATUS_INFO-Struktur (MpClient.h)
description: Statusinformationen für den Schadsoftwareschutz-Manager.
ms.assetid: 614F14EC-64CC-4E3F-8A89-42AA1E0DC95D
keywords:
- MPSTATUS_INFO struktur legacy Windows Environment Features (Legacy-Windows-Umgebungsfeatures)
- PMPSTATUS_INFO Strukturzeiger Legacy Windows Umgebungsfeatures
topic_type:
- apiref
api_name:
- MPSTATUS_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb93bd15fe05955c9e8d87828d4b94b08e3d577659c629b52b3f908cb045ba3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883301"
---
# <a name="mpstatus_info-structure"></a>MPSTATUS \_ INFO-Struktur

Statusinformationen für den Schadsoftwareschutz-Manager.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPSTATUS_INFO {
  DWORD               ProductStatus;
  MPSCAN_RESULT       LastQuickScan;
  MPSCAN_RESULT       LastFullScan;
  MPTHREAT_STATS      ThreatStats;
  MPTHREAT_STATS_DATA ThreatState[MP_THREAT_STAT_MAX_VALUE+1];
  MPCOMPONENT_STATUS  Component[MPCOMPONENT_MAXVALUE+1];
  ULARGE_INTEGER      ProductExpirationTime;
} MPSTATUS_INFO, *PMPSTATUS_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**ProductStatus**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Gesamter Produktstatus. Dies ist eine Kombination von Bitflags aus [**MPSTATUS \_ FLAG**](mpstatus-flag.md).

</dd> <dt>

**LastQuickScan**
</dt> <dd>

Typ: **[ **MPSCAN \_ RESULT**](mpscan-result.md)**

</dd> <dd>

Ergebnisse der letzten Überprüfung durch den Malwareschutz-Manager. Siehe [**\_ MPSCAN-ERGEBNIS.**](mpscan-result.md)

</dd> <dt>

**LastFullScan**
</dt> <dd>

Typ: **[ **MPSCAN \_ RESULT**](mpscan-result.md)**

</dd> <dd>

Ergebnisse der letzten vollständigen Überprüfung durch den Malwareschutz-Manager. Siehe [**\_ MPSCAN-ERGEBNIS.**](mpscan-result.md)

</dd> <dt>

**ThreatStats**
</dt> <dd>

Typ: **[ **MPTHREAT \_ STATS**](mpthreat-stats.md)**

</dd> <dd>

Statistiken zu aktiven Bedrohungen. Siehe [**MPTHREAT \_ STATS**](mpthreat-stats.md).

</dd> <dt>

**ThreatState**
</dt> <dd>

Typ: **[**MPTHREAT \_ STATS \_ DATA**](mpthreat-stats-data.md) \[ MP THREAT \_ \_ STAT MAX \_ \_ VALUE+1\]**

</dd> <dd>

Zusätzliche Daten zu Bedrohungsstatistiken, z. B. die Anzahl der Bedrohungen. Siehe [**MPTHREAT \_ STATS \_ DATA**](mpthreat-stats-data.md).

</dd> <dt>

**Komponente**
</dt> <dd>

Typ: **[**MPCOMPONENT \_ STATUS**](mpcomponent-status.md) \[ MPCOMPONENT \_ MAXVALUE+1\]**

</dd> <dd>

Ein Array von Status für mehrere Komponenten. Verwenden Sie einen Wert aus der [**MPCOMPONENT-ID-Enumeration \_**](mpcomponent-id.md) als Index für das Array.

</dd> <dt>

**ProductExpirationTime**
</dt> <dd>

Typ: **ULARGE \_ INTEGER**

</dd> <dd>

Produktablaufzeitstempel in UNC. Dies ist nur gültig, wenn der Ablaufstatus festgelegt ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MPCOMPONENT-ID \_**](mpcomponent-id.md)
</dt> <dt>

[**MPCOMPONENT-STATUS \_**](mpcomponent-status.md)
</dt> <dt>

[**\_MPSCAN-ERGEBNIS**](mpscan-result.md)
</dt> <dt>

[**\_MPSTATUS-FLAG**](mpstatus-flag.md)
</dt> <dt>

[**\_MPTHREAT-STATISTIKEN**](mpthreat-stats.md)
</dt> <dt>

[**\_MPTHREAT-STATISTIKDATEN \_**](mpthreat-stats-data.md)
</dt> </dl>

 

 





