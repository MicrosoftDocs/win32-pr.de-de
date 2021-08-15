---
description: Skaliert einen Farbwert.
ms.assetid: 35e8adee-7ce5-4db5-8276-f0e408748e78
title: D3DXColorScale-Funktion (D3dx9math.h)
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
ms.openlocfilehash: 95ae2ea24547f566a6da014f408dbfbce5be3112a61688f69e125e91d6085493
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119241420"
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

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Zeiger auf eine [**D3DXCOLOR-Struktur,**](d3dxcolor.md) die das Ergebnis des Vorgangs ist.

</dd> <dt>

*pC* \[ In\]
</dt> <dd>

Typ: **const [**D3DXCOLOR**](d3dxcolor.md) \***

Zeiger auf eine [**D3DXCOLOR-Quellstruktur.**](d3dxcolor.md)

</dd> <dt>

*s* \[ in\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Skalierungsfaktor. Sie skaliert die Farbe und behandelt sie wie einen 4D-Vektor. Es gibt keine Grenzwerte für den Wert von s. Wenn s 1 ist, ist die resultierende Farbe die ursprüngliche Farbe.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Diese Funktion gibt einen Zeiger auf eine [**D3DXCOLOR-Struktur**](d3dxcolor.md) zurück, bei der es sich um den skalierten Farbwert handelt.

## <a name="remarks"></a>Hinweise

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXColorScale-Funktion** als Parameter für eine andere Funktion verwendet werden.

Diese Funktion berechnet den skalierten Farbwert, indem die Farbkomponenten der [**D3DXCOLOR-Struktur**](d3dxcolor.md) mit dem angegebenen Skalierungsfaktor multipliziert werden, wie im folgenden Beispiel gezeigt.


```
pOut->r = pC->r * s;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXColorLerp**](d3dxcolorlerp.md)
</dt> <dt>

[**D3DXColorModulate**](d3dxcolormodulate.md)
</dt> <dt>

[**D3DXColorNegative**](d3dxcolornegative.md)
</dt> </dl>

 

 
