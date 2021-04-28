---
description: 'D3DXQuaternionSquad-Funktion (D3dx9math.h): Interpolate zwischen Quaternionen mithilfe der pherischen Quadrangleinterpolation.'
ms.assetid: afce9afb-64cc-4059-90f5-7ed1aca9b3cb
title: D3DXQuaternionSquad-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSquad
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c7bef8671b38ec2e8208a6de0ec7542cf28ffa44
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117988"
---
# <a name="d3dxquaternionsquad-function-d3dx9mathh"></a>D3DXQuaternionSquad-Funktion (D3dx9math.h)

Interpoliert zwischen Quaternionen mithilfe der pherischen Quadrangleinterpolation.

## <a name="syntax"></a>Syntax


```C++
D3DXQUATERNION* D3DXQuaternionSquad(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pA,
  _In_    const D3DXQUATERNION *pB,
  _In_    const D3DXQUATERNION *pC,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Zeiger auf die [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) die das Ergebnis des Vorgangs ist.

</dd> <dt>

*pQ1* \[ In\]
</dt> <dd>

Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Zeiger auf eine [**D3DXQUATERNION-Quellstruktur.**](d3dxquaternion.md)

</dd> <dt>

*pA* \[ In\]
</dt> <dd>

Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Zeiger auf eine [**D3DXQUATERNION-Quellstruktur.**](d3dxquaternion.md)

</dd> <dt>

*pB* \[ In\]
</dt> <dd>

Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Zeiger auf eine [**D3DXQUATERNION-Quellstruktur.**](d3dxquaternion.md)

</dd> <dt>

*pC* \[ In\]
</dt> <dd>

Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Zeiger auf eine [**D3DXQUATERNION-Quellstruktur.**](d3dxquaternion.md)

</dd> <dt>

*t* \[ in\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Parameter, der angibt, wie weit zwischen den Quaternionen interpoliert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Zeiger auf eine [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) die das Ergebnis der sphärischen Quadrangleinterpolation ist.

## <a name="remarks"></a>Bemerkungen

Diese Funktion verwendet die folgende Sequenz von sphärischen linearen Interpolationsvorgängen:


```
Slerp(Slerp(pQ1, pC, t), Slerp(pA, pB, t), 2t(1 - t))
```



Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird. Auf diese Weise kann die **D3DXQuaternionSquad-Funktion** als Parameter für eine andere Funktion verwendet werden.

Ein Beispiel für die Interpolation zwischen Quaternionen finden Sie im SkinnedMesh-Beispiel. Sie erhalten dieses Beispiel und erfahren mehr über das DirectX SDK. Informationen zum DirectX SDK finden Sie unter [Wo befindet sich das DirectX SDK?](../directx-sdk--august-2009-.md).

Verwenden Sie [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für alle Quaternioneingaben, die nicht bereits normalisiert sind.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXQuaternionExp**](d3dxquaternionexp.md)
</dt> <dt>

[**D3DXQuaternionLn**](d3dxquaternionln.md)
</dt> <dt>

[**D3DXQuaternionSquadSetup**](d3dxquaternionsquadsetup.md)
</dt> </dl>

 

 
