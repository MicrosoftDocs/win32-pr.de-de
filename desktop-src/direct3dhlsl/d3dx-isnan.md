---
title: D3DX_IsNan-Funktion
description: Bestimmt, ob der Wert ein NaN (Not a Number) ist.
ms.assetid: 862d1d34-36ab-471e-b3ce-ce71896441e5
keywords:
- D3DX_IsNan HlSL-Funktion
topic_type:
- apiref
api_name:
- D3DX_IsNan
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b8851fb216bf400971a281fb589b92205014e006651d4fc89592d98f5c93916
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793749"
---
# <a name="d3dx_isnan-function"></a>\_D3DX-IsNan-Funktion

Bestimmt, ob der Wert ein NaN (Not a Number) ist.

## <a name="syntax"></a>Syntax

``` syntax
bool D3DX_IsNan(
   FLOAT _V
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*\_V* 
</dt> <dd>

Der angegebene Wert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

TRUE, wenn ein NaN; andernfalls FALSE.

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

 

 





