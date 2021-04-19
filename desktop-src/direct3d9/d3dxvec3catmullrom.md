---
description: Führt eine Catmull-Rom interpolung mithilfe der angegebenen 3D-Vektoren aus.
ms.assetid: 779f067c-ac46-4fde-9e18-e31b1504b490
title: D3DXVec3CatmullRom-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3CatmullRom
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d56c4551f6451d5b817ca0a312ceea6961d3fcce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367405"
---
# <a name="d3dxvec3catmullrom-function-d3dx9mathh"></a>D3DXVec3CatmullRom-Funktion (D3dx9math. h)

Führt eine Catmull-Rom interpolung mithilfe der angegebenen 3D-Vektoren aus.

## <a name="syntax"></a>Syntax


```C++
D3DXVECTOR3* D3DXVec3CatmullRom(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV0,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pV3,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pout* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Ein Zeiger auf die [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die das Ergebnis des Vorgangs ist.

</dd> <dt>

*pV0* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, ein Positions Vektor.

</dd> <dt>

*pV1* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, ein Positions Vektor.

</dd> <dt>

*pV2* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, ein Positions Vektor.

</dd> <dt>

*pV3* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, ein Positions Vektor.

</dd> <dt>

*s* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Gewichtungsfaktor. Siehe Hinweise.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die das Ergebnis der Catmull-Rom interpolung ist.

## <a name="remarks"></a>Bemerkungen

In den vier Punkten (P1, P2, P3, P4) finden Sie eine f (s)-Funktion wie folgt:


```
Q(s) is a cubic function. 
Q(s) interpolates between p2 and p3 as s ranges from 0 to 1. 
Q(s) is parallel to the line joining p1 to p3 when s is 0. 
Q(s) is parallel to the line joining p2 to p4 when s is 1. 
```



Die Catmull-Rom Spline kann von der Hermite Spline abgeleitet werden, indem Sie Folgendes festlegen:


```
v1 = p2
v2 = p3
t1 = (p3 - p1) / 2
t2 = (p4 - p2) / 2
```



Dabei gilt:

v1 ist der Inhalt von pV0.

v2 ist der Inhalt von pV1.

P3 ist der Inhalt von pV2.

P4 ist der Inhalt von pV3.

Verwenden der Hermite-Spline-Gleichung:


```
Q(s) = (2s3 - 3s2 + 1)v1 + (-2s3 + 3s2)v2 + (s3 - 2s2 + s)t1 + (s3 - s2)t2
```



und ersetzen Sie durch die Ergebnisse v1, v2, T1, T2:


```
Q(s) = (2s3 - 3s2 + 1)p2 + (-2s3 + 3s2)p3 + (s3 - 2s2 + s)(p3 - p1) / 2 + (s3 - s2)(p4 - p2) / 2
```



Dies kann wie folgt neu angeordnet werden:


```
Q(s) = [(-s3 + 2s2 - s)p1 + (3s3 - 5s2 + 2)p2 + (-3s3 + 4s2 + s)p3 + (s3 - s2)p4] / 2
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2CatmullRom**](d3dxvec2catmullrom.md)
</dt> <dt>

[**D3DXVec4CatmullRom**](d3dxvec4catmullrom.md)
</dt> </dl>

 

 
