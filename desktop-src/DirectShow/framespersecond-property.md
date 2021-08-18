---
description: Die FramesPerSecond-Eigenschaft ruft die Videobildrate für den aktuellen DVD-Titel ab.
ms.assetid: c5d36308-1447-4636-9b3a-4a3f93d27789
title: FramesPerSecond-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96a883f031680a57711fa092f29bc9ecbd76cb1a017c03f80337959050e62cd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015668"
---
# <a name="framespersecond-property"></a>FramesPerSecond-Eigenschaft

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `FramesPerSecond` -Eigenschaft ruft die Videobildrate für den aktuellen DVD-Titel ab.

``` syntax
[ iFramesPerSec = ] MSWebDVD.FramesPerSecond
```

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, der die Videobildrate darstellt. 25 oder 30 Frames pro Sekunde.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist schreibgeschützt und hat keinen Standardwert. NTSC-Videosignale werden mit 30 Bildern pro Sekunde angezeigt. PAL wird mit 25 Bildern pro Sekunde angezeigt. Ein Datenträger wird für die Wiedergabe auf NTSC oder PAL codiert, kann aber nicht auf beiden wiedergegeben werden.

 

 



