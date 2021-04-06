---
title: Quelle für tertiäres Image übermittelt
description: Quelle für tertiäres Image übermittelt
ms.assetid: e2d41729-87c5-4cec-931c-8702585930f2
keywords:
- Windows Media Player Mobile Skins, Schaltflächen Bildquelle
- Skins, Schaltflächen Bildquelle
- Verweis für Skins, Schaltflächen
- Schaltflächen in Skins, Bildquelle
- Bildquelle für Skins, Schaltflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a37f79ab3c5fbf02eed1f0a02219a517b12ce1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947741"
---
# <a name="pushed-tertiary-image-source"></a>Quelle für tertiäres Image übermittelt

Die playpautsstopsfunktion erfordert, dass Sie den Speicherort des gedrückten Bilds für den tertiären Zustand der Schaltfläche definieren. Dies ist das Bild, das Benutzern angezeigt wird, wenn Sie die Schaltfläche "playpaust beenden" beim Streaming einer Liveübertragung pushen.

Um dieses Bild zu definieren, müssen Sie den Bildtyp gefolgt von einem Leerzeichen und dem @-Symbol und einem weiteren Leerzeichen eingeben. Sie müssen dann zwei positive ganze Zahlen eingeben, die die oberen linken Koordinaten (in Pixel) des Bilds definieren, das Sie in den zu zeichnenden Bitmaptyp verwenden möchten.

Wenn Sie z. b. das pushbild für eine tertiäre Bildquelle definieren möchten, geben Sie Folgendes ein, wenn sich das Bild in der über drückten Bitmap befindet:


```C++
Pushed @ 324,0

```



Tertiäre Zustände dürfen kein deaktiviertes Image aufweisen. Es wird davon ausgegangen, dass es sich um die gleiche Breite und Höhe wie die primären und sekundären Images handelt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schaltflächen**](buttons.md)
</dt> </dl>

 

 




