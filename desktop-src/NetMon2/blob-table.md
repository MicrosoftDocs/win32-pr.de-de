---
description: Enthält ein Array von BLOB.
ms.assetid: e87f493b-f160-4316-b369-75d20c735213
title: BLOB_TABLE Struktur (Netmon. h)
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
ms.openlocfilehash: 32bacc925381f1c7ed30aa66247671b67e31b7e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215893"
---
# <a name="blob_table-structure"></a>BLOB- \_ Tabellenstruktur

Die **BLOB- \_ Tabellen** Struktur enthält ein Array von BLOBs.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD dwNumBlobs;
  HBLOB hBlobs[];
} BLOB_TABLE, *PBLOB_TABLE;
```



## <a name="members"></a>Member

<dl> <dt>

**dwnumblosb**
</dt> <dd>

Indikator, dem viele blobdie folgen.

</dd> <dt>

**hblob**
</dt> <dd>

Handle für das BLOB-Array.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




