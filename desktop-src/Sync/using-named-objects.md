---
description: Das folgende Beispiel veranschaulicht die Verwendung von Objektnamen durch Erstellen und Öffnen eines benannten Mutex.
ms.assetid: 06199f83-8fe0-42b9-9db1-58fe1443db4e
title: Verwenden von benannten Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24e31d21af713a28d5bee501349e818327750cba15a961ebd0f6a5295be91e0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117765129"
---
# <a name="using-named-objects"></a>Verwenden von benannten Objekten

Das folgende Beispiel veranschaulicht die Verwendung von [Objektnamen durch](object-names.md) Erstellen und Öffnen eines benannten Mutex.

## <a name="first-process"></a>Erster Prozess

Der erste Prozess verwendet die [**CreateMutex-Funktion,**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) um das Mutex-Objekt zu erstellen. Beachten Sie, dass diese Funktion auch dann erfolgreich ist, wenn ein Objekt mit demselben Namen vorhanden ist.


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

Der zweite Prozess verwendet die [**OpenMutex-Funktion,**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) um ein Handle für den vorhandenen Mutex zu öffnen. Diese Funktion schlägt fehl, wenn kein Mutex-Objekt mit dem angegebenen Namen vorhanden ist. Der Zugriffsparameter fordert Vollzugriff auf das Mutex-Objekt an, was erforderlich ist, damit das Handle in einer der Wartefunktionen verwendet werden kann.


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

 

 
