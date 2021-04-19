---
description: Bietet eine kurze Einführung in einige Arten von Pufferüberlauf Situationen und bietet einige Ideen und Ressourcen, die Sie dabei unterstützen, neue Risiken zu vermeiden und vorhandene Risiken zu verringern.
ms.assetid: 713fd6de-16af-49d2-8940-763c4a6e414b
title: Vermeiden von Pufferüberläufen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c8a3456384e799380fa0041172fb2b2ea09c0c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364092"
---
# <a name="avoiding-buffer-overruns"></a><span data-ttu-id="ebac1-103">Vermeiden von Pufferüberläufen</span><span class="sxs-lookup"><span data-stu-id="ebac1-103">Avoiding Buffer Overruns</span></span>

<span data-ttu-id="ebac1-104">Ein Pufferüberlauf ist eine der häufigsten Ursachen für Sicherheitsrisiken.</span><span class="sxs-lookup"><span data-stu-id="ebac1-104">A buffer overrun is one of the most common sources of security risk.</span></span> <span data-ttu-id="ebac1-105">Ein Pufferüberlauf wird im Wesentlichen durch die Behandlung von nicht überprüften, externer Eingaben als vertrauenswürdige Daten verursacht.</span><span class="sxs-lookup"><span data-stu-id="ebac1-105">A buffer overrun is essentially caused by treating unchecked, external input as trustworthy data.</span></span> <span data-ttu-id="ebac1-106">Der Vorgang des Kopierens dieser Daten unter Verwendung von Vorgängen wie [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)), " **Strauch**", " **straucpy**" oder " **wcscpy**" kann zu unerwarteten Ergebnissen führen, was eine System Beschädigung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="ebac1-106">The act of copying this data, using operations such as [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)), **strcat**, **strcpy**, or **wcscpy**, can create unanticipated results, which allows for system corruption.</span></span> <span data-ttu-id="ebac1-107">In den meisten Fällen wird Ihre Anwendung mit einem zentralen Dump-, Segmentierungs-oder Zugriffs Verstoß abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="ebac1-107">In the best of cases, your application will abort with a core dump, segmentation fault, or access violation.</span></span> <span data-ttu-id="ebac1-108">Im schlimmsten Fall kann ein Angreifer den Pufferüberlauf ausnutzen, indem er einen anderen bösartigen Code in Ihrem Prozess einführt und ausführt.</span><span class="sxs-lookup"><span data-stu-id="ebac1-108">In the worst of cases, an attacker can exploit the buffer overrun by introducing and executing other malicious code in your process.</span></span> <span data-ttu-id="ebac1-109">Das Kopieren von nicht überprüften, Eingabedaten in einen Stapel basierten Puffer ist die häufigste Ursache für ausnutzbare Fehler.</span><span class="sxs-lookup"><span data-stu-id="ebac1-109">Copying unchecked, input data into a stack-based buffer is the most common cause of exploitable faults.</span></span>

<span data-ttu-id="ebac1-110">Pufferüberläufe können auf unterschiedlichste Weise erfolgen.</span><span class="sxs-lookup"><span data-stu-id="ebac1-110">Buffer overruns can occur in a variety of ways.</span></span> <span data-ttu-id="ebac1-111">Die folgende Liste bietet eine kurze Einführung in einige Arten von Pufferüberlauf Situationen und bietet einige Ideen und Ressourcen, mit denen Sie das Erstellen neuer Risiken und das verringern vorhandener Risiken vermeiden können:</span><span class="sxs-lookup"><span data-stu-id="ebac1-111">The following list provides a brief introduction to a few types of buffer overrun situations and offers some ideas and resources to help you avoid creating new risks and mitigate existing ones:</span></span>

<dl> <dt>

<span data-ttu-id="ebac1-112"><span id="Static_buffer_overruns"></span><span id="static_buffer_overruns"></span><span id="STATIC_BUFFER_OVERRUNS"></span>Über Läufe statischer Puffer</span><span class="sxs-lookup"><span data-stu-id="ebac1-112"><span id="Static_buffer_overruns"></span><span id="static_buffer_overruns"></span><span id="STATIC_BUFFER_OVERRUNS"></span>Static buffer overruns</span></span>
</dt> <dd>

<span data-ttu-id="ebac1-113">Ein statischer Pufferüberlauf tritt auf, wenn ein Puffer, der auf dem Stapel deklariert wurde, mit mehr Daten geschrieben wird, als Sie aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="ebac1-113">A static buffer overrun occurs when a buffer, which has been declared on the stack, is written to with more data than it was allocated to hold.</span></span> <span data-ttu-id="ebac1-114">Die weniger offensichtlichen Versionen dieses Fehlers treten auf, wenn nicht überprüfte Benutzereingabe Daten direkt in eine statische Variable kopiert werden, was eine potenzielle Stapel Beschädigung zur Folge hat.</span><span class="sxs-lookup"><span data-stu-id="ebac1-114">The less apparent versions of this error occur when unverified user input data is copied directly to a static variable, causing potential stack corruption.</span></span>

</dd> <dt>

<span data-ttu-id="ebac1-115"><span id="Heap_overruns"></span><span id="heap_overruns"></span><span id="HEAP_OVERRUNS"></span>Heap Überläufe</span><span class="sxs-lookup"><span data-stu-id="ebac1-115"><span id="Heap_overruns"></span><span id="heap_overruns"></span><span id="HEAP_OVERRUNS"></span>Heap overruns</span></span>
</dt> <dd>

<span data-ttu-id="ebac1-116">Heap Überläufe, wie z. b. statische Pufferüberläufe, können zu Arbeitsspeicher-und Stapel Beschädigungen führen.</span><span class="sxs-lookup"><span data-stu-id="ebac1-116">Heap overruns, like static buffer overruns, can lead to memory and stack corruption.</span></span> <span data-ttu-id="ebac1-117">Da Heap Überläufe nicht auf dem Stapel, sondern im Heap Speicher stattfinden, werden Sie von manchen Benutzern als weniger schwerwiegend angesehen, schwerwiegende Probleme zu verursachen. Trotzdem ist für Heap Überläufe eine echte Programmierung erforderlich, und es sind nur die Möglichkeit, Systemrisiken als statische Pufferüberläufe zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="ebac1-117">Because heap overruns occur in heap memory rather than on the stack, some people consider them to be less able to cause serious problems; nevertheless, heap overruns require real programming care and are just as able to allow system risks as static buffer overruns.</span></span>

</dd> <dt>

<span data-ttu-id="ebac1-118"><span id="Array_indexing_errors"></span><span id="array_indexing_errors"></span><span id="ARRAY_INDEXING_ERRORS"></span>Array Indizierungs Fehler</span><span class="sxs-lookup"><span data-stu-id="ebac1-118"><span id="Array_indexing_errors"></span><span id="array_indexing_errors"></span><span id="ARRAY_INDEXING_ERRORS"></span>Array indexing errors</span></span>
</dt> <dd>

<span data-ttu-id="ebac1-119">Array Indizierungs Fehler sind auch eine Quelle für Arbeitsspeicher Überläufe.</span><span class="sxs-lookup"><span data-stu-id="ebac1-119">Array indexing errors also are a source of memory overruns.</span></span> <span data-ttu-id="ebac1-120">Eine sorgfältige Überprüfung der Begrenzungen und die Index Verwaltung helfen dabei, diese Art von Arbeitsspeicher Überlauf zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="ebac1-120">Careful bounds checking and index management will help prevent this type of memory overrun.</span></span>

</dd> </dl>

<span data-ttu-id="ebac1-121">Das verhindern von Pufferüberläufen ist hauptsächlich das Schreiben von gutem Code.</span><span class="sxs-lookup"><span data-stu-id="ebac1-121">Preventing buffer overruns is primarily about writing good code.</span></span> <span data-ttu-id="ebac1-122">Überprüfen Sie immer alle Eingaben, und führen Sie ggf. einen Fehler aus.</span><span class="sxs-lookup"><span data-stu-id="ebac1-122">Always validate all your inputs and fail gracefully when necessary.</span></span> <span data-ttu-id="ebac1-123">Weitere Informationen zum Schreiben von sicherem Code finden Sie in den folgenden Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="ebac1-123">For more information about writing secure code, see the following resources:</span></span>

-   <span data-ttu-id="ebac1-124">Maguire, Steve \[ 1993 \] , *Schreiben von Solid-Code*, ISBN 1-55615-551-4, Microsoft Press, Redmond, Washington.</span><span class="sxs-lookup"><span data-stu-id="ebac1-124">Maguire, Steve \[1993\], *Writing Solid Code*, ISBN 1-55615-551-4, Microsoft Press, Redmond, Washington.</span></span>
-   <span data-ttu-id="ebac1-125">Howard, Michael und LeBlanc, David \[ 2003 \] , *Schreiben von sicherem Code*, 2D Ed., ISBN 0-7356-1722-8, Microsoft Press, Redmond, Washington.</span><span class="sxs-lookup"><span data-stu-id="ebac1-125">Howard, Michael and LeBlanc, David \[2003\], *Writing Secure Code*, 2d ed., ISBN 0-7356-1722-8, Microsoft Press, Redmond, Washington.</span></span>

> [!Note]  
> <span data-ttu-id="ebac1-126">Diese Ressourcen sind in einigen Sprachen und Ländern möglicherweise nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ebac1-126">These resources may not be available in some languages and countries.</span></span>

 

<span data-ttu-id="ebac1-127">Die Behandlung sicherer Zeichen folgen ist ein lang Zeitproblem, das sowohl durch die Verwendung von bewährten Programmierverfahren als auch durch die neurüstung vorhandener Systeme mit sicheren Funktionen zur Zeichen folgen Behandlung weiterhin behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="ebac1-127">Safe string handling is a long-standing issue that continues to be addressed both by following good programming practices and often by using and retrofitting existing systems with secure, string-handling functions.</span></span> <span data-ttu-id="ebac1-128">Ein Beispiel für eine Reihe von Funktionen für die Windows-Shell beginnt mit [**stringcbcat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata).</span><span class="sxs-lookup"><span data-stu-id="ebac1-128">An example of such a set of functions for the Windows shell starts with [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata).</span></span>

 

 
