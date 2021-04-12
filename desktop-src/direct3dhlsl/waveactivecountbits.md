---
title: Waveactivezähltbits-Funktion
description: Zählt die Anzahl von booleschen Variablen, die für alle aktiven Bereiche in der aktuellen Wave als true ausgewertet werden, und repliziert das Ergebnis in alle Bereiche in der Wave.
ms.assetid: 053E100C-7E09-4F9D-9F38-9D5E208A38CE
keywords:
- Waveactivezähltbits-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveActiveCountBits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c4d2db55e9e3a0ad8f0a66be183d6e39d2a8b9c
ms.sourcegitcommit: a232805e6c618673f2df904111cc4f5a33e15504
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2020
ms.locfileid: "104316868"
---
# <a name="waveactivecountbits-function"></a>Waveactivezähltbits-Funktion

Zählt die Anzahl von booleschen Variablen, die für alle aktiven Bereiche in der aktuellen Wave als true ausgewertet werden, und repliziert das Ergebnis in alle Bereiche in der Wave.

## <a name="syntax"></a>Syntax


``` syntax
uint WaveActiveCountBits(
   bool bBit
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Bbit* 
</dt> <dd>

Die auszuwertenden booleschen Variablen. Durch die Angabe eines expliziten echten booleschen Werts wird die Anzahl der aktiven Bereiche zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Anzahl, die in allen aktiven Bereichen in der aktuellen Wave als true ausgewertet wird.

## <a name="remarks"></a>Bemerkungen

Diese Funktion wird vom Shader-Modell 6,0 in allen shaderphasen unterstützt. 



 

## <a name="examples"></a>Beispiele

Dies kann effizienter als ein vollständiger waveactivesum implementiert werden, wie im folgenden Beispiel beschrieben:

``` syntax
result = WaveActiveCountBits( WaveActiveBallot( bBit ) );
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Shader-Modell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader-Modell 6](shader-model-6-0.md)
</dt> </dl>

 

 




