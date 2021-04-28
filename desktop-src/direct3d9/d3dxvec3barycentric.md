---
description: 'D3DXVec3BaryCentric-Funktion (D3dx9math.h): Gibt unter Verwendung der angegebenen 3D-Vektoren einen Punkt in baryzentrierten Koordinaten zurück.'
ms.assetid: ecbabc76-9936-4f31-adec-1ec807984787
title: D3DXVec3BaryCentric-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3BaryCentric
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c966eeabe78deabefb2877405f649f3d162f9d73
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097894"
---
# <a name="d3dxvec3barycentric-function-d3dx9mathh"></a>D3DXVec3BaryCentric-Funktion (D3dx9math.h)

Gibt unter Verwendung der angegebenen 3D-Vektoren einen Punkt in baryzentrierten Koordinaten zurück.

## <a name="syntax"></a>Syntax


```C++
D3DXVECTOR3* D3DXVec3BaryCentric(
  _Out_       D3DXVECTOR3 *pOut,
  _In_  const D3DXVECTOR3 *pV1,
  _In_  const D3DXVECTOR3 *pV2,
  _In_  const D3DXVECTOR3 *pV3,
  _In_        FLOAT       f,
  _In_        FLOAT       g
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Zeiger auf die [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die das Ergebnis des Vorgangs ist.

</dd> <dt>

*pV1* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Quellstruktur.**](d3dxvector3.md)

</dd> <dt>

*pV2* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Quellstruktur.**](d3dxvector3.md)

</dd> <dt>

*pV3* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Quellstruktur.**](d3dxvector3.md)

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

Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Zeiger auf eine [**D3DXVECTOR3-Struktur**](d3dxvector3.md) in baryzentrischen Koordinaten.

## <a name="remarks"></a>Bemerkungen

Die **D3DXVec3BaryCentric-Funktion** bietet eine Möglichkeit, Punkte in und um ein Dreieck zu verstehen, unabhängig davon, wo sich das Dreieck tatsächlich befindet. Diese Funktion gibt den resultierenden Punkt mithilfe der folgenden Gleichung zurück: V1 + f(V2-V1) + g(V3-V1).

Jeder Punkt in der Ebene V1V2V3 kann durch die Barycentric-Koordinate (f,g) dargestellt werden. Der Parameter *f* steuert, wie viel V2 in das Ergebnis gewichtet wird, und der Parameter *g* steuert, wie viel V3 in das Ergebnis gewichtet wird. Schließlich steuert 1-f-g, wie viel V1 in das Ergebnis gewichtet wird.

Beachten Sie die folgenden Beziehungen.

-   Wenn (f>=0 &, & g>=0 &, & 1-f-g>=0), befindet sich der Punkt innerhalb des Dreiecks V1V2V3.
-   Wenn (f==0 &, & g>=0 &, & 1-f-g>=0), befindet sich der Punkt in der Zeile V1V3.
-   Wenn (f>=0 &, & g==0 &, & 1-f-g>=0), befindet sich der Punkt in der Zeile V1V2.
-   Wenn (f>=0 &, & g>=0 &, & 1-f-g==0), befindet sich der Punkt in der Zeile V2V3.

Barycentric-Koordinaten sind eine Form allgemeiner Koordinaten. In diesem Kontext stellt die Verwendung von Barycentric-Koordinaten eine Änderung der Koordinatensysteme dar. Was für kartesische Koordinaten gilt, gilt für baryzentrische Koordinaten.

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird. Auf diese Weise kann die **D3DXVec3BaryCentric-Funktion** als Parameter für eine andere Funktion verwendet werden.

Barycentric-Koordinaten definieren einen Punkt innerhalb eines Dreiecks in Bezug auf die Scheitelpunkte des Dreiecks. Eine ausführlichere Beschreibung der baryzentrischen Koordinaten finden Sie unter [Mathworld es Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
