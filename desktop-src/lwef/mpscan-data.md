---
title: MPSCAN_DATA Struktur (mpclient. h)
description: Überprüfen Sie die an den Rückruf übergebenen Daten.
ms.assetid: 6C9AAF1E-7566-43EE-A100-5112E9B8878C
keywords:
- MPSCAN_DATA Struktur Funktionen der Legacy-Windows-Umgebung
- PMPSCAN_DATA Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPSCAN_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e78508313f102e2baad19cf359a5c3a7c172db0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479167"
---
# <a name="mpscan_data-structure"></a>Mpscan- \_ Datenstruktur

Überprüfen Sie die an den Rückruf übergebenen Daten.

Diese Struktur enthält kumulative Bedrohungs-und Ressourcen Statistiken. Diese Stat-Felder sind immer gültig.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPSCAN_DATA {
  MPSCAN_TYPE      ScanType;
  PMPRESOURCE_INFO ResourceInfo;
  MPRESOURCE_STATS ResourceStats;
  MPTHREAT_STATS   ThreatStats;
} MPSCAN_DATA, *PMPSCAN_DATA;
```



## <a name="members"></a>Member

<dl> <dt>

**ScanType**
</dt> <dd>

Typ: **[ **mpscan- \_ Typ**](mpscan-type.md)**

</dd> <dd>

Scantyp.

</dd> <dt>

**ResourceInfo**
</dt> <dd>

Typ: **pmpresource- \_ Informationen**

</dd> <dd>

Ressourceninformationen Informationen finden Sie unter [**mpresource- \_ Informationen**](mpresource-info.md).

</dd> <dt>

**Resourcestats**
</dt> <dd>

Typ: **[ **mpresource- \_ Statistik**](mpresource-stats.md)**

</dd> <dd>

Ressourcenbezogene kumulative Statistiken.

</dd> <dt>

**Bedrohlich stats**
</dt> <dd>

Typ: **[ **mpthreat- \_ Statistik**](mpthreat-stats.md)**

</dd> <dd>

Bedrohungs Statistik mit erfolgreichen Überprüfungs Vervollständigungen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**mpresource- \_ Informationen**](mpresource-info.md)
</dt> <dt>

[**mpresource- \_ Statistik**](mpresource-stats.md)
</dt> <dt>

[**mpscan- \_ Typ**](mpscan-type.md)
</dt> <dt>

[**mpthreat- \_ Statistik**](mpthreat-stats.md)
</dt> </dl>

 

 





