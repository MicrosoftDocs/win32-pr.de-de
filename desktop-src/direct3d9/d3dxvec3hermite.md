---
description: 'D3DXVec3Hermite-Funktion (D3dx9math.h): Führt eine Hermite-Splineinterpolation unter Verwendung der angegebenen 3D-Vektoren aus.'
ms.assetid: d45b1179-0e11-4f58-8d50-432236cb88ca
title: D3DXVec3Hermite-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Hermite
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b35c99ac6127f1d0b74598fd53465709b45f533c6fbcbd7b898bb572fcc6a941
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118297772"
---
# <a name="d3dxvec3hermite-function-d3dx9mathh"></a>D3DXVec3Hermite-Funktion (D3dx9math.h)

Führt eine Hermite-Splineinterpolation unter Verwendung der angegebenen 3D-Vektoren aus.

## <a name="syntax"></a>Syntax


```C++
D3DXVECTOR3* D3DXVec3Hermite(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pT1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pT2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Zeiger auf die [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die das Ergebnis des Vorgangs ist.

</dd> <dt>

*pV1* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Quellstruktur,**](d3dxvector3.md) einen Positionsvektor.

</dd> <dt>

*pT1* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Quellstruktur,**](d3dxvector3.md) einen Tangensvektor.

</dd> <dt>

*pV2* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Quellstruktur,**](d3dxvector3.md) einen Positionsvektor.

</dd> <dt>

*pT2* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Quellstruktur,**](d3dxvector3.md) einen Tangensvektor.

</dd> <dt>

*s* \[ in\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Gewichtungsfaktor. Siehe Hinweise.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die das Ergebnis der Hermite-Splineinterpolation ist.

## <a name="remarks"></a>Hinweise

Die **D3DXVec3Hermite-Funktion** interpoliert mithilfe der Hermite-Splineinterpolation von (positionA, tangentA) nach (positionB, tangentB).

Die Splineinterpolation ist eine Verallgemeinerung des Splines mit einfacherEntschärfung. Die Rampe ist eine Funktion von Q(s) mit den folgenden Eigenschaften.

Q(s) = Assstelle + Bssstelle + Cs + D (und daher Q(s) = 3Aszept + 2Bs + C)

a) Q(0) = v1, also Q'(0) = t1

b) Q(1) = v2, also Q'(1) = t2

v1 ist der Inhalt von pV1, v2 im Inhalt von pV2, t1 ist der Inhalt von pT1 und t2 ist der Inhalt von pT2.

Diese Eigenschaften werden für A, B, C, D verwendet.

``` syntax
D = v1  (from a)
C = t1  (from a)
3A + 2B = t2 - t1 (substituting for C)
A + B = v2 - v1 - t1 (substituting for C and D)
```

Schließen Sie die Lösungen für A, B, C und D ein, um Q(s) zu generieren.

``` syntax
A = 2v1 - 2v2 + t2 + t1 
B = 3v2 - 3v1 - 2t1 - t2
C = t1 
D = v1
```

Dies ergibt:

Q(s) = (2v1 - 2v2 + t2 + t1)ssstelle + (3v2 - 3v1 - 2t1 - t2)ssstelle + t1s + v1

Dies kann wie hier angezeigt neu angeordnet werden:

Q(s) = (2ssstelle – 3ssstelle + 1)v1 + (-2ssstelle + 3ssstelle)v2 + (ssstelle – 2ssstelle + s)t1 + (ssstelle – ssstelle)t2

Hermite-Splines sind nützlich zum Steuern der Animation, da die Kurve alle Kontrollpunkte durchläuft. Da die Position und der Tangens explizit an den Enden jedes Segments angegeben werden, ist es außerdem einfach, eine kontinuierliche C2-Kurve zu erstellen, solange Sie sicherstellen, dass Ihre Anfangsposition und der Tangens mit den Endwerten des letzten Segments übereinstimmen.

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXVec3Hermite-Funktion** als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
