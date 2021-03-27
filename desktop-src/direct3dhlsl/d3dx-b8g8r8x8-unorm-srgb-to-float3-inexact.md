---
title: D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact-Funktion
description: Entpackt DXGI- \_ Format \_ B8G8R8X8 \_ unorm \_ sRGB-Shader-Daten in eine XMFLOAT3. | D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact-Funktion
ms.assetid: caa64f89-7b9e-4bc0-82dc-31edfd31d495
keywords:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ef3f0b97ee3d5e21fef7b0227304fc5b187df2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982113"
---
# <a name="d3dx_b8g8r8x8_unorm_srgb_to_float3_inexact-function"></a>D3DX \_ B8G8R8X8 \_ unorm \_ sRGB \_ in \_ FLOAT3 \_ ungenau-Funktion

Entpackt DXGI- \_ Format \_ B8G8R8X8 \_ unorm \_ sRGB-Shader-Daten in eine XMFLOAT3.

## <a name="syntax"></a>Syntax

``` syntax
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact(
   UINT packedInput
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*packedinput* 
</dt> <dd>

Die gepackten Shader-Daten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die entpackten Shader-Daten.

## <a name="remarks"></a>Bemerkungen

Diese Funktion verwendet shaderanweisungen, die keine hohe genug Genauigkeit aufweisen, um die genaue Antwort zu erhalten. Die Alternative Funktion [**D3DX \_ B8G8R8X8 \_ unorm \_ sRGB \_ to \_ FLOAT3**](d3dx-b8g8r8x8-unorm-srgb-to-float3.md) verwendet eine im Shader gespeicherte Such Tabelle, um eine exakte sRGB-Konvertierung für die Gleit Komma Zahl zu verwenden.

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

 

 





