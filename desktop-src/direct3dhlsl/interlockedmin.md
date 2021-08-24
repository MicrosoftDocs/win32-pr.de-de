---
title: InterlockedMin-Funktion (HLSL-Referenz)
description: Führt eine garantierte atomare Min. aus.
ms.assetid: a6d3d81c-45d7-4e15-b8ec-fa2e30f854ce
keywords:
- InterlockedMin-Funktion HLSL
topic_type:
- apiref
api_name:
- InterlockedMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c84650ce8f95f9ba0aa6e3d5bf5d54f2915a1a94fdf96d9f89179598004744e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672660"
---
# <a name="interlockedmin-function-hlsl-reference"></a>InterlockedMin-Funktion (HLSL-Referenz)

Führt eine garantierte atomare Min. aus.

## <a name="syntax"></a>Syntax

``` syntax
void InterlockedMin(
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

Dieser Vorgang kann nur für int- und uint-typisierte Ressourcen und Freigegebene Arbeitsspeichervariablen ausgeführt werden. Es gibt zwei mögliche Verwendungsmöglichkeiten für diese Funktion. Die erste ist, wenn R ein Variablentyp für gemeinsam genutzten Arbeitsspeicher ist. In diesem Fall führt die Funktion einen atomaren Mindestwert für das Shared Memory-Register aus, auf das vom Dest verwiesen wird. Das zweite Szenario ist, wenn R ein Ressourcenvariablentyp ist. In diesem Szenario führt die Funktion einen atomaren Mindestwert für den Ressourcenspeicherort aus, auf den vom Dest verwiesen wird. Die überladene Funktion verfügt über eine zusätzliche Ausgabevariable, die auf den ursprünglichen Wert dest festgelegt wird. Dieser überladene Vorgang ist nur verfügbar, wenn R lesbar und beschreibbar ist.

### <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höhere Shadermodelle | Ja       |



 

Diese Funktion wird in den folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      |  x   |  x     |  x       | x     | x       |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Systeminterne Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




