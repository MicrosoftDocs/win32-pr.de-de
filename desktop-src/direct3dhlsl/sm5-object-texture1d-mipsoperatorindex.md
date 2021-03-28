---
title: 'Texture1D:: MIPS. Operator-Funktion'
description: Gibt eine schreibgeschützte Ressourcen Variable oder ein Texture1D-Wert zurück.
ms.assetid: 0b64f0d3-f9a1-474b-b229-d91d18922d5c
keywords:
- MIPS. Operator Function HLSL
topic_type:
- apiref
api_name:
- mips.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4713fe20fa52e948113a220969229c413c5dc4d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340228"
---
# <a name="texture1dmipsoperator----function"></a>Texture1D:: MIPS. Operator-Funktion

Gibt eine schreibgeschützte Ressourcen Variable oder ein [**Texture1D**](sm5-object-texture1d.md)-Wert zurück.

## <a name="syntax"></a>Syntax

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint pos
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*mipslice* \[ in\]
</dt> <dd>

Typ: **uint**

Der MIP-Slice-Index.

</dd> <dt>

*POS* \[ in\]
</dt> <dd>

Typ: **uint**

Die Indexposition. Enthält die x-Koordinate.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **R**

Eine schreibgeschützte Ressourcen Variable.

## <a name="remarks"></a>Bemerkungen

### <a name="usage-example"></a>Verwendungsbeispiel


```
Texture1D<float4> tex;
uint mip = 2;
uint pos = 1234;
float4 f = tex.mips[mip][pos];
      
```



Diese Funktion wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Texture1D](sm5-object-texture1d.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




