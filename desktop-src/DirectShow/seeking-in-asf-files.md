---
description: Suchen in ASF-Dateien
ms.assetid: da0d687b-f571-4623-9705-e697ba8bc04e
title: Suchen in ASF-Dateien (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e957fbdf7ed7df1a9cb38b14e39d384b15ab25b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521288"
---
# <a name="seeking-in-asf-files-directshow"></a>Suchen in ASF-Dateien (DirectShow)

Der [WM-ASF-Reader](wm-asf-reader-filter.md)kann über seine [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) -Schnittstelle eine sehr genaue Temporale Suche auf Windows Media – basierten Inhalten mit einem temporalen Index durchführen. (Alle Frame indizierten Inhalte enthalten auch einen temporalen Index.) Garantierte Frame-exakte Suchvorgänge werden im WM-ASF-Reader nicht direkt unterstützt. es gibt jedoch eine Möglichkeit, dies zu tun, wenn Sie diese Funktionalität benötigen. Verwenden Sie zunächst das Windows Media-Format-SDK direkt zum Erstellen einer Instanz des synchronen Reader-Objekts, öffnen Sie die Datei, rufen Sie den einem angegebenen Frame zugeordneten Zeitstempel ab, und verwenden Sie dann die Schnittstelle DirectShow **imediaseeking** , um zu diesem Zeitpunkt zu suchen. Die [**ivideoframestep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) -Schnittstelle unterstützt keine Frame genaue Suche von Windows Media – basierten Inhalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Lesen von ASF-Dateien in DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



