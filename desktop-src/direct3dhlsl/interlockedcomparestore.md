---
title: InterlockedCompareStore-Funktion (HLSL-Referenz)
description: Vergleicht das Ziel atomisch mit dem Vergleichswert. Wenn sie identisch sind, wird das Ziel mit dem Eingabewert überschrieben.
ms.assetid: eaf7e669-5240-40c9-9840-f4e7916e51b4
keywords:
- InterlockedCompareStore-Funktion HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareStore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7dbf13629b9c3b9b38cc3bd72a8a992ab40bd09c0333c155a7c109f71466f23b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119244"
---
# <a name="interlockedcomparestore-function-hlsl-reference"></a>InterlockedCompareStore-Funktion (HLSL-Referenz)

Vergleicht das Ziel atomisch mit dem Vergleichswert. Wenn sie identisch sind, wird das Ziel mit dem Eingabewert überschrieben.

## <a name="syntax"></a>Syntax

``` syntax
void InterlockedCompareStore(
  in R dest,
  in T compare_value,
  in T value
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*dest* \[ In\]
</dt> <dd>

Typ: **R**

Die Zieladresse.

</dd> <dt>

*Vergleichen \_ des Werts* \[ in\]
</dt> <dd>

Typ: **T**

Der Vergleichswert.

</dd> <dt>

*value* \[ In\]
</dt> <dd>

Typ: **T**

Der Eingabewert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Vergleicht atomisch den Wert, auf den *von dest* verwiesen wird, mit dem Vergleichswert und speichert den Wert *an* dem Speicherort, auf den *vom dest* verwiesen wird, wenn die Werte übereinstimmen. *\_* Dieser Vorgang kann nur für **int-** oder **uint-typierte** Ressourcen und Freigegebene Arbeitsspeichervariablen ausgeführt werden. Es gibt zwei mögliche Verwendungsmöglichkeiten für diese Funktion. Die erste ist, wenn R ein Variablentyp für freigegebenen Arbeitsspeicher ist. In diesem Fall führt die Funktion den Vorgang für das Shared Memory-Register aus, auf das von *dest verwiesen wird.* Das zweite Szenario ist, wenn R ein Ressourcenvariablentyp ist. In diesem Szenario führt die Funktion den Vorgang für den Ressourcenspeicherort aus, auf den von *dest verwiesen wird.*

### <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höher– Shadermodelle | Ja       |



 

Diese Funktion wird in den folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|  x     | x    |  x     |  x       | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Systeminterne Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




