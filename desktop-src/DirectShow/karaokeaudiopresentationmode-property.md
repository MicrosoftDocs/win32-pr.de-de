---
description: Mit der Eigenschaft "karaokeaudiopressentiments ationmode" wird die "right left Speaker"-Mischung für die zusätzlichen Karaoke-Kanäle festgelegt oder abgerufen.
ms.assetid: f32706eb-7f97-433d-854a-17d57cc60190
title: Karaokeaudiopressentiments ationmode (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429f15c99d58136d4c423c4f66b19d12c93802a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343546"
---
# <a name="karaokeaudiopresentationmode-property"></a>Karaokeaudiopressentiments ationmode (Eigenschaft)

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `KaraokeAudioPresentationMode` Eigenschaft legt den Rechts linken sprechermix für die zusätzlichen Karaoke-Kanäle fest oder ruft ihn ab.

``` syntax
[iMode ] = MSWebDVD.KaraokeAudioPresentationMode
```

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert mit einem Satz von Bitflags zurück, der angibt, wie die zusätzlichen Karaoke-Kanäle auf den linken und rechten Referenten herabgestuft werden.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist Lese-/Schreibzugriff mit dem Standardwert 0 (null).

Audiokanäle sind NULL basiert, sodass die Kanäle 0 und 1 im Allgemeinen die Kanäle für den rechten und linken Sprecher darstellen und die Kanäle 2 bis 4 die drei zusätzlichen Karaoke-Kanäle sind. Wenn das mswebdvd-Objekt in den Modus "Karaoke" wechselt, werden die Kanäle 2 und höher automatisch mit einem Mutes Verwenden Sie bitweise **or** -Vorgänge, um das entsprechende Bit festzulegen, um einen hilfsanchannel an den linken Sprecher, den rechten Sprecher, beide Sprecher (beide Bits on) oder an keine Sprecher (beide Bits off) zu senden. Diese Bits sind standardmäßig deaktiviert, wenn der DVD-Navigator in den Karaoke-Modus wechselt. Der Wert der Bits und die entsprechende Aktion werden in der folgenden Tabelle angegeben.



| Wert  | BESCHREIBUNG                            |
|--------|----------------------------------------|
| 0x0004 | Downmix von Channel 2 zum linken Sprecher  |
| 0x0008 | Downmix von Channel 3 zum linken Sprecher  |
| 0x0010 | Downmix von Channel 4 zum linken Sprecher  |
| 0x0400 | Downmix von Channel 2 zum rechten Redner |
| 0x0800 | Downmix von Channel 3 zum rechten Redner |
| 0x1000 | Downmix von Channel 4 zum rechten Redner |



 

 

 



