---
title: Angeben von Zeitformaten
description: Angeben von Zeitformaten
ms.assetid: 11d28d63-ed3e-4137-b9d8-1681bf0e33ff
keywords:
- Mciwndgettimeformat-Makro
- Mciwndsettimeformat-Makro
- Mciwnduationtime-Makro
- Mciwnduabframes-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e390e811bde4d797572c19f372923906f6b738b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310071"
---
# <a name="specifying-time-formats"></a>Angeben von Zeitformaten

Multimediare-Datentypen können in der Regel Zeit verwenden, um signifikante Positionen innerhalb ihrer Inhalte zu identifizieren. Allgemeine Zeitformate sind Millisekunden, nachverfolgt und Frames. andere weniger gängige Zeitformate, wie z. b. SMPTE (Society of Motion Picture und TV Engineers) 24, sind ebenfalls vorhanden. Zeit ist das Format und das Referenzsystem für Waveform-Audiodaten, MIDI und CD-Audiodaten. Video unterstützt Zeit, obwohl es als Sequenz von Frames (Stream) aufgezeichnet wird, die in der Regel mit einer bestimmten Geschwindigkeit wiedergegeben wird. Zum Festlegen des Zeit Formats sind mehrere Makros verfügbar.

Sie können das aktuelle Zeitformat für eine Datei oder ein Gerät abrufen, indem Sie das [**mciwndgettimeformat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) -Makro verwenden. Sie können das aktuelle Zeitformat in ein beliebiges anderes Zeitformat ändern, das von einem Gerät unterstützt wird, indem Sie das [**mciwndsettimeformat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) -Makro verwenden. Sie können auch das Zeitformat auf Millisekunden oder Frames festlegen, indem Sie die Makros [**mciwndusetime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) oder [**mciwnduseframes**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) verwenden.

> [!Note]  
> Nicht kontinuierliche Formate, wie z. b. "Tracks" und "SMPTE", können dazu führen, dass sich die Symbolleiste im- In diesen Zeitformaten können Sie die Symbolleiste ausschalten, indem Sie \_ beim Erstellen eines mciwnd-Fensters den Fenster Stil mciwndf noplaybar angeben.

 

 

 




