---
description: Gibt einen 2D-Vektor zurück, der aus den größten Komponenten von zwei 2D-Vektoren besteht.
ms.assetid: 5eb5141b-d611-4c6b-a3e3-c7ad8f223657
title: D3DXVec2Maximize-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Maximize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ad2c68d7ab26a6aa80f5abb08207702433d55c6dc12473d94a87a2b1c3b25249
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044638"
---
# <a name="d3dxvec2maximize-function"></a>D3DXVec2Maximize-Funktion

Gibt einen 2D-Vektor zurück, der aus den größten Komponenten von zwei 2D-Vektoren besteht.

## <a name="syntax"></a>Syntax


```C++
D3DXVECTOR2* D3DXVec2Maximize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Zeiger auf die [**D3DXVECTOR2-Struktur,**](d3dxvector2.md) die das Ergebnis des Vorgangs ist.

</dd> <dt>

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

Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Zeiger auf eine [**D3DXVECTOR2-Struktur,**](d3dxvector2.md) die aus den größten Komponenten der beiden Vektoren besteht.

## <a name="remarks"></a>Hinweise

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird. Auf diese Weise kann die **D3DXVec2Maximize-Funktion** als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2Minimize**](d3dxvec2minimize.md)
</dt> </dl>

 

 




