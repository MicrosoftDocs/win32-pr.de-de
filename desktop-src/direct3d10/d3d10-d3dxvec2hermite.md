---
description: 'D3DXVec2Hermite-Funktion (D3DX10Math.h): Führt eine Hermite-Splineinterpolation mit den angegebenen 2D-Vektoren aus.'
ms.assetid: 2d6ff836-a1a7-4cd0-aea3-4fe344f4e211
title: D3DXVec2Hermite-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Hermite
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e64350d4f54fef493ec7fe935474218a1b111503
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108378"
---
# <a name="d3dxvec2hermite-function-d3dx10mathh"></a>D3DXVec2Hermite-Funktion (D3DX10Math.h)

Führt eine Hermite-Splineinterpolation unter Verwendung der angegebenen 2D-Vektoren aus.

## <a name="syntax"></a>Syntax


```C++
D3DXVECTOR2* D3DXVec2Hermite(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pT1,
  _In_    const D3DXVECTOR2 *pV2,
  _In_    const D3DXVECTOR2 *pT2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

Zeiger auf [**D3DXVECTOR2,**](d3d10-d3dxvector2.md) das das Ergebnis des Vorgangs ist.

</dd> <dt>

*pV1* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Zeiger auf eine D3DXVECTOR2-Quellstruktur, einen Positionsvektor.

</dd> <dt>

*pT1* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Zeiger auf eine D3DXVECTOR2-Quellstruktur, einen Tangensvektor.

</dd> <dt>

*pV2* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Zeiger auf eine D3DXVECTOR2-Quellstruktur, einen Positionsvektor.

</dd> <dt>

*pT2* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Zeiger auf eine D3DXVECTOR2-Quellstruktur, einen Tangensvektor.

</dd> <dt>

*s* \[ in\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Gewichtungsfaktor. Siehe Hinweise.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

Zeiger auf eine D3DXVECTOR2-Struktur, die das Ergebnis der Hermite-Splineinterpolation ist.

## <a name="remarks"></a>Bemerkungen

Die **D3DXVec2Hermite-Funktion** interpoliert mithilfe der Hermite-Splineinterpolation von (positionA, tangentA) in (positionB, tangentB).

Die Splineinterpolation ist eine Generalisierung der einfachen, einfachen Spline. Die Rampe ist eine Funktion von Q(s) mit den folgenden Eigenschaften.

Q(s) = As( + Bs) + Cs + D (und daher Q'(s) = 3As× + 2Bs + C)

a) Q(0) = v1, also Q'(0) = t1

b) Q(1) = v2, also Q'(1) = t2

v1 ist der Inhalt von pV1, v2 im Inhalt von pV2, t1 ist der Inhalt von pT1 und t2 der Inhalt von pT2.

Diese Eigenschaften werden zur Lösung für A, B, C, D verwendet.


```
D = v1  (from a)
C = t1  (from a)
3A + 2B = t2 - t-1 (substituting for C)
A + B = v2 - v1 - t1 (substituting for C and D)
```



Schließen Sie die Lösungen für A, B, C und D ein, um Fragen zu generieren.


```
A = 2v1 - 2v2 + t2 + t1 
B = 3v2 - 3v1 - 2t1 - t2
C = t1 
D = v1
```



Dies ergibt:

Q(s) = (2v1 - 2v2 + t2 + t1)s) + (3v2 - 3v1 - 2t1 - t2)s× t1s + v1

Dies kann neu angeordnet werden wie:

Q(s) = (2s, 3s) + 1)v1 + (-2s, + 3s) v2 + (s= - 2s): + s)t1 + (s) - s2)t2

Einsemit-Splines sind nützlich, um Animationen zu steuern, da die Kurve alle Kontrollpunkte durchläuft. Da die Position und der Tangens explizit an den Enden jedes Segments angegeben werden, ist es außerdem einfach, eine kontinuierliche C2-Kurve zu erstellen, solange Sie sicherstellen, dass Ihre Anfangsposition und der Tangens mit den Endwerten des letzten Segments übereinstimmen.

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXVec2Hermite-Funktion** als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
