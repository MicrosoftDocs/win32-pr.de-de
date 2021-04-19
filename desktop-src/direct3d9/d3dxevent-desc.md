---
description: Beschreibt ein Animations Ereignis.
ms.assetid: ddcdd143-bcbd-450c-a4df-914797a562e6
title: D3DXEVENT_DESC-Struktur (D3dx9anim. h)
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
ms.openlocfilehash: 32e02e75d3d73569b60c466f45dace2c074a6b3e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363972"
---
# <a name="d3dxevent_desc-structure"></a>D3DXEVENT- \_ Struktur

Beschreibt ein Animations Ereignis.

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

**Type**
</dt> <dd>

Type: **[ **D3DXEVENT- \_ Typ**](./d3dxevent-type.md)**

</dd> <dd>

Der Ereignistyp, wie in [**D3DXEVENT \_ Type**](./d3dxevent-type.md)definiert.

</dd> <dt>

**Nachverfolgen**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Bezeichner des Ereignis Titels.

</dd> <dt>

**StartTime**
</dt> <dd>

Typ: **[ **Double**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Startzeit des Ereignisses in der globalen Zeit.

</dd> <dt>

**Dauer**
</dt> <dd>

Typ: **[ **Double**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Dauer des Ereignisses in der globalen Zeit.

</dd> <dt>

**Umstellung**
</dt> <dd>

Type: **[ **D3DXTRANSITION- \_ Typ**](./d3dxtransition-type.md)**

</dd> <dd>

Die Übergangs Art des Ereignisses, wie in [**D3DXTRANSITION \_ Type**](./d3dxtransition-type.md)definiert.

</dd> <dt>

**Weight**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Gewichtung für das Ereignis.

</dd> <dt>

**Geschwindigkeit**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Nachverfolgen der Geschwindigkeit für das Ereignis.

</dd> <dt>

**Position**
</dt> <dd>

Typ: **[ **Double**](../winprog/windows-data-types.md)**

</dd> <dd>

Position für das Ereignis nachverfolgen.

</dd> <dt>

**Aktivieren**
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Flag aktivieren.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
