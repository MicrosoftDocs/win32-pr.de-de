---
title: OutputPatch::Operator-Funktion
description: Gibt den n. Kontrollpunkt im Patch zurück. | OutputPatch::Operator-Funktion
ms.assetid: 3ac15fe8-8bab-46a2-8826-61ade927c99e
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
ms.openlocfilehash: 684925491ce7b5ac50cb293b3c8a0270557c9b9e65fcfcde63e9699127bc7ed0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023470"
---
# <a name="outputpatchoperator--function"></a>OutputPatch::Operator-Funktion

Gibt den<sup>n-th-Kontrollpunkt</sup> im Patch zurück. 

## <a name="syntax"></a>Syntax

``` syntax
T Operator[](
  in uint n
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*n* \[ in\]
</dt> <dd>

Typ: **uint**

Der Eingabeindex.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **T**

Der *n-te*<sup></sup> Kontrollpunkt.

## <a name="remarks"></a>Hinweise

Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        | x    | x      |          |       |         |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[OutputPatch](sm5-object-outputpatch.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




