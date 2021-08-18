---
description: 'D3DXVec3TransformCoord-Funktion (D3DX10Math.h): Transformiert einen 3D-Vektor durch eine bestimmte Matrix und projiziert das Ergebnis zurück in w = 1.'
ms.assetid: e138fdc0-6999-45ab-8bcf-54f53bd9b1bf
title: D3DXVec3TransformCoord-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformCoord
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: b50c6680a52ef64e46e8dace325f124362e4efa79576e0d386c445a3766bf943
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729910"
---
# <a name="d3dxvec3transformcoord-function-d3dx10mathh"></a>D3DXVec3TransformCoord-Funktion (D3DX10Math.h)

Transformiert einen 3D-Vektor durch eine bestimmte Matrix und projiziert das Ergebnis zurück in w = 1.

## <a name="syntax"></a>Syntax


```C++
D3DXVECTOR3* D3DXVec3TransformCoord(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Zeiger auf [**D3DXVECTOR3,**](d3d10-d3dxvector3.md) das das Ergebnis des Vorgangs ist.

</dd> <dt>

*pV* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf die D3DXVECTOR3-Quellstruktur.

</dd> <dt>

*pM* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Zeiger auf die [**D3DXMATRIX-Quellstruktur.**](d3d10-d3dxmatrix.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Zeiger auf eine D3DXVECTOR3-Struktur, die der transformierte Vektor ist.

## <a name="remarks"></a>Hinweise

Diese Funktion transformiert den Vektor pV (x, y, z, 1) durch die Matrix pM und projiziert das Ergebnis zurück in w=1.

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann die D3DXVec3TransformCoord-Funktion als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Math.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
