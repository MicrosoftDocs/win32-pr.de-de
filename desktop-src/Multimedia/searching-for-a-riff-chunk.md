---
title: Suchen nach einem Riff Block
description: Suchen nach einem Riff Block
ms.assetid: ce974fb3-3af0-4400-8f55-65d63627592a
keywords:
- Multimedia-Datei-e/a, suchen nach einem Riff Block
- Datei-e/a, suchen nach einem Riff Block
- Eingabe und Ausgabe (e/a), suchen nach einem Riff Block
- E/a (Eingabe und Ausgabe), suchen nach einem Riff Block
- Suchen nach einem Riff Block
- Format der Ressourcenaustausch Datei (Riff)
- Riff (Ressourcenaustausch-Dateiformat)
- Riff-e/a
- Riff Block
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b45b2182e44ac84423c29a79fe29e96820d5bf2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390321"
---
# <a name="searching-for-a-riff-chunk"></a><span data-ttu-id="3c2bf-112">Suchen nach einem Riff Block</span><span class="sxs-lookup"><span data-stu-id="3c2bf-112">Searching for a RIFF Chunk</span></span>

<span data-ttu-id="3c2bf-113">Im folgenden Beispiel wird die [**mmioabstieg**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) -Funktion verwendet, um nach einem "Riff"-Block mit dem Formulartyp "Wave" zu suchen, um zu überprüfen, ob es sich bei der soeben geöffneten Datei um eine Waveform-Audiodatei handelt.</span><span class="sxs-lookup"><span data-stu-id="3c2bf-113">The following example uses the [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) function to search for a "RIFF" chunk with a form type of "WAVE" to verify that the file that has just been opened is a waveform-audio file.</span></span>


```C++
HMMIO    hmmio; 
MMCKINFO mmckinfoParent; 
MMCKINFO mmckinfoSubchunk; 
. 
. 
. 
// Locate a "RIFF" chunk with a "WAVE" form type to make 
// sure the file is a waveform-audio file. 
mmckinfoParent.fccType = mmioFOURCC('W', 'A', 'V', 'E'); 
if (mmioDescend(hmmio, (LPMMCKINFO) &mmckinfoParent, NULL, 
    MMIO_FINDRIFF)) 
    // The file is not a waveform-audio file. 
else 
    // The file is a waveform-audio file 

```



 

 