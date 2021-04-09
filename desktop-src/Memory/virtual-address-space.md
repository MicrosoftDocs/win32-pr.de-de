---
description: Der virtuelle Adressraum für einen Prozess ist der Satz von virtuellen Speicheradressen, der verwendet werden kann. Der Adressraum für jeden Prozess ist privat, und von anderen Prozessen kann nicht darauf zugegriffen werden, es sei denn, er ist freigegeben.
ms.assetid: 747f9f53-a595-4f4b-8b81-3123d59edb2f
title: Virtueller Adressraum (Speicherverwaltung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6584d0404799e6b0e5ab343c7d8b39d7f8d741a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959083"
---
# <a name="virtual-address-space-memory-management"></a><span data-ttu-id="4a4ce-104">Virtueller Adressraum (Speicherverwaltung)</span><span class="sxs-lookup"><span data-stu-id="4a4ce-104">Virtual Address Space (Memory Management)</span></span>

<span data-ttu-id="4a4ce-105">Der virtuelle Adressraum für einen Prozess ist der Satz von virtuellen Speicheradressen, der verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4a4ce-105">The virtual address space for a process is the set of virtual memory addresses that it can use.</span></span> <span data-ttu-id="4a4ce-106">Der Adressraum für jeden Prozess ist privat, und von anderen Prozessen kann nicht darauf zugegriffen werden, es sei denn, er ist freigegeben.</span><span class="sxs-lookup"><span data-stu-id="4a4ce-106">The address space for each process is private and cannot be accessed by other processes unless it is shared.</span></span>

<span data-ttu-id="4a4ce-107">Eine virtuelle Adresse stellt nicht den tatsächlichen physischen Speicherort eines Objekts im Arbeitsspeicher dar. Stattdessen behält das System eine *Seiten Tabelle* für jeden Prozess bei, bei dem es sich um eine interne Datenstruktur handelt, mit der virtuelle Adressen in die entsprechenden physischen Adressen übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="4a4ce-107">A virtual address does not represent the actual physical location of an object in memory; instead, the system maintains a *page table* for each process, which is an internal data structure used to translate virtual addresses into their corresponding physical addresses.</span></span> <span data-ttu-id="4a4ce-108">Jedes Mal, wenn ein Thread auf eine Adresse verweist, übersetzt das System die virtuelle Adresse in eine physische Adresse.</span><span class="sxs-lookup"><span data-stu-id="4a4ce-108">Each time a thread references an address, the system translates the virtual address to a physical address.</span></span>

<span data-ttu-id="4a4ce-109">Der virtuelle Adressraum für 32-Bit-Windows beträgt 4 Gigabyte (GB) und ist in zwei Partitionen unterteilt: eine für den Prozess und die andere für die Verwendung durch das System reserviert.</span><span class="sxs-lookup"><span data-stu-id="4a4ce-109">The virtual address space for 32-bit Windows is 4 gigabytes (GB) in size and divided into two partitions: one for use by the process and the other reserved for use by the system.</span></span> <span data-ttu-id="4a4ce-110">Weitere Informationen zum virtuellen Adressraum in 64-Bit-Fenstern finden Sie unter [Virtueller Adressraum in 64-Bit-Fenstern](../winprog64/virtual-address-space.md).</span><span class="sxs-lookup"><span data-stu-id="4a4ce-110">For more information about the virtual address space in 64-bit Windows, see [Virtual Address Space in 64-bit Windows](../winprog64/virtual-address-space.md).</span></span>

<span data-ttu-id="4a4ce-111">Weitere Informationen zum virtuellen Arbeitsspeicher finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="4a4ce-111">For more information about virtual memory, see the following topics:</span></span>

-   [<span data-ttu-id="4a4ce-112">Virtueller Adressraum und physischer Speicher</span><span class="sxs-lookup"><span data-stu-id="4a4ce-112">Virtual Address Space and Physical Storage</span></span>](virtual-address-space-and-physical-storage.md)
-   [<span data-ttu-id="4a4ce-113">Arbeitssatz</span><span class="sxs-lookup"><span data-stu-id="4a4ce-113">Working Set</span></span>](working-set.md)
-   [<span data-ttu-id="4a4ce-114">Seiten Status</span><span class="sxs-lookup"><span data-stu-id="4a4ce-114">Page State</span></span>](page-state.md)
-   [<span data-ttu-id="4a4ce-115">Bereich von zugewiesener Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="4a4ce-115">Scope of Allocated Memory</span></span>](scope-of-allocated-memory.md)
-   [<span data-ttu-id="4a4ce-116">Datenausführungsverhinderung</span><span class="sxs-lookup"><span data-stu-id="4a4ce-116">Data Execution Prevention</span></span>](data-execution-prevention.md)
-   [<span data-ttu-id="4a4ce-117">Arbeitsspeicherschutz</span><span class="sxs-lookup"><span data-stu-id="4a4ce-117">Memory Protection</span></span>](memory-protection.md)
-   [<span data-ttu-id="4a4ce-118">Arbeitsspeicher Grenzwerte für Windows-Releases</span><span class="sxs-lookup"><span data-stu-id="4a4ce-118">Memory Limits for Windows Releases</span></span>](memory-limits-for-windows-releases.md)

## <a name="default-virtual-address-space-for-32-bit-windows"></a><span data-ttu-id="4a4ce-119">Standardmäßiger virtueller Adressraum für 32-Bit-Windows</span><span class="sxs-lookup"><span data-stu-id="4a4ce-119">Default Virtual Address Space for 32-bit Windows</span></span>

<span data-ttu-id="4a4ce-120">In der folgenden Tabelle wird der Standard Speicherbereich für jede Partition angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4a4ce-120">The following table shows the default memory range for each partition.</span></span>



| <span data-ttu-id="4a4ce-121">Speicherbereich</span><span class="sxs-lookup"><span data-stu-id="4a4ce-121">Memory range</span></span>                             | <span data-ttu-id="4a4ce-122">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="4a4ce-122">Usage</span></span>                |
|------------------------------------------|----------------------|
| <span data-ttu-id="4a4ce-123">Niedriges 2 GB (0x00000000 bis 0x7FFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="4a4ce-123">Low 2GB (0x00000000 through 0x7FFFFFFF)</span></span>  | <span data-ttu-id="4a4ce-124">Wird vom-Prozess verwendet.</span><span class="sxs-lookup"><span data-stu-id="4a4ce-124">Used by the process.</span></span> |
| <span data-ttu-id="4a4ce-125">High 2 GB (0x80000000 bis 0xffffffff)</span><span class="sxs-lookup"><span data-stu-id="4a4ce-125">High 2GB (0x80000000 through 0xFFFFFFFF)</span></span> | <span data-ttu-id="4a4ce-126">Wird vom System verwendet.</span><span class="sxs-lookup"><span data-stu-id="4a4ce-126">Used by the system.</span></span>  |



 

## <a name="virtual-address-space-for-32-bit-windows-with-4gt"></a><span data-ttu-id="4a4ce-127">Virtueller Adressraum für 32-Bit-Windows mit 4GT</span><span class="sxs-lookup"><span data-stu-id="4a4ce-127">Virtual Address Space for 32-bit Windows with 4GT</span></span>

<span data-ttu-id="4a4ce-128">Wenn die [4-Gigabyte-](4-gigabyte-tuning.md) Optimierung (4GT) aktiviert ist, lautet der Speicherbereich für jede Partition wie folgt.</span><span class="sxs-lookup"><span data-stu-id="4a4ce-128">If [4-gigabyte tuning](4-gigabyte-tuning.md) (4GT) is enabled, the memory range for each partition is as follows.</span></span>



| <span data-ttu-id="4a4ce-129">Speicherbereich</span><span class="sxs-lookup"><span data-stu-id="4a4ce-129">Memory range</span></span>                             | <span data-ttu-id="4a4ce-130">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="4a4ce-130">Usage</span></span>                |
|------------------------------------------|----------------------|
| <span data-ttu-id="4a4ce-131">Niedrig 3 GB (0x00000000 bis 0xBFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="4a4ce-131">Low 3GB (0x00000000 through 0xBFFFFFFF)</span></span>  | <span data-ttu-id="4a4ce-132">Wird vom-Prozess verwendet.</span><span class="sxs-lookup"><span data-stu-id="4a4ce-132">Used by the process.</span></span> |
| <span data-ttu-id="4a4ce-133">Hoch 1 GB (0xC0000000 bis 0xffffffff)</span><span class="sxs-lookup"><span data-stu-id="4a4ce-133">High 1GB (0xC0000000 through 0xFFFFFFFF)</span></span> | <span data-ttu-id="4a4ce-134">Wird vom System verwendet.</span><span class="sxs-lookup"><span data-stu-id="4a4ce-134">Used by the system.</span></span>  |



 

<span data-ttu-id="4a4ce-135">Nach der Aktivierung von 4GT hat ein Prozess, bei dem das Flag für die [**Image \_ Datei mit \_ großen \_ Adressen \_**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image) Werten in seinem Bild Header festgelegt wurde, Zugriff auf die zusätzlichen 1 GB Arbeitsspeicher über den unteren 2 GB.</span><span class="sxs-lookup"><span data-stu-id="4a4ce-135">After 4GT is enabled, a process that has the [**IMAGE\_FILE\_LARGE\_ADDRESS\_AWARE**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image) flag set in its image header will have access to the additional 1 GB of memory above the low 2 GB.</span></span>

## <a name="adjusting-the-virtual-address-space-for-32-bit-windows"></a><span data-ttu-id="4a4ce-136">Anpassen des virtuellen Adressraums für 32-Bit-Windows</span><span class="sxs-lookup"><span data-stu-id="4a4ce-136">Adjusting the Virtual Address Space for 32-bit Windows</span></span>

<span data-ttu-id="4a4ce-137">Sie können den folgenden Befehl verwenden, um eine Start Eintrags Option festzulegen, mit der die Größe der Partition konfiguriert wird, die für den Prozess zur Verfügung steht, um einen Wert zwischen 2048 (2 GB) und 3072 (3 GB) zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="4a4ce-137">You can use the following command to set a boot entry option that configures the size of the partition that is available for use by the process to a value between 2048 (2 GB) and 3072 (3 GB):</span></span>

<span data-ttu-id="4a4ce-138">[Bcdedit/set](/windows-hardware/drivers/devtest/bcdedit--set) **Erhöhung** von *Megabytes*</span><span class="sxs-lookup"><span data-stu-id="4a4ce-138">[BCDEdit /set](/windows-hardware/drivers/devtest/bcdedit--set) **increaseuserva** *Megabytes*</span></span>

<span data-ttu-id="4a4ce-139">Nachdem die Option Boot Entry festgelegt wurde, lautet der Arbeitsspeicher Bereich für jede Partition wie folgt.</span><span class="sxs-lookup"><span data-stu-id="4a4ce-139">After the boot entry option is set, the memory range for each partition is as follows.</span></span>



| <span data-ttu-id="4a4ce-140">Speicherbereich</span><span class="sxs-lookup"><span data-stu-id="4a4ce-140">Memory range</span></span>                            | <span data-ttu-id="4a4ce-141">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="4a4ce-141">Usage</span></span>                |
|-----------------------------------------|----------------------|
| <span data-ttu-id="4a4ce-142">Niedrig (0x00000000 bis *Megabyte*)</span><span class="sxs-lookup"><span data-stu-id="4a4ce-142">Low (0x00000000 through *Megabytes*)</span></span>    | <span data-ttu-id="4a4ce-143">Wird vom-Prozess verwendet.</span><span class="sxs-lookup"><span data-stu-id="4a4ce-143">Used by the process.</span></span> |
| <span data-ttu-id="4a4ce-144">Hoch (*Megabytes*+ 1 bis 0xffffffff)</span><span class="sxs-lookup"><span data-stu-id="4a4ce-144">High (*Megabytes*+1 through 0xFFFFFFFF)</span></span> | <span data-ttu-id="4a4ce-145">Wird vom System verwendet.</span><span class="sxs-lookup"><span data-stu-id="4a4ce-145">Used by the system.</span></span>  |



 

<span data-ttu-id="4a4ce-146">**Windows Server 2003:** Legen Sie den **Option/USERVA bei** -Schalter in boot.ini auf einen Wert zwischen 2048 und 3072 fest.</span><span class="sxs-lookup"><span data-stu-id="4a4ce-146">**Windows Server 2003:** Set the **/USERVA** switch in boot.ini to a value between 2048 and 3072.</span></span>

 

 
