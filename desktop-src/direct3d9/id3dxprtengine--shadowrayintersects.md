---
description: Verwendet effiziente Ray-Tracing in PRT-Simulationen (Precomputed Radiance Transfer), um zu bestimmen, ob ein Strahl ein Gitter schneidet. Wird normalerweise verwendet, um zu bestimmen, ob sich ein angegebener Punkt im Schatten befindet.
ms.assetid: fcd53a0f-80e8-4013-8efd-125e38f4ccd0
title: ID3DXPRTEngine::ShadowRayIntersects-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ShadowRayIntersects
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5064e788d89de6e5143ad826a4f61a4afd802931c6964193c8fa46626edf955d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729594"
---
# <a name="id3dxprtengineshadowrayintersects-method"></a>ID3DXPRTEngine::ShadowRayIntersects-Methode

Verwendet effiziente Ray-Tracing in PRT-Simulationen (Precomputed Radiance Transfer), um zu bestimmen, ob ein Strahl ein Gitter schneidet. Wird normalerweise verwendet, um zu bestimmen, ob sich ein angegebener Punkt im Schatten befindet.

## <a name="syntax"></a>Syntax


```C++
BOOL ShadowRayIntersects(
  [in] const D3DXVECTOR3 *pRayPos,
  [in] const D3DXVECTOR3 *pRayDir
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pRayPos* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) wobei der Punkt angegeben wird, an dem der Strahl beginnt.

</dd> <dt>

*pRayDir* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur**](d3dxvector3.md) unter Angabe der normalisierten Richtung des Strahls.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

Gibt **TRUE zurück,** wenn der Strahl das aktuelle Gitter schneidet. andernfalls gibt **FALSE zurück.**

## <a name="remarks"></a>Hinweise

Verwenden [**Sie ID3DXPRTEngine::SetMinMaxIntersection,**](id3dxprtengine--setminmaxintersection.md) um minimale und maximale Schnittmengen mit dem Strahl zu setzen.

Diese Methode wird schneller als [**ID3DXPRTEngine::ClosestRayIntersects ausgeführt.**](id3dxprtengine--closestrayintersects.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ClosestRayIntersects**](id3dxprtengine--closestrayintersects.md)
</dt> <dt>

[**ID3DXPRTEngine::SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md)
</dt> </dl>

 

 
