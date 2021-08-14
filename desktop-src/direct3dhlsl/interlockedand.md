---
title: InterlockedAnd-Funktion (HLSL-Referenz)
description: Führt einen garantierten atomaren und aus.
ms.assetid: 7dc5185a-ea37-493d-975d-dbb803c886d3
keywords:
- InterlockedAnd-Funktion HLSL
topic_type:
- apiref
api_name:
- InterlockedAnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b058b5d235e04761c24ace1d6f1bb5cca1187f01d8fe0eb1a9d0178c036bf5f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511330"
---
# <a name="interlockedand-function-hlsl-reference"></a>InterlockedAnd-Funktion (HLSL-Referenz)

Führt einen garantierten atomaren und aus.

## <a name="syntax"></a>Syntax

``` syntax
void InterlockedAnd(
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

*value* \[ In\]
</dt> <dd>

Typ: **T**

Der Eingabewert.

</dd> <dt>

*ursprünglicher \_ Wert* \[ out\]
</dt> <dd>

Typ: **T**

Optional. Der ursprüngliche Eingabewert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Dieser Vorgang kann nur für int- oder uint-typierte Ressourcen und Freigegebene Arbeitsspeichervariablen ausgeführt werden. Es gibt zwei mögliche Verwendungsmöglichkeiten für diese Funktion. Die erste ist, wenn R ein Variablentyp für freigegebenen Arbeitsspeicher ist. In diesem Fall führt die Funktion einen atomaren und einen Wert für das Shared Memory-Register aus, auf das von dest verwiesen wird. Das zweite Szenario ist, wenn R ein Ressourcenvariablentyp ist. In diesem Szenario führt die Funktion einen atomaren und einen Wert für den Ressourcenspeicherort aus, auf den von dest verwiesen wird. Die überladene Funktion verfügt über eine zusätzliche Ausgabevariable, die auf den ursprünglichen Wert von dest festgelegt wird. Dieser überladene Vorgang ist nur verfügbar, wenn R lesbar und beschreibbar ist.

### <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höher – Shadermodelle | ja       |



 

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

 

 




