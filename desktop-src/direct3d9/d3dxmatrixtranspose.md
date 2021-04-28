---
description: 'D3DXMatrixTranspose-Funktion (D3dx9math.h): Gibt die Matrix transponieren einer Matrix zurück.'
ms.assetid: 0ba9682f-3dd6-48b2-82b1-6e34e8ce5452
title: D3DXMatrixTranspose-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTranspose
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9cb050061b10de963258bcd7527d3c86260d5abc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098108"
---
# <a name="d3dxmatrixtranspose-function-d3dx9mathh"></a>D3DXMatrixTranspose-Funktion (D3dx9math.h)

Gibt die Matrix transponieren einer Matrix zurück.

## <a name="syntax"></a>Syntax


```C++
D3DXMATRIX* D3DXMatrixTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Zeiger auf die [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die das Ergebnis des Vorgangs ist.

</dd> <dt>

*pM* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Zeiger auf die [**D3DXMATRIX-Quellstruktur.**](d3dxmatrix.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Zeiger auf die [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die die Matrix transponiert.

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird. Auf diese Weise kann die **D3DXMatrixTranspose-Funktion** als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




