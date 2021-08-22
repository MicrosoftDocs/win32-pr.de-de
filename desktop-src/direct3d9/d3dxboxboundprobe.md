---
description: Bestimmt, ob ein Strahl das Volumen des Begrenzungsfelds eines Felds schneidet.
ms.assetid: 45ff8540-ed5c-4f54-b3b7-3385087a6863
title: D3DXBoxBoundProbe-Funktion (D3DX9Mesh.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 197582c2f404124edd5a49c9d7780ce35cac61b15438a81d120839f283b82373
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676390"
---
# <a name="d3dxboxboundprobe-function"></a>D3DXBoxBoundProbe-Funktion

Bestimmt, ob ein Strahl das Volumen des Begrenzungsfelds eines Felds schneidet.

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

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die die untere linke Ecke des Begrenzungsfelds beschreibt. Siehe Hinweise.

</dd> <dt>

*pMax* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die die obere rechte Ecke des Begrenzungsfelds beschreibt. Siehe Hinweise.

</dd> <dt>

*pRayPosition* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur**](d3dxvector3.md) unter Angabe der Ursprungskoordinate des Strahls.

</dd> <dt>

*pRayDirection* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur**](d3dxvector3.md) unter Angabe der Richtung des Strahls. Dieser Vektor sollte nicht (0,0,0) sein, muss aber nicht normalisiert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

Gibt **TRUE zurück,** wenn der Strahl das Volumen des Begrenzungsfelds des Felds überschneidet. Andernfalls wird **FALSE zurückgegeben.**

## <a name="remarks"></a>Hinweise

**D3DXboxBoundProbe** bestimmt, ob der Strahl das Volumen des Begrenzungsfelds des Felds überschneidet, nicht nur die Oberfläche des Felds.

Die an **D3DXboxBoundProbe** übergebenen Werte sind xmin, xmax, ymin, ymax, zmin und zmax. Daher definiert Folgendes die Ecken des begrenzungsgebundenen Felds.


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



Die Tiefe des Begrenzungsfelds in z-Richtung ist zmax - zmin, in der y-Richtung ist ymax - ymin und in x-Richtung xmax - xmin. Bei den folgenden minimalen und maximalen Vektoren, min (-1, -1, -1) und max (1, 1, 1), wird das Begrenzungsfeld beispielsweise wie folgt definiert.


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
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXComputeBoundingBox**](d3dxcomputeboundingbox.md)
</dt> </dl>

 

 
