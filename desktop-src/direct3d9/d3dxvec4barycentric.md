---
description: Gibt unter Verwendung der angegebenen 4D-Vektoren einen Punkt in der unter-/ein-basierten Koordinaten zurück.
ms.assetid: 80d73232-76bf-4f40-add2-dd1bdcc5cd98
title: D3DXVec4BaryCentric-Funktion (D3dx9math. h)
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
ms.openlocfilehash: 75f0d068d1545f1b8b55dc3b976d3585e6f9bc88
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355017"
---
# <a name="d3dxvec4barycentric-function-d3dx9mathh"></a>D3DXVec4BaryCentric-Funktion (D3dx9math. h)

Gibt unter Verwendung der angegebenen 4D-Vektoren einen Punkt in der unter-/ein-basierten Koordinaten zurück.

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

*Pout* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Ein Zeiger auf die [**D3DXVECTOR4**](d3dxvector4.md) -Struktur, die das Ergebnis des Vorgangs ist.

</dd> <dt>

*pV1* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***

Zeiger auf eine Quell- [**D3DXVECTOR4**](d3dxvector4.md) -Struktur.

</dd> <dt>

*pV2* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***

Zeiger auf eine Quell- [**D3DXVECTOR4**](d3dxvector4.md) -Struktur.

</dd> <dt>

*pV3* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***

Zeiger auf eine Quell- [**D3DXVECTOR4**](d3dxvector4.md) -Struktur.

</dd> <dt>

*f* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Gewichtungsfaktor. Siehe Hinweise.

</dd> <dt>

*g* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Gewichtungsfaktor. Siehe Hinweise.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Zeiger auf eine [**D3DXVECTOR4**](d3dxvector4.md) -Struktur in den baryzentrierten Koordinaten.

## <a name="remarks"></a>Bemerkungen

Die **D3DXVec4BaryCentric** -Funktion bietet eine Möglichkeit, Punkte in und um ein Dreieck zu verstehen, unabhängig davon, wo sich das Dreieck tatsächlich befindet. Diese Funktion gibt den resultierenden Punkt mithilfe der folgenden Gleichung zurück: v1 + f (V2-V1) + g (v3-v1).

Jeder Punkt in der Ebene V1V2V3 kann durch die baryzentrische Koordinate (f, g) dargestellt werden. Mit dem Parameter *f* wird gesteuert, wie viel v2 in das Ergebnis gewichtet wird, und der Parameter *g* steuert, wie viel v3 in das Ergebnis gewichtet wird. Schließlich steuert 1-f-g, wie viel V1 in das Ergebnis gewichtet wird.

Beachten Sie die folgenden Beziehungen.

-   Wenn (f>= 0 &, & g>= 0 &, & 1-f-g>= 0), befindet sich der Punkt innerhalb des Dreiecks V1V2V3.
-   Wenn (f = = 0 &, & g>= 0 &, & 1-f-g>= 0), befindet sich der Punkt in der Zeile V1V3.
-   Wenn (f>= 0 &, & g = = 0 &, & 1-f-g>= 0), befindet sich der Punkt in der Zeile v1v2.
-   Wenn (f>= 0 &, & g>= 0 &, & 1-f-g = = 0), befindet sich der Punkt in der Zeile V2V3.

Baryzentrierte Koordinaten sind eine Form allgemeiner Koordinaten. In diesem Kontext stellt die Verwendung von barzentrischen Koordinaten eine Änderung in Koordinatensystemen dar. Was für kartesische Koordinaten true ist, ist für barzentrierte Koordinaten "true".

Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXVec4BaryCentric** -Funktion als Parameter für eine andere Funktion verwendet werden.

In den Scheitel Punkten des Dreiecks wird ein Punkt innerhalb eines Dreiecks definiert. Eine ausführlichere Beschreibung von baryzentrischen Koordinaten finden Sie in [der Beschreibung von mathworld in der Beschreibung der baryzentrierten Koordinaten](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
