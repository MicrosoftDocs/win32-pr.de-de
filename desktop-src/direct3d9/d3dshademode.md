---
description: Definiert Konstanten, die die unterstützten Schattierungsmodi beschreiben.
ms.assetid: ba4e0c62-b496-427b-a324-2fb560d153ba
title: D3DSHADEMODE-Enumeration (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSHADEMODE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 6a8c937000912eb203986bed4889785b9484afec7682418aed43fcc58c438e58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119241560"
---
# <a name="d3dshademode-enumeration"></a>D3DSHADEMODE-Enumeration

Definiert Konstanten, die die unterstützten Schattierungsmodi beschreiben.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DSHADEMODE { 
  D3DSHADE_FLAT         = 1,
  D3DSHADE_GOURAUD      = 2,
  D3DSHADE_PHONG        = 3,
  D3DSHADE_FORCE_DWORD  = 0x7fffffff
} D3DSHADEMODE, *LPD3DSHADEMODE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DSHADE_FLAT"></span><span id="d3dshade_flat"></span>**D3DSHADE \_ FLAT**
</dt> <dd>

Flacher Schattierungsmodus. Die Farbe und die Glanzkomponente des ersten Scheitelpunkts im Dreieck werden verwendet, um die Farbe und die Glanzkomponente des Gesichts zu bestimmen. Diese Farben bleiben über das Dreieck hinweg konstant. Das heißt, sie werden nicht interpoliert. Das Specular Alpha wird interpoliert. Siehe Hinweise.

</dd> <dt>

<span id="D3DSHADE_GOURAUD"></span><span id="d3dshade_gouraud"></span>**D3DSHADE \_ GOURAUD**
</dt> <dd>

Gouraud-Schattierungsmodus. Die Farbe und die Glanzkomponenten des Gesichts werden durch eine lineare Interpolation zwischen allen drei Scheitelpunkten des Dreiecks bestimmt.

</dd> <dt>

<span id="D3DSHADE_PHONG"></span><span id="d3dshade_phong"></span>**D3DSHADE \_ PHONG**
</dt> <dd>

Wird nicht unterstützt.

</dd> <dt>

<span id="D3DSHADE_FORCE_DWORD"></span><span id="d3dshade_force_dword"></span>**D3DSHADE \_ FORCE \_ DWORD**
</dt> <dd>

Erzwingt, dass diese Enumeration in eine Größe von 32 Bits kompiliert wird. Ohne diesen Wert würden einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der erste Scheitelpunkt eines Dreiecks für den Flachschattierungsmodus wird wie folgt definiert.

-   Für eine Dreiecksliste ist der erste Scheitelpunkt des Dreiecks i i \* 3.
-   Bei einem Dreiecksstreifen ist der erste Scheitelpunkt des Dreiecks i der Scheitelpunkt i.
-   Bei einem Dreiecksfächer ist der erste Scheitelpunkt des Dreiecks i der Scheitelpunkt i + 1.

Die Member dieses enumerationierten Typs definieren die Vales für den D3DRS \_ SHADEMODE-Renderzustand.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
