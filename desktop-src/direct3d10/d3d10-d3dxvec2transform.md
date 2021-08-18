---
description: 'D3DXVec2Transform-Funktion (D3DX10Math.h): Transformiert einen 2D-Vektor durch eine angegebene Matrix.'
ms.assetid: 4b57eb7f-fae9-48ac-a806-510da75d25a6
title: D3DXVec2Transform-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Transform
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 18b239ea888d576dcbcc87b07944efb21a77ac9f13f671b2bd4f096b93b976de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990690"
---
# <a name="d3dxvec2transform-function-d3dx10mathh"></a>D3DXVec2Transform-Funktion (D3DX10Math.h)

Transformiert einen 2D-Vektor durch eine angegebene Matrix.

## <a name="syntax"></a>Syntax


```C++
D3DXVECTOR4* D3DXVec2Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Zeiger auf die [**D3DXVECTOR4-Struktur,**](d3d10-d3dxvector4.md) die das Ergebnis des Vorgangs ist.

</dd> <dt>

*pV* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Zeiger auf die [**D3DXVECTOR2-Quelle.**](d3d10-d3dxvector2.md)

</dd> <dt>

*pM* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Zeiger auf die [**D3DXMATRIX-Quellstruktur.**](d3d10-d3dxmatrix.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Zeiger auf eine D3DXVECTOR4-Struktur, die der transformierte Vektor ist.

## <a name="remarks"></a>Hinweise

Diese Funktion transformiert den Vektor pV (x, y, 0, 1) durch die Matrix-pM.

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann die D3DXVec2Transform-Funktion als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
