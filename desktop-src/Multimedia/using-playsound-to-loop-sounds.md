---
title: Verwenden von PlaySound für Schleifen Klänge
description: Verwenden von PlaySound für Schleifen Klänge
ms.assetid: 747b9a76-5ff3-488e-ba85-c4d926e1e723
keywords:
- Wellenform-Audio, PlaySound-Funktion
- Wellenform-Audio, Schleifen Klänge
- Wellenform-Audio, Parameter "f dwsound"
- PlaySound-Funktion, Schleifen Klänge
- PlaySound-Funktion, Parameter "sdwsound"
- Schleifen von Waveform-audiosounds
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5373e703c7a02068094e312dee18690a797b330e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390144"
---
# <a name="using-playsound-to-loop-sounds"></a>Verwenden von PlaySound für Schleifen Klänge

Wenn Sie die snd \_ -Schleife und die "snd \_ Async"-Flags für den *fdwsound* -Parameter der [**PlaySound**](/previous-versions//dd743680(v=vs.85)) -Funktion angeben, wird der Sound weiterhin wiederholt abgespielt, wie im folgenden Beispiel gezeigt:


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_LOOP | SND_ASYNC); 
```



Wenn Sie einen Soundschleifen möchten, müssen Sie ihn asynchron wiedergeben. Das snd- \_ synchronisierungsflag kann nicht mit dem snd-Schleifen Kennzeichen verwendet werden \_ . Ein Schleifen Sound wird weiterhin abgespielt, bis Sie **PlaySound** zum Abspielen eines weiteren Sounds aufruft. Verwenden Sie die folgende Anweisung, um die Wiedergabe eines Sounds (Schleife oder asynchron) zu unterbinden, ohne einen anderen Sound wiedergeben zu müssen:


```C++
PlaySound(NULL, NULL, 0); 
```



 

 