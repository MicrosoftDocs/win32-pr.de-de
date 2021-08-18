---
title: InputPatch::Operator-Funktion
description: Gibt den n-ten Steuerungspunkt im Patch zurück. | InputPatch::Operator-Funktion
ms.assetid: 2c1eda6b-a9c1-40d3-be91-7a2e8f1da9fc
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
ms.openlocfilehash: 81c768d138f6ee1853f9930a56f1a1864b468e8be9ff421f4dba1698b790053c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986030"
---
# <a name="inputpatchoperator--function"></a>InputPatch::Operator-Funktion

Gibt den *n-ten*<sup></sup> Steuerungspunkt im Patch zurück.

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

Der *n-ten*<sup></sup> Kontrollpunkt.

## <a name="remarks"></a>Hinweise

Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[InputPatch](sm5-object-inputpatch.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




