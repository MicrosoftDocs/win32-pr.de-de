---
description: Bestimmt, ob sich ein Strahl mit einem Mesh schneidet.
ms.assetid: 325f5b40-80ba-4400-a143-bae41146ab07
title: D3DXIntersect-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersect
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc877fb1301e01b05184625ba2e92a2c680cfa9f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366461"
---
# <a name="d3dxintersect-function"></a>D3DXIntersect-Funktion

Bestimmt, ob sich ein Strahl mit einem Mesh schneidet.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXIntersect(
  _In_        LPD3DXBASEMESH pMesh,
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

*pmesh* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

Zeiger auf eine [**ID3DXBaseMesh**](id3dxbasemesh.md) -Schnittstelle, die das zu testende Mesh darstellt.

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

*Phit* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)\***

Zeiger auf einen booleschen Werten. Wenn das Strahl eine Dreiecksfläche im Mesh schneidet, wird dieser Wert auf " **true**" festgelegt. Andernfalls wird dieser Wert auf " **false**" festgelegt.

</dd> <dt>

*pfakeingedex* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Zeiger auf einen Indexwert der Oberfläche, die dem Ray-Ursprung am nächsten ist, wenn Phit **true** ist.

</dd> <dt>

*pU* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)\***

Zeiger auf eine baryzentrierte Treffer Koordinate, U.

</dd> <dt>

*PV* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)\***

Zeiger auf eine baryzentrierte Treffer Koordinate, V.

</dd> <dt>

*pdist* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)\***

Zeiger auf eine Strahl Schnittstellen-Parameter Entfernung.

</dd> <dt>

*ppallhits* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Zeiger auf ein [**ID3DXBuffer**](id3dxbuffer.md) -Objekt, das ein Array von [**D3DXINTERSECTINFO**](d3dxintersectinfo.md) -Strukturen enthält.

</dd> <dt>

*pgräfin-Steuer Treffer* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Zeiger auf ein DWORD, das die Anzahl der Einträge im ppallhits-Array enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert lauten: E \_ outo-Memory.

## <a name="remarks"></a>Bemerkungen

Die **D3DXIntersect** -Funktion bietet eine Möglichkeit, Punkte in und um ein Dreieck zu verstehen, unabhängig davon, wo sich das Dreieck tatsächlich befindet. Diese Funktion gibt den resultierenden Punkt mithilfe der folgenden Gleichung zurück: v1 + U (V2-V1) + V (v3-v1).

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

 

 
