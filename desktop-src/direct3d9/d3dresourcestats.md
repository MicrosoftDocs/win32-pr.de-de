---
description: Vom ResourceManager D3DDEVINFO erfasste Ressourcenstatistiken \_ bei Verwendung des asynchronen Abfragemechanismus.
ms.assetid: f4d9c6db-4002-439c-9a88-485763badc82
title: D3DRESOURCESTATS-Struktur (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRESOURCESTATS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: dc992c5b8246ce302cda8924b8521c923575c8914c83b35c8c1e789e4bc1c826
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527472"
---
# <a name="d3dresourcestats-structure"></a>D3DRESOURCESTATS-Struktur

Vom [**\_ ResourceManager D3DDEVINFO**](d3ddevinfo-resourcemanager.md) erfasste Ressourcenstatistiken bei Verwendung des asynchronen Abfragemechanismus.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DRESOURCESTATS {
  BOOL  bThrashing;
  DWORD ApproxBytesDownloaded;
  DWORD NumEvicts;
  DWORD NumVidCreates;
  DWORD LastPri;
  DWORD NumUsed;
  DWORD NumUsedInVidMem;
  DWORD WorkingSet;
  DWORD WorkingSetBytes;
  DWORD TotalManaged;
  DWORD TotalBytes;
} D3DRESOURCESTATS, *LPD3DRESOURCESTATS;
```



## <a name="members"></a>Member

<dl> <dt>

**bThrashing**
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

Gibt an, ob ein Thrashing erfolgt.

</dd> <dt>

**ApproxBytesDownloaded**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Ungefähre Anzahl von Bytes, die vom Ressourcen-Manager heruntergeladen wurden.

</dd> <dt>

**NumEvicts**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der entfernten Objekte.

</dd> <dt>

**NumVidCreates**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der im Videospeicher erstellten Objekte.

</dd> <dt>

**LastPri**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Priorität des letzten entfernten Objekts.

</dd> <dt>

**NumUsed**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der auf das Gerät festgelegten Objekte.

</dd> <dt>

**NumUsedInVidMem**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der auf das Gerät festgelegten Objekte, die sich bereits im Videospeicher befinden.

</dd> <dt>

**Workingset**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Objekte im Videospeicher.

</dd> <dt>

**WorkingSetBytes**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Bytes im Videospeicher.

</dd> <dt>

**TotalManaged**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Gesamtzahl der verwalteten Objekte.

</dd> <dt>

**TotalBytes**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Gesamtanzahl der Bytes verwalteter Objekte.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[Asynchrone Benachrichtigung (Direct3D 9)](asynchronous-notification.md)
</dt> </dl>

 

 
