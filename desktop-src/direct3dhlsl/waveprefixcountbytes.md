---
title: WavePrefixCountBits-Funktion
description: Gibt die Summe aller angegebenen booleschen Variablen zurück, die für alle aktiven Lanes auf TRUE festgelegt sind, wobei indizes kleiner als die aktuelle Lane sind.
ms.assetid: AEC9AFD7-6478-4397-B531-73990D30AA48
keywords:
- WavePrefixCountBits-Funktion HLSL
topic_type:
- apiref
api_name:
- WavePrefixCountBits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 048b63d24e87d97f0e0223083a91694c0471b9e38ad21afbc487c02d711d720d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504676"
---
# <a name="waveprefixcountbits-function"></a>WavePrefixCountBits-Funktion

Gibt die Summe aller angegebenen booleschen Variablen zurück, die für alle aktiven Lanes auf TRUE festgelegt sind, wobei indizes kleiner als die aktuelle Lane sind.

## <a name="syntax"></a>Syntax


``` syntax
uint WavePrefixCountBits(
   bool bBit
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bBit* 
</dt> <dd>

Die angegebenen booleschen Variablen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Summe aller angegebenen booleschen Variablen, die für alle aktiven Lanes mit Indizes kleiner als die aktuelle Lane auf TRUE festgelegt sind.

## <a name="remarks"></a>Hinweise

Diese Funktion wird vom Shadermodell 6.0 in allen Shaderstufen unterstützt. 



 

## <a name="examples"></a>Beispiele

Der folgende Code beschreibt, wie ein komprimierter Schreibvorgang in einen geordneten Stream implementiert wird, bei dem die Anzahl der pro Lane geschriebenen Elemente entweder 1 oder 0 beträgt.

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

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht über Shadermodell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shadermodell 6](shader-model-6-0.md)
</dt> </dl>

 

 




