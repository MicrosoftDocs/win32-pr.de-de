---
description: Bestimmt, ob sich ein Strahl mit einer Teilmenge dieses Netzes schneidet.
ms.assetid: 31f90141-60be-4c7f-8d6a-a1a97ff26d9d
title: ID3DX10Mesh::IntersectSubset-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.IntersectSubset
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a08d4db92dc75f40d0073367dda9a9ea26863418
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219613"
---
# <a name="id3dx10meshintersectsubset-method"></a>ID3DX10Mesh:: intersectsubset-Methode

Bestimmt, ob sich ein Strahl mit einer Teilmenge dieses Netzes schneidet.

## <a name="syntax"></a>Syntax


```C++
HRESULT IntersectSubset(
  [in]  UINT        AttribId,
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

*Atungbid* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Attribut-ID, die die Teilmenge des Netzes identifiziert.

</dd> <dt>

" *praypos* \[ " in\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Zeiger auf eine [**D3DXVECTOR3**](d3d10-d3dxvector3.md) -Struktur, die den Punkt angibt, an dem das Ray beginnt.

</dd> <dt>

" *praydir* \[ " in\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Zeiger auf eine [**D3DXVECTOR3**](d3d10-d3dxvector3.md) -Struktur, die die Richtung des Strahls angibt.

</dd> <dt>

*phitcount* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

Gibt an, wie oft sich der Strahl mit dem Mesh interniert hat.

</dd> <dt>

*pfakeingedex* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

Zeiger auf einen Indexwert der Oberfläche, die dem Ray-Ursprung am nächsten ist, wenn Phit **true** ist.

</dd> <dt>

*pU* \[ in\]
</dt> <dd>

Typ: **float \***

Zeiger auf eine baryzentrierte Treffer Koordinate, U.

</dd> <dt>

*PV* \[ in\]
</dt> <dd>

Typ: **float \***

Zeiger auf eine baryzentrierte Treffer Koordinate, V.

</dd> <dt>

*pdist* \[ in\]
</dt> <dd>

Typ: **float \***

Zeiger auf eine Strahl Schnittstellen-Parameter Entfernung.

</dd> <dt>

*ppallhits* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Zeiger auf eine [**ID3D10Blob-Schnittstelle**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob), die ein Array von [**d3dx10 \_ Intersect \_ Info**](d3dx10-intersect-info.md) -Strukturen enthält. Dies ist eine Liste aller Treffer, die im schnittschnitttest aufgetreten sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.

## <a name="remarks"></a>Bemerkungen

Diese API bietet eine Möglichkeit, Punkte in und um ein Dreieck zu verstehen, unabhängig davon, wo sich das Dreieck tatsächlich befindet. Diese Funktion gibt den resultierenden Punkt mithilfe der folgenden Gleichung zurück: v1 + U (V2-V1) + V (v3-v1).

Jeder Punkt in der Ebene V1V2V3 kann durch die baryzentrische Koordinate (U, V) dargestellt werden. Mit dem Parameter U wird gesteuert, wie viel v2 in das Ergebnis gewichtet wird, und mit dem Parameter V wird gesteuert, wie viel v3 in das Ergebnis gewichtet wird. Schließlich steuert der Wert von \[ 1-(U + V), \] wie viel V1 in das Ergebnis gewichtet wird.

Baryzentrierte Koordinaten sind eine Form allgemeiner Koordinaten. In diesem Kontext stellt die Verwendung von barzentrischen Koordinaten eine Änderung in Koordinatensystemen dar. Was für kartesische Koordinaten true ist, ist für barzentrierte Koordinaten "true".

In den Scheitel Punkten des Dreiecks wird ein Punkt innerhalb eines Dreiecks definiert. Eine ausführlichere Beschreibung von baryzentrischen Koordinaten finden Sie in [der Beschreibung von mathworld in der Beschreibung der baryzentrierten Koordinaten](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
