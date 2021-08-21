---
title: Suchen nach einer neuen Position in einer Datei
description: Suchen nach einer neuen Position in einer Datei
ms.assetid: 276c3e43-bf9f-4a0a-b33a-7eaa701e92a6
keywords:
- Multimediadatei-E/A, Verschieben an den Anfang der Dateien
- Datei-E/A, Verschieben zum Anfang der Dateien
- Eingabe und Ausgabe (E/A), Verschieben zum Anfang der Dateien
- E/A (Eingabe und Ausgabe), Verschieben zum Anfang der Dateien
- Verschieben an den Anfang von E/A-Dateien
- Multimediadatei-E/A, Suche nach neuer Position in Dateien
- Datei-E/A, Suche nach neuer Position in Dateien
- Eingabe und Ausgabe (E/A), Suche nach einer neuen Position in Dateien
- E/A (Eingabe und Ausgabe), Suche nach neuer Position in Dateien
- Suchen nach einer neuen Position in E/A-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97e51ab51065bcdf89af84f2fd622558261dd4cf42cac3e50fe54fb116a7ad9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136584"
---
# <a name="seeking-to-a-new-position-in-a-file"></a>Suchen nach einer neuen Position in einer Datei

Das folgende Beispiel wechselt mithilfe der [**mmioSeek-Funktion**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) an den Anfang einer geöffneten Datei.


```C++
mmioSeek(hFile, 0L, SEEK_SET); 
```



Das folgende Beispiel wechselt an das Ende einer geöffneten Datei.


```C++
mmioSeek(hFile, 0L, SEEK_END); 
```



Im folgenden Beispiel wird vom Ende einer geöffneten Datei an eine Position von 10 Bytes bewegt.


```C++
mmioSeek(hFile, -10L, SEEK_END); 

```



 

 