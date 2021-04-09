---
title: Out-of-Context-Hook-Funktionen
ms.assetid: c0156485-db1e-42d3-bbbd-c51835a597ed
description: 'Weitere Informationen finden Sie hier: Out-of-Context-Hook-Funktionen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d5837c39850c5821d44146498f62d4c874e7802
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867155"
---
# <a name="out-of-context-hook-functions"></a><span data-ttu-id="67b95-103">Out-of-Context-Hook-Funktionen</span><span class="sxs-lookup"><span data-stu-id="67b95-103">Out-of-Context Hook Functions</span></span>

<span data-ttu-id="67b95-104">In der folgenden Liste werden die wichtigsten Aspekte von Funktionen für den Out-of-Context-Hook erläutert:</span><span class="sxs-lookup"><span data-stu-id="67b95-104">The following list outlines the key aspects of out-of-context hook functions:</span></span>

-   <span data-ttu-id="67b95-105">Out-of-Context-Hookfunktionen befinden sich im Adressraum des Clients, unabhängig davon, ob Sie sich im Code Körper oder in einer DLL befinden.</span><span class="sxs-lookup"><span data-stu-id="67b95-105">Out-of-context hook functions are located in the client's address space, whether it is in the code body or in a DLL.</span></span>
-   <span data-ttu-id="67b95-106">Out-of-Context-Hook-Funktionen werden nicht im Adressraum des Servers zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="67b95-106">Out-of-context hook functions are not mapped into the server's address space.</span></span>
-   <span data-ttu-id="67b95-107">Wenn ein Ereignis ausgelöst wird, werden die Parameter für die Hook-Funktion über Prozess Grenzen hinweg gemarshallt.</span><span class="sxs-lookup"><span data-stu-id="67b95-107">When an event is triggered, the parameters for the hook function are marshaled across process boundaries.</span></span>
-   <span data-ttu-id="67b95-108">Out-of-Context-Hook-Funktionen sind aufgrund von Marshalling merklich langsamer als in-context-Hook-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="67b95-108">Out-of-context hook functions are noticeably slower than in-context hook functions due to marshaling.</span></span>
-   <span data-ttu-id="67b95-109">Das System fügt die Ereignis Benachrichtigungen in die Warteschlange ein, sodass Sie asynchron eintreffen (aufgrund der Zeit, die zum Durchführen von Marshalling erforderlich ist).</span><span class="sxs-lookup"><span data-stu-id="67b95-109">The system queues the event notifications so that they arrive asynchronously (because of the time required to perform marshaling).</span></span>

<span data-ttu-id="67b95-110">Obwohl die Ereignis Benachrichtigungen asynchron sind, stellt Microsoft Active Accessibility sicher, dass die Rückruffunktion alle Ereignisse in der Reihenfolge empfängt, in der Sie generiert werden.</span><span class="sxs-lookup"><span data-stu-id="67b95-110">Although the event notifications are asynchronous, Microsoft Active Accessibility assures that the callback function receives all events in the order in which they are generated.</span></span>

<span data-ttu-id="67b95-111">Die Benutzer Komponente des Betriebssystems weist Speicher für Ereignisse zu, die durch out-of-Context-Hook-Funktionen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="67b95-111">The USER component of the operating system allocates memory for events that are handled by out-of-context hook functions.</span></span> <span data-ttu-id="67b95-112">Der Arbeitsspeicher wird freigegeben, wenn die Hook-Funktionen zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="67b95-112">The memory is freed when the hook functions return.</span></span> <span data-ttu-id="67b95-113">Wenn eine Hook-Funktion Ereignisse nicht schnell genug verarbeitet, werden die Benutzerressourcen gesenkt, was zu einem Fehler oder extrem langsamen Antwortzeiten führt.</span><span class="sxs-lookup"><span data-stu-id="67b95-113">If a hook function does not process events quickly enough, USER resources are lowered, eventually resulting in a fault or extremely slow response times.</span></span> <span data-ttu-id="67b95-114">Folgende Probleme können auftreten:</span><span class="sxs-lookup"><span data-stu-id="67b95-114">These problems may occur if:</span></span>

-   <span data-ttu-id="67b95-115">Ereignisse werden sehr schnell ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="67b95-115">Events are fired very rapidly.</span></span>
-   <span data-ttu-id="67b95-116">Das System ist langsam.</span><span class="sxs-lookup"><span data-stu-id="67b95-116">The system is slow.</span></span>
-   <span data-ttu-id="67b95-117">Die Hook-Funktion verarbeitet Ereignisse langsam.</span><span class="sxs-lookup"><span data-stu-id="67b95-117">The hook function processes events slowly.</span></span>
-   <span data-ttu-id="67b95-118">Der Client wird unter Windows 9X ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="67b95-118">The client is running on Windows 9x.</span></span>

 

 




