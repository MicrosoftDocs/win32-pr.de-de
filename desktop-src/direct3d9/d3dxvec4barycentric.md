---
description: 'D3DXVec4BaryCentric-Funktion (D3dx9math.h): Gibt unter Verwendung der angegebenen 4D-Vektoren einen Punkt in barycentric-Koordinaten zurück.'
ms.assetid: 80d73232-76bf-4f40-add2-dd1bdcc5cd98
title: D3DXVec4BaryCentric-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4BaryCentric
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 28c8ffc80b908f1ea894a22581c72e4371f87e5f55def2bdb9a1a66cc255ba90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118297639"
---
# <a name="d3dxvec4barycentric-function-d3dx9mathh"></a>D3DXVec4BaryCentric-Funktion (D3dx9math.h)

Gibt unter Verwendung der angegebenen 4D-Vektoren einen Punkt in Barycentric-Koordinaten zurück.

## <a name="syntax"></a>Syntax


```C++
D3DXVECTOR4* D3DXVec4BaryCentric(
  _Out_       D3DXVECTOR4 *pOut,
  _In_  const D3DXVECTOR4 *pV1,
  _In_  const D3DXVECTOR4 *pV2,
  _In_  const D3DXVECTOR4 *pV3,
  _In_        FLOAT       f,
  _In_        FLOAT       g
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Zeiger auf die [**D3DXVECTOR4-Struktur,**](d3dxvector4.md) die das Ergebnis des Vorgangs ist.

</dd> <dt>

*pV1* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Zeiger auf eine [**D3DXVECTOR4-Quellstruktur.**](d3dxvector4.md)

</dd> <dt>

*pV2* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Zeiger auf eine [**D3DXVECTOR4-Quellstruktur.**](d3dxvector4.md)

</dd> <dt>

*pV3* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Zeiger auf eine [**D3DXVECTOR4-Quellstruktur.**](d3dxvector4.md)

</dd> <dt>

*f* \[ in\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Gewichtungsfaktor. Siehe Hinweise.

</dd> <dt>

*g* \[ in\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Gewichtungsfaktor. Siehe Hinweise.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Zeiger auf eine [**D3DXVECTOR4-Struktur**](d3dxvector4.md) in baryzentrischen Koordinaten.

## <a name="remarks"></a>Hinweise

Die **D3DXVec4BaryCentric-Funktion** bietet eine Möglichkeit, Punkte in und um ein Dreieck zu verstehen, unabhängig davon, wo sich das Dreieck tatsächlich befindet. Diese Funktion gibt den resultierenden Punkt mithilfe der folgenden Gleichung zurück: V1 + f(V2-V1) + g(V3-V1).

Jeder Punkt in der Ebene V1V2V3 kann durch die Barycentric-Koordinate (f,g) dargestellt werden. Der Parameter *f* steuert, wie viel V2 in das Ergebnis gewichtet wird, und der Parameter *g* steuert, wie viel V3 in das Ergebnis gewichtet wird. Schließlich steuert 1-f-g, wie viel V1 in das Ergebnis gewichtet wird.

Beachten Sie die folgenden Beziehungen.

-   Wenn (f>=0 &, & g>=0 &, & 1-f-g>=0), befindet sich der Punkt innerhalb des Dreiecks V1V2V3.
-   Wenn (f==0 &, & g>=0 &, & 1-f-g>=0), befindet sich der Punkt in der Zeile V1V3.
-   Wenn (f>=0 &, & g==0 &, & 1-f-g>=0), befindet sich der Punkt in der Zeile V1V2.
-   Wenn (f>=0 &, & g>=0 &, & 1-f-g==0), befindet sich der Punkt in der Zeile V2V3.

Barycentric-Koordinaten sind eine Form allgemeiner Koordinaten. In diesem Kontext stellt die Verwendung von Barycentric-Koordinaten eine Änderung der Koordinatensysteme dar. Was für kartesische Koordinaten gilt, gilt für baryzentrische Koordinaten.

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird. Auf diese Weise kann die **D3DXVec4BaryCentric-Funktion** als Parameter für eine andere Funktion verwendet werden.

Barycentric-Koordinaten definieren einen Punkt innerhalb eines Dreiecks in Bezug auf die Scheitelpunkte des Dreiecks. Eine ausführlichere Beschreibung der baryzentrischen Koordinaten finden Sie unter [Mathworld es Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
