---
description: Projiziert ein Array (x, y, z, 0) aus dem Objekt Raum in den Bildschirmbereich.
ms.assetid: cf022741-0bae-4c22-872f-bd94c3721aff
title: D3DXVec3ProjectArray-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3ProjectArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f802d8ab564f2cbfe1cc60ad6aed13959bef9383
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354412"
---
# <a name="d3dxvec3projectarray-function-d3dx9mathh"></a>D3DXVec3ProjectArray-Funktion (D3dx9math. h)

Projiziert ein Array (x, y, z, 0) aus dem Objekt Raum in den Bildschirmbereich.

## <a name="syntax"></a>Syntax


```C++
D3DXVECTOR3* D3DXVec3ProjectArray(
  _Inout_       D3DXVECTOR3  *pOut,
  _In_          UINT         OutStride,
  _In_    const D3DXVECTOR3  *pV,
  _In_          UINT         VStride,
  _In_    const D3DVIEWPORT9 *pViewport,
  _In_    const D3DXMATRIX   *pProjection,
  _In_    const D3DXMATRIX   *pView,
  _In_    const D3DXMATRIX   *pWorld,
  _In_          UINT         n
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pout* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Ein Zeiger auf die [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die das Ergebnis des Vorgangs ist.

</dd> <dt>

*Outstride* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Schritt zwischen Vektoren im Ausgabedatenstrom.

</dd> <dt>

*PV* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Ein Zeiger auf die Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur.

</dd> <dt>

*Vstride* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Schritt zwischen Vektoren im Eingabedaten Strom.

</dd> <dt>

*pviewport* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DVIEWPORT9**](d3dviewport9.md) \***

Zeiger auf eine [**D3DVIEWPORT9**](d3dviewport9.md) -Struktur, die den Viewport darstellt.

</dd> <dt>

*pprojection* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***

Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die die Projektions Matrix darstellt.

</dd> <dt>

*PView* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***

Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die die Ansichts Matrix darstellt.

</dd> <dt>

*pworld* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***

Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die die Weltmatrix darstellt.

</dd> <dt>

*n* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der Elemente im Array.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, bei der es sich um das Array handelt, das vom Objekt Raum auf den Bildschirmbereich

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXVec3ProjectArray** -Funktion als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec3Unproject**](d3dxvec3unproject.md)
</dt> </dl>

 

 
