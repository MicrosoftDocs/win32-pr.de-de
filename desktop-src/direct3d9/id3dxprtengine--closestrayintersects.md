---
description: Verwendet effiziente Ray-Tracing in PRT-Simulationen (Precomputed Radiance Transfer), um zu bestimmen, ob ein Strahl ein Gittermodell überschneidet.
ms.assetid: e506aed3-bf14-4f29-845b-2091f5b00950
title: ID3DXPRTEngine::ClosestRayIntersects-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ClosestRayIntersects
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a2620140337807891efa739da4540e3895394f63bcc494396c13e7c15d0c1b29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729786"
---
# <a name="id3dxprtengineclosestrayintersects-method"></a>ID3DXPRTEngine::ClosestRayIntersects-Methode

Verwendet effiziente Ray-Tracing in PRT-Simulationen (Precomputed Radiance Transfer), um zu bestimmen, ob ein Strahl ein Gittermodell überschneidet. Wenn eine Schnittmenge gefunden wird, gibt die -Methode den Index des nächstgelegenen Gittergesichts zurück, das vom Strahl und den baryzentrischen Koordinaten des Schnittpunkts erreicht wird.

## <a name="syntax"></a>Syntax


```C++
BOOL ClosestRayIntersects(
  [in]  const D3DXVECTOR3 *pRayPos,
  [in]  const D3DXVECTOR3 *pRayDir,
  [in]        DWORD       *pFaceIndex,
  [out]       FLOAT       *pU,
  [out]       FLOAT       *pV,
  [out]       FLOAT       *pDist
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pRayPos* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) der den Punkt angibt, an dem der Strahl beginnt.

</dd> <dt>

*pRayDir* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die die normalisierte Richtung des Strahls angibt.

</dd> <dt>

*pFaceIndex* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Zeiger auf den Index des aktuellen Netzgesichts, das zuerst vom angegebenen Strahl getroffen wird, basierend auf dem Stapeln aller Blocknetzflächen vor dem aktuellen Gitter.

</dd> <dt>

*pU* \[ out\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Zeiger auf eine baryzentrische Trefferkoordinate, U, für den Scheitelpunkt 0 des Dreiecks.

</dd> <dt>

*pV* \[ out\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Zeiger auf eine barycentric-Trefferkoordinate V für Scheitelpunkt 1 des Dreiecks.

</dd> <dt>

*pDist* \[ out\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Zeiger auf den Abstand des Schnittpunkts entlang des Strahls.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

Gibt **TRUE** zurück, wenn der Strahl das aktuelle Gitternetz überschneidet. andernfalls gibt **FALSE** zurück.

## <a name="remarks"></a>Hinweise

Verwenden Sie [**ID3DXPRTEngine::SetMinMaxIntersection,**](id3dxprtengine--setminmaxintersection.md) um minimale und maximale Entfernungen der Schnittmenge mit dem Strahl festzulegen.

Die balyzentrische Koordinate des dritten Scheitelpunkts (Scheitelpunkt 2) des Dreiecks ist 1 – ( U + V ).

Diese Methode wird langsamer als [**ID3DXPRTEngine::ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md)ausgeführt. Verwenden Sie **ID3DXPRTEngine::ShadowRayIntersects,** wenn die Position des Schnittpunkts nicht benötigt wird.

Barycentric-Koordinaten definieren einen Punkt innerhalb eines Dreiecks in Bezug auf die Scheitelpunkte des Dreiecks. Eine ausführlichere Beschreibung der baryzentrischen Koordinaten finden Sie unter [Mathworld es Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md)
</dt> <dt>

[**ID3DXPRTEngine::SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md)
</dt> </dl>

 

 
