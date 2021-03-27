---
title: D3DX_FLOAT4_to_R10G10B10A2_UNORM-Funktion
description: Packt den angegebenen XMFLOAT4 zurück in ein DXGI- \_ Format \_ R10G10B10A2 \_ unorm.
ms.assetid: 20471435-bb1a-4151-a03a-c334b2a7d944
keywords:
- D3DX_FLOAT4_to_R10G10B10A2_UNORM-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R10G10B10A2_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b2c8d80b8822d03a43e813226c28dde8693397a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982089"
---
# <a name="d3dx_float4_to_r10g10b10a2_unorm-function"></a>D3DX \_ float4 \_ to \_ R10G10B10A2 \_ unorm-Funktion

Packt den angegebenen XMFLOAT4 zurück in ein DXGI- \_ Format \_ R10G10B10A2 \_ unorm.

## <a name="syntax"></a>Syntax

``` syntax
UINT D3DX_FLOAT4_to_R10G10B10A2_UNORM(
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

 

 





