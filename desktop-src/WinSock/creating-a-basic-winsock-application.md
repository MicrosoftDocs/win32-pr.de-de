---
description: Erstellen einer grundlegenden Windows Sockets (Winsock)-Anwendung
ms.assetid: 56af2e95-ea82-49e4-b335-86dcf4c38780
title: Erstellen einer grundlegenden Winsock-Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0d5b5695ddb3b329bb4f81da6149fcf740a4240
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129208"
---
# <a name="creating-a-basic-winsock-application"></a><span data-ttu-id="53dd6-103">Erstellen einer grundlegenden Winsock-Anwendung</span><span class="sxs-lookup"><span data-stu-id="53dd6-103">Creating a Basic Winsock Application</span></span>

<span data-ttu-id="53dd6-104">**So erstellen Sie eine Winsock-Basisanwendung**</span><span class="sxs-lookup"><span data-stu-id="53dd6-104">**To create a basic Winsock application**</span></span>

1.  <span data-ttu-id="53dd6-105">Erstellen Sie ein neues leeres Projekt.</span><span class="sxs-lookup"><span data-stu-id="53dd6-105">Create a new empty project.</span></span>
2.  <span data-ttu-id="53dd6-106">Fügen Sie dem Projekt eine leere C++-Quelldatei hinzu.</span><span class="sxs-lookup"><span data-stu-id="53dd6-106">Add an empty C++ source file to the project.</span></span>
3.  <span data-ttu-id="53dd6-107">Stellen Sie sicher, dass sich die Buildumgebung auf das include-, lib-und src-Verzeichnis des Microsoft Windows Software Development Kit (SDK) oder auf dem früheren Platform Software Development Kit (SDK) bezieht.</span><span class="sxs-lookup"><span data-stu-id="53dd6-107">Ensure that the build environment refers to the Include, Lib, and Src directories of the Microsoft Windows Software Development Kit (SDK) or the earlier Platform Software Development Kit (SDK).</span></span>
4.  <span data-ttu-id="53dd6-108">Stellen Sie sicher, dass die Buildumgebung mit der Winsock-Bibliotheksdatei Ws2 \_ 32. lib verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="53dd6-108">Ensure that the build environment links to the Winsock Library file Ws2\_32.lib.</span></span> <span data-ttu-id="53dd6-109">Anwendungen, die Winsock verwenden, müssen mit der \_ Bibliotheksdatei Ws2 32. lib verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="53dd6-109">Applications that use Winsock must be linked with the Ws2\_32.lib library file.</span></span> <span data-ttu-id="53dd6-110">Der \# pragma-Kommentar weist den Linker an, dass die Datei *Ws2 \_ 32. lib* benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="53dd6-110">The \#pragma comment indicates to the linker that the *Ws2\_32.lib* file is needed.</span></span>
5.  <span data-ttu-id="53dd6-111">Beginnen Sie mit dem Programmieren der Winsock-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="53dd6-111">Begin programming the Winsock application.</span></span> <span data-ttu-id="53dd6-112">Verwenden Sie die Winsock-API, indem Sie die Winsock 2-Header Dateien einschließen.</span><span class="sxs-lookup"><span data-stu-id="53dd6-112">Use the Winsock API by including the Winsock 2 header files.</span></span> <span data-ttu-id="53dd6-113">Die Header Datei " *Winsock2. h* " enthält die meisten WinSock-Funktionen,-Strukturen und-Definitionen.</span><span class="sxs-lookup"><span data-stu-id="53dd6-113">The *Winsock2.h* header file contains most of the Winsock functions, structures, and definitions.</span></span> <span data-ttu-id="53dd6-114">Die Header Datei " *Ws2tcpip. h* " enthält Definitionen, die im Winsock 2-Protocol-Specific Anhang-Dokument für TCP/IP eingeführt wurden und neuere Funktionen und Strukturen enthalten, die zum Abrufen von IP-Adressen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="53dd6-114">The *Ws2tcpip.h* header file contains definitions introduced in the WinSock 2 Protocol-Specific Annex document for TCP/IP that includes newer functions and structures used to retrieve IP addresses.</span></span>
    > [!Note]  
    > <span data-ttu-id="53dd6-115">Stdio. h wird für die Standardeingabe und-Ausgabe verwendet, insbesondere die **printf ()** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="53dd6-115">Stdio.h is used for standard input and output, specifically the **printf()** function.</span></span>

     


