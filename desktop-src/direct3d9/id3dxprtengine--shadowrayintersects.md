---
description: Verwendet effiziente Ray-Tracing in PRT-Simulationen (preberechneten Radiance Transfer), um zu bestimmen, ob ein Strahl ein Mesh schneidet. Wird normalerweise verwendet, um zu bestimmen, ob ein bestimmter Punkt im Schatten ist.
ms.assetid: fcd53a0f-80e8-4013-8efd-125e38f4ccd0
title: 'ID3DXPRTEngine:: shadowrayintersekten-Methode (D3DX9Mesh. h)'
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
ms.openlocfilehash: 701aa4c89ee6a9d657721d872565c9b2056bb435
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050877"
---
# <a name="id3dxprtengineshadowrayintersects-method"></a>ID3DXPRTEngine:: shadowrayintersekten-Methode

Verwendet effiziente Ray-Tracing in PRT-Simulationen (preberechneten Radiance Transfer), um zu bestimmen, ob ein Strahl ein Mesh schneidet. Wird normalerweise verwendet, um zu bestimmen, ob ein bestimmter Punkt im Schatten ist.

## <a name="syntax"></a>Syntax


```C++
BOOL ShadowRayIntersects(
  [in] const D3DXVECTOR3 *pRayPos,
  [in] const D3DXVECTOR3 *pRayDir
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

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **bool**](../winprog/windows-data-types.md)**

Gibt " **true** " zurück, wenn der Strahl das aktuelle Mesh überschneidet. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie [**ID3DXPRTEngine:: setminmaxschnittstrente**](id3dxprtengine--setminmaxintersection.md) , um den minimalen und maximalen Abstand der Schnittmenge mit dem Ray festzulegen.

Diese Methode wird schneller ausgeführt als [**ID3DXPRTEngine:: closestrayintersekten**](id3dxprtengine--closestrayintersects.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine:: closestrayintersekten**](id3dxprtengine--closestrayintersects.md)
</dt> <dt>

[**ID3DXPRTEngine:: setminmaxschnitt Menge**](id3dxprtengine--setminmaxintersection.md)
</dt> </dl>

 

 
