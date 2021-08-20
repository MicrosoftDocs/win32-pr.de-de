---
title: D3DX_FLOAT3_to_B8G8R8X8_UNORM-Funktion
description: Packt das angegebene XMFLOAT3 in ein DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM UINT.
ms.assetid: 9492578b-e3c3-4856-b6d2-49f776a21d77
keywords:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM HlSL-Funktion
topic_type:
- apiref
api_name:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee8da37854e78abb09e8d6781453d47cf3abed43847a96fe09b7d637e52ca429
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516378"
---
# <a name="d3dx_float3_to_b8g8r8x8_unorm-function"></a>UNORM-Funktion "D3DX \_ \_ FLOAT3" zu \_ "B8G8R8X8X8" \_

Packt das angegebene XMFLOAT3 in ein DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM UINT.

## <a name="syntax"></a>Syntax

``` syntax
UINT D3DX_FLOAT3_to_B8G8R8X8_UNORM(
   hlsl_precise XMFLOAT3 unpackedInput
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

[Entpacken und Packen von DXGI \_ FORMAT für In-Place Bildbearbeitung](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





