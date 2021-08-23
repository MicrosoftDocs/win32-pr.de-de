---
title: InterlockedExchange-Funktion (HLSL-Referenz)
description: Weist dem Wert dest zu und gibt den ursprünglichen Wert zurück.
ms.assetid: 1e7ce7ff-9e23-47fa-8e76-713f6bf57abf
keywords:
- InterlockedExchange-Funktion HLSL
topic_type:
- apiref
api_name:
- InterlockedExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3880a85af5658d0d50eb079c2dd1fc300e6a4de4b7f606688ab9d7a317cf321c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511320"
---
# <a name="interlockedexchange-function-hlsl-reference"></a>InterlockedExchange-Funktion (HLSL-Referenz)

Weist dem Wert dest zu und gibt den ursprünglichen Wert zurück.

## <a name="syntax"></a>Syntax

``` syntax
void InterlockedExchange(
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

Der ursprüngliche Wert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Dieser Vorgang kann nur für skalar typierte Ressourcen und Freigegebene Arbeitsspeichervariablen ausgeführt werden. Es gibt zwei mögliche Verwendungsmöglichkeiten für diese Funktion. Die erste ist, wenn R ein Variablentyp für freigegebenen Arbeitsspeicher ist. In diesem Fall führt die Funktion den Vorgang für das Shared Memory-Register aus, auf das vom dest verwiesen wird. Das zweite Szenario ist, wenn R ein Ressourcenvariablentyp ist. In diesem Szenario führt die Funktion den Vorgang für den Ressourcenspeicherort aus, auf den vom dest verwiesen wird. Dieser Vorgang ist nur verfügbar, wenn R lesbar und schreibbar ist.

### <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höher– Shadermodelle | ja       |



 

Diese Funktion wird in den folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      |  x   | x      |  x       | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Systeminterne Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




