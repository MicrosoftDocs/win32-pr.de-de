---
description: 'D3DXVec4Hermite-Funktion (D3dx9math.h): Führt eine Hermite-Splineinterpolation mithilfe der angegebenen 4D-Vektoren aus.'
ms.assetid: 687d4dcf-ee75-4dda-b6d2-5ba0b5281a64
title: D3DXVec4Hermite-Funktion (D3dx9math.h)
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
ms.openlocfilehash: a62d96181b4242073b9e6a2176d841add86cbfeab4238bfb4cbb538bfd88e1e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730728"
---
# <a name="d3dxvec4hermite-function-d3dx9mathh"></a>D3DXVec4Hermite-Funktion (D3dx9math.h)

Führt eine Hermite-Splineinterpolation mithilfe der angegebenen 4D-Vektoren aus.

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

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Zeiger auf die [**D3DXVECTOR4-Struktur,**](d3dxvector4.md) die das Ergebnis des Vorgangs ist.

</dd> <dt>

*pV1* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Zeiger auf eine [**D3DXVECTOR4-Quellstruktur,**](d3dxvector4.md) einen Positionsvektor.

</dd> <dt>

*pT1* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Zeiger auf eine [**D3DXVECTOR4-Quellstruktur,**](d3dxvector4.md) einen Tangensvektor.

</dd> <dt>

*pV2* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Zeiger auf eine [**D3DXVECTOR4-Quellstruktur,**](d3dxvector4.md) einen Positionsvektor.

</dd> <dt>

*pT2* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Zeiger auf eine [**D3DXVECTOR4-Quellstruktur,**](d3dxvector4.md) einen Tangensvektor.

</dd> <dt>

*s* \[ in\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Gewichtungsfaktor. Siehe Hinweise.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Zeiger auf eine [**D3DXVECTOR4-Struktur,**](d3dxvector4.md) die das Ergebnis der Hermite-Splineinterpolation ist.

## <a name="remarks"></a>Hinweise

Die **D3DXVec4Hermite-Funktion** interpoliert mithilfe der Hermite-Splineinterpolation von (positionA, tangentA) in (positionB, tangentB).

Die Splineinterpolation ist eine Generalisierung der einfachen, einfachen Spline. Die Rampe ist eine Funktion von Q(s) mit den folgenden Eigenschaften.

Q(s) = As( + Bs) + Cs + D (und daher Q'(s) = 3As× + 2Bs + C)

a) Q(0) = v1, also Q'(0) = t1

b) Q(1) = v2, also Q'(1) = t2

v1 ist der Inhalt von pV1, v2 im Inhalt von pV2, t1 ist der Inhalt von pT1 und t2 der Inhalt von pT2.

Diese Eigenschaften werden zur Lösung für A, B, C, D verwendet.

Schließen Sie die Lösungen für A, B, C und D ein, um Fragen zu generieren.

``` syntax
A = 2v1 - 2v2 + t2 + t1 
B = 3v2 - 3v1 - 2t1 - t2
C = t1 
D = v1
```

Dies ergibt:

Q(s) = (2v1 - 2v2 + t2 + t1)s) + (3v2 - 3v1 - 2t1 - t2)s× t1s + v1

Dies kann neu angeordnet werden wie:

Q(s) = (2s, 3s) + 1)v1 + (-2s, + 3s) v2 + (ss - 2s): + s)t1 + (s) - s2)t2

Einsemit-Splines sind nützlich, um Animationen zu steuern, da die Kurve alle Kontrollpunkte durchläuft. Da die Position und der Tangens explizit an den Enden jedes Segments angegeben werden, ist es außerdem einfach, eine kontinuierliche C2-Kurve zu erstellen, solange Sie sicherstellen, dass Ihre Anfangsposition und der Tangens mit den Endwerten des letzten Segments übereinstimmen.

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXVec4Hermite-Funktion** als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
