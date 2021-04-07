---
title: Ändern der e/a-Puffergröße
description: Ändern der e/a-Puffergröße
ms.assetid: eff97399-143e-477b-bb16-7305e83a2317
keywords:
- Multimedia-Datei-e/a, Ändern der Puffergröße
- Datei-e/a, Ändern der Puffergröße
- Eingabe und Ausgabe (e/a), Ändern der Puffergröße
- E/a (Eingabe und Ausgabe), Ändern der Puffergröße
- Ändern der e/a-Puffergröße
- nicht gepufferte e/a
- gepufferte e/a
- mmiosetbuffer-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2171f4f09b933a3de5ec1e99750261fdda2f80
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038997"
---
# <a name="changing-the-io-buffer-size"></a>Ändern der e/a-Puffergröße

Im folgenden Beispiel wird eine Datei mit dem Namen SAMPLE.TXT für nicht gepufferte e/a-Vorgänge geöffnet. Anschließend wird die gepufferte e/a mit einem internen 16K-Puffer mithilfe der [**mmiosetbuffer**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer) -Funktion aktiviert.


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



 

 