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
# <a name="using-named-objects"></a><span data-ttu-id="5bfc8-103">Verwenden von benannten Objekten</span><span class="sxs-lookup"><span data-stu-id="5bfc8-103">Using Named Objects</span></span>

<span data-ttu-id="5bfc8-104">Im folgenden Beispiel wird die Verwendung von [Objektnamen](object-names.md) veranschaulicht, indem ein benannter Mutex erstellt und geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="5bfc8-104">The following example illustrates the use of [object names](object-names.md) by creating and opening a named mutex.</span></span>

## <a name="first-process"></a><span data-ttu-id="5bfc8-105">Erster Prozess</span><span class="sxs-lookup"><span data-stu-id="5bfc8-105">First Process</span></span>

<span data-ttu-id="5bfc8-106">Der erste Prozess verwendet die Funktion " [**kreatemutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) ", um das Mutex-Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5bfc8-106">The first process uses the [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) function to create the mutex object.</span></span> <span data-ttu-id="5bfc8-107">Beachten Sie, dass diese Funktion auch dann erfolgreich ist, wenn ein vorhandenes Objekt mit demselben Namen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5bfc8-107">Note that this function succeeds even if there is an existing object with the same name.</span></span>


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



## <a name="second-process"></a><span data-ttu-id="5bfc8-108">Zweiter Prozess</span><span class="sxs-lookup"><span data-stu-id="5bfc8-108">Second Process</span></span>

<span data-ttu-id="5bfc8-109">Der zweite Prozess verwendet die [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) -Funktion, um ein Handle für den vorhandenen Mutex zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5bfc8-109">The second process uses the [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) function to open a handle to the existing mutex.</span></span> <span data-ttu-id="5bfc8-110">Diese Funktion schlägt fehl, wenn kein Mutex-Objekt mit dem angegebenen Namen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5bfc8-110">This function fails if a mutex object with the specified name does not exist.</span></span> <span data-ttu-id="5bfc8-111">Der Access-Parameter fordert Vollzugriff auf das Mutex-Objekt an, das erforderlich ist, damit das Handle in allen warte Funktionen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5bfc8-111">The access parameter requests full access to the mutex object, which is necessary for the handle to be used in any of the wait functions.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="5bfc8-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5bfc8-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5bfc8-113">Objektnamen</span><span class="sxs-lookup"><span data-stu-id="5bfc8-113">Object Names</span></span>](object-names.md)
</dt> <dt>

[<span data-ttu-id="5bfc8-114">Verwenden von Mutex-Objekten</span><span class="sxs-lookup"><span data-stu-id="5bfc8-114">Using Mutex Objects</span></span>](using-mutex-objects.md)
</dt> </dl>

 

 
