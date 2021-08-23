---
description: 'D3DXQuaternionBaryCentric-Funktion (D3DX10Math.h): Gibt eine Quaternion in barycentric-Koordinaten zurück.'
ms.assetid: 0a8d8d5a-f486-4457-86e9-27e76eaf1bc4
title: D3DXQuaternionBaryCentric-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionBaryCentric
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6a51a0606ae45be79c26d062c64ab5710a658436371ca146f81c2183c34ca85b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991150"
---
# <a name="d3dxquaternionbarycentric-function-d3dx10mathh"></a>D3DXQuaternionBaryCentric-Funktion (D3DX10Math.h)

Gibt eine Quaternion in baryzentrischen Koordinaten zurück.

## <a name="syntax"></a>Syntax


```C++
D3DXQUATERNION* D3DXQuaternionBaryCentric(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2,
  _In_    const D3DXQUATERNION *pQ3,
  _In_          FLOAT          f,
  _In_          FLOAT          g
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Zeiger auf [**D3DXQUATERNION,**](d3d10-d3dxquaternion.md) das das Ergebnis des Vorgangs ist.

</dd> <dt>

*pQ1* \[ In\]
</dt> <dd>

Typ: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Zeiger auf eine D3DXQUATERNION-Quellstruktur.

</dd> <dt>

*pQ2* \[ In\]
</dt> <dd>

Typ: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Zeiger auf eine D3DXQUATERNION-Quellstruktur.

</dd> <dt>

*pQ3* \[ In\]
</dt> <dd>

Typ: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Zeiger auf eine D3DXQUATERNION-Quellstruktur.

</dd> <dt>

*f* \[ in\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Gewichtungsfaktor. Siehe Hinweise.

</dd> <dt>

*g* \[ in\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Gewichtungsfaktor. Siehe Hinweise.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Zeiger auf eine D3DXQUATERNION-Struktur in baryzentrischen Koordinaten.

## <a name="remarks"></a>Hinweise

Um die baryzentrischen Koordinaten zu berechnen, implementiert die D3DXQuaternionBaryCentric-Funktion die folgende Reihe von sphärischen linearen Interpolationsvorgängen:


```
Slerp(Slerp(Q1, Q2, f+g), Slerp(Q1, Q3, f+g), g/(f+g))
```



Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann die D3DXQuaternionBaryCentric-Funktion als Parameter für eine andere Funktion verwendet werden.

Verwenden Sie [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) für alle Quaternioneingaben, die noch nicht normalisiert sind.

Barycentric-Koordinaten definieren einen Punkt innerhalb eines Dreiecks in Bezug auf die Scheitelpunkte des Dreiecks. Eine ausführlichere Beschreibung der baryzentrischen Koordinaten finden Sie unter [Mathworld es Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
