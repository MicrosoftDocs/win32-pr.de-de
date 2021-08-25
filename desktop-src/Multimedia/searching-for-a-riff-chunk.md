---
title: Suchen nach einemUNK-Block
description: Suchen nach einemUNK-Block
ms.assetid: ce974fb3-3af0-4400-8f55-65d63627592a
keywords:
- Multimediadatei-E/A, Suchen nach EINEM BLOCK
- Datei-E/A, Suchen nach EINEM BLOCK
- Eingabe und Ausgabe (E/A), Suchen nach EINEM BLOCK
- E/A (Eingabe und Ausgabe), Suchen nach EINEM BLOCK
- Suchen nach einem BLOCK FÜR DIE-Suche
- Resource Interchange File Format (ENDE)
- RAFF (Dateiformat für Ressourcenaustausch)
- ORGANISATIONS-E/A
- blockunk (blockunk)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acbb09c7777cf675ceb0f11ae84fb50a3b9deaa73910ca9e15280c3fb88c42cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119782090"
---
# <a name="searching-for-a-riff-chunk"></a>Suchen nach einemUNK-Block

Im folgenden Beispiel wird die [**mmioDescend-Funktion**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) verwendet, um nach einem Block vom Typ "UNK" mit dem Formulartyp "WAVE" zu suchen, um zu überprüfen, ob es sich bei der gerade geöffneten Datei um eine Waveform-Audiodatei handelt.


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



 

 