---
title: Abschnitt "Bitmaps"
description: Abschnitt "Bitmaps"
ms.assetid: db2801e5-c55a-4681-9fe9-6027f28653e0
keywords:
- Windows Media Player Mobile Skins, Bitmaps
- Skins, Bitmaps
- Erstellen von Skins, Bitmaps (Abschnitt)
- Schreiben von Code für Skins, Bitmaps (Abschnitt)
- Bitmaps in Skins, Bitmaps (Abschnitt)
- Skin-Definitions Dateien, Abschnitt "Bitmaps"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4a5e41e8e2b095b199a072e31abde3c1cbaa29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036879"
---
# <a name="bitmaps-section"></a>Abschnitt "Bitmaps"

Als nächstes müssen Sie über einen Abschnitt verfügen, der die einzelnen Bitmapdateien definiert. Jedem Bitmaptyp, den Sie verwenden, muss eine Datei zugewiesen sein, aber Sie können über mehrere Typen mit derselben Bitmap verfügen.


```C++
[ Bitmaps ]

//  <Name>      <File name>     <X,Y>
//  ------      -----------     -----
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0

```



Der Abschnitt Bitmaps muss mit dem Wort Bitmaps in eckigen Klammern und dann einer Zeile für jeden Bitmaptyp beginnen, den Sie definieren möchten. In diesem Beispiel wurden fünf Typen von Bitmaps definiert. Weitere Informationen zum Abschnitt Bitmaps finden Sie unter [Bitmaps](bitmaps.md) in der Skin-Referenz.

> [!Note]  
> Die Region und die Super Bitmaps sind in Windows Media Player 10 Mobile oder höher als veraltet markiert.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schreiben des Codes**](writing-the-code.md)
</dt> </dl>

 

 




