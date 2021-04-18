---
description: Transformiert ein Array (x, y, 0, 1) durch eine angegebene Matrix.
ms.assetid: 11d69f65-2aef-46f4-b274-e173a11382a8
title: D3DXVec4TransformArray-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4TransformArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3102d1766ba43525829e045503c1838a19d4b0e6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354419"
---
# <a name="d3dxvec4transformarray-function-d3dx9mathh"></a>D3DXVec4TransformArray-Funktion (D3dx9math. h)

Transformiert ein Array (x, y, 0, 1) durch eine angegebene Matrix.

## <a name="syntax"></a>Syntax


```C++
D3DXVECTOR4* D3DXVec4TransformArray(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR4 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pout* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Zeiger auf das [**D3DXVECTOR4**](d3dxvector4.md) -Array, das das Ergebnis des Vorgangs ist.

</dd> <dt>

*Outstride* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Schritt zwischen Vektoren im Ausgabedatenstrom.

</dd> <dt>

*PV* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***

Zeiger auf das Quell- [**D3DXVECTOR4**](d3dxvector4.md) Array.

</dd> <dt>

*Vstride* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Schritt zwischen Vektoren im Eingabedaten Strom.

</dd> <dt>

*pm* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***

Ein Zeiger auf die Quell- [**D3DXMATRIX**](d3dxmatrix.md) -Struktur.

</dd> <dt>

*n* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der Elemente im Array.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Zeiger auf eine [**D3DXVECTOR4**](d3dxvector4.md) -Struktur, die das transformierte Array ist.

## <a name="remarks"></a>Bemerkungen

Diese Funktion wandelt das Array *PV* (x, y, 0, 1) durch die Matrix *pm* um.

Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXVec4TransformArray** -Funktion als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
