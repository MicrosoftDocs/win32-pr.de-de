---
title: Öffnen von Streams in einer AVI-Datei und Schließen der Datei
description: Öffnen von Streams in einer AVI-Datei und Schließen der Datei
ms.assetid: 3c6afa04-3d95-48cd-b468-7167bac07d46
keywords:
- AVIFileGetStream-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ca06378862ec543e9da8f671eca50841c85d744
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206584"
---
# <a name="opening-streams-in-an-avi-file-and-closing-the-file"></a><span data-ttu-id="d28e2-104">Öffnen von Streams in einer AVI-Datei und Schließen der Datei</span><span class="sxs-lookup"><span data-stu-id="d28e2-104">Opening Streams in an AVI File and Closing the File</span></span>

<span data-ttu-id="d28e2-105">Im folgenden Beispiel werden alle Streams in einer AVI-Datei mithilfe der [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream) -Funktion geöffnet.</span><span class="sxs-lookup"><span data-stu-id="d28e2-105">The following example opens all the streams in an AVI file using the [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream) function.</span></span> <span data-ttu-id="d28e2-106">Wenn ein Fehler auftritt, wird die Datei geschlossen.</span><span class="sxs-lookup"><span data-stu-id="d28e2-106">If an error is encountered, the file is closed.</span></span>


```C++
// InsertAVIFile - opens the streams in an AVI file. 
// 
// pfile - file-interface pointer from AVIFileOpen 
// 
// Global variables 
// gcpavi - count of the number of streams in an AVI file 
// gapavi[] = array of stream-interface pointers 
 
void InsertAVIFile(PAVIFILE pfile, HWND hwnd, LPSTR lpszFile) 
{ 
    int    i; 
    gcpavi = 0; 
 
    // Open the streams until a stream is not available. 
    for (i = gcpavi; i < MAXNUMSTREAMS; i++) { 
        gapavi[i] = NULL; 
        if (AVIFileGetStream(pfile, &gapavi[i], 0L, i - gcpavi) 
            != AVIERR_OK) 
        break; 
 
    if (gapavi[i] == NULL) 
        break; 
    } 
    // Display error message-stream not found. 
    if (gcpavi == i) 
    { 
        // Handle failure.
        if (pfile) // If file is open, close it 
            AVIFileRelease(pfile); 
        return; 
    } 
    else { 
        gcpavi = i - 1; 
    } 
 
//  . 
//  . Place functions to process data here. 
//  . 
} 
 
```



 

 




