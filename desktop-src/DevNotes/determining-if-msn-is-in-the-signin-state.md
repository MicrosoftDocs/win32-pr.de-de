---
description: Das folgende Codebeispiel zeigt die Verwendung eines mutex-Objekts, um zu bestimmen, ob MSN Explorer angemeldet ist.
ms.assetid: ec52a61c-9d2c-4327-977b-fb13d042bc37
title: Bestimmen, ob sich MSN im Anmeldestatus befindet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5da0abffc1735d2bf7af6ee6f9a68bf0d71ca1a2fda44176a0905c3e8faec6d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654191"
---
# <a name="determining-if-msn-is-in-the-sign-in-state"></a>Bestimmen, ob sich MSN im Anmeldestatus befindet

Das folgende Codebeispiel zeigt die Verwendung eines mutex-Objekts, um zu bestimmen, ob MSN Explorer angemeldet ist. Wenn Sie das Handle nicht mehr verwenden, rufen Sie unbedingt die [**CloseHandle-Funktion**](/windows/win32/api/handleapi/nf-handleapi-closehandle) auf.

> [!Note]  
> Dieses Mutex-Objekt kann bei der Überprüfung von MSN Explorer 7 verwendet werden.  x-Anmeldestatus. In nachfolgenden Versionen ist sie möglicherweise nicht verfügbar.

 


```C++
    HANDLE hMSNSignedInMutex;

    hMSNSignedInMutex = OpenMutex(SYNCHRONIZE, FALSE, 
        "{ECCC50B5-064B-4693-B104-925714A4C74B}");

    if (hMSNSignedInMutex != NULL)
    {
        // MSN Explorer is signed in
    }
```



 

 
