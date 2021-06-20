---
description: Erfahren Sie, wie der WM ASF-Reader eine sehr genaue temporale Suche auf Windows Media-basierten Inhalten durchführen kann, die über einen temporalen Index in DirectShow verfügt.
ms.assetid: da0d687b-f571-4623-9705-e697ba8bc04e
title: Suchen in ASF-Dateien (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92ffc570536463b86a88e1f26be338bd748c790c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405583"
---
# <a name="seeking-in-asf-files-directshow"></a>Suchen in ASF-Dateien (DirectShow)

Der [WM ASF-Reader](wm-asf-reader-filter.md)kann über seine [**IMediaSeeking-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) sehr genaue temporale Suchmaßnahmen für Windows Media-basierte Inhalte ausführen, die einen temporalen Index haben. (Alle frameindizierten Inhalte enthalten auch einen temporalen Index.) Garantierte framegenaue Suchfunktionen werden im WM ASF-Reader nicht direkt unterstützt, aber es gibt eine Möglichkeit, dies zu tun, wenn Sie diese Funktionalität benötigen. Verwenden Sie zunächst das Windows Media Format SDK direkt, um eine Instanz des synchronen Readerobjekts zu erstellen, die Datei zu öffnen, den einem angegebenen Frame zugeordneten Zeitstempel zu erhalten und dann die DirectShow **IMediaSeeking-Schnittstelle** zu verwenden, um nach dieser Zeit zu suchen. Die [**IVideoFrameStep-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) unterstützt keine framegenaue Suche nach Windows Media-basierten Inhalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Lesen von ASF-Dateien in DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



