---
title: InterlockedOr-Funktion (HLSL-Referenz)
description: Führt einen garantierten atomaren oder aus.
ms.assetid: ecbe6b2f-8eff-41d7-9ca3-4487c9ffeaf6
keywords:
- InterlockedOr-Funktion HLSL
topic_type:
- apiref
api_name:
- InterlockedOr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c426237ec112a08fb7d422181a0efcd9ec0277d0628eda780492dae568ffaf38
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854250"
---
# <a name="interlockedor-function-hlsl-reference"></a>InterlockedOr-Funktion (HLSL-Referenz)

Führt einen garantierten atomaren oder aus.

## <a name="syntax"></a>Syntax

``` syntax
void InterlockedOr(
  in  R dest,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*dest* \[ In\]
</dt> <dd>

Typ: **R**

Die Zieladresse.

</dd> <dt>

*wert* \[ In\]
</dt> <dd>

Typ: **T**

Der Eingabewert.

</dd> <dt>

*Ursprünglicher \_ Wert* \[ out\]
</dt> <dd>

Typ: **T**

Optional. Der ursprüngliche Eingabewert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Dieser Vorgang kann nur für int- oder uint-typisierte Ressourcen und Freigegebene Speichervariablen ausgeführt werden. Es gibt zwei mögliche Verwendungsmöglichkeiten für diese Funktion. Die erste ist, wenn R ein Variablentyp für gemeinsam genutzten Arbeitsspeicher ist. In diesem Fall führt die Funktion eine atomare oder einen Wert für das Shared Memory-Register aus, auf das vom Dest verwiesen wird. Das zweite Szenario ist, wenn R ein Ressourcenvariablentyp ist. In diesem Szenario führt die Funktion einen atomaren oder einen Wert für den Ressourcenspeicherort aus, auf den vom Dest verwiesen wird. Die überladene Funktion verfügt über eine zusätzliche Ausgabevariable, die auf den ursprünglichen Wert dest festgelegt wird. Dieser überladene Vorgang ist nur verfügbar, wenn R lesbar und beschreibbar ist.

### <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höhere Shadermodelle | Ja       |



 

Diese Funktion wird in den folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      |  x   |  x     |  x       | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Systeminterne Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




