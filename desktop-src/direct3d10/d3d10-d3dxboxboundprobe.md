---
description: Die D3DXBoxBoundProbe-Funktion (D3DX10math.h) bestimmt, ob ein Strahl das Volumen des umgebenden Felds eines Felds überschneidet.
ms.assetid: d3cdcf89-461b-44b0-b5d0-ca2e3869a5ad
title: D3DXBoxBoundProbe-Funktion (D3DX10math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXBoxBoundProbe
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ae06fa2e42e99dc64a0684844e341f26e30d797e75d3a822aa0b1ddee690703d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028810"
---
# <a name="d3dxboxboundprobe-function-d3dx10mathh"></a>D3DXBoxBoundProbe-Funktion (D3DX10math.h)

Bestimmt, ob ein Strahl das Volumen des umgebenden Felds eines Felds überschneidet.

## <a name="syntax"></a>Syntax


```C++
BOOL D3DXBoxBoundProbe(
  _In_ const D3DXVECTOR3 *pMin,
  _In_ const D3DXVECTOR3 *pMax,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMin* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf einen [**D3DXVECTOR3,**](d3d10-d3dxvector3.md)der die untere linke Ecke des umgebenden Felds beschreibt. Siehe Hinweise.

</dd> <dt>

*pMax* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3d10-d3dxvector3.md) die die obere rechte Ecke des umgebenden Felds beschreibt. Siehe Hinweise.

</dd> <dt>

*pRayPosition* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf eine D3DXVECTOR3-Struktur, die die Ursprungskoordinate des Strahls angibt.

</dd> <dt>

*pRayDirection* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf eine D3DXVECTOR3-Struktur, die die Richtung des Strahls angibt. Dieser Vektor sollte nicht (0,0,0) sein, muss aber nicht normalisiert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

Gibt **TRUE** zurück, wenn der Strahl das Volumen des umgebenden Felds des Felds überschneidet. Andernfalls gibt **FALSE** zurück.

## <a name="remarks"></a>Hinweise

**D3DXBoxBoundProbe** bestimmt, ob der Strahl das Volumen des umgebenden Felds des Felds überschneidet, nicht nur die Oberfläche des Felds.

Die an **D3DXBoxBoundProbe** übergebenen Werte sind xmin, xmax, ymin, ymax, zmin und zmax. Daher werden im Folgenden die Ecken des umgebenden Felds definiert.


```
xmax, ymax, zmax
xmax, ymax, zmin
xmax, ymin, zmax
xmax, ymin, zmin
xmin, ymax, zmax
xmin, ymax, zmin
xmin, ymin, zmax
xmin, ymin, zmin
```



Die Tiefe des umgebenden Felds in z-Richtung ist zmax - zmin, in der y-Richtung ist ymax - ymin, und in x-Richtung ist xmax - xmin. Mit den folgenden minimalen und maximalen Vektoren, min (-1, -1, -1) und max (1, 1, 1), wird der Begrenzungsfeld wie folgt definiert.


```
 1,  1,  1
 1,  1, -1
 1, -1,  1
 1, -1, -1
-1,  1,  1
-1,  1, -1
-1, -1,  1
-1, -1, -l
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header  | D3DX10math.h |
| Bibliothek | D3DX10.lib  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Meshfunktionen](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
