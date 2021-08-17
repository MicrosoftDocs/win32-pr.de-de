---
title: D3DX_INT4_to_R8G8B8A8_SINT-Funktion
description: Packt den angegebenen XMINT4 wieder in ein DXGI \_ FORMAT \_ R8G8B8A8 \_ SINT.
ms.assetid: ab9c5454-1673-43a9-ab76-bcd7b510b9a8
keywords:
- D3DX_INT4_to_R8G8B8A8_SINT-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_INT4_to_R8G8B8A8_SINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdeb7a92bff374d7b93d647971afd52746fbb768d9a33ec7c3a5c33b1c493523
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118515864"
---
# <a name="d3dx_int4_to_r8g8b8a8_sint-function"></a>D3DX \_ INT4 \_ bis \_ R8G8B8A8 \_ SINT-Funktion

Packt den angegebenen XMINT4 wieder in ein DXGI \_ FORMAT \_ R8G8B8A8 \_ SINT.

## <a name="syntax"></a>Syntax

``` syntax
UINT D3DX_INT4_to_R8G8B8A8_SINT(
   hlsl_precise XMINT4 unpackedInput
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*unpackedInput* 
</dt> <dd>

Die zu packenden Shaderdaten.

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

[Entpacken und Packen des \_ DXGI-FORMATS für In-Place Bildbearbeitung](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





