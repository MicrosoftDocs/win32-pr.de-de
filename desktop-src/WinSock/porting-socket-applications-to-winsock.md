---
description: In diesem Abschnitt werden die Aspekte der Winsock-Portierung beschrieben.
ms.assetid: 41c0c98e-3990-4600-ab9f-fa87edbea402
title: Portieren von Socketanwendungen auf Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e2b3480d5572405d33b3a3532892a48633caa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356753"
---
# <a name="porting-socket-applications-to-winsock"></a><span data-ttu-id="6a4b5-103">Portieren von Socketanwendungen auf Winsock</span><span class="sxs-lookup"><span data-stu-id="6a4b5-103">Porting Socket Applications to Winsock</span></span>

<span data-ttu-id="6a4b5-104">In diesem Abschnitt werden die Aspekte der Winsock-Portierung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6a4b5-104">This section describes Winsock porting considerations.</span></span>

<span data-ttu-id="6a4b5-105">Es gibt eine begrenzte Anzahl von Instanzen, bei denen Windows Sockets von der strikten Einhaltung der Berkeley-Konventionen umgeleitet wurde, in der Regel aufgrund von Implementierungs Problemen in der Microsoft Windows-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="6a4b5-105">There are a limited number of instances where Windows Sockets has diverted from strict adherence to the Berkeley conventions, usually due to implementation difficulties in the Microsoft Windows environment.</span></span>

<span data-ttu-id="6a4b5-106">Wenn eine Abweichung von Berkeley-Konventionen in Windows Sockets auftritt, wird die Abweichung ausdrücklich und eindeutig vermerkt.</span><span class="sxs-lookup"><span data-stu-id="6a4b5-106">When a deviation from Berkeley conventions occurs in Windows Sockets, the deviation is specifically and clearly noted.</span></span> <span data-ttu-id="6a4b5-107">Wenn eine Funktion z. b. für Windows Sockets spezifisch ist, wird diese Abweichung mit einem Ausdruck in der Funktionsbeschreibung wie folgt angegeben:</span><span class="sxs-lookup"><span data-stu-id="6a4b5-107">For example, if a function is specific to Windows Sockets, that deviation is specified with a phrase in the function description similar to the following:</span></span>

<span data-ttu-id="6a4b5-108">Die **\[ Funktion "Function \] -Name** " ist eine Microsoft-spezifische Erweiterung der Windows Sockets 2-API.</span><span class="sxs-lookup"><span data-stu-id="6a4b5-108">The **\[function-name\]** function is a Microsoft-specific extension to the Windows Sockets 2 API.</span></span>

<span data-ttu-id="6a4b5-109">Dieser Abschnitt enthält Informationen zum Portieren von UNIX-Socketanwendungen (BSD) in Winsock:</span><span class="sxs-lookup"><span data-stu-id="6a4b5-109">This section provides information about porting Berkeley (BSD) UNIX socket applications to Winsock:</span></span>

-   [<span data-ttu-id="6a4b5-110">Socket-Datentyp</span><span class="sxs-lookup"><span data-stu-id="6a4b5-110">Socket Data Type</span></span>](socket-data-type-2.md)
-   [<span data-ttu-id="6a4b5-111">Makros für Auswahl, FD \_ -Satz und FD \_ xxx</span><span class="sxs-lookup"><span data-stu-id="6a4b5-111">Select, FD\_SET, and FD\_XXX Macros</span></span>](select-and-fd---2.md)
-   [<span data-ttu-id="6a4b5-112">Fehler Codes: errno, h \_ errno und WSAGetLastError</span><span class="sxs-lookup"><span data-stu-id="6a4b5-112">Error Codes - errno, h\_errno and WSAGetLastError</span></span>](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
-   [<span data-ttu-id="6a4b5-113">Zeiger</span><span class="sxs-lookup"><span data-stu-id="6a4b5-113">Pointers</span></span>](pointers-2.md)
-   [<span data-ttu-id="6a4b5-114">Umbenannte Funktionen</span><span class="sxs-lookup"><span data-stu-id="6a4b5-114">Renamed Functions</span></span>](renamed-functions-2.md)
-   [<span data-ttu-id="6a4b5-115">Maximale Anzahl unterstützter Sockets</span><span class="sxs-lookup"><span data-stu-id="6a4b5-115">Maximum Number of Sockets Supported</span></span>](maximum-number-of-sockets-supported-2.md)
-   [<span data-ttu-id="6a4b5-116">Includedateien</span><span class="sxs-lookup"><span data-stu-id="6a4b5-116">Include Files</span></span>](include-files-2.md)
-   [<span data-ttu-id="6a4b5-117">Rückgabewerte bei Funktions Fehlern</span><span class="sxs-lookup"><span data-stu-id="6a4b5-117">Return Values on Function Failure</span></span>](return-values-on-function-failure-2.md)
-   [<span data-ttu-id="6a4b5-118">Rohdaten Sockets</span><span class="sxs-lookup"><span data-stu-id="6a4b5-118">Raw Sockets</span></span>](service-provided-raw-sockets-2.md)
-   [<span data-ttu-id="6a4b5-119">Byte Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="6a4b5-119">Byte Ordering</span></span>](byte-ordering-2.md)
-   [<span data-ttu-id="6a4b5-120">Erweiterte Byte-Order Konvertierungs Routinen</span><span class="sxs-lookup"><span data-stu-id="6a4b5-120">Extended Byte-Order Conversion Routines</span></span>](extended-byte-order-conversion-routines-2.md)

## <a name="related-topics"></a><span data-ttu-id="6a4b5-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6a4b5-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a4b5-122">Behandeln von Winsock-Fehlern</span><span class="sxs-lookup"><span data-stu-id="6a4b5-122">Handling Winsock Errors</span></span>](handling-winsock-errors.md)
</dt> <dt>

[<span data-ttu-id="6a4b5-123">Portieren von Socketanwendungen auf Winsock</span><span class="sxs-lookup"><span data-stu-id="6a4b5-123">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="6a4b5-124">Windows Sockets-Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="6a4b5-124">Windows Sockets Error Codes</span></span>](windows-sockets-error-codes-2.md)
</dt> <dt>

[<span data-ttu-id="6a4b5-125">Überlegungen zur Winsock-Programmierung</span><span class="sxs-lookup"><span data-stu-id="6a4b5-125">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 



