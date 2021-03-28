---
title: Waveprefixzähltbits-Funktion
description: Gibt die Summe aller angegebenen booleschen Variablen für alle aktiven Bereiche mit Indizes zurück, die kleiner als die aktuelle Seite sind.
ms.assetid: AEC9AFD7-6478-4397-B531-73990D30AA48
keywords:
- Waveprefixzähltbits-Funktion HLSL
topic_type:
- apiref
api_name:
- WavePrefixCountBits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72f35df1e463ff89441938e4cae19a890821baf9
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104039845"
---
# <a name="waveprefixcountbits-function"></a>Waveprefixzähltbits-Funktion

Gibt die Summe aller angegebenen booleschen Variablen für alle aktiven Bereiche mit Indizes zurück, die kleiner als die aktuelle Seite sind.

## <a name="syntax"></a>Syntax


``` syntax
uint WavePrefixCountBits(
   bool bBit
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Bbit* 
</dt> <dd>

Die angegebenen booleschen Variablen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Summe aller angegebenen booleschen Variablen ist für alle aktiven Bereiche mit Indizes, die kleiner als die aktuelle Strecke sind, auf true festgelegt.

## <a name="remarks"></a>Bemerkungen

Diese Funktion wird vom Shader-Modell 6,0 in allen shaderphasen unterstützt. 



 

## <a name="examples"></a>Beispiele

Im folgenden Code wird beschrieben, wie ein komprimierter Schreibvorgang in einen geordneten Stream implementiert wird, wobei die Anzahl der pro Lane geschriebenen Elemente entweder 1 oder 0 ist.

``` syntax
bool bDoesThisLaneHaveAnAppendItem = <expr>;
// compute number of items to append for the whole wave
uint laneAppendOffset = WavePrefixCountBits( bDoesThisLaneHaveAnAppendItem );
uint appendCount = WaveActiveCountBits( bDoesThisLaneHaveAnAppendItem);
// update the output location for this whole wave
uint appendOffset;
if ( WaveIsFirstLane () )
{
    // this way, we only issue one atomic for the entire wave, which reduces contention
    // and keeps the output data for each lane in this wave together in the output buffer
    InterlockedAdd(bufferSize, appendCount, appendOffset);
}
appendOffset = WaveReadLaneFirst( appendOffset ); // broadcast value
appendOffset += laneAppendOffset; // and add in the offset for this lane
buffer[appendOffset] = myData; // write to the offset location for this lane
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Shader-Modell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader-Modell 6](shader-model-6-0.md)
</dt> </dl>

 

 




