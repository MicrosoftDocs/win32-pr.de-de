---
description: Im folgenden Beispiel wird die Verwendung von Objektnamen veranschaulicht, indem ein benannter Mutex erstellt und geöffnet wird.
ms.assetid: 06199f83-8fe0-42b9-9db1-58fe1443db4e
title: Verwenden von benannten Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a349e3e26f661ca988bc5c5ebbc7b3c6ea622956
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348636"
---
# <a name="using-named-objects"></a>Verwenden von benannten Objekten

Im folgenden Beispiel wird die Verwendung von [Objektnamen](object-names.md) veranschaulicht, indem ein benannter Mutex erstellt und geöffnet wird.

## <a name="first-process"></a>Erster Prozess

Der erste Prozess verwendet die Funktion " [**kreatemutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) ", um das Mutex-Objekt zu erstellen. Beachten Sie, dass diese Funktion auch dann erfolgreich ist, wenn ein vorhandenes Objekt mit demselben Namen vorhanden ist.


```C++
#include <windows.h>
#include <stdio.h>
#include <conio.h>

// This process creates the mutex object.

int main(void)
{
    HANDLE hMutex; 

    hMutex = CreateMutex( 
        NULL,                        // default security descriptor
        FALSE,                       // mutex not owned
        TEXT("NameOfMutexObject"));  // object name

    if (hMutex == NULL) 
        printf("CreateMutex error: %d\n", GetLastError() ); 
    else 
        if ( GetLastError() == ERROR_ALREADY_EXISTS ) 
            printf("CreateMutex opened an existing mutex\n"); 
        else printf("CreateMutex created a new mutex.\n");

    // Keep this process around until the second process is run
    _getch();

    CloseHandle(hMutex);

    return 0;
}
```



## <a name="second-process"></a>Zweiter Prozess

Der zweite Prozess verwendet die [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) -Funktion, um ein Handle für den vorhandenen Mutex zu öffnen. Diese Funktion schlägt fehl, wenn kein Mutex-Objekt mit dem angegebenen Namen vorhanden ist. Der Access-Parameter fordert Vollzugriff auf das Mutex-Objekt an, das erforderlich ist, damit das Handle in allen warte Funktionen verwendet werden kann.


```C++
#include <windows.h>
#include <stdio.h>

// This process opens a handle to a mutex created by another process.

int main(void)
{
    HANDLE hMutex; 

    hMutex = OpenMutex( 
        MUTEX_ALL_ACCESS,            // request full access
        FALSE,                       // handle not inheritable
        TEXT("NameOfMutexObject"));  // object name

    if (hMutex == NULL) 
        printf("OpenMutex error: %d\n", GetLastError() );
    else printf("OpenMutex successfully opened the mutex.\n");

    CloseHandle(hMutex);

    return 0;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Objektnamen](object-names.md)
</dt> <dt>

[Verwenden von Mutex-Objekten](using-mutex-objects.md)
</dt> </dl>

 

 
