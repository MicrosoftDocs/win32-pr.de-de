---
title: Normale sekundäre Bildquelle
description: Normale sekundäre Bildquelle
ms.assetid: fe5c0da2-0c40-456f-ab56-ac61ed69ff2d
keywords:
- Windows Media Player Mobile Skins, Schaltflächenbildquelle
- Skins, Schaltflächenbildquelle
- Referenz für Skins, Schaltflächen
- Schaltflächen in Skins, Bildquelle
- Bildquelle für Skins, Schaltflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f6aeb48ceabc873d4aeb0db910db896712fe16377aa0f67b76205ad8a39c83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118573730"
---
# <a name="normal-secondary-image-source"></a>Normale sekundäre Bildquelle

Abhängig von der Schaltflächenfunktion müssen Sie möglicherweise den Speicherort des normalen Bilds für den sekundären Zustand der Schaltfläche definieren. Dies ist das Bild, das Benutzern angezeigt wird, wenn sie zum ersten Mal eine PlayPause-Funktionsschaltfläche drücken.

Um dieses Bild zu definieren, müssen Sie den Bildtyp gefolgt von einem Leerzeichen, dem @-Symbol und einem anderen Leerzeichen eingeben. Anschließend müssen Sie zwei positive ganze Zahlen eingeben, die die Koordinaten oben links (in Pixel) des Bilds definieren, das Sie innerhalb des Bitmaptyps verwenden möchten, aus dem Sie zeichnen.

Wenn Sie z. B. das normale Bild für eine sekundäre Bildquelle definieren möchten, geben Sie Folgendes ein, wenn sich das Bild in der Bitmap mitHilfe von Push befindet:


```C++
Pushed @ 210,0

```



Sekundäre Zustände können kein Deaktiviert-Image aufweisen. Es wird davon ausgegangen, dass sekundäre Images die gleiche Breite und Höhe wie das primäre Image aufweisen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schaltflächen**](buttons.md)
</dt> </dl>

 

 




