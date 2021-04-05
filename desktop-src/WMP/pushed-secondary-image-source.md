---
title: Quelle für das sekundäre Image
description: Quelle für das sekundäre Image
ms.assetid: f2a2380d-c876-456b-837b-01b3997d81f2
keywords:
- Windows Media Player Mobile Skins, Schaltflächen Bildquelle
- Skins, Schaltflächen Bildquelle
- Verweis für Skins, Schaltflächen
- Schaltflächen in Skins, Bildquelle
- Bildquelle für Skins, Schaltflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6de50f72c8af34fa4f3e44507e172cae6890dc47
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037037"
---
# <a name="pushed-secondary-image-source"></a>Quelle für das sekundäre Image

Abhängig von der Schaltflächen Funktion müssen Sie möglicherweise den Speicherort des gedrückten Bilds für den sekundären Zustand der Schaltfläche definieren. Dies ist das Bild, das Benutzern angezeigt wird, wenn Sie eine PLAYPAUSE-Funktions Schaltfläche beim zweiten Mal pushen.

Um dieses Bild zu definieren, müssen Sie den Bildtyp gefolgt von einem Leerzeichen und dem @-Symbol und einem weiteren Leerzeichen eingeben. Sie müssen dann zwei positive ganze Zahlen eingeben, die die oberen linken Koordinaten (in Pixel) des Bilds definieren, aus dem Sie zeichnen möchten.

Wenn Sie z. b. das pushbild für eine sekundäre Bildquelle definieren möchten, geben Sie Folgendes ein, wenn sich das Bild in der über drückten Bitmap befindet:


```C++
Pushed @ 248,0

```



Sekundäre Zustände können nicht über ein deaktiviertes Image verfügen. Bei sekundären Images wird davon ausgegangen, dass Sie dieselbe Breite und Höhe aufweisen wie das primäre Image.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schaltflächen**](buttons.md)
</dt> </dl>

 

 




