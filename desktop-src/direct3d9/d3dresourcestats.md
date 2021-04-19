---
description: Ressourcen Statistik, die von D3DDEVINFO \_ ResourceManager erfasst wird, wenn der asynchrone Abfrage Mechanismus verwendet wird.
ms.assetid: f4d9c6db-4002-439c-9a88-485763badc82
title: D3DRESOURCESTATS-Struktur (D3D9Types. h)
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
ms.openlocfilehash: f6f549011b9750f69187c0e0cbf34ec94764c9ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370408"
---
# <a name="d3dresourcestats-structure"></a>D3DRESOURCESTATS-Struktur

Ressourcen Statistik, die von [**D3DDEVINFO \_ ResourceManager**](d3ddevinfo-resourcemanager.md) erfasst wird, wenn der asynchrone Abfrage Mechanismus verwendet wird.

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

**bthrashing**
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Gibt an, ob eine Überlastung auftritt.

</dd> <dt>

**Approxbytesherunter geladen**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Ungefähre Anzahl von Bytes, die vom Ressourcen-Manager heruntergeladen werden.

</dd> <dt>

**Numevicts**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der entfernten Objekte.

</dd> <dt>

**Numviderstellt**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl von Objekten, die im Videospeicher erstellt wurden.

</dd> <dt>

**Lastpri**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Priorität des letzten Objekts, das entfernt wurde.

</dd> <dt>

**Numused**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl von Objekten, die auf das Gerät festgelegt sind.

</dd> <dt>

**Numusedinvidmem**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Objekte, die auf das Gerät festgelegt sind, die bereits im Videospeicher vorhanden sind.

</dd> <dt>

**Workingset**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl von Objekten im Videospeicher.

</dd> <dt>

**Workingsetbytes**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl von Bytes im Videospeicher.

</dd> <dt>

**Totalmanaged**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Gesamtanzahl verwalteter Objekte.

</dd> <dt>

**TotalBytes**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Gesamtanzahl der Bytes von verwalteten Objekten.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[Asynchrone Benachrichtigung (Direct3D 9)](asynchronous-notification.md)
</dt> </dl>

 

 
