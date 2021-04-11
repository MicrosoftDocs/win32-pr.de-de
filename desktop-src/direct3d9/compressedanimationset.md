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
# <a name="compressedanimationset"></a><span data-ttu-id="3a945-103">Compressedanimationset</span><span class="sxs-lookup"><span data-stu-id="3a945-103">CompressedAnimationSet</span></span>

<span data-ttu-id="3a945-104">Enthält Animations Satz Daten.</span><span class="sxs-lookup"><span data-stu-id="3a945-104">Contains animation set data.</span></span>

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

<span data-ttu-id="3a945-105">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="3a945-105">Where:</span></span>

-   <span data-ttu-id="3a945-106">Compressedblocksize: die Gesamtgröße der komprimierten Daten im komprimierten Keyframe-Animationsdaten Puffer in Bytes.</span><span class="sxs-lookup"><span data-stu-id="3a945-106">CompressedBlockSize - Total size, in bytes, of the compressed data in the compressed key frame animation data buffer.</span></span>
-   <span data-ttu-id="3a945-107">Tickspersec: Anzahl der Animations Tastatur-Frame Ticks, die pro Sekunde auftreten.</span><span class="sxs-lookup"><span data-stu-id="3a945-107">TicksPerSec - Number of animation key frame ticks that occur per second.</span></span>
-   <span data-ttu-id="3a945-108">Playbacktype-Typ der Animations Satz-Wiedergabe Schleife.</span><span class="sxs-lookup"><span data-stu-id="3a945-108">PlaybackType - Type of the animation set playback loop.</span></span> <span data-ttu-id="3a945-109">Siehe [**D3DXPLAYBACK \_ Type**](./d3dxplayback-type.md).</span><span class="sxs-lookup"><span data-stu-id="3a945-109">See [**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md).</span></span>
-   <span data-ttu-id="3a945-110">BufferLength: minimale Puffergröße (in Bytes), die zum Speichern komprimierter Keyframe-Animationsdaten erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="3a945-110">BufferLength - Minimum buffer size, in bytes, required to hold compressed key frame animation data.</span></span> <span data-ttu-id="3a945-111">Der Wert ist gleich ((compressedblocksize + 3)/4).</span><span class="sxs-lookup"><span data-stu-id="3a945-111">Value is equal to ( ( CompressedBlockSize + 3 ) / 4 ).</span></span>
-   <span data-ttu-id="3a945-112">Compresseddata \[ BufferLength \] : ein Array mit komprimierten Datenwerten.</span><span class="sxs-lookup"><span data-stu-id="3a945-112">CompressedData\[BufferLength\] - An array of compressed data values.</span></span>

## <a name="see-also"></a><span data-ttu-id="3a945-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a945-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a945-114">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="3a945-114">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> <dt>

[<span data-ttu-id="3a945-115">**Xfilecompressedanimationset**</span><span class="sxs-lookup"><span data-stu-id="3a945-115">**XFILECOMPRESSEDANIMATIONSET**</span></span>](xfilecompressedanimationset.md)
</dt> </dl>

 

 
