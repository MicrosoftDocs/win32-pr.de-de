---
description: Identifiziert Arbeitsspeicher Daten.
ms.assetid: 0ec0597f-d83a-4c1e-b993-30f0bbd64e6b
title: D3DXF_FILELOADMEMORY-Struktur (D3dx9xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXF_FILELOADMEMORY
api_type:
- HeaderDef
api_location:
- d3dx9xof.h
ms.openlocfilehash: a7ad988d9906101db57af6f8f5042766c3e32ccc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961604"
---
# <a name="d3dxf_fileloadmemory-structure"></a>D3DXF \_ fileloadmemory-Struktur

Identifiziert Arbeitsspeicher Daten.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXF_FILELOADMEMORY {
  LPCVOID lpMemory;
  SIZE_T  dSize;
} D3DXF_FILELOADMEMORY, *LPD3DXF_FILELOADMEMORY;
```



## <a name="members"></a>Member

<dl> <dt>

**lpmemory**
</dt> <dd>

Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**

</dd> <dd>

Zeiger auf einen Speicherblock, der geladen werden soll.

</dd> <dt>

**dsize**
</dt> <dd>

Typ: **[ **Größe \_ T**](../winprog/windows-data-types.md)**

</dd> <dd>

Größe des zu ladenden Speicherblocks in Bytes.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur identifiziert Daten, die aus dem Arbeitsspeicher geladen werden sollen, wenn eine Anwendung die Methode " [**kreateenumuject**](id3dxfile--createenumobject.md) " verwendet und das Flag "D3DXF \_ fileload \_ frommemory" angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9xof. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX X-Dateistrukturen](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> </dl>

 

 
