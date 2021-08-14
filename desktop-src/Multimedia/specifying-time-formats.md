---
title: Angeben von Zeitformaten
description: Angeben von Zeitformaten
ms.assetid: 11d28d63-ed3e-4137-b9d8-1681bf0e33ff
keywords:
- MCIWndGetTimeFormat-Makro
- MCIWndSetTimeFormat-Makro
- MCIWndUseTime-Makro
- MCIWndUseFrames-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50c14303879a3d13d018be8691eb1947ee1ed67907df796ae38cffc3936bf2ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801703"
---
# <a name="specifying-time-formats"></a>Angeben von Zeitformaten

Multimediadatentypen können in der Regel Zeit nutzen, um signifikante Positionen innerhalb ihres Inhalts zu identifizieren. Gängige Zeitformate sind Millisekunden, Spuren und Frames. es gibt auch andere weniger gängige Zeitformate, z. B. SMPTE (Society of Motion Picture and Tv Engineers) 24. Die Zeit ist das Format- und Referenzsystem für Waveform-Audio- und CD-Audiodaten. Video unterstützt Zeit, obwohl es als Sequenz von Frames (Stream) aufgezeichnet wird, die in der Regel mit einer bestimmten Geschwindigkeit wiedergegeben wird. Mehrere Makros sind für die Benennung des Zeitformats verfügbar.

Sie können das aktuelle Zeitformat für eine Datei oder ein Gerät abrufen, indem Sie das [**MCIWndGetTimeFormat-Makro**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) verwenden. Sie können das aktuelle Zeitformat mithilfe des [**MCIWndSetTimeFormat-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) in ein beliebiges anderes Zeitformat ändern, das von einem Gerät unterstützt wird. Alternativ können Sie das Zeitformat mithilfe der Makros [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) oder [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) auf Millisekunden oder Frames festlegen.

> [!Note]  
> Nicht zusammenhängende Formate wie Spuren und SMPTE können dazu führen, dass sich die Symbolleiste unregelmäßig verhält. Für diese Zeitformate können Sie die Symbolleiste deaktivieren, indem Sie \_ beim Erstellen eines MCIWnd-Fensters den MCIWNDF-NOPLAYBAR-Fensterstil angeben.

 

 

 




