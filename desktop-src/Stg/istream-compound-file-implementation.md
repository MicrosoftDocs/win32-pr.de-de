---
title: Implementierung von IStream-Verbund Dateien
description: Die IStream-Schnittstelle unterstützt das Lesen und Schreiben von Daten in Streamobjekte. In einem strukturierten Speicher Objekt enthalten Streamobjekte die Daten, und die Speicher stellen die Struktur bereit.
ms.assetid: 52474e37-0e14-4dcc-8e04-4442cfd26eb3
keywords:
- IStream-Schnittstellen-STG, Implementierung von Verbund Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d15e671521f4a1e81b78579bc1225eccb48898
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "106364271"
---
# <a name="istream---compound-file-implementation"></a><span data-ttu-id="6d3e7-105">Implementierung von IStream-Verbund Dateien</span><span class="sxs-lookup"><span data-stu-id="6d3e7-105">IStream - Compound File Implementation</span></span>

<span data-ttu-id="6d3e7-106">Die [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) -Schnittstelle unterstützt das Lesen und Schreiben von Daten in Streamobjekte.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-106">The [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) interface supports reading and writing data to stream objects.</span></span> <span data-ttu-id="6d3e7-107">In einem strukturierten Speicher Objekt enthalten Streamobjekte die Daten, und die Speicher stellen die Struktur bereit.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-107">In a structured storage object, stream objects contain the data and storages provide the structure.</span></span> <span data-ttu-id="6d3e7-108">Einfache Daten können direkt in einen Stream geschrieben werden, aber häufig sind Streams Elemente, die in einem Speicher Objekt geschachtelt sind.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-108">Simple data can be written directly to a stream, but more frequently, streams are elements nested within a storage object.</span></span> <span data-ttu-id="6d3e7-109">Sie ähneln Standard Dateien.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-109">They are similar to standard files.</span></span>

<span data-ttu-id="6d3e7-110">Die Spezifikation von [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) definiert mehr Funktionen, als von der com-Implementierung unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-110">The specification of [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) defines more functionality than the COM implementation supports.</span></span> <span data-ttu-id="6d3e7-111">Die **IStream** -Schnittstelle definiert z. b. Datenströme bis zu 2 ⁶ ⁴ Bytes, die einen 64-Bit-Such Zeiger erfordern.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-111">For example, the **IStream** interface defines streams up to 2⁶⁴ bytes in length requiring a 64-bit seek pointer.</span></span> <span data-ttu-id="6d3e7-112">Die com-Implementierung unterstützt jedoch nur Datenströme mit einer Länge von bis zu 2 ³ ² (4 GB), Lese-und Schreibvorgänge sind immer auf jeweils 2 ³ ² Byte beschränkt.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-112">However, the COM implementation only supports streams up to 2³² bytes in length (4 GB) and read and write operations are always limited to 2³² bytes at a time.</span></span> <span data-ttu-id="6d3e7-113">Die com-Implementierung unterstützt auch keine Stream-Transaktions-oder Regions sperren.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-113">The COM implementation also does not support stream transactioning or region locking.</span></span>

