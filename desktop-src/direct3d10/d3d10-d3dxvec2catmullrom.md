---
description: Führt eine Catmull-Rom interpolung mithilfe der angegebenen 2D-Vektoren aus.
ms.assetid: 8ec1abfa-0fa9-486a-b86d-bbb8f1d63849
title: D3DXVec2CatmullRom-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2CatmullRom
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 71f499313a31c200b5cc657664b10b43dde47ba6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363164"
---
# <a name="d3dxvec2catmullrom-function-d3dx10mathh"></a>D3DXVec2CatmullRom-Funktion (D3DX10Math. h)

Führt eine Catmull-Rom interpolung mithilfe der angegebenen 2D-Vektoren aus.

## <a name="syntax"></a>Syntax


```C++
D3DXVECTOR2* D3DXVec2CatmullRom(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV0,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2,
  _In_    const D3DXVECTOR2 *pV3,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pout* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

Zeiger auf das [**D3DXVECTOR2**](d3d10-d3dxvector2.md) , das das Ergebnis des Vorgangs ist.

</dd> <dt>

*pV0* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Zeiger auf eine Quell-D3DXVECTOR2-Struktur, ein Positions Vektor.

</dd> <dt>

*pV1* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Zeiger auf eine Quell-D3DXVECTOR2-Struktur, ein Positions Vektor.

</dd> <dt>

*pV2* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Zeiger auf eine Quell-D3DXVECTOR2-Struktur, ein Positions Vektor.

</dd> <dt>

*pV3* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Zeiger auf eine Quell-D3DXVECTOR2-Struktur, ein Positions Vektor.

</dd> <dt>

*s* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Gewichtungsfaktor. Siehe Hinweise.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

Zeiger auf eine D3DXVECTOR2-Struktur, die das Ergebnis der Catmull-Rom interpolung ist.

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
Q(s) = (2s3 - 3s2 + 1)p2 + (-2s3 + 3s2)p3 + (s3 - 2s2 + s)(p3 - p1) / 2 + (s3 - s2)(p4 - p2)/2
```



Dies kann wie folgt neu angeordnet werden:


```
Q(s) = [(-s3 + 2s2 - s)p1 + (3s3 - 5s2 + 2)p2 + (-3s3 + 4s2 + s)p3 + (s3 - s2)p4] / 2
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
