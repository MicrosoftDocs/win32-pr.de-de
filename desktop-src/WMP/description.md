---
title: Beschreibung (Windows Media Player SDK)
description: Beschreibung
ms.assetid: 940ef0bf-d651-411a-b36d-99dcc01d8508
keywords:
- Windows Media Player Mobile Skins, Abschnitt "Beschreibung"
- Skins, Abschnitt "Beschreibung"
- Referenz für Skins, Abschnitt "Beschreibung"
- Beschreibungsabschnitt in Skins
- Skindefinitionsdateien, Abschnitt "Beschreibung"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 486ca5235939352ffabb924aaf38a706b436d4c1358a92b9aef4996614c53623
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749957"
---
# <a name="description-windows-media-player-sdk"></a>Beschreibung (Windows Media Player SDK)

Wenn Sie eine Skin für Windows Media Player 9 Serie für Windows Mobile 2003 oder höher erstellen, müssen Sie einen Abschnitt Beschreibung einschließen. Im Abschnitt Beschreibung können Sie die Breite und Höhe der Anzeige, die Anzeigeauflösung und die Anzeigeausrichtung angeben, für die die Skin entworfen wurde. Der Abschnitt Beschreibung muss in der Skindefinitionsdatei vor jedem anderen Abschnitt und direkt nach der anfänglichen Versionsdeklaration angezeigt werden.

Der Abschnitt Beschreibung der Skindefinitionsdatei muss mit der folgenden Zeile beginnen:


```C++
[ Description ]

```



Anschließend müssen Sie Informationen zu den Abmessungen der Skin und der Anzeigeauflösung hinzufügen. Das folgende Beispiel zeigt, wie Dimensionen angegeben werden:


```C++
//              <X,Y>       <DPI>

//              -------     -----

    Dimensions  240,320      96

```



Dies gibt an, dass Sie die Skin so entworfen haben, dass sie 240 Pixel breit, 320 Pixel hoch und mit einer Anzeigeauflösung von 96 DPI angezeigt wird. Beachten Sie, dass dies eine Ausrichtung im Hochformat impliziert.

Sie können optional den Ausrichtungsmodus angeben, für den Sie die Skin im Abschnitt beschreibung entworfen haben. Das folgende Beispiel zeigt, wie die Ausrichtung angegeben wird:


```C++
//     <Orientation>

//     -------------

    Orientation Portrait

```



In der folgenden Tabelle sind die Werte aufgeführt, die Sie für Orientation verwenden können.



| Ausrichtung | BESCHREIBUNG                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------|
| Querformat   | Die Breite der Skin ist größer als die Höhe der Skin. Die Anzeige ist horizontal ausgerichtet.   |
| Hochformat    | Die Höhe der Skin ist größer als die Breite der Skin. Die Anzeige ist vertikal ausgerichtet. |
| Square      | Die Höhe der Skin entspricht der Breite der Skin. Die Anzeige hat keine Ausrichtung.                    |



 

> [!Note]  
> Windows Media Player 9-Serie für Windows Mobile 2003 zeigt nur dann eine bestimmte Skin an, wenn der in der Skindefinitionsdatei angegebene Beschreibungsabschnitt mit dem aktuellen Zustand des Geräts übereinstimmt.

 

Achten Sie darauf, immer die richtigen Dimensionen, Auflösung und Ausrichtung anzugeben, für die Ihre Skin erstellt wurde. Wenn die von Ihrer Skin angegebenen Dimensionen beispielsweise eine Querformatausrichtung beschreiben, ist Ihre Skin nicht verfügbar, wenn sich das Gerät im Hochformat befindet, auch wenn Sie hochformatiert in der Ausrichtungslinie angeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Skin Reference**](skin-reference.md)
</dt> </dl>

 

 