<span data-ttu-id="6d3e7-114">Um einen einfachen Datenstrom auf der Grundlage des globalen Speichers zu erstellen, rufen Sie einen [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) -Zeiger ab, indem Sie die API-Funktion [**CreateStreamOnHGlobal**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-114">To create a simple stream based on global memory, get an [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) pointer by calling the API function [**CreateStreamOnHGlobal**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal).</span></span> <span data-ttu-id="6d3e7-115">Wenn Sie einen **IStream** -Zeiger innerhalb eines Verbund Datei Objekts abrufen möchten, müssen Sie entweder [**stgkreatedocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) oder [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-115">To get an **IStream** pointer within a compound file object, call either [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) or [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage).</span></span> <span data-ttu-id="6d3e7-116">Diese Funktionen rufen einen [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Zeiger ab, mit dem Sie dann für einen **IStream** -Zeiger " [**foratestream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) " oder " [**OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) " aufrufen können.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-116">These functions retrieve an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) pointer, with which you can then call [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) or [**OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) for an **IStream** pointer.</span></span> <span data-ttu-id="6d3e7-117">In beiden Fällen wird derselbe **IStream** -Implementierungs Code verwendet.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-117">In either case, the same **IStream** implementation code is used.</span></span>

> [!Note]  
> <span data-ttu-id="6d3e7-118">Die Implementierung der Verbund Datei von strukturiertem Speicher ist in einer [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode für [**ISequentialStream**](/windows/desktop/api/Objidl/nn-objidl-isequentialstream)nicht erfolgreich, enthält jedoch die [**Lese**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) -und [**Schreib**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) Methoden über den [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) -Schnittstellen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-118">The compound file implementation of structured storage does not succeed on a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method for [**ISequentialStream**](/windows/desktop/api/Objidl/nn-objidl-isequentialstream), but it includes the [**Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) and [**Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) methods through the [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) interface pointer.</span></span>

 

## <a name="when-to-use"></a><span data-ttu-id="6d3e7-119">Verwendungs Zeitpunkt</span><span class="sxs-lookup"><span data-stu-id="6d3e7-119">When to Use</span></span>

<span data-ttu-id="6d3e7-120">Ruft die Methoden von [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) auf, um Daten zu lesen und in einen Stream zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-120">Call the methods of [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) to read and write data to a stream.</span></span>

<span data-ttu-id="6d3e7-121">Da Stream-Objekte an andere Prozesse gemarshallt werden können, können Anwendungen die Daten in Speicher Objekten freigeben, ohne globalen Speicher verwenden zu müssen.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-121">Because stream objects can be marshaled to other processes, applications can share the data in storage objects without having to use global memory.</span></span> <span data-ttu-id="6d3e7-122">In der Implementierung der com-Verbund Datei von Streamobjekten wird durch die benutzerdefinierten Marshallingfunktionen in com eine Remote Version des ursprünglichen Objekts im neuen Prozess erstellt, wenn die beiden Prozesse über Shared-Memory-Zugriff verfügen.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-122">In the COM compound file implementation of stream objects, the custom marshaling facilities in COM create a remote version of the original object in the new process when the two processes have shared-memory access.</span></span> <span data-ttu-id="6d3e7-123">Folglich muss die Remote Version nicht mit dem ursprünglichen Prozess kommunizieren, um die zugehörigen Funktionen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-123">Thus, the remote version does not need to communicate with the original process to carry out its functions.</span></span>

<span data-ttu-id="6d3e7-124">Die Remote Version des Stream-Objekts nutzt denselben Such Zeiger wie der ursprüngliche Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-124">The remote version of the stream object shares the same seek pointer as the original stream.</span></span> <span data-ttu-id="6d3e7-125">Wenn Sie den Seek-Zeiger nicht freigeben möchten, verwenden Sie die [**IStream:: Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) -Methode, um eine Kopie des Datenstrom Objekts für den Remote Prozess bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-125">If you do not want to share the seek pointer, use the [**IStream::Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) method to provide a copy of the stream object for the remote process.</span></span>

> [!Note]
> <span data-ttu-id="6d3e7-126">Wenn Sie ein Streamobjekt erstellen, das größer als der Heap im Arbeitsspeicher Ihres Computers ist, und Sie ein **HGLOBAL** -Handle für ein globales Speicher Objekt verwenden, ruft das Stream-Objekt die [**globalrebelegc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) -Methode intern auf, wenn Sie mehr Arbeitsspeicher benötigt.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-126">If creating a stream object that is larger than the heap in your computer's memory and you are using an **HGLOBAL** handle to a global memory object, the stream object calls the [**GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) method internally whe it requires more memory.</span></span> <span data-ttu-id="6d3e7-127">Da **globalrezuweisungen** immer Daten aus der Quelle in das Ziel kopiert, erfordert die Erhöhung eines Streamobjekts von 20 MB auf 25 MB beispielsweise eine große Zeit Menge.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-127">Because **GlobalRealloc** always copies data from the source to the destination, increasing a stream object from 20 MB to 25 MB, for example, requires large amounts of time.</span></span> <span data-ttu-id="6d3e7-128">Dies liegt an der Größe der kopierten Inkremente und wird verschlechtert, wenn auf dem Computer weniger als 45 MB Arbeitsspeicher vorhanden sind, da Datenträger ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-128">This is due to the size of the increments copied and is worsened if there is less than 45 MB of memory on the computer because of disk swapping.</span></span>
>
> <span data-ttu-id="6d3e7-129">Die bevorzugte Lösung besteht darin, eine [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) -Methode zu implementieren, die von [**virtualbelegc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) zugeordnete Arbeitsspeicher anstelle von [**globalbelegc**](/windows/desktop/api/winbase/nf-winbase-globalalloc)verwendet.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-129">The preferred solution is to implement an [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) method that uses memory allocated by [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) instead of [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc).</span></span> <span data-ttu-id="6d3e7-130">Dadurch kann ein großer Teil des virtuellen Adressraums reserviert werden, und anschließend wird der Arbeitsspeicher in diesem Adressraum nach Bedarf übernommen.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-130">This can reserve a large chunk of virtual address space and then commit memory within that address space as required.</span></span> <span data-ttu-id="6d3e7-131">Es findet kein Daten Kopiervorgang statt, und der Arbeitsspeicher wird nur nach Bedarf committet.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-131">No data copying occurs and memory is committed only as it is required.</span></span>
>
> <span data-ttu-id="6d3e7-132">Eine Alternative zu [**GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) besteht darin, die [**IStream:: SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) -Methode für das Stream-Objekt aufzurufen, um die Speicher Belegung im Voraus zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-132">An alternative to [**GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) is to call the [**IStream::SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) method on the stream object to increase the memory allocation in advance.</span></span> <span data-ttu-id="6d3e7-133">Dies ist jedoch nicht so effizient wie die Verwendung von [**virtualzugewiesenen**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc), wie oben beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-133">This is not, however, as efficient as using [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc), as described above.</span></span>

 

## <a name="methods"></a><span data-ttu-id="6d3e7-134">Methoden</span><span class="sxs-lookup"><span data-stu-id="6d3e7-134">Methods</span></span>

<dl> <dt>

<span data-ttu-id="6d3e7-135"><span id="ISequentialStream__Read"></span><span id="isequentialstream__read"></span><span id="ISEQUENTIALSTREAM__READ"></span>[**ISequentialStream:: Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)</span><span class="sxs-lookup"><span data-stu-id="6d3e7-135"><span id="ISequentialStream__Read"></span><span id="isequentialstream__read"></span><span id="ISEQUENTIALSTREAM__READ"></span>[**ISequentialStream::Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)</span></span>
</dt> <dd>

<span data-ttu-id="6d3e7-136">Liest eine angegebene Anzahl von Bytes beginnend beim aktuellen Suchzeiger aus dem Datenstromobjekt in den Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-136">Reads a specified number of bytes from the stream object into memory starting at the current seek pointer.</span></span> <span data-ttu-id="6d3e7-137">Diese Implementierung gibt "S OK" zurück, \_ Wenn das Ende des Streams während des Lesevorgang erreicht wurde.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-137">This implementation returns S\_OK if the end of the stream was reached during the read.</span></span> <span data-ttu-id="6d3e7-138">(Dies ist das gleiche wie das "Dateiende"-Verhalten im DOS-FAT-Dateisystem.)</span><span class="sxs-lookup"><span data-stu-id="6d3e7-138">(This is the same as the "end of file" behavior found in the MS-DOS FAT file system.)</span></span>

</dd> <dt>

<span data-ttu-id="6d3e7-139"><span id="ISequentialStream__Write"></span><span id="isequentialstream__write"></span><span id="ISEQUENTIALSTREAM__WRITE"></span>[**ISequentialStream:: Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write)</span><span class="sxs-lookup"><span data-stu-id="6d3e7-139"><span id="ISequentialStream__Write"></span><span id="isequentialstream__write"></span><span id="ISEQUENTIALSTREAM__WRITE"></span>[**ISequentialStream::Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write)</span></span>
</dt> <dd>

<span data-ttu-id="6d3e7-140">Schreibt eine angegebene Anzahl von Bytes in das Streamobjekt, beginnend beim aktuellen Such Zeiger.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-140">Writes a specified number from bytes into the stream object starting at the current seek pointer.</span></span> <span data-ttu-id="6d3e7-141">In dieser Implementierung sind Streamobjekte nicht sparsam.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-141">In this implementation, stream objects are not sparse.</span></span> <span data-ttu-id="6d3e7-142">Alle Füll Bytes werden schließlich auf dem Datenträger zugeordnet und dem Stream zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-142">Any fill bytes are eventually allocated on the disk and assigned to the stream.</span></span>

</dd> <dt>

<span data-ttu-id="6d3e7-143"><span id="IStream__Seek"></span><span id="istream__seek"></span><span id="ISTREAM__SEEK"></span>[**IStream:: Seek**](/windows/desktop/api/Objidl/nf-objidl-istream-seek)</span><span class="sxs-lookup"><span data-stu-id="6d3e7-143"><span id="IStream__Seek"></span><span id="istream__seek"></span><span id="ISTREAM__SEEK"></span>[**IStream::Seek**](/windows/desktop/api/Objidl/nf-objidl-istream-seek)</span></span>
</dt> <dd>

<span data-ttu-id="6d3e7-144">Verschiebt den Suchzeiger auf eine neue Position im Verhältnis zum Anfang oder Ende des Datenstroms bzw. zum aktuellen Suchzeiger.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-144">Changes the seek pointer to a new location relative to the beginning of the stream, to the end of the stream, or to the current seek pointer.</span></span>

</dd> <dt>

<span data-ttu-id="6d3e7-145"><span id="IStream__SetSize"></span><span id="istream__setsize"></span><span id="ISTREAM__SETSIZE"></span>[**IStream:: SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize)</span><span class="sxs-lookup"><span data-stu-id="6d3e7-145"><span id="IStream__SetSize"></span><span id="istream__setsize"></span><span id="ISTREAM__SETSIZE"></span>[**IStream::SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize)</span></span>
</dt> <dd>

<span data-ttu-id="6d3e7-146">Ändert die Größe des Streamobjekts.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-146">Changes the size of the stream object.</span></span> <span data-ttu-id="6d3e7-147">In dieser Implementierung gibt es keine Garantie dafür, dass der zugeordnete Speicherplatz zusammenhängend ist.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-147">In this implementation, there is no guarantee that the space allocated will be contiguous.</span></span>

</dd> <dt>

<span data-ttu-id="6d3e7-148"><span id="IStream__CopyTo"></span><span id="istream__copyto"></span><span id="ISTREAM__COPYTO"></span>[**IStream:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto)</span><span class="sxs-lookup"><span data-stu-id="6d3e7-148"><span id="IStream__CopyTo"></span><span id="istream__copyto"></span><span id="ISTREAM__COPYTO"></span>[**IStream::CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto)</span></span>
</dt> <dd>

<span data-ttu-id="6d3e7-149">Kopiert eine angegebene Anzahl von Bytes vom aktuellen Suchzeiger im Datenstrom an den aktuellen Suchzeiger in einem anderen Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-149">Copies a specified number of bytes from the current seek pointer in the stream to the current seek pointer in another stream.</span></span>

</dd> <dt>

<span data-ttu-id="6d3e7-150"><span id="IStream__Commit"></span><span id="istream__commit"></span><span id="ISTREAM__COMMIT"></span>[**IStream:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istream-commit)</span><span class="sxs-lookup"><span data-stu-id="6d3e7-150"><span id="IStream__Commit"></span><span id="istream__commit"></span><span id="ISTREAM__COMMIT"></span>[**IStream::Commit**](/windows/desktop/api/Objidl/nf-objidl-istream-commit)</span></span>
</dt> <dd>

<span data-ttu-id="6d3e7-151">Die Implementierung der Verbund Datei von [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) unterstützt das Öffnen von Streams nur im direkten Modus, nicht im Transaktionsmodus.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-151">The compound file implementation of [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) supports opening streams only in direct mode, not transacted mode.</span></span> <span data-ttu-id="6d3e7-152">Daher hat die-Methode keine Auswirkung, wenn Sie nicht aufgerufen wird, um alle Speicherpuffer auf die nächste Speicher Ebene zu leeren.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-152">Therefore, the method has no effect when called other than to flush all memory buffers to the next storage level.</span></span>

<span data-ttu-id="6d3e7-153">In dieser Implementierung spielt es keine Rolle, ob Sie Änderungen an Streams übertragen. Sie benötigen nur Änderungen für Speicher Objekte.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-153">In this implementation, it does not matter if you commit changes to streams, you need only commit changes for storage objects.</span></span>

</dd> <dt>

<span data-ttu-id="6d3e7-154"><span id="IStream__Revert"></span><span id="istream__revert"></span><span id="ISTREAM__REVERT"></span>[**IStream:: Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert)</span><span class="sxs-lookup"><span data-stu-id="6d3e7-154"><span id="IStream__Revert"></span><span id="istream__revert"></span><span id="ISTREAM__REVERT"></span>[**IStream::Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert)</span></span>
</dt> <dd>

<span data-ttu-id="6d3e7-155">Diese Implementierung bietet keine Unterstützung für transaktive Streams, sodass ein Aufrufder Methode keine Auswirkung hat.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-155">This implementation does not support transacted streams, so a call to this method has no effect.</span></span>

</dd> <dt>

<span data-ttu-id="6d3e7-156"><span id="IStream__LockRegion"></span><span id="istream__lockregion"></span><span id="ISTREAM__LOCKREGION"></span>[**IStream:: LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion)</span><span class="sxs-lookup"><span data-stu-id="6d3e7-156"><span id="IStream__LockRegion"></span><span id="istream__lockregion"></span><span id="ISTREAM__LOCKREGION"></span>[**IStream::LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion)</span></span>
</dt> <dd>

<span data-ttu-id="6d3e7-157">Bereichs Sperren werden von dieser Implementierung nicht unterstützt, sodass ein aufrufender aufrufungsmethode keine Auswirkung hat.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-157">Range-locking is not supported by this implementation, so a call to this method has no effect.</span></span>

</dd> <dt>

<span data-ttu-id="6d3e7-158"><span id="IStream__UnlockRegion"></span><span id="istream__unlockregion"></span><span id="ISTREAM__UNLOCKREGION"></span>[**IStream:: UnlockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-unlockregion)</span><span class="sxs-lookup"><span data-stu-id="6d3e7-158"><span id="IStream__UnlockRegion"></span><span id="istream__unlockregion"></span><span id="ISTREAM__UNLOCKREGION"></span>[**IStream::UnlockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-unlockregion)</span></span>
</dt> <dd>

<span data-ttu-id="6d3e7-159">Entfernt die Zugriffsbeschränkung für einen Bereich von Bytes, der zuvor durch [**IStream:: LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion)eingeschränkt wurde.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-159">Removes the access restriction on a range of bytes previously restricted with [**IStream::LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion).</span></span>

</dd> <dt>

<span data-ttu-id="6d3e7-160"><span id="IStream__Stat"></span><span id="istream__stat"></span><span id="ISTREAM__STAT"></span>[**IStream:: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)</span><span class="sxs-lookup"><span data-stu-id="6d3e7-160"><span id="IStream__Stat"></span><span id="istream__stat"></span><span id="ISTREAM__STAT"></span>[**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)</span></span>
</dt> <dd>

<span data-ttu-id="6d3e7-161">Ruft die [**Statuslisten**](/windows/win32/api/objidl/ns-objidl-statstg) Struktur für diesen Datenstrom ab.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-161">Retrieves the [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) structure for this stream</span></span>

</dd> <dt>

<span data-ttu-id="6d3e7-162"><span id="IStream__Clone"></span><span id="istream__clone"></span><span id="ISTREAM__CLONE"></span>[**IStream:: Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone)</span><span class="sxs-lookup"><span data-stu-id="6d3e7-162"><span id="IStream__Clone"></span><span id="istream__clone"></span><span id="ISTREAM__CLONE"></span>[**IStream::Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone)</span></span>
</dt> <dd>

<span data-ttu-id="6d3e7-163">Erstellt ein neues Datenstromobjekt mit einem eigenen Suchzeiger, der auf die gleichen Bytes wie der Originaldatenstrom verweist.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-163">Creates a new stream object with its own seek pointer that references the same bytes as the original stream.</span></span>

</dd> </dl>

<span data-ttu-id="6d3e7-164">Ein [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) im einfachen Modus unterliegt den folgenden Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-164">A simple-mode [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) is subject to the following constraints.</span></span>

-   <span data-ttu-id="6d3e7-165">Ein Datenstrom ist der einfache Modus, wenn er von einem Speicher im einfachen Modus erstellt oder geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-165">A stream is simple mode if it was created or opened from a simple-mode storage.</span></span> <span data-ttu-id="6d3e7-166">Bei einem Speicher handelt es sich um einen einfachen Modus, wenn er erstellt oder geöffnet wird, wobei das \_ in der *GRF Mode* -Parameter festgelegte STGM Simple-Flag</span><span class="sxs-lookup"><span data-stu-id="6d3e7-166">A storage is simple mode if it is created or opened with the STGM\_SIMPLE flag set in the *grfMode* parameter.</span></span>
-   <span data-ttu-id="6d3e7-167">Die Methoden [**Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) und [**CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto) werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-167">The [**Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) and [**CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto) methods are not supported.</span></span>
-   <span data-ttu-id="6d3e7-168">Die [**stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) -Methode wird unterstützt, aber der STATFLAG- \_ Wert Noname muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-168">The [**Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) method is supported, but the STATFLAG\_NONAME value must be specified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d3e7-169">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6d3e7-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d3e7-170">**IStream**</span><span class="sxs-lookup"><span data-stu-id="6d3e7-170">**IStream**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> <dt>

[<span data-ttu-id="6d3e7-171">**IStorage**</span><span class="sxs-lookup"><span data-stu-id="6d3e7-171">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[<span data-ttu-id="6d3e7-172">**"Kreatestreamonhglobal"**</span><span class="sxs-lookup"><span data-stu-id="6d3e7-172">**CreateStreamOnHGlobal**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal)
</dt> <dt>

[<span data-ttu-id="6d3e7-173">**Stgkreatedocfile**</span><span class="sxs-lookup"><span data-stu-id="6d3e7-173">**StgCreateDocfile**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[<span data-ttu-id="6d3e7-174">**StgOpenStorage**</span><span class="sxs-lookup"><span data-stu-id="6d3e7-174">**StgOpenStorage**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> </dl>

 

 