---
title: Suchen in ASF-Dateien (Windows Media Format 11 SDK)
description: Erfahren Sie, wie der WM ASF-Reader eine sehr genaue temporale Suche für medienbasierte Inhalte Windows durchführen kann, die über einen temporalen Index im Windows Media Format 11 SDK verfügt.
ms.assetid: a1717cb4-9f41-4148-b088-a6517be7da9b
keywords:
- Windows Medienformat-SDK, Suchen in ASF-Dateien
- Windows Medienformat-SDK, DirectShow
- Advanced Systems Format (ASF),DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF),seeking
- ASF (Advanced Systems Format), seeking
- DirectShow,Suchen in ASF-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6730f1535c9601cfd0697e374ddfa35b05250ed49fc4b575fa3458b69e389285
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845895"
---
# <a name="seeking-in-asf-files-windows-media-format-11-sdk"></a>Suchen in ASF-Dateien (Windows Media Format 11 SDK)

Der [WM ASF-Reader](wm-asf-reader-filter.md)kann über seine **IMediaSeeking-Schnittstelle** eine sehr genaue temporale Suche für medienbasierte Inhalte durchführen, die über einen temporalen Index Windows sind. (Alle frameindizierten Inhalte enthalten auch einen temporalen Index.) Garantierte framegenaue Suchfunktionen werden im WM ASF-Reader nicht direkt unterstützt, aber es gibt eine Möglichkeit, dies zu tun, wenn Sie diese Funktionalität benötigen. Verwenden Sie zunächst das Windows Media Format SDK direkt, um eine Instanz des synchronen Readerobjekts zu erstellen, die Datei zu öffnen, den einem angegebenen Frame zugeordneten Zeitstempel zu erhalten und dann die **IMediaSeeking-Schnittstelle** von DirectShow zu verwenden, um zu diesem Zeitpunkt zu suchen. Die **IVideoFrameStep-Schnittstelle** von DirectShow unterstützt keine framegenaue Suche Windows medienbasierten Inhalten. Das DSSeekFm-Beispiel im Windows Media Format SDK veranschaulicht, wie Frame-genaue Suchungen mithilfe des WM ASF-Readers erfolgen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**WM ASF-Readerfilter**](wm-asf-reader-filter.md)
</dt> </dl>

 

 




