---
title: Die eigenständige Anwendung
description: Diese eigenständige Anwendung, die aus einem Aufruf einer einzelnen Funktion besteht, bildet die Grundlage unserer verteilten Anwendung.
ms.assetid: 640f5d01-84c8-4fe8-9dae-f4d55cc6f06b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 946d76d0259fd3db971da345a10108cb3dbe11c23184b4ea9a88254e4ecb5e0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923864"
---
# <a name="the-standalone-application"></a>Die eigenständige Anwendung

Diese eigenständige Anwendung, die aus einem Aufruf einer einzelnen Funktion besteht, bildet die Grundlage unserer verteilten Anwendung. Die Funktion **HelloProc wird** in einer eigenen Quelldatei definiert, sodass sie kompiliert und entweder mit einer eigenständigen Anwendung oder einer verteilten Anwendung verknüpft werden kann.


```C++
/* file hellop.c */
#include <stdio.h>
#include <windows.h>

void HelloProc(char * pszString)
{
    printf("%s\n", pszString);
}
 
/* file: hello.c, a stand-alone application */
#include "hellop.c"

void main(void)
{
    char * pszString = "Hello, World";
    HelloProc(pszString);
}
```



 

 




