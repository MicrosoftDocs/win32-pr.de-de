---
description: Konjugiert eine Quaternion und benennt Sie um.
ms.assetid: 25407a60-f7c0-4063-8d1d-2d6d03bdb217
title: D3DXQuaternionInverse-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionInverse
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b2f830b7f8f797e4ed94eb22b4c2a05c3bd3e4cd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394217"
---
# <a name="d3dxquaternioninverse-function-d3dx9mathh"></a>D3DXQuaternionInverse-Funktion (D3dx9math. h)

Konjugiert eine Quaternion und benennt Sie um.

## <a name="syntax"></a>Syntax


```C++
D3DXQUATERNION* D3DXQuaternionInverse(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pout* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Ein Zeiger auf die [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur, die das Ergebnis des Vorgangs ist.

</dd> <dt>

*PQ* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***

Ein Zeiger auf die Quell- [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Zeiger auf eine [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur, die die umgekehrte Quaternion der Quaternion ist.

## <a name="remarks"></a>Bemerkungen


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXQuaternionInverse** -Funktion als Parameter für eine andere Funktion verwendet werden.

Verwenden Sie [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für eine beliebige Quaternion-Eingabe, die nicht bereits normalisiert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXQuaternionConjugate**](d3dxquaternionconjugate.md)
</dt> <dt>

[**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md)
</dt> </dl>

 

 




