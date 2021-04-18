---
description: Die D3DXBoxBoundProbe-Funktion (D3DX10math. h) bestimmt, ob ein Strahl das Volume des Begrenzungs Rahmens eines Felds schneidet.
ms.assetid: d3cdcf89-461b-44b0-b5d0-ca2e3869a5ad
title: D3DXBoxBoundProbe-Funktion (D3DX10math. h)
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
ms.openlocfilehash: e1a8d1a7b879814cff43e31b060cc2af53167818
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106358187"
---
# <a name="d3dxboxboundprobe-function-d3dx10mathh"></a>D3DXBoxBoundProbe-Funktion (D3DX10math. h)

Bestimmt, ob ein Strahl das Volume des umgebenden Felds eines Felds schneidet.

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

*Pmin* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Ein Zeiger auf einen [**D3DXVECTOR3**](d3d10-d3dxvector3.md), der die untere linke Ecke des umgebenden Felds beschreibt. Siehe Hinweise.

</dd> <dt>

*pmax* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3**](d3d10-d3dxvector3.md) -Struktur, die die obere rechte Ecke des Begrenzungs Rahmens beschreibt. Siehe Hinweise.

</dd> <dt>

" *prayposition* \[ " in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf eine D3DXVECTOR3-Struktur, die die Ursprungs Koordinate des Strahls angibt.

</dd> <dt>

" *praydirection* \[ " in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf eine D3DXVECTOR3-Struktur, die die Richtung des Strahls angibt. Dieser Vektor sollte nicht (0, 0, 0) sein, muss jedoch nicht normalisiert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **bool**](../winprog/windows-data-types.md)**

Gibt " **true** " zurück, wenn der Strahl das Volume des umgebenden Felds der Box schneidet. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

**D3DXBoxBoundProbe** bestimmt, ob der Strahl das Volume des umgebenden Felds der Box, nicht nur die Oberfläche des Felds, schneidet.

Die an **D3DXBoxBoundProbe** über gebenden Werte sind xmin, xmax, ymin, ymax, zmin und zmax. Folglich werden im folgenden die Ecken des umgebenden Felds definiert.


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



Die Tiefe des umgebenden Felds in der z-Richtung ist zmax-zmin, in der y-Richtung ist ymax-ymin, und in der x-Richtung ist xmax-xmin. Beispielsweise wird mit den folgenden minimalen und maximalen Vektoren min (-1,-1,-1) und Max (1, 1, 1) das umgebende Feld wie folgt definiert.


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
| Header  | D3DX10math. h |
| Bibliothek | D3dx10. lib  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
