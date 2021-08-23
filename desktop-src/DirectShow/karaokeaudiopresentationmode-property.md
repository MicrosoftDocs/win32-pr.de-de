---
description: Die Eigenschaft ProzentokeAudioPresentationMode legt die Link-rechts-Lautsprechermischung für die zusätzlichen Sendekanäle fest oder ruft sie ab.
ms.assetid: f32706eb-7f97-433d-854a-17d57cc60190
title: Moduseigenschaft "QualokeAudioPresentationMode"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af634a3beaade7e497cdc6d158ccf1121ebb09542bdec92ceaae823b1b91ccdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952379"
---
# <a name="karaokeaudiopresentationmode-property"></a>Moduseigenschaft "QualokeAudioPresentationMode"

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `KaraokeAudioPresentationMode` -Eigenschaft legt die Linke-rechts-Lautsprechermischung für die Hilfskanäle fest oder ruft sie ab.

``` syntax
[iMode ] = MSWebDVD.KaraokeAudioPresentationMode
```

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, der einen Satz von Bitflags enthält, der angibt, wie die Hilfskanalkanäle links und rechts gemischt werden.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird mit dem Standardwert 0 (null) gelesen/geschrieben.

Audiokanäle sind nullbasiert, sodass die Kanäle 0 und 1 im Allgemeinen die Kanäle rechts und links darstellen, und Kanäle 2 bis 4 sind die drei zusätzlichen Sendekanäle. Wenn das MSWebDVD-Objekt in den Modus "Tarifoke" wechselt, werden kanäle 2 und höher automatisch stummgeschaltet. Verwenden Sie  bitweise OR-Vorgänge, um das entsprechende Bit festzulegen, um einen Hilfskanal an den linken Lautsprecher, den rechten Lautsprecher, beide Sprecher (beide Bits eingeschaltet) oder an keine Sprecher (beide Bits aus) zu senden. Diese Bits sind standardmäßig deaktiviert, wenn der DVD-Navigator in den Modus "Dvdoke" wechselt. Der Wert der Bits und ihre entsprechende Aktion sind in der folgenden Tabelle angegeben.



| Wert  | Beschreibung                            |
|--------|----------------------------------------|
| 0x0004 | Downmix Channel 2 zum linken Lautsprecher  |
| 0x0008 | Downmix Channel 3 zum linken Lautsprecher  |
| 0x0010 | Downmix Channel 4 zum linken Lautsprecher  |
| 0x0400 | Downmix Channel 2 zum rechten Lautsprecher |
| 0x0800 | Downmix Channel 3 zum rechten Lautsprecher |
| 0x1000 | Downmix Channel 4 zum rechten Lautsprecher |



 

 

 



