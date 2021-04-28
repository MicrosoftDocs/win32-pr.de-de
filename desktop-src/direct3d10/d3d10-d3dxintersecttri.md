---
description: 'D3DXIntersectTri-Funktion (D3DX10math.h): Berechnet die Schnittmenge eines Strahls und eines Dreiecks.'
ms.assetid: 819f2543-8046-47c9-93b8-7d888264786f
title: D3DXIntersectTri-Funktion (D3DX10math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c8bf502cca48701a7d71a083e515f9988cafe303
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113238"
---
# <a name="d3dxintersecttri-function-d3dx10mathh"></a>D3DXIntersectTri-Funktion (D3DX10math.h)

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

Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3d10-d3dxvector3.md) die die Erste Dreiecksvertexposition beschreibt.

</dd> <dt>

*p1* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3d10-d3dxvector3.md) die die Position des zweiten Dreiecks vertex beschreibt.

</dd> <dt>

*p2* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3d10-d3dxvector3.md) die die Position des dritten Dreiecks vertex beschreibt.

</dd> <dt>

*pRayPos* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3d10-d3dxvector3.md) wobei der Punkt angegeben wird, an dem der Strahl beginnt.

</dd> <dt>

*pRayDir* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur**](d3d10-d3dxvector3.md) unter Angabe der Richtung des Strahls.

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

Jeder Punkt in der Ebene V1V2V3 kann durch die baryzentrische Koordinate (U,V) dargestellt werden. Der Parameter U steuert, wie viel V2 in das Ergebnis gewichtet wird, und der Parameter V steuert, wie viel V3 in das Ergebnis gewichtet wird. Schließlich steuert der Wert von 1 – \[ (U + V), \] wie viel V1 in das Ergebnis gewichtet wird.

Barycentric-Koordinaten sind eine Form allgemeiner Koordinaten. In diesem Kontext stellt die Verwendung von baryzentrischen Koordinaten eine Änderung der Koordinatensysteme dar. Was für kartesische Koordinaten gilt, gilt für baryzentrische Koordinaten.

Barycentric-Koordinaten definieren einen Punkt innerhalb eines Dreiecks in Bezug auf die Scheitelpunkte des Dreiecks. Eine ausführlichere Beschreibung der baryzentrischen Koordinaten finden Sie unter [Mathworld es Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mesh-Funktionen](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
