---
description: 'D3DXQuaternionRotationMatrix-Funktion (D3DX10Math.h): Erstellt eine Quaternion aus einer Rotationsmatrix.'
ms.assetid: 316bf3e0-32ff-4e5e-b771-99f7eea2e27c
title: D3DXQuaternionRotationMatrix-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationMatrix
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a27a75261c177fc39bca75af667f244ddef25e9a7f541a1bbdc5da6b4574f427
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991030"
---
# <a name="d3dxquaternionrotationmatrix-function-d3dx10mathh"></a>D3DXQuaternionRotationMatrix-Funktion (D3DX10Math.h)

Erstellt eine Quaternion aus einer Rotationsmatrix.

## <a name="syntax"></a>Syntax


```C++
D3DXQUATERNION* D3DXQuaternionRotationMatrix(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Zeiger auf das [**D3DXQUATERNION-Steuerelement,**](d3d10-d3dxquaternion.md) das das Ergebnis des Vorgangs ist.

</dd> <dt>

*pM* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Zeiger auf die [**D3DXMATRIX-Quellstruktur.**](d3d10-d3dxmatrix.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Zeiger auf die D3DXQUATERNION-Struktur, die aus einer Rotationsmatrix erstellt wurde.

## <a name="remarks"></a>Hinweise

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann die D3DXQuaternionRotationMatrix-Funktion als Parameter für eine andere Funktion verwendet werden.

Verwenden [**Sie D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) für alle Quaternioneingaben, die noch nicht normalisiert sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
