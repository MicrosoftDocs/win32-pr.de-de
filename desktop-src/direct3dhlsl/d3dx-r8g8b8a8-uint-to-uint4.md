---
title: D3DX_R8G8B8A8_UINT_to_UINT4-Funktion
description: Entpackt das DXGI- \_ Format \_ R8G8B8A8 \_ uint-Shader-Daten in eine XMUINT4.
ms.assetid: fe25041f-db18-4555-a77a-e8d487143aa6
keywords:
- D3DX_R8G8B8A8_UINT_to_UINT4-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_UINT_to_UINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a371a36e797e1bff17aff457e11b140e4775894
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982210"
---
# <a name="d3dx_r8g8b8a8_uint_to_uint4-function"></a>D3DX \_ R8G8B8A8 \_ uint \_ to \_ UINT4-Funktion

Entpackt das DXGI- \_ Format \_ R8G8B8A8 \_ uint-Shader-Daten in eine XMUINT4.

## <a name="syntax"></a>Syntax

``` syntax
XMUINT4 D3DX_R8G8B8A8_UINT_to_UINT4(
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

 

 





