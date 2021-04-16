---
description: Das folgende Codebeispiel zeigt die Verwendung eines Mutex-Objekts, um zu bestimmen, ob MSN Explorer angemeldet ist.
ms.assetid: ec52a61c-9d2c-4327-977b-fb13d042bc37
title: Ermitteln, ob MSN im Anmeldestatus ist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba2d7af3511035c997493f0439a8635c1a928a75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523960"
---
# <a name="determining-if-msn-is-in-the-sign-in-state"></a>Ermitteln, ob MSN im Anmeldestatus ist

Das folgende Codebeispiel zeigt die Verwendung eines Mutex-Objekts, um zu bestimmen, ob MSN Explorer angemeldet ist. Wenn Sie die Verwendung des Handles abgeschlossen haben, stellen Sie sicher, dass Sie die [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) -Funktion aufgerufen haben.

> [!Note]  
> Dieses Mutex-Objekt ist für die Überprüfung von MSN Explorer 7 verfügbar. *x* -Anmeldestatus. Er ist möglicherweise in nachfolgenden Versionen nicht verfügbar.

 


```C++
    HANDLE hMSNSignedInMutex;

    hMSNSignedInMutex = OpenMutex(SYNCHRONIZE, FALSE, 
        "{ECCC50B5-064B-4693-B104-925714A4C74B}");

    if (hMSNSignedInMutex != NULL)
    {
        // MSN Explorer is signed in
    }
```



 

 
