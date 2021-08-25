---
title: mad-Funktion
description: Führt eine arithmetische Multiplikations-/Add-Operation für drei Werte aus.
ms.assetid: 2e58229d-2387-4319-adc6-2d66eda88bd1
keywords:
- mad-Funktion HLSL
topic_type:
- apiref
api_name:
- mad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 52e0e4819e4c78f092ee99c78403ace5d0205037db3096dfe45865c2216d486d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788820"
---
# <a name="mad-function"></a>mad-Funktion

Führt eine arithmetische Multiplikations-/Add-Operation für drei Werte aus.

## <a name="syntax"></a>Syntax

``` syntax
numeric mad(
  in numeric mvalue,
  in numeric avalue,
  in numeric bvalue
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*mvalue* \[ In\]
</dt> <dd>

Typ: **numerisch**

Der Multiplikationswert.

</dd> <dt>

*avalue* \[ In\]
</dt> <dd>

Typ: **numerisch**

Der erste Additionswert.

</dd> <dt>

*bvalue* \[ In\]
</dt> <dd>

Typ: **numerisch**

Der zweite Additionswert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **numerisch**

Das Ergebnis von *mvalue* \* *avalue*  +  *bvalue*.

## <a name="remarks"></a>Hinweise

### <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höhere Shadermodelle | Ja       |



 

Diese Funktion wird in den folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

Shaderautoren können mithilfe der instrinsischen Instrinsik explizit auf die **unbrauchbare** Hardwareanweisung in der kompilierten Shaderausgabe abzielen. Dies ist besonders nützlich bei Shadern, die Ergebnisse mit dem [schlüsselwort precise](dx-graphics-hlsl-appendix-keywords.md) markieren.  Die **tollsinnige** Anweisung kann in der Hardware entweder als "fused" implementiert werden, was eine höhere Genauigkeit als die Implementierung einer **mul-Anweisung** gefolgt von einer **add-Anweisung** bietet, oder als **ein mul**  +  **add**.

Wenn Shaderautoren  die instrinsische Farbe verwenden, um ein Ergebnis zu berechnen, das der Shader als präzise markiert hat, geben sie der Hardware an, eine gültige Implementierung der **irrsinnigen** Anweisung zu verwenden (fused oder nicht), solange die Implementierung für alle Verwendungen dieser intrinsischen **Intrinsik** in einem Shader auf dieser Hardware konsistent ist. Shader können dann die Vorteile potenzieller Leistungsverbesserungen nutzen, indem sie eine native **tollanweisung** (im Gegensatz zu **mul**  +  **add**) auf einigen Hardwarekomponenten verwenden. Das Ergebnis der Ausführung einer nativen **rauschenden** Hardwareanweisung unterscheidet sich möglicherweise von der Ausführung eines **Muls** gefolgt von einer **add -Anweisung.** Unabhängig vom Ergebnis muss das Ergebnis jedoch konsistent sein, damit der gleiche Vorgang in mehreren Shadern oder verschiedenen Teilen eines Shaders ausgeführt wird.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Systeminterne Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




