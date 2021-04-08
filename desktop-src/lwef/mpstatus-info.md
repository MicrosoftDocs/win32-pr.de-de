---
title: MPSTATUS_INFO Struktur (mpclient. h)
description: Status Informationen für den Malware Schutz-Manager.
ms.assetid: 614F14EC-64CC-4E3F-8A89-42AA1E0DC95D
keywords:
- MPSTATUS_INFO Struktur Funktionen der Legacy-Windows-Umgebung
- PMPSTATUS_INFO Struktur Zeiger Legacy-Windows-Umgebungs Features
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
ms.openlocfilehash: efe31981f819d85d13457553beb1ce3c869b98bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740129"
---
# <a name="mpstatus_info-structure"></a>Mpstatus- \_ Informationsstruktur

Status Informationen für den Malware Schutz-Manager.

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

**Productstatus**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Gesamtprodukt Status. Dies ist eine Kombination von Bitflags aus dem [**mpstatus- \_ Flag**](mpstatus-flag.md).

</dd> <dt>

**Lastquickscan**
</dt> <dd>

Typ: **[ **mpscan- \_ Ergebnis**](mpscan-result.md)**

</dd> <dd>

Ergebnisse der letzten Überprüfung durch den Malware Schutz-Manager. Siehe [**mpscan- \_ Ergebnis**](mpscan-result.md).

</dd> <dt>

**Lastfullscan**
</dt> <dd>

Typ: **[ **mpscan- \_ Ergebnis**](mpscan-result.md)**

</dd> <dd>

Ergebnisse der letzten vollständigen Überprüfung durch den Malware Schutz-Manager. Siehe [**mpscan- \_ Ergebnis**](mpscan-result.md).

</dd> <dt>

**Bedrohlich stats**
</dt> <dd>

Typ: **[ **mpthreat- \_ Statistik**](mpthreat-stats.md)**

</dd> <dd>

Aktive Bedrohungs Statistiken. Siehe [**mpthreat \_ Stats**](mpthreat-stats.md).

</dd> <dt>

**Status**
</dt> <dd>

Typ: **[**mpthreat \_ Stats \_ Data**](mpthreat-stats-data.md) \[ MP \_ Threat \_ stat \_ maximal \_ Wert + 1\]**

</dd> <dd>

Zusätzliche Bedrohungs Statistikdaten, z. b. die Anzahl der Bedrohungen. Siehe [**mpthreat \_ Stats- \_ Daten**](mpthreat-stats-data.md).

</dd> <dt>

**Komponente**
</dt> <dd>

Typ: **[**mpcomponent- \_ Status**](mpcomponent-status.md) \[ mpcomponent \_ MaxValue + 1\]**

</dd> <dd>

Ein Array von Status für mehrere Komponenten. Verwenden Sie einen Wert aus der [**mpcomponent- \_ ID**](mpcomponent-id.md) -Enumeration als Index in das Array.

</dd> <dt>

**Productexpirationtime**
</dt> <dd>

Typ: **ularge \_ Integer**

</dd> <dd>

Zeitstempel für den Produktablauf in UNC. Dies ist nur gültig, wenn der Ablauf Status auf festgelegt ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**mpcomponent- \_ ID**](mpcomponent-id.md)
</dt> <dt>

[**mpcomponent- \_ Status**](mpcomponent-status.md)
</dt> <dt>

[**mpscan- \_ Ergebnis**](mpscan-result.md)
</dt> <dt>

[**\_mpstatusflag**](mpstatus-flag.md)
</dt> <dt>

[**mpthreat- \_ Statistik**](mpthreat-stats.md)
</dt> <dt>

[**mpthreat- \_ Statistik \_ Daten**](mpthreat-stats-data.md)
</dt> </dl>

 

 





