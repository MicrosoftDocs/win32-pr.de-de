---
description: Multipliziert zwei Quaternionen.
ms.assetid: 11072fc9-dae8-4f63-b07d-b709eed381df
title: D3DXQuaternionMultiply-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionMultiply
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 753fd206e2b970182ed44c216f1339d56973c416
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132381"
---
# <a name="d3dxquaternionmultiply-function-d3dx9mathh"></a>D3DXQuaternionMultiply-Funktion (D3dx9math. h)

Multipliziert zwei Quaternionen.

## <a name="syntax"></a>Syntax


```C++
D3DXQUATERNION* D3DXQuaternionMultiply(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pout* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Ein Zeiger auf die [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur, die das Ergebnis des Vorgangs ist.

</dd> <dt>

*pQ1* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***

Zeiger auf eine Quell- [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur.

</dd> <dt>

*pQ2* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***

Zeiger auf eine Quell- [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Zeiger auf eine [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur, die das Produkt aus zwei Quaternionen ist.

## <a name="remarks"></a>Bemerkungen

Das Ergebnis stellt die Drehung Q1, gefolgt von der Drehung Q2 (out = Q2 \* Q1) dar. Dies geschieht, damit **D3DXQuaternionMultiply** dieselbe Semantik wie [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) beibehält, da Einheiten Quaternionen als eine andere Möglichkeit zur Darstellung von Rotations Matrizen angesehen werden können.

Transformationen werden in derselben Reihenfolge für die **D3DXQuaternionMultiply** -Funktion und die [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) -Funktion verkettet. Wenn z. b. MX und My die gleichen Drehungen wie QX und qY darstellen, stellen sowohl m als auch q die gleichen Drehungen dar.


```
D3DXMatrixMultiply(&m, &mX, &mY);
D3DXQuaternionMultiply(&q, &qX, &qY);
```



Die Multiplikation von Quaternionen ist nicht kommutativ.

Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXQuaternionMultiply** -Funktion als Parameter für eine andere Funktion verwendet werden.

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

[**D3DXMatrixMultiply**](d3dxmatrixmultiply.md)
</dt> </dl>

 

 