```C++
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



> [!Note]
>
> <span data-ttu-id="53dd6-116">Die Header Datei " *iphlpapi. h* " ist erforderlich, wenn eine Anwendung die IP-hilfsprogrammapis verwendet.</span><span class="sxs-lookup"><span data-stu-id="53dd6-116">The *Iphlpapi.h* header file is required if an application is using the IP Helper APIs.</span></span> <span data-ttu-id="53dd6-117">Wenn die Header Datei " *iphlpapi. h* " erforderlich ist, \# sollte die includezeile für die Header Datei " *Winsock2. h* " vor der \# Include-Zeile für die Header Datei " *iphlpapi. h* " platziert werden.</span><span class="sxs-lookup"><span data-stu-id="53dd6-117">When the *Iphlpapi.h* header file is required, the \#include line for the *Winsock2.h* header file should be placed before the \#include line for the *Iphlpapi.h* header file.</span></span>
>
> <span data-ttu-id="53dd6-118">Die Header Datei " *Winsock2. h* " enthält intern Kernelemente aus der Header Datei " *Windows. h* ", sodass \# in Winsock-Anwendungen normalerweise keine Include-Zeile für die Header Datei " *Windows. h* " vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="53dd6-118">The *Winsock2.h* header file internally includes core elements from the *Windows.h* header file, so there is not usually an \#include line for the *Windows.h* header file in Winsock applications.</span></span> <span data-ttu-id="53dd6-119">Wenn eine \# Include-Zeile für die Header Datei " *Windows. h* " erforderlich ist, sollte diesem das \# Win32 \_ \_ -und Mean-Makro definiert werden \_ .</span><span class="sxs-lookup"><span data-stu-id="53dd6-119">If an \#include line is needed for the *Windows.h* header file, this should be preceded with the \#define WIN32\_LEAN\_AND\_MEAN macro.</span></span> <span data-ttu-id="53dd6-120">Aus historischen Gründen hat der *Windows. h* -Header standardmäßig die *Winsock. h* -Header Datei für Windows Sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="53dd6-120">For historical reasons, the *Windows.h* header defaults to including the *Winsock.h* header file for Windows Sockets 1.1.</span></span> <span data-ttu-id="53dd6-121">Die Deklarationen in der Header Datei " *Winsock. h* " verursachen einen Konflikt mit den Deklarationen in der *Winsock2. h* -Header Datei, die von Windows Sockets 2,0 benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="53dd6-121">The declarations in the *Winsock.h* header file will conflict with the declarations in the *Winsock2.h* header file required by Windows Sockets 2.0.</span></span> <span data-ttu-id="53dd6-122">Das Win32 \_ \_ -und \_ Mean-Makro verhindert, dass die *Winsock. h* -Datei vom *Windows. h* -Header eingeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="53dd6-122">The WIN32\_LEAN\_AND\_MEAN macro prevents the *Winsock.h* from being included by the *Windows.h* header.</span></span> <span data-ttu-id="53dd6-123">Im folgenden wird ein Beispiel gezeigt, das dies veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="53dd6-123">An example illustrating this is shown below.</span></span>

 


```C++
#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <windows.h>
#include <winsock2.h>
#include <ws2tcpip.h>
#include <iphlpapi.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



<span data-ttu-id="53dd6-124">Nächster Schritt: [Initialisieren von Winsock](initializing-winsock.md)</span><span class="sxs-lookup"><span data-stu-id="53dd6-124">Next Step: [Initializing Winsock](initializing-winsock.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="53dd6-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="53dd6-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53dd6-126">Einstieg in Winsock</span><span class="sxs-lookup"><span data-stu-id="53dd6-126">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="53dd6-127">Informationen zu Servern und Clients</span><span class="sxs-lookup"><span data-stu-id="53dd6-127">About Servers and Clients</span></span>](about-clients-and-servers.md)
</dt> </dl>

 

 



