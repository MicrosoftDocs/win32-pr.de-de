---
title: 'Inputpatch:: Operator-Funktion'
description: 'Gibt den n-ten Steuerungspunkt im Patch zurück. | Inputpatch:: Operator-Funktion'
ms.assetid: 2c1eda6b-a9c1-40d3-be91-7a2e8f1da9fc
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
ms.openlocfilehash: 5d95cb8adae6e7a91629614e0ae10b4161dbac3f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219218"
---
# <a name="inputpatchoperator--function"></a>Inputpatch:: Operator-Funktion

Gibt den *n*-<sup>ten Steuerungspunkt</sup> im Patch zurück.

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

Der Eingabe Index.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **T**

Der *n*-<sup>te Steuerungspunkt</sup> .

## <a name="remarks"></a>Bemerkungen

Diese Funktion wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Input Patch](sm5-object-inputpatch.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




