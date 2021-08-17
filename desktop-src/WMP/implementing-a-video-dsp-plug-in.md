---
title: Implementieren eines Video-DSP-Plug-Ins
description: Implementieren eines Video-DSP-Plug-Ins
ms.assetid: 36c06c57-7623-430b-8280-9dba7b0a2e9b
keywords:
- Windows Media Player-Plug-Ins, Video-DSP
- Plug-Ins, Video-DSP
- Digitale Signalverarbeitungs-Plug-Ins, Implementieren von Code
- DSP-Plug-Ins, Implementieren von Code
- Digitale Signalverarbeitungs-Plug-Ins, Ändern von Beispielcode
- DSP-Plug-Ins, Ändern von Beispielcode
- Digitale Signalverarbeitungs-Plug-Ins, Videoimplementierung
- DSP-Plug-Ins, Videoimplementierungen
- Video-DSP-Plug-Ins, Implementieren von Code
- Video-DSP-Plug-Ins, Ändern von Beispielcode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4afdbabd36167c11ef7c1c57aeccb475605f9365c550c572422af3440d760ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135703"
---
# <a name="implementing-a-video-dsp-plug-in"></a>Implementieren eines Video-DSP-Plug-Ins

Computervideoanzeigeadapter unterstützen eine Reihe von Videoformaten. Digitale Videocodecs unterstützen auch eine Reihe von Videoformaten. Beim Versuch, eine bestimmte Videodatei wiederzugeben, müssen Windows Media Player ein Format auswählen, das für das Rendering verwendet werden soll. Der Player versucht, die beste Übereinstimmung zwischen den Formaten zu finden, die vom Videocodec unterstützt werden, und den Formaten, die vom Videoanzeigeadapter unterstützt werden, d. h. dem Format, das die höchste Qualität liefert.

Um ein Windows Media Player DSP-Plug-In zu erstellen, das Videos verarbeitet, müssen Sie zunächst entscheiden, welche Videoformate Das Plug-In verarbeiten soll. Das Beispiel-Video-DSP-Plug-In funktioniert mit den folgenden Videoformaten:

-   NV12
-   YV12
-   YUY2
-   UYVY
-   RGB32
-   RGB24
-   RGB555
-   RGB565

Welche Formate Sie verarbeiten möchten, liegt bei Ihnen. Sie können Formate aus dem Beispiel-Plug-In entfernen, damit sie nicht mehr unterstützt werden, und Sie können Code hinzufügen, um zusätzliche Formate zu verarbeiten.

Die folgenden Abschnitte enthalten zusätzliche Informationen, die Sie kennen sollten, bevor Sie Ihr eigenes Video-DSP-Plug-In für Windows Media Player erstellen:

-   [Videoformataushandlung im Beispielvideo-DSP-Plug-In](video-format-negotiation-in-the-sample-video-dsp-plug-in.md)
-   [DoProcessOutput im Beispiel-Video-DSP-Plug-In](doprocessoutput-in-the-sample-video-dsp-plug-in.md)
-   [Verarbeiten des Videos](processing-the-video.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren ihres DSP-Codes**](implementing-your-dsp-code.md)
</dt> </dl>

 

 




