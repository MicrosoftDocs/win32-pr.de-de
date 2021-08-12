---
title: D3DX_FLOAT4_to_R8G8B8A8_SNORM-Funktion
description: Packt die angegebene XMFLOAT4 wieder in ein DXGI \_ FORMAT \_ R8G8B8A8 \_ SNORM.
ms.assetid: 425aeabd-6249-4777-8935-827691abef24
keywords:
- D3DX_FLOAT4_to_R8G8B8A8_SNORM-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R8G8B8A8_SNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0382cc5e7bfc47b8046eec437cbc25cf559c9116b4e6215cce9a3fb8f344f059
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118286728"
---
# <a name="d3dx_float4_to_r8g8b8a8_snorm-function"></a>D3DX \_ FLOAT4 \_ zu \_ R8G8B8A8-SNORM-Funktion \_

Packt die angegebene XMFLOAT4 wieder in ein DXGI \_ FORMAT \_ R8G8B8A8 \_ SNORM.

## <a name="syntax"></a>Syntax

``` syntax
UINT D3DX_FLOAT4_to_R8G8B8A8_SNORM(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*unpackedInput* 
</dt> <dd>

Die zu packender Shaderdaten.

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

 

 





