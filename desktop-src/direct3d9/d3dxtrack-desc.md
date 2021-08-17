---
description: Beschreibt eine Animationsspur und gibt die Mischung aus Gewichtung, Geschwindigkeit und Position für die Spur zu einem bestimmten Zeitpunkt an.
ms.assetid: f1469b6f-861f-4b7d-a187-933092a5d257
title: D3DXTRACK_DESC -Struktur (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTRACK_DESC
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: cddabb3ea79951e35831c2cdc32e11baeb5c7c1c4ce174fd29d9382edb391953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731117"
---
# <a name="d3dxtrack_desc-structure"></a>D3DXTRACK \_ DESC-Struktur

Beschreibt eine Animationsspur und gibt die Mischung aus Gewichtung, Geschwindigkeit und Position für die Spur zu einem bestimmten Zeitpunkt an.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXTRACK_DESC {
  D3DXPRIORITY_TYPE Priority;
  FLOAT             Weight;
  FLOAT             Speed;
  DOUBLE            Position;
  BOOL              Enable;
} D3DXTRACK_DESC, *LPD3DXTRACK_DESC;
```



## <a name="members"></a>Member

<dl> <dt>

**Priority**
</dt> <dd>

Typ: **[ **D3DXPRIORITY \_ TYPE**](./d3dxpriority-type.md)**

</dd> <dd>

Prioritätstyp, wie in [**D3DXPRIORITY \_ TYPE definiert.**](./d3dxpriority-type.md)

</dd> <dt>

**Weight**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Gewichtungswert. Die Gewichtung bestimmt den Anteil dieser Spur, der mit anderen Spuren kombiniert werden soll.

</dd> <dt>

**Geschwindigkeit**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Geschwindigkeitswert. Dies wird ähnlich wie ein Multiplikator verwendet, um den Zeitraum der Spur zu skalieren.

</dd> <dt>

**Position**
</dt> <dd>

Typ: **[ **DOUBLE**](../winprog/windows-data-types.md)**

</dd> <dd>

Zeitposition der Spur im lokalen Zeitrahmen des aktuellen Animationssets.

</dd> <dt>

**Aktivieren**
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

Nachverfolgen des Aktivierens/Deaktivierens. Legen Sie zum Aktivieren auf **TRUE fest.** Legen Sie zum Deaktivieren auf **FALSE fest.**

</dd> </dl>

## <a name="remarks"></a>Hinweise

Spuren mit der gleichen Priorität werden kombiniert, und die beiden resultierenden Werte werden dann mithilfe des Prioritätsmischungsfaktors kombiniert. Einer Spur muss ein Animationssatz (separat gespeichert) zugeordnet sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9anim.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
