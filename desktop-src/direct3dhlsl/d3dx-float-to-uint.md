---
title: D3DX_FLOAT_to_UINT-Funktion
description: Konvertiert einen float-Wert in uint.
ms.assetid: 05c5de72-8915-4541-a82d-242e46bfa883
keywords:
- D3DX_FLOAT_to_UINT-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT_to_UINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e729ba805d63068844192a134236722288fe8a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354296"
---
# <a name="d3dx_float_to_uint-function"></a>D3DX \_ float \_ in \_ uint-Funktion

Konvertiert einen float-Wert in uint.

## <a name="syntax"></a>Syntax

``` syntax
UINT D3DX_FLOAT_to_UINT(
   FLOAT _V,
   FLOAT _Scale
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*\_Ramelow* 
</dt> <dd>

Der v-Vektor.

</dd> <dt>

*\_Skalieren* 
</dt> <dd>

Der Skalierungs Wert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der konvertierte float-Wert.

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

 

 





