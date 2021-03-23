---
title: Übersicht über deskriptortabellen
description: 'Jede Deskriptortabelle speichert Deskriptoren von einem oder mehreren Typen: Srvs, uave, cbvs und Samplers. Eine Deskriptortabelle ist keine Speicher Belegung. Es handelt sich einfach um einen Offset und eine Länge in einem deskriptorheap.'
ms.assetid: 4A5749CE-DD84-40E1-B67F-31828165A631
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d446a0570cf813eacaa4d036781e8cd4b8def3c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74105151"
---
# <a name="descriptor-tables-overview"></a><span data-ttu-id="f1e54-104">Übersicht über deskriptortabellen</span><span class="sxs-lookup"><span data-stu-id="f1e54-104">Descriptor Tables Overview</span></span>

<span data-ttu-id="f1e54-105">Jede Deskriptortabelle speichert Deskriptoren von einem oder mehreren Typen: Srvs, uave, cbvs und Samplers.</span><span class="sxs-lookup"><span data-stu-id="f1e54-105">Each descriptor table stores descriptors of one or more types - SRVs, UAVe, CBVs, and Samplers.</span></span> <span data-ttu-id="f1e54-106">Eine Deskriptortabelle ist keine Speicher Belegung. Es handelt sich einfach um einen Offset und eine Länge in einem deskriptorheap.</span><span class="sxs-lookup"><span data-stu-id="f1e54-106">A descriptor table is not an allocation of memory; it is simply an offset and length into a descriptor heap.</span></span>

-   [<span data-ttu-id="f1e54-107">Verweisen auf deskriptortabellen</span><span class="sxs-lookup"><span data-stu-id="f1e54-107">Referencing descriptor tables</span></span>](#referencing-descriptor-tables)
-   [<span data-ttu-id="f1e54-108">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="f1e54-108">Related topics</span></span>](#related-topics)

## <a name="referencing-descriptor-tables"></a><span data-ttu-id="f1e54-109">Verweisen auf deskriptortabellen</span><span class="sxs-lookup"><span data-stu-id="f1e54-109">Referencing descriptor tables</span></span>

<span data-ttu-id="f1e54-110">Die Grafik Pipeline durch die Stamm Signatur erhält Zugriff auf Ressourcen, indem Sie über den Index auf deskriptortabellen verweist.</span><span class="sxs-lookup"><span data-stu-id="f1e54-110">The graphics pipeline, through the root signature, gain access to resources by referencing into descriptor tables by index.</span></span>

<span data-ttu-id="f1e54-111">Eine Deskriptortabelle ist tatsächlich nur ein Unterbereich eines deskriptorheaps.</span><span class="sxs-lookup"><span data-stu-id="f1e54-111">A descriptor table is actually just a sub-range of a descriptor heap.</span></span> <span data-ttu-id="f1e54-112">Deskriptorheaps stellen die zugrunde liegende Speicher Belegung für eine Auflistung von Deskriptoren dar.</span><span class="sxs-lookup"><span data-stu-id="f1e54-112">Descriptor heaps represent the underlying memory allocation for a collection of descriptors.</span></span> <span data-ttu-id="f1e54-113">Da die Speicher Belegung eine Eigenschaft eines-Objekts ist, das einen deskriptorheap erstellt, ist die Definition einer Deskriptortabelle aus einer Tabelle garantiert so kostengünstig wie die Identifizierung eines Bereichs im Heap für die Hardware.</span><span class="sxs-lookup"><span data-stu-id="f1e54-113">Since memory allocation is a property of a creating a descriptor heap, defining a descriptor table out of one is guaranteed to be as cheap as identifying a region in the heap to the hardware.</span></span> <span data-ttu-id="f1e54-114">Deskriptortabellen müssen nicht auf API-Ebene erstellt oder zerstört werden – Sie werden nur für Treiber als Offset und Größe aus einem Heap identifiziert, wenn auf Sie verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="f1e54-114">Descriptor tables don’t need to be created or destroyed at the API level– they are merely identified to drivers as an offset and size out of a heap whenever referenced.</span></span>

<span data-ttu-id="f1e54-115">Es ist durchaus möglich, dass eine APP sehr große deskriptortabellen definiert, wenn deren Shader eine Vielzahl von verfügbaren Deskriptoren (häufig auf Texturen verweisen) im laufenden Betrieb (möglicherweise durch Materialdaten) auswählen möchten.</span><span class="sxs-lookup"><span data-stu-id="f1e54-115">It is certainly possible for an app to define very large descriptor tables when its shaders want the freedom to select from a vast set of available descriptors (often referencing textures) on the fly (perhaps driven by material data).</span></span>

<span data-ttu-id="f1e54-116">Die Stamm Signatur verweist auf den deskriptortabelleneintrag mit einem Verweis auf den Heap, die Startposition der Tabelle (ein Offset vom Beginn des Heaps) und die Länge (in Einträgen) der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="f1e54-116">The Root Signature references the descriptor table entry with a reference to the heap, the start location of the table (an offset from the start of the heap), and the length (in entries) of the table.</span></span> <span data-ttu-id="f1e54-117">Die folgende Abbildung zeigt die folgenden Konzepte: die deskriptortabellenzeiger aus der Stamm Signatur und die Deskriptoren im deskriptorheap, die auf die vollständige Textur oder die Puffer Daten in einem uploadheap verweisen.</span><span class="sxs-lookup"><span data-stu-id="f1e54-117">The image below shows these concepts: the descriptor table pointers from the Root Signature and the descriptors within the descriptor heap referencing the full texture or buffer data in an upload heap.</span></span>

![deskriptortabellen](images/descriptor-table.png)

## <a name="related-topics"></a><span data-ttu-id="f1e54-119">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="f1e54-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1e54-120">Deskriptortabellen</span><span class="sxs-lookup"><span data-stu-id="f1e54-120">Descriptor Tables</span></span>](descriptor-tables.md)
</dt> </dl>

 

 




