---
title: WaveActiveMin-Funktion
description: Gibt den Minimalwert des Ausdrucks auf allen aktiven Spuren in der aktuellen Welle zurück und repliziert ihn zurück an alle aktiven Lanes.
ms.assetid: BA762C02-894C-4AF9-A226-C1E3AAC286FF
keywords:
- WaveActiveMin-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveActiveMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b97f2e58449e8b33270318f305a6fee87662a6aac4643b35152024366bf8b08b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721787"
---
# <a name="waveactivemin-function"></a>WaveActiveMin-Funktion

Gibt den Minimalwert des Ausdrucks auf allen aktiven Spuren in der aktuellen Welle zurück und repliziert ihn zurück an alle aktiven Lanes.

## <a name="syntax"></a>Syntax

``` syntax
<type> WaveActiveMin(
   <type> expr
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*expr* 
</dt> <dd>

Der auszuwertende Ausdruck.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Minimalwert.

## <a name="remarks"></a>Hinweise

Die Reihenfolge der Vorgänge ist nicht definiert.

Diese Funktion wird von Shadermodell 6.0 in allen Shaderstufen unterstützt. 



 

## <a name="examples"></a>Beispiele

``` syntax
 float3 minPos = WaveActiveMin( myPoint.position );
    BoundingBox.min = min( minPos, BoundingBox.min );
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Shadermodell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shadermodell 6](shader-model-6-0.md)
</dt> </dl>

 

 




