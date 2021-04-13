---
title: Suchen einer neuen Position in einer Datei
description: Suchen einer neuen Position in einer Datei
ms.assetid: 276c3e43-bf9f-4a0a-b33a-7eaa701e92a6
keywords:
- Multimedia-Datei-e/a, verschieben an den Anfang von Dateien
- Datei-e/a, verschieben an den Anfang von Dateien
- Eingabe und Ausgabe (e/a), verschieben an den Anfang von Dateien
- E/a (Eingabe und Ausgabe), verschieben an den Anfang von Dateien
- Wechseln zum Anfang von e/a-Dateien
- Multimedia-Datei-e/a, Suche nach neuer Position in Dateien
- Datei-e/a, Suche nach neuer Position in Dateien
- Eingabe und Ausgabe (e/a), Suchen neuer Positionen in Dateien
- E/a (Eingabe und Ausgabe), neue Position in Dateien suchen
- Suchen neuer Positionen in e/a-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 949ca3e9d118fdd83e5b53ae9336ad8ab601c64b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314672"
---
# <a name="seeking-to-a-new-position-in-a-file"></a><span data-ttu-id="7248e-113">Suchen einer neuen Position in einer Datei</span><span class="sxs-lookup"><span data-stu-id="7248e-113">Seeking to a New Position in a File</span></span>

<span data-ttu-id="7248e-114">Im folgenden Beispiel wird mithilfe der [**mmioseek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) -Funktion an den Anfang einer geöffneten Datei verschoben.</span><span class="sxs-lookup"><span data-stu-id="7248e-114">The following example moves to the beginning of an open file using the [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) function.</span></span>


```C++
mmioSeek(hFile, 0L, SEEK_SET); 
```



<span data-ttu-id="7248e-115">Das folgende Beispiel wechselt zum Ende einer geöffneten Datei.</span><span class="sxs-lookup"><span data-stu-id="7248e-115">The following example moves to the end of an open file.</span></span>


```C++
mmioSeek(hFile, 0L, SEEK_END); 
```



<span data-ttu-id="7248e-116">Im folgenden Beispiel wird vom Ende einer geöffneten Datei an eine Position von 10 Bytes verschoben.</span><span class="sxs-lookup"><span data-stu-id="7248e-116">The following example moves to a position 10 bytes from the end of an open file.</span></span>


```C++
mmioSeek(hFile, -10L, SEEK_END); 

```



 

 