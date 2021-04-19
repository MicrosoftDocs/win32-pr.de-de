---
title: Zugreifen auf einen Datei-e/a-Puffer
description: Zugreifen auf einen Datei-e/a-Puffer
ms.assetid: b829d8ef-8e0b-4c30-b8cf-e9feccc63bbf
keywords:
- Multimedia-Datei-e/a, zugreifen auf Puffer
- Datei-e/a, zugreifen auf Puffer
- Eingabe und Ausgabe (e/a), zugreifen auf Puffer
- E/a (Eingabe und Ausgabe), zugreifen auf Puffer
- Zugreifen auf e/a-Puffer
- gepufferte e/a
- mmioabtinfo-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57c89b2376f1bae68d55c76d7731b6ee78f6bf7d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106338458"
---
# <a name="accessing-a-file-io-buffer"></a><span data-ttu-id="36942-110">Zugreifen auf einen Datei-e/a-Puffer</span><span class="sxs-lookup"><span data-stu-id="36942-110">Accessing a File I/O Buffer</span></span>

<span data-ttu-id="36942-111">Im folgenden Beispiel wird direkt auf einen e/a-Puffer zugegriffen, um Daten aus einer Waveform-Audiodatei zu lesen.</span><span class="sxs-lookup"><span data-stu-id="36942-111">The following example accesses an I/O buffer directly to read data from a waveform-audio file.</span></span>


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



<span data-ttu-id="36942-112">Wenn Sie den Zugriff auf einen Datei-e/a-Puffer abgeschlossen haben, können Sie die [**mmioabtinfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo) -Funktion aufrufen und dabei eine Adresse der [**mmioinfo**](/previous-versions//dd757322(v=vs.85)) -Struktur übergeben, die von der [**mmiogetinfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo) -Funktion ausgefüllt wird</span><span class="sxs-lookup"><span data-stu-id="36942-112">When you finish accessing a file I/O buffer, call the [**mmioSetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo) function, passing an address of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure filled by the [**mmioGetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo) function.</span></span> <span data-ttu-id="36942-113">Wenn Sie in den Puffer geschrieben haben, legen Sie das MMIO- \_ Flag "Dirty" im **dwFlags** -Member der **mmioinfo** -Struktur vor dem Aufruf von **mmiosetinfo** fest.</span><span class="sxs-lookup"><span data-stu-id="36942-113">If you wrote to the buffer, set the MMIO\_DIRTY flag in the **dwFlags** member of the **MMIOINFO** structure before calling **mmioSetInfo**.</span></span> <span data-ttu-id="36942-114">Andernfalls wird der Puffer nicht auf den Datenträger geleert.</span><span class="sxs-lookup"><span data-stu-id="36942-114">Otherwise, the buffer will not be flushed to disk.</span></span>

 

 