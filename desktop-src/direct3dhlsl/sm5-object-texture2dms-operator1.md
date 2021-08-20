---
title: Texture2DMS::Operator-Funktion
description: Ruft einen Wert aus der Ressource an dem am Beispielindex 0 angegebenen Speicherort ab.
ms.assetid: 80380D3F-1E71-4C43-A17B-F94F6E5215B1
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
ms.openlocfilehash: 67b10ee5c6a089fa78b75dab10dd90cae8fe2f417172df1936e4c1c4104a2b53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117905237"
---
# <a name="texture2dmsoperator--function"></a>Texture2DMS::Operator-Funktion

Ruft einen Wert aus der Ressource an dem am Beispielindex 0 angegebenen Speicherort ab.

## <a name="syntax"></a>Syntax

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*pos* \[ In\]
</dt> <dd>

Typ: **uint2**

Die Indexposition. Enthält die Koordinaten (x, y).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **R**

Eine schreibgeschützte Ressourcenvariable.

## <a name="remarks"></a>Hinweise

Informationen zum Auswählen eines bestimmten Beispiels finden Sie unter [**Beispiel. \[ \] Operator \[ \]**](sm5-object-texture2dms-sampleoperatorindex.md).

Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Texture2DMS](sm5-object-texture2dms.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




