---
description: 'D3DXVec2Normalize-Funktion (D3dx9math.h): Gibt die normalisierte Version eines 2D-Vektors zurück.'
ms.assetid: 2796a5d1-cb1c-4093-87f2-a2ad43279d91
title: D3DXVec2Normalize-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Normalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3322981be5c266bee20a61e85302cb22538a7b0d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097968"
---
# <a name="d3dxvec2normalize-function-d3dx9mathh"></a>D3DXVec2Normalize-Funktion (D3dx9math.h)

Gibt die normalisierte Version eines 2D-Vektors zurück.

## <a name="syntax"></a>Syntax


```C++
D3DXVECTOR2* D3DXVec2Normalize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Zeiger auf die [**D3DXVECTOR2-Struktur,**](d3dxvector2.md) die das Ergebnis des Vorgangs ist.

</dd> <dt>

*pV* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Zeiger auf die [**D3DXVECTOR2-Quellstruktur.**](d3dxvector2.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Zeiger auf eine [**D3DXVECTOR2-Struktur,**](d3dxvector2.md) bei der es sich um die normalisierte Version des Vektors handelt.

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird. Auf diese Weise kann die **D3DXVec2Normalize-Funktion** als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




