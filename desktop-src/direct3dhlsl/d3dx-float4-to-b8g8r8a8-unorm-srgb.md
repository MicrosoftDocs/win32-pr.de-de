---
title: D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB-Funktion
description: Packt das angegebene XMFLOAT4 in ein DXGI- \_ Format \_ B8G8R8A8 \_ unorm \_ sRGB uint.
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
ms.openlocfilehash: c20292e1038d31c6d853eb8ae62f7e764e722a6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219640"
---
# <a name="d3dx_float4_to_b8g8r8a8_unorm_srgb-function"></a>D3DX \_ float4 \_ to \_ B8G8R8A8 \_ unorm \_ sRGB-Funktion

Packt das angegebene XMFLOAT4 in ein DXGI- \_ Format \_ B8G8R8A8 \_ unorm \_ sRGB uint.

## <a name="syntax"></a>Syntax

``` syntax
UINT D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*unpackedinput* 
</dt> <dd>

Die entpackten Shader-Daten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die gepackten Shader-Daten.

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

 

 





