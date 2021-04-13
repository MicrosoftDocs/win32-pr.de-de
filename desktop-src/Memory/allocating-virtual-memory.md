---
description: Die Funktionen des virtuellen Arbeitsspeichers bearbeiten Arbeitsspeicher Seiten. Die Funktionen verwenden die Größe einer Seite auf dem aktuellen Computer, um die angegebenen Größen und Adressen abzurunden.
ms.assetid: 509cd529-ff79-4b07-9e09-3c5ae65f6cba
title: Zuordnen des virtuellen Speichers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89f42b4f7eb9d5de3c8c5e9339c9e5931a89e371
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345369"
---
# <a name="allocating-virtual-memory"></a><span data-ttu-id="67a17-104">Zuordnen des virtuellen Speichers</span><span class="sxs-lookup"><span data-stu-id="67a17-104">Allocating Virtual Memory</span></span>

<span data-ttu-id="67a17-105">Die Funktionen des virtuellen Arbeitsspeichers bearbeiten Arbeitsspeicher Seiten.</span><span class="sxs-lookup"><span data-stu-id="67a17-105">The virtual memory functions manipulate pages of memory.</span></span> <span data-ttu-id="67a17-106">Die Funktionen verwenden die Größe einer Seite auf dem aktuellen Computer, um die angegebenen Größen und Adressen abzurunden.</span><span class="sxs-lookup"><span data-stu-id="67a17-106">The functions use the size of a page on the current computer to round off specified sizes and addresses.</span></span>

<span data-ttu-id="67a17-107">Die [**virtualzuweisung**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) -Funktion führt einen der folgenden Vorgänge aus:</span><span class="sxs-lookup"><span data-stu-id="67a17-107">The [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) function performs one of the following operations:</span></span>

-   <span data-ttu-id="67a17-108">Reserviert eine oder mehrere freie Seiten.</span><span class="sxs-lookup"><span data-stu-id="67a17-108">Reserves one or more free pages.</span></span>
-   <span data-ttu-id="67a17-109">Führt einen Commit für eine oder mehrere reservierte Seiten aus.</span><span class="sxs-lookup"><span data-stu-id="67a17-109">Commits one or more reserved pages.</span></span>
-   <span data-ttu-id="67a17-110">Reserviert und führt einen Commit für eine oder mehrere freie Seiten aus.</span><span class="sxs-lookup"><span data-stu-id="67a17-110">Reserves and commits one or more free pages.</span></span>

<span data-ttu-id="67a17-111">Sie können die Startadresse der Seiten angeben, für die reserviert oder ein Commit ausgeführt werden soll, oder Sie können zulassen, dass das System die Adresse bestimmt.</span><span class="sxs-lookup"><span data-stu-id="67a17-111">You can specify the starting address of the pages to be reserved or committed, or you can allow the system to determine the address.</span></span> <span data-ttu-id="67a17-112">Die-Funktion rundet die angegebene Adresse auf die entsprechende Seitenbegrenzung.</span><span class="sxs-lookup"><span data-stu-id="67a17-112">The function rounds the specified address to the appropriate page boundary.</span></span> <span data-ttu-id="67a17-113">Auf reservierte Seiten kann nicht zugegriffen werden, aber zugeordnete Seiten können mit Seiten Lese **Berechtigung \_ , Seiten** **\_ Schreib** Zugriff **oder \_ Seiten** Speicherzugriff zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="67a17-113">Reserved pages are not accessible, but committed pages can be allocated with **PAGE\_READWRITE**, **PAGE\_READONLY**, or **PAGE\_NOACCESS** access.</span></span> <span data-ttu-id="67a17-114">Wenn für Seiten ein Commit ausgeführt wird, werden Arbeitsspeicher Gebühren aus der Gesamtgröße des Arbeitsspeichers und der Auslagerungs Dateien auf dem Datenträger belegt, aber jede Seite wird initialisiert und in den physischen Speicher geladen, wenn Sie zum ersten Mal versucht, diese Seite zu lesen oder zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="67a17-114">When pages are committed, memory charges are allocated from the overall size of RAM and paging files on disk, but each page is initialized and loaded into physical memory only at the first attempt to read from or write to that page.</span></span> <span data-ttu-id="67a17-115">Sie können normale Zeiger Verweise verwenden, um auf den Speicher zuzugreifen, der von der [**virtualbelegc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) -Funktion zugesichert wurde.</span><span class="sxs-lookup"><span data-stu-id="67a17-115">You can use normal pointer references to access memory committed by the [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) function.</span></span>

 

 
