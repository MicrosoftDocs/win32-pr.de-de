---
title: Bildquelle für deaktivierte Trackleiste
description: Bildquelle für deaktivierte Trackleiste
ms.assetid: ecbe1670-2914-4b66-92bd-d854e6c1e897
keywords:
- Windows Media Player Mobile Skins, Trackleisten
- Skins, Trackleisten
- Referenz für Skins, Trackleisten
- Trackbars in Skins, Bildquelle
- Bildquelle für Skins, Trackleisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6b3f5f58198d55f2dcd17b23b102c91eb4dff4787489e13775c6be71faa3223
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338945"
---
# <a name="image-source-for-disabled-trackbar"></a>Bildquelle für deaktivierte Trackleiste

Sie müssen die Quelle des Bilds definieren, das angezeigt werden soll, wenn eine Trackleiste deaktiviert ist, indem Sie den Bitmaptyp verwenden, aus dem Sie das Bild zeichnen möchten. Das angezeigte Bild befindet sich in der Regel in der Super-Datei, oder wenn Sie eine Skin für Windows Media Player 10 Mobile erstellen, befindet sich das Bild in der SeekThumb-Datei. Sie müssen den Bildtyp gefolgt von einem Leerzeichen, dem @-Symbol und einem anderen Leerzeichen eingeben. Anschließend müssen Sie zwei positive ganze Zahlen eingeben, die die Koordinaten oben links (in Pixel) des Bilds definieren, das Sie innerhalb des Bitmaptyps verwenden möchten, aus dem Sie zeichnen.

Um beispielsweise ein Bild aus der SeekThumb-Bitmap zu verwenden, das eine obere und linke Position von 50,60 Pixel aufweist, geben Sie Folgendes ein:


```C++
Disabled @ 50,60

```



Sie müssen einen Bildspeicherort für ein deaktiviertes Trackbarbild definieren. Wenn Sie kein neues Bild anzeigen möchten, können Sie das Hintergrundbild als Deaktiviertes Bild mit einem Offset von 0,0 definieren:


```C++
Disabled @ 50,60

```



Im vorherigen Beispiel stellt 50,60 den Speicherort der Schaltfläche dar, mit der Sie in der SeekThumb-Datei arbeiten (in diesem Fall die gleiche Position wie die Schaltfläche auf der Hintergrundbitmap). Es wird jedoch dringend empfohlen, ein Deaktiviert-Bild für alle Trackleisten anzuzeigen, um dem Benutzer eine visuelle Anzeige zu geben, da Trackleisten unter bestimmten Bedingungen nicht verwendet werden können. Beispielsweise können Seek-Trackleisten deaktiviert werden, wenn die aktuelle Wiedergabeliste leer ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Trackbars**](trackbars.md)
</dt> </dl>

 

 




