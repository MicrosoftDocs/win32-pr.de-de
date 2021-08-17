---
title: D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact-Funktion
description: Entpackt DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM \_ SRGB-Shaderdaten in ein XMFLOAT3. | D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact-Funktion
ms.assetid: caa64f89-7b9e-4bc0-82dc-31edfd31d495
keywords:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact HlSL-Funktion
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
ms.openlocfilehash: f696381402d8ad42c92310029631e66b457e3b211d22d8f9de3dd98c1f1312ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986870"
---
# <a name="d3dx_b8g8r8x8_unorm_srgb_to_float3_inexact-function"></a>Ungenaue Funktion "D3DX \_ B8G8R8X8 \_ UNORM \_ SRGB \_ to \_ \_ FLOAT3"

Entpackt DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM \_ SRGB-Shaderdaten in ein XMFLOAT3.

## <a name="syntax"></a>Syntax

``` syntax
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact(
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

Diese Funktion verwendet Shaderanweisungen, die nicht über eine ausreichende Genauigkeit verfügen, um die genaue Antwort zu geben. Die alternative Funktion [**D3DX \_ B8G8R8X8 \_ UNORM \_ SRGB \_ in \_ FLOAT3**](d3dx-b8g8r8x8-unorm-srgb-to-float3.md) verwendet eine im Shader gespeicherte Nachschlagetabelle, um eine genaue Konvertierung von SRGB in Float zu ermöglichen.

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

 

 





