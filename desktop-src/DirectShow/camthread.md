---
description: Die Klasse "camthread" ist eine abstrakte Klasse zum Verwalten von Arbeitsthreads.
ms.assetid: c217d879-0203-4566-96ad-7463b05bc990
title: Camthread-Klasse (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5c2bde058267ae4c530f33a96778792d5fe247b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368392"
---
# <a name="camthread-class"></a><span data-ttu-id="2ed6d-103">Camthread-Klasse</span><span class="sxs-lookup"><span data-stu-id="2ed6d-103">CAMThread class</span></span>

<span data-ttu-id="2ed6d-104">Die- `CAMThread` Klasse ist eine abstrakte Klasse zum Verwalten von Arbeitsthreads.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-104">The `CAMThread` class is an abstract class for managing worker threads.</span></span>



| <span data-ttu-id="2ed6d-105">Geschützte Member-Variablen</span><span class="sxs-lookup"><span data-stu-id="2ed6d-105">Protected Member Variables</span></span>                                 | <span data-ttu-id="2ed6d-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2ed6d-106">Description</span></span>                                                                  |
|------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="2ed6d-107">**m \_ hThread**</span><span class="sxs-lookup"><span data-stu-id="2ed6d-107">**m\_hThread**</span></span>](camthread-m-hthread.md)                  | <span data-ttu-id="2ed6d-108">Handle für den Thread.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-108">Handle to the thread.</span></span>                                                        |
| <span data-ttu-id="2ed6d-109">Öffentliche Element Variablen</span><span class="sxs-lookup"><span data-stu-id="2ed6d-109">Public Member Variables</span></span>                                    | <span data-ttu-id="2ed6d-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2ed6d-110">Description</span></span>                                                                  |
| [<span data-ttu-id="2ed6d-111">**m \_ accesslock**</span><span class="sxs-lookup"><span data-stu-id="2ed6d-111">**m\_AccessLock**</span></span>](camthread-m-accesslock.md)            | <span data-ttu-id="2ed6d-112">Kritischer Abschnitt, der den Zugriff auf den Thread durch andere Threads sperrt.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-112">Critical section that locks the thread from being accessed by other threads.</span></span> |
| [<span data-ttu-id="2ed6d-113">**m \_ workerlock**</span><span class="sxs-lookup"><span data-stu-id="2ed6d-113">**m\_WorkerLock**</span></span>](camthread-m-workerlock.md)            | <span data-ttu-id="2ed6d-114">Kritischer Abschnitt, der die von Threads gemeinsam genutzten Daten sperrt.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-114">Critical section that locks data shared among threads.</span></span>                       |
| <span data-ttu-id="2ed6d-115">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="2ed6d-115">Public Methods</span></span>                                             | <span data-ttu-id="2ed6d-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2ed6d-116">Description</span></span>                                                                  |
| [<span data-ttu-id="2ed6d-117">**Camthread**</span><span class="sxs-lookup"><span data-stu-id="2ed6d-117">**CAMThread**</span></span>](camthread-camthread.md)                   | <span data-ttu-id="2ed6d-118">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-118">Constructor method.</span></span>                                                          |
| [<span data-ttu-id="2ed6d-119">**~ Camthread**</span><span class="sxs-lookup"><span data-stu-id="2ed6d-119">**~ CAMThread**</span></span>](camthread--camthread.md)                | <span data-ttu-id="2ed6d-120">Dekonstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-120">Destructor method.</span></span> <span data-ttu-id="2ed6d-121">Virtu.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-121">Virtual.</span></span>                                                  |
| [<span data-ttu-id="2ed6d-122">**Initialthumproc**</span><span class="sxs-lookup"><span data-stu-id="2ed6d-122">**InitialThreadProc**</span></span>](camthread-initialthreadproc.md)   | <span data-ttu-id="2ed6d-123">Ruft die ThreadProc-Methode auf, wenn der Thread erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-123">Calls the ThreadProc method when the thread is created.</span></span>                      |
| [<span data-ttu-id="2ed6d-124">**Stelle**</span><span class="sxs-lookup"><span data-stu-id="2ed6d-124">**Create**</span></span>](camthread-create.md)                         | <span data-ttu-id="2ed6d-125">Erstellt den Thread.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-125">Creates the thread.</span></span>                                                          |
| [<span data-ttu-id="2ed6d-126">**Callworker**</span><span class="sxs-lookup"><span data-stu-id="2ed6d-126">**CallWorker**</span></span>](camthread-callworker.md)                 | <span data-ttu-id="2ed6d-127">Signalisiert dem Thread eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-127">Signals the thread with a request.</span></span>                                           |
| [<span data-ttu-id="2ed6d-128">**Schließen**</span><span class="sxs-lookup"><span data-stu-id="2ed6d-128">**Close**</span></span>](camthread-close.md)                           | <span data-ttu-id="2ed6d-129">Wartet, bis der Thread beendet wird, und gibt dann seine Ressourcen frei.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-129">Waits for the thread to exit, then releases its resources.</span></span>                   |
| [<span data-ttu-id="2ed6d-130">**Threadexists**</span><span class="sxs-lookup"><span data-stu-id="2ed6d-130">**ThreadExists**</span></span>](camthread-threadexists.md)             | <span data-ttu-id="2ed6d-131">Fragt ab, ob der Thread vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-131">Queries whether the thread exists.</span></span>                                           |
| [<span data-ttu-id="2ed6d-132">**GetRequest**</span><span class="sxs-lookup"><span data-stu-id="2ed6d-132">**GetRequest**</span></span>](camthread-getrequest.md)                 | <span data-ttu-id="2ed6d-133">Wartet auf die nächste Anforderung.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-133">Waits for the next request.</span></span>                                                  |
| [<span data-ttu-id="2ed6d-134">**Check Request**</span><span class="sxs-lookup"><span data-stu-id="2ed6d-134">**CheckRequest**</span></span>](camthread-checkrequest.md)             | <span data-ttu-id="2ed6d-135">Überprüft, ob eine Anforderung vorhanden ist, ohne zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-135">Checks if there is a request, without blocking.</span></span>                              |
| [<span data-ttu-id="2ed6d-136">**Antwort**</span><span class="sxs-lookup"><span data-stu-id="2ed6d-136">**Reply**</span></span>](camthread-reply.md)                           | <span data-ttu-id="2ed6d-137">Antwortet auf eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-137">Replies to a request.</span></span>                                                        |
| [<span data-ttu-id="2ed6d-138">**Getrequesthandle**</span><span class="sxs-lookup"><span data-stu-id="2ed6d-138">**GetRequestHandle**</span></span>](camthread-getrequesthandle.md)     | <span data-ttu-id="2ed6d-139">Ruft ein Handle für das Ereignis ab, das von der callworker-Methode signalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-139">Retrieves a handle to the event signaled by the CallWorker method.</span></span>           |
| [<span data-ttu-id="2ed6d-140">**Getrequestparam**</span><span class="sxs-lookup"><span data-stu-id="2ed6d-140">**GetRequestParam**</span></span>](camthread-getrequestparam.md)       | <span data-ttu-id="2ed6d-141">Ruft die aktuelle Anforderung ab.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-141">Retrieves the latest request.</span></span>                                                |
| [<span data-ttu-id="2ed6d-142">**Coinitializehelper**</span><span class="sxs-lookup"><span data-stu-id="2ed6d-142">**CoInitializeHelper**</span></span>](camthread-coinitializehelper.md) | <span data-ttu-id="2ed6d-143">Ruft CoInitializeEx am Anfang des Threads auf.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-143">Calls CoInitializeEx at the start of the thread.</span></span>                             |
| <span data-ttu-id="2ed6d-144">Reine virtuelle Methoden</span><span class="sxs-lookup"><span data-stu-id="2ed6d-144">Pure Virtual Methods</span></span>                                       | <span data-ttu-id="2ed6d-145">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2ed6d-145">Description</span></span>                                                                  |
| [<span data-ttu-id="2ed6d-146">**ThreadProc**</span><span class="sxs-lookup"><span data-stu-id="2ed6d-146">**ThreadProc**</span></span>](camthread-threadproc.md)                 | <span data-ttu-id="2ed6d-147">Thread Prozedur.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-147">Thread procedure.</span></span>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="2ed6d-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ed6d-148">Remarks</span></span>

