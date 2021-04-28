---
description: 'D3DXVec3Unproject-Funktion (D3DX10Math.h): Projiziert einen Vektor aus dem Bildschirmbereich in den Objektraum.'
ms.assetid: c96d732d-0594-42b4-bc54-458a313f153e
title: D3DXVec3Unproject-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Unproject
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 08d38691d0e780e49293149bdb7a08b1ea0ef1fb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103028"
---
# <a name="d3dxvec3unproject-function-d3dx10mathh"></a>D3DXVec3Unproject-Funktion (D3DX10Math.h)

Projektiert einen Vektor aus dem Bildschirmbereich in den Objektraum.

## <a name="syntax"></a>Syntax


```C++
D3DXVECTOR3* D3DXVec3Unproject(
  _Inout_       D3DXVECTOR3    *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_    const D3D10_VIEWPORT *pViewport,
  _In_    const D3DXMATRIX     *pProjection,
  _In_    const D3DXMATRIX     *pView,
  _In_    const D3DXMATRIX     *pWorld
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

*pViewport* \[ In\]
</dt> <dd>

Typ: **const [**D3D10 \_ VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) \***

Zeiger auf einen [**D3D10 \_ VIEWPORT,**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)der den Viewport darstellt.

</dd> <dt>

*pProjection* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3d10-d3dxmatrix.md) die die Projektionsmatrix darstellt.

</dd> <dt>

*pView* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Zeiger auf eine D3DXMATRIX-Struktur, die die Ansichtsmatrix darstellt.

</dd> <dt>

*pWorld* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Zeiger auf eine D3DXMATRIX-Struktur, die die Weltmatrix darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Zeiger auf eine D3DXVECTOR3-Struktur, bei der es sich um den Vektor handelt, der vom Bildschirmbereich in den Objektbereich projiziert wird.

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann die D3DXVec3Unproject-Funktion als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Math.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
