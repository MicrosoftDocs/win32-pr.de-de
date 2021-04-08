---
title: Erstellen und Löschen einer Datei
description: Erstellen und Löschen einer Datei
ms.assetid: a4b4a310-7230-4f1d-b084-c47db39adaac
keywords:
- Multimedia-Datei-e/a, Erstellen von Dateien
- Datei-e/a, Erstellen von Dateien
- Eingabe und Ausgabe (e/a), Erstellen von Dateien
- E/a (Eingabe und Ausgabe), Erstellen von Dateien
- Erstellen von e/a-Dateien
- Multimedia-Datei-e/a, Löschen von Dateien
- Datei-e/a, Löschen von Dateien
- Eingabe und Ausgabe (e/a), Löschen von Dateien
- E/a (Eingabe und Ausgabe), Löschen von Dateien
- Löschen von e/a-Dateien
- mmioopen-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c22cd6330874d0b5da74d69193359c025c709c79
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725369"
---
# <a name="creating-and-deleting-a-file"></a>Erstellen und Löschen einer Datei

Um eine Datei zu erstellen, legen Sie den *dwOpenFlags* -Parameter der [**mmioopen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) -Funktion auf MMIO \_ Create fest. Im folgenden Beispiel wird eine Datei erstellt und zum Lesen und Schreiben geöffnet.


```C++
HMMIO hFile; 

hFile = mmioOpen("NEWFILE.TXT", NULL, MMIO_CREATE | MMIO_READWRITE); 
if (hFile != NULL) 
    // File created successfully. 
else 
    // File cannot be created. 
```



Wenn die Datei, die Sie erstellen, bereits vorhanden ist, wird Sie auf die Länge 0 (null) gekürzt.

Zum Löschen einer Datei legen Sie den *dwOpenFlags* -Parameter der **mmioopen** -Funktion auf MMIO \_ Delete fest. Nachdem Sie eine Datei gelöscht haben, können Sie Sie nicht mehr wiederherstellen. Wenn Ihre Anwendung eine Datei auf Anforderung eines Benutzers löscht, Fragen Sie den Benutzer ab, bevor Sie die Datei löschen, um sicherzustellen, dass der Benutzer Sie löschen möchte.

 

 