---
description: Projiziert einen Vektor aus dem Bildschirmbereich in den Objektbereich.
ms.assetid: c96d732d-0594-42b4-bc54-458a313f153e
title: D3DXVec3Unproject-Funktion (D3DX10Math. h)
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
ms.openlocfilehash: 21916392c689bcac794d44ec2c42c3e0b39abb0c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366657"
---
# <a name="d3dxvec3unproject-function-d3dx10mathh"></a>D3DXVec3Unproject-Funktion (D3DX10Math. h)

Projiziert einen Vektor aus dem Bildschirmbereich in den Objektbereich.

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

*Pout* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Zeiger auf das [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , das das Ergebnis des Vorgangs ist.

</dd> <dt>

*PV* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Ein Zeiger auf die Quell-D3DXVECTOR3-Struktur.

</dd> <dt>

*pviewport* \[ in\]
</dt> <dd>

Typ: **Konstanten [**d3d10 \_ Viewport**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) \***

Zeiger auf einen [**d3d10 \_ Viewport**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), der den Viewport darstellt.

</dd> <dt>

*pprojection* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Zeiger auf eine [**D3DXMATRIX**](d3d10-d3dxmatrix.md) -Struktur, die die Projektions Matrix darstellt.

</dd> <dt>

*PView* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Zeiger auf eine D3DXMATRIX-Struktur, die die Ansichts Matrix darstellt.

</dd> <dt>

*pworld* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Zeiger auf eine D3DXMATRIX-Struktur, die die Weltmatrix darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Zeiger auf eine D3DXVECTOR3-Struktur, bei der es sich um den Vektor handelt, der vom Bildschirmbereich zum Objekt Raum projiziert

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird. Auf diese Weise kann die D3DXVec3Unproject-Funktion als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
