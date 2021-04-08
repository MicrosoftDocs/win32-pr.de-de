---
title: MPNIS_PRIVATE_DATA Struktur (mpclient. h)
description: Private NIS-Benachrichtigungen.
ms.assetid: 19B4928F-BC78-4DEA-A563-1516B6454465
keywords:
- MPNIS_PRIVATE_DATA Struktur Funktionen der Legacy-Windows-Umgebung
- PMPNIS_PRIVATE_DATA Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPNIS_PRIVATE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21340665a32b619c42d7909e8cd1b72ca6d09fb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740137"
---
# <a name="mpnis_private_data-structure"></a>Private mpnis- \_ \_ Datenstruktur

Private NIS-Benachrichtigungen.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPNIS_PRIVATE_DATA {
  DWORD dwNotificationType;
  DWORD cbDataSize;
  BYTE  *pbData;
} MPNIS_PRIVATE_DATA, *PMPNIS_PRIVATE_DATA;
```



## <a name="members"></a>Member

<dl> <dt>

**dwnotificationtype**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Hier wird der Benachrichtigungstyp angegeben.

</dd> <dt>

**cbDataSize**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Größe der reservierten Daten in Bytes.

</dd> <dt>

**pbData**
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



 

 





