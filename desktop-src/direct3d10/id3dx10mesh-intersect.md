---
description: Bestimmt, ob sich ein Strahl mit diesem Netz überschneidet.
ms.assetid: 74565d4a-94e6-4faa-bf70-9c1b35e5e5d8
title: ID3DX10Mesh::Intersect-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Intersect
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1693db027baad13d69c43e394407ed8eb037d2dbb95eb217ccca473d1f91d08a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634550"
---
# <a name="id3dx10meshintersect-method"></a>ID3DX10Mesh::Intersect-Methode

Bestimmt, ob sich ein Strahl mit diesem Netz überschneidet.

## <a name="syntax"></a>Syntax


```C++
HRESULT Intersect(
  [in]  D3DXVECTOR3 *pRayPos,
  [in]  D3DXVECTOR3 *pRayDir,
  [in]  UINT        *pHitCount,
  [in]  UINT        *pFaceIndex,
  [in]  float       *pU,
  [in]  float       *pV,
  [in]  float       *pDist,
  [out] ID3D10Blob  **ppAllHits
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pRayPos* \[ In\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3d10-d3dxvector3.md) wobei der Punkt angegeben wird, an dem der Strahl beginnt.

</dd> <dt>

*pRayDir* \[ In\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Zeiger auf eine [**D3DXVECTOR3-Struktur**](d3d10-d3dxvector3.md) unter Angabe der Richtung des Strahls.

</dd> <dt>

*pHitCount* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Die Anzahl der Schnitte des Strahls mit dem Gitter.

</dd> <dt>

*pFaceIndex* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Zeiger auf einen Indexwert des Gesichts, das dem Ray-Ursprung am nächsten ist, wenn pHit **TRUE ist.**

</dd> <dt>

*pU* \[ In\]
</dt> <dd>

Typ: **\* float**

Zeiger auf eine baryzentrierte Trefferkoordinate, U.

</dd> <dt>

*pV* \[ In\]
</dt> <dd>

Typ: **\* float**

Zeiger auf eine baryzentrierte Trefferkoordinate, V.

</dd> <dt>

*pDist* \[ In\]
</dt> <dd>

Typ: **\* float**

Zeiger auf den Abstand eines Ray-Schnittpunktparameters.

</dd> <dt>

*ppAllHits* \[ out\]
</dt> <dd>

Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Zeiger auf eine [**ID3D10Blob-Schnittstelle,**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)die ein Array von [**D3DX10 \_ INTERSECT \_ INFO-Strukturen**](d3dx10-intersect-info.md) enthält. Dies ist eine Liste aller Treffer, die beim Schnittmengentest aufgetreten sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Unter [Direct3D 10-Rückgabecodes aufgeführten Werte.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

Diese API bietet eine Möglichkeit, Punkte in und um ein Dreieck zu verstehen, unabhängig davon, wo sich das Dreieck tatsächlich befindet. Diese Funktion gibt den resultierenden Punkt mithilfe der folgenden Gleichung zurück: V1 + U(V2 - V1) + V(V3 - V1).

Jeder Punkt in der Ebene V1V2V3 kann durch die baryzentrierte Koordinate (U,V) dargestellt werden. Der Parameter U steuert, wie viel V2 in das Ergebnis gewichtet wird, und der Parameter V steuert, wie viel V3 in das Ergebnis gewichtet wird. Schließlich steuert der Wert von 1 – (U + V), wie viel \[ \] V1 in das Ergebnis gewichtet wird.

Baryzentrierte Koordinaten sind eine Form allgemeiner Koordinaten. In diesem Kontext stellt die Verwendung von baryzentrierten Koordinaten eine Änderung der Koordinatensysteme dar. Was für kartesische Koordinaten gilt, gilt für baryzentrierte Koordinaten.

Baryzentrierte Koordinaten definieren einen Punkt innerhalb eines Dreiecks in Bezug auf die Scheitelpunkt des Dreiecks. Eine detailliertere Beschreibung der baryzentrierten Koordinaten finden Sie unter [Beschreibung der baryzentrierten Koordinaten von Mathworld.](https://mathworld.wolfram.com/BarycentricCoordinates.html)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
