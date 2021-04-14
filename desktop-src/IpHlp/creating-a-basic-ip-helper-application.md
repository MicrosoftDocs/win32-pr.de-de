---
description: Erstellen einer grundlegenden IP-Hilfsanwendung
ms.assetid: b53f1cf5-3659-407e-8279-5c94333f3017
title: Erstellen einer grundlegenden IP-Hilfsanwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baae961f8ffb6aa899e96fd05f0cb9f0c41469ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350268"
---
# <a name="creating-a-basic-ip-helper-application"></a><span data-ttu-id="ea1b9-103">Erstellen einer grundlegenden IP-Hilfsanwendung</span><span class="sxs-lookup"><span data-stu-id="ea1b9-103">Creating a Basic IP Helper Application</span></span>

<span data-ttu-id="ea1b9-104">**So erstellen Sie eine Basis-IP-Hilfsanwendung**</span><span class="sxs-lookup"><span data-stu-id="ea1b9-104">**To create a basic IP Helper application**</span></span>

1.  <span data-ttu-id="ea1b9-105">Erstellen Sie ein neues leeres Projekt.</span><span class="sxs-lookup"><span data-stu-id="ea1b9-105">Create a new empty project.</span></span>
2.  <span data-ttu-id="ea1b9-106">Fügen Sie dem Projekt eine leere C++-Quelldatei hinzu.</span><span class="sxs-lookup"><span data-stu-id="ea1b9-106">Add an empty C++ source file to the project.</span></span>
3.  <span data-ttu-id="ea1b9-107">Stellen Sie sicher, dass sich die Buildumgebung auf das include-, lib-und src-Verzeichnis des Platform Software Development Kit (SDK) bezieht.</span><span class="sxs-lookup"><span data-stu-id="ea1b9-107">Ensure that the build environment refers to the Include, Lib, and Src directories of the Platform Software Development Kit (SDK).</span></span>
4.  <span data-ttu-id="ea1b9-108">Stellen Sie sicher, dass die Buildumgebung mit der IP-hilfsbibliotheks Datei iphlpapi. lib und der Winsock-Bibliotheksdatei ws2 \_ 32. lib verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="ea1b9-108">Ensure that the build environment links to the IP Helper Library file Iphlpapi.lib and the Winsock Library file WS2\_32.lib.</span></span>
    > [!Note]  
    > <span data-ttu-id="ea1b9-109">Einige grundlegende Winsock-Funktionen werden verwendet, um IP-Adress Werte und andere Informationen zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="ea1b9-109">Some basic Winsock functions are used to return IP address values and other information.</span></span>

     

