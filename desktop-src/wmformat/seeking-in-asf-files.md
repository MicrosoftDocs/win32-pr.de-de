---
title: Suchen in ASF-Dateien (Windows Media Format 11 SDK)
description: Erfahren Sie, wie der WM ASF-Reader eine sehr genaue temporale Suche auf Windows Media-basierten Inhalten durchführen kann, die über einen temporalen Index im Windows Media Format 11 SDK verfügt.
ms.assetid: a1717cb4-9f41-4148-b088-a6517be7da9b
keywords:
- Windows Media Format SDK, Suchen in ASF-Dateien
- Windows Media Format SDK, DirectShow
- Advanced Systems Format (ASF),DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF),seeking
- ASF (Advanced Systems Format), seeking
- DirectShow,Suchen in ASF-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 807631861cdc820457360058f22fca380fca29ea
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409883"
---
# <a name="seeking-in-asf-files-windows-media-format-11-sdk"></a>Suchen in ASF-Dateien (Windows Media Format 11 SDK)

Der [WM ASF-Reader](wm-asf-reader-filter.md)kann über seine **IMediaSeeking-Schnittstelle** sehr genaue temporale Suchmaßnahmen für Windows Media-basierte Inhalte ausführen, die über einen temporalen Index verfügt. (Alle frameindizierten Inhalte enthalten auch einen temporalen Index.) Garantierte framegenaue Suchfunktionen werden im WM ASF-Reader nicht direkt unterstützt, aber es gibt eine Möglichkeit, dies zu tun, wenn Sie diese Funktionalität benötigen. Verwenden Sie zunächst das Windows Media Format SDK direkt, um eine Instanz des synchronen Readerobjekts zu erstellen, die Datei zu öffnen, den einem angegebenen Frame zugeordneten Zeitstempel zu erhalten und dann die DirectShow **IMediaSeeking-Schnittstelle** zu verwenden, um nach dieser Zeit zu suchen. Die **IVideoFrameStep-Schnittstelle** von DirectShow unterstützt keine framegenaue Suche nach Windows Media-basierten Inhalten. Das DSSeekFm-Beispiel im Windows Media Format SDK veranschaulicht, wie Frame-genaue Suchungen mithilfe des WM ASF-Readers ausgeführt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**WM ASF-Readerfilter**](wm-asf-reader-filter.md)
</dt> </dl>

 

 




