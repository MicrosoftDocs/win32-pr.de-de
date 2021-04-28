---
description: 'D3DXVec3TransformCoord-Funktion (D3dx9math.h): Transformiert einen 3D-Vektor durch eine bestimmte Matrix und projektiert das Ergebnis zurück in w = 1.'
ms.assetid: 4075b067-1e64-46c9-be73-5fa765c9cb9d
title: D3DXVec3TransformCoord-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformCoord
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e4e3514d4717262a7afab7ae808d747de3a1b635
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115628"
---
# <a name="d3dxvec3transformcoord-function-d3dx9mathh"></a>D3DXVec3TransformCoord-Funktion (D3dx9math.h)

Transformiert einen 3D-Vektor durch eine bestimmte Matrix und projektiert das Ergebnis zurück in w = 1.

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

Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Zeiger auf die [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die das Ergebnis des Vorgangs ist.

</dd> <dt>

*pV* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf die [**D3DXVECTOR3-Quellstruktur.**](d3dxvector3.md)

</dd> <dt>

*pM* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Zeiger auf die [**D3DXMATRIX-Quellstruktur.**](d3dxmatrix.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die der transformierte Vektor ist.

## <a name="remarks"></a>Bemerkungen

Diese Funktion transformiert den Vektor *pV* (x, y, z, 1) durch die Matrix *pM* und projektiert das Ergebnis wieder in w=1.

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird. Auf diese Weise kann die **D3DXVec3TransformCoord-Funktion** als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec3Transform**](d3dxvec3transform.md)
</dt> <dt>

[**D3DXVec3TransformNormal**](d3dxvec3transformnormal.md)
</dt> </dl>

 

 




