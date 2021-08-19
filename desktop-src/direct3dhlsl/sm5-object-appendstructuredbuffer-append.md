---
title: AppendStructuredBuffer::Append-Funktion
description: Fügt einen Wert an das Ende des Puffers an.
ms.assetid: 667bc6dc-c0d0-419a-9227-99ce30b9cc73
keywords:
- Append-Funktion HLSL
topic_type:
- apiref
api_name:
- Append
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 863269c5127915af82b8ef82aa36b60b17941d8627b3f81a789f75618219c773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725394"
---
# <a name="append-function"></a>Append-Funktion

Fügt einen Wert an das Ende des Puffers an.

## <a name="syntax"></a>Syntax

``` syntax
void Append(
  in T value
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*wert* \[ In\]
</dt> <dd>

Typ: **T**

Der Eingabewert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Keine

## <a name="remarks"></a>Bemerkungen

T kann ein beliebiger Datentyp sein, einschließlich Strukturen.

Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[AppendStructuredBuffer](sm5-object-appendstructuredbuffer.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




