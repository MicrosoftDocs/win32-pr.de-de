---
description: Erstellt einen e/a-Abschluss Anschluss (Input/Output), ordnet ihn einem angegebenen Datei Handle zu oder erstellt einen e/a-Abschlussport, der noch keinem Datei Handle zugeordnet ist und die Zuordnung zu einem späteren Zeitpunkt zulässt.
ms.assetid: 40cb47fc-7b15-47f6-bee2-2611d4686053
title: Funktion "anateiocompletionport" (ioapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateIoCompletionPort
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: b85ec931e740de192655ada091a990cd97180b6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360582"
---
# <a name="createiocompletionport-function"></a><span data-ttu-id="2770c-103">Funktion "anateiocompletionport"</span><span class="sxs-lookup"><span data-stu-id="2770c-103">CreateIoCompletionPort function</span></span>

<span data-ttu-id="2770c-104">Erstellt einen e/a-Abschluss Anschluss (Input/Output), ordnet ihn einem angegebenen Datei Handle zu oder erstellt einen e/a-Abschlussport, der noch keinem Datei Handle zugeordnet ist und die Zuordnung zu einem späteren Zeitpunkt zulässt.</span><span class="sxs-lookup"><span data-stu-id="2770c-104">Creates an input/output (I/O) completion port and associates it with a specified file handle, or creates an I/O completion port that is not yet associated with a file handle, allowing association at a later time.</span></span>

<span data-ttu-id="2770c-105">Wenn Sie eine Instanz eines geöffneten Datei Handles mit einem e/a-Abschlussport verknüpfen, kann ein Prozess eine Benachrichtigung über den Abschluss von asynchronen e/a-Vorgängen, die das Datei Handle betreffen, empfangen.</span><span class="sxs-lookup"><span data-stu-id="2770c-105">Associating an instance of an opened file handle with an I/O completion port allows a process to receive notification of the completion of asynchronous I/O operations involving that file handle.</span></span>

> [!Note]
>
> <span data-ttu-id="2770c-106">Der hier verwendete Begriff " *Datei Handle* " bezieht sich auf eine System Abstraktion, die einen überlappenden e/a-Endpunkt darstellt, nicht nur auf eine Datei auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="2770c-106">The term *file handle* as used here refers to a system abstraction that represents an overlapped I/O endpoint, not only a file on disk.</span></span> <span data-ttu-id="2770c-107">Alle Systemobjekte, die überlappende e/a-Vorgänge unterstützen, z. b. Netzwerk Endpunkte, TCP-Sockets, Named Pipes und e-Mail-Slots, können als Datei Handles verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2770c-107">Any system objects that support overlapped I/O such as network endpoints, TCP sockets, named pipes, and mail slots can be used as file handles.</span></span> <span data-ttu-id="2770c-108">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="2770c-108">For additional information, see the Remarks section.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="2770c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2770c-109">Syntax</span></span>


```C++
HANDLE WINAPI CreateIoCompletionPort(
  _In_     HANDLE    FileHandle,
  _In_opt_ HANDLE    ExistingCompletionPort,
  _In_     ULONG_PTR CompletionKey,
  _In_     DWORD     NumberOfConcurrentThreads
);
```



## <a name="parameters"></a><span data-ttu-id="2770c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2770c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2770c-111">*FILEHANDLE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2770c-111">*FileHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2770c-112">Ein geöffnetes Datei Handle oder ein **ungültiger \_ handle- \_ Wert**.</span><span class="sxs-lookup"><span data-stu-id="2770c-112">An open file handle or **INVALID\_HANDLE\_VALUE**.</span></span>

<span data-ttu-id="2770c-113">Das Handle muss ein Objekt sein, das überlappende e/a unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2770c-113">The handle must be to an object that supports overlapped I/O.</span></span>

<span data-ttu-id="2770c-114">Wenn ein Handle bereitgestellt wird, muss es für überlappende e/a-Vervollständigung geöffnet worden sein.</span><span class="sxs-lookup"><span data-stu-id="2770c-114">If a handle is provided, it has to have been opened for overlapped I/O completion.</span></span> <span data-ttu-id="2770c-115">Beispielsweise müssen Sie das überlappende Flag für das **\_ Dateiflag \_** angeben, wenn [**Sie das Handle mithilfe der Funktion "**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) -Funktion" abrufen.</span><span class="sxs-lookup"><span data-stu-id="2770c-115">For example, you must specify the **FILE\_FLAG\_OVERLAPPED** flag when using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function to obtain the handle.</span></span>

<span data-ttu-id="2770c-116">Wenn ein **ungültiger \_ handle- \_ Wert** angegeben wird, erstellt die Funktion einen e/a-Abschlussport, ohne ihn einem Datei Handle zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="2770c-116">If **INVALID\_HANDLE\_VALUE** is specified, the function creates an I/O completion port without associating it with a file handle.</span></span> <span data-ttu-id="2770c-117">In diesem Fall muss der *existingcompletionport* -Parameter **null** sein, und der *completionkey* -Parameter wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="2770c-117">In this case, the *ExistingCompletionPort* parameter must be **NULL** and the *CompletionKey* parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="2770c-118">*Existingcompletionport* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="2770c-118">*ExistingCompletionPort* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2770c-119">Ein Handle für einen vorhandenen e/a-Abschlussport oder **null**.</span><span class="sxs-lookup"><span data-stu-id="2770c-119">A handle to an existing I/O completion port or **NULL**.</span></span>

<span data-ttu-id="2770c-120">Wenn dieser Parameter einen vorhandenen e/a-Abschlussport angibt, ordnet die Funktion ihn dem Handle zu, das durch den *FILEHANDLE* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2770c-120">If this parameter specifies an existing I/O completion port, the function associates it with the handle specified by the *FileHandle* parameter.</span></span> <span data-ttu-id="2770c-121">Die-Funktion gibt bei erfolgreicher Ausführung das Handle des vorhandenen e/a-Abschlussports zurück. Es wird kein neuer e/a-Abschlussport erstellt.</span><span class="sxs-lookup"><span data-stu-id="2770c-121">The function returns the handle of the existing I/O completion port if successful; it does not create a new I/O completion port.</span></span>

<span data-ttu-id="2770c-122">Wenn dieser Parameter **null** ist, wird von der Funktion ein neuer e/a-Abschlussport erstellt und, wenn der *FILEHANDLE* -Parameter gültig ist, der neue e/a-Abschlussport zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="2770c-122">If this parameter is **NULL**, the function creates a new I/O completion port and, if the *FileHandle* parameter is valid, associates it with the new I/O completion port.</span></span> <span data-ttu-id="2770c-123">Andernfalls erfolgt keine Zuordnung von Datei Handles.</span><span class="sxs-lookup"><span data-stu-id="2770c-123">Otherwise no file handle association occurs.</span></span> <span data-ttu-id="2770c-124">Bei erfolgreicher Ausführung gibt die Funktion das Handle an den neuen e/a-Abschlussport zurück.</span><span class="sxs-lookup"><span data-stu-id="2770c-124">The function returns the handle to the new I/O completion port if successful.</span></span>

</dd> <dt>

<span data-ttu-id="2770c-125">*Completionkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2770c-125">*CompletionKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2770c-126">Der benutzerdefinierte Vervollständigungs Schlüssel pro handle, der in jedem e/a-abschlusspaket für das angegebene Datei Handle enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="2770c-126">The per-handle user-defined completion key that is included in every I/O completion packet for the specified file handle.</span></span> <span data-ttu-id="2770c-127">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="2770c-127">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="2770c-128">*Anzahl von concurrentthreads* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2770c-128">*NumberOfConcurrentThreads* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2770c-129">Die maximale Anzahl von Threads, die das Betriebssystem für die gleichzeitige Verarbeitung von e/a-Abschluss Paketen für den e/a-Abschlussport zulassen kann.</span><span class="sxs-lookup"><span data-stu-id="2770c-129">The maximum number of threads that the operating system can allow to concurrently process I/O completion packets for the I/O completion port.</span></span> <span data-ttu-id="2770c-130">Dieser Parameter wird ignoriert, wenn der *existingcompletionport* -Parameter nicht **null** ist.</span><span class="sxs-lookup"><span data-stu-id="2770c-130">This parameter is ignored if the *ExistingCompletionPort* parameter is not **NULL**.</span></span>

<span data-ttu-id="2770c-131">Wenn dieser Parameter NULL ist, lässt das System so viele gleichzeitig ausgeführten Threads zu, wie Prozessoren im System vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="2770c-131">If this parameter is zero, the system allows as many concurrently running threads as there are processors in the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2770c-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2770c-132">Return value</span></span>

<span data-ttu-id="2770c-133">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert das Handle für einen e/a-Abschlussport:</span><span class="sxs-lookup"><span data-stu-id="2770c-133">If the function succeeds, the return value is the handle to an I/O completion port:</span></span>

-   <span data-ttu-id="2770c-134">Wenn der *existingcompletionport* -Parameter **null** war, ist der Rückgabewert ein neues handle.</span><span class="sxs-lookup"><span data-stu-id="2770c-134">If the *ExistingCompletionPort* parameter was **NULL**, the return value is a new handle.</span></span>

-   <span data-ttu-id="2770c-135">Wenn der *existingcompletionport* -Parameter ein gültiger e/a-Abschluss Port Handle war, ist der Rückgabewert derselbe handle.</span><span class="sxs-lookup"><span data-stu-id="2770c-135">If the *ExistingCompletionPort* parameter was a valid I/O completion port handle, the return value is that same handle.</span></span>

-   <span data-ttu-id="2770c-136">Wenn der *FILEHANDLE* -Parameter ein gültiges Handle war, ist dieses Datei Handle nun dem zurückgegebenen e/a-Abschlussport zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="2770c-136">If the *FileHandle* parameter was a valid handle, that file handle is now associated with the returned I/O completion port.</span></span>

<span data-ttu-id="2770c-137">Wenn die Funktion fehlschlägt, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="2770c-137">If the function fails, the return value is **NULL**.</span></span> <span data-ttu-id="2770c-138">Um erweiterte Fehlerinformationen abzurufen, müssen Sie die [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2770c-138">To get extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="2770c-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2770c-139">Remarks</span></span>

<span data-ttu-id="2770c-140">Das e/a-System kann angewiesen werden, e/a-Abschluss Benachrichtigungs Pakete an e/a-Abschlussports zu senden, wo Sie in die Warteschlange gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="2770c-140">The I/O system can be instructed to send I/O completion notification packets to I/O completion ports, where they are queued.</span></span> <span data-ttu-id="2770c-141">Diese Funktion wird **von der Funktion** "-Funktion" (Funktion) bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="2770c-141">The **CreateIoCompletionPort** function provides this functionality.</span></span>

<span data-ttu-id="2770c-142">Ein e/a-Abschlussport und sein Handle sind dem Prozess zugeordnet, der ihn erstellt hat und der nicht zwischen Prozessen freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="2770c-142">An I/O completion port and its handle are associated with the process that created it and is not sharable between processes.</span></span> <span data-ttu-id="2770c-143">Ein einzelnes Handle kann jedoch zwischen Threads im gleichen Prozess freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2770c-143">However, a single handle is sharable between threads in the same process.</span></span>

<span data-ttu-id="2770c-144">" **Kreateiocompletionport** " kann in drei verschiedenen Modi verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="2770c-144">**CreateIoCompletionPort** can be used in three distinct modes:</span></span>

-   <span data-ttu-id="2770c-145">Erstellen Sie nur einen e/a-Abschlussport, ohne ihn einem Datei Handle zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="2770c-145">Create only an I/O completion port without associating it with a file handle.</span></span>
-   <span data-ttu-id="2770c-146">Ordnen Sie einen vorhandenen e/a-Abschlussport einem Datei Handle zu.</span><span class="sxs-lookup"><span data-stu-id="2770c-146">Associate an existing I/O completion port with a file handle.</span></span>
-   <span data-ttu-id="2770c-147">Führt sowohl die Erstellung als auch die Zuordnung in einem einzelnen-Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="2770c-147">Perform both creation and association in a single call.</span></span>

<span data-ttu-id="2770c-148">Um einen e/a-Abschlussport ohne Zuordnung zu erstellen, legen Sie den *FILEHANDLE* -Parameter auf **einen ungültigen \_ handle- \_ Wert**, den *existingcompletionport* -Parameter auf **null** und den *completionkey* -Parameter auf 0 (null) fest (Dies wird in diesem Fall ignoriert).</span><span class="sxs-lookup"><span data-stu-id="2770c-148">To create an I/O completion port without associating it, set the *FileHandle* parameter to **INVALID\_HANDLE\_VALUE**, the *ExistingCompletionPort* parameter to **NULL**, and the *CompletionKey* parameter to zero (which is ignored in this case).</span></span> <span data-ttu-id="2770c-149">Legen Sie den Parameter " *numofconcurrentthreads* " auf den gewünschten Parallelitäts Wert für den neuen e/a-Abschlussport oder NULL für den Standardwert (die Anzahl der Prozessoren im System) fest.</span><span class="sxs-lookup"><span data-stu-id="2770c-149">Set the *NumberOfConcurrentThreads* parameter to the desired concurrency value for the new I/O completion port, or zero for the default (the number of processors in the system).</span></span>

<span data-ttu-id="2770c-150">Das Handle, das im *FILEHANDLE* -Parameter übergeben wird, kann ein beliebiges Handle sein, das überlappende e/a unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2770c-150">The handle passed in the *FileHandle* parameter can be any handle that supports overlapped I/O.</span></span> <span data-ttu-id="2770c-151">In den meisten Fällen handelt es sich hierbei um ein Handle [**, das von der Funktion "**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) " mit dem überlappenden Flag " **\_ Dateiflag \_** " geöffnet wird (z. b. Dateien, Postfächer und Pipes).</span><span class="sxs-lookup"><span data-stu-id="2770c-151">Most commonly, this is a handle opened by the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function using the **FILE\_FLAG\_OVERLAPPED** flag (for example, files, mail slots, and pipes).</span></span> <span data-ttu-id="2770c-152">Objekte, die von anderen Funktionen wie [**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) erstellt werden, können auch einem e/a-Abschlussport zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="2770c-152">Objects created by other functions such as [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) can also be associated with an I/O completion port.</span></span> <span data-ttu-id="2770c-153">Ein Beispiel für die Verwendung von Sockets finden Sie unter [**Accept tex**](/windows/desktop/api/mswsock/nf-mswsock-acceptex).</span><span class="sxs-lookup"><span data-stu-id="2770c-153">For an example using sockets, see [**AcceptEx**](/windows/desktop/api/mswsock/nf-mswsock-acceptex).</span></span> <span data-ttu-id="2770c-154">Ein Handle kann nur einem e/a-Abschlussport zugeordnet werden, und nachdem die Zuordnung erfolgt ist, bleibt das Handle diesem e/a-Abschlussport zugeordnet, bis er geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="2770c-154">A handle can be associated with only one I/O completion port, and after the association is made, the handle remains associated with that I/O completion port until it is closed.</span></span>

<span data-ttu-id="2770c-155">Weitere Informationen zu e/a-Abschluss Port Theorie, Verwendung und zugehörigen Funktionen finden Sie unter e [/](i-o-completion-ports.md)a-Abschlussports.</span><span class="sxs-lookup"><span data-stu-id="2770c-155">For more information on I/O completion port theory, usage, and associated functions, see [I/O Completion Ports](i-o-completion-ports.md).</span></span>

<span data-ttu-id="2770c-156">Mehrere Datei Handles können einem einzelnen e/a-Abschlussport zugeordnet werden, indem **CreateIoCompletionPort** mehrmals mit dem gleichen e/a-Abschluss Port Handle im *existingcompletionport* -Parameter und einem anderen Datei Handle im *FILEHANDLE* -Parameter aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2770c-156">Multiple file handles can be associated with a single I/O completion port by calling **CreateIoCompletionPort** multiple times with the same I/O completion port handle in the *ExistingCompletionPort* parameter and a different file handle in the *FileHandle* parameter each time.</span></span>

<span data-ttu-id="2770c-157">Verwenden Sie den *completionkey* -Parameter, um Ihre Anwendung zu unterstützen, welche e/a-Vorgänge abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="2770c-157">Use the *CompletionKey* parameter to help your application track which I/O operations have completed.</span></span> <span data-ttu-id="2770c-158">Dieser Wert wird nicht von " **kreateiocompletionport** " für funktionale Steuerelemente verwendet. Stattdessen wird Sie an das im *FILEHANDLE* -Parameter angegebene Datei Handle zum Zeitpunkt der Zuordnung mit einem e/a-Abschlussport angefügt.</span><span class="sxs-lookup"><span data-stu-id="2770c-158">This value is not used by **CreateIoCompletionPort** for functional control; rather, it is attached to the file handle specified in the *FileHandle* parameter at the time of association with an I/O completion port.</span></span> <span data-ttu-id="2770c-159">Dieser Vervollständigungs Schlüssel sollte für jedes Datei Handle eindeutig sein, und er begleitet das Datei Handle während des internen Beendigungs Warteschlangen Prozesses.</span><span class="sxs-lookup"><span data-stu-id="2770c-159">This completion key should be unique for each file handle, and it accompanies the file handle throughout the internal completion queuing process.</span></span> <span data-ttu-id="2770c-160">Sie wird beim Eintreffen eines Vervollständigungs Pakets im [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) -Funktions Aufrufwert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2770c-160">It is returned in the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function call when a completion packet arrives.</span></span> <span data-ttu-id="2770c-161">Der *completionkey* -Parameter wird auch von der [**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md) -Funktion verwendet, um Ihre eigenen speziellen Vervollständigungs Pakete in die Warteschlange zu stellen.</span><span class="sxs-lookup"><span data-stu-id="2770c-161">The *CompletionKey* parameter is also used by the [**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md) function to queue your own special-purpose completion packets.</span></span>

<span data-ttu-id="2770c-162">Nachdem eine Instanz eines geöffneten Handles einem e/a-Abschlussport zugeordnet ist, kann Sie nicht in der Funktion "read [**fileex**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) " oder " [**schreitefileex**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) " verwendet werden, da diese Funktionen über eigene asynchrone e/a-Mechanismen verfügen.</span><span class="sxs-lookup"><span data-stu-id="2770c-162">After an instance of an open handle is associated with an I/O completion port, it cannot be used in the [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) or [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) function because these functions have their own asynchronous I/O mechanisms.</span></span>

<span data-ttu-id="2770c-163">Es empfiehlt sich, ein Datei Handle, das einem e/a-Abschlussport zugeordnet ist, entweder mithilfe der Vererbung von Handles oder eines Aufrufes der [**dupligehandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) -Funktion nicht freizugeben.</span><span class="sxs-lookup"><span data-stu-id="2770c-163">It is best not to share a file handle associated with an I/O completion port by using either handle inheritance or a call to the [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) function.</span></span> <span data-ttu-id="2770c-164">Mit diesen doppelten Handles ausgeführte Vorgänge generieren Abschluss Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="2770c-164">Operations performed with such duplicate handles generate completion notifications.</span></span> <span data-ttu-id="2770c-165">Eine sorgfältige Überlegung wird empfohlen.</span><span class="sxs-lookup"><span data-stu-id="2770c-165">Careful consideration is advised.</span></span>

<span data-ttu-id="2770c-166">Der e/a-Abschluss Port Handle und jedes Datei Handle, das diesem bestimmten e/a-Abschlussport zugeordnet ist, werden als *Verweise auf den e/* a-Abschlussport bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="2770c-166">The I/O completion port handle and every file handle associated with that particular I/O completion port are known as *references to the I/O completion port*.</span></span> <span data-ttu-id="2770c-167">Der e/a-Abschlussport wird freigegeben, wenn keine Verweise mehr vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="2770c-167">The I/O completion port is released when there are no more references to it.</span></span> <span data-ttu-id="2770c-168">Daher müssen alle diese Handles ordnungsgemäß geschlossen werden, um den e/a-Abschlussport und seine zugeordneten Systemressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="2770c-168">Therefore, all of these handles must be properly closed to release the I/O completion port and its associated system resources.</span></span> <span data-ttu-id="2770c-169">Nachdem diese Bedingungen erfüllt sind, schließen Sie den e/a-Abschluss Port handle, indem Sie die [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2770c-169">After these conditions are satisfied, close the I/O completion port handle by calling the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span>

<span data-ttu-id="2770c-170">In Windows 8 und Windows Server 2012 wird diese Funktion von den folgenden Technologien unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2770c-170">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="2770c-171">Technologie</span><span class="sxs-lookup"><span data-stu-id="2770c-171">Technology</span></span>                                           | <span data-ttu-id="2770c-172">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="2770c-172">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="2770c-173">Server Message Block-Protokoll (SMB) 3,0</span><span class="sxs-lookup"><span data-stu-id="2770c-173">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="2770c-174">Ja</span><span class="sxs-lookup"><span data-stu-id="2770c-174">Yes</span></span><br/> |
| <span data-ttu-id="2770c-175">SMB 3,0 transparent Failover (TFO)</span><span class="sxs-lookup"><span data-stu-id="2770c-175">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="2770c-176">Ja</span><span class="sxs-lookup"><span data-stu-id="2770c-176">Yes</span></span><br/> |
| <span data-ttu-id="2770c-177">SMB 3,0 mit Dateifreigaben mit horizontaler Skalierung (also)</span><span class="sxs-lookup"><span data-stu-id="2770c-177">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="2770c-178">Ja</span><span class="sxs-lookup"><span data-stu-id="2770c-178">Yes</span></span><br/> |
| <span data-ttu-id="2770c-179">Freigegebenes Clustervolume Datei System (csvfs)</span><span class="sxs-lookup"><span data-stu-id="2770c-179">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="2770c-180">Ja</span><span class="sxs-lookup"><span data-stu-id="2770c-180">Yes</span></span><br/> |
| <span data-ttu-id="2770c-181">Robustes Dateisystem (Resilient File System, ReFS)</span><span class="sxs-lookup"><span data-stu-id="2770c-181">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="2770c-182">Ja</span><span class="sxs-lookup"><span data-stu-id="2770c-182">Yes</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2770c-183">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2770c-183">Requirements</span></span>



| <span data-ttu-id="2770c-184">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2770c-184">Requirement</span></span> | <span data-ttu-id="2770c-185">Wert</span><span class="sxs-lookup"><span data-stu-id="2770c-185">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2770c-186">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2770c-186">Minimum supported client</span></span><br/> | <span data-ttu-id="2770c-187">\[UWP-Apps für Windows XP-Desktop-Apps \|\]</span><span class="sxs-lookup"><span data-stu-id="2770c-187">Windows XP \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="2770c-188">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2770c-188">Minimum supported server</span></span><br/> | <span data-ttu-id="2770c-189">Windows Server 2003 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="2770c-189">Windows Server 2003 \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="2770c-190">Header</span><span class="sxs-lookup"><span data-stu-id="2770c-190">Header</span></span><br/>                   | <dl> <span data-ttu-id="2770c-191"><dt>Ioapi. h (Include Windows. h); </dt> <dt>Winbase. h unter Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2770c-191"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="2770c-192">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2770c-192">Library</span></span><br/>                  | <dl> <span data-ttu-id="2770c-193"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="2770c-193"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                                                  |
| <span data-ttu-id="2770c-194">DLL</span><span class="sxs-lookup"><span data-stu-id="2770c-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2770c-195"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2770c-195"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a><span data-ttu-id="2770c-196">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2770c-196">See also</span></span>

<dl> <dt>

<span data-ttu-id="2770c-197">**Übersichts Themen**</span><span class="sxs-lookup"><span data-stu-id="2770c-197">**Overview Topics**</span></span>
</dt> <dt>

[<span data-ttu-id="2770c-198">Dateiverwaltungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="2770c-198">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="2770c-199">E/a-Abschlussports</span><span class="sxs-lookup"><span data-stu-id="2770c-199">I/O Completion Ports</span></span>](i-o-completion-ports.md)
</dt> <dt>

[<span data-ttu-id="2770c-200">Verwenden der Windows-Header</span><span class="sxs-lookup"><span data-stu-id="2770c-200">Using the Windows Headers</span></span>](/windows/desktop/WinProg/using-the-windows-headers)
</dt> <dt>

[<span data-ttu-id="2770c-201">Windows Sockets 2</span><span class="sxs-lookup"><span data-stu-id="2770c-201">Windows Sockets 2</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

<span data-ttu-id="2770c-202">**Funktionen**</span><span class="sxs-lookup"><span data-stu-id="2770c-202">**Functions**</span></span>
</dt> <dt>

[<span data-ttu-id="2770c-203">**Akzeptex**</span><span class="sxs-lookup"><span data-stu-id="2770c-203">**AcceptEx**</span></span>](/windows/desktop/api/mswsock/nf-mswsock-acceptex)
</dt> <dt>

[<span data-ttu-id="2770c-204">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="2770c-204">**CreateFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="2770c-205">**Duplialisiehandle**</span><span class="sxs-lookup"><span data-stu-id="2770c-205">**DuplicateHandle**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)
</dt> <dt>

[<span data-ttu-id="2770c-206">**GetQueuedCompletionStatus**</span><span class="sxs-lookup"><span data-stu-id="2770c-206">**GetQueuedCompletionStatus**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[<span data-ttu-id="2770c-207">**GetQueuedCompletionStatus usex**</span><span class="sxs-lookup"><span data-stu-id="2770c-207">**GetQueuedCompletionStatusEx**</span></span>](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[<span data-ttu-id="2770c-208">**' PostQueuedCompletionStatus '**</span><span class="sxs-lookup"><span data-stu-id="2770c-208">**PostQueuedCompletionStatus**</span></span>](postqueuedcompletionstatus.md)
</dt> <dt>

[<span data-ttu-id="2770c-209">**ReadFileEx**</span><span class="sxs-lookup"><span data-stu-id="2770c-209">**ReadFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)
</dt> <dt>

[<span data-ttu-id="2770c-210">**WriteFileEx**</span><span class="sxs-lookup"><span data-stu-id="2770c-210">**WriteFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)
</dt> </dl>

 

