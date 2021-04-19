---
description: Berechnet die Schnittmenge eines Strahls und eines Dreiecks.
ms.assetid: f335a71d-7203-4ea1-a6bf-407b28c712e6
title: D3DXIntersectTri-Funktion (D3DX9Mesh. h)
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
ms.openlocfilehash: 41c7012cea0a533dc447db0575def6b418d0e59e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363137"
---
# <a name="d3dxintersecttri-function-d3dx9meshh"></a>D3DXIntersectTri-Funktion (D3DX9Mesh. h)

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

*P0* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die Position des ersten Dreiecks Scheitel Punkts beschreibt.

</dd> <dt>

*P1* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die Position des zweiten Dreiecks Vertex beschreibt.

</dd> <dt>

*P2* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die dritte Position des Dreiecks Vertex beschreibt.

</dd> <dt>

" *praypos* \[ " in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die den Punkt angibt, an dem das Ray beginnt.

</dd> <dt>

" *praydir* \[ " in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die Richtung des Strahls angibt.

</dd> <dt>

*pU* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)\***

Baryzentrierte Treffer Koordinaten, U.

</dd> <dt>

*PV* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)\***

Für den baryzentrischen Treffer, V.

</dd> <dt>

*pdist* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)\***

Der Ray-schnittungsparameter.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **bool**](../winprog/windows-data-types.md)**

Gibt " **true** " zurück, wenn das Strahl den Bereich des Dreiecks schneidet. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Die [**D3DXIntersect**](d3dxintersect.md) -Funktion bietet eine Möglichkeit, Punkte in und um ein Dreieck zu verstehen, unabhängig davon, wo sich das Dreieck tatsächlich befindet. Diese Funktion gibt den resultierenden Punkt mithilfe der folgenden Gleichung zurück: v1 + U (V2-V1) + V (v3-v1).

Jeder Punkt in der Ebene V1V2V3 kann durch die baryzentrische Koordinate (U, V) dargestellt werden. Mit dem Parameter U wird gesteuert, wie viel v2 in das Ergebnis gewichtet wird, und mit dem Parameter V wird gesteuert, wie viel v3 in das Ergebnis gewichtet wird. Schließlich steuert der Wert von \[ 1-(U + V), \] wie viel V1 in das Ergebnis gewichtet wird.

Baryzentrierte Koordinaten sind eine Form allgemeiner Koordinaten. In diesem Kontext stellt die Verwendung von barzentrischen Koordinaten eine Änderung in Koordinatensystemen dar. Was für kartesische Koordinaten true ist, ist für barzentrierte Koordinaten "true".

In den Scheitel Punkten des Dreiecks wird ein Punkt innerhalb eines Dreiecks definiert. Eine ausführlichere Beschreibung von baryzentrischen Koordinaten finden Sie in [der Beschreibung von mathworld in der Beschreibung der baryzentrierten Koordinaten](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
