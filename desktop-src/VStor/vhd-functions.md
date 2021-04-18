---
description: 'Weitere Informationen finden Sie hier: <span id=vhd.vhd_functions></span> Virtual Disk Functions'
MS-HAID: vhd.vhd\_functions
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Virtual Disk-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f31af2b24a55baa3c64bfe5bd9e09e0b9e2f59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345728"
---
# <a name="span-idvhdvhd_functionsspanvirtual-disk-functions"></a><span data-ttu-id="50ac1-103"><span id="vhd.vhd_functions"></span>Virtual Disk-Funktionen</span><span class="sxs-lookup"><span data-stu-id="50ac1-103"><span id="vhd.vhd_functions"></span>Virtual Disk Functions</span></span>

<span data-ttu-id="50ac1-104">Die folgenden Funktionen werden in virtuellen Datenträgern verwendet:</span><span class="sxs-lookup"><span data-stu-id="50ac1-104">The following functions are used in Virtual Disks:</span></span>

## <a name="span-idin_this_sectionspanin-this-section"></a><span data-ttu-id="50ac1-105"><span id="in_this_section"></span>In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="50ac1-105"><span id="in_this_section"></span>In this section</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="50ac1-106">Thema</span><span class="sxs-lookup"><span data-stu-id="50ac1-106">Topic</span></span></th>
<th><span data-ttu-id="50ac1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="50ac1-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="50ac1-108"><a href="/windows/win32/api/virtdisk/nf-virtdisk-applysnapshotvhdset"><strong>Applysnapshotvhdset</strong></a></span><span class="sxs-lookup"><span data-stu-id="50ac1-108"><a href="/windows/win32/api/virtdisk/nf-virtdisk-applysnapshotvhdset"><strong>ApplySnapshotVhdSet</strong></a></span></span></p></td>
<td><p><span data-ttu-id="50ac1-109">Wendet eine Momentaufnahme des aktuellen virtuellen Datenträgers für VHD-Set-Dateien an.</span><span class="sxs-lookup"><span data-stu-id="50ac1-109">Applies a snapshot of the current virtual disk for VHD Set files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50ac1-110"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-addvirtualdiskparent"><strong>Addvirtualdiskparent</strong></a></span><span class="sxs-lookup"><span data-stu-id="50ac1-110"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-addvirtualdiskparent"><strong>AddVirtualDiskParent</strong></a></span></span></p></td>
<td><p><span data-ttu-id="50ac1-111">Fügt einem virtuellen Datenträger, der mit dem <strong>OPEN_VIRTUAL_DISK_FLAG_CUSTOM_DIFF_CHAIN</strong> -Flag geöffnet wurde, ein übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="50ac1-111">Attaches a parent to a virtual disk opened with the <strong>OPEN_VIRTUAL_DISK_FLAG_CUSTOM_DIFF_CHAIN</strong> flag.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50ac1-112"><a href="/windows/win32/api/virtdisk/nf-virtdisk-attachvirtualdisk"><strong>Attachvirtualdisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="50ac1-112"><a href="/windows/win32/api/virtdisk/nf-virtdisk-attachvirtualdisk"><strong>AttachVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="50ac1-113">Fügt eine virtuelle Festplatte (VHD) oder eine CD-oder DVD-Abbild Datei (ISO) an, indem ein geeigneter VHD-Anbieter zum Erreichen der Anlage gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="50ac1-113">Attaches a virtual hard disk (VHD) or CD or DVD image file (ISO) by locating an appropriate VHD provider to accomplish the attachment.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50ac1-114"><a href="/windows/win32/api/virtdisk/nf-virtdisk-breakmirrorvirtualdisk"><strong>Breakmirrorvirtualdisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="50ac1-114"><a href="/windows/win32/api/virtdisk/nf-virtdisk-breakmirrorvirtualdisk"><strong>BreakMirrorVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="50ac1-115">Unterbricht einen zuvor initiierten Spiegel Vorgang und legt den Spiegel als aktiven virtuellen Datenträger fest.</span><span class="sxs-lookup"><span data-stu-id="50ac1-115">Breaks a previously initiated mirror operation and sets the mirror to be the active virtual disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50ac1-116"><a href="/windows/win32/api/virtdisk/nf-virtdisk-compactvirtualdisk"><strong>Compactvirtualdisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="50ac1-116"><a href="/windows/win32/api/virtdisk/nf-virtdisk-compactvirtualdisk"><strong>CompactVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="50ac1-117">Verringert die Größe einer Sicherungs Speicherdatei für eine virtuelle Festplatte (VHD).</span><span class="sxs-lookup"><span data-stu-id="50ac1-117">Reduces the size of a virtual hard disk (VHD) backing store file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50ac1-118"><a href="/windows/win32/api/virtdisk/nf-virtdisk-createvirtualdisk"><strong>"Kreatevirtualdisk"</strong></a></span><span class="sxs-lookup"><span data-stu-id="50ac1-118"><a href="/windows/win32/api/virtdisk/nf-virtdisk-createvirtualdisk"><strong>CreateVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="50ac1-119">Erstellt eine virtuelle Festplatten Abbild Datei (VHD), entweder mithilfe von Standardparametern oder mithilfe eines vorhandenen virtuellen Datenträgers oder physischen Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="50ac1-119">Creates a virtual hard disk (VHD) image file, either using default parameters or using an existing virtual disk or physical disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50ac1-120"><a href="/windows/win32/api/virtdisk/nf-virtdisk-deletesnapshotvhdset"><strong>Delta-esnapshotvhdset</strong></a></span><span class="sxs-lookup"><span data-stu-id="50ac1-120"><a href="/windows/win32/api/virtdisk/nf-virtdisk-deletesnapshotvhdset"><strong>DeleteSnapshotVhdSet</strong></a></span></span></p></td>
<td><p><span data-ttu-id="50ac1-121">Löscht eine Momentaufnahme aus einer VHD-Satz Datei.</span><span class="sxs-lookup"><span data-stu-id="50ac1-121">Deletes a snapshot from a VHD Set file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50ac1-122"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-deletevirtualdiskmetadata"><strong>Deletevirtualdiskmetadata</strong></a></span><span class="sxs-lookup"><span data-stu-id="50ac1-122"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-deletevirtualdiskmetadata"><strong>DeleteVirtualDiskMetadata</strong></a></span></span></p></td>
<td><p><span data-ttu-id="50ac1-123">Löscht Metadaten von einem virtuellen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="50ac1-123">Deletes metadata from a virtual disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50ac1-124"><a href="/windows/win32/api/virtdisk/nf-virtdisk-detachvirtualdisk"><strong>Detachvirtualdisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="50ac1-124"><a href="/windows/win32/api/virtdisk/nf-virtdisk-detachvirtualdisk"><strong>DetachVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="50ac1-125">Trennt eine virtuelle Festplatte (VHD) oder eine CD-oder DVD-Abbild Datei (ISO), indem Sie einen entsprechenden virtuellen Datenträger Anbieter zum Ausführen des Vorgangs sucht.</span><span class="sxs-lookup"><span data-stu-id="50ac1-125">Detaches a virtual hard disk (VHD) or CD or DVD image file (ISO) by locating an appropriate virtual disk provider to accomplish the operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50ac1-126"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-enumeratevirtualdiskmetadata"><strong>Enumeratevirtualdiskmetadata</strong></a></span><span class="sxs-lookup"><span data-stu-id="50ac1-126"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-enumeratevirtualdiskmetadata"><strong>EnumerateVirtualDiskMetadata</strong></a></span></span></p></td>
<td><p><span data-ttu-id="50ac1-127">Listet die Metadaten auf, die einem virtuellen Datenträger zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="50ac1-127">Enumerates the metadata associated with a virtual disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50ac1-128"><a href="/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk"><strong>Expandvirtualdisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="50ac1-128"><a href="/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk"><strong>ExpandVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="50ac1-129">Vergrößert die Größe einer festen oder dynamisch erweiterbaren virtuellen Festplatte (VHD).</span><span class="sxs-lookup"><span data-stu-id="50ac1-129">Increases the size of a fixed or dynamically expandable virtual hard disk (VHD).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50ac1-130"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getstoragedependencyinformation"><strong>Getstoragedependencyinformation</strong></a></span><span class="sxs-lookup"><span data-stu-id="50ac1-130"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getstoragedependencyinformation"><strong>GetStorageDependencyInformation</strong></a></span></span></p></td>
<td><p><span data-ttu-id="50ac1-131">Gibt die Beziehungen zwischen virtuellen Festplatten (VHDs), CD-oder DVD-Abbild Datei (ISO) oder den Volumes auf diesen Datenträgern und dem übergeordneten Datenträger oder Volume zurück.</span><span class="sxs-lookup"><span data-stu-id="50ac1-131">Returns the relationships between virtual hard disks (VHDs) or CD or DVD image file (ISO) or the volumes contained within those disks and their parent disk or volume.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50ac1-132"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskinformation"><strong>Getvirtualdiskinformation</strong></a></span><span class="sxs-lookup"><span data-stu-id="50ac1-132"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskinformation"><strong>GetVirtualDiskInformation</strong></a></span></span></p></td>
<td><p><span data-ttu-id="50ac1-133">Ruft Informationen zu einer virtuellen Festplatte ab.</span><span class="sxs-lookup"><span data-stu-id="50ac1-133">Retrieves information about a VHD.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50ac1-134"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-getvirtualdiskmetadata"><strong>Getvirtualdiskmetadata</strong></a></span><span class="sxs-lookup"><span data-stu-id="50ac1-134"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-getvirtualdiskmetadata"><strong>GetVirtualDiskMetadata</strong></a></span></span></p></td>
<td><p><span data-ttu-id="50ac1-135">Ruft die angegebenen Metadaten von der virtuellen Festplatte ab.</span><span class="sxs-lookup"><span data-stu-id="50ac1-135">Retrieves the specified metadata from the virtual disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50ac1-136"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskoperationprogress"><strong>Getvirtualdiskoperationprogress</strong></a></span><span class="sxs-lookup"><span data-stu-id="50ac1-136"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskoperationprogress"><strong>GetVirtualDiskOperationProgress</strong></a></span></span></p></td>
<td><p><span data-ttu-id="50ac1-137">Überprüft den Fortschritt eines asynchronen virtuellen Festplatten Vorgangs (VHD).</span><span class="sxs-lookup"><span data-stu-id="50ac1-137">Checks the progress of an asynchronous virtual hard disk (VHD) operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50ac1-138"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskphysicalpath"><strong>Getvirtualdiskphysicalpath</strong></a></span><span class="sxs-lookup"><span data-stu-id="50ac1-138"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskphysicalpath"><strong>GetVirtualDiskPhysicalPath</strong></a></span></span></p></td>
<td><p><span data-ttu-id="50ac1-139">Ruft den Pfad zum physischen Geräte Objekt ab, das eine virtuelle Festplatte (VHD) oder eine CD-oder DVD-Abbild Datei (ISO) enthält.</span><span class="sxs-lookup"><span data-stu-id="50ac1-139">Retrieves the path to the physical device object that contains a virtual hard disk (VHD) or CD or DVD image file (ISO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50ac1-140"><a href="/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk"><strong>Mergevirtualdisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="50ac1-140"><a href="/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk"><strong>MergeVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="50ac1-141">Führt eine untergeordnete virtuelle Festplatte (VHD) in einer differenzierenden Kette mit mindestens einem übergeordneten virtuellen Datenträger in der Kette zusammen.</span><span class="sxs-lookup"><span data-stu-id="50ac1-141">Merges a child virtual hard disk (VHD) in a differencing chain with one or more parent virtual disks in the chain.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50ac1-142"><a href="/windows/win32/api/virtdisk/nf-virtdisk-mirrorvirtualdisk"><strong>Mirrorvirtualdisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="50ac1-142"><a href="/windows/win32/api/virtdisk/nf-virtdisk-mirrorvirtualdisk"><strong>MirrorVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="50ac1-143">Initiiert eine Spiegel Operation für einen virtuellen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="50ac1-143">Initiates a mirror operation for a virtual disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50ac1-144"><a href="/windows/win32/api/virtdisk/nf-virtdisk-modifyvhdset"><strong>Modifyvhdset</strong></a></span><span class="sxs-lookup"><span data-stu-id="50ac1-144"><a href="/windows/win32/api/virtdisk/nf-virtdisk-modifyvhdset"><strong>ModifyVhdSet</strong></a></span></span></p></td>
<td><p><span data-ttu-id="50ac1-145">Ändert den internen Inhalt einer virtuellen Datenträger Datei.</span><span class="sxs-lookup"><span data-stu-id="50ac1-145">Modifies the internal contents of a virtual disk file.</span></span> <span data-ttu-id="50ac1-146">Kann zum Festlegen des aktiven Blatts oder zum Beheben von Momentaufnahme Einträgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="50ac1-146">Can be used to set the active leaf, or to fix up snapshot entries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50ac1-147"><a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk"><strong>Openvirtualdisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="50ac1-147"><a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk"><strong>OpenVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="50ac1-148">Öffnet eine virtuelle Festplatte (VHD) oder eine CD-oder DVD-Abbild Datei (ISO) zur Verwendung.</span><span class="sxs-lookup"><span data-stu-id="50ac1-148">Opens a virtual hard disk (VHD) or CD or DVD image file (ISO) for use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50ac1-149"><a href="/windows/win32/api/virtdisk/nf-virtdisk-querychangesvirtualdisk"><strong>Querychangesvirtualdisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="50ac1-149"><a href="/windows/win32/api/virtdisk/nf-virtdisk-querychangesvirtualdisk"><strong>QueryChangesVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="50ac1-150">Ruft Informationen zu Änderungen an den angegebenen Bereichen einer virtuellen Festplatte (VHD) ab, die von der robusten Änderungs Nachverfolgung (RCT) nachverfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="50ac1-150">Retrieves information about changes to the specified areas of a virtual hard disk (VHD) that are tracked by resilient change tracking (RCT).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50ac1-151"><a href="/windows/win32/api/virtdisk/nf-virtdisk-rawscsivirtualdisk"><strong>Rawscsivirtualdisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="50ac1-151"><a href="/windows/win32/api/virtdisk/nf-virtdisk-rawscsivirtualdisk"><strong>RawSCSIVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="50ac1-152">Gibt eine eingebettete SCSI-Anforderung direkt an eine virtuelle Festplatte aus.</span><span class="sxs-lookup"><span data-stu-id="50ac1-152">Issues an embedded SCSI request directly to a virtual hard disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50ac1-153"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-resizevirtualdisk"><strong>Resizevirtualdisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="50ac1-153"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-resizevirtualdisk"><strong>ResizeVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="50ac1-154">Ändert die Größe eines virtuellen Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="50ac1-154">Resizes a virtual disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50ac1-155"><a href="/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation"><strong>Setvirtualdiskinformation</strong></a></span><span class="sxs-lookup"><span data-stu-id="50ac1-155"><a href="/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation"><strong>SetVirtualDiskInformation</strong></a></span></span></p></td>
<td><p><span data-ttu-id="50ac1-156">Legt Informationen zu einer virtuellen Festplatte (VHD) fest.</span><span class="sxs-lookup"><span data-stu-id="50ac1-156">Sets information about a virtual hard disk (VHD).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50ac1-157"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-setvirtualdiskmetadata"><strong>Setvirtualdiskmetadata</strong></a></span><span class="sxs-lookup"><span data-stu-id="50ac1-157"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-setvirtualdiskmetadata"><strong>SetVirtualDiskMetadata</strong></a></span></span></p></td>
<td><p><span data-ttu-id="50ac1-158">Legt ein Metadatenelement für einen virtuellen Datenträger fest.</span><span class="sxs-lookup"><span data-stu-id="50ac1-158">Sets a metadata item for a virtual disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50ac1-159"><a href="/windows/win32/api/virtdisk/nf-virtdisk-takesnapshotvhdset"><strong>Takesnapshotvhdset</strong></a></span><span class="sxs-lookup"><span data-stu-id="50ac1-159"><a href="/windows/win32/api/virtdisk/nf-virtdisk-takesnapshotvhdset"><strong>TakeSnapshotVhdSet</strong></a></span></span></p></td>
<td><p><span data-ttu-id="50ac1-160">Erstellt eine Momentaufnahme des aktuellen virtuellen Datenträgers für VHD-Satz Dateien.</span><span class="sxs-lookup"><span data-stu-id="50ac1-160">Creates a snapshot of the current virtual disk for VHD Set files.</span></span></p></td>
</tr>
</tbody>
</table>

 

 

 
