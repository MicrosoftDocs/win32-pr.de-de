---
description: 'D3DXVec3Unproject-Funktion (D3dx9math.h): Projiziert einen Vektor aus dem Bildschirmbereich in den Objektraum.'
ms.assetid: 9fd69cae-1d9c-4fae-9e15-8eb9950b4850
title: D3DXVec3Unproject-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Unproject
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2c3ea6ec1aa60f48589b10575e279bed81b2c94f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115558"
---
# <a name="d3dxvec3unproject-function-d3dx9mathh"></a>D3DXVec3Unproject-Funktion (D3dx9math.h)

Projektiert einen Vektor aus dem Bildschirmbereich in den Objektraum.

## <a name="syntax"></a>Syntax


```C++
D3DXVECTOR3* D3DXVec3Unproject(
  _Inout_       D3DXVECTOR3  *pOut,
  _In_    const D3DXVECTOR3  *pV,
  _In_    const D3DVIEWPORT9 *pViewport,
  _In_    const D3DXMATRIX   *pProjection,
  _In_    const D3DXMATRIX   *pView,
  _In_    const D3DXMATRIX   *pWorld
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

*pViewport* \[ In\]
</dt> <dd>

Typ: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***

Zeiger auf eine [**D3DVIEWPORT9-Struktur,**](d3dviewport9.md) die den Viewport darstellt.

</dd> <dt>

*pProjection* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die die Projektionsmatrix darstellt.

</dd> <dt>

*pView* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die die Ansichtsmatrix darstellt.

</dd> <dt>

*pWorld* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die die Weltmatrix darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) bei der es sich um den Vektor handelt, der vom Bildschirmbereich in den Objektbereich projiziert wird.

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird. Auf diese Weise kann die **D3DXVec3Unproject-Funktion** als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec3Project**](d3dxvec3project.md)
</dt> </dl>

 

 




