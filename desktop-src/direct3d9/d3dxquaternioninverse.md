---
description: 'D3DXQuaternionInverse-Funktion (D3dx9math.h): Konjugiert und normalisiert eine Quaternion.'
ms.assetid: 25407a60-f7c0-4063-8d1d-2d6d03bdb217
title: D3DXQuaternionInverse-Funktion (D3dx9math.h)
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
ms.openlocfilehash: 6ebb2520efa3c7c78d98fd8b90ec1ba9615e9927
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094068"
---
# <a name="d3dxquaternioninverse-function-d3dx9mathh"></a>D3DXQuaternionInverse-Funktion (D3dx9math.h)

Konjugiert und renormalisiert eine Quaternion.

## <a name="syntax"></a>Syntax


```C++
D3DXQUATERNION* D3DXQuaternionInverse(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Zeiger auf die [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) die das Ergebnis des Vorgangs ist.

</dd> <dt>

*pQ* \[ In\]
</dt> <dd>

Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Zeiger auf die [**D3DXQUATERNION-Quellstruktur.**](d3dxquaternion.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Zeiger auf eine [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) die die umgekehrte Quaternion der Quaternion ist.

## <a name="remarks"></a>Bemerkungen


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird. Auf diese Weise kann die **D3DXQuaternionInverse-Funktion** als Parameter für eine andere Funktion verwendet werden.

Verwenden Sie [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für alle Quaternioneingaben, die noch nicht normalisiert sind.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXQuaternionConjugate**](d3dxquaternionconjugate.md)
</dt> <dt>

[**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md)
</dt> </dl>

 

 




