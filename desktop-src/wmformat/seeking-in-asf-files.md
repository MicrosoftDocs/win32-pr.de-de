---
title: Suchen in ASF-Dateien (Windows Media Format 11 SDK)
description: Suchen in ASF-Dateien
ms.assetid: a1717cb4-9f41-4148-b088-a6517be7da9b
keywords:
- Windows Media-Format-SDK, suchen in ASF-Dateien
- Windows Media-Format-SDK, DirectShow
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), suchen
- ASF (Advanced Systems Format), suchen
- DirectShow, suchen in ASF-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18389ded80f0202564cba0ce6384b5ff02d26fdd
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039933"
---
# <a name="seeking-in-asf-files-windows-media-format-11-sdk"></a>Suchen in ASF-Dateien (Windows Media Format 11 SDK)

Der [WM-ASF-Reader](wm-asf-reader-filter.md)kann über seine **imediaseeking** -Schnittstelle eine sehr genaue Temporale Suche auf Windows Media – basierten Inhalten mit einem temporalen Index durchführen. (Alle Frame indizierten Inhalte enthalten auch einen temporalen Index.) Garantierte Frame-exakte Suchvorgänge werden im WM-ASF-Reader nicht direkt unterstützt. es gibt jedoch eine Möglichkeit, dies zu tun, wenn Sie diese Funktionalität benötigen. Verwenden Sie zunächst das Windows Media-Format-SDK direkt zum Erstellen einer Instanz des synchronen Reader-Objekts, öffnen Sie die Datei, rufen Sie den einem angegebenen Frame zugeordneten Zeitstempel ab, und verwenden Sie dann die Schnittstelle DirectShow **imediaseeking** , um zu diesem Zeitpunkt zu suchen. Die DirectShow **ivideoframestep** -Schnittstelle unterstützt keine Frame genaue Suche von Windows Media – basierten Inhalten. Das dsseekfm-Beispiel im Windows Media-Format-SDK veranschaulicht, wie Sie eine Frame genaue Suche mithilfe des WM-ASF-Readers durchführen können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**WM-ASF-Lesefilter**](wm-asf-reader-filter.md)
</dt> </dl>

 

 




