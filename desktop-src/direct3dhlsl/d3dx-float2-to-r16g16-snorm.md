---
title: D3DX_FLOAT2_to_R16G16_SNORM-Funktion
description: Packt den angegebenen XMFLOAT2 zurück in ein DXGI- \_ Format \_ R16G16 \_ snorm.
ms.assetid: 7c5c6aae-b750-435a-9582-18b7689bc2d9
keywords:
- D3DX_FLOAT2_to_R16G16_SNORM-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT2_to_R16G16_SNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba63d7d7f03988e416d06b645e5c15163e431a7e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961636"
---
# <a name="d3dx_float2_to_r16g16_snorm-function"></a>D3DX \_ FLOAT2 \_ to \_ R16G16 \_ snorm-Funktion

Packt den angegebenen XMFLOAT2 zurück in ein DXGI- \_ Format \_ R16G16 \_ snorm.

## <a name="syntax"></a>Syntax

``` syntax
UINT D3DX_FLOAT2_to_R16G16_SNORM(
   hlsl_precise XMFLOAT2 unpackedInput
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

 

 





