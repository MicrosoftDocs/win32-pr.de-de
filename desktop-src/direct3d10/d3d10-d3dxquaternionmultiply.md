---
description: 'D3DXQuaternionMultiply-Funktion (D3DX10Math.h): Multipliziert zwei Quaternionen.'
ms.assetid: f549e383-9c39-47a9-84e4-82365bdf1155
title: D3DXQuaternionMultiply-Funktion (D3DX10Math.h)
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
ms.openlocfilehash: 4f84ecac1eb910f4b3c97aba6ed42691c70b5b1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103158"
---
# <a name="d3dxquaternionmultiply-function-d3dx10mathh"></a>D3DXQuaternionMultiply-Funktion (D3DX10Math.h)

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

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***

Zeiger auf das [**D3DXQUATERNION-Steuerelement,**](d3d10-d3dxquaternion.md) das das Ergebnis des Vorgangs ist.

</dd> <dt>

*pQ1* \[ In\]
</dt> <dd>

Typ: **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) \***

Zeiger auf eine [**D3DXQUATERNION-Quellstruktur.**](d3d10-d3dxquaternion.md)

</dd> <dt>

*pQ2* \[ In\]
</dt> <dd>

Typ: **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) \***

Zeiger auf eine [**D3DXQUATERNION-Quellstruktur.**](d3d10-d3dxquaternion.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Zeiger auf eine [**D3DXQUATERNION-Struktur,**](d3d10-d3dxquaternion.md) die das Produkt von zwei Quaternionen ist.

## <a name="remarks"></a>Bemerkungen

Das Ergebnis stellt die Drehung Q1 gefolgt von der Drehung Q2 (Out = Q2 \* Q1) dar. Dies erfolgt so, dass **D3DXQuaternionMultiply** dieselbe Semantik wie [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) beibekommen, da Einheitenquaternionen als eine andere Möglichkeit zur Darstellung von Rotationsmatrizen betrachtet werden können.

Transformationen werden für die **Funktionen D3DXQuaternionMultiply** und [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) in der gleichen Reihenfolge verkettet. Angenommen, mX und mY stellen die gleichen Drehungen wie qX und qY dar, stellen sowohl m als auch q die gleichen Drehungen dar.


```
D3DXMatrixMultiply(&m, &mX, &mY);
D3DXQuaternionMultiply(&q, &qX, &qY);
```



Die Multiplikation von Quaternionen ist nicht kommutativ.

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXQuaternionMultiply-Funktion** als Parameter für eine andere Funktion verwendet werden.

Verwenden Sie [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) für alle Quaternioneingaben, die nicht bereits normalisiert sind.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
