---
title: Pushed Secondary Image Source
description: Pushed Secondary Image Source
ms.assetid: f2a2380d-c876-456b-837b-01b3997d81f2
keywords:
- Windows Media Player Mobile Skins, Schaltflächenbildquelle
- Skins, Schaltflächenbildquelle
- Referenz für Skins, Schaltflächen
- Schaltflächen in Skins, Bildquelle
- Bildquelle für Skins, Schaltflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37045da71b8417856ec72ac7e57a6a787426ba486993b9fef03910b4d32e663d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861830"
---
# <a name="pushed-secondary-image-source"></a>Pushed Secondary Image Source

Abhängig von der Schaltflächenfunktion müssen Sie möglicherweise den Speicherort des pushierten Bilds für den sekundären Zustand der Schaltfläche definieren. Dies ist das Bild, das Benutzern angezeigt wird, wenn sie beim zweiten Mal eine PlayPause-Funktionsschaltfläche drücken.

Um dieses Bild zu definieren, müssen Sie den Bildtyp gefolgt von einem Leerzeichen, dem @-Symbol und einem anderen Leerzeichen eingeben. Anschließend müssen Sie zwei positive ganze Zahlen eingeben, die die oberen linken Koordinaten (in Pixel) des Bilds definieren, das Sie innerhalb des Bildtyps verwenden möchten, aus dem Sie zeichnen.

Geben Sie z. B. Folgendes ein, um das pushed-Bild für eine sekundäre Bildquelle zu definieren, wenn sich Das Bild in der Bitmap "Pushed" befindet:


```C++
Pushed @ 248,0

```



Sekundäre Zustände dürfen kein Deaktiviert-Image haben. Es wird davon ausgegangen, dass sekundäre Bilder die gleiche Breite und Höhe wie das primäre Bild haben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schaltflächen**](buttons.md)
</dt> </dl>

 

 




