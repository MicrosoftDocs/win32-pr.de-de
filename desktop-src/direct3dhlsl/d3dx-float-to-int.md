---
title: D3DX_FLOAT_to_INT-Funktion
description: Konvertiert einen float-Wert in einen int-Wert.
ms.assetid: 69b67218-fe25-478f-9f7e-05f94d9f99d5
keywords:
- D3DX_FLOAT_to_INT-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT_to_INT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c127ef20cdd21cbc83e466f75844b4f80f47f948
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531064"
---
# <a name="d3dx_float_to_int-function"></a>D3DX \_ float \_ to \_ int-Funktion

Konvertiert einen float-Wert in einen int-Wert.

## <a name="syntax"></a>Syntax

``` syntax
INT D3DX_FLOAT_to_INT(
   FLOAT _V,
   FLOAT _Scale
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*\_Ramelow* 
</dt> <dd>

Der v-Wert.

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

 

 





