---
title: Erstellen und Löschen einer Datei
description: Erstellen und Löschen einer Datei
ms.assetid: a4b4a310-7230-4f1d-b084-c47db39adaac
keywords:
- Multimediadatei-E/A, Erstellen von Dateien
- Datei-E/A, Erstellen von Dateien
- Eingabe und Ausgabe (E/A), Erstellen von Dateien
- E/A (Eingabe und Ausgabe), Erstellen von Dateien
- Erstellen von E/A-Dateien
- Multimediadatei-E/A, Löschen von Dateien
- Datei-E/A, Löschen von Dateien
- Eingabe und Ausgabe (E/A), Löschen von Dateien
- E/A (Eingabe und Ausgabe), Löschen von Dateien
- Löschen von E/A-Dateien
- mmioOpen-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91a2ee8e70508e2c5dc3b24c084cf0b081b6629a519703ef43a15845ef3ec76a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785730"
---
# <a name="creating-and-deleting-a-file"></a>Erstellen und Löschen einer Datei

Legen Sie zum Erstellen einer Datei den *dwOpenFlags-Parameter* der [**mmioOpen-Funktion**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) auf MMIO \_ CREATE fest. Im folgenden Beispiel wird eine Datei erstellt und zum Lesen und Schreiben geöffnet.


```C++
HMMIO hFile; 

hFile = mmioOpen("NEWFILE.TXT", NULL, MMIO_CREATE | MMIO_READWRITE); 
if (hFile != NULL) 
    // File created successfully. 
else 
    // File cannot be created. 
```



Wenn die Datei, die Sie erstellen, bereits vorhanden ist, wird sie auf die Länge 0 (null) gekürzt.

Legen Sie zum Löschen einer Datei den *dwOpenFlags-Parameter* der **mmioOpen-Funktion** auf MMIO \_ DELETE fest. Nachdem Sie eine Datei gelöscht haben, kann sie nicht mehr standardmäßig wiederhergestellt werden. Wenn Ihre Anwendung eine Datei auf Anforderung eines Benutzers löscht, fragen Sie den Benutzer ab, bevor Sie die Datei löschen, um sicherzustellen, dass der Benutzer sie löschen möchte.

 

 