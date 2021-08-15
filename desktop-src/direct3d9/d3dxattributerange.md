---
description: 'D3DXATTRIBUTERANGE-Struktur: Speichert einen Attributtabelleneintrag.'
ms.assetid: b9f13b12-35ba-4e4c-93ac-3dd44d611b47
title: D3DXATTRIBUTERANGE-Struktur (D3dx9mesh.h)
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
ms.openlocfilehash: 73fe2214b2c1b8acb1bc657bd41803c425b4c86f34d022d6367c3011eebd6d50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118526808"
---
# <a name="d3dxattributerange-structure"></a>D3DXATTRIBUTERANGE-Struktur

Speichert einen Attributtabelleneintrag.

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

**AttribId**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Attributtabellenbezeichner.

</dd> <dt>

**FaceStart**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Startgesicht.

</dd> <dt>

**FaceCount**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Gesichtserkennungen.

</dd> <dt>

**VertexStart**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Scheitelpunkt wird gestartet.

</dd> <dt>

**VertexCount**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Scheitelpunktanzahl.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Eine Attributtabelle wird verwendet, um Bereiche des Gitters zu identifizieren, die mit unterschiedlichen Texturen, Renderzuständen, Materialien und so weiter gezeichnet werden müssen. Darüber hinaus kann die Anwendung die Attributtabelle verwenden, um Teile eines Gitters auszublenden, indem beim Zeichnen des Rahmens kein angegebener Attributbezeichner (AttribId) gezeichnunget wird.

Der LPD3DXATTRIBUTERANGE-Typ wird als Zeiger auf die **D3DXATTRIBUTERANGE-Struktur** definiert.


```
typedef D3DXATTRIBUTERANGE* LPD3DXATTRIBUTERANGE;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
