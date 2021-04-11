---
description: Bestimmt, ob ein Strahl das Volume des umgebenden Felds eines Felds schneidet.
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
ms.openlocfilehash: 707ab21a3babe7d9a93f776f438cbaab7137849b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132353"
---
# <a name="d3dxboxboundprobe-function"></a>D3DXBoxBoundProbe-Funktion

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

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die linke untere Ecke des Begrenzungs Rahmens beschreibt. Siehe Hinweise.

</dd> <dt>

*pmax* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die obere rechte Ecke des Begrenzungs Rahmens beschreibt. Siehe Hinweise.

</dd> <dt>

" *prayposition* \[ " in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die Ursprungs Koordinate des Strahls angibt.

</dd> <dt>

" *praydirection* \[ " in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die Richtung des Strahls angibt. Dieser Vektor sollte nicht (0, 0, 0) sein, muss jedoch nicht normalisiert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **bool**](../winprog/windows-data-types.md)**

Gibt " **true** " zurück, wenn der Strahl das Volume des umgebenden Felds der Box schneidet. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

**D3DXboxBoundProbe** bestimmt, ob der Strahl das Volume des umgebenden Felds der Box, nicht nur die Oberfläche des Felds, schneidet.

Die an **D3DXboxBoundProbe** über gebenden Werte sind xmin, xmax, ymin, ymax, zmin und zmax. Folglich werden im folgenden die Ecken des umgebenden Felds definiert.


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
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXComputeBoundingBox**](d3dxcomputeboundingbox.md)
</dt> </dl>

 

 
