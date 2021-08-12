---
title: WaveActiveBitAnd-Funktion
description: Gibt das bitweise AND aller Werte des Ausdrucks auf allen aktiven Spuren in der aktuellen Welle zurück und repliziert es zurück an alle aktiven Lanes.
ms.assetid: 602884CD-E656-4DEB-A30A-8A7D127A2217
keywords:
- WaveActiveBitAnd-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveActiveBitAnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 96d09d91df4ff9226a8fb86203be0bd79bc3c11d1882553607358c3c84d3814c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118282998"
---
# <a name="waveactivebitand-function"></a>WaveActiveBitAnd-Funktion

Gibt das bitweise AND aller Werte des Ausdrucks auf allen aktiven Spuren in der aktuellen Welle zurück und repliziert es zurück an alle aktiven Lanes.

## <a name="syntax"></a>Syntax


``` syntax
<int_type> WaveActiveBitAnd(
   <int_type> expr
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*expr* 
</dt> <dd>

Der auszuwertende Ausdruck.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der bitweise AND-Wert.

## <a name="remarks"></a>Hinweise

Diese Funktion wird von Shadermodell 6.0 in allen Shaderstufen unterstützt. 



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht über Shadermodell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shadermodell 6](shader-model-6-0.md)
</dt> </dl>

 

 




