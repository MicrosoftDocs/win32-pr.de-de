---
title: D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact-Funktion
description: Entpackt DXGI- \_ Format \_ R8G8B8A8 \_ unorm \_ sRGB-Shader-Daten in eine XMFLOAT4. | D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact-Funktion
ms.assetid: ca7c2bf8-30fd-48fa-b4d9-e69c28c7f603
keywords:
- D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact-Funktion HLSL
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
ms.openlocfilehash: 74d3d4a9d47eb520d151fe2e3388e99f401fc0a4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961648"
---
# <a name="d3dx_r8g8b8a8_unorm_srgb_to_float4_inexact-function"></a>D3DX \_ R8G8B8A8 \_ unorm \_ sRGB \_ in \_ float4 \_ ungenau-Funktion

Entpackt DXGI- \_ Format \_ R8G8B8A8 \_ unorm \_ sRGB-Shader-Daten in eine XMFLOAT4.

## <a name="syntax"></a>Syntax

``` syntax
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact(
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

Diese Funktion verwendet shaderanweisungen, die keine hohe genug Genauigkeit aufweisen, um die genaue Antwort zu erhalten. Die Alternative Funktion [**D3DX \_ R8G8B8A8 \_ unorm \_ sRGB \_ to \_ float4**](d3dx-r8g8b8a8-unorm-srgb-to-float4.md) verwendet eine im Shader gespeicherte Such Tabelle, um eine exakte sRGB-Konvertierung für die Gleit Komma Zahl zu verwenden.

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

 

 





