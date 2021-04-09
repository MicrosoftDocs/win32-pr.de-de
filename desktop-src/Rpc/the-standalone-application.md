---
title: Die eigenständige Anwendung
description: Diese eigenständige Anwendung, die aus einem Rückruf einer einzelnen Funktion besteht, bildet die Grundlage der verteilten Anwendung.
ms.assetid: 640f5d01-84c8-4fe8-9dae-f4d55cc6f06b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddf1b11df2372a1db5c74659d1800b62e53b7309
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036958"
---
# <a name="the-standalone-application"></a>Die eigenständige Anwendung

Diese eigenständige Anwendung, die aus einem Rückruf einer einzelnen Funktion besteht, bildet die Grundlage der verteilten Anwendung. Die **helloproc**-Funktion wird in ihrer eigenen Quelldatei definiert, sodass Sie kompiliert und mit einer eigenständigen Anwendung oder einer verteilten Anwendung verknüpft werden kann.


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



 

 




