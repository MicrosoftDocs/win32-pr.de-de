---
title: MPNIS_PRIVATE_DATA -Struktur (MpClient.h)
description: Private NIS-Benachrichtigungen.
ms.assetid: 19B4928F-BC78-4DEA-A563-1516B6454465
keywords:
- MPNIS_PRIVATE_DATA struktur Legacy Windows Umgebungsfeatures
- PMPNIS_PRIVATE_DATA strukturzeiger Legacy-Windows Umgebungsfeatures
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
ms.openlocfilehash: a50719e4ecc0beff848467023a1c5f941ff06ceb891b05674e199d47a38b8659
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119556140"
---
# <a name="mpnis_private_data-structure"></a>MPNIS \_ PRIVATE \_ DATA-Struktur

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

**dwNotificationType**
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

Typ: **BYTE \***

</dd> <dd>

Zeiger auf reservierte Daten.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





