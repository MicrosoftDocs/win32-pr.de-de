---
title: MPCONFIGURATION_DATA Struktur (mpclient. h)
description: Enthält Daten zu Konfigurationsänderungen, einschließlich der alten und neuen Werte.
ms.assetid: AB70B1C0-C148-44BC-8C0E-CC5D2A66BCA5
keywords:
- MPCONFIGURATION_DATA Struktur Funktionen der Legacy-Windows-Umgebung
- PMPCONFIGURATION_DATA Struktur Zeiger Legacy-Windows-Umgebungs Features
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
ms.openlocfilehash: 7bb54ae4e323f2144dd25c52005d8484b0a207e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040459"
---
# <a name="mpconfiguration_data-structure"></a>Mpconfiguration- \_ Datenstruktur

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

Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**

</dd> <dd>

Der Name der geänderten Konfiguration.

</dd> <dt>

**DataType**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Der Typ der verwendeten Daten.

</dd> <dt>

**Previousdatasize**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Größe der vorherigen Daten in Bytes.

</dd> <dt>

**ppreviousdata**
</dt> <dd>

Typ: **Byte \** _

</dd> <dd>

Zeiger auf vorherige Daten.

</dd> <dt>

_ *Currentdatasize**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Größe der neuen Daten in Bytes.

</dd> <dt>

**pcurrentdata**
</dt> <dd>

Type: **Byte \***

</dd> <dd>

Zeiger auf neue Daten.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



 

 





