---
description: Verwendet effiziente Ray-Tracing in PRT-Simulationen (preberechneten Radiance Transfer), um zu bestimmen, ob ein Strahl ein Mesh schneidet.
ms.assetid: e506aed3-bf14-4f29-845b-2091f5b00950
title: 'ID3DXPRTEngine:: closestrayintersekten-Methode (D3DX9Mesh. h)'
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
ms.openlocfilehash: 4fd802f636077c9ec2a9f0f1060ffd43493aabf1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219673"
---
# <a name="id3dxprtengineclosestrayintersects-method"></a>ID3DXPRTEngine:: closestrayintersekten-Methode

Verwendet effiziente Ray-Tracing in PRT-Simulationen (preberechneten Radiance Transfer), um zu bestimmen, ob ein Strahl ein Mesh schneidet. Wenn eine Schnittmenge gefunden wird, gibt die Methode den Index der nächstgelegenen Mesh-Oberfläche zurück, die vom Strahl und den baryzentrischen Koordinaten des Schnittstellen Punkts getroffen wird.

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

" *praypos* \[ " in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die den Punkt angibt, an dem das Ray beginnt.

</dd> <dt>

" *praydir* \[ " in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die normalisierte Richtung des Strahls angibt.

</dd> <dt>

*pfakeingedex* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ein Zeiger auf den Index der aktuellen Gitterfläche, die zuerst vom angegebenen Strahl getroffen wird, basierend auf dem Stapeln aller blocknetz Flächen vor dem aktuellen Mesh.

</dd> <dt>

*pU* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)\***

Zeiger auf eine baryzentrierte Treffer Koordinate, U, für Vertex 0 des Dreiecks.

</dd> <dt>

*PV* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)\***

Zeiger auf eine baryzentrierte Treffer Koordinate, V, für Scheitelpunkt 1 des Dreiecks.

</dd> <dt>

*pdist* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)\***

Zeiger auf den Abstand des Schnittpunkt entlang des Strahls.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **bool**](../winprog/windows-data-types.md)**

Gibt " **true** " zurück, wenn der Strahl das aktuelle Mesh überschneidet. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie [**ID3DXPRTEngine:: setminmaxschnittstrente**](id3dxprtengine--setminmaxintersection.md) , um den minimalen und maximalen Abstand der Schnittmenge mit dem Ray festzulegen.

Die barzentrische Koordinate des dritten Vertex (Vertex 2) des Dreiecks ist 1-(U + V).

Diese Methode wird langsamer ausgeführt als [**ID3DXPRTEngine:: shadowrayintersekten**](id3dxprtengine--shadowrayintersects.md). Verwenden Sie **ID3DXPRTEngine:: shadowrayintersekten** , wenn die Position des Schnitt Punkts nicht benötigt wird.

In den Scheitel Punkten des Dreiecks wird ein Punkt innerhalb eines Dreiecks definiert. Eine ausführlichere Beschreibung von baryzentrischen Koordinaten finden Sie in [der Beschreibung von mathworld in der Beschreibung der baryzentrierten Koordinaten](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine:: shadowrayintersekten**](id3dxprtengine--shadowrayintersects.md)
</dt> <dt>

[**ID3DXPRTEngine:: setminmaxschnitt Menge**](id3dxprtengine--setminmaxintersection.md)
</dt> </dl>

 

 
