---
description: Subtrahiert zwei Farbwerte, um einen neuen Farbwert zu erstellen.
ms.assetid: c21f8402-c1c2-4909-896f-2872ef518537
title: D3DXColorSubtract-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorSubtract
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a1d0d9c884dbbfb8e4ae718985be90d22002bd0f2a4cf25f45d02ded12718d2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300140"
---
# <a name="d3dxcolorsubtract-function"></a>D3DXColorSubtract-Funktion

Subtrahiert zwei Farbwerte, um einen neuen Farbwert zu erstellen.

## <a name="syntax"></a>Syntax


```C++
D3DXCOLOR* D3DXColorSubtract(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Zeiger auf eine [**D3DXCOLOR-Struktur,**](d3dxcolor.md) die das Ergebnis des Vorgangs ist.

</dd> <dt>

*pC1* \[ In\]
</dt> <dd>

Typ: **const [**D3DXCOLOR**](d3dxcolor.md) \***

Zeiger auf eine [**D3DXCOLOR-Quellstruktur.**](d3dxcolor.md)

</dd> <dt>

*pC2* \[ In\]
</dt> <dd>

Typ: **const [**D3DXCOLOR**](d3dxcolor.md) \***

Zeiger auf eine [**D3DXCOLOR-Quellstruktur.**](d3dxcolor.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Diese Funktion gibt einen Zeiger auf eine [**D3DXCOLOR-Struktur**](d3dxcolor.md) zurück, die den Unterschied zwischen zwei Farbwerten angibt.

## <a name="remarks"></a>Hinweise

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXColorSubtract-Funktion** als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXColorAdd**](d3dxcoloradd.md)
</dt> </dl>

 

 




