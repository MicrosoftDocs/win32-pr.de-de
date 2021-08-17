---
title: D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact-Funktion
description: Entpackt DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM \_ SRGB-Shaderdaten in XMFLOAT4. | D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact-Funktion
ms.assetid: ca7c2bf8-30fd-48fa-b4d9-e69c28c7f603
keywords:
- D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact HlSL-Funktion
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ede0d10bd8c90514771fa6520eb41e0bd555a3d969b230bb2932665ec0c81796
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117727345"
---
# <a name="d3dx_r8g8b8a8_unorm_srgb_to_float4_inexact-function"></a>D3DX \_ R8G8B8A8 \_ UNORM \_ SRGB \_ to \_ FLOAT4 \_ inexact function (Ungenaue Funktion von D3DX R8G8B8A8 UNORM SRGB zu FLOAT4)

Entpackt DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM \_ SRGB-Shaderdaten in XMFLOAT4.

## <a name="syntax"></a>Syntax

``` syntax
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact(
   UINT packedInput
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*packedInput* 
</dt> <dd>

Die gepackten Shaderdaten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die entpackten Shaderdaten.

## <a name="remarks"></a>Hinweise

Diese Funktion verwendet Shaderanweisungen, die nicht über eine ausreichende Genauigkeit verfügen, um die genaue Antwort zu geben. Die alternative Funktion [**D3DX \_ R8G8B8A8 \_ UNORM \_ SRGB \_ in \_ FLOAT4**](d3dx-r8g8b8a8-unorm-srgb-to-float4.md) verwendet eine im Shader gespeicherte Suchtabelle, um eine genaue Konvertierung von SRGB in float zu ermöglichen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert.inl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Funktionen](format-conversion-functions.md)
</dt> <dt>

[Entpacken und Packen von DXGI \_ FORMAT für In-Place Bildbearbeitung](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





