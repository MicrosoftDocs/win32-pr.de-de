---
description: Die maximale Anzahl von Sockets, die von einem bestimmten Windows Sockets-Dienstanbieter unterstützt werden, ist Implementierungs spezifisch.
ms.assetid: acf5ab29-3848-4dbc-afa7-a0f19045ddec
title: Maximale Anzahl unterstützter Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 207893836a411a2465ffcefe10e838c2e8b59011
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357331"
---
# <a name="maximum-number-of-sockets-supported"></a><span data-ttu-id="be1cf-103">Maximale Anzahl unterstützter Sockets</span><span class="sxs-lookup"><span data-stu-id="be1cf-103">Maximum Number of Sockets Supported</span></span>

<span data-ttu-id="be1cf-104">Die maximale Anzahl von Sockets, die von einem bestimmten Windows Sockets-Dienstanbieter unterstützt werden, ist Implementierungs spezifisch.</span><span class="sxs-lookup"><span data-stu-id="be1cf-104">The maximum number of sockets supported by a particular Windows Sockets service provider is implementation specific.</span></span> <span data-ttu-id="be1cf-105">Der Microsoft Winsock-Anbieter schränkt die maximale Anzahl von Sockets ein, die nur durch den verfügbaren Speicher auf dem lokalen Computer unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="be1cf-105">The Microsoft Winsock provider limits the maximum number of sockets supported only by available memory on the local computer.</span></span> <span data-ttu-id="be1cf-106">Allerdings können Winsock-Anbieter von Drittanbietern Einschränkungen hinsichtlich der Anzahl der unterstützten Sockets aufweisen.</span><span class="sxs-lookup"><span data-stu-id="be1cf-106">However, third-party Winsock providers may have limitations on the numbers of sockets supported.</span></span> <span data-ttu-id="be1cf-107">Eine Anwendung sollte keine Annahmen über die Verfügbarkeit einer bestimmten Anzahl von Sockets treffen.</span><span class="sxs-lookup"><span data-stu-id="be1cf-107">An application should make no assumptions about the availability of a certain number of sockets.</span></span> <span data-ttu-id="be1cf-108">Weitere Informationen zu diesem Thema finden Sie unter [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup).</span><span class="sxs-lookup"><span data-stu-id="be1cf-108">For more information on this topic see [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup).</span></span>

## <a name="fd_set-and-select"></a><span data-ttu-id="be1cf-109">FD \_ festgelegt und auswählen</span><span class="sxs-lookup"><span data-stu-id="be1cf-109">FD\_SET and select</span></span>

<span data-ttu-id="be1cf-110">\_In der Header Datei " *Winsock2. h* " sind eine Reihe von FD xxx-Makros definiert, die zum Portieren von Anwendungen auf Windows aus der UNIX-Umgebung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="be1cf-110">A number of FD\_XXX macros are defined in the *Winsock2.h* header file for use in porting applications to Windows from the UNIX environment.</span></span> <span data-ttu-id="be1cf-111">Diese Makros werden zusammen mit den Funktionen [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) und [**wsapoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) zum Portieren von Anwendungen auf Windows verwendet.</span><span class="sxs-lookup"><span data-stu-id="be1cf-111">These macros are used with the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) and [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) functions for porting applications to Windows.</span></span> <span data-ttu-id="be1cf-112">Die maximale Anzahl von Sockets, die eine Windows Sockets-Anwendung verwenden kann, wird von der Manifestressource FD \_ SetSize nicht beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="be1cf-112">The maximum number of sockets that a Windows Sockets application can use is not affected by the manifest constant FD\_SETSIZE.</span></span> <span data-ttu-id="be1cf-113">Dieser Wert, der in der Header Datei " *Winsock2. h* " definiert ist, wird zum Erstellen der mit **Select** -Funktion verwendeten [**FD- \_ set**](/windows/desktop/api/winsock/nf-winsock-fd_set) -Strukturen verwendet.</span><span class="sxs-lookup"><span data-stu-id="be1cf-113">This value defined in the *Winsock2.h* header file is used in constructing the [**FD\_SET**](/windows/desktop/api/winsock/nf-winsock-fd_set) structures used with **select** function.</span></span> <span data-ttu-id="be1cf-114">Der Standardwert in Winsock2. h ist 64.</span><span class="sxs-lookup"><span data-stu-id="be1cf-114">The default value in Winsock2.h is 64.</span></span> <span data-ttu-id="be1cf-115">Wenn eine Anwendung in der Lage ist, mehr als 64 Sockets mithilfe der **Select** -und **wsapoll** -Funktionen zu verwenden, sollte die Implementierung das Manifest- \_ SetSize-Manifest in jeder Quelldatei definieren, bevor die *Winsock2. h* -Header Datei eingeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="be1cf-115">If an application is designed to be capable of working with more than 64 sockets using the **select** and **WSAPoll** functions, the implementor should define the manifest FD\_SETSIZE in every source file before including the *Winsock2.h* header file.</span></span> <span data-ttu-id="be1cf-116">Eine Möglichkeit, dies zu tun, besteht darin, die Definition innerhalb der Compileroptionen in das Makefile aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="be1cf-116">One way of doing this may be to include the definition within the compiler options in the makefile.</span></span> <span data-ttu-id="be1cf-117">Beispielsweise können Sie "-DFD \_ SetSize = 128" als Option zur Compilerbefehlszeile für Microsoft C++ hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="be1cf-117">For example, you could add "-DFD\_SETSIZE=128" as an option to the compiler command line for Microsoft C++.</span></span> <span data-ttu-id="be1cf-118">Es muss betont werden, dass \_ die Definition von FD SetSize als bestimmter Wert keine Auswirkung auf die tatsächliche Anzahl der Sockets ist, die von einem Windows Sockets Service-Anbieter bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="be1cf-118">It must be emphasized that defining FD\_SETSIZE as a particular value has no effect on the actual number of sockets provided by a Windows Sockets service provider.</span></span> <span data-ttu-id="be1cf-119">Dieser Wert wirkt sich nur auf die FD \_ xxx-Makros aus, die von den Funktionen **Select** und **wsapoll** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="be1cf-119">This value only affects the FD\_XXX macros used by the **select** and **WSAPoll** functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="be1cf-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="be1cf-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be1cf-121">**FD- \_ Satz**</span><span class="sxs-lookup"><span data-stu-id="be1cf-121">**FD\_SET**</span></span>](/windows/desktop/api/winsock/nf-winsock-fd_set)
</dt> <dt>

[<span data-ttu-id="be1cf-122">Portieren von Socketanwendungen auf Winsock</span><span class="sxs-lookup"><span data-stu-id="be1cf-122">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="be1cf-123">**Auswahl**</span><span class="sxs-lookup"><span data-stu-id="be1cf-123">**select**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-select)
</dt> <dt>

[<span data-ttu-id="be1cf-124">Überlegungen zur Winsock-Programmierung</span><span class="sxs-lookup"><span data-stu-id="be1cf-124">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="be1cf-125">**WSAStartup**</span><span class="sxs-lookup"><span data-stu-id="be1cf-125">**WSAStartup**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsastartup)
</dt> <dt>

[<span data-ttu-id="be1cf-126">**Wsapoll**</span><span class="sxs-lookup"><span data-stu-id="be1cf-126">**WSAPoll**</span></span>](/windows/win32/api/winsock2/nf-winsock2-wsapoll)
</dt> </dl>

 

 
