---
title: Ziehpunkt Bildquelle
description: Ziehpunkt Bildquelle
ms.assetid: dca1f54d-ee79-4fd4-9c4e-8226f65c9515
keywords:
- Windows Media Player Mobile Skins, trackbars
- Skins, trackbars
- Verweis für Skins, trackbars
- trackbars in Skins, Bildquelle
- trackbars in Skins, Thumb-Bildquelle
- Bildquelle für Skins, trackbars
- Thumb, Bildquelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac19053b58c7d12543d38c639abe5a43c01ff64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036624"
---
# <a name="thumb-image-source"></a>Ziehpunkt Bildquelle

Sie müssen den Namen der Datei definieren, die das Thumb-Bild enthält. Dies muss ein gültiger Dateiname mit der Erweiterung BMP, GIF, JPG oder PNG sein. Die Datei muss drei nebeneinander Abbilder gleicher Größe enthalten. Sie müssen einander nebeneinander und ohne Leerzeichen dazwischen liegen. Die linke obere Position des linken Bilds muss sich in der linken oberen Ecke der Datei befinden. Das Bild auf der linken Seite ist das normale Bild für das Ziehpunkt Bild, und das Bild in der Mitte zeigt den gedrückten Zustand an, und das Bild auf der rechten Seite stellt den deaktivierten Zustand dar.


```C++
SeekThumb.bmp

```



Möglicherweise möchten Sie bestimmte Bereiche des Thumb-Bilds transparent machen. Auf diese Weise können Sie Thumb-Bilder in anderen Formen als rechteckig erstellen. Jeder Bereich des Zieh Punkts, den Sie mit der Farbe ausfüllen, die durch den RGB-Wert 255, 0, 255 angegeben wird, wird in der Skin als transparent angezeigt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Trackbars**](trackbars.md)
</dt> </dl>

 

 




