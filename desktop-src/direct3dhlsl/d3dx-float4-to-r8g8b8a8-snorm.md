---
title: D3DX_FLOAT4_to_R8G8B8A8_SNORM-Funktion
description: Packt den angegebenen XMFLOAT4 zurück in ein DXGI- \_ Format \_ R8G8B8A8 \_ snorm.
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
ms.openlocfilehash: 194835ef126a3441dc2b842784dfa841ae1d7d6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355777"
---
# <a name="d3dx_float4_to_r8g8b8a8_snorm-function"></a>D3DX \_ float4 \_ to \_ R8G8B8A8 \_ snorm-Funktion

Packt den angegebenen XMFLOAT4 zurück in ein DXGI- \_ Format \_ R8G8B8A8 \_ snorm.

## <a name="syntax"></a>Syntax

``` syntax
UINT D3DX_FLOAT4_to_R8G8B8A8_SNORM(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*unpackedinput* 
</dt> <dd>

Die zu Packungs-Shader-Daten.

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

 

 





