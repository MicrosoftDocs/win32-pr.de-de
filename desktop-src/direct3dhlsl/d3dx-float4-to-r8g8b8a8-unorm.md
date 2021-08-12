---
title: D3DX_FLOAT4_to_R8G8B8A8_UNORM-Funktion
description: Entpackt DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM-Shaderdaten in XMFLOAT4. | D3DX_FLOAT4_to_R8G8B8A8_UNORM-Funktion
ms.assetid: c589c1e5-24ee-4fd7-b18d-5ede52f9f05d
keywords:
- D3DX_FLOAT4_to_R8G8B8A8_UNORM-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R8G8B8A8_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b21f753c2f08294c2f82bdbfc12bfad5de618d89817bca279fa4b7d3d4578c20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118286630"
---
# <a name="d3dx_float4_to_r8g8b8a8_unorm-function"></a>D3DX \_ FLOAT4 \_ bis \_ R8G8B8A8 \_ UNORM-Funktion

Entpackt DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM-Shaderdaten in XMFLOAT4.

## <a name="syntax"></a>Syntax

``` syntax
XMFLOAT4 D3DX_FLOAT4_to_R8G8B8A8_UNORM(
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

[Entpacken und Packen des \_ DXGI-FORMATS für In-Place Bildbearbeitung](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