<span data-ttu-id="2ed6d-149">Diese Klasse stellt Methoden zum Erstellen eines Arbeits Thread, zum Übergeben von Anforderungen an den Thread und zum warten auf das Beenden des Threads bereit.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-149">This class provides methods for creating a worker thread, passing requests to the thread, and waiting for the thread to exit.</span></span> <span data-ttu-id="2ed6d-150">Gehen Sie folgendermaßen vor, um diese Klasse zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="2ed6d-150">To use this class, do the following:</span></span>

-   <span data-ttu-id="2ed6d-151">Leiten Sie eine Klasse von ab, `CAMThread` und überschreiben Sie die reine virtuelle Methode " [**camthread:: ThreadProc**](camthread-threadproc.md)".</span><span class="sxs-lookup"><span data-stu-id="2ed6d-151">Derive a class from `CAMThread` and override the pure virtual method [**CAMThread::ThreadProc**](camthread-threadproc.md).</span></span> <span data-ttu-id="2ed6d-152">Bei dieser Methode handelt es sich um die Thread Prozedur, die am Anfang des Threads aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-152">This method is the thread procedure that gets called at the start of the thread.</span></span>
-   <span data-ttu-id="2ed6d-153">Erstellen Sie in Ihrer Anwendung eine Instanz der abgeleiteten Klasse.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-153">In your application, create an instance of your derived class.</span></span> <span data-ttu-id="2ed6d-154">Beim Erstellen des Objekts wird der Thread nicht erstellt.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-154">Creating the object does not create the thread.</span></span> <span data-ttu-id="2ed6d-155">Um den Thread zu erstellen, rufen Sie die Methode " [**camthread:: Create**](camthread-create.md) " auf.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-155">To create the thread, call the [**CAMThread::Create**](camthread-create.md) method.</span></span>
-   <span data-ttu-id="2ed6d-156">Rufen Sie die Methode " [**camthread:: callworker**](camthread-callworker.md) " auf, um Anforderungen an den Thread zu senden.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-156">To send requests to the thread, call the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span> <span data-ttu-id="2ed6d-157">Diese Methode nimmt einen DWORD-Parameter an, dessen Bedeutung von ihrer Klasse definiert wird.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-157">This method takes a DWORD parameter, whose meaning is defined by your class.</span></span> <span data-ttu-id="2ed6d-158">Die-Methode wird blockiert, bis der Thread antwortet (siehe unten).</span><span class="sxs-lookup"><span data-stu-id="2ed6d-158">The method blocks until the thread responds (see below).</span></span>
-   <span data-ttu-id="2ed6d-159">Antworten Sie in ihrer Thread Prozedur auf Anforderungen, indem Sie entweder " [**camthread:: GetRequest**](camthread-getrequest.md) " oder " [**camthread:: CheckRequest**](camthread-checkrequest.md)" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-159">In your thread procedure, respond to requests by calling either [**CAMThread::GetRequest**](camthread-getrequest.md) or [**CAMThread::CheckRequest**](camthread-checkrequest.md).</span></span> <span data-ttu-id="2ed6d-160">Die GetRequest-Methode blockiert, bis ein anderer Thread callworker aufruft.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-160">The GetRequest method blocks until another thread calls CallWorker.</span></span> <span data-ttu-id="2ed6d-161">Die CheckRequest-Methode ist nicht blockierend, sodass der Thread bei asynchroner Arbeit auf neue Anforderungen prüfen kann.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-161">The CheckRequest method is non-blocking, which enables the thread to check for new requests while working asynchronously.</span></span>
-   <span data-ttu-id="2ed6d-162">Wenn der Thread eine Anforderung empfängt, rufen Sie " [**camthread:: Reply**](camthread-reply.md) " auf, um die Blockierung des aufrufenden Threads aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-162">When the thread receives a request, call [**CAMThread::Reply**](camthread-reply.md) to unblock the calling thread.</span></span> <span data-ttu-id="2ed6d-163">Die Reply-Methode nimmt einen DWORD-Parameter an, der als Rückgabewert für callworker an den aufrufenden Thread übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-163">The Reply method takes a DWORD parameter, which is passed to the calling thread as the return value for CallWorker.</span></span>

