---
title: D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB-Funktion
description: Packt den angegebenen XMFLOAT4 in ein \_ DXGI-FORMAT \_ B8G8R8A8 \_ UNORM \_ SRGB UINT.
ms.assetid: 2fc36f19-44ce-43ba-9d9f-e8061f94a207
keywords:
- D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6661ea7bce5f5a10fec8c3d96bf178fc4e169ba53d013143b89c8114de71cc60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118286836"
---
# <a name="d3dx_float4_to_b8g8r8a8_unorm_srgb-function"></a>D3DX \_ FLOAT4 \_ bis \_ B8G8R8A8 \_ UNORM \_ SRGB-Funktion

Packt den angegebenen XMFLOAT4 in ein \_ DXGI-FORMAT \_ B8G8R8A8 \_ UNORM \_ SRGB UINT.

## <a name="syntax"></a>Syntax

``` syntax
UINT D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*unpackedInput* 
</dt> <dd>

Die entpackten Shaderdaten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die gepackten Shaderdaten.

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

 

 





