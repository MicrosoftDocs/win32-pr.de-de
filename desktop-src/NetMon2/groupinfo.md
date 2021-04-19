---
description: Ordnet einen Gruppennamen und sein Handle zu.
ms.assetid: 76f3fe37-cf85-42ab-8f9e-3ab2c6053dcd
title: GroupInfo-Struktur (Netmon. h)
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
ms.openlocfilehash: 5152b0a621a34e49d6f1024a81b7e91aed94a06b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343040"
---
# <a name="groupinfo-structure"></a>GroupInfo-Struktur

Die **groupInfo** -Struktur ordnet einen Gruppennamen und sein Handle zu.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  char   szGroupName[EXPERTGROUPNAMELENGTH+1];
  HGROUP hGroup;
} GROUPINFO, *PGROUPINFO;
```



## <a name="members"></a>Member

<dl> <dt>

**szgroupname**
</dt> <dd>

Inkrementierter Wert eines Arrays in der **GroupName** -Struktur.

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
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




