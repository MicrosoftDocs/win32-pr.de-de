---
title: 'Texture1D:: Operator-Funktion'
description: Gibt eine schreibgeschützte Ressourcen Variable für ein Texture1D-Wert zurück.
ms.assetid: df54097d-4d1b-496a-a17d-6e9a10cfb996
keywords:
- Operator Function HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 44e5b502c7ae8b766363956920d7922858b4d771
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102715"
---
# <a name="texture1doperator--function"></a>Texture1D:: Operator-Funktion

Gibt eine schreibgeschützte Ressourcen Variable für ein [**Texture1D**](sm5-object-texture1d.md)-Wert zurück.

## <a name="syntax"></a>Syntax

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*POS* \[ in\]
</dt> <dd>

Typ: **uint**

Die Indexposition. Enthält die x-Koordinate.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **R**

Eine schreibgeschützte Ressourcen Variable.

## <a name="remarks"></a>Bemerkungen

Diese Methode greift immer auf die erste MIP-Ebene zu. Um andere MIP-Ebenen anzugeben, verwenden Sie stattdessen den [**\[ \] \[ \] MIP.-Operator**](sm5-object-texture1d-mipsoperatorindex.md) .

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

 

 




