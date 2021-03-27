---
title: Waveactivesum-Funktion
description: Fasst den Wert des Ausdrucks für alle aktiven Bereiche in der aktuellen Wave zusammen und repliziert Sie in allen Bereichen in der aktuellen Wave.
ms.assetid: 94CEF4AA-D6DE-4B00-9743-F491F255FE3D
keywords:
- Waveactivesum-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveActiveSum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b98ecf2521841b9da73e1b917d44f1d91b7876d2
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103949220"
---
# <a name="waveactivesum-function"></a>Waveactivesum-Funktion

Fasst den Wert des Ausdrucks für alle aktiven Bereiche in der aktuellen Wave zusammen und repliziert Sie in allen Bereichen in der aktuellen Wave.

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

Der Sum-Wert.

## <a name="remarks"></a>Bemerkungen

Die Reihenfolge der Vorgänge ist nicht definiert.

Diese Funktion wird vom Shader-Modell 6,0 in allen shaderphasen unterstützt. 



 

## <a name="examples"></a>Beispiele

``` syntax
float3 total = WaveActiveSum( position ); // sum positions in wave
float3 center = total/count;           // compute average of these positions
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Shader-Modell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader-Modell 6](shader-model-6-0.md)
</dt> </dl>

 

 




