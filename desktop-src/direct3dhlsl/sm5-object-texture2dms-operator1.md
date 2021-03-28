---
title: 'Texture2DMS:: Operator-Funktion'
description: Ruft einen Wert aus der Ressource an dem Speicherort ab, der im Beispiel Index 0 angegeben ist.
ms.assetid: 80380D3F-1E71-4C43-A17B-F94F6E5215B1
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
ms.openlocfilehash: 6ae7976e6871dc2547ed5c372e1551e5bf0ca148
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104976960"
---
# <a name="texture2dmsoperator--function"></a>Texture2DMS:: Operator-Funktion

Ruft einen Wert aus der Ressource an dem Speicherort ab, der im Beispiel Index 0 angegeben ist.

## <a name="syntax"></a>Syntax

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*POS* \[ in\]
</dt> <dd>

Typ: **uint2**

Die Indexposition. Enthält die (x, y)-Koordinaten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **R**

Eine schreibgeschützte Ressourcen Variable.

## <a name="remarks"></a>Bemerkungen

Informationen zum Auswählen eines bestimmten Beispiels finden Sie im [**Beispiel. \[Operator \] . \[ \]**](sm5-object-texture2dms-sampleoperatorindex.md)

Diese Funktion wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Texture2DMS](sm5-object-texture2dms.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




