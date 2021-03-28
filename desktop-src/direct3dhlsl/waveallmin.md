---
title: Waveactivemin-Funktion
description: Gibt den minimalen Wert des Ausdrucks über alle aktiven Bereiche in der aktuellen Wave zurück, die auf alle aktiven Bereiche repliziert werden.
ms.assetid: BA762C02-894C-4AF9-A226-C1E3AAC286FF
keywords:
- Waveactivemin-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveActiveMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91555df354ab2b7ffc447a9422c4811ae23e6e0c
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104039840"
---
# <a name="waveactivemin-function"></a>Waveactivemin-Funktion

Gibt den minimalen Wert des Ausdrucks über alle aktiven Bereiche in der aktuellen Wave zurück, die auf alle aktiven Bereiche repliziert werden.

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

## <a name="remarks"></a>Bemerkungen

Die Reihenfolge der Vorgänge ist nicht definiert.

Diese Funktion wird vom Shader-Modell 6,0 in allen shaderphasen unterstützt. 



 

## <a name="examples"></a>Beispiele

``` syntax
 float3 minPos = WaveActiveMin( myPoint.position );
    BoundingBox.min = min( minPos, BoundingBox.min );
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Shader-Modell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader-Modell 6](shader-model-6-0.md)
</dt> </dl>

 

 




