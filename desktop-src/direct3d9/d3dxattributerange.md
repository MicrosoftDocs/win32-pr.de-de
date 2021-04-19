---
description: Speichert einen Attribut Tabelleneintrag.
ms.assetid: b9f13b12-35ba-4e4c-93ac-3dd44d611b47
title: D3DXATTRIBUTERANGE-Struktur (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXATTRIBUTERANGE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: a842bbf41847f4b4e65c975e11f3e160cea1422d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350694"
---
# <a name="d3dxattributerange-structure"></a>D3DXATTRIBUTERANGE-Struktur

Speichert einen Attribut Tabelleneintrag.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXATTRIBUTERANGE {
  DWORD AttribId;
  DWORD FaceStart;
  DWORD FaceCount;
  DWORD VertexStart;
  DWORD VertexCount;
} D3DXATTRIBUTERANGE, *LPD3DXATTRIBUTERANGE;
```



## <a name="members"></a>Member

<dl> <dt>

**Atungbid**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Attribut Tabellen Bezeichner.

</dd> <dt>

**Fakestart**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Startseite.

</dd> <dt>

**FaceCount**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Gesichter.

</dd> <dt>

**VertexStart**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Der Scheitelpunkt wird gestartet.

</dd> <dt>

**VertexCount**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Vertex-Anzahl.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Eine Attribut Tabelle wird verwendet, um Bereiche des Netzes zu identifizieren, die mit unterschiedlichen Texturen, renderzuständen, Materialien usw. gezeichnet werden müssen. Außerdem kann die Anwendung die Attribut Tabelle verwenden, um Teile eines Netzes auszublenden, indem beim Zeichnen des Frames kein angegebener Attribut Bezeichner (atungbid) gezeichnet wird.

Der LPD3DXATTRIBUTERANGE-Typ wird als Zeiger auf die **D3DXATTRIBUTERANGE** -Struktur definiert.


```
typedef D3DXATTRIBUTERANGE* LPD3DXATTRIBUTERANGE;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
