---
title: Abschnitt "Bitmaps"
description: Abschnitt "Bitmaps"
ms.assetid: db2801e5-c55a-4681-9fe9-6027f28653e0
keywords:
- Windows Media Player Mobile Skins, Bitmaps
- Skins, Bitmaps
- Erstellen von Skins, Abschnitt "Bitmaps"
- Schreiben von Code für Skins, Abschnitt "Bitmaps"
- Bitmaps in Skins, Abschnitt "Bitmaps"
- Skindefinitionsdateien, Abschnitt "Bitmaps"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3062a8679e916fc8eaa733ab82c3df51845969873fcf83534be5f9ec6e4c6f14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573460"
---
# <a name="bitmaps-section"></a>Abschnitt "Bitmaps"

Als Nächstes benötigen Sie einen Abschnitt, der jede Ihrer Bitmapdateien definiert. Jedem Typ von Bitmap, den Sie verwenden, muss eine Datei zugewiesen sein. Sie können jedoch mehrere Typen verwenden, die dieselbe Bitmap verwenden.


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



Der Abschnitt Bitmaps muss mit dem Wort Bitmaps in Klammern beginnen und dann eine Linie für jeden Bitmaptyp, den Sie definieren möchten. In diesem Beispiel wurden fünf Arten von Bitmaps definiert. Weitere Informationen zum Abschnitt Bitmaps finden Sie unter [Bitmaps](bitmaps.md) in der Skin Reference.

> [!Note]  
> Die Bitmaps Region und Super sind in Windows Media Player 10 Mobile- oder höher-Skins veraltet.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schreiben des Codes**](writing-the-code.md)
</dt> </dl>

 

 




