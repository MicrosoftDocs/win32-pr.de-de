---
description: Beschreibt einen Animations Titel und gibt das Mischungs Gewicht, die Geschwindigkeit und die Position für den Track zu einem bestimmten Zeitpunkt an.
ms.assetid: f1469b6f-861f-4b7d-a187-933092a5d257
title: D3DXTRACK_DESC-Struktur (D3dx9anim. h)
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
ms.openlocfilehash: 12f1604cf954bcdd6a2a898fec5410804112e498
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365309"
---
# <a name="d3dxtrack_desc-structure"></a>D3DXTRACK- \_ Struktur

Beschreibt einen Animations Titel und gibt das Mischungs Gewicht, die Geschwindigkeit und die Position für den Track zu einem bestimmten Zeitpunkt an.

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

Type: **[ **D3DXPRIORITY- \_ Typ**](./d3dxpriority-type.md)**

</dd> <dd>

Der Prioritäts Typen, wie in [**D3DXPRIORITY \_ Type**](./d3dxpriority-type.md)definiert.

</dd> <dt>

**Weight**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Gewichtungswert. Die Gewichtung bestimmt den Anteil dieses Titels zum Mischen mit anderen Spuren.

</dd> <dt>

**Geschwindigkeit**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Geschwindigkeitswert. Dies wird ähnlich wie bei einem Multiplikator verwendet, um den Zeitraum des Titels zu skalieren.

</dd> <dt>

**Position**
</dt> <dd>

Typ: **[ **Double**](../winprog/windows-data-types.md)**

</dd> <dd>

Uhrzeit Position des Titels im lokalen Zeitrahmen des aktuellen Animations Satzes.

</dd> <dt>

**Aktivieren**
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Nachverfolgen von aktivieren/deaktivieren. Legen Sie zum Aktivieren von auf **true** fest. Legen Sie zum Deaktivieren von auf **false** fest.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Spuren mit der gleichen Priorität werden kombiniert, und die beiden resultierenden Werte werden dann mithilfe des Prioritäts-Blend-Faktors gemischt. Einem Track muss ein Animations Satz (separat gespeichert) zugeordnet sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
