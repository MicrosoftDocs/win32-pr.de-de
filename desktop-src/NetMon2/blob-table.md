---
description: Enthält ein Array von BLOBs.
ms.assetid: e87f493b-f160-4316-b369-75d20c735213
title: BLOB_TABLE-Struktur (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BLOB_TABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: e0615ad9c11657a47d9eaa87035207cb499634cd4ded6ae484d6f5d256c23e15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144343"
---
# <a name="blob_table-structure"></a>BLOB \_ TABLE-Struktur

Die **BLOB \_ TABLE-Struktur** enthält ein Array von BLOBs.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD dwNumBlobs;
  HBLOB hBlobs[];
} BLOB_TABLE, *PBLOB_TABLE;
```



## <a name="members"></a>Member

<dl> <dt>

**dwNumBlobs**
</dt> <dd>

Indikator, dem viele BLOBs folgen.

</dd> <dt>

**hBlobs**
</dt> <dd>

Handle für das BLOB-Array.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




