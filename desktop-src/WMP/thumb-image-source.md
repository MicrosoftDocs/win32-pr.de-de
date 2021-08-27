---
title: Thumb Image Source
description: Thumb Image Source
ms.assetid: dca1f54d-ee79-4fd4-9c4e-8226f65c9515
keywords:
- Windows Media Player Mobile Skins, Trackbars
- Skins, Trackbars
- Referenz für Skins, Trackbars
- Trackleisten in Skins, Bildquelle
- Trackleisten in Skins, Quelle des Fingerabdruckbilds
- Bildquelle für Skins, Trackleisten
- Thumb, Bildquelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550569a2858ba283824f28f6793097caa140c6112bccc41b3423413e17b6d89a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122770"
---
# <a name="thumb-image-source"></a>Thumb Image Source

Sie müssen den Namen der Datei definieren, die das Fingerabdruckbild enthält. Dies muss ein gültiger Dateiname mit der Erweiterung .bmp, .gif, .jpg oder .png. Die Datei muss drei nebeneinander gespeicherte Bilder identischer Größe enthalten. Sie müssen ohne Leerzeichen nebeneinander liegen. Die linke obere Position des linken Bilds muss in der linken oberen Ecke der Datei stehen. Das Bild auf der linken Seite ist das normale Bild für das Daumenbild, und das Bild in der Mitte stellt den zustandsbewegten Push und das Bild auf der rechten Seite den deaktivierten Zustand wieder.


```C++
SeekThumb.bmp

```



Möglicherweise möchten Sie bestimmte Bereiche des Fingerabdruckbilds transparent machen. Auf diese Weise können Sie Thumb-Bilder in anderen Formen als rechteckigen Erstellen. Jeder Bereich des Daumenbilds, den Sie mit der durch den RGB-Wert 255, 0, 255 angegebenen Farbe füllen, wird in Ihrer Skin transparent angezeigt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Trackbars**](trackbars.md)
</dt> </dl>

 

 




