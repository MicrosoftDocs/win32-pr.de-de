---
description: Definiert die Fensterdimensionen einer Renderzieloberfläche, auf die ein 3D-Volume zeigt.
ms.assetid: fb2c6048-f837-497d-8e4f-e18942d37899
title: D3DVIEWPORT9-Struktur (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVIEWPORT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 40162e4350e5a68670023701f1cdae973fb8a7bac3a6d4f5c301136c4e8c2702
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527266"
---
# <a name="d3dviewport9-structure"></a>D3DVIEWPORT9-Struktur

Definiert die Fensterdimensionen einer Renderzieloberfläche, auf die ein 3D-Volume zeigt.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DVIEWPORT9 {
  DWORD X;
  DWORD Y;
  DWORD Width;
  DWORD Height;
  float MinZ;
  float MaxZ;
} D3DVIEWPORT9, *LPD3DVIEWPORT9;
```



## <a name="members"></a>Member

<dl> <dt>

**X**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Pixelkoordinate der oberen linken Ecke des Viewports auf der Renderzieloberfläche. Dieser Member kann auf 0 festgelegt werden, es sei denn, Sie möchten eine Teilmenge der Oberfläche rendern.

</dd> <dt>

**J**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Pixelkoordinate der oberen linken Ecke des Viewports auf der Renderzieloberfläche. Dieser Member kann auf 0 festgelegt werden, es sei denn, Sie möchten eine Teilmenge der Oberfläche rendern.

</dd> <dt>

**Width**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Breitendimension des Clipvolumens in Pixel. Sofern Sie nicht nur eine Teilmenge der Oberfläche rendern, sollte dieser Member auf die Breitendimension der Renderzieloberfläche festgelegt werden.

</dd> <dt>

**Height**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Höhendimension des Clipvolumens in Pixel. Sofern Sie nicht nur eine Teilmenge der Oberfläche rendern, sollte dieses Member auf die Höhendimension der Renderzieloberfläche festgelegt werden.

</dd> <dt>

**MinZ**
</dt> <dd>

Typ: **float**

</dd> <dd>

Zusammen mit MaxZ ein Wert, der den Bereich der Tiefenwerte, in dem eine Szene gerendert werden soll, sowie die Minimal- und Höchstwerte des Clipvolumens beschreibt. Die meisten Anwendungen legen diesen Wert auf 0,0 fest. Das Clipping erfolgt nach dem Anwenden der Projektionsmatrix.

</dd> <dt>

**MaxZ**
</dt> <dd>

Typ: **float**

</dd> <dd>

Zusammen mit MinZ ein Wert, der den Bereich der Tiefenwerte beschreibt, in dem eine Szene gerendert werden soll, sowie die Minimal- und Höchstwerte des Clipvolumens. Die meisten Anwendungen legen diesen Wert auf 1,0 fest. Das Clipping erfolgt nach dem Anwenden der Projektionsmatrix.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Elemente X, Y, Width und Height beschreiben die Position und die Abmessungen des Viewports auf der Renderzieloberfläche. Anwendungen werden in der Regel auf der gesamten Zieloberfläche gerendert. Beim Rendern auf einer 640 x 480-Oberfläche sollten diese Member 0, 0, 640 bzw. 480 sein. MinZ und MaxZ sind in der Regel auf 0,0 und 1,0 festgelegt, können aber auf andere Werte festgelegt werden, um bestimmte Effekte zu erzielen. Beispielsweise können Sie beide auf 0,0 festlegen, um das System zu zwingen, Objekte im Vordergrund einer Szene zu rendern, oder beide auf 1,0, um die Objekte in den Hintergrund zu zwingen.

Wenn sich die Viewportparameter für ein Gerät ändern (aufgrund eines Aufrufs der [**SetViewport-Methode),**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) erstellt der Treiber eine neue Transformationsmatrix.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getviewport)
</dt> <dt>

[**SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport)
</dt> </dl>

 

 
