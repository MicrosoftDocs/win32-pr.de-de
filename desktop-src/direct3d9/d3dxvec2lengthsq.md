---
description: Gibt das Quadrat der Länge eines 2D-Vektors zurück.
ms.assetid: 0ecc40bb-7613-463a-a8a0-5e184feb441f
title: D3DXVec2LengthSq-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2LengthSq
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b05ad62f1a7ee26cfb25251b43c3df9dfe87314c5b1d92ac19f65e19416d3ed2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804060"
---
# <a name="d3dxvec2lengthsq-function"></a>D3DXVec2LengthSq-Funktion

Gibt das Quadrat der Länge eines 2D-Vektors zurück.

## <a name="syntax"></a>Syntax


```C++
FLOAT D3DXVec2LengthSq(
  _In_ const D3DXVECTOR2 *pV
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pV* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Zeiger auf die [**D3DXVECTOR2-Quellstruktur.**](d3dxvector2.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Die quadratische Länge des Vektors.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2Length**](d3dxvec2length.md)
</dt> </dl>

 

 
