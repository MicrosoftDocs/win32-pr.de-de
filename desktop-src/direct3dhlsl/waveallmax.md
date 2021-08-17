---
title: WaveActiveMax-Funktion
description: Gibt den Maximalwert des Ausdrucks für alle aktiven Lanes in der aktuellen Welle zurück und repliziert ihn wieder auf alle aktiven Lanes.
ms.assetid: 19101C56-2618-4F34-8725-DF92198ABDA4
keywords:
- WaveActiveMax-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveActiveMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8c85936ca28aabe0365fd912b4d764739b0ab15765241a243ad67143dacd0d7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119484200"
---
# <a name="waveactivemax-function"></a>WaveActiveMax-Funktion

Gibt den Maximalwert des Ausdrucks für alle aktiven Lanes in der aktuellen Welle zurück und repliziert ihn wieder auf alle aktiven Lanes.

## <a name="syntax"></a>Syntax

``` syntax
<type> WaveActiveMax(
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

Der Maximalwert.

## <a name="remarks"></a>Hinweise

Die Reihenfolge der Vorgänge ist nicht definiert.

Diese Funktion wird vom Shadermodell 6.0 in allen Shaderstufen unterstützt. 



 

## <a name="examples"></a>Beispiele

``` syntax
 float3 maxPos = WaveActiveMax( myPoint.position );
    BoundingBox.max = max( maxPos, BoundingBox.max );
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Shadermodell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shadermodell 6](shader-model-6-0.md)
</dt> </dl>

 

 




