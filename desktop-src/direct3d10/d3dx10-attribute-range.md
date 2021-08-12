---
description: 'D3DX10_ATTRIBUTE_RANGE struktur: Speichert einen Attributtabelleneintrag.'
ms.assetid: 81c77dc9-e078-46a1-a435-4b241e36ec13
title: D3DX10_ATTRIBUTE_RANGE -Struktur (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ATTRIBUTE_RANGE
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 9dafba8928d0c488c0ab4a5c50bbe632012c70d1cebcced3e1c970e029f1181a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118303485"
---
# <a name="d3dx10_attribute_range-structure"></a>D3DX10 \_ ATTRIBUTE \_ RANGE-Struktur

Speichert einen Attributtabelleneintrag.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DX10_ATTRIBUTE_RANGE {
  UINT AttribId;
  UINT FaceStart;
  UINT FaceCount;
  UINT VertexStart;
  UINT VertexCount;
} D3DX10_ATTRIBUTE_RANGE, *LPD3DX10_ATTRIBUTE_RANGE;
```



## <a name="members"></a>Member

<dl> <dt>

**AttribId**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Attributtabellenbezeichner.

</dd> <dt>

**FaceStart**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Startgesicht.

</dd> <dt>

**FaceCount**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Gesichtserkennungen.

</dd> <dt>

**VertexStart**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Scheitelpunkt wird gestartet.

</dd> <dt>

**VertexCount**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Scheitelpunktanzahl.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Eine Attributtabelle wird verwendet, um Bereiche des Gitters zu identifizieren, die mit unterschiedlichen Texturen, Renderzuständen, Materialien und so weiter gezeichnet werden müssen. Darüber hinaus kann die Anwendung die Attributtabelle verwenden, um Teile eines Gitters auszublenden, indem beim Zeichnen des Rahmens kein angegebener Attributbezeichner (AttribId) gezeichnunget wird.

Der TYP LPD3DX ATTRIBUTE RANGE wird als Zeiger auf die \_ \_ D3DX \_ ATTRIBUTE \_ RANGE-Struktur definiert.


```
typedef D3DX_ATTRIBUTE_RANGE* LPD3DX_ATTRIBUTE_RANGE;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
