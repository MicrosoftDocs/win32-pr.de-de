---
description: Die framesPerSecond-Eigenschaft ruft die Video Frame Rate für den aktuellen DVD-Titel ab.
ms.assetid: c5d36308-1447-4636-9b3a-4a3f93d27789
title: FramesPerSecond (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e00ec3281d88a2901f630c9231edbf1e76a89c23
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344781"
---
# <a name="framespersecond-property"></a>FramesPerSecond (Eigenschaft)

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `FramesPerSecond` Eigenschaft ruft die Video Frame Rate für den aktuellen DVD-Titel ab.

``` syntax
[ iFramesPerSec = ] MSWebDVD.FramesPerSecond
```

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, der die Video Frame Rate darstellt. entweder 25 oder 30 Frames pro Sekunde.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist schreibgeschützt und weist keinen Standardwert auf. NTSC-Videosignale werden bei 30 Frames pro Sekunde angezeigt. PAL wird bei 25 Frames pro Sekunde angezeigt. Ein Disc ist für die Wiedergabe in NTSC oder PAL codiert, kann aber nicht auf beiden spielen.

 

 



