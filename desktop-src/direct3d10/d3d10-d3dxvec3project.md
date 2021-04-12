---
description: Projiziert einen 3D-Vektor aus dem Objekt Raum in den Bildschirmbereich.
ms.assetid: 6fc59788-c3f7-4f47-a345-9108105e820e
title: D3DXVec3Project-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Project
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: c8d86949f754afb7639a0c28ff6d8b14c0e40ff0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354976"
---
# <a name="d3dxvec3project-function-d3dx10mathh"></a>D3DXVec3Project-Funktion (D3DX10Math. h)

Projiziert einen 3D-Vektor aus dem Objekt Raum in den Bildschirmbereich.

## <a name="syntax"></a>Syntax


```C++
D3DXVECTOR3* D3DXVec3Project(
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

Zeiger auf eine D3DXVECTOR3-Struktur, bei der es sich um den Vektor handelt, der vom Objekt Raum zum Bildschirmbereich projiziert

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird. Auf diese Weise kann die D3DXVec3Project-Funktion als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
