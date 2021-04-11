---
title: MPRESERVED_DATA Struktur (mpclient. h)
description: Reservierte Benachrichtigungs Daten.
ms.assetid: C92206BD-6E56-4B7D-ABB1-DC1149AE141D
keywords:
- MPRESERVED_DATA Struktur Funktionen der Legacy-Windows-Umgebung
- PMPRESERVED_DATA Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPRESERVED_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b1e08184da71fe857cb412ef986c986a0c59baa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104547"
---
# <a name="mpreserved_data-structure"></a>Mbeibehaltene \_ Datenstruktur

Reservierte Benachrichtigungs Daten.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPRESERVED_DATA {
  DWORD cbReservedData;
  BYTE  *pbReservedData;
} MPRESERVED_DATA, *PMPRESERVED_DATA;
```



## <a name="members"></a>Member

<dl> <dt>

**cbreserveddata**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Größe der reservierten Daten in Bytes.

</dd> <dt>

**pbreserveddata**
</dt> <dd>

Type: **Byte \***

</dd> <dd>

Zeiger auf reservierte Daten.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



 

 





