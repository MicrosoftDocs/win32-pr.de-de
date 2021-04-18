---
title: Mit der neuen API können Apps "Trim-und unmap"-Hinweise an Speichermedien senden.
description: Neue API ermöglicht apps das Senden von \ 0034; Trim und unmap \ 0034; Hinweise zu Speichermedien
ms.assetid: DDBC3592-BD4D-4826-83FE-387564DA07E8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e043c1188bda790b4ed151e8a79e1f7b4c6f0f9
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "106340537"
---
# <a name="new-api-allows-apps-to-send-trim-and-unmap-hints-to-storage-media"></a><span data-ttu-id="e87be-103">Mit der neuen API können Apps "Trim-und unmap"-Hinweise an Speichermedien senden.</span><span class="sxs-lookup"><span data-stu-id="e87be-103">New API allows apps to send "TRIM and Unmap" hints to storage media</span></span>

## <a name="platforms"></a><span data-ttu-id="e87be-104">Plattformen</span><span class="sxs-lookup"><span data-stu-id="e87be-104">Platforms</span></span>

<span data-ttu-id="e87be-105">**Clients** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="e87be-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="e87be-106">**Server** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e87be-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="e87be-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e87be-107">Description</span></span>

<span data-ttu-id="e87be-108">Mithilfe von Trim-hinweisen wird das Laufwerk benachrichtigt, dass bestimmte zuvor zugewiesene Sektoren von der APP nicht mehr benötigt werden und gelöscht werden können.</span><span class="sxs-lookup"><span data-stu-id="e87be-108">TRIM hints notify the drive that certain sectors that previously were allocated are no longer needed by the app and can be purged.</span></span> <span data-ttu-id="e87be-109">Dies wird in der Regel verwendet, wenn eine APP große Speicher Belegungen über eine Datei zuweist und die Zuordnungen für die Datei dann selbst verwaltet (z. b. virtuelle Festplatten Dateien).</span><span class="sxs-lookup"><span data-stu-id="e87be-109">This is typically used when an app makes large space allocations via a file and then self-manages the allocations to the file (for example, Virtual Hard Disk files).</span></span>

<span data-ttu-id="e87be-110">**Was ist Trim?**</span><span class="sxs-lookup"><span data-stu-id="e87be-110">**What is TRIM?**</span></span>

