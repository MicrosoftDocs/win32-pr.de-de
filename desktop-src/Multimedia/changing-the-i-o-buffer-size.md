---
title: Ändern der E/A-Puffergröße
description: Ändern der E/A-Puffergröße
ms.assetid: eff97399-143e-477b-bb16-7305e83a2317
keywords:
- Multimediadatei-E/A, Ändern der Puffergröße
- Datei-E/A, Ändern der Puffergröße
- Eingabe und Ausgabe (E/A), Ändern der Puffergröße
- E/A (Eingabe und Ausgabe), Ändern der Puffergröße
- Ändern der E/A-Puffergröße
- Ungepufferte E/A
- Gepufferte E/A
- mmioSetBuffer-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 826fabfb7e51b80bf406721b3d5e7b094f83c1c3fe2061f7edea0810a41dc639
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145083"
---
# <a name="changing-the-io-buffer-size"></a>Ändern der E/A-Puffergröße

Im folgenden Beispiel wird eine Datei mit dem Namen SAMPLE.TXT für nicht gepufferte E/A geöffnet und dann gepufferte E/A mit einem internen 16K-Puffer mithilfe der [**mmioSetBuffer-Funktion**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer) aktiviert.


```C++
HMMIO hFile; 

if ((hFile = mmioOpen("SAMPLE.TXT", NULL, MMIO_READ)) != NULL) 
{ 
    // File opened successfully; request an I/O buffer. 
    if (mmioSetBuffer(hFile, NULL, 16384L, 0)) 
        // Buffer cannot be allocated. 
    else 
        // Buffer allocated successfully. 
} 
else 
    // File cannot be opened. 
```



 

 