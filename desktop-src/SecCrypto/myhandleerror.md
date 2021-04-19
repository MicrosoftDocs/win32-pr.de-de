---
description: Die mylenker Error-Funktion ist ein Beispiel für eine Tool Funktion, mit der eine Fehlermeldung gedruckt und das aufrufende Programm beendet wird.
ms.assetid: 7b28509f-a77f-4b60-90d4-18edaa6d1a2d
title: Mylenker Error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 047c9642a1b19c2af4a6e5ef2134ca305c472c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357017"
---
# <a name="myhandleerror"></a>Mylenker Error

Die **mylenker Error** -Funktion ist ein Beispiel für eine Tool Funktion, mit der eine Fehlermeldung gedruckt und das aufrufende Programm beendet wird. In den Beispielen für verschiedene CryptoAPI-Funktionen in der [kryptografiereferenz](cryptography-reference.md) und in den ausführlicheren Beispielen bei der [Verwendung von Cryptography](using-cryptography.md) wird diese Funktion implementiert. Echte Anwendungen erfordern möglicherweise komplexere Fehler Behandlungs Funktionen.


```C++
#include <stdio.h>
#include <tchar.h>
#include <windows.h>

void MyHandleError(LPTSTR psz)
{
    _ftprintf(stderr, TEXT("An error occurred in the program. \n"));
    _ftprintf(stderr, TEXT("%s\n"), psz);
    _ftprintf(stderr, TEXT("Error number %x.\n"), GetLastError());
    _ftprintf(stderr, TEXT("Program terminating. \n"));
    exit(1);
} // End of MyHandleError

```



 

 



