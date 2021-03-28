---
title: Interlockedor-Funktion (HLSL-Referenz)
description: Führt eine garantierte atomarische or-Ausführung aus.
ms.assetid: ecbe6b2f-8eff-41d7-9ca3-4487c9ffeaf6
keywords:
- Interlockedor-Funktion HLSL
topic_type:
- apiref
api_name:
- InterlockedOr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 36ab900416d6d04e0e47a843aa345c1a01318c50
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2020
ms.locfileid: "104993327"
---
# <a name="interlockedor-function-hlsl-reference"></a>Interlockedor-Funktion (HLSL-Referenz)

Führt eine garantierte atomarische or-Ausführung aus.

## <a name="syntax"></a>Syntax

``` syntax
void InterlockedOr(
  in  R dest,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*dest* \[ in\]
</dt> <dd>

Typ: **R**

Die Zieladresse.

</dd> <dt>

*Wert* \[ in\]
</dt> <dd>

Typ: **T**

Der Eingabewert.

</dd> <dt>

*ursprünglicher \_ Wert* ausgehend \[\]
</dt> <dd>

Typ: **T**

Optional. Der ursprüngliche Eingabe Wert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Dieser Vorgang kann nur für typisierte int-oder uint-Ressourcen und Shared Memory-Variablen ausgeführt werden. Es gibt zwei Verwendungsmöglichkeiten für diese Funktion. Der erste ist, wenn R ein Variablentyp für den gemeinsamen Speicher ist. In diesem Fall führt die Funktion eine atomarische or-Werte für das Shared Memory-Register aus, auf das von dest verwiesen wird. Das zweite Szenario ist, wenn R ein Ressourcen Variablentyp ist. In diesem Szenario führt die Funktion eine atomarische or-Werte für den Ressourcen Speicherort aus, auf den "dest" verweist. Die überladene Funktion verfügt über eine zusätzliche Ausgabevariable, die auf den ursprünglichen Wert von dest festgelegt wird. Dieser überladene Vorgang ist nur verfügbar, wenn R lesbar und beschreibbar ist.

### <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle | ja       |



 

Diese Funktion wird in den folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      |  x   |  x     |  x       | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Intrinsische Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




