---
description: Bestimmt das Punktprodukt von zwei 2D-Vektoren.
ms.assetid: ae77ff29-44be-4b67-9c63-aaffa4fe8d59
title: D3DXVec2Dot-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Dot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 98cb865ebd075dcd78db8200b18de1644107e9a497b977fe062017c758e52256
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523826"
---
# <a name="d3dxvec2dot-function"></a>D3DXVec2Dot-Funktion

Bestimmt das Punktprodukt von zwei 2D-Vektoren.

## <a name="syntax"></a>Syntax


```C++
FLOAT D3DXVec2Dot(
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

Das Skalarprodukt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2CCW**](d3dxvec2ccw.md)
</dt> </dl>

 

 
