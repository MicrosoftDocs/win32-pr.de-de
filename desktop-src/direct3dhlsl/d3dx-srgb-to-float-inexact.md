---
title: D3DX_SRGB_to_FLOAT_inexact-Funktion
description: Konvertiert einen sRGB-Wert in float. | D3DX_SRGB_to_FLOAT_inexact-Funktion
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
ms.openlocfilehash: 44804ad73ab49ce4f62274c870d8487501c44361
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982209"
---
# <a name="d3dx_srgb_to_float_inexact-function"></a>D3DX \_ sRGB \_ in \_ \_ ungenau-Funktion

Konvertiert einen sRGB-Wert in float.

## <a name="syntax"></a>Syntax

``` syntax
FLOAT D3DX_SRGB_to_FLOAT_inexact(
   hlsl_precise FLOAT val
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*ster* 
</dt> <dd>

Der zu konvertierende sRGB-Wert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der konvertierte sRGB-Wert.

## <a name="remarks"></a>Bemerkungen

Diese Funktion hat keine hohe Genauigkeit, um die genaue Antwort zu erhalten. Die Alternative Funktion [**D3DX \_ sRGB \_ to \_ float**](d3dx-srgb-to-float.md) verwendet eine Nachschlage Tabelle, um eine exakte sRGB-Konvertierung zu verwenden.

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

 

 





