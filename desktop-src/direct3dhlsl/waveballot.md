---
title: Waveactiveballot-Funktion
description: Gibt einen uint4-Wert zurück, der eine Bitmaske der Auswertung des booleschen Ausdrucks für alle aktiven Bereiche in der aktuellen Wave enthält.
ms.assetid: 67FE28E0-F397-431A-8CF8-64E4AD88CDBC
keywords:
- Waveactiveballot-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveActiveBallot
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3cdd89fad7da1e4ba7f3d5e032370834166a114
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104517210"
---
# <a name="waveactiveballot-function"></a>Waveactiveballot-Funktion

Gibt einen uint4-Wert zurück, der eine Bitmaske der Auswertung des booleschen Ausdrucks für alle aktiven Bereiche in der aktuellen Wave enthält. 

## <a name="syntax"></a>Syntax

``` syntax
uint4 WaveBallot(
   bool expr
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*expr* 
</dt> <dd>

Der auszuwertende boolesche Ausdruck.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein uint4-Wert, der eine Bitmaske der Auswertung des booleschen Ausdrucks für alle aktiven Bereiche in der aktuellen Wave enthält. Das unwichtigste Bit entspricht dem Bereich mit dem Index 0 (null). Die Bits, die inaktiven Bereichen entsprechen, sind 0 (null). Die Bits, die größer oder gleich [**wavegetlanecount**](wavegetlanecount.md) sind, sind 0 (null).

## <a name="remarks"></a>Bemerkungen

Unterschiedliche GPUs verfügen über unterschiedliche SIMD-Prozessor breiten (Lane Counts). Die meisten dieser **wavexxx** -Funktionen können auf Abstraktions Ebene betrieben werden, wenn die Breite des SIMD-Computers verborgen ist. Verwenden Sie die systeminternen Funktionen, die nicht auf der Computer Breite basieren, um die Portabilität von Code über GPUs zu maximieren. Verwenden Sie z.B. Folgendes:

``` syntax
uint result = WaveActiveCountBits( bBit );
```

anstelle von:

``` syntax
uint result = countbits( WaveActiveBallot( bBit ) );
```

Diese Funktion wird vom Shader-Modell 6,0 in allen shaderphasen unterstützt. 



 

## <a name="examples"></a>Beispiele

``` syntax
// get a bitwise representation of the number of currently active lanes:
uint4 waveBits = WaveActiveBallot( true ); // convert to bits 
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Shader-Modell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader-Modell 6](shader-model-6-0.md)
</dt> </dl>

 

 




