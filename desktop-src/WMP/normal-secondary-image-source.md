---
title: Normale sekundäre Image Quelle
description: Normale sekundäre Image Quelle
ms.assetid: fe5c0da2-0c40-456f-ab56-ac61ed69ff2d
keywords:
- Windows Media Player Mobile Skins, Schaltflächen Bildquelle
- Skins, Schaltflächen Bildquelle
- Verweis für Skins, Schaltflächen
- Schaltflächen in Skins, Bildquelle
- Bildquelle für Skins, Schaltflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ff828f6d0f0c8348453cb00fef04ab31718693
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342293"
---
# <a name="normal-secondary-image-source"></a>Normale sekundäre Image Quelle

Abhängig von der Schaltflächen Funktion müssen Sie möglicherweise den Speicherort des normalen Bilds für den sekundären Zustand der Schaltfläche definieren. Dies ist das Bild, das Benutzern angezeigt wird, wenn Sie beim ersten Mal eine PLAYPAUSE-Funktions Schaltfläche übersetzen.

Um dieses Bild zu definieren, müssen Sie den Bildtyp gefolgt von einem Leerzeichen und dem @-Symbol und einem weiteren Leerzeichen eingeben. Sie müssen dann zwei positive ganze Zahlen eingeben, die die oberen linken Koordinaten (in Pixel) des Bilds definieren, das Sie in den zu zeichnenden Bitmaptyp verwenden möchten.

Wenn Sie z. b. das normale Bild für eine sekundäre Bildquelle definieren möchten, geben Sie Folgendes ein, wenn sich das Bild in der über drückten Bitmap befindet:


```C++
Pushed @ 210,0

```



Sekundäre Zustände können nicht über ein deaktiviertes Image verfügen. Bei sekundären Images wird davon ausgegangen, dass Sie dieselbe Breite und Höhe aufweisen wie das primäre Image.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schaltflächen**](buttons.md)
</dt> </dl>

 

 




