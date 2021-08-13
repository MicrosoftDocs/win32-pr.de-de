---
description: Überschneidet den angegebenen Strahl mit der angegebenen Netzteilmenge. Dies bietet ähnliche Funktionen wie D3DXIntersect.
ms.assetid: 4a757b9e-18eb-424e-9f3e-cdf917c23787
title: D3DXIntersectSubset-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersectSubset
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 95a987730706f32654aab8f63feed61ae87c4d58d27ccccdaed9767d3303bbf8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460380"
---
# <a name="d3dxintersectsubset-function"></a>D3DXIntersectSubset-Funktion

Überschneidet den angegebenen Strahl mit der angegebenen Netzteilmenge. Dies bietet ähnliche Funktionen wie [**D3DXIntersect.**](d3dxintersect.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXIntersectSubset(
  _In_        LPD3DXBASEMESH pMesh,
  _In_        DWORD          AttribId,
  _In_  const D3DXVECTOR3    *pRayPos,
  _In_  const D3DXVECTOR3    *pRayDir,
  _Out_       BOOL           *pHit,
  _Out_       DWORD          *pFaceIndex,
  _Out_       FLOAT          *pU,
  _Out_       FLOAT          *pV,
  _Out_       FLOAT          *pDist,
  _Out_       LPD3DXBUFFER   *ppAllHits,
  _Out_       DWORD          *pCountOfHits
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMesh* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

Zeiger auf eine [**ID3DXBaseMesh-Schnittstelle,**](id3dxbasemesh.md) die das zu testete Gitternetz darstellt. Das Gitternetz muss nach Attribut sortiert sein.

</dd> <dt>

*AttribId* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Attributbezeichner der Teilmenge, mit der die Schnittmenge überschneidet werden soll.

</dd> <dt>

*pRayPos* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) wobei der Punkt angegeben wird, an dem der Strahl beginnt.

</dd> <dt>

*pRayDir* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur**](d3dxvector3.md) unter Angabe der Richtung des Strahls.

</dd> <dt>

*pHit* \[ out\]
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)\***

Zeiger auf eine BOOL. Wenn der Strahl ein dreieckiges Gesicht im Netz schneidet, wird dieser Wert auf **TRUE festgelegt.** Andernfalls wird dieser Wert auf **FALSE festgelegt.**

</dd> <dt>

*pFaceIndex* \[ out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Zeiger auf einen Indexwert des Gesichts, das dem Ray-Ursprung am nächsten ist, wenn pHit **TRUE ist.**

</dd> <dt>

*pU* \[ out\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Zeiger auf eine baryzentrierte Trefferkoordinate, U.

</dd> <dt>

*pV* \[ out\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Zeiger auf eine baryzentrierte Trefferkoordinate, V.

</dd> <dt>

*pDist* \[ out\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Zeiger auf den Abstand eines Ray-Schnittpunktparameters.

</dd> <dt>

*ppAllHits* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Array von [**D3DXINTERSECTINFO-Strukturen,**](d3dxintersectinfo.md) die alle Treffer darstellen, nicht nur die nächstgelegenen Treffer.

</dd> <dt>

*pCountOfHits* \[ out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Anzahl der Elemente im Array, die von ppAllHits zurückgegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert folgender Wert sein: E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Die **D3DXIntersectSubset-Funktion** bietet eine Möglichkeit, Punkte in und um ein Dreieck zu verstehen, unabhängig davon, wo sich das Dreieck tatsächlich befindet. Diese Funktion gibt den resultierenden Punkt mithilfe der folgenden Gleichung zurück: V1 + U(V2 - V1) + V(V3 - V1).

Jeder Punkt in der Ebene V1V2V3 kann durch die baryzentrierte Koordinate (U,V) dargestellt werden. Der Parameter U steuert, wie viel V2 in das Ergebnis gewichtet wird, und der Parameter V steuert, wie viel V3 in das Ergebnis gewichtet wird. Schließlich steuert der Wert von 1 – (U + V), wie viel \[ \] V1 in das Ergebnis gewichtet wird.

Baryzentrierte Koordinaten sind eine Form allgemeiner Koordinaten. In diesem Kontext stellt die Verwendung von baryzentrierten Koordinaten eine Änderung der Koordinatensysteme dar. Was für kartesische Koordinaten zutrifft, gilt für baryzentrierte Koordinaten.

Baryzentrierte Koordinaten definieren einen Punkt innerhalb eines Dreiecks in Bezug auf die Scheitelpunkt des Dreiecks. Eine detailliertere Beschreibung der baryzentrierten Koordinaten finden Sie unter [Beschreibung der baryzentrierten Koordinaten von Mathworld.](https://mathworld.wolfram.com/BarycentricCoordinates.html)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
