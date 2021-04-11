---
description: Enthält Animations Satz Daten.
ms.assetid: 8d29b9fe-cc6e-48e3-b754-f00f17e4c80a
title: Compressedanimationset
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6cdf8fde552583884604fa66ec1167183918ed5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041496"
---
# <a name="compressedanimationset"></a>Compressedanimationset

Enthält Animations Satz Daten.

``` syntax
template CompressedAnimationSet
{
    <7F9B00B3-F125-4890-876E-1C42BF697C4D>
    DWORD CompressedBlockSize;
    FLOAT TicksPerSec;
    DWORD PlaybackType;
    DWORD BufferLength;
    array DWORD CompressedData[BufferLength];
}
```

Hierbei gilt:

-   Compressedblocksize: die Gesamtgröße der komprimierten Daten im komprimierten Keyframe-Animationsdaten Puffer in Bytes.
-   Tickspersec: Anzahl der Animations Tastatur-Frame Ticks, die pro Sekunde auftreten.
-   Playbacktype-Typ der Animations Satz-Wiedergabe Schleife. Siehe [**D3DXPLAYBACK \_ Type**](./d3dxplayback-type.md).
-   BufferLength: minimale Puffergröße (in Bytes), die zum Speichern komprimierter Keyframe-Animationsdaten erforderlich ist. Der Wert ist gleich ((compressedblocksize + 3)/4).
-   Compresseddata \[ BufferLength \] : ein Array mit komprimierten Datenwerten.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> <dt>

[**Xfilecompressedanimationset**](xfilecompressedanimationset.md)
</dt> </dl>

 

 
