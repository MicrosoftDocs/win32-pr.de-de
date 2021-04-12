---
description: In Winsock-Anwendungen ist ein socketdeskriptor kein Dateideskriptor und muss mit den Winsock-Funktionen verwendet werden.
ms.assetid: bc434b35-9231-4b03-bc8f-cf59aaeb821e
title: Socket-Datentyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea031032e0d05abc02f7c3c948477c7fe9a1d1de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347068"
---
# <a name="socket-data-type"></a><span data-ttu-id="6c01a-103">Socket-Datentyp</span><span class="sxs-lookup"><span data-stu-id="6c01a-103">Socket Data Type</span></span>

<span data-ttu-id="6c01a-104">In Winsock-Anwendungen ist ein socketdeskriptor kein Dateideskriptor und muss mit den Winsock-Funktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c01a-104">In Winsock applications, a socket descriptor is not a file descriptor and must be used with the Winsock functions.</span></span>

<span data-ttu-id="6c01a-105">In Unix wird ein socketdeskriptor durch einen Standarddatei Deskriptor dargestellt.</span><span class="sxs-lookup"><span data-stu-id="6c01a-105">In UNIX, a socket descriptor is represented by a standard file descriptor.</span></span> <span data-ttu-id="6c01a-106">Folglich kann ein socketdeskriptor unter UNIX an jede der standardmäßigen Datei-e/a-Funktionen (z. b. lesen und schreiben) weitergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6c01a-106">As a result, a socket descriptor on UNIX may be passed to any of the standard file I/O functions (read and write, for example).</span></span>

<span data-ttu-id="6c01a-107">Außerdem sind alle Handles in UNIX, einschließlich Sockethandles, kleine, nicht negative ganze Zahlen, und einige Anwendungen treffen Annahmen, dass dies zutrifft.</span><span class="sxs-lookup"><span data-stu-id="6c01a-107">Furthermore, all handles in UNIX, including socket handles, are small, non-negative integers, and some applications make assumptions that this will be true.</span></span>

<span data-ttu-id="6c01a-108">Windows Sockets-Handles haben keine Einschränkungen, außer dass der Wert ungültiger \_ Socket kein gültiger Socket ist.</span><span class="sxs-lookup"><span data-stu-id="6c01a-108">Windows Sockets handles have no restrictions, other than that the value INVALID\_SOCKET is not a valid socket.</span></span> <span data-ttu-id="6c01a-109">Sockethandles können einen beliebigen Wert im Bereich 0 bis zu einem ungültigen \_ Socket – 1 annehmen.</span><span class="sxs-lookup"><span data-stu-id="6c01a-109">Socket handles may take any value in the range 0 to INVALID\_SOCKET–1.</span></span>

<span data-ttu-id="6c01a-110">Da der **socketyp** nicht signiert ist, kann das Kompilieren von vorhandenem Quellcode aus, z. b. eine UNIX-Umgebung, zu Compilerwarnungen zu nicht übereinstimmenden, nicht signierten Datentyp Konflikten führen.</span><span class="sxs-lookup"><span data-stu-id="6c01a-110">Because the **SOCKET** type is unsigned, compiling existing source code from, for example, a UNIX environment may lead to compiler warnings about signed/unsigned data type mismatches.</span></span>

<span data-ttu-id="6c01a-111">Dies bedeutet beispielsweise, dass die Überprüfung auf Fehler bei Rückgabe der [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) -und [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) -Funktionen nicht durchgeführt werden soll, indem der Rückgabewert mit – 1 verglichen wird, oder ob der Wert negativ ist (sowohl gängige als auch rechtliche Ansätze in Unix).</span><span class="sxs-lookup"><span data-stu-id="6c01a-111">This means, for example, that checking for errors when the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) and [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) functions return should not be done by comparing the return value with –1, or seeing if the value is negative (both common and legal approaches in UNIX).</span></span> <span data-ttu-id="6c01a-112">Stattdessen sollte eine Anwendung die \_ in der Header Datei " *Winsock2. h* " definierte Manifest-Konstante mit ungültigem Socket verwenden.</span><span class="sxs-lookup"><span data-stu-id="6c01a-112">Instead, an application should use the manifest constant INVALID\_SOCKET as defined in the *Winsock2.h* header file.</span></span> <span data-ttu-id="6c01a-113">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="6c01a-113">For example:</span></span>

<span data-ttu-id="6c01a-114">Typischer BSD-Unix-Stil</span><span class="sxs-lookup"><span data-stu-id="6c01a-114">Typical BSD UNIX Style</span></span>


```C++
s = socket(...);
if (s == -1)    /* or s < 0 */
    {/*...*/}
```



<span data-ttu-id="6c01a-115">Bevorzugter Stil</span><span class="sxs-lookup"><span data-stu-id="6c01a-115">Preferred Style</span></span>


```C++
s = socket(...);
if (s == INVALID_SOCKET)
    {/*...*/}
```



## <a name="related-topics"></a><span data-ttu-id="6c01a-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6c01a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c01a-117">Portieren von Socketanwendungen auf Winsock</span><span class="sxs-lookup"><span data-stu-id="6c01a-117">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="6c01a-118">Überlegungen zur Winsock-Programmierung</span><span class="sxs-lookup"><span data-stu-id="6c01a-118">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 