<span data-ttu-id="2ed6d-164">Wenn Sie mit dem Thread abgeschlossen sind, können Sie die Methode " [**camthread:: Close**](camthread-close.md) " aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-164">When you are done with the thread, call the [**CAMThread::Close**](camthread-close.md) method.</span></span> <span data-ttu-id="2ed6d-165">Diese Methode wartet darauf, dass der Thread beendet wird, und schließt dann das Thread handle.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-165">This method waits for the thread to exit, and then closes the thread handle.</span></span> <span data-ttu-id="2ed6d-166">Es ist sichergestellt, dass Ihre ThreadProc-Nachricht entweder eigenständig oder als Reaktion auf eine callworker-Anforderung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-166">Your ThreadProc message must be guaranteed to exit, either on its own or in response to a CallWorker request.</span></span> <span data-ttu-id="2ed6d-167">Die dekonstruktormethode ruft auch Close auf.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-167">The destructor method also calls Close.</span></span>

<span data-ttu-id="2ed6d-168">Diese Schritte werden im folgenden Beispiel veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="2ed6d-168">The following example illustrates these steps:</span></span>


```C++
class MyThread : public CAMThread
{
protected:
    DWORD ThreadProc(void);
};

DWORD MyThread::ThreadProc()
{
    BOOL bShutDown = FALSE;
    while (!bShutDown)
    {
        DWORD req = GetRequest();
        printf("Request: %d\n", req);
        bShutDown = (req == 0);
        Reply(bShutDown ? S_FALSE : S_OK);
    }
    printf("Quitting Thread\n");
    return 1;
}

void main()
{
    MyThread thread;
    DWORD reply;
    
    thread.Create();
    reply = thread.CallWorker(3);
    reply = thread.CallWorker(0); // Thread exits.
}
```



