---
description: Beschreibt ein Animationsereignis.
ms.assetid: ddcdd143-bcbd-450c-a4df-914797a562e6
title: D3DXEVENT_DESC -Struktur (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEVENT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: d5569eccd5b99939cd50797ee73593ce5a2bfc8ddd60236e05218ddcca7f4383
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731808"
---
# <a name="d3dxevent_desc-structure"></a>D3DXEVENT \_ DESC-Struktur

Beschreibt ein Animationsereignis.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXEVENT_DESC {
  D3DXEVENT_TYPE      Type;
  UINT                Track;
  DOUBLE              StartTime;
  DOUBLE              Duration;
  D3DXTRANSITION_TYPE Transition;
  union {
    FLOAT  Weight;
    FLOAT  Speed;
    DOUBLE Position;
    BOOL   Enable;
  };
} D3DXEVENT_DESC, *LPD3DXEVENT_DESC;
```



## <a name="members"></a>Member

<dl> <dt>

**Typ**
</dt> <dd>

Typ: **[ **D3DXEVENT \_ TYPE**](./d3dxevent-type.md)**

</dd> <dd>

Ereignistyp, wie in [**D3DXEVENT \_ TYPE definiert.**](./d3dxevent-type.md)

</dd> <dt>

**Track**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Ereignisverfolgungsbezeichner.

</dd> <dt>

**StartTime**
</dt> <dd>

Typ: **[ **DOUBLE**](../winprog/windows-data-types.md)**

</dd> <dd>

Startzeit des Ereignisses in globaler Zeit.

</dd> <dt>

**Dauer**
</dt> <dd>

Typ: **[ **DOUBLE**](../winprog/windows-data-types.md)**

</dd> <dd>

Dauer des Ereignisses in globaler Zeit.

</dd> <dt>

**Umstellung**
</dt> <dd>

Typ: **[ **D3DXTRANSITION \_ TYPE**](./d3dxtransition-type.md)**

</dd> <dd>

Übergangsstil des Ereignisses, wie in [**D3DXTRANSITION \_ TYPE definiert.**](./d3dxtransition-type.md)

</dd> <dt>

**Weight**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Nachverfolgen der Gewichtung für das Ereignis.

</dd> <dt>

**Geschwindigkeit**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Nachverfolgen der Geschwindigkeit für das Ereignis.

</dd> <dt>

**Position**
</dt> <dd>

Typ: **[ **DOUBLE**](../winprog/windows-data-types.md)**

</dd> <dd>

Nachverfolgen der Position für das Ereignis.

</dd> <dt>

**Aktivieren**
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

Flag aktivieren.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9anim.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
