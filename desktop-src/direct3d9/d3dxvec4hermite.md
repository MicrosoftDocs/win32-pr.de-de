---
description: Führt eine aufgenommene Spline-interpolung mithilfe der angegebenen 4D-Vektoren aus.
ms.assetid: 687d4dcf-ee75-4dda-b6d2-5ba0b5281a64
title: D3DXVec4Hermite-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Hermite
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 85cf60150606a37c2e68ebf72bd4a3772d346660
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219551"
---
# <a name="d3dxvec4hermite-function-d3dx9mathh"></a>D3DXVec4Hermite-Funktion (D3dx9math. h)

Führt eine aufgenommene Spline-interpolung mithilfe der angegebenen 4D-Vektoren aus.

## <a name="syntax"></a>Syntax


```C++
D3DXVECTOR4* D3DXVec4Hermite(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pT1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pT2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pout* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Ein Zeiger auf die [**D3DXVECTOR4**](d3dxvector4.md) -Struktur, die das Ergebnis des Vorgangs ist.

</dd> <dt>

*pV1* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***

Zeiger auf eine Quell- [**D3DXVECTOR4**](d3dxvector4.md) -Struktur, ein Positions Vektor.

</dd> <dt>

*pT1* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***

Zeiger auf eine [**D3DXVECTOR4**](d3dxvector4.md) -Quell Struktur, ein Tangens Vektor.

</dd> <dt>

*pV2* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***

Zeiger auf eine Quell- [**D3DXVECTOR4**](d3dxvector4.md) -Struktur, ein Positions Vektor.

</dd> <dt>

*PT2* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***

Zeiger auf eine [**D3DXVECTOR4**](d3dxvector4.md) -Quell Struktur, ein Tangens Vektor.

</dd> <dt>

*s* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Gewichtungsfaktor. Siehe Hinweise.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Ein Zeiger auf eine [**D3DXVECTOR4**](d3dxvector4.md) -Struktur, die das Ergebnis der Hermite-Spline-interpolung ist.

## <a name="remarks"></a>Bemerkungen

Die **D3DXVec4Hermite** -Funktion interpoliert von (positiona, tangenta) bis (positionb, tangentb) mithilfe der herdie Spline-Interpolation.

Die Spline-interpolung ist eine Generalisierung der Easy-in-Easy-out-Spline. Die-Rampe ist eine Funktion von Q (s) mit den folgenden Eigenschaften.

Q (s) = As ³ + b ² + CS + D (und somit q ' (s) = 3AS ² + 2B + C)

a) q (0) = v1, also q ' (0) = T1

b) q (1) = v2, also q ' (1) = T2

v1 ist der Inhalt von pV1, v2 im Inhalt von pV2, T1 ist der Inhalt von pT1, und T2 ist der Inhalt von PT2.

Diese Eigenschaften werden verwendet, um für A, B, C, D zu lösen.

Binden Sie die Lösungen für A, B, C und D ein, um Q (s) zu generieren.

``` syntax
A = 2v1 - 2v2 + t2 + t1 
B = 3v2 - 3v1 - 2t1 - t2
C = t1 
D = v1
```

Dies ergibt:

Q (s) = (2v1-2v2 + T2 + T1) s ³ + (3v2-3v1-2t1-T2) s ² + T1S + v1

Diese können wie folgt neu angeordnet werden:

Q (s) = (2S ³-3S ² + 1) v1 + (-2S ³ + 3S ²) v2 + (s ³-2S ² + s) T1 + (s ³-s ²) T2

Hermite-Splines sind zum Steuern der Animation nützlich, da die Kurve alle Steuerungs Punkte durchläuft. Da die Position und der Tangens an den Enden der einzelnen Segmente explizit angegeben werden, ist es einfach, eine C2-kontinuierliche Kurve zu erstellen, solange Sie sicherstellen, dass die Anfangsposition und der Tangens mit den Endwerten des letzten Segments übereinstimmen.

Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXVec4Hermite** -Funktion als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
