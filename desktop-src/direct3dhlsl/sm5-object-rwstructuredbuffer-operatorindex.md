---
title: 'Rwstructuredbuffer:: Operator-Funktion'
description: 'Gibt eine Ressourcen Variable zurück. | Rwstructuredbuffer:: Operator-Funktion'
ms.assetid: e821b60e-38db-463f-b0c6-47f2a4c9ccee
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
ms.openlocfilehash: e915d7862f7994d3b438bf3255ee836ede4b3d7d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530632"
---
# <a name="rwstructuredbufferoperator--function"></a>Rwstructuredbuffer:: Operator-Funktion

Gibt eine Ressourcen Variable zurück.

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

Die Indexposition.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **R**

Eine Ressourcen Variable.

## <a name="remarks"></a>Bemerkungen

Eine strukturierte Ressource kann basierend auf den Komponentennamen der Strukturen weiter indiziert werden.

Diese Funktion wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Rwstructuredbuffer](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




