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
ms.openlocfilehash: 1ef71912dd5c8efeb25f2ad30dd9746b1cb493aff2aa28dd2008ef764a1135ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731298"
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

Zeiger auf eine [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) die das Ergebnis der pherischen Quadrangleinterpolation ist.

## <a name="remarks"></a>Hinweise

Diese Funktion verwendet die folgende Sequenz von pherischen linearen Interpolationsvorgängen:


```
Slerp(Slerp(pQ1, pC, t), Slerp(pA, pB, t), 2t(1 - t))
```



Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird. Auf diese Weise kann die **D3DXQuaternionSquad-Funktion** als Parameter für eine andere Funktion verwendet werden.

Ein Beispiel für die Interpolation zwischen Quaternionen finden Sie im SkinnedMesh-Beispiel. Sie können dieses Beispiel erhalten und sich über das DirectX SDK darüber informieren. Informationen zum DirectX SDK finden Sie unter [Wo ist das DirectX SDK?](../directx-sdk--august-2009-.md).

Verwenden [**Sie D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für alle Quaternioneingaben, die noch nicht normalisiert sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
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

 

 
