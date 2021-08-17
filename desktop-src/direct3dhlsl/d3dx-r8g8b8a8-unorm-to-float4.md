---
title: D3DX_R8G8B8A8_UNORM_to_FLOAT4-Funktion
description: Entpackt DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM-Shaderdaten in XMFLOAT4. | D3DX_R8G8B8A8_UNORM_to_FLOAT4-Funktion
ms.assetid: 94430f29-4872-4ecd-99b9-72f3b77c47f2
keywords:
- D3DX_R8G8B8A8_UNORM_to_FLOAT4-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_UNORM_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e366478c12fdab5072a514b4ffea967b9a2b272c98e392fc4b7476ba81bc4efa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793456"
---
# <a name="d3dx_r8g8b8a8_unorm_to_float4-function"></a>D3DX \_ R8G8B8A8 \_ UNORM \_ zu \_ FLOAT4-Funktion

Entpackt DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM-Shaderdaten in XMFLOAT4.

## <a name="syntax"></a>Syntax

``` syntax
XMFLOAT4 D3DX_R8G8B8A8_UNORM_to_FLOAT4(
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

 

 





