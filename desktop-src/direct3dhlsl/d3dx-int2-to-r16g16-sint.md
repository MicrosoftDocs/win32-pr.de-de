---
title: D3DX_INT2_to_R16G16_SINT-Funktion
description: Packt den angegebenen XMINT2 zurück in ein DXGI- \_ Format \_ R16G16 \_ Sint.
ms.assetid: dc37e8a3-31d4-4af6-9bc3-9aa5062c066a
keywords:
- D3DX_INT2_to_R16G16_SINT-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_INT2_to_R16G16_SINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a97d60ba29b2451dea973b4ec0453f3a4df2ecdd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982532"
---
# <a name="d3dx_int2_to_r16g16_sint-function"></a>D3DX \_ int2 \_ to \_ R16G16 \_ Sint-Funktion

Packt den angegebenen XMINT2 zurück in ein DXGI- \_ Format \_ R16G16 \_ Sint.

## <a name="syntax"></a>Syntax

``` syntax
UINT D3DX_INT2_to_R16G16_SINT(
   hlsl_precise XMINT2 unpackedInput
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

 

 





