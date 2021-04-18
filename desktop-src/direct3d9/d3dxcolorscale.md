---
description: Skaliert einen Farbwert.
ms.assetid: 35e8adee-7ce5-4db5-8276-f0e408748e78
title: D3DXColorScale-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorScale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 74020f302a26162df1e42cb4c9f020af3f64e59c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351968"
---
# <a name="d3dxcolorscale-function"></a>D3DXColorScale-Funktion

Skaliert einen Farbwert.

## <a name="syntax"></a>Syntax


```C++
D3DXCOLOR* D3DXColorScale(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pout* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Zeiger auf eine [**D3DXCOLOR**](d3dxcolor.md) -Struktur, die das Ergebnis des Vorgangs ist.

</dd> <dt>

*PC* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXCOLOR**](d3dxcolor.md) \***

Zeiger auf eine Quell- [**D3DXCOLOR**](d3dxcolor.md) -Struktur.

</dd> <dt>

*s* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Skalierungsfaktor. Die Farbe wird skaliert und wie ein 4D-Vektor behandelt. Es gibt keine Einschränkungen für den Wert von s. Wenn s den Wert 1 hat, ist die resultierende Farbe die ursprüngliche Farbe.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Diese Funktion gibt einen Zeiger auf eine [**D3DXCOLOR**](d3dxcolor.md) -Struktur zurück, die der skalierte Farbwert ist.

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXColorScale** -Funktion als Parameter für eine andere Funktion verwendet werden.

Diese Funktion berechnet den skalierten Farbwert, indem die Farbkomponenten der [**D3DXCOLOR**](d3dxcolor.md) -Struktur mit dem angegebenen Skalierungsfaktor multipliziert werden, wie im folgenden Beispiel gezeigt.


```
pOut->r = pC->r * s;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXColorLerp**](d3dxcolorlerp.md)
</dt> <dt>

[**D3DXColorModulate**](d3dxcolormodulate.md)
</dt> <dt>

[**D3DXColorNegative**](d3dxcolornegative.md)
</dt> </dl>

 

 
