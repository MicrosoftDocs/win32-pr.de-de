---
description: Der VM-Speicherplatz auf 32-Bit-Systemen kann aufgrund der Fragmentierung erschöpft werden. Mehrere Registrierungsschlüssel können verwendet werden, um Arbeitsspeicher Limits auf 32-Bit-Systemen zu konfigurieren, bei denen dieses Problem auftritt.
ms.assetid: ec2a8c6b-cd8e-4085-b337-02f78a210bb5
title: Registrierungsschlüssel für die Speicherverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48e8c53bd54f8caeb82aad58ceed61cc5644c112
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869064"
---
# <a name="memory-management-registry-keys"></a><span data-ttu-id="6a188-104">Registrierungsschlüssel für die Speicherverwaltung</span><span class="sxs-lookup"><span data-stu-id="6a188-104">Memory Management Registry Keys</span></span>

<span data-ttu-id="6a188-105">Der VM-Speicherplatz auf 32-Bit-Systemen kann aufgrund der Fragmentierung erschöpft werden.</span><span class="sxs-lookup"><span data-stu-id="6a188-105">System virtual address (VA) space on 32-bit systems can become exhausted due to fragmentation.</span></span> <span data-ttu-id="6a188-106">Mehrere Registrierungsschlüssel können verwendet werden, um Arbeitsspeicher Limits auf 32-Bit-Systemen zu konfigurieren, bei denen dieses Problem auftritt.</span><span class="sxs-lookup"><span data-stu-id="6a188-106">Several registry keys can be used to configure memory limits on 32-bit systems that experience this issue.</span></span> <span data-ttu-id="6a188-107">Der System-VA-Speicherplatz auf 64-Bit-Systemen unterliegt nicht der Erschöpfung durch Fragmentierung. Daher haben diese Schlüssel keine Auswirkung auf 64-Bit-Systeme.</span><span class="sxs-lookup"><span data-stu-id="6a188-107">System VA space on 64-bit systems is not subject to exhaustion by fragmentation; therefore, these keys have no effect on 64-bit systems.</span></span>

<span data-ttu-id="6a188-108">Bei 32-Bit-Systemen müssen diese Registrierungsschlüssel für die Speicherverwaltung explizit unter folgendem Registrierungsschlüssel erstellt werden:</span><span class="sxs-lookup"><span data-stu-id="6a188-108">For 32-bit systems, these memory management registry keys must be explicitly created under the following registry key:</span></span>

<span data-ttu-id="6a188-109">**HKEY \_ Lokales \_** \\ **System** \\ steuerungsedienstesteuerungsedienstesteuerungssteuerungs- \\  \\  \\ **Speicherverwaltung**</span><span class="sxs-lookup"><span data-stu-id="6a188-109">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**Current Control Set**\\**Control**\\**Session Manager**\\**Memory Management**</span></span>

<span data-ttu-id="6a188-110">**Windows Server 2008 und Windows Vista:** Diese Registrierungsschlüssel sind auf 32-Bit-Systemen ab Windows Server 2008 und Windows Vista mit Service Pack 1 (SP1) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6a188-110">**Windows Server 2008 and Windows Vista:** These registry keys are available on 32-bit systems starting with Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

<span data-ttu-id="6a188-111">Informationen zu den standardmäßigen Arbeitsspeicher-und Adressraum Limits für 32-Bit-und 64-Bit-Systeme finden Sie unter Arbeits [Speicher Grenzwerte für Windows-Versionen](memory-limits-for-windows-releases.md).</span><span class="sxs-lookup"><span data-stu-id="6a188-111">For default memory and address space limits on both 32-bit and 64-bit systems, see [Memory Limits for Windows Releases](memory-limits-for-windows-releases.md).</span></span>

<span data-ttu-id="6a188-112">In der folgenden Tabelle werden die Registrierungsschlüssel für die Speicherverwaltung beschrieben, die zum Konfigurieren von Arbeitsspeicher Limits auf 32-Bit-Systemen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="6a188-112">The following table describes the memory management registry keys that can be used to configure memory limits on 32-bit systems.</span></span> <span data-ttu-id="6a188-113">Alle diese Schlüssel verfügen über einen reg \_ DWORD-Typ und mögliche Werte, die zwischen 0 und 2.048 MB liegen.</span><span class="sxs-lookup"><span data-stu-id="6a188-113">All of these keys have a REG\_DWORD type and possible values that range from 0 through 2,048 MB.</span></span> <span data-ttu-id="6a188-114">Der Standardwert ist 0 (null). Dies bedeutet, dass keine Begrenzung erzwungen wird.</span><span class="sxs-lookup"><span data-stu-id="6a188-114">The default is 0, which means no limit is enforced.</span></span> <span data-ttu-id="6a188-115">Die Werte werden automatisch auf die nächste System-VA-Zuordnungs Grenze aufgerundet. diese ist 2 MB auf 32-Bit-Systemen, die über eine aktivierte [physische Adress Erweiterung](physical-address-extension.md) (PE) und 4 MB auf 32-Bit-Systemen verfügen, für die keine PE aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="6a188-115">Values are automatically rounded up to the next system VA allocation boundary, which is 2 MB on 32-bit systems that have [Physical Address Extension](physical-address-extension.md) (PAE) enabled and 4 MB on 32-bit systems that do not have PAE enabled.</span></span>



