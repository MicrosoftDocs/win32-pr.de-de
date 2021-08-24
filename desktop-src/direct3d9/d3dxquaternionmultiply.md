---
description: 'D3DXQuaternionMultiply-Funktion (D3dx9math.h): Multipliziert zwei Quaternionen.'
ms.assetid: 11072fc9-dae8-4f63-b07d-b709eed381df
title: D3DXQuaternionMultiply-Funktion (D3dx9math.h)
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
ms.openlocfilehash: e4fe5c7f6d95bef19ce77e7ea7815e6808eae63e7643bbfc40e6b0fa1bb45767
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750070"
---
# <a name="d3dxquaternionmultiply-function-d3dx9mathh"></a>D3DXQuaternionMultiply-Funktion (D3dx9math.h)

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

Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Zeiger auf die [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) die das Ergebnis des Vorgangs ist.

</dd> <dt>

*pQ1* \[ In\]
</dt> <dd>

Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Zeiger auf eine [**D3DXQUATERNION-Quellstruktur.**](d3dxquaternion.md)

</dd> <dt>

*pQ2* \[ In\]
</dt> <dd>

Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Zeiger auf eine [**D3DXQUATERNION-Quellstruktur.**](d3dxquaternion.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Zeiger auf eine [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) die das Produkt zweier Quaternionen ist.

## <a name="remarks"></a>Hinweise

Das Ergebnis stellt die Drehung Q1 gefolgt von der Drehung Q2 (Out = Q2 \* Q1) dar. Dies erfolgt so, dass **D3DXQuaternionMultiply** die gleiche Semantik wie [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) beibekommen, da Einheitenquaternionen als eine andere Möglichkeit zur Darstellung von Rotationsmatrizen betrachtet werden können.

Transformationen werden für die **Funktionen D3DXQuaternionMultiply** und [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) in derselben Reihenfolge verkettet. Angenommen, mX und mY stellen die gleichen Drehungen wie qX und qY dar, stellen sowohl m als auch q die gleichen Drehungen dar.


```
D3DXMatrixMultiply(&m, &mX, &mY);
D3DXQuaternionMultiply(&q, &qX, &qY);
```



Die Multiplikation von Quaternionen ist nicht kommutativ.

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird. Auf diese Weise kann die **D3DXQuaternionMultiply-Funktion** als Parameter für eine andere Funktion verwendet werden.

Verwenden [**Sie D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für alle Quaternioneingaben, die noch nicht normalisiert sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixMultiply**](d3dxmatrixmultiply.md)
</dt> </dl>

 

 




