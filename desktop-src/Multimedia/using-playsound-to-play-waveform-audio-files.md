---
title: Verwenden von PlaySound zum Abspielen von Waveform-Audio Dateien
description: Verwenden von PlaySound zum Abspielen von Waveform-Audio Dateien
ms.assetid: 8b7d191b-6b0c-4dff-84de-cb3a5c314b80
keywords:
- Wellenform-Audio, PlaySound-Funktion
- Wellenform-Audiodatei, Abspielen von Dateien
- Wellenform-Audiodatei, WAV-Dateinamenerweiterung
- PlaySound-Funktion, experimentieren von Waveform-Audiodateien
- Wiedergabe von Waveform-Audiodateien, PlaySound-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9d5dde46827b7892217f760c749e75e19f368f5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948734"
---
# <a name="using-playsound-to-play-waveform-audio-files"></a><span data-ttu-id="07b3f-108">Verwenden von PlaySound zum Abspielen von Waveform-Audio Dateien</span><span class="sxs-lookup"><span data-stu-id="07b3f-108">Using PlaySound to Play Waveform-Audio Files</span></span>

<span data-ttu-id="07b3f-109">Die meisten Waveform-Audiodateien verwenden den. WAV-Dateinamenerweiterung.</span><span class="sxs-lookup"><span data-stu-id="07b3f-109">Most waveform-audio files use the .WAV filename extension.</span></span>

<span data-ttu-id="07b3f-110">Mit der folgenden Anweisung werden die C: \\ Sounds- \\ Glocken abgespielt. WAV-Datei:</span><span class="sxs-lookup"><span data-stu-id="07b3f-110">The following statement plays the C:\\SOUNDS\\BELLS.WAV file:</span></span>


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_SYNC); 
```



<span data-ttu-id="07b3f-111">Wenn die angegebene Datei nicht vorhanden ist oder die Datei nicht in den verfügbaren Arbeitsspeicher passt, gibt [**PlaySound**](/previous-versions//dd743680(v=vs.85)) den Standardsystem Sound wieder.</span><span class="sxs-lookup"><span data-stu-id="07b3f-111">If the specified file does not exist, or if the file does not fit into the available memory, [**PlaySound**](/previous-versions//dd743680(v=vs.85)) plays the default system sound.</span></span> <span data-ttu-id="07b3f-112">Wenn kein standardmäßiger System Sound definiert wurde, schlägt **PlaySound** fehl, ohne einen Sound zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="07b3f-112">If no default system sound has been defined, **PlaySound** fails without producing any sound.</span></span> <span data-ttu-id="07b3f-113">Wenn Sie nicht möchten, dass der standardmäßige System Sound wiedergegeben wird, geben Sie das snd- \_ NODEFAULT-Flag an, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="07b3f-113">If you do not want the default system sound to play, specify the SND\_NODEFAULT flag, as shown in the following example:</span></span>


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_SYNC | SND_NODEFAULT); 
```



 

 