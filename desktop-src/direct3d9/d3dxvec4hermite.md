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
ms.openlocfilehash: b08ed785c24ba9580be0fc7f620a471ea96184a8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097698"
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

## <a name="remarks"></a>Bemerkungen

Die **D3DXVec4Hermite-Funktion** interpoliert mithilfe der Hermite-Splineinterpolation von (positionA, tangentA) nach (positionB, tangentB).

Die Splineinterpolation ist eine Verallgemeinerung des Splines mit einfacherEntschärfung. Die Rampe ist eine Funktion von Q(s) mit den folgenden Eigenschaften.

Q(s) = Assstelle + Bssstelle + Cs + D (und daher Q(s) = 3Aszept + 2Bs + C)

a) Q(0) = v1, also Q'(0) = t1

b) Q(1) = v2, also Q'(1) = t2

v1 ist der Inhalt von pV1, v2 im Inhalt von pV2, t1 ist der Inhalt von pT1 und t2 ist der Inhalt von pT2.

Diese Eigenschaften werden für A, B, C, D verwendet.

Schließen Sie die Lösungen für A, B, C und D ein, um Q(s) zu generieren.

``` syntax
A = 2v1 - 2v2 + t2 + t1 
B = 3v2 - 3v1 - 2t1 - t2
C = t1 
D = v1
```

Dies ergibt:

Q(s) = (2v1 - 2v2 + t2 + t1)ssstelle + (3v2 - 3v1 - 2t1 - t2)stif + t1s + v1

Dies kann wie hier angezeigt neu angeordnet werden:

Q(s) = (2ssstelle – 3ssstelle + 1)v1 + (-2ssstelle + 3ssstelle)v2 + (ssstelle – 2ssstelle + s)t1 + (ssstelle – ssstelle)t2

Hermite-Splines sind nützlich zum Steuern der Animation, da die Kurve alle Kontrollpunkte durchläuft. Da die Position und der Tangens explizit an den Enden jedes Segments angegeben werden, ist es außerdem einfach, eine kontinuierliche C2-Kurve zu erstellen, solange Sie sicherstellen, dass Ihre Anfangsposition und der Tangens mit den Endwerten des letzten Segments übereinstimmen.

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXVec4Hermite-Funktion** als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
