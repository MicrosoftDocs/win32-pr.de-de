---
title: mad-Funktion
description: Führt eine arithmetische Multiplikation/Add-Operation für drei Werte aus.
ms.assetid: 2e58229d-2387-4319-adc6-2d66eda88bd1
keywords:
- Mad-Funktion HLSL
topic_type:
- apiref
api_name:
- mad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 208b1bbc87c430ca5a58a70fb3c86f9edae762bf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104472005"
---
# <a name="mad-function"></a>mad-Funktion

Führt eine arithmetische Multiplikation/Add-Operation für drei Werte aus.

## <a name="syntax"></a>Syntax

``` syntax
numeric mad(
  in numeric mvalue,
  in numeric avalue,
  in numeric bvalue
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*mValue* \[ in\]
</dt> <dd>

Typ: **numerisch**

Der Multiplikations Wert.

</dd> <dt>

*verfügbar* \[ in\]
</dt> <dd>

Typ: **numerisch**

Der erste Additions Wert.

</dd> <dt>

*bvalue* \[ in\]
</dt> <dd>

Typ: **numerisch**

Der zweite Additions Wert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **numerisch**

Das Ergebnis des *mValue* -Werts für den \*   +  *bvalue*.

## <a name="remarks"></a>Bemerkungen

### <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle | ja       |



 

Diese Funktion wird in den folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

Shaderautoren können **die Mad-Hardware Anweisung** in der kompilierten Shader-Ausgabe mit dem **Mad** instrauc explizit als Ziel verwenden. Dies ist besonders nützlich für Shader, die Ergebnisse mit dem Schlüsselwort " [präzise](dx-graphics-hlsl-appendix-keywords.md) " markieren. Die **Mad** -Anweisung kann in Hardware als "Fused" implementiert werden, was eine höhere Genauigkeit als die Implementierung einer **mul** -Anweisung, gefolgt von einer **Add** -Anweisung oder als **mul**-  +  **Add**, bietet.

Wenn shaderautoren den **Mad** instrauc verwenden, um ein Ergebnis zu berechnen, das der Shader als genau gekennzeichnet hat, geben Sie der Hardware an, dass eine beliebige gültige Implementierung der **Mad** -Anweisung verwendet werden soll ("Fused" oder "Not"), solange die Implementierung für alle Verwendungen dieses **verrückten** in jedem Shader auf dieser Hardware konsistent ist. Shader können dann potenzielle Leistungsverbesserungen nutzen, indem Sie eine native **Mad** -Anweisung (im Gegensatz zu **mul**  +  **Add**) auf Hardware anwenden. Das Ergebnis der Ausführung einer systemeigenen **Mad** -Hardware Anweisung unterscheidet sich möglicherweise von der Durchführung einer **mul** , gefolgt von einem **Add**-in. Allerdings muss das Ergebnis, was das Ergebnis ist, konsistent sein, damit derselbe Vorgang in mehreren Shader oder unterschiedlichen Teilen eines Shader erfolgt.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Intrinsische Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




