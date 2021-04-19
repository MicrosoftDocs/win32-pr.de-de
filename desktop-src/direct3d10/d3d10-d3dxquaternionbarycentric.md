---
description: Gibt eine Quaternion in baryzentrierten Koordinaten zurück.
ms.assetid: 0a8d8d5a-f486-4457-86e9-27e76eaf1bc4
title: D3DXQuaternionBaryCentric-Funktion (D3DX10Math. h)
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
ms.openlocfilehash: f7cdfcf5b8e7052fcbea72f12123a0ea44422853
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367471"
---
# <a name="d3dxquaternionbarycentric-function-d3dx10mathh"></a>D3DXQuaternionBaryCentric-Funktion (D3DX10Math. h)

Gibt eine Quaternion in baryzentrierten Koordinaten zurück.

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

*Pout* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Zeiger auf das [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , das das Ergebnis des Vorgangs ist.

</dd> <dt>

*pQ1* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Zeiger auf eine Quell-D3DXQUATERNION-Struktur.

</dd> <dt>

*pQ2* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Zeiger auf eine Quell-D3DXQUATERNION-Struktur.

</dd> <dt>

*pQ3* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Zeiger auf eine Quell-D3DXQUATERNION-Struktur.

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

Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Zeiger auf eine D3DXQUATERNION-Struktur in den baryzentrierten Koordinaten.

## <a name="remarks"></a>Bemerkungen

Zum Berechnen der barzentrischen Koordinaten implementiert die D3DXQuaternionBaryCentric-Funktion die folgende Reihe von sphärischen linearen Interpolations Vorgängen:


```
Slerp(Slerp(Q1, Q2, f+g), Slerp(Q1, Q3, f+g), g/(f+g))
```



Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird. Auf diese Weise kann die D3DXQuaternionBaryCentric-Funktion als Parameter für eine andere Funktion verwendet werden.

Verwenden Sie [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) für eine beliebige Quaternion-Eingabe, die nicht bereits normalisiert ist.

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

 

 
