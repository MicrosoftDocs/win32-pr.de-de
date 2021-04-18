---
title: Bildquelle für deaktivierte TrackBar
description: Bildquelle für deaktivierte TrackBar
ms.assetid: ecbe1670-2914-4b66-92bd-d854e6c1e897
keywords:
- Windows Media Player Mobile Skins, trackbars
- Skins, trackbars
- Verweis für Skins, trackbars
- trackbars in Skins, Bildquelle
- Bildquelle für Skins, trackbars
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbae540f97c7d1f7241035b074f45e6267e51615
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337988"
---
# <a name="image-source-for-disabled-trackbar"></a>Bildquelle für deaktivierte TrackBar

Sie müssen die Quelle des Bilds definieren, das Sie anzeigen möchten, wenn eine TrackBar deaktiviert ist. verwenden Sie dazu den Bitmaptyp, aus dem das Bild gezeichnet werden soll. Das Bild, das Sie anzeigen, befindet sich in der Regel in der Super Datei, oder wenn Sie ein Skin für Windows Media Player 10 Mobile erstellen, befindet sich das Bild in der seekthumb-Datei. Sie müssen den Bildtyp gefolgt von einem Leerzeichen und dem @-Symbol und einem weiteren Leerzeichen eingeben. Sie müssen dann zwei positive ganze Zahlen eingeben, die die oberen linken Koordinaten (in Pixel) des Bilds definieren, das Sie in den zu zeichnenden Bitmaptyp verwenden möchten.

Wenn Sie z. b. ein Bild aus der seekthumb-Bitmap mit einer oberen und linken Position von 50, 60 Pixeln verwenden möchten, geben Sie Folgendes ein:


```C++
Disabled @ 50,60

```



Sie müssen einen bildort für ein deaktiviertes TrackBar-Bild definieren. Wenn Sie kein neues Bild anzeigen möchten, können Sie das Hintergrundbild als deaktiviertes Bild mit einem Offset von 0 (null) definieren:


```C++
Disabled @ 50,60

```



Im vorherigen Beispiel stellt 50, 60 den Speicherort der Schaltfläche dar, mit der Sie in der seekthumb-Datei arbeiten (in diesem Fall die gleiche Position wie die Schaltfläche auf der Hintergrund Bitmap). Es wird jedoch dringend empfohlen, ein deaktiviertes Bild für alle trackbars anzuzeigen, um dem Benutzer einen visuellen Hinweis zu geben, da trackbars unter bestimmten Bedingungen nicht verwendbar sind. Beispielsweise können Such trackbars deaktiviert werden, wenn die aktuelle Wiedergabeliste leer ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Trackbars**](trackbars.md)
</dt> </dl>

 

 




