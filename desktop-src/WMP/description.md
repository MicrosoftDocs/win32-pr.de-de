---
title: Beschreibung (Windows Media Player SDK)
description: BESCHREIBUNG
ms.assetid: 940ef0bf-d651-411a-b36d-99dcc01d8508
keywords:
- Windows Media Player Mobile Skins, Beschreibungs Abschnitt
- Skins, Beschreibungs Abschnitt
- Referenz für Skins, Beschreibungs Abschnitt
- Beschreibungs Abschnitt in Skins
- Skin-Definitions Dateien, Beschreibungs Abschnitt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4a1b714fb917f9d13ee710509cfc5bf696e3eef
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391422"
---
# <a name="description-windows-media-player-sdk"></a>Beschreibung (Windows Media Player SDK)

Wenn Sie ein Skin für Windows Media Player 9-Reihe für Windows Mobile 2003 oder höher erstellen, müssen Sie einen Beschreibungs Abschnitt einschließen. Im Abschnitt Beschreibung können Sie die Breite und Höhe der Anzeige, die Bildschirmauflösung und die Anzeige Ausrichtung angeben, für die die Skin entworfen wurde. Der Beschreibungs Abschnitt muss in der Skin-Definitionsdatei vor jedem anderen Abschnitt und unmittelbar nach der Deklaration der ersten Version angezeigt werden.

Der Beschreibungs Abschnitt der Skin-Definitionsdatei muss mit der folgenden Zeile beginnen:


```C++
[ Description ]

```



Anschließend müssen Sie Informationen zu den Dimensionen der Skin und der Bildschirmauflösung hinzufügen. Im folgenden Beispiel wird gezeigt, wie Dimensionen angegeben werden:


```C++
//              <X,Y>       <DPI>

//              -------     -----

    Dimensions  240,320      96

```



Dies gibt an, dass Sie die Skin so entworfen haben, dass Sie 240 Pixel Breite, 320 Pixel hoch und die Verwendung der 96 dpi-Anzeige Auflösung anzeigt. Beachten Sie, dass dies eine Ausrichtung im Hochformat impliziert.

Sie können optional den Orientierungs Modus angeben, für den Sie die Skin im Abschnitt Beschreibung entworfen haben. Im folgenden Beispiel wird gezeigt, wie Sie die Ausrichtung angeben:


```C++
//     <Orientation>

//     -------------

    Orientation Portrait

```



In der folgenden Tabelle sind die Werte aufgelistet, die Sie für die Ausrichtung verwenden können.



| Ausrichtung | BESCHREIBUNG                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------|
| Querformat   | Die Breite der Skin ist größer als die Höhe der Skin. Die Anzeige ist horizontal ausgerichtet.   |
| Hochformat    | Die Höhe der Skin ist größer als die Breite der Skin. Die Anzeige ist vertikal ausgerichtet. |
| Square      | Die Höhe der Skin ist gleich der Breite der Skin. Die Anzeige hat keine Ausrichtung.                    |



 

> [!Note]  
> Windows Media Player 9-Serie für Windows Mobile 2003 zeigt nur eine bestimmte Skin an, wenn der in der Skin-Definitionsdatei angegebene Beschreibungs Abschnitt mit dem aktuellen Status des Geräts übereinstimmt.

 

Sie sollten darauf achten, dass Sie immer die richtigen Dimensionen, die richtige Auflösung und die richtige Ausrichtung angeben, für die die Skin erstellt wurde. Wenn die von der Skin angegebenen Dimensionen z. b. eine Querformat Beschreibung beschreiben, ist die Skin nicht verfügbar, wenn sich das Gerät im Hochformat befindet, auch wenn Sie das Hochformat in der Leitungs Linie angeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Skin-Referenz**](skin-reference.md)
</dt> </dl>

 

 




