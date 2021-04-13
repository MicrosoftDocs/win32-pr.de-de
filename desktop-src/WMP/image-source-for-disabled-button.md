---
title: Bildquelle für deaktivierte Schaltfläche
description: Bildquelle für deaktivierte Schaltfläche
ms.assetid: 6c50e0bd-c174-4335-8d34-ae25feec9ec6
keywords:
- Windows Media Player Mobile Skins, Schaltflächen Bildquelle
- Skins, Schaltflächen Bildquelle
- Verweis für Skins, Schaltflächen
- Schaltflächen in Skins, Bildquelle
- Bildquelle für Skins, Schaltflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05ccd0362f3dd11acec71eaf0b92574f2c27c77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388334"
---
# <a name="image-source-for-disabled-button"></a>Bildquelle für deaktivierte Schaltfläche

Sie müssen die Quelle des Abbilds definieren, das angezeigt werden soll, wenn eine Schaltfläche deaktiviert ist oder einen Zustand aufweist, der auf OFF festgelegt ist. Das Bild stammt aus der Datei, die Sie im Abschnitt Bitmaps als deaktiviert definiert haben. Sie müssen den Bildtyp gefolgt von einem Leerzeichen und dem @-Symbol und einem weiteren Leerzeichen eingeben. Sie müssen dann zwei positive ganze Zahlen eingeben, die die oberen linken Koordinaten (in Pixel) des Bilds definieren, das Sie in der Bitmapdatei verwenden möchten. Der Speicherort, an dem das Bild angezeigt wird, stammt aus den Koordinaten, die für die Schaltfläche relativ zum Hintergrundbild definiert sind, aber der Speicherort, von dem Sie stammt, wird durch die beiden Zahlen definiert, die nach "deaktiviertem @" stehen, und ist relativ zur deaktivierten Bitmap, aus der das Bild

Verwenden Sie z. b. den folgenden Code, um ein Bild aus der deaktivierten Bitmap zu verwenden, das sich in der deaktivierten Datei an einer oberen und linken Position von 50, 60 Pixeln befindet:


```C++
Disabled @ 50,60

```



Sie müssen eine deaktivierte Bitmap definieren. Wenn Sie kein anderes Bild anzeigen möchten, können Sie die Hintergrund Bitmap als deaktivierte Bitmap mit einem Offset von 0 (null) definieren:


```C++
Disabled @ 50,60

```



Im vorherigen Beispiel ist 50, 60 der Speicherort der Schaltfläche, mit der Sie in der deaktivierten Datei arbeiten (in diesem Fall der gleiche Speicherort wie die Schaltfläche auf der Hintergrund Bitmap). Es wird jedoch dringend empfohlen, dass Sie ein deaktiviertes Bild für alle Schaltflächen anzeigen, um Ihren Benutzern einen visuellen Hinweis zu geben, da viele Schaltflächen unter bestimmten Bedingungen nicht verwendbar sind, wie z. b. eine leere Wiedergabeliste. Wenn Benutzer wissen, dass eine Schaltfläche deaktiviert ist, versuchen Sie nicht, darauf zu klicken, oder denken Sie daran, dass Ihre Skin nicht wie vorgesehen funktioniert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schaltflächen**](buttons.md)
</dt> </dl>

 

 




