---
title: StructuredBuffer::Operator-Funktion
description: Gibt eine schreibgeschützte Ressourcenvariable eines StructuredBuffer zurück.
ms.assetid: e2a1b0f7-f374-44a3-b567-8a2318e8b2b8
keywords:
- Operatorfunktion HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c852a56769df2179daf6055542c9ebf4724a353312e295daecd59af08163711c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118509116"
---
# <a name="structuredbufferoperator--function"></a>StructuredBuffer::Operator-Funktion

Gibt eine schreibgeschützte Ressourcenvariable eines [**StructuredBuffer-Werts zurück.**](sm5-object-structuredbuffer.md)

## <a name="syntax"></a>Syntax

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*pos* \[ In\]
</dt> <dd>

Typ: **uint**

Die Indexposition.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **R**

Eine schreibgeschützte Ressourcenvariable.

## <a name="remarks"></a>Hinweise

Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[StructuredBuffer](sm5-object-structuredbuffer.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




