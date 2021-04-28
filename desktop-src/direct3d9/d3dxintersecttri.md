---
description: 'D3DXIntersectTri-Funktion (D3DX9Mesh.h): Berechnet die Schnittmenge eines Strahls und eines Dreiecks.'
ms.assetid: f335a71d-7203-4ea1-a6bf-407b28c712e6
title: D3DXIntersectTri-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersectTri
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 33d45beda51a7a2c80debafbab864c2accb33653
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098268"
---
# <a name="d3dxintersecttri-function-d3dx9meshh"></a>D3DXIntersectTri-Funktion (D3DX9Mesh.h)

Berechnet die Schnittmenge eines Strahls und eines Dreiecks.

## <a name="syntax"></a>Syntax


```C++
BOOL D3DXIntersectTri(
  _In_  const D3DXVECTOR3 *p0,
  _In_  const D3DXVECTOR3 *p1,
  _In_  const D3DXVECTOR3 *p2,
  _In_  const D3DXVECTOR3 *pRayPos,
  _In_  const D3DXVECTOR3 *pRayDir,
  _Out_       FLOAT       *pU,
  _Out_       FLOAT       *pV,
  _Out_       FLOAT       *pDist
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*p0* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die die position des ersten Dreiecksvertex beschreibt.

</dd> <dt>

*p1* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die die position des zweiten Dreiecksvertex beschreibt.

</dd> <dt>

*p2* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die die Position des dritten Dreiecksvertex beschreibt.

</dd> <dt>

*pRayPos* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) der den Punkt angibt, an dem der Strahl beginnt.

</dd> <dt>

*pRayDir* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die die Richtung des Strahls angibt.

</dd> <dt>

*pU* \[ out\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Barycentric-Trefferkoordinaten, U.

</dd> <dt>

*pV* \[ out\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Barycentric-Trefferkoordinaten, V.

</dd> <dt>

*pDist* \[ out\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Entfernung des Ray-Intersection-Parameters.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

Gibt **TRUE** zurück, wenn der Strahl den Bereich des Dreiecks überschneidet. Andernfalls gibt **FALSE** zurück.

## <a name="remarks"></a>Bemerkungen

Die [**D3DXIntersect-Funktion**](d3dxintersect.md) bietet eine Möglichkeit, Punkte in und um ein Dreieck zu verstehen, unabhängig davon, wo sich das Dreieck tatsächlich befindet. Diese Funktion gibt den resultierenden Punkt mithilfe der folgenden Gleichung zurück: V1 + U(V2 - V1) + V(V3 - V1).

Jeder Punkt in der Ebene V1V2V3 kann durch die baryzentrische Koordinate (U,V) dargestellt werden. Der Parameter U steuert, wie viel V2 in das Ergebnis gewichtet wird, und der Parameter V steuert, wie viel V3 in das Ergebnis gewichtet wird. Schließlich steuert der Wert von 1 – \[ (U + V), \] wie viel V1 in das Ergebnis gewichtet wird.

Barycentric-Koordinaten sind eine Form allgemeiner Koordinaten. In diesem Kontext stellt die Verwendung von baryzentrischen Koordinaten eine Änderung der Koordinatensysteme dar. Was für kartesische Koordinaten gilt, gilt für baryzentrische Koordinaten.

Barycentric-Koordinaten definieren einen Punkt innerhalb eines Dreiecks in Bezug auf die Scheitelpunkte des Dreiecks. Eine detailliertere Beschreibung der baryzentrierten Koordinaten finden Sie unter [Beschreibung der baryzentrierten Koordinaten von Mathworld.](https://mathworld.wolfram.com/BarycentricCoordinates.html)

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
