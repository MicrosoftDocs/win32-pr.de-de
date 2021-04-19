---
description: Transformiert ein Array (x, y, 0, 0) durch eine angegebene Matrix.
ms.assetid: 9f5d8fdc-f3e1-41dc-be4e-9ffc6be1947f
title: D3DXVec2TransformNormalArray-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformNormalArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0aece37f9bebb46bab8a0d2a1c27bf19e0c2b0bd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364381"
---
# <a name="d3dxvec2transformnormalarray-function-d3dx9mathh"></a>D3DXVec2TransformNormalArray-Funktion (D3dx9math. h)

Transformiert ein Array (x, y, 0, 0) durch eine angegebene Matrix.

## <a name="syntax"></a>Syntax


```C++
D3DXVECTOR2* D3DXVec2TransformNormalArray(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR2 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pout* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Ein Zeiger auf die [**D3DXVECTOR2**](d3dxvector2.md) -Struktur, die das Ergebnis des Vorgangs ist.

</dd> <dt>

*Outstride* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Schritt zwischen Vektoren im Ausgabedatenstrom.

</dd> <dt>

*PV* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR2**](d3dxvector2.md) \***

Zeiger auf das Quell- [**D3DXVECTOR2**](d3dxvector2.md) Array.

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

Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Zeiger auf eine [**D3DXVECTOR2**](d3dxvector2.md) -Struktur, die das transformierte Array ist.

## <a name="remarks"></a>Bemerkungen

Diese Funktion transformiert den Vektor (*PV-*>x, *PV-*>y, 0, 0) durch die Matrix, auf die von pm gezeigt wird *.*

Wenn Sie eine normale Transformation durchführen möchten, sollte die Matrix, die Sie an diese Funktion übergeben, die Umwandlung der Umkehrung der Matrix sein, die zum Transformieren eines Punkts verwendet werden soll.

Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXVec2TransformNormalArray** -Funktion als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
