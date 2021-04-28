---
description: 'D3DXPlaneIntersectLine-Funktion (D3DX10Math.h): Sucht die Schnittmenge zwischen einer Ebene und einer Linie.'
ms.assetid: aea1c4e1-f8c0-46df-bb33-2b517396d69e
title: D3DXPlaneIntersectLine-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneIntersectLine
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1d32bb312c97b793f492f7a29bebe11529b79cf9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108808"
---
# <a name="d3dxplaneintersectline-function-d3dx10mathh"></a>D3DXPlaneIntersectLine-Funktion (D3DX10Math.h)

Sucht die Schnittmenge zwischen einer Ebene und einer Linie.

## <a name="syntax"></a>Syntax


```C++
D3DXVECTOR3* D3DXPlaneIntersectLine(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXPLANE   *pP,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Zeiger auf einen [**D3DXVECTOR3,**](d3d10-d3dxvector3.md)der die Schnittmenge zwischen der angegebenen Ebene und Linie identifiziert.

</dd> <dt>

*pP* \[ In\]
</dt> <dd>

Typ: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***

Zeiger auf die [**D3DXPLANE-Quelldatei.**](d3d10-d3dxplane.md)

</dd> <dt>

*pV1* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf eine D3DXVECTOR3-Quellstruktur, die einen Zeilenstartpunkt definiert.

</dd> <dt>

*pV2* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf eine D3DXVECTOR3-Quellstruktur, die einen Zeilenendpunkt definiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Zeiger auf eine D3DXVECTOR3-Struktur, die die Schnittmenge zwischen der angegebenen Ebene und Linie ist.

## <a name="remarks"></a>Bemerkungen

Wenn die Linie parallel zur Ebene ist, wird **NULL** zurückgegeben.

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann die D3DXPlaneIntersectLine-Funktion als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
