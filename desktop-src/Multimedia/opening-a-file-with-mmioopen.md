---
title: Öffnen einer Datei mit mmioopen
description: Öffnen einer Datei mit mmioopen
ms.assetid: 947d1b1c-ec00-4bd9-948a-4b8e3bfb84f6
keywords:
- Multimedia-Datei-e/a, Öffnen von Dateien
- Datei-e/a, Öffnen von Dateien
- Eingabe und Ausgabe (e/a), Öffnen von Dateien
- E/a (Eingabe und Ausgabe), Öffnen von Dateien
- Multimedia-Datei-e/a, mmioopen-Funktion
- Datei-e/a, mmioopen-Funktion
- Eingabe und Ausgabe (e/a), mmioopen-Funktion
- E/a (Eingabe und Ausgabe), mmioopen-Funktion
- mmioopen-Funktion
- Öffnen von e/a-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2123b73c5f3a93cbb6e72711a7137652f7534b2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473069"
---
# <a name="opening-a-file-with-mmioopen"></a><span data-ttu-id="25a2e-113">Öffnen einer Datei mit mmioopen</span><span class="sxs-lookup"><span data-stu-id="25a2e-113">Opening a File with mmioOpen</span></span>

<span data-ttu-id="25a2e-114">Zum Öffnen einer Datei für grundlegende e/a-Vorgänge legen Sie den *lpmmioinfo* -Parameter der [**mmioopen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) -Funktion auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="25a2e-114">To open a file for basic I/O operations, set the *lpmmioinfo* parameter of the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function to **NULL**.</span></span> <span data-ttu-id="25a2e-115">Im folgenden Beispiel wird eine Datei mit dem Namen "C: \\ Samples \\SAMPLE1.TXT" zum Lesen geöffnet, und der Rückgabewert wird auf Fehler überprüft.</span><span class="sxs-lookup"><span data-stu-id="25a2e-115">The following example opens a file named "C:\\SAMPLES\\SAMPLE1.TXT" for reading, and checks the return value for error.</span></span>


```C++
HMMIO hFile; 

if ((hFile = mmioOpen("C:\\SAMPLES\\SAMPLE1.TXT", NULL, 
    MMIO_READ)) != NULL) 
    // File opened successfully. 
else 
    // File cannot be opened. 
```



<span data-ttu-id="25a2e-116">Verwenden Sie den *dwFlags* -Parameter von **mmioopen** , um Flags zum Öffnen einer Datei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="25a2e-116">Use the *dwFlags* parameter of **mmioOpen** to specify flags for opening a file.</span></span>

 

 