---
description: 'D3DXVec4CatmullRom-Funktion (D3dx9math.h): Führt unter Verwendung der angegebenen 4D-Vektoren eine Catmull-Rom Interpolation durch.'
ms.assetid: 24c26e70-b02c-4621-8b7e-db16f99dddb5
title: D3DXVec4CatmullRom-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4CatmullRom
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 06ba24374ee2ad4e6fd008d90c55d2990dc166f6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115528"
---
# <a name="d3dxvec4catmullrom-function-d3dx9mathh"></a>D3DXVec4CatmullRom-Funktion (D3dx9math.h)

Führt eine Catmull-Rom Interpolation unter Verwendung der angegebenen 4D-Vektoren aus.

## <a name="syntax"></a>Syntax


```C++
D3DXVECTOR4* D3DXVec4CatmullRom(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV0,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pV3,
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

*pV0* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Zeiger auf eine [**D3DXVECTOR4-Quellstruktur,**](d3dxvector4.md) einen Positionsvektor.

</dd> <dt>

*pV1* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Zeiger auf eine [**D3DXVECTOR4-Quellstruktur,**](d3dxvector4.md) einen Positionsvektor.

</dd> <dt>

*pV2* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Zeiger auf eine [**D3DXVECTOR4-Quellstruktur,**](d3dxvector4.md) einen Positionsvektor.

</dd> <dt>

*pV3* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Zeiger auf eine [**D3DXVECTOR4-Quellstruktur,**](d3dxvector4.md) einen Positionsvektor.

</dd> <dt>

*s* \[ in\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Gewichtungsfaktor. Siehe Hinweise.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Zeiger auf eine [**D3DXVECTOR4-Struktur,**](d3dxvector4.md) die das Ergebnis der Catmull-Rom ist.

## <a name="remarks"></a>Bemerkungen

Suchen Sie bei vier Punkten (p1, p2, p3, p4) eine Funktion Q(s) so, dass:


```
Q(s) is a cubic function. 
Q(s) interpolates between p2 and p3 as s ranges from 0 to 1. 
Q(s) is parallel to the line joining p1 to p3 when s is 0. 
Q(s) is parallel to the line joining p2 to p4 when s is 1. 
```



Die Catmull-Rom spline kann durch Festlegen von vom Hermite-Spline abgeleitet werden:


```
v1 = p2
v2 = p3
t1 = (p3 - p1) / 2
t2 = (p4 - p2) / 2
```



Dabei gilt:

v1 ist der Inhalt von pV0.

v2 im Inhalt von pV1.

p3 ist der Inhalt von pV2.

p4 ist der Inhalt von pV3.

Verwenden der Splinegleichung "Hermite":


```
Q(s) = (2s3 - 3s2 + 1)v1 + (-2s3 + 3s2)v2 + (s3 - 2s2 + s)t1 + (s3 - s2)t2
```



und der Ersatz für v1, v2, t1, t2 ergibt:


```
Q(s) = (2s3 - 3s2 + 1)p2 + (-2s3 + 3s2)p3 + (s3 - 2s2 + s)(p3 - p1) / 2 + (s3 - s2)(p4 - p2) / 2
```



Dies kann neu angeordnet werden wie:


```
Q(s) = [(-s3 + 2s2 - s)p1 + (3s3 - 5s2 + 2)p2 + (-3s3 + 4s2 + s)p3 + (s3 - s2)p4] / 2
```



## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2CatmullRom**](d3dxvec2catmullrom.md)
</dt> <dt>

[**D3DXVec3CatmullRom**](d3dxvec3catmullrom.md)
</dt> </dl>

 

 
