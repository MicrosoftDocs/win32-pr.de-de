---
title: D3DX_UINT4_to_R8G8B8A8_UINT-Funktion
description: Packt den angegebenen XMUINT4 wieder in ein DXGI \_ FORMAT \_ R8G8B8A8 \_ UINT.
ms.assetid: d4770dfc-1387-40c3-a4f8-365a1421fa3c
keywords:
- D3DX_UINT4_to_R8G8B8A8_UINT-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_UINT4_to_R8G8B8A8_UINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c2185a28e094af06a25581152b9620e21446e614ed7b187bf2365fc912078ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117727274"
---
# <a name="d3dx_uint4_to_r8g8b8a8_uint-function"></a>D3DX \_ UINT4 \_ zu \_ R8G8B8A8 \_ UINT-Funktion

Packt den angegebenen XMUINT4 wieder in ein DXGI \_ FORMAT \_ R8G8B8A8 \_ UINT.

## <a name="syntax"></a>Syntax

``` syntax
UINT D3DX_UINT4_to_R8G8B8A8_UINT(
   hlsl_precise XMUINT4 unpackedInput
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

 

 





