---
description: Mit dem lokalen Thread Speicher (Thread Local Storage, TLS) können Sie eindeutige Daten für jeden Thread bereitstellen, auf den der Prozess mit einem globalen Index zugreifen kann. Ein Thread ordnet den Index zu, der von den anderen Threads zum Abrufen der eindeutigen Daten, die dem Index zugeordnet sind, verwendet werden kann.
ms.assetid: 40df7410-64d6-4edd-8009-d9c3d2aca920
title: Threadlokaler Speicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e17d2ff7a1ff253ce5a20b3921cc9605bf2989f6
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "104565862"
---
# <a name="thread-local-storage"></a><span data-ttu-id="8d35d-104">Threadlokaler Speicher</span><span class="sxs-lookup"><span data-stu-id="8d35d-104">Thread Local Storage</span></span>

<span data-ttu-id="8d35d-105">Alle Threads eines Prozesses teilen sich dessen virtuellen Adressraum.</span><span class="sxs-lookup"><span data-stu-id="8d35d-105">All threads of a process share its virtual address space.</span></span> <span data-ttu-id="8d35d-106">Die lokalen Variablen einer Funktion sind für jeden Thread, der die Funktion ausführt, eindeutig.</span><span class="sxs-lookup"><span data-stu-id="8d35d-106">The local variables of a function are unique to each thread that runs the function.</span></span> <span data-ttu-id="8d35d-107">Die statischen und globalen Variablen werden jedoch von allen Threads im Prozess gemeinsam genutzt.</span><span class="sxs-lookup"><span data-stu-id="8d35d-107">However, the static and global variables are shared by all threads in the process.</span></span> <span data-ttu-id="8d35d-108">Mit dem *lokalen Thread Speicher (Thread Local Storage* , TLS) können Sie eindeutige Daten für jeden Thread bereitstellen, auf den der Prozess mit einem globalen Index zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="8d35d-108">With *thread local storage* (TLS), you can provide unique data for each thread that the process can access using a global index.</span></span> <span data-ttu-id="8d35d-109">Ein Thread ordnet den Index zu, der von den anderen Threads zum Abrufen der eindeutigen Daten, die dem Index zugeordnet sind, verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8d35d-109">One thread allocates the index, which can be used by the other threads to retrieve the unique data associated with the index.</span></span>

<span data-ttu-id="8d35d-110">Der verfügbare Konstante TLS- \_ Wert \_ definiert die Mindestanzahl von TLS-Indizes, die in jedem Prozess verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="8d35d-110">The constant TLS\_MINIMUM\_AVAILABLE defines the minimum number of TLS indexes available in each process.</span></span> <span data-ttu-id="8d35d-111">Dieser Minimalwert ist garantiert mindestens 64 für alle Systeme.</span><span class="sxs-lookup"><span data-stu-id="8d35d-111">This minimum is guaranteed to be at least 64 for all systems.</span></span> <span data-ttu-id="8d35d-112">Die maximale Anzahl von Indizes pro Prozess ist 1.088.</span><span class="sxs-lookup"><span data-stu-id="8d35d-112">The maximum number of indexes per process is 1,088.</span></span>

<span data-ttu-id="8d35d-113">Wenn die Threads erstellt werden, ordnet das System ein Array von **LPVOID** -Werten für TLS zu, die mit NULL initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="8d35d-113">When the threads are created, the system allocates an array of **LPVOID** values for TLS, which are initialized to NULL.</span></span> <span data-ttu-id="8d35d-114">Bevor ein Index verwendet werden kann, muss er von einem der Threads zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="8d35d-114">Before an index can be used, it must be allocated by one of the threads.</span></span> <span data-ttu-id="8d35d-115">Jeder Thread speichert seine Daten für einen TLS-Index in einem *TLS-Slot* im Array.</span><span class="sxs-lookup"><span data-stu-id="8d35d-115">Each thread stores its data for a TLS index in a *TLS slot* in the array.</span></span> <span data-ttu-id="8d35d-116">Wenn die einem Index zugeordneten Daten in einen **LPVOID** -Wert passen, können Sie die Daten direkt im TLS-Slot speichern.</span><span class="sxs-lookup"><span data-stu-id="8d35d-116">If the data associated with an index will fit in an **LPVOID** value, you can store the data directly in the TLS slot.</span></span> <span data-ttu-id="8d35d-117">Wenn Sie jedoch eine große Anzahl von Indizes auf diese Weise verwenden, ist es besser, separaten Speicher zuzuordnen, die Daten zu konsolidieren und die Anzahl der verwendeten TLS-Slots zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="8d35d-117">However, if you are using a large number of indexes in this way, it is better to allocate separate storage, consolidate the data, and minimize the number of TLS slots in use.</span></span>

