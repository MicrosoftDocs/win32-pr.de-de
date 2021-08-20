---
description: Ordnet einen Gruppennamen und dessen Handle zu.
ms.assetid: 76f3fe37-cf85-42ab-8f9e-3ab2c6053dcd
title: GROUPINFO-Struktur (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GROUPINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 333584e0ecc7a7ec9f5606891ee729eb7d925a01ea190960ff4444c1f7b8ae82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117981655"
---
# <a name="groupinfo-structure"></a>GROUPINFO-Struktur

Die **GROUPINFO-Struktur** ordnet einen Gruppennamen und dessen Handle zu.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  char   szGroupName[EXPERTGROUPNAMELENGTH+1];
  HGROUP hGroup;
} GROUPINFO, *PGROUPINFO;
```



## <a name="members"></a>Member

<dl> <dt>

**szGroupName**
</dt> <dd>

Erhöhter Wert eines Arrays in der **GROUPNAME-Struktur.**

</dd> <dt>

**hGroup**
</dt> <dd>

Handle für eine Gruppe.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




