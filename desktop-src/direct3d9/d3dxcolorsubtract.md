---
description: Subtrahiert zwei Farbwerte, um einen neuen Farbwert zu erstellen.
ms.assetid: c21f8402-c1c2-4909-896f-2872ef518537
title: D3DXColorSubtract-Funktion (D3dx9math. h)
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
ms.openlocfilehash: 47f28ea3a3fb6d1556e699fed3820e228faf6604
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355201"
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

*Pout* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Zeiger auf eine [**D3DXCOLOR**](d3dxcolor.md) -Struktur, die das Ergebnis des Vorgangs ist.

</dd> <dt>

*pC1* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXCOLOR**](d3dxcolor.md) \***

Zeiger auf eine Quell- [**D3DXCOLOR**](d3dxcolor.md) -Struktur.

</dd> <dt>

*pC2* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXCOLOR**](d3dxcolor.md) \***

Zeiger auf eine Quell- [**D3DXCOLOR**](d3dxcolor.md) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Diese Funktion gibt einen Zeiger auf eine [**D3DXCOLOR**](d3dxcolor.md) -Struktur zurück, die den Unterschied zwischen zwei Farbwerten ist.

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXColorSubtract** -Funktion als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXColorAdd**](d3dxcoloradd.md)
</dt> </dl>

 

 




