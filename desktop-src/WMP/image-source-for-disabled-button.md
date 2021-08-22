---
title: Bildquelle für deaktivierte Schaltfläche
description: Bildquelle für deaktivierte Schaltfläche
ms.assetid: 6c50e0bd-c174-4335-8d34-ae25feec9ec6
keywords:
- Windows Media Player Mobile Skins, Schaltflächenbildquelle
- Skins, Schaltflächenbildquelle
- Referenz für Skins, Schaltflächen
- Schaltflächen in Skins, Bildquelle
- Bildquelle für Skins, Schaltflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 071a3b31a25eb40d82d33f241a6eaebf690fe11aa2128528739a7e7bbb4dc217
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119509260"
---
# <a name="image-source-for-disabled-button"></a>Bildquelle für deaktivierte Schaltfläche

Sie müssen die Quelle des Bilds definieren, das angezeigt werden soll, wenn eine Schaltfläche deaktiviert ist oder einen Status auf "off" hat. Das Bild stammt aus der Datei, die Sie im Abschnitt Bitmaps als Deaktiviert definiert haben. Sie müssen den Bildtyp gefolgt von einem Leerzeichen, dem @-Symbol und einem anderen Leerzeichen eingeben. Anschließend müssen Sie zwei positive ganze Zahlen eingeben, die die Koordinaten oben links (in Pixel) des Bilds definieren, das Sie in der Bitmapdatei verwenden möchten. Die Position, an der das Bild angezeigt wird, stammt aus den Koordinaten, die für die Schaltfläche relativ zum Hintergrundbild definiert sind. Die Position, aus der es stammt, wird jedoch durch die beiden Zahlen definiert, die auf "Disabled @" folgen, und ist relativ zur Bitmap Disabled, aus der Sie das Bild lesen.

Verwenden Sie beispielsweise den folgenden Code, um ein Bild aus der Bitmap Deaktiviert zu verwenden, das sich in der Datei Deaktiviert an einer oberen und linken Position von 50,60 Pixel befindet:


```C++
Disabled @ 50,60

```



Sie müssen eine Disabled-Bitmap definieren. Wenn Sie kein anderes Bild anzeigen möchten, können Sie die Hintergrundbitmap als Deaktivierte Bitmap mit einem Offset von 0,0 definieren:


```C++
Disabled @ 50,60

```



Im vorherigen Beispiel ist 50,60 der Speicherort der Schaltfläche, mit der Sie in der Datei Deaktiviert arbeiten (in diesem Fall derselbe Speicherort wie die Schaltfläche in der Hintergrundbitmap). Es wird jedoch dringend empfohlen, ein Deaktiviert-Bild für alle Schaltflächen anzuzeigen, um Ihren Benutzern eine visuelle Anzeige zu geben, da viele Schaltflächen unter bestimmten Bedingungen nicht verwendet werden können, z. B. einer leeren Wiedergabeliste. Wenn Benutzer wissen, dass eine Schaltfläche deaktiviert ist, versuchen sie nicht weiter, darauf zu klicken, oder denken, dass Ihre Skin nicht wie vorgesehen funktioniert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schaltflächen**](buttons.md)
</dt> </dl>

 

 




