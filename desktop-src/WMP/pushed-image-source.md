---
title: Bildquelle mit pushübertragung
description: Bildquelle mit pushübertragung
ms.assetid: 6cc290d8-2c15-4789-970d-9a3663a64d08
keywords:
- Windows Media Player Mobile Skins, Schaltflächen Bildquelle
- Skins, Schaltflächen Bildquelle
- Verweis für Skins, Schaltflächen
- Schaltflächen in Skins, Bildquelle
- Bildquelle für Skins, Schaltflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021c77a305e0f6981823c8a1e471862554c32e08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711555"
---
# <a name="pushed-image-source"></a>Bildquelle mit pushübertragung

Sie müssen die Quelle des Bilds definieren, das Sie anzeigen möchten, wenn der Benutzer eine Schaltfläche drückt. Das Bild stammt aus der Datei, die Sie im Abschnitt Bitmaps als per pushübertragung definiert haben. Sie müssen den Bildtyp gefolgt von einem Leerzeichen und dem @-Symbol und einem weiteren Leerzeichen eingeben. Sie müssen dann zwei positive ganze Zahlen eingeben, die die oberen und linken Koordinaten (in Pixel) des Bilds definieren, das Sie in der Datei mit dem pushbild verwenden möchten. Die Position, an der das Bild angezeigt wird, stammt aus den Koordinaten, die für die Schaltfläche relativ zum Hintergrundbild definiert sind. der Speicherort, von dem Sie stammt, wird jedoch durch die beiden Zahlen definiert, die auf "gedrücktes @" folgen

Wenn Sie z. b. ein Bild aus dem gedrückten Bild verwenden möchten, das sich in der über drückten Datei befindet, deren Links oben links ist, verwenden Sie den folgenden Code:


```C++
Pushed @ 50,60

```



Wenn Sie kein anderes Bild anzeigen möchten, können Sie die Bitmap des Hintergrunds als pushbitmap definieren. Geben Sie hierzu die Hintergrund Datei als die übersetzte Datei an, und geben Sie den Offset in der oberen linken Ecke der Schaltfläche an:


```C++
Pushed @ 50,60

```



Wenn Sie dies tun, kann keine der Schaltflächen ein gedrücktes Bild anzeigen. Es wird empfohlen, ein gedrücktes Bild für alle Schaltflächen anzuzeigen, um dem Benutzer einen visuellen Hinweis zu geben, denn es ist nicht immer klar, ob ein TAP ein Ergebnis liefert, insbesondere wenn Musik abgespielt wird oder der Bildschirm für das Tippen ausgeschaltet ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schaltflächen**](buttons.md)
</dt> </dl>

 

 