5.  <span data-ttu-id="ea1b9-110">Beginnen Sie mit der Programmierung der IP-Hilfsanwendung.</span><span class="sxs-lookup"><span data-stu-id="ea1b9-110">Begin programming the IP Helper application.</span></span> <span data-ttu-id="ea1b9-111">Verwenden Sie die IP-hilfsprogrammapi, indem Sie die IP-hilfheaderdatei einschließen</span><span class="sxs-lookup"><span data-stu-id="ea1b9-111">Use the IP Helper API by including the IP Helper header file.</span></span>

    ```C++
    #include <winsock2.h>
    #include <iphlpapi.h>
    #include <stdio.h>

    int main() {
      return 0;
    }
    
    ```

    

    > [!Note]
    >
    > <span data-ttu-id="ea1b9-112">Die Header Datei " *iphlpapi. h* " ist für Anwendungen erforderlich, die die IP-Hilfsfunktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="ea1b9-112">The *Iphlpapi.h* header file is required for applications that use the IP Helper functions.</span></span> <span data-ttu-id="ea1b9-113">Die Header Datei " *iphlpapi. h* " enthält automatisch andere Header Dateien mit Strukturen und Enumerationen, die von den IP-Hilfsfunktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea1b9-113">The *Iphlpapi.h* header file automatically includes other headers files with structures and enumerations used by the IP Helper functions.</span></span>
    >
    > <span data-ttu-id="ea1b9-114">Die neuen in Windows Vista und höher eingeführten IP-Hilfsfunktionen sind in der Header Datei " *nettioapi. h* " definiert, die automatisch in der Header Datei " *iphlpapi. h* " enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="ea1b9-114">The new IP Helper functions introduced in Windows Vista and later are defined in the *Netioapi.h* header file which is automatically included by the *Iphlpapi.h* header file.</span></span> <span data-ttu-id="ea1b9-115">Die Header Datei " *nettioapi. h* " sollte niemals direkt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea1b9-115">The *Netioapi.h* header file should never be used directly.</span></span>
    >
    > <span data-ttu-id="ea1b9-116">Viele der von den IP-Hilfsobjekten verwendeten Strukturen und Enumerationen werden in den Header Dateien " *iprtrmib. h*", " *ipexport. h*" und " *iptypes. h* " definiert.</span><span class="sxs-lookup"><span data-stu-id="ea1b9-116">Many of the structures and enumerations used by IP Helper functions are defined in the *Iprtrmib.h*, *Ipexport.h*, and *Iptypes.h* header files.</span></span> <span data-ttu-id="ea1b9-117">Diese Header Dateien werden automatisch in der Header Datei " *iphlpapi. h* " eingeschlossen und sollten niemals direkt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea1b9-117">These header files are automatically included in the *Iphlpapi.h* header file and should never be used directly.</span></span>
    >
    > <span data-ttu-id="ea1b9-118">Im Microsoft Windows Software Development Kit (SDK), das für Windows Vista und höher veröffentlicht wurde, hat sich die Organisation der Header Dateien geändert.</span><span class="sxs-lookup"><span data-stu-id="ea1b9-118">On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed.</span></span> <span data-ttu-id="ea1b9-119">Einige der Strukturen sind nun in den Header Dateien " *ipmib. h*", " *tcpmib. h*" und " *udpmib. h* " definiert, nicht in der Header Datei " *iprtrmib. h* ".</span><span class="sxs-lookup"><span data-stu-id="ea1b9-119">Some of the structures are now defined in the *Ipmib.h*, *Tcpmib.h*, and *Udpmib.h* header files, not in the *Iprtrmib.h* header file.</span></span> <span data-ttu-id="ea1b9-120">Die Header Datei " *ipmib. h* " enthält automatisch die Header Datei " *ifmib. h* ".</span><span class="sxs-lookup"><span data-stu-id="ea1b9-120">The *Ipmib.h* header file automatically includes the *Ifmib.h* header file.</span></span> <span data-ttu-id="ea1b9-121">Beachten Sie, dass diese Header Dateien automatisch in der Datei " *iprtrmib. h*" enthalten sind, die automatisch in der Header Datei " *iphlpapi. h* " enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="ea1b9-121">Note that these header files are automatically included in *Iprtrmib.h*, which is automatically included in the *Iphlpapi.h* header file.</span></span>
    >
    > <span data-ttu-id="ea1b9-122">Die Header Datei " *Winsock2. h* " für Windows Sockets 2,0 ist für die meisten Anwendungen erforderlich, die die IP-hilfsprogrammapis verwenden.</span><span class="sxs-lookup"><span data-stu-id="ea1b9-122">The *Winsock2.h* header file for Windows Sockets 2.0 is required by most applications using the IP Helper APIs.</span></span> <span data-ttu-id="ea1b9-123">Wenn die *Winsock2. h* -Header Datei erforderlich ist, \# sollte die Include-Zeile für diese Datei vor der \# Include-Zeile für die Header Datei " *iphlpapi. h* " platziert werden.</span><span class="sxs-lookup"><span data-stu-id="ea1b9-123">When the *Winsock2.h* header file is required, the \#include line for this file should be placed before the \#include line for the *Iphlpapi.h* header file.</span></span>
    >
    > <span data-ttu-id="ea1b9-124">Die Header Datei " *Winsock2. h* " enthält intern Kernelemente aus der Header Datei " *Windows. h* ", sodass \# in IP-Hilfsanwendungen normalerweise keine Include-Zeile für die *Windows. h* -Header Datei vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ea1b9-124">The *Winsock2.h* header file internally includes core elements from the *Windows.h* header file, so there is not usually an \#include line for *Windows.h* header file in IP Helper applications.</span></span> <span data-ttu-id="ea1b9-125">Wenn eine \# Include-Zeile für die Header Datei " *Windows. h* " erforderlich ist, sollte diesem das \# Win32 \_ \_ -und Mean-Makro definiert werden \_ .</span><span class="sxs-lookup"><span data-stu-id="ea1b9-125">If an \#include line is needed for the *Windows.h* header file, this should be preceded with the \#define WIN32\_LEAN\_AND\_MEAN macro.</span></span> <span data-ttu-id="ea1b9-126">Aus historischen Gründen hat der *Windows. h* -Header standardmäßig die *Winsock. h* -Header Datei für Windows Sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="ea1b9-126">For historical reasons, the *Windows.h* header defaults to including the *Winsock.h* header file for Windows Sockets 1.1.</span></span> <span data-ttu-id="ea1b9-127">Die Deklarationen in der *Winsock. h* -Header Datei für Windows Sockets 1,1 stehen in Konflikt mit den Deklarationen in der *Winsock2. h* -Header Datei, die von Windows Sockets 2,0 benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="ea1b9-127">The declarations in the *Winsock.h* header file for Windows Sockets 1.1 will conflict with the declarations in the *Winsock2.h* header file required by Windows Sockets 2.0.</span></span> <span data-ttu-id="ea1b9-128">Das Win32 \_ \_ -und \_ Mean-Makro verhindert, dass die Header Datei " *Winsock. h* " in der Header Datei " *Windows. h* " enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="ea1b9-128">The WIN32\_LEAN\_AND\_MEAN macro prevents the *Winsock.h* header file from being included by the *Windows.h* header file.</span></span> <span data-ttu-id="ea1b9-129">Im folgenden wird ein Beispiel gezeigt, das dies veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="ea1b9-129">An example illustrating this is shown below.</span></span>

     

    ```C++
    #ifndef WIN32_LEAN_AND_MEAN
    #define WIN32_LEAN_AND_MEAN
    #endif

    #include <windows.h>

    #include <winsock2.h>
    #include <iphlpapi.h>
    #include <stdio.h>

    int main() {
      return 0;
    }
    
    ```

    

    > [!Note]
    >
    > <span data-ttu-id="ea1b9-130">Diese grundlegende IP-Hilfsanwendung verwendet nur einige IP-Adressdaten Strukturen und eine IP-Adresse für Zeichen folgen Konvertierungs Funktionen von Windows Sockets 2,0.</span><span class="sxs-lookup"><span data-stu-id="ea1b9-130">This basic IP Helper application only uses some IP address data structures and IP address to string conversion functions from Windows Sockets 2.0.</span></span> <span data-ttu-id="ea1b9-131">Diese Windows Sockets-Funktionen können verwendet werden, ohne dass [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) aufgerufen wird, um Windows Sockets-Ressourcen und [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) zu initialisieren, wenn diese Ressourcen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea1b9-131">These Windows Sockets functions can be used without calling [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) to initialize Windows Sockets resources and [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) when done using these resources.</span></span>
    >
    > <span data-ttu-id="ea1b9-132">In IP-Hilfsanwendungen, die andere andere Winsock-Funktionen als diese IP-Adressen für Zeichen folgen Funktionen verwenden, muss die [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) -Funktion aufgerufen werden, um Windows Sockets-Ressourcen vor dem Aufrufen von Windows Sockets-Funktionen zu initialisieren, und [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) sollte aufgerufen werden, wenn die Anwendung mithilfe von Windows Sockets-Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ea1b9-132">In IP Helper applications that use other Winsock functions other than these IP address to string functions, the [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) function must be called to initialize Windows Sockets resources before calling any Windows Sockets functions and [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) should be called when the application is done using Windows Sockets resources.</span></span>

     

    > [!Note]
    >
    > <span data-ttu-id="ea1b9-133">Die Header Datei " *stdio. h* " ist für die Verwendung verschiedener Standard-C-Funktionen in dieser grundlegenden IP-Hilfsanwendung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ea1b9-133">The *Stdio.h* header file is required for the use of various standard C functions in this basic IP Helper application.</span></span>

     

    <span data-ttu-id="ea1b9-134">Nächster Schritt: [Abrufen von Informationen mithilfe von getnetworkpara](retrieving-information-using-getnetworkparams.md) Metern</span><span class="sxs-lookup"><span data-stu-id="ea1b9-134">Next Step: [Retrieving Information Using GetNetworkParams](retrieving-information-using-getnetworkparams.md)</span></span>

 

 
