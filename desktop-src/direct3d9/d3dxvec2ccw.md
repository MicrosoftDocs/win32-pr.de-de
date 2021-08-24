---
description: Gibt die z-Komponente zurück, indem das Kreuzprodukt von zwei 2D-Vektoren verwendet wird.
ms.assetid: daec19f2-cd0f-4a68-affc-9a42bda8912c
title: D3DXVec2CCW-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2CCW
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2b38adaf28b6e2394608cfb6f73f4a39d803d4fd5106f826d810a5c8dfd02618
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119630700"
---
# <a name="d3dxvec2ccw-function"></a>D3DXVec2CCW-Funktion

Gibt die z-Komponente zurück, indem das Kreuzprodukt von zwei 2D-Vektoren verwendet wird.

## <a name="syntax"></a>Syntax


```C++
FLOAT D3DXVec2CCW(
  _In_ const D3DXVECTOR2 *pV1,
  _In_ const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pV1* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Zeiger auf eine [**D3DXVECTOR2-Quellstruktur.**](d3dxvector2.md)

</dd> <dt>

*pV2* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Zeiger auf eine [**D3DXVECTOR2-Quellstruktur.**](d3dxvector2.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Die z-Komponente.

## <a name="remarks"></a>Hinweise

Diese Funktion bestimmt die z-Komponente, indem sie das Kreuzprodukt anhand der folgenden Formel bestimmt: ((x1,y1,0) cross (x2,y2,0)). Oder wie im folgenden Beispiel gezeigt.


```
pV1->x * pV2->y - pV1->y * pV2->x
```



Wenn der Wert der z-Komponente positiv ist, ist der Vektor V2 gegen den Uhrzeigersinn vom Vektor V1. Diese Informationen sind für das Back-Face-Culling nützlich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2Dot**](d3dxvec2dot.md)
</dt> </dl>

 

 
