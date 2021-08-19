---
title: D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4-Funktion
description: Entpackt DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM \_ SRGB-Shaderdaten in XMFLOAT4. | D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4-Funktion
ms.assetid: 67ad1768-aeb9-4c01-ae3e-0cd79476a459
keywords:
- D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4 HlSL-Funktion
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf2775c73d60317aa1e0892f16903ddf3270c99def0fe0a55b750079a2c7c3c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986850"
---
# <a name="d3dx_r8g8b8a8_unorm_srgb_to_float4-function"></a>D3DX \_ R8G8B8A8 \_ UNORM \_ SRGB \_ zu \_ FLOAT4-Funktion

Entpackt DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM \_ SRGB-Shaderdaten in XMFLOAT4.

## <a name="syntax"></a>Syntax

``` syntax
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4(
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

 

 





