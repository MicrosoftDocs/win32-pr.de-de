---
title: D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact-Funktion
description: Entpackt DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM \_ SRGB-Shaderdaten in XMFLOAT4. | D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact-Funktion
ms.assetid: f709267f-8dcd-47c8-b4cf-3cc903a08c35
keywords:
- D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact HlSL-Funktion
topic_type:
- apiref
api_name:
- D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b6fc32a06ff436046de76e212ef8f90a06338a55caa285865f12c98d6d4b068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793884"
---
# <a name="d3dx_b8g8r8a8_unorm_srgb_to_float4_inexact-function"></a>Ungenaue Funktion "D3DX \_ B8G8R8A8 \_ UNORM \_ SRGB \_ to \_ \_ FLOAT4"

Entpackt DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM \_ SRGB-Shaderdaten in XMFLOAT4.

## <a name="syntax"></a>Syntax

``` syntax
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact(
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

Diese Funktion verwendet Shaderanweisungen, die nicht über eine ausreichende Genauigkeit verfügen, um die genaue Antwort zu geben. Die alternative Funktion [**D3DX \_ B8G8R8A8 \_ UNORM \_ SRGB \_ in \_ FLOAT4**](d3dx-r10g10b10a2-unorm-to-float4.md) verwendet eine im Shader gespeicherte Suchtabelle, um eine genaue Konvertierung von SRGB in Float zu ermöglichen.

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

 

 





