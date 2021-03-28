---
title: D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3-Funktion
description: Entpackt DXGI- \_ Format \_ B8G8R8X8 \_ unorm \_ sRGB-Shader-Daten in eine XMFLOAT3. | D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3-Funktion
ms.assetid: 9b3c511c-95c2-454c-95b9-ff6ab0920466
keywords:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 277f10bc574e03a7bd608a333cba65f95a3e0b43
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995799"
---
# <a name="d3dx_b8g8r8x8_unorm_srgb_to_float3-function"></a>D3DX \_ B8G8R8X8 \_ unorm \_ sRGB \_ in die \_ FLOAT3-Funktion

Entpackt DXGI- \_ Format \_ B8G8R8X8 \_ unorm \_ sRGB-Shader-Daten in eine XMFLOAT3.

## <a name="syntax"></a>Syntax

``` syntax
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3(
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

 

 