<span data-ttu-id="2ed6d-169">In ihrer abgeleiteten Klasse können Sie auch Element Funktionen definieren, die die Parameter an callworker überprüfen.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-169">In your derived class, you can also define member functions that validate the parameters to CallWorker.</span></span> <span data-ttu-id="2ed6d-170">Das folgende Beispiel zeigt eine typische Vorgehensweise:</span><span class="sxs-lookup"><span data-stu-id="2ed6d-170">The following example shows a typical way to do this:</span></span>


```C++
enum Command {CMD_INIT, CMD_RUN, CMD_STOP, CMD_EXIT};

HRESULT Init(void)  { return CallWorker(CMD_INIT); }
HRESULT Run(void)   { return CallWorker(CMD_RUN); }
HRESULT Stop(void)  { return CallWorker(CMD_STOP); }
HRESULT Exit(void)  { return CallWorker(CMD_EXIT); }
```



<span data-ttu-id="2ed6d-171">Die- `CAMThread` Klasse stellt zwei kritische Abschnitte als öffentliche Element Variablen bereit.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-171">The `CAMThread` class provides two critical sections as public member variables.</span></span> <span data-ttu-id="2ed6d-172">Verwenden `CAMThread::m_AccessLock` Sie, um den Zugriff auf den Thread durch andere Threads zu sperren.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-172">Use `CAMThread::m_AccessLock` to lock the thread from being accessed by other threads.</span></span> <span data-ttu-id="2ed6d-173">(Beispielsweise enthalten die Methoden Create und callworker diese Sperre, um Vorgänge für den Thread zu serialisieren.) Verwenden Sie " [**camthread:: m \_ workerlock**](camthread-m-workerlock.md) ", um Daten zu sperren, die von Threads gemeinsam genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-173">(For example, the Create and CallWorker methods hold this lock, to serialize operations on the thread.) Use [**CAMThread::m\_WorkerLock**](camthread-m-workerlock.md) to lock data that is shared among threads.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ed6d-174">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ed6d-174">Requirements</span></span>



| <span data-ttu-id="2ed6d-175">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2ed6d-175">Requirement</span></span> | <span data-ttu-id="2ed6d-176">Wert</span><span class="sxs-lookup"><span data-stu-id="2ed6d-176">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ed6d-177">Header</span><span class="sxs-lookup"><span data-stu-id="2ed6d-177">Header</span></span><br/>  | <dl> <span data-ttu-id="2ed6d-178"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2ed6d-178"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="2ed6d-179">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2ed6d-179">Library</span></span><br/> | <dl> <span data-ttu-id="2ed6d-180">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="2ed6d-180"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




