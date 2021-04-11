---
title: MPSCAN_RESULT Struktur (mpclient. h)
description: Die Ergebnisse einer Überprüfung.
ms.assetid: 9031A371-092A-4175-BE1D-90442A5BED2D
keywords:
- MPSCAN_RESULT Struktur Funktionen der Legacy-Windows-Umgebung
- PMPSCAN_RESULT Struktur Zeiger Legacy-Windows-Umgebungs Features
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
ms.openlocfilehash: e7be60df7993732bafcd7c44ac2fb581c111aed6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213746"
---
# <a name="mpscan_result-structure"></a>Mpscan- \_ Ergebnis Struktur

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

Typ: **[ **mpscan- \_ Typ**](mpscan-type.md)**

</dd> <dd>

Scantyp. Siehe [**mpscan- \_ Typ**](mpscan-type.md).

</dd> <dt>

**Quelle**
</dt> <dd>

Typ: **[ **mpsource**](mpsource.md)**

</dd> <dd>

Scan Quelle, z. b. Benutzer oder System initiiert. Siehe [**mpsource**](mpsource.md).

</dd> <dt>

**Scanguid**
</dt> <dd>

Typ: **GUID**

</dd> <dd>

Scan Bezeichner.

</dd> <dt>

**StartTime**
</dt> <dd>

Typ: **ularge \_ Integer**

</dd> <dd>

Startzeitpunkt der Überprüfung.

</dd> <dt>

**EndTime**
</dt> <dd>

Typ: **ularge \_ Integer**

</dd> <dd>

Endzeit des Scan Vorgangs.

</dd> <dt>

**Bedrohlich stats**
</dt> <dd>

Typ: **[ **mpthreat- \_ Statistik**](mpthreat-stats.md)**

</dd> <dd>

Bedrohungs bezogene Statistiken. Siehe [**mpthreat \_ Stats**](mpthreat-stats.md).

</dd> <dt>

**Resourcestats**
</dt> <dd>

Typ: **[ **mpresource- \_ Statistik**](mpresource-stats.md)**

</dd> <dd>

Ressourcenbezogene Statistiken. Siehe [**mpresource- \_ Statistik**](mpresource-stats.md).

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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**mpresource- \_ Statistik**](mpresource-stats.md)
</dt> <dt>

[**mpscan- \_ Typ**](mpscan-type.md)
</dt> <dt>

[**Mpsource**](mpsource.md)
</dt> <dt>

[**mpthreat- \_ Statistik**](mpthreat-stats.md)
</dt> </dl>

 

 





