---
description: Multipliziert zwei Quaternionen.
ms.assetid: f549e383-9c39-47a9-84e4-82365bdf1155
title: D3DXQuaternionMultiply-Funktion (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 74e10117bf27d922480418e5aa0b8ea60a13528c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353756"
---
# <a name="d3dxquaternionmultiply-function-d3dx10mathh"></a>D3DXQuaternionMultiply-Funktion (D3DX10Math. h)

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

Typ: **[ **D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***

Zeiger auf das [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , das das Ergebnis des Vorgangs ist.

</dd> <dt>

*pQ1* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) \***

Zeiger auf eine Quell- [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) -Struktur.

</dd> <dt>

*pQ2* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) \***

Zeiger auf eine Quell- [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Zeiger auf eine [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) -Struktur, die das Produkt aus zwei Quaternionen ist.

## <a name="remarks"></a>Bemerkungen

Das Ergebnis stellt die Drehung Q1, gefolgt von der Drehung Q2 (out = Q2 \* Q1) dar. Dies geschieht, damit **D3DXQuaternionMultiply** dieselbe Semantik wie [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) beibehält, da Einheiten Quaternionen als eine andere Möglichkeit zur Darstellung von Rotations Matrizen angesehen werden können.

Transformationen werden in derselben Reihenfolge für die **D3DXQuaternionMultiply** -Funktion und die [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) -Funktion verkettet. Wenn z. b. MX und My die gleichen Drehungen wie QX und qY darstellen, stellen sowohl m als auch q die gleichen Drehungen dar.


```
D3DXMatrixMultiply(&m, &mX, &mY);
D3DXQuaternionMultiply(&q, &qX, &qY);
```



Die Multiplikation von Quaternionen ist nicht kommutativ.

Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXQuaternionMultiply** -Funktion als Parameter für eine andere Funktion verwendet werden.

Verwenden Sie [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) für eine beliebige Quaternion-Eingabe, die nicht bereits normalisiert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
