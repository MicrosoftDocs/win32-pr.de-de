---
title: Zugreifen auf einen Datei-E/A-Puffer
description: Zugreifen auf einen Datei-E/A-Puffer
ms.assetid: b829d8ef-8e0b-4c30-b8cf-e9feccc63bbf
keywords:
- Multimediadatei-E/A, Zugreifen auf Puffer
- Datei-E/A, Zugreifen auf Puffer
- Eingabe und Ausgabe (E/A), Zugreifen auf Puffer
- E/A (Eingabe und Ausgabe),Zugreifen auf Puffer
- Zugreifen auf E/A-Puffer
- Gepufferte E/A
- mmioSetInfo-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e4ab9533f0f121d42f859961b60d405477856faacee8d8cf36a0dfb975e2587
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808640"
---
# <a name="accessing-a-file-io-buffer"></a>Zugreifen auf einen Datei-E/A-Puffer

Im folgenden Beispiel wird direkt auf einen E/A-Puffer zugegriffen, um Daten aus einer Waveform-Audiodatei zu lesen.


```C++
HMMIO    hmmio; 
MMIOINFO mmioinfo; 
DWORD    dwDataSize; 
DWORD    dwCount; 
HPSTR    hptr; 

// Get information about the file I/O buffer. 
if (mmioGetInfo(hmmio, &mmioinfo, 0)) 
{ 
    Error("Failed to get I/O buffer info."); 
    . 
    . 
    . 
    mmioClose(hmmio, 0); 
    return; 
} 
 
// Read the entire file by directly reading the file I/O buffer. 
// When the end of the I/O buffer is reached, advance the buffer. 

for (dwCount = dwDataSize, hptr = lpData; dwCount  0; dwCount--) 
{ 
    // Check to see if the I/O buffer must be advanced. 
    if (mmioinfo.pchNext == mmioinfo.pchEndRead) 
    { 
        if(mmioAdvance(hmmio, &mmioinfo, MMIO_READ)) 
        { 
            Error("Failed to advance buffer."); 
            . 
            . 
            . 
            mmioClose(hmmio, 0); 
            return; 
        } 
    } 
 
    // Get a character from the buffer. 
    *hptr++ = *mmioinfo.pchNext++; 
} 
 
// End direct buffer access and close the file. 
mmioSetInfo(hmmio, &mmioinfo, 0); 
mmioClose(hmmio, 0); 

```



Wenn Sie den Zugriff auf einen Datei-E/A-Puffer abgeschlossen haben, rufen Sie die [**mmioSetInfo-Funktion**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo) auf, und übergeben Sie eine Adresse der [**MMIOINFO-Struktur,**](/previous-versions//dd757322(v=vs.85)) die von der [**mmioGetInfo-Funktion**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo) gefüllt wird. Wenn Sie in den Puffer geschrieben haben, legen Sie das MMIO \_ DIRTY-Flag im **dwFlags-Member** der **MMIOINFO-Struktur** fest, bevor **Sie mmioSetInfo** aufrufen. Andernfalls wird der Puffer nicht auf den Datenträger geleert.

 

 