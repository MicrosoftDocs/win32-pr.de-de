---
title: Öffnen einer Datei mit mmioOpen
description: Öffnen einer Datei mit mmioOpen
ms.assetid: 947d1b1c-ec00-4bd9-948a-4b8e3bfb84f6
keywords:
- Multimediadatei-E/A, Öffnen von Dateien
- Datei-E/A, Öffnen von Dateien
- Eingabe und Ausgabe (E/A), Öffnen von Dateien
- E/A (Eingabe und Ausgabe),Öffnen von Dateien
- Multimediadatei-E/A,mmioOpen-Funktion
- File I/O,mmioOpen-Funktion
- Eingabe und Ausgabe (E/A), mmioOpen-Funktion
- E/A (Eingabe und Ausgabe),mmioOpen-Funktion
- mmioOpen-Funktion
- Öffnen von E/A-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffbd323e888b181b0166572d11687d3dde66e83f0ce73541555b1f49083564ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893190"
---
# <a name="opening-a-file-with-mmioopen"></a>Öffnen einer Datei mit mmioOpen

Um eine Datei für grundlegende E/A-Vorgänge zu öffnen, legen Sie den *lpmmioinfo-Parameter* der [**mmioOpen-Funktion**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) auf **NULL** fest. Im folgenden Beispiel wird eine Datei mit dem Namen "C: SAMPLESSAMPLE1.TXT" zum Lesen geöffnet \\ und der \\ Rückgabewert auf Fehler überprüft.


```C++
HMMIO hFile; 

if ((hFile = mmioOpen("C:\\SAMPLES\\SAMPLE1.TXT", NULL, 
    MMIO_READ)) != NULL) 
    // File opened successfully. 
else 
    // File cannot be opened. 
```



Verwenden Sie den *dwFlags-Parameter* von **mmioOpen,** um Flags zum Öffnen einer Datei anzugeben.

 

 