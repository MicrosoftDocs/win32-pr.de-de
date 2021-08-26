---
title: MPSTATUS_DATAEX_UNUSED-Struktur (MpClient.h)
description: Dummystruktur für Nicht-SRP.
ms.assetid: 396744CE-2435-4591-B0CF-A4392C88640F
keywords:
- MPSTATUS_DATAEX_UNUSED struktur legacy Windows Environment Features (Legacy-Windows-Umgebungsfeatures)
- PMPSTATUS_DATAEX_UNUSED Strukturzeiger Legacy Windows-Umgebungsfeatures
topic_type:
- apiref
api_name:
- MPSTATUS_DATAEX_UNUSED
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 245315d12b5fbe76ec2f552e510336aa3974753678e04f87c33546737f180c56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961090"
---
# <a name="mpstatus_dataex_unused-structure"></a>MPSTATUS \_ DATAEX \_ UNUSED-Struktur

Dummystruktur für Nicht-SRP.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPSTATUS_DATAEX_UNUSED {
  DWORD dwNone;
} MPSTATUS_DATAEX_UNUSED, *PMPSTATUS_DATAEX_UNUSED;
```



## <a name="members"></a>Member

<dl> <dt>

**dwNone**
</dt> <dd>

Typ: **DWORD**

</dd> <dd></dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





