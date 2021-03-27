---
title: Waveactivemax-Funktion
description: Gibt den maximalen Wert des Ausdrucks für alle aktiven Bereiche in der aktuellen Wave zurück und repliziert Sie zurück in alle aktiven Bereiche.
ms.assetid: 19101C56-2618-4F34-8725-DF92198ABDA4
keywords:
- Waveactivemax-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveActiveMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c0fd10f578d598c326cdfb4cf943d3a35fe78a9
ms.sourcegitcommit: a232805e6c618673f2df904111cc4f5a33e15504
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2020
ms.locfileid: "104391275"
---
# <a name="waveactivemax-function"></a>Waveactivemax-Funktion

Gibt den maximalen Wert des Ausdrucks für alle aktiven Bereiche in der aktuellen Wave zurück und repliziert Sie zurück in alle aktiven Bereiche.

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

## <a name="remarks"></a>Bemerkungen

Die Reihenfolge der Vorgänge ist nicht definiert.

Diese Funktion wird vom Shader-Modell 6,0 in allen shaderphasen unterstützt. 



 

## <a name="examples"></a>Beispiele

``` syntax
 float3 maxPos = WaveActiveMax( myPoint.position );
    BoundingBox.max = max( maxPos, BoundingBox.max );
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Shader-Modell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader-Modell 6](shader-model-6-0.md)
</dt> </dl>

 

 




