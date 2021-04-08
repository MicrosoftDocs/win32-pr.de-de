---
title: Informationen über strukturierte Speicherung
description: Herkömmliche Dateisysteme stoßen auf Herausforderungen, wenn Sie versuchen, in einem Dokument effizient mehrere Arten von Objekten zu speichern.
ms.assetid: a571f7c2-0490-463c-813e-de4a9fd12a2d
keywords:
- Informationen über strukturierte Speicherung
- Strukturierte Speicherung, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d048907c196c871af943e5a15cc95b367724a31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709078"
---
# <a name="about-structured-storage"></a><span data-ttu-id="28d80-105">Informationen über strukturierte Speicherung</span><span class="sxs-lookup"><span data-stu-id="28d80-105">About Structured Storage</span></span>

<span data-ttu-id="28d80-106">Herkömmliche Dateisysteme stoßen auf Herausforderungen, wenn Sie versuchen, in einem Dokument effizient mehrere Arten von Objekten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="28d80-106">Traditional file systems encounter challenges when they attempt to store efficiently multiple kinds of objects in one document.</span></span> <span data-ttu-id="28d80-107">COM bietet eine Lösung: ein Dateisystem in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="28d80-107">COM provides a solution: a file system within a file.</span></span> <span data-ttu-id="28d80-108">Der strukturierte com-Speicher definiert, wie eine einzelne Datei Entität als strukturierte Auflistung von zwei Typen von Objekten behandelt wird – Storages und Streams –, die wie Verzeichnisse und Dateien funktionieren.</span><span class="sxs-lookup"><span data-stu-id="28d80-108">COM structured storage defines how to treat a single file entity as a structured collection of two types of objects—storages and streams—that perform like directories and files.</span></span> <span data-ttu-id="28d80-109">Dieses Schema wird als *strukturierter Speicher* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="28d80-109">This scheme is called *structured storage*.</span></span> <span data-ttu-id="28d80-110">Der Zweck der strukturierten Speicherung besteht darin, die Leistungseinbußen und den Aufwand für das Speichern von separaten Objekten in einer Flatfile zu verringern.</span><span class="sxs-lookup"><span data-stu-id="28d80-110">The purpose of structured storage is to reduce the performance penalties and overhead associated with storing separate objects in a flat file.</span></span>

<span data-ttu-id="28d80-111">Dieser Abschnitt enthält eine Übersicht über die Vorteile und Grundlagen der strukturierten Speicherung, die Eigenschaften Sätze und die asynchrone strukturierte Speicherung sowie eine historische Betrachtung der Dateisysteme:</span><span class="sxs-lookup"><span data-stu-id="28d80-111">This section contains an overview of structured storage benefits and fundamentals, property sets and asynchronous structured storage as well as a historical look at file systems:</span></span>

-   <span data-ttu-id="28d80-112">Implementierung der Verbund Datei</span><span class="sxs-lookup"><span data-stu-id="28d80-112">Compound file implementation</span></span>
-   <span data-ttu-id="28d80-113">NTFS-Dateisystem Implementierung</span><span class="sxs-lookup"><span data-stu-id="28d80-113">NTFS file system implementation</span></span>
-   <span data-ttu-id="28d80-114">Eigenständige Implementierung</span><span class="sxs-lookup"><span data-stu-id="28d80-114">Stand-alone implementation</span></span>

<span data-ttu-id="28d80-115">Dieser Abschnitt enthält Links zur [Entwicklung von Dateisystemen](the-evolution-of-file-systems.md), [Storages und Streams](storages-and-streams.md), [Verbund Dateien](compound-files.md), [Grundlagen strukturierter Speicherung](structured-storage-fundamentals.md)und [strukturierten Speicher Beispielen](using-structured-storage.md).</span><span class="sxs-lookup"><span data-stu-id="28d80-115">This section includes links to [The Evolution of File Systems](the-evolution-of-file-systems.md), [Storages and Streams](storages-and-streams.md), [Compound Files](compound-files.md), [Structured Storage Fundamentals](structured-storage-fundamentals.md), and [Structured Storage Samples](using-structured-storage.md).</span></span>

 

 




