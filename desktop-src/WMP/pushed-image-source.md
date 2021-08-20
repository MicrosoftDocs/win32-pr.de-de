---
title: Übertragen der Bildquelle per Push
description: Übertragen der Bildquelle per Push
ms.assetid: 6cc290d8-2c15-4789-970d-9a3663a64d08
keywords:
- Windows Media Player Mobile Skins, Schaltflächenbildquelle
- Skins, Schaltflächenbildquelle
- Referenz für Skins, Schaltflächen
- Schaltflächen in Skins, Bildquelle
- Bildquelle für Skins, Schaltflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b336f19900b53a4ae9fff39ce76af9fe52daac4de9e94fb09dcf7b0561f1dde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861840"
---
# <a name="pushed-image-source"></a>Übertragen der Bildquelle per Push

Sie müssen die Quelle des Bilds definieren, das angezeigt werden soll, wenn der Benutzer eine Schaltfläche drückt. Das Bild stammt aus der Datei, die Sie im Abschnitt Bitmaps als Pushed definiert haben. Sie müssen den Bildtyp gefolgt von einem Leerzeichen, dem @-Symbol und einem anderen Leerzeichen eingeben. Anschließend müssen Sie zwei positive ganze Zahlen eingeben, die die obere und linke Koordinate (in Pixel) des Bilds definieren, das Sie in der Datei mit dem übertragenen Bild verwenden möchten. Die Position, an der das Bild angezeigt wird, stammt aus den Koordinaten, die für die Schaltfläche relativ zum Hintergrundbild definiert sind. aber der Speicherort, aus dem es stammt, wird durch die beiden Zahlen definiert, die auf "Pushed @" folgen, und ist relativ zu dem Gepushten Bild, aus dem Sie das Bild lesen.

Wenn Sie beispielsweise ein Bild aus dem Pushed-Image verwenden möchten, das sich in der Datei Pushed befindet, deren linker oberer Speicherort 50,60 ist, verwenden Sie den folgenden Code:


```C++
Pushed @ 50,60

```



Wenn Sie kein anderes Bild anzeigen möchten, können Sie die Hintergrundbitmap als Ihre gepushte Bitmap definieren. Geben Sie hierzu die Hintergrunddatei als Pushdatei an, und geben Sie den Offset in der linken oberen Ecke der Schaltfläche an:


```C++
Pushed @ 50,60

```



Wenn Sie dies tun, kann keine Ihrer Schaltflächen ein Per Push übertragenes Bild anzeigen. Es wird empfohlen, dass Sie für alle Schaltflächen ein Bild mit Gedrückter Taste anzeigen, um dem Benutzer einen visuellen Hinweis zu geben, da nicht immer klar ist, ob ein Tippen ein Ergebnis erzeugt, insbesondere wenn Musik wiedergegeben wird oder der Tippton ausgeschaltet ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schaltflächen**](buttons.md)
</dt> </dl>

 

 




