---
title: Übereinstimmung mit Windows Media Player Farben
description: Übereinstimmung mit Windows Media Player Farben
ms.assetid: b4d1da08-a4cf-46dd-82a5-40562bb3c049
keywords:
- Windows Media Player online stores,matching Windows Media Player colors
- Onlineshops,übereinstimmende Windows Media Player Farben
- Typ 1 Onlineshops,übereinstimmende Windows Media Player Farben
- Typ 2 Onlineshops,übereinstimmende Windows Media Player Farben
- Windows Media Player onlineshops,Windows Media Player Farbabgleich
- Onlineshops,Windows Media Player Farbabgleich
- Typ 1 Onlineshops,Windows Media Player Farbabgleich
- Typ 2 Onlineshops,Windows Media Player Farbabgleich
- Windows Media Player Onlineshops, Farbabgleich für Windows Media Player
- Onlineshops,Farbabgleich für Windows Media Player
- Typ 1 Onlineshops,Farbvergleich für Windows Media Player
- Typ 2 Onlineshops,Farbvergleich für Windows Media Player
- Farbvergleich für Windows Media Player
- Übereinstimmende Windows Media Player Farben
- Windows Media Player,übereinstimmende Farben
- Windows Media Player,Farbabgleich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3dbb7ed8b73973d35bc8ad884109c569d1c4738d038cf48f657068c5bde51bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135183"
---
# <a name="matching-the-windows-media-player-colors"></a>Übereinstimmung mit Windows Media Player Farben

Es ist einfach, die Webseite Ihres Onlineshops Windows Media Player farblich zu ändern. Behandeln Sie einfach **das External.OnColorChange-Ereignis.** Um eine Funktion zum Behandeln des Ereignisses anzugeben, verwenden Sie code wie den folgenden, wenn Ihre Webseite geladen wird:


```C++
// Set up the color change event.
external.OnColorChange = OnAppColor;
```



Jedes Mal, wenn der Benutzer das Farbschema der Windows Media Player ändert, wird der Player Ihre Funktion aufrufen. Das folgende Beispiel zeigt eine einfache Funktion, die den Webseitenhintergrund auf die Übereinstimmung mit der **External.appColorLight-Eigenschaft** legt:


```C++
// Match the current color.
function OnAppColor()
{
    window.document.bgColor = external.appColorLight;
}
```



Es stehen auch andere Farbeigenschaften zur Verfügung, die Sie verwenden können. Weitere Informationen [finden Sie unter Externes Objekt für Type 2 Online Stores](external-object-for-type-2-online-stores.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**External.appColorLight**](external-appcolorlight.md)
</dt> <dt>

[**External.OnColorChange-Ereignis**](external-oncolorchange-event.md)
</dt> <dt>

[**Allgemeine Informationen zu Onlineshops vom Typ 1 und 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




