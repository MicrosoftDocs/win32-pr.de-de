---
title: WaveActiveSum-Funktion
description: Summiert den Wert des Ausdrucks über alle aktiven Lanes in der aktuellen Welle hinweg und repliziert ihn auf alle Spuren in der aktuellen Welle.
ms.assetid: 94CEF4AA-D6DE-4B00-9743-F491F255FE3D
keywords:
- WaveActiveSum-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveActiveSum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 403768b875ed9462b79fb5d0abeee9539189597591f3a3b20f5a3b9662995542
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742260"
---
# <a name="waveactivesum-function"></a>WaveActiveSum-Funktion

Summiert den Wert des Ausdrucks über alle aktiven Lanes in der aktuellen Welle hinweg und repliziert ihn auf alle Spuren in der aktuellen Welle.

## <a name="syntax"></a>Syntax

``` syntax
<type> WaveActiveSum(
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

Der Summenwert.

## <a name="remarks"></a>Hinweise

Die Reihenfolge der Vorgänge ist nicht definiert.

Diese Funktion wird von Shadermodell 6.0 in allen Shaderstufen unterstützt. 



 

## <a name="examples"></a>Beispiele

``` syntax
float3 total = WaveActiveSum( position ); // sum positions in wave
float3 center = total/count;           // compute average of these positions
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Shadermodell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shadermodell 6](shader-model-6-0.md)
</dt> </dl>

 

 




