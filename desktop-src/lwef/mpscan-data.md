---
title: MPSCAN_DATA -Struktur (MpClient.h)
description: Überprüfen Sie die an den Rückruf übergebenen Daten.
ms.assetid: 6C9AAF1E-7566-43EE-A100-5112E9B8878C
keywords:
- MPSCAN_DATA struktur Legacy Windows Umgebungsfeatures
- PMPSCAN_DATA Strukturzeiger Legacy-Windows-Umgebungsfeatures
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
ms.openlocfilehash: 5b7c00357b8f104fff42b94de552d52979c364dee64a82bb8e438946319c8c13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975990"
---
# <a name="mpscan_data-structure"></a>MPSCAN \_ DATA-Struktur

Überprüfen Sie die an den Rückruf übergebenen Daten.

Diese Struktur enthält kumulative Bedrohungs- und Ressourcenstatistiken. Diese Statistikfelder sind immer gültig.

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

Typ: **[ **MPSCAN \_ TYPE**](mpscan-type.md)**

</dd> <dd>

Scantyp.

</dd> <dt>

**ResourceInfo**
</dt> <dd>

Typ: **PMPRESOURCE \_ INFO**

</dd> <dd>

Ressourceninformationen Weitere Informationen [**finden Sie unter MPRESOURCE \_ INFO**](mpresource-info.md).

</dd> <dt>

**ResourceStats**
</dt> <dd>

Typ: **[ **MPRESOURCE \_ STATS**](mpresource-stats.md)**

</dd> <dd>

Ressourcenbezogene kumulative Statistiken.

</dd> <dt>

**ThreatStats**
</dt> <dd>

Typ: **[ **MPTHREAT \_ STATS**](mpthreat-stats.md)**

</dd> <dd>

Bedrohungsstatistiken mit erfolgreichen Überprüfungsabschluss.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MPRESOURCE-INFORMATIONEN \_**](mpresource-info.md)
</dt> <dt>

[**\_MPRESOURCE-STATISTIKEN**](mpresource-stats.md)
</dt> <dt>

[**\_MPSCAN-TYP**](mpscan-type.md)
</dt> <dt>

[**MPTHREAT \_ STATS**](mpthreat-stats.md)
</dt> </dl>

 

 





