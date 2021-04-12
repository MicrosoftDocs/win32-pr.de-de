---
description: Gibt unter Verwendung der angegebenen 2D-Vektoren einen Punkt in der unter-/codezentrierten Koordinaten zurück.
ms.assetid: 8eceb2c0-26a0-4a7f-9830-85327dcb31ab
title: D3DXVec2BaryCentric-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2BaryCentric
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 270371fdda42b59cb755f1e0dc7e0fa43a863a1d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355567"
---
# <a name="d3dxvec2barycentric-function-d3dx10mathh"></a>D3DXVec2BaryCentric-Funktion (D3DX10Math. h)

Gibt unter Verwendung der angegebenen 2D-Vektoren einen Punkt in der unter-/codezentrierten Koordinaten zurück.

## <a name="syntax"></a>Syntax


```C++
D3DXVECTOR2* D3DXVec2BaryCentric(
  _In_       D3DXVECTOR2 *pOut,
  _In_ const D3DXVECTOR2 *pV1,
  _In_ const D3DXVECTOR2 *pV2,
  _In_ const D3DXVECTOR2 *pV3,
  _In_       FLOAT       f,
  _In_       FLOAT       g
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pout* \[ in\]
</dt> <dd>

Typ: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

Zeiger auf das [**D3DXVECTOR2**](d3d10-d3dxvector2.md) , das das Ergebnis des Vorgangs ist.

</dd> <dt>

*pV1* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Zeiger auf eine Quell-D3DXVECTOR2-Struktur.

</dd> <dt>

*pV2* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Zeiger auf eine Quell-D3DXVECTOR2-Struktur.

</dd> <dt>

*pV3* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Zeiger auf eine Quell-D3DXVECTOR2-Struktur.

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

Typ: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

Zeiger auf eine D3DXVECTOR2-Struktur in den baryzentrierten Koordinaten.

## <a name="remarks"></a>Bemerkungen

Die D3DXVec2BaryCentric-Funktion bietet eine Möglichkeit, Punkte in und um ein Dreieck zu verstehen, unabhängig davon, wo sich das Dreieck tatsächlich befindet. Diese Funktion gibt den resultierenden Punkt mithilfe der folgenden Gleichung zurück: v1 + f (V2-V1) + g (v3-v1).

Jeder Punkt in der Ebene V1V2V3 kann durch die baryzentrische Koordinate (f, g) dargestellt werden. Der Parameter f steuert, wie viel v2 in das Ergebnis gewichtet wird, und der Parameter g steuert, wie viel v3 in das Ergebnis gewichtet wird. Schließlich steuert 1-f-g, wie viel V1 in das Ergebnis gewichtet wird.

Beachten Sie die folgenden Beziehungen.

-   Wenn (f>= 0 &, & g>= 0 &, & 1-f-g>= 0), befindet sich der Punkt innerhalb des Dreiecks V1V2V3.
-   Wenn (f = = 0 &, & g>= 0 &, & 1-f-g>= 0), befindet sich der Punkt in der Zeile V1V3.
-   Wenn (f>= 0 &, & g = = 0 &, & 1-f-g>= 0), befindet sich der Punkt in der Zeile v1v2.
-   Wenn (f>= 0 &, & g>= 0 &, & 1-f-g = = 0), befindet sich der Punkt in der Zeile V2V3.

Baryzentrierte Koordinaten sind eine Form allgemeiner Koordinaten. In diesem Kontext stellt die Verwendung von barzentrischen Koordinaten eine Änderung in Koordinatensystemen dar. Was für kartesische Koordinaten true ist, ist für barzentrierte Koordinaten "true".

Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird. Auf diese Weise kann die D3DXVec2BaryCentric-Funktion als Parameter für eine andere Funktion verwendet werden.

In den Scheitel Punkten des Dreiecks wird ein Punkt innerhalb eines Dreiecks definiert. Eine ausführlichere Beschreibung von baryzentrischen Koordinaten finden Sie in [der Beschreibung von mathworld in der Beschreibung der baryzentrierten Koordinaten](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
