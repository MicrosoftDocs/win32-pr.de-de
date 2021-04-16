---
description: Definiert Konstanten, die die unterstützten Schattierungs Modi beschreiben.
ms.assetid: ba4e0c62-b496-427b-a324-2fb560d153ba
title: D3DSHADEMODE-Enumeration (D3d9types. h)
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
ms.openlocfilehash: 9950e0074bef7a7b0c211177b3902cd69e2e112c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354537"
---
# <a name="d3dshademode-enumeration"></a>D3DSHADEMODE-Enumeration

Definiert Konstanten, die die unterstützten Schattierungs Modi beschreiben.

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

<span id="D3DSHADE_FLAT"></span><span id="d3dshade_flat"></span>**D3DSHADE \_ Flat**
</dt> <dd>

Flacher Schattierungs Modus. Die Farbe und die Glanz Komponente des ersten Scheitel Punkts im Dreieck werden verwendet, um die Farbe und die Glanz Komponente der Vorderseite zu bestimmen. Diese Farben bleiben über das Dreieck konstant. Das heißt, Sie werden nicht interpoliert. Das Glanz Alpha ist interpoliert. Siehe Hinweise.

</dd> <dt>

<span id="D3DSHADE_GOURAUD"></span><span id="d3dshade_gouraud"></span>**D3DSHADE- \_ Gouraud**
</dt> <dd>

Der Gouraud-Schattierungs Modus. Die Farbe und die Glanz Komponenten der Vorderseite werden durch eine lineare interpolung zwischen allen drei Scheitel Punkten des Dreiecks bestimmt.

</dd> <dt>

<span id="D3DSHADE_PHONG"></span><span id="d3dshade_phong"></span>**D3DSHADE \_ Phong**
</dt> <dd>

Wird nicht unterstützt.

</dd> <dt>

<span id="D3DSHADE_FORCE_DWORD"></span><span id="d3dshade_force_dword"></span>**D3DSHADE \_ Erzwingen von \_ DWORD**
</dt> <dd>

Erzwingt die Kompilierung dieser Enumeration in 32 Bits. Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der erste Scheitelpunkt eines Dreiecks für den flachen Schattierungs Modus wird wie folgt definiert.

-   Für eine Dreiecks Liste ist der erste Scheitelpunkt des Dreiecks i \* 3.
-   Bei einem Dreiecks Streifen ist der erste Scheitelpunkt des Dreiecks "Scheitelpunkt i".
-   Bei einem Dreiecks Lüfter ist der erste Scheitelpunkt des Dreiecks "Scheitelpunkt i + 1".

Die Member dieses Enumerationstyps definieren die Werte für den D3DRS \_ SHADEMODE-Rendering-Zustand.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
