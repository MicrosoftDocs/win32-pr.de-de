---
description: Berechnet das übersetzte Produkt von zwei Matrizen.
ms.assetid: 43927500-9413-41a4-a6ee-974d85dd1054
title: D3DXMatrixMultiplyTranspose-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixMultiplyTranspose
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b599453ae108a5a8bab8ee896858760c85799948
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363119"
---
# <a name="d3dxmatrixmultiplytranspose-function-d3dx9mathh"></a>D3DXMatrixMultiplyTranspose-Funktion (D3dx9math. h)

Berechnet das übersetzte Produkt von zwei Matrizen.

## <a name="syntax"></a>Syntax


```C++
D3DXMATRIX* D3DXMatrixMultiplyTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pout* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.

</dd> <dt>

*pM1* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***

Zeiger auf eine Quell- [**D3DXMATRIX**](d3dxmatrix.md) -Struktur.

</dd> <dt>

*pM2* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***

Zeiger auf eine Quell- [**D3DXMATRIX**](d3dxmatrix.md) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die das Produkt von zwei Matrizen ist.

## <a name="remarks"></a>Bemerkungen

Das Ergebnis ist die Umsetzung des Produkts von zwei Transformations Matrizen: Out = T (M1 \* m2).

Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXMatrixMultiplyTranspose** -Funktion als Parameter für eine andere Funktion verwendet werden.

Diese Funktion ist nützlich, um Matrizen als Konstanten für Scheitelpunkt-und Pixel-Shader festzulegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixMultiply**](d3dxmatrixmultiply.md)
</dt> <dt>

[**D3DXQuaternionMultiply**](d3dxquaternionmultiply.md)
</dt> </dl>

 

 




