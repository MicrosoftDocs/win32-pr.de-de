---
title: WaveActiveCountBits-Funktion
description: Zählt die Anzahl der booleschen Variablen, die für alle aktiven Lanes in der aktuellen Welle als TRUE ausgewertet werden, und repliziert das Ergebnis auf alle Lanes in der Welle.
ms.assetid: 053E100C-7E09-4F9D-9F38-9D5E208A38CE
keywords:
- WaveActiveCountBits-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveActiveCountBits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e1642cbd5cbdef162511185e9d2c05e849d78486b82e8219623286f33e39223
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504935"
---
# <a name="waveactivecountbits-function"></a>WaveActiveCountBits-Funktion

Zählt die Anzahl der booleschen Variablen, die für alle aktiven Lanes in der aktuellen Welle als TRUE ausgewertet werden, und repliziert das Ergebnis auf alle Lanes in der Welle.

## <a name="syntax"></a>Syntax


``` syntax
uint WaveActiveCountBits(
   bool bBit
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bBit* 
</dt> <dd>

Die booleschen Variablen, die ausgewertet werden sollen. Wenn Sie einen expliziten true booleschen Wert bereitstellen, wird die Anzahl der aktiven Lanes zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Anzahl von , die für alle aktiven Lanes in der aktuellen Welle als "true" ausgewertet wird.

## <a name="remarks"></a>Hinweise

Diese Funktion wird vom Shadermodell 6.0 in allen Shaderstufen unterstützt. 



 

## <a name="examples"></a>Beispiele

Dies kann effizienter als ein vollständiges WaveActiveSum implementiert werden, wie im folgenden Beispiel beschrieben:

``` syntax
result = WaveActiveCountBits( WaveActiveBallot( bBit ) );
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Shadermodell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shadermodell 6](shader-model-6-0.md)
</dt> </dl>

 

 




