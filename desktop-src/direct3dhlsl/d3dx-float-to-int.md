---
title: D3DX_FLOAT_to_INT-Funktion
description: Konvertiert einen FLOAT-Wert in INT.
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
ms.openlocfilehash: fb76c5c459daaaba4dd7d038b65b9dc34e895f283b66545684ef1f5fb10c95cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516663"
---
# <a name="d3dx_float_to_int-function"></a>D3DX \_ FLOAT \_ to \_ INT-Funktion

Konvertiert einen FLOAT-Wert in INT.

## <a name="syntax"></a>Syntax

``` syntax
INT D3DX_FLOAT_to_INT(
   FLOAT _V,
   FLOAT _Scale
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*\_V* 
</dt> <dd>

Der v-Wert.

</dd> <dt>

*\_Skalieren* 
</dt> <dd>

Der Skalierungswert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der konvertierte FLOAT-Wert

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert.inl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Funktionen](format-conversion-functions.md)
</dt> <dt>

[Entpacken und Packen des \_ DXGI-FORMATS für In-Place Bildbearbeitung](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





