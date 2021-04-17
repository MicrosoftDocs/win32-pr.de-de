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
# <a name="using-playsound-to-loop-sounds"></a><span data-ttu-id="1f93e-109">Verwenden von PlaySound für Schleifen Klänge</span><span class="sxs-lookup"><span data-stu-id="1f93e-109">Using PlaySound to Loop Sounds</span></span>

<span data-ttu-id="1f93e-110">Wenn Sie die snd \_ -Schleife und die "snd \_ Async"-Flags für den *fdwsound* -Parameter der [**PlaySound**](/previous-versions//dd743680(v=vs.85)) -Funktion angeben, wird der Sound weiterhin wiederholt abgespielt, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="1f93e-110">If you specify the SND\_LOOP and SND\_ASYNC flags for the *fdwSound* parameter of the [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function, the sound will continue to play repeatedly as shown in the following example:</span></span>


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_LOOP | SND_ASYNC); 
```



<span data-ttu-id="1f93e-111">Wenn Sie einen Soundschleifen möchten, müssen Sie ihn asynchron wiedergeben. Das snd- \_ synchronisierungsflag kann nicht mit dem snd-Schleifen Kennzeichen verwendet werden \_ .</span><span class="sxs-lookup"><span data-stu-id="1f93e-111">If you want to loop a sound, you must play it asynchronously; you cannot use the SND\_SYNC flag with the SND\_LOOP flag.</span></span> <span data-ttu-id="1f93e-112">Ein Schleifen Sound wird weiterhin abgespielt, bis Sie **PlaySound** zum Abspielen eines weiteren Sounds aufruft.</span><span class="sxs-lookup"><span data-stu-id="1f93e-112">A looped sound will continue to play until you call **PlaySound** to play another sound.</span></span> <span data-ttu-id="1f93e-113">Verwenden Sie die folgende Anweisung, um die Wiedergabe eines Sounds (Schleife oder asynchron) zu unterbinden, ohne einen anderen Sound wiedergeben zu müssen:</span><span class="sxs-lookup"><span data-stu-id="1f93e-113">To stop playing a sound (looped or asynchronous) without playing another sound, use the following statement:</span></span>


```C++
PlaySound(NULL, NULL, 0); 
```



 

 