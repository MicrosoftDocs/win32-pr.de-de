---
title: D3DX_B8G8R8A8_UNORM_to_FLOAT4-Funktion
description: Entpackt DXGI- \_ Format \_ B8G8R8A8 \_ unorm-Shader-Daten in eine XMFLOAT4.
ms.assetid: 1a52058c-825d-4607-b67d-8226dccdee54
keywords:
- D3DX_B8G8R8A8_UNORM_to_FLOAT4-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8A8_UNORM_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6bca17f350d40b1f74884232da9d1250bdb0abd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982114"
---
# <a name="d3dx_b8g8r8a8_unorm_to_float4-function"></a>D3DX \_ B8G8R8A8 \_ unorm \_ to \_ float4-Funktion

Entpackt DXGI- \_ Format \_ B8G8R8A8 \_ unorm-Shader-Daten in eine XMFLOAT4.

## <a name="syntax"></a>Syntax

``` syntax
XMFLOAT4 D3DX_B8G8R8A8_UNORM_to_FLOAT4(
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

 

 





