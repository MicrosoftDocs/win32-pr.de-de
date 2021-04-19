---
description: Definiert die Fenster Dimensionen einer Renderziel-Oberfläche, auf die ein 3D-Volume projiziert wird.
ms.assetid: fb2c6048-f837-497d-8e4f-e18942d37899
title: D3DVIEWPORT9-Struktur (D3D9Types. h)
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
ms.openlocfilehash: 3d96000de50934ebdc893ffc3866dd3252703bdc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367382"
---
# <a name="d3dviewport9-structure"></a>D3DVIEWPORT9-Struktur

Definiert die Fenster Dimensionen einer Renderziel-Oberfläche, auf die ein 3D-Volume projiziert wird.

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

Die Pixel Koordinate der oberen linken Ecke des Viewports auf der renderzieloberfläche. Dieser Member kann auf 0 festgelegt werden, es sei denn, Sie möchten zu einer Teilmenge der-Oberfläche rendert werden.

</dd> <dt>

**J**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Pixel Koordinate der oberen linken Ecke des Viewports auf der renderzieloberfläche. Dieser Member kann auf 0 festgelegt werden, es sei denn, Sie möchten zu einer Teilmenge der-Oberfläche rendert werden.

</dd> <dt>

**Width**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Width-Dimension des Clip-Volumes in Pixel. Wenn Sie nur eine Teilmenge der-Oberfläche rendern, sollte dieser Member auf die Width-Dimension der renderzieloberfläche festgelegt werden.

</dd> <dt>

**Height**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Height-Dimension des Clip Volumes in Pixel. Wenn Sie nur eine Teilmenge der-Oberfläche rendern, sollte dieser Member auf die Height-Dimension der renderzieloberfläche festgelegt werden.

</dd> <dt>

**Minz**
</dt> <dd>

Typ: **float**

</dd> <dd>

Mit MaxZ können Sie den Bereich der tiefen Werte beschreiben, in die eine Szene gerendert werden soll, den minimalen und maximalen Wert des Clip-Volumes. Die meisten Anwendungen legen diesen Wert auf 0,0 fest. Das Clipping erfolgt nach dem Anwenden der Projektions Matrix.

</dd> <dt>

**MaxZ**
</dt> <dd>

Typ: **float**

</dd> <dd>

Mit Minz, dem Wert, der den Bereich der tiefen Werte beschreibt, in den eine Szene gerendert werden soll, dem minimalen und maximalen Wert des Clip-Volumes. Die meisten Anwendungen legen diesen Wert auf 1,0 fest. Das Clipping erfolgt nach dem Anwenden der Projektions Matrix.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Elemente X, Y, Width und Height beschreiben die Position und die Dimensionen des Viewports auf der renderzieloberfläche. Normalerweise renderanwendungen auf der gesamten Ziel Oberfläche. beim Rendern auf einer 640 x 480-Oberfläche sollten diese Member jeweils 0, 0, 640 und 480 sein. Minz und MaxZ sind in der Regel auf 0,0 und 1,0 festgelegt, können jedoch auf andere Werte festgelegt werden, um bestimmte Effekte zu erzielen. Sie können Sie z. b. auf 0,0 festlegen, um zu erzwingen, dass das Systemobjekte im Vordergrund einer Szene oder beides auf 1,0, um die Objekte im Hintergrund zu erzwingen.

Wenn die Viewport-Parameter für ein Gerät geändert werden (aufgrund eines Aufrufes der [**setviewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) -Methode), erstellt der Treiber eine neue Transformationsmatrix.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**Getviewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getviewport)
</dt> <dt>

[**Setviewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport)
</dt> </dl>

 

 
