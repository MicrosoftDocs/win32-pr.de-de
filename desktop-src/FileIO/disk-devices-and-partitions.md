---
description: Beschreibt eine Festplatte, Partitionierung und den Master Boot Record.
ms.assetid: daf45180-2cc3-433d-823e-395e85ce3410
title: Datenträger Geräte und Partitionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e063b943d33118a45cb6ab4c304569094af2c32e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553702"
---
# <a name="disk-devices-and-partitions"></a><span data-ttu-id="7adda-103">Datenträger Geräte und Partitionen</span><span class="sxs-lookup"><span data-stu-id="7adda-103">Disk Devices and Partitions</span></span>

<span data-ttu-id="7adda-104">Eine Festplatte besteht aus einem Satz von gestapelten platzern, von denen jede Daten in konzentrischen Kreisen oder nach *verfolgt*.</span><span class="sxs-lookup"><span data-stu-id="7adda-104">A hard disk consists of a set of stacked platters, each of which has data stored electromagnetically in concentric circles, or *tracks*.</span></span> <span data-ttu-id="7adda-105">Jede Platte verfügt über zwei Köpfe, eine auf jeder Seite der Platte, die Daten während des Datenträgers liest oder schreibt.</span><span class="sxs-lookup"><span data-stu-id="7adda-105">Each platter has two heads, one on each side of the platter, that reads or writes data as the disk spins.</span></span> <span data-ttu-id="7adda-106">Ein *Festplattenlaufwerk* steuert die Positionierung, das Lesen und Schreiben der Festplatte.</span><span class="sxs-lookup"><span data-stu-id="7adda-106">A *hard disk drive* controls the positioning, reading, and writing of the hard disk.</span></span> <span data-ttu-id="7adda-107">Beachten Sie, dass die Köpfe aller Scheiben als Einheit positioniert werden.</span><span class="sxs-lookup"><span data-stu-id="7adda-107">Note that the heads of all platters are positioned as a unit.</span></span>

<span data-ttu-id="7adda-108">Die kleinste adressierbare Einheit einer Spur ist ein *Sektor*.</span><span class="sxs-lookup"><span data-stu-id="7adda-108">The smallest addressable unit of a track is a *sector*.</span></span> <span data-ttu-id="7adda-109">Ein *Zylinder* ist als Satz von Spuren definiert, die an derselben Position auf jeder Platte angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="7adda-109">A *cylinder* is defined as the set of tracks that appear in the same location on each platter.</span></span> <span data-ttu-id="7adda-110">Im folgenden Diagramm wird z. b. eine Festplatte mit vier platzern angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7adda-110">For example, the following diagram shows a hard disk with four platters.</span></span> <span data-ttu-id="7adda-111">Zylinder x besteht aus acht Spuren (Nachverfolgung x von jeder Seite jeder Platte).</span><span class="sxs-lookup"><span data-stu-id="7adda-111">Cylinder X consists of eight tracks (track X from each side of each platter).</span></span>

![Festplatte, einschließlich Spuren, Sektoren und platzern](images/diskdevice.png)

<span data-ttu-id="7adda-113">Eine Festplatte kann eine oder mehrere logische Regionen enthalten, die als *Partitionen* bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="7adda-113">A hard disk can contain one or more logical regions called *partitions*.</span></span> <span data-ttu-id="7adda-114">Partitionen werden erstellt, wenn der Benutzer eine Festplatte als *Basis* Datenträger formatiert.</span><span class="sxs-lookup"><span data-stu-id="7adda-114">Partitions are created when the user formats a hard disk as a *basic disk*.</span></span> <span data-ttu-id="7adda-115">Windows unterstützt auch *dynamische* Datenträger, die in diesem Thema nicht erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="7adda-115">Windows also supports *dynamic disks*, which are not discussed in this topic.</span></span> <span data-ttu-id="7adda-116">Weitere Informationen zu Basis Datenträgern und dynamischen Datenträgern finden Sie unter [Basic und Dynamic Disks](basic-and-dynamic-disks.md).</span><span class="sxs-lookup"><span data-stu-id="7adda-116">For more information about basic disks and dynamic disks, see [Basic and Dynamic Disks](basic-and-dynamic-disks.md).</span></span>

<span data-ttu-id="7adda-117">Die Erstellung mehrerer Partitionen auf einem Datenträger ermöglicht das Aussehen von separaten Festplatten.</span><span class="sxs-lookup"><span data-stu-id="7adda-117">The creation of multiple partitions on a disk allows the appearance of having separate hard drives.</span></span> <span data-ttu-id="7adda-118">Beispielsweise enthält ein System mit einer Festplatte, die über eine Partition verfügt, ein einzelnes Volume, das vom System als Laufwerk C festgelegt wird. Ein System mit einer Festplatte mit zwei Partitionen enthält normalerweise die Laufwerke C und D. Wenn mehrere Partitionen auf einer Festplatte vorhanden sind, kann es einfacher sein, das System zu verwalten, z. b. zum Organisieren von Dateien oder zur Unterstützung mehrerer Benutzer.</span><span class="sxs-lookup"><span data-stu-id="7adda-118">For example, a system with one hard disk that has one partition contains a single volume, designated by the system as drive C. A system with a hard disk with two partitions typically contains drives C and D. Having multiple partitions on a hard disk can make it easier to manage the system, for example to organize files or to support multiple users.</span></span>

<span data-ttu-id="7adda-119">Der erste physische Sektor auf einem Basis Datenträger enthält eine Datenstruktur, die als Master Boot Record (MBR) bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="7adda-119">The first physical sector on a basic disk contains a data structure known as the Master Boot Record (MBR).</span></span> <span data-ttu-id="7adda-120">Der MBR enthält Folgendes:</span><span class="sxs-lookup"><span data-stu-id="7adda-120">The MBR contains the following:</span></span>

-   <span data-ttu-id="7adda-121">Ein Start Programm (bis zu 442 Bytes groß)</span><span class="sxs-lookup"><span data-stu-id="7adda-121">A boot program (up to 442 bytes in size)</span></span>
-   <span data-ttu-id="7adda-122">Eine Datenträger Signatur (eine eindeutige 4-Byte-Zahl)</span><span class="sxs-lookup"><span data-stu-id="7adda-122">A disk signature (a unique 4-byte number)</span></span>
-   <span data-ttu-id="7adda-123">Eine Partitionstabelle (bis zu vier Einträge)</span><span class="sxs-lookup"><span data-stu-id="7adda-123">A partition table (up to four entries)</span></span>
-   <span data-ttu-id="7adda-124">Ein End-of-MBR-Marker (immer 0x55aa)</span><span class="sxs-lookup"><span data-stu-id="7adda-124">An end-of-MBR marker (always 0x55AA)</span></span>

## <a name="related-topics"></a><span data-ttu-id="7adda-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7adda-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7adda-126">Informationen zur Volumeverwaltung</span><span class="sxs-lookup"><span data-stu-id="7adda-126">About Volume Management</span></span>](about-volume-management.md)
</dt> <dt>

[<span data-ttu-id="7adda-127">Basis-und dynamische Datenträger</span><span class="sxs-lookup"><span data-stu-id="7adda-127">Basic and Dynamic Disks</span></span>](basic-and-dynamic-disks.md)
</dt> </dl>

 

 



