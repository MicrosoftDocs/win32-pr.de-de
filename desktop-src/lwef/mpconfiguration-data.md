---
title: MPCONFIGURATION_DATA -Struktur (MpClient.h)
description: Enthält Daten zu Konfigurationsänderungen, einschließlich der alten und neuen Werte.
ms.assetid: AB70B1C0-C148-44BC-8C0E-CC5D2A66BCA5
keywords:
- MPCONFIGURATION_DATA struktur Legacy Windows Umgebungsfeatures
- PMPCONFIGURATION_DATA strukturzeiger Legacy-Windows-Umgebungsfeatures
topic_type:
- apiref
api_name:
- MPCONFIGURATION_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 192cb4d2e35d1b471ef92fb976535bb1e6ed733e2f29ebf86d357f722904514c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114580"
---
# <a name="mpconfiguration_data-structure"></a>\_MPCONFIGURATION-DATENstruktur

Enthält Daten zu Konfigurationsänderungen, einschließlich der alten und neuen Werte.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPCONFIGURATION_DATA {
  MP_MIDL_STRING LPWSTR ConfigurationName;
  DWORD                 DataType;
  DWORD                 PreviousDataSize;
  BYTE                  *pPreviousData;
  DWORD                 CurrentDataSize;
  BYTE                  *pCurrentData;
} MPCONFIGURATION_DATA, *PMPCONFIGURATION_DATA;
```



## <a name="members"></a>Member

<dl> <dt>

**ConfigurationName**
</dt> <dd>

Typ: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Name der geänderten Konfiguration.

</dd> <dt>

**DataType**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Der Typ der verwendeten Daten.

</dd> <dt>

**PreviousDataSize**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Größe der vorherigen Daten in Bytes.

</dd> <dt>

**pPreviousData**
</dt> <dd>

Typ: **BYTE \***

</dd> <dd>

Zeiger auf vorherige Daten.

</dd> <dt>

**CurrentDataSize**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Größe der neuen Daten in Bytes.

</dd> <dt>

**pCurrentData**
</dt> <dd>

Typ: **BYTE \***

</dd> <dd>

Zeiger auf neue Daten.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





