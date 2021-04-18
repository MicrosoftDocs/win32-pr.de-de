---
title: Übereinstimmung der Windows-Media Player Farben
description: Übereinstimmung der Windows-Media Player Farben
ms.assetid: b4d1da08-a4cf-46dd-82a5-40562bb3c049
keywords:
- Windows Media Player Online Stores, übereinstimmende Windows Media Player Farben
- Online Stores, übereinstimmende Windows-Media Player Farben
- Typ 1 Online Stores, übereinstimmende Windows-Media Player Farben
- Typ 2 Online Stores, übereinstimmende Windows-Media Player Farben
- Windows Media Player Online Stores, Windows Media Player Farbabgleich
- Online Stores, Windows Media Player Farbabgleich
- Typ 1 Online Stores, Windows Media Player Farbabgleich
- Typ 2 Online Stores, Windows Media Player Farbabgleich
- Windows Media Player Online Stores, Farbabgleich für Windows Media Player
- Online Stores, Farbabgleich für Windows-Media Player
- Typ 1 Online Stores, Farbabgleich für Windows-Media Player
- Typ 2 Online Stores, Farbabgleich für Windows Media Player
- Farbabgleich für Windows-Media Player
- übereinstimmende Windows-Media Player Farben
- Windows Media Player, übereinstimmende Farben
- Windows Media Player, Farbabgleich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eedf3e5df7c02f498c0dc21aeeed16c99452003c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340852"
---
# <a name="matching-the-windows-media-player-colors"></a>Übereinstimmung der Windows-Media Player Farben

Es ist einfach, die Online Store-Webseite mit dem Windows-Media Player Farbschema zu vergleichen. Behandeln Sie einfach das **externe. oncolorchange** -Ereignis. Wenn Sie eine Funktion zur Behandlung des Ereignisses angeben möchten, verwenden Sie Code wie den folgenden, wenn die Webseite geladen wird:


```C++
// Set up the color change event.
external.OnColorChange = OnAppColor;
```



Jedes Mal, wenn der Benutzer das Farbschema von Windows Media Player ändert, ruft der Player die Funktion auf. Das folgende Beispiel zeigt eine einfache Funktion, mit der der Webseiten Hintergrund so festgelegt wird, dass er der **externen. appcolorlight** -Eigenschaft entspricht:


```C++
// Match the current color.
function OnAppColor()
{
    window.document.bgColor = external.appColorLight;
}
```



Für ihre Verwendung stehen auch andere Farbeigenschaften zur Verfügung. Siehe [externes Objekt für den Typ 2 Online Stores](external-object-for-type-2-online-stores.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Extern. appcolorlight**](external-appcolorlight.md)
</dt> <dt>

[**Externes. oncolorchange-Ereignis**](external-oncolorchange-event.md)
</dt> <dt>

[**Informationen, die von Typ 1 und Typ 2 Online Stores gemeinsam sind**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