<span data-ttu-id="e87be-111">Solid-State-Laufwerke (SSDs) sind in der Regel Flash speicherbasierte Geräte mit Block Löschung. Dies bedeutet, dass beim Schreiben von Daten in den SSD-Daten nicht an Ort und Stelle geschrieben werden dürfen und an einem anderen Ort geschrieben werden müssen, bis der Block in die Garbage Collection aufgenommen werden kann.</span><span class="sxs-lookup"><span data-stu-id="e87be-111">Solid state drives (SSDs) are typically flash memory based block-erased devices; this means that when data is written to the SSD, it cannot be over-written in place and must be written elsewhere until the block can be garbage collected.</span></span> <span data-ttu-id="e87be-112">Da das SSD über keinen internen Mechanismus verfügt, um zu bestimmen, ob bestimmte Blöcke entfernt werden und andere benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="e87be-112">Since the SSD has no internal mechanism for determining that certain blocks are removed and others are needed.</span></span> <span data-ttu-id="e87be-113">Der SSD kann die einzige Zeit markieren, die der Bereich "Dirty" ist, wenn er überschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="e87be-113">The only time the SSD can mark a sector ‘dirty’ is when it is over-written.</span></span> <span data-ttu-id="e87be-114">In anderen Fällen, z. b. Wenn eine Datei gelöscht wird, behält der SSD diese Sektoren bei, da der Löschvorgang nur als MFT-Änderung (Master File Table) ausgeführt wird und nicht als Vorgang für alle Bereiche der Datei.</span><span class="sxs-lookup"><span data-stu-id="e87be-114">In other cases, such as when a file is deleted, the SSD retains these sectors because the deletion is performed as a master file table (MFT) change only, and not as an operation to all the sectors of the file.</span></span> <span data-ttu-id="e87be-115">In Windows 7 haben wir eine Standardmethode für die Kommunikation mit SSDs zu Sektoren eingeführt, die nicht mehr benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="e87be-115">In Windows 7, we introduced a standard way of communicating with SSDs about sectors that are not needed any more.</span></span> <span data-ttu-id="e87be-116">Dieser Befehl ist in der [T13-Spezifikation](https://www.t13.org/Standards/Default.aspx?DocumentType=3) als Befehl zum kürzen definiert. NTFS sendet den Befehl Trim für einige normale Inline Vorgänge, z. b. "DeleteFile".</span><span class="sxs-lookup"><span data-stu-id="e87be-116">This command is defined in the [T13 specification](https://www.t13.org/Standards/Default.aspx?DocumentType=3) as the TRIM command; NTFS sends the TRIM command for some normal inline operations such as “deletefile.”</span></span>

<span data-ttu-id="e87be-117">**Andere Verwendungsmöglichkeiten von Trim in der Speicher Welt**</span><span class="sxs-lookup"><span data-stu-id="e87be-117">**Other uses of TRIM in the storage world**</span></span>

<span data-ttu-id="e87be-118">Wie SSDs, Storage Area Networks (SANs) und die neuen Implementierungen von Software Spaces für Windows 8-Features verwenden Trim-Befehls Hinweise zum Verwalten Ihrer Leerzeichen in schlank bereitgestellten Umgebungen.</span><span class="sxs-lookup"><span data-stu-id="e87be-118">Like SSDs, storage area networks (SANs) and the new Windows 8 feature Software Spaces implementations consume TRIM command hints to manage their spaces in thinly provisioned environments.</span></span> <span data-ttu-id="e87be-119">Sans und Software Plätze weisen Speicherbereiche zu, die größer sind als Sektoren oder Cluster (von 1 MB bis 1 GB).</span><span class="sxs-lookup"><span data-stu-id="e87be-119">SANs and Software Spaces allocate regions of storage in sizes that are greater than sectors or clusters (anywhere from 1MB to 1GB).</span></span> <span data-ttu-id="e87be-120">Wenn Sie für Ihre Zuordnungs Größe (oder höher als die Zuordnungs Größe) Trim-Hinweise erhalten, kann das San/SSD einen Bereich aufheben, um den Speicherplatz für andere Dateien freizugeben.</span><span class="sxs-lookup"><span data-stu-id="e87be-120">When they receive TRIM hints for its allocation size (or greater than the allocation size), the SAN/SSD can de-allocate a region to free up the space for other files.</span></span> <span data-ttu-id="e87be-121">Sie durchlaufen in der Regel alle Trim-Hinweise an das zugrunde liegende Medium (SSD oder HDD), damit Sie den freigegebenen Speicherplatz entsprechend verbrauchen können.</span><span class="sxs-lookup"><span data-stu-id="e87be-121">They typically pass through all TRIM hints to the underlying media (SSD or HDD) so that they can consume the freed up space as appropriate.</span></span> <span data-ttu-id="e87be-122">In der Regel verschieben Sie Daten nicht, um die Zuordnung von Regionen aufzuheben, und Sie verfolgen auch keine Trim-Bereiche nach den zugewiesenen Regionen (wenn die Region leer ist).</span><span class="sxs-lookup"><span data-stu-id="e87be-122">They do not typically move data around to de-allocate regions, nor do they keep track of TRIM areas to de-allocated regions (when the region is empty).</span></span>

<span data-ttu-id="e87be-123">Schlank zugewiesene Sans verwenden die an Sie weiter gegebenen Trim-Hinweise, um den gesamten physischen Speicherbedarf zu verringern und so die Kosten zu senken.</span><span class="sxs-lookup"><span data-stu-id="e87be-123">Thinly provisioned SANs use the TRIM hints that are passed to them to help reduce the overall physical storage footprint, hence reducing cost.</span></span> <span data-ttu-id="e87be-124">Die [T10-SCSI-Spezifikation](https://www.t10.org) definiert den Befehl "unmap" (ähnlich wie der Trim-Befehl). Hier gilt der Befehl für alle Arten von Speicher, einschließlich HDDs, SSDs und anderen.</span><span class="sxs-lookup"><span data-stu-id="e87be-124">The [T10 SCSI specification](https://www.t10.org) defines the ‘Unmap’ command (similar to the TRIM command); here the command is applicable to all kinds of storage including HDDs, SSDs, and others.</span></span> <span data-ttu-id="e87be-125">Der unmap-Befehl hilft beim Entfernen physischer Blöcke aus der San-Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="e87be-125">The UnMap command helps to remove physical blocks from the SAN’s allocation.</span></span>

## <a name="how-to-use-the-new-api"></a><span data-ttu-id="e87be-126">Verwenden der neuen API</span><span class="sxs-lookup"><span data-stu-id="e87be-126">How to use the new API</span></span>


```
#define FSCTL_FILE_LEVEL_TRIM CTL_CODE(FILE_DEVICE_FILE_SYSTEM, 130, METHOD_BUFFERED, FILE_WRITE_DATA)

Where 
typedef struct _EXTENT_PAIR {
    ULONGLONG Offset;
    ULONGLONG Length;
} EXTENT_PAIR, *PEXTENT_PAIR;

typedef struct _FILE_LEVEL_TRIM {
    //
    // A count of how many Offset:Length pairs are given
    //
    DWORD PairCount;
    //
    // All the pairs.
    //
    EXTENT_PAIR Pairs[1];
} FILE_LEVEL_TRIM, *PFILE_LEVEL_TRIM;
```



<span data-ttu-id="e87be-127">Die Datei Trim wird über den Puffer, wenn möglich, oder asynchron (nicht gepuffert) an das Gerät ioctl DSM Command Trim übermittelt.</span><span class="sxs-lookup"><span data-stu-id="e87be-127">File TRIM is passed via the buffer if possible or asynchronously (non-buffered) to the Device IOCTL DSM command TRIM.</span></span> <span data-ttu-id="e87be-128">Dies wird dem Befehl Trim für ATA-Geräte zugeordnet und der Befehl zum Aufheben der Zuordnung für SCSI-Geräte.</span><span class="sxs-lookup"><span data-stu-id="e87be-128">This is mapped to the TRIM command for ATA devices and UnMap command for SCSI devices.</span></span> <span data-ttu-id="e87be-129">Der Code zum Kürzen von Dateien sendet die Regionen nacheinander, wie in den oben aufgeführten Blöcken angegeben.</span><span class="sxs-lookup"><span data-stu-id="e87be-129">The file TRIM code sends the regions one-by-one as specified by the extents above.</span></span>

<span data-ttu-id="e87be-130">File Trim wartet nicht auf Rückgabe vom Gerät, da die Befehle Trim und unmap als Hinweise zu den zugrunde liegenden Speichermedien definiert sind und Rückgabecodes nicht erwartet werden.</span><span class="sxs-lookup"><span data-stu-id="e87be-130">File TRIM does not wait for returns from the device, because the TRIM and Unmap commands are defined as hints to the underlying storage media and return codes are not expected.</span></span>

<span data-ttu-id="e87be-131">**End-to-End-Workflow:**</span><span class="sxs-lookup"><span data-stu-id="e87be-131">**End-to-end workflow:**</span></span>

1.  <span data-ttu-id="e87be-132">Datei Trim abrufen</span><span class="sxs-lookup"><span data-stu-id="e87be-132">Call File Trim</span></span>
    1.  <span data-ttu-id="e87be-133">Datei Trim untersucht Eingaben für Fehler</span><span class="sxs-lookup"><span data-stu-id="e87be-133">File TRIM examines inputs for errors</span></span>
    2.  <span data-ttu-id="e87be-134">Durch Datei Trim werden die Blöcke in LCN-Regionen aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="e87be-134">File TRIM breaks up the extents into LCN regions</span></span>
    3.  <span data-ttu-id="e87be-135">Die Datei Trim wird für falsch ausgerichtete Bereiche, die an Trim übermittelt werden, auf-und heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="e87be-135">File TRIM rounds up and down for mis-aligned regions that are passed into TRIM</span></span>
    4.  <span data-ttu-id="e87be-136">Durch Datei Trim werden Einträge im Cache gelöscht, die sich auf die Trim-Bereiche beziehen.</span><span class="sxs-lookup"><span data-stu-id="e87be-136">File TRIM purges entries in the cache that relate to the TRIM areas</span></span>
    5.  <span data-ttu-id="e87be-137">Die Datei Trim übergibt IOCTL \_ DSM (Trim) pro Region.</span><span class="sxs-lookup"><span data-stu-id="e87be-137">File TRIM passes IOCTL\_DSM (Trim) per region</span></span>
2.  <span data-ttu-id="e87be-138">Datei-Trim-Rückgabe oder-Fehler</span><span class="sxs-lookup"><span data-stu-id="e87be-138">File TRIM returns or errors</span></span>
    1.  <span data-ttu-id="e87be-139">Die Fehlerüberprüfung erfolgt bei der Eingabe Gültigkeit.</span><span class="sxs-lookup"><span data-stu-id="e87be-139">Error checking is done on input validity</span></span>
    2.  <span data-ttu-id="e87be-140">Wenn nur einige der Blöcke gültig sind, wird ein Fehler für den gesamten API-Befehl zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e87be-140">If only some of the extents are valid, one error is returned for the complete API call</span></span>

<span data-ttu-id="e87be-141">**Anwendungsfälle**</span><span class="sxs-lookup"><span data-stu-id="e87be-141">**Use cases**</span></span>

<span data-ttu-id="e87be-142">**Virtuelle Festplatte (Virtual Hard Disk, VHD) auf einem SSD-Laufwerk:**</span><span class="sxs-lookup"><span data-stu-id="e87be-142">**Consumer virtual hard disk (VHD) mounted on an SSD:**</span></span>

<span data-ttu-id="e87be-143">Die virtuelle Festplatte wird anfänglich auf "sauberen", nicht verwendeten Medien bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="e87be-143">The VHD is initially mounted on ‘clean’ unused media.</span></span> <span data-ttu-id="e87be-144">Bei Verwendung der VHD verwendet die VHD Teile der Speichermedien für Dateien usw. Wenn Dateien auf dem Speichermedium gelöscht werden, werden diese Dateien nicht aus der SSD entfernt, da die komplette VHD als eine Datei auf dem SSD gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="e87be-144">As the VHD is used, the VHD consumes parts of the storage media for files, etc. When it deletes files in the storage media, these files are not removed from the SSD since the complete VHD is stored as one file on the SSD.</span></span> <span data-ttu-id="e87be-145">In der Hyper-V-Umgebung wird die Datei Kürzung für alle Regionen aufgerufen, die gelöscht werden, wenn "Delete-File" in der VHD-Umgebung auftritt.</span><span class="sxs-lookup"><span data-stu-id="e87be-145">The Hyper-V environment calls File TRIM for all regions that are deleted when delete-file occurs in the VHD environment.</span></span> <span data-ttu-id="e87be-146">Die Datei-Metriken \_ werden in den SSD übersetzt, damit die SSD-Leistung optimiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="e87be-146">The File\_TRIMs are translated to the SSD so that the SSD performance can be optimized.</span></span>

<span data-ttu-id="e87be-147">**In einem dünn bereitgestellten San eingebundene consumervhd:**</span><span class="sxs-lookup"><span data-stu-id="e87be-147">**Consumer VHD mounted on a thinly provisioned SAN:**</span></span>

<span data-ttu-id="e87be-148">Die virtuelle Festplatte wird anfänglich auf einer minimalen Festplatte einer dünn bereitgestellten Umgebung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="e87be-148">The VHD is initially mounted on one minimum slab of a thinly provisioned environment.</span></span> <span data-ttu-id="e87be-149">Wenn Dateien auf der virtuellen Festplatte gespeichert werden, wächst der Speicherbedarf der virtuellen Festplatte in Vielfachen von Platten.</span><span class="sxs-lookup"><span data-stu-id="e87be-149">As files are stored in the VHD, the storage footprint of the VHD grows in multiples of slabs.</span></span> <span data-ttu-id="e87be-150">Wenn Dateien in der virtuellen Festplatte entfernt werden, ruft die Hyper-V-Datei in \_ das zugrunde liegende, schlank bereitgestellte San auf.</span><span class="sxs-lookup"><span data-stu-id="e87be-150">When files are removed in the VHD, the Hyper-V calls File\_TRIM to the underlying thinly provisioned SAN.</span></span> <span data-ttu-id="e87be-151">Wenn die Festplatten größer sind als die Granularität der Platte, kann das San nun eine Platte entfernen und somit den Speicherbedarf der VHD auf diesem San verringern.</span><span class="sxs-lookup"><span data-stu-id="e87be-151">If the TRIMs are bigger than the SLAB granularity, the SAN can now remove a SLAB and hence reduce the footprint of the VHD on that SAN.</span></span>

<span data-ttu-id="e87be-152">Wenn sich die virtuelle Festplatte auf einem Windows 8-basierten Server befindet, sendet der Speicher Optimierer auch die drei-MS-Werte, um den Festplatten Speicherplatz der virtuellen Festplatte innerhalb der bereitgestellten VHD zu verringern.</span><span class="sxs-lookup"><span data-stu-id="e87be-152">If the VHD is resident on a Windows 8 based server, the Storage Optimizer will also send TRIMs to reduce the slab footprint of the VHD from within the mounted VHD.</span></span>

## <a name="tests"></a><span data-ttu-id="e87be-153">Tests</span><span class="sxs-lookup"><span data-stu-id="e87be-153">Tests</span></span>

<span data-ttu-id="e87be-154">In früheren Betriebssystemversionen gibt es keine vergleichbaren APIs.</span><span class="sxs-lookup"><span data-stu-id="e87be-154">There are no comparable APIs in earlier operating system releases.</span></span> <span data-ttu-id="e87be-155">Die tatsächliche API selbst sollte keine Auswirkung auf die Leistung haben, obwohl das Speichermedium (wenn es korrekt implementiert ist) eine bessere Schreibleistung darstellen kann.</span><span class="sxs-lookup"><span data-stu-id="e87be-155">There should be no performance impact from the actual API itself, though the storage media (if implemented correctly) can show better write performance.</span></span> <span data-ttu-id="e87be-156">Die API sollte sehr sorgfältig verwendet werden. nur Blöcke, die nicht mehr benötigt werden, sollten nach unten weitergegeben werden, da diese Blöcke permanent aus den Speichermedien entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="e87be-156">The API should be used very carefully; only extents that are no longer needed should be passed down as those extents will be permanently removed from the storage media.</span></span>

## <a name="resources"></a><span data-ttu-id="e87be-157">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e87be-157">Resources</span></span>

-   [<span data-ttu-id="e87be-158">T13-Spezifikation</span><span class="sxs-lookup"><span data-stu-id="e87be-158">T13 specification</span></span>](http://www.t13.org/Standards/Default.aspx?DocumentType=3)
-   [<span data-ttu-id="e87be-159">T10-SCSI-Spezifikation</span><span class="sxs-lookup"><span data-stu-id="e87be-159">T10 SCSI specification</span></span>](https://www.t10.org/)

 

 




