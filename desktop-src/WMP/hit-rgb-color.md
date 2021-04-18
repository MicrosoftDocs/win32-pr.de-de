---
title: RGB-Farbe
description: RGB-Farbe
ms.assetid: b71a0a66-11aa-4a21-b78a-3bd90f80a428
keywords:
- Windows Media Player Mobile Skins, Schaltflächen Farben
- Skins, Schaltflächen Farben
- Verweis für Skins, Schaltflächen
- Schaltflächen in Skins, Farben
- Farb Verweis für Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c69863c4197702383f729c8d7e8d30d3cb52bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340640"
---
# <a name="hit-rgb-color"></a>RGB-Farbe

Wenn Sie die Bereichs Schaltflächen (pushhit, degglehit und 2pushhit) verwenden, müssen Sie die Farbe definieren, mit der Windows Media Player den Trefferbereich der Schaltfläche bestimmen soll. Dieser Wert muss mithilfe von drei positiven ganzen Zahlen angegeben werden, die durch Kommas getrennt sind. Diese ganzen Zahlen stellen die Menge von rot, grün und blau für eine bitmapfarbe dar und reichen von 0 bis 255.

> [!Note]  
> Schaltflächen Typen sind in Skins für Windows Media Player 10 Mobile oder höher veraltet.

 

Sie können für die Werte beliebige Farben verwenden. Stellen Sie jedoch sicher, dass jede von Ihnen definierte Regions Schaltfläche eine eindeutige Farbe in der Regions Bilddatei aufweist und dass der Farbwert, den Sie hier als Zahl definieren, mit der im Regions Bild verwendeten tatsächlichen Farbe übereinstimmt.

In der folgenden Tabelle werden einige typische Farben angezeigt, die Sie möglicherweise verwenden möchten.



| Wert       | BESCHREIBUNG |
|-------------|-------------|
| 0, 0, 0       | Schwarz       |
| 255.255.255 | Weiß       |
| 255, 0, 0     | Red         |
| RGB, 0     | Grün       |
| 0, RGB     | Blau        |



 

Wenn Sie keine Bereichs Schaltflächen verwenden, müssen Sie Folgendes eingeben:


```C++
0,0,0

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schaltflächen**](buttons.md)
</dt> </dl>

 

 




