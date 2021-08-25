---
title: WaveActiveCountBits-Funktion
description: Zählt die Anzahl der booleschen Variablen, die auf allen aktiven Spuren in der aktuellen Welle als true ausgewertet werden, und repliziert das Ergebnis auf alle Spuren in der Welle.
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
ms.openlocfilehash: a53a2953ba7d77f1969a7d5dabef3c17437e8bbb
ms.sourcegitcommit: 8d7ce0c4827f8a4fd501cc6487f1a8360e944577
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/24/2021
ms.locfileid: "122767604"
---
# <a name="waveactivecountbits-function"></a>WaveActiveCountBits-Funktion

Zählt die Anzahl der booleschen Variablen, die auf allen aktiven Spuren in der aktuellen Welle als true ausgewertet werden, und repliziert das Ergebnis auf alle Spuren in der Welle.

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

Die auswertenden booleschen Variablen. Wenn Sie einen expliziten booleschen True-Wert bereitstellen, wird die Anzahl der aktiven Lanes zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Anzahl der Lanes, für die die boolesche Variable auf allen aktiven Spuren in der aktuellen Welle als TRUE ausgewertet wird.

## <a name="remarks"></a>Bemerkungen

Diese Funktion wird von Shadermodell 6.0 in allen Shaderstufen unterstützt. 



 

## <a name="examples"></a>Beispiele

Dies kann effizienter implementiert werden als ein vollständiges WaveActiveSum, wie im folgenden Beispiel beschrieben:

``` syntax
result = WaveActiveCountBits( WaveActiveBallot( bBit ) );
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht über Shadermodell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shadermodell 6](shader-model-6-0.md)
</dt> </dl>

 

 




