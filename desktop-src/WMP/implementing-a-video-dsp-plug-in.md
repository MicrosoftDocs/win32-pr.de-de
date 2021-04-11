---
title: Implementieren eines Video DSP-Plug-ins
description: Implementieren eines Video DSP-Plug-ins
ms.assetid: 36c06c57-7623-430b-8280-9dba7b0a2e9b
keywords:
- Windows Media Player-Plug-ins, videodsp
- Plug-ins, videodsp
- Plug-Ins für die digitale Signalverarbeitung, Implementieren von Code
- DSP-Plug-ins, Implementieren von Code
- Plug-Ins für die digitale Signalverarbeitung, Ändern von Beispielcode
- DSP-Plug-ins, Ändern von Beispielcode
- Plug-Ins für die digitale Signalverarbeitung, Video Implementierung
- DSP-Plug-ins, Video Implementierung
- Video DSP-Plug-ins, Implementieren von Code
- Video DSP-Plug-ins, Ändern von Beispielcode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43f1b819f328fc586d21208c00b6f0d03dca4fe9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310259"
---
# <a name="implementing-a-video-dsp-plug-in"></a>Implementieren eines Video DSP-Plug-ins

Computer-Videoanzeige Adapter unterstützen eine Reihe von Videoformaten. Digitale Video Codecs unterstützen auch eine Reihe von Videoformaten. Wenn Sie versuchen, eine bestimmte Videodatei wiederzugeben, muss Windows Media Player ein Format auswählen, das für das Rendering verwendet werden soll. Der Player versucht, die beste Übereinstimmung zwischen den vom Videocodec unterstützten Formaten und den vom Videoanzeige Adapter unterstützten Formaten zu finden, d. –. dem, der die höchste Qualität ergibt.

Um ein Windows Media Player DSP-Plug-in zu erstellen, das Video verarbeitet, müssen Sie zunächst entscheiden, welche Videoformate Sie für das Plug-in erstellen möchten. Das Beispiel-Video-DSP-Plug-in funktioniert mit den folgenden Videoformaten:

-   NV12
-   YV12
-   Im YUY2
-   UYVY
-   RGB32
-   RGB24
-   RGB555
-   RGB565

Die Formate, die Sie für die Verarbeitung auswählen, werden Ihnen angezeigt. Sie können Formate aus dem Plug-in-Beispiel entfernen, sodass Sie nicht länger unterstützt werden, und Sie können Code hinzufügen, um zusätzliche Formate zu verarbeiten.

Die folgenden Abschnitte enthalten zusätzliche Informationen, die Sie kennen sollten, bevor Sie Ihr eigenes Video DSP-Plug-in für Windows Media Player erstellen:

-   [Aushandlung des Video Formats im Beispiel-Video-DSP-Plug-in](video-format-negotiation-in-the-sample-video-dsp-plug-in.md)
-   [DoProcess Output im Beispiel-Video-DSP-Plug-in](doprocessoutput-in-the-sample-video-dsp-plug-in.md)
-   [Verarbeiten des Videos](processing-the-video.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren des DSP-Codes**](implementing-your-dsp-code.md)
</dt> </dl>

 

 




