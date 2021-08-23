---
description: Identifiziert Speicherdaten.
ms.assetid: 0ec0597f-d83a-4c1e-b993-30f0bbd64e6b
title: D3DXF_FILELOADMEMORY -Struktur (D3dx9xof.h)
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
ms.openlocfilehash: b3709e6eeb99026b76d066edfccbae578b5c851d6e73936ffe06d10fbf69dcb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045058"
---
# <a name="d3dxf_fileloadmemory-structure"></a>D3DXF \_ FILELOADMEMORY-Struktur

Identifiziert Speicherdaten.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXF_FILELOADMEMORY {
  LPCVOID lpMemory;
  SIZE_T  dSize;
} D3DXF_FILELOADMEMORY, *LPD3DXF_FILELOADMEMORY;
```



## <a name="members"></a>Member

<dl> <dt>

**lpMemory**
</dt> <dd>

Typ: **[ **LPCVOID**](../winprog/windows-data-types.md)**

</dd> <dd>

Zeiger auf einen Speicherblock, der geladen werden soll.

</dd> <dt>

**dSize**
</dt> <dd>

Typ: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**

</dd> <dd>

Größe des zu ladenden Speicherblocks in Bytes.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur identifiziert Daten, die aus dem Arbeitsspeicher geladen werden sollen, wenn eine Anwendung die [**CreateEnumObject-Methode**](id3dxfile--createenumobject.md) verwendet, und gibt das Flag D3DXF \_ FILELOAD \_ FROMMEMORY an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9xof.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX X-Dateistrukturen](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> </dl>

 

 
