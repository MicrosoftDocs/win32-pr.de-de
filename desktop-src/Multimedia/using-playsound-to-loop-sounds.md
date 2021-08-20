---
title: Verwenden von PlaySound zum Schleifen von Sounds
description: Verwenden von PlaySound zum Schleifen von Sounds
ms.assetid: 747b9a76-5ff3-488e-ba85-c4d926e1e723
keywords:
- Waveform-Audio, PlaySound-Funktion
- Waveformaudio, Schleifengeräusche
- Waveform-Audio, fdwSound-Parameter
- PlaySound-Funktion, Schleifengeräusche
- PlaySound-Funktion, fdwSound-Parameter
- Looping waveform-audio sounds
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf97321a72ab566bf622e725700dbf336ddba6d92b9b8e6df9150357492656f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136118"
---
# <a name="using-playsound-to-loop-sounds"></a>Verwenden von PlaySound zum Schleifen von Sounds

Wenn Sie die Flags SND \_ LOOP und SND \_ ASYNC für den *fdwSound-Parameter* der [**PlaySound-Funktion**](/previous-versions//dd743680(v=vs.85)) angeben, wird der Sound wie im folgenden Beispiel gezeigt wiederholt wiedergegeben:


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_LOOP | SND_ASYNC); 
```



Wenn Sie einen Sound in einer Schleife durchlaufen möchten, müssen Sie ihn asynchron wiedergeben. Sie können das SND \_ SYNC-Flag nicht mit dem SND \_ LOOP-Flag verwenden. Ein Schleifenton wird weiterhin wiedergegeben, bis Sie **PlaySound** aufrufen, um einen anderen Sound wiederzuspielen. Verwenden Sie die folgende Anweisung, um die Wiedergabe eines Sounds (looped oder asynchron) zu beenden, ohne einen anderen Sound wiederzuspielen:


```C++
PlaySound(NULL, NULL, 0); 
```



 

 