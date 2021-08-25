---
title: D3DX_INT_to_FLOAT-Funktion
description: Konvertiert einen INT-Wert in FLOAT.
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
ms.openlocfilehash: 97d49320c2b7bfd53b2fa4e0303a7d2e9bf6c22427557ee3827aed31f5915d1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855490"
---
# <a name="d3dx_int_to_float-function"></a>D3DX \_ INT \_ zu \_ FLOAT-Funktion

Konvertiert einen INT-Wert in FLOAT.

## <a name="syntax"></a>Syntax

``` syntax
FLOAT D3DX_INT_to_FLOAT(
   INT _V,
   FLOAT _Scale
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*\_V* 
</dt> <dd>

Der v-Wert.

</dd> <dt>

*\_Skalieren* 
</dt> <dd>

Der Skalierungswert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der konvertierte int-Wert.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert.inl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Funktionen](format-conversion-functions.md)
</dt> <dt>

[Entpacken und Packen des \_ DXGI-FORMATS für In-Place Bildbearbeitung](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





