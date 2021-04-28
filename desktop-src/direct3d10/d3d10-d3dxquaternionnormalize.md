---
description: 'D3DXQuaternionNormalize-Funktion (D3DX10Math.h): Berechnet eine Einheitslängen-Quaternion.'
ms.assetid: 6735a632-64d7-4bc1-b63e-d0cd27f5a29b
title: D3DXQuaternionNormalize-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionNormalize
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6d031dfc63cb92d43a9cca27813c9425e2ff1acb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103138"
---
# <a name="d3dxquaternionnormalize-function-d3dx10mathh"></a>D3DXQuaternionNormalize-Funktion (D3DX10Math.h)

Berechnet eine Einheitslängen-Quaternion.

## <a name="syntax"></a>Syntax


```C++
D3DXQUATERNION* D3DXQuaternionNormalize(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Zeiger auf [**D3DXQUATERNION,**](d3d10-d3dxquaternion.md) das das Ergebnis des Vorgangs ist.

</dd> <dt>

*pQ* \[ In\]
</dt> <dd>

Typ: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Zeiger auf die D3DXQUATERNION-Quellstruktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Zeiger auf eine D3DXQUATERNION-Struktur, die der Normalität der Quaternion entspricht.

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann die D3DXQuaternionNormalize-Funktion als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