| <span data-ttu-id="6a188-116">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="6a188-116">Key</span></span>                   | <span data-ttu-id="6a188-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6a188-117">Description</span></span>                                                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a188-118">**Nonteipoollimit**</span><span class="sxs-lookup"><span data-stu-id="6a188-118">**NonPagedPoolLimit**</span></span> | <span data-ttu-id="6a188-119">Gibt die maximale Menge an System-VA-Speicherplatz an, die vom nicht auslagerenden Pool verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="6a188-119">Specifies the maximum amount of system VA space that can be used by the nonpaged pool.</span></span> <span data-ttu-id="6a188-120">Unter bestimmten Umständen wird dieser Grenzwert möglicherweise um einen kleinen Wert überschritten.</span><span class="sxs-lookup"><span data-stu-id="6a188-120">Under certain conditions, this limit may be exceeded by a small amount.</span></span> |
| <span data-ttu-id="6a188-121">**Paar-poollimit**</span><span class="sxs-lookup"><span data-stu-id="6a188-121">**PagedPoolLimit**</span></span>    | <span data-ttu-id="6a188-122">Gibt die maximale Menge an System-VA-Speicherplatz an, die vom Auslagerungs Pool verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="6a188-122">Specifies the maximum amount of system VA space that can be used by the paged pool.</span></span>                                                                            |
| <span data-ttu-id="6a188-123">**Sessionspacelimit**</span><span class="sxs-lookup"><span data-stu-id="6a188-123">**SessionSpaceLimit**</span></span> | <span data-ttu-id="6a188-124">Gibt die maximale Menge an System-VA-Speicherplatz an, die von Sitzungs Speicher Belegungen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="6a188-124">Specifies the maximum amount of system VA space that can be used by session space allocations.</span></span>                                                                 |
| <span data-ttu-id="6a188-125">**Systemcachelimit**</span><span class="sxs-lookup"><span data-stu-id="6a188-125">**SystemCacheLimit**</span></span>  | <span data-ttu-id="6a188-126">Gibt die maximale Menge an System-VA-Speicherplatz an, die vom System Cache verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="6a188-126">Specifies the maximum amount of system VA space that can be used by the system cache.</span></span> <span data-ttu-id="6a188-127">Unter bestimmten Umständen wird dieser Grenzwert möglicherweise um einen kleinen Wert überschritten.</span><span class="sxs-lookup"><span data-stu-id="6a188-127">Under certain conditions, this limit may be exceeded by a small amount.</span></span>  |
| <span data-ttu-id="6a188-128">**Systempteslimit**</span><span class="sxs-lookup"><span data-stu-id="6a188-128">**SystemPtesLimit**</span></span>   | <span data-ttu-id="6a188-129">Gibt die maximale Menge an System-VA-Speicherplatz an, der von e/a-Zuordnungen und anderen Ressourcen verwendet werden kann, die Seitentabellen Einträge (PTEs) für das System verwenden.</span><span class="sxs-lookup"><span data-stu-id="6a188-129">Specifies the maximum amount of system VA space that can be used by I/O mappings and other resources that consume system page table entries (PTEs).</span></span>            |



 

<span data-ttu-id="6a188-130">Wenn Sie bestimmen, ob der System-VA-Speicherplatz erschöpft ist, müssen Sie einen Kernel Debugger verwenden.</span><span class="sxs-lookup"><span data-stu-id="6a188-130">Determining whether system VA space is being exhausted requires the use of a kernel debugger.</span></span> <span data-ttu-id="6a188-131">Weitere Informationen finden Sie unter [Debugtools für Windows](https://msdn.microsoft.com/library/cc267445.aspx).</span><span class="sxs-lookup"><span data-stu-id="6a188-131">For more information, see [Debugging Tools for Windows](https://msdn.microsoft.com/library/cc267445.aspx).</span></span>

 

 



