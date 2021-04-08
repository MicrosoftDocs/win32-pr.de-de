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
# <a name="creating-and-deleting-a-file"></a><span data-ttu-id="679d2-114">Erstellen und Löschen einer Datei</span><span class="sxs-lookup"><span data-stu-id="679d2-114">Creating and Deleting a File</span></span>

<span data-ttu-id="679d2-115">Um eine Datei zu erstellen, legen Sie den *dwOpenFlags* -Parameter der [**mmioopen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) -Funktion auf MMIO \_ Create fest.</span><span class="sxs-lookup"><span data-stu-id="679d2-115">To create a file, set the *dwOpenFlags* parameter of the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function to MMIO\_CREATE.</span></span> <span data-ttu-id="679d2-116">Im folgenden Beispiel wird eine Datei erstellt und zum Lesen und Schreiben geöffnet.</span><span class="sxs-lookup"><span data-stu-id="679d2-116">The following example creates a file and opens it for reading and writing.</span></span>


```C++
HMMIO hFile; 

hFile = mmioOpen("NEWFILE.TXT", NULL, MMIO_CREATE | MMIO_READWRITE); 
if (hFile != NULL) 
    // File created successfully. 
else 
    // File cannot be created. 
```



<span data-ttu-id="679d2-117">Wenn die Datei, die Sie erstellen, bereits vorhanden ist, wird Sie auf die Länge 0 (null) gekürzt.</span><span class="sxs-lookup"><span data-stu-id="679d2-117">If the file you are creating already exists, it will be truncated to zero length.</span></span>

<span data-ttu-id="679d2-118">Zum Löschen einer Datei legen Sie den *dwOpenFlags* -Parameter der **mmioopen** -Funktion auf MMIO \_ Delete fest.</span><span class="sxs-lookup"><span data-stu-id="679d2-118">To delete a file, set the *dwOpenFlags* parameter of the **mmioOpen** function to MMIO\_DELETE.</span></span> <span data-ttu-id="679d2-119">Nachdem Sie eine Datei gelöscht haben, können Sie Sie nicht mehr wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="679d2-119">After you delete a file, it cannot be recovered by any standard means.</span></span> <span data-ttu-id="679d2-120">Wenn Ihre Anwendung eine Datei auf Anforderung eines Benutzers löscht, Fragen Sie den Benutzer ab, bevor Sie die Datei löschen, um sicherzustellen, dass der Benutzer Sie löschen möchte.</span><span class="sxs-lookup"><span data-stu-id="679d2-120">If your application is deleting a file at the request of a user, query the user before deleting the file to make sure the user wants to delete it.</span></span>

 

 