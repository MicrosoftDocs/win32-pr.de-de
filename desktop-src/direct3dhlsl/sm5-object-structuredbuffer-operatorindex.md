---
title: 'Structuredbuffer:: Operator-Funktion'
description: Gibt eine schreibgeschützte Ressourcen Variable eines structuredbuffer zurück.
ms.assetid: e2a1b0f7-f374-44a3-b567-8a2318e8b2b8
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
ms.openlocfilehash: 1f0d75bdfbcd3bfc560e896416f241f1291120d6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102718"
---
# <a name="structuredbufferoperator--function"></a>Structuredbuffer:: Operator-Funktion

Gibt eine schreibgeschützte Ressourcen Variable eines [**structuredbuffer**](sm5-object-structuredbuffer.md)zurück.

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

Eine schreibgeschützte Ressourcen Variable.

## <a name="remarks"></a>Bemerkungen

Diese Funktion wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Structuredbuffer](sm5-object-structuredbuffer.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




