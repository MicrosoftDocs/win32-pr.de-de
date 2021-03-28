---
title: D3DX_IsNan-Funktion
description: Bestimmt, ob der Wert ein NaN (not a Number) ist.
ms.assetid: 862d1d34-36ab-471e-b3ce-ce71896441e5
keywords:
- D3DX_IsNan-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_IsNan
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60aac82ebfb145bc11aac8d4ab509a4260767a74
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961734"
---
# <a name="d3dx_isnan-function"></a>D3DX \_ isNaN-Funktion

Bestimmt, ob der Wert ein NaN (not a Number) ist.

## <a name="syntax"></a>Syntax

``` syntax
bool D3DX_IsNan(
   FLOAT _V
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*\_Ramelow* 
</dt> <dd>

Der angegebene Wert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

true, wenn ein NaN; andernfalls false.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX \_ dxgiformatconvert. INL</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Funktionen](format-conversion-functions.md)
</dt> <dt>

[Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





