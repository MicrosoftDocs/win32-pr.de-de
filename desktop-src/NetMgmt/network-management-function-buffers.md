---
title: Puffer der Netzwerk Verwaltungsfunktion
description: Die RPC-Lauf Zeit Bibliothek verarbeitet die Puffer, die für die Netzwerk Verwaltungsfunktionen des 32-Bit-Datenabruf erforderlich sind, wie folgt.
ms.assetid: f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385382d12aa5b5c8c7c93b9a833f684d913c5783
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206901"
---
# <a name="network-management-function-buffers"></a><span data-ttu-id="80c72-103">Puffer der Netzwerk Verwaltungsfunktion</span><span class="sxs-lookup"><span data-stu-id="80c72-103">Network Management Function Buffers</span></span>

<span data-ttu-id="80c72-104">Die RPC-Lauf Zeit Bibliothek verarbeitet die Puffer, die für die Netzwerk Verwaltungsfunktionen des 32-Bit-Datenabruf erforderlich sind, wie folgt:</span><span class="sxs-lookup"><span data-stu-id="80c72-104">The RPC run-time library handles the buffers required by the 32-bit data retrieval network management functions as follows:</span></span>

-   <span data-ttu-id="80c72-105">**Senden von Daten an den Server** (durch in-Parameter angegebene Daten \[ \] ).</span><span class="sxs-lookup"><span data-stu-id="80c72-105">**Sending data to the server** (data specified by \[in\] parameters).</span></span>

    <span data-ttu-id="80c72-106">Der Aufrufer muss den Puffer für die relevante Informationsstruktur (oder Strukturen) zuordnen und seine Freigabe zuweisen und eine Zeiger Variable an die Funktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="80c72-106">The caller must allocate and deallocate the buffer for the relevant information structure (or structures) and pass a pointer variable to the function.</span></span> <span data-ttu-id="80c72-107">Der Aufrufer muss die Pufferlänge nicht angeben.</span><span class="sxs-lookup"><span data-stu-id="80c72-107">The caller does not need to specify the buffer length.</span></span>

    <span data-ttu-id="80c72-108">Beispiel: [ **NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)</span><span class="sxs-lookup"><span data-stu-id="80c72-108">Example: [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)</span></span>

-   <span data-ttu-id="80c72-109">**Abrufen von Daten vom Server** (durch out-Parameter angegebene Daten \[ \] ).</span><span class="sxs-lookup"><span data-stu-id="80c72-109">**Retrieving data from the server** (data specified by \[out\] parameters).</span></span>

    <span data-ttu-id="80c72-110">Das System ordnet den Puffer für die zurückgegebenen Informationen zu.</span><span class="sxs-lookup"><span data-stu-id="80c72-110">The system allocates the buffer for the returned information.</span></span> <span data-ttu-id="80c72-111">Der Aufrufer muss bei der Eingabe eine Zeiger Variable an die Funktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="80c72-111">The caller must pass a pointer variable to the function on input.</span></span> <span data-ttu-id="80c72-112">Bei erfolgreicher Rückgabe erhält der Zeiger die Adresse des vom System zugewiesenen Puffers, der die zurückgegebenen Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="80c72-112">On successful return, the pointer receives the address of the system-allocated buffer that contains the returned information.</span></span> <span data-ttu-id="80c72-113">Dadurch wird der aufrufende Code vereinfacht, da der Aufrufer die Größe des Puffers nicht einschätzen muss oder die Größe des Puffers ändern und die Funktion erneut ausgeben muss.</span><span class="sxs-lookup"><span data-stu-id="80c72-113">This simplifies the calling code, because the caller does not need to estimate the size of the buffer, or resize the buffer and reissue the function.</span></span>

    <span data-ttu-id="80c72-114">Wenn der Aufrufer die Verarbeitung der zurückgegebenen Informationen abgeschlossen hat, muss der vom System zugewiesene Speicher durch Aufrufen der Funktion " [**nettapibufferfree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) " freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="80c72-114">When the caller has finished processing the returned information, it must free the system-allocated memory by calling the [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) function.</span></span> <span data-ttu-id="80c72-115">Weitere Informationen zum Angeben von Puffergrößen finden Sie unter [Puffer Längen der Netzwerk Verwaltungsfunktion](network-management-function-buffer-lengths.md).</span><span class="sxs-lookup"><span data-stu-id="80c72-115">For more information about specifying buffer sizes, see [Network Management Function Buffer Lengths](network-management-function-buffer-lengths.md).</span></span>

    <span data-ttu-id="80c72-116">Beispiel: [ **netgroupum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)</span><span class="sxs-lookup"><span data-stu-id="80c72-116">Example: [**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)</span></span>

 

 




