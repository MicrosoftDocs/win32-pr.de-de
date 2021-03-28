---
title: D3DX_INT_to_FLOAT-Funktion
description: Konvertiert einen int-Wert in float.
ms.assetid: bee2fb3e-ffde-4013-a321-275d6beb5f77
keywords:
- D3DX_INT_to_FLOAT-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_INT_to_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06a4d588661b1b2f5ddc14c7564699c7d2b47b4e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982500"
---
# <a name="d3dx_int_to_float-function"></a>D3DX \_ int \_ to \_ float-Funktion

Konvertiert einen int-Wert in float.

## <a name="syntax"></a>Syntax

``` syntax
FLOAT D3DX_INT_to_FLOAT(
   INT _V,
   FLOAT _Scale
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*\_Ramelow* 
</dt> <dd>

Der v-Wert.

</dd> <dt>

*\_Skalieren* 
</dt> <dd>

Der Skalierungs Wert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der konvertierte int-Wert.

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

 

 