<span data-ttu-id="8d35d-118">Das folgende Diagramm veranschaulicht die Funktionsweise von TLS.</span><span class="sxs-lookup"><span data-stu-id="8d35d-118">The following diagram illustrates how TLS works.</span></span> <span data-ttu-id="8d35d-119">Ein Codebeispiel zur Veranschaulichung der Verwendung von lokalem Thread Speicher finden [Sie unter Verwenden von lokalem Thread Speicher](using-thread-local-storage.md).</span><span class="sxs-lookup"><span data-stu-id="8d35d-119">For a code example illustrating the use of thread local storage, see [Using Thread Local Storage](using-thread-local-storage.md).</span></span>

![Diagramm, das zeigt, wie der T L S-Prozess funktioniert.](images/tls.png)

<span data-ttu-id="8d35d-121">Der Prozess verfügt über zwei Threads: Thread 1 und Thread 2.</span><span class="sxs-lookup"><span data-stu-id="8d35d-121">The process has two threads, Thread 1 and Thread 2.</span></span> <span data-ttu-id="8d35d-122">Es ordnet zwei Indizes für die Verwendung mit TLS, gdwTlsIndex1 und gdwTlsIndex2 zu.</span><span class="sxs-lookup"><span data-stu-id="8d35d-122">It allocates two indexes for use with TLS, gdwTlsIndex1 and gdwTlsIndex2.</span></span> <span data-ttu-id="8d35d-123">Jeder Thread ordnet zwei Speicherblöcke (einen für jeden Index) zu, in denen die Daten gespeichert werden, und speichert die Zeiger auf diese Speicherblöcke in den entsprechenden TLS-Slots.</span><span class="sxs-lookup"><span data-stu-id="8d35d-123">Each thread allocates two memory blocks (one for each index) in which to store the data, and stores the pointers to these memory blocks in the corresponding TLS slots.</span></span> <span data-ttu-id="8d35d-124">Um auf die mit einem Index verknüpften Daten zuzugreifen, ruft der Thread den Zeiger auf den Speicherblock aus dem TLS-Slot ab und speichert ihn in der lokalen lpvdata-Variablen.</span><span class="sxs-lookup"><span data-stu-id="8d35d-124">To access the data associated with an index, the thread retrieves the pointer to the memory block from the TLS slot and stores it in the lpvData local variable.</span></span>

<span data-ttu-id="8d35d-125">Es ist ideal, TLS in einer Dynamic Link Library (dll) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8d35d-125">It is ideal to use TLS in a dynamic-link library (DLL).</span></span> <span data-ttu-id="8d35d-126">Ein Beispiel finden Sie unter [Verwenden von lokalem Thread Speicher in einer Dynamic Link Library](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md).</span><span class="sxs-lookup"><span data-stu-id="8d35d-126">For an example, see [Using Thread Local Storage in a Dynamic Link Library](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d35d-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8d35d-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d35d-128">Lokaler Thread Speicher (Visual C++)</span><span class="sxs-lookup"><span data-stu-id="8d35d-128">Thread Local Storage (Visual C++)</span></span>](/cpp/parallel/thread-local-storage-tls?view=vs-2019)
</dt> <dt>

[<span data-ttu-id="8d35d-129">Verwenden von TLS (threadlokaler Speicher)</span><span class="sxs-lookup"><span data-stu-id="8d35d-129">Using Thread Local Storage</span></span>](using-thread-local-storage.md)
</dt> <dt>

[<span data-ttu-id="8d35d-130">Verwenden des lokalen Thread Speichers in einer Dynamic Link Library</span><span class="sxs-lookup"><span data-stu-id="8d35d-130">Using Thread Local Storage in a Dynamic Link Library</span></span>](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md)
</dt> </dl>

 

 
