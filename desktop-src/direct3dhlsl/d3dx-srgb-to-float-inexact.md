---
title: D3DX_SRGB_to_FLOAT_inexact-Funktion
description: Konvertiert einen SRGB-Wert in FLOAT. | D3DX_SRGB_to_FLOAT_inexact-Funktion
ms.assetid: 6eadda6d-ff99-4a8e-9e30-ae455732438e
keywords:
- D3DX_SRGB_to_FLOAT_inexact-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_SRGB_to_FLOAT_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9dd841e022da85d609c203f57288af62a6c99ecc9f56079982308a095285f39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118515691"
---
# <a name="d3dx_srgb_to_float_inexact-function"></a>D3DX SRGB to FLOAT inexact function (D3DX \_ SRGB \_ zu FLOAT \_ \_ inexact-Funktion)

Konvertiert einen SRGB-Wert in FLOAT.

## <a name="syntax"></a>Syntax

``` syntax
FLOAT D3DX_SRGB_to_FLOAT_inexact(
   hlsl_precise FLOAT val
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Val* 
</dt> <dd>

Der zu konvertierende SRGB-Wert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der konvertierte SRGB-Wert.

## <a name="remarks"></a>Hinweise

Diese Funktion hat nicht genügend Genauigkeit, um die genaue Antwort zu geben. Die alternative [**Funktion D3DX \_ SRGB zu \_ \_ FLOAT**](d3dx-srgb-to-float.md) verwendet eine Nachschlagetabelle, um eine exakte SRGB- in float-Konvertierung zu geben.

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

 

 





