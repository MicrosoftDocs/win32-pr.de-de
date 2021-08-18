---
title: RWStructuredBuffer::Operator-Funktion
description: Gibt eine Ressourcenvariable zurück. | RWStructuredBuffer::Operator-Funktion
ms.assetid: e821b60e-38db-463f-b0c6-47f2a4c9ccee
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
ms.openlocfilehash: ad2e8085a52a920f7fe87a2820398877167a137c14c4ebe39bacd71ae2ba0324
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118509319"
---
# <a name="rwstructuredbufferoperator--function"></a>RWStructuredBuffer::Operator-Funktion

Gibt eine Ressourcenvariable zurück.

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

Eine Ressourcenvariable.

## <a name="remarks"></a>Hinweise

Eine strukturierte Ressource kann basierend auf den Komponentennamen der Strukturen weiter indiziert werden.

Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[RWStructuredBuffer](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




