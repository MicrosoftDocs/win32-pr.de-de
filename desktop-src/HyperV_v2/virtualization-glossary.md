---
description: Glossar der Begriffe, die in der Dokumentation zum Windows Virtualization SDK verwendet werden.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 365D0295-EA0B-4B40-8272-DFF62B2A6F3D
title: Hyper-V-Glossar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: badb8fdfd25c4b7e11529778ab2cbd3c8cee5f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217810"
---
# <a name="hyper-v-glossary"></a><span data-ttu-id="cb3a8-103">Hyper-V-Glossar</span><span class="sxs-lookup"><span data-stu-id="cb3a8-103">Hyper-V glossary</span></span>

<span data-ttu-id="cb3a8-104">Dieses Thema enthält ein Glossar der Begriffe, die in der Dokumentation zum Windows Virtualization SDK verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-104">This topic provides a glossary of terms used in the Windows Virtualization SDK documentation.</span></span>

<dl> <dt>

<span data-ttu-id="cb3a8-105"><span id="hyperv.virtualization_glossary_binding"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_BINDING"></span>**lichere**</span><span class="sxs-lookup"><span data-stu-id="cb3a8-105"><span id="hyperv.virtualization_glossary_binding"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_BINDING"></span>**binding**</span></span>
</dt> <dd>

<span data-ttu-id="cb3a8-106">Ein Prozess, mit dem Software Dienste und Ebenen miteinander verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-106">A process by which software services and layers are linked together.</span></span> <span data-ttu-id="cb3a8-107">Wenn ein Netzwerkdienst installiert wird, werden die Bindungs Beziehungen und die Abhängigkeiten für die Dienste festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-107">When a network service is installed, the binding relationships and dependencies for the services are established.</span></span>

</dd> <dt>

<span data-ttu-id="cb3a8-108"><span id="hyperv.virtualization_glossary_checkpoint"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_CHECKPOINT"></span>**Kal**</span><span class="sxs-lookup"><span data-stu-id="cb3a8-108"><span id="hyperv.virtualization_glossary_checkpoint"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_CHECKPOINT"></span>**checkpoint**</span></span>
</dt> <dd>

<span data-ttu-id="cb3a8-109">Eine Momentaufnahme eines virtuellen Computers, der es einem Administrator ermöglicht, den Rollback des virtuellen Computers zum Zeitpunkt der Erstellung des Prüf Punkts wieder in seinen Zustand auszuführen.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-109">A snapshot of a virtual machine that enables an administrator to roll the virtual machine back to its state at the moment the checkpoint was created.</span></span>

</dd> <dt>

<span data-ttu-id="cb3a8-110"><span id="hyperv.virtualization_glossary_compact"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_COMPACT"></span>**theit**</span><span class="sxs-lookup"><span data-stu-id="cb3a8-110"><span id="hyperv.virtualization_glossary_compact"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_COMPACT"></span>**compact**</span></span>
</dt> <dd>

<span data-ttu-id="cb3a8-111">Um die Größe einer dynamisch erweiterbaren virtuellen Festplatte zu verringern, indem Sie nicht verwendeten Speicherplatz aus der VHD-Datei entfernen.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-111">To reduce the size of a dynamically expanding virtual hard disk by removing unused space from the .vhd file.</span></span>

</dd> <dt>

<span data-ttu-id="cb3a8-112"><span id="hyperv.virtualization_glossary_dvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DVHD"></span>**differenzierende virtuelle Festplatte**</span><span class="sxs-lookup"><span data-stu-id="cb3a8-112"><span id="hyperv.virtualization_glossary_dvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DVHD"></span>**differencing virtual hard disk**</span></span>
</dt> <dd>

<span data-ttu-id="cb3a8-113">Eine virtuelle Festplatte, auf der die Änderungen an einer zugeordneten übergeordneten virtuellen Festplatte gespeichert werden, um das übergeordnete Element intakt zu lassen.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-113">A virtual hard disk that stores the changes to an associated parent virtual hard disk for the purpose of keeping the parent intact.</span></span> <span data-ttu-id="cb3a8-114">Der differenzierende Datenträger ist eine separate VHD-Datei, die mit der VHD-Datei des übergeordneten Datenträgers verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-114">The differencing disk is a separate .vhd file that is associated with the .vhd file of the parent disk.</span></span> <span data-ttu-id="cb3a8-115">Änderungen werden auf der differenzierenden Festplatte weiterhin gesammelt, bis Sie mit dem übergeordneten Datenträger zusammengeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-115">Changes continue to accumulate in the differencing disk until it is merged to the parent disk.</span></span>

</dd> <dt>

<span data-ttu-id="cb3a8-116"><span id="hyperv.virtualization_glossary_devhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DEVHD"></span>**dynamisch erweiterbare virtuelle Festplatte**</span><span class="sxs-lookup"><span data-stu-id="cb3a8-116"><span id="hyperv.virtualization_glossary_devhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DEVHD"></span>**dynamically expanding virtual hard disk**</span></span>
</dt> <dd>

<span data-ttu-id="cb3a8-117">Eine virtuelle Festplatte, die bei jeder Änderung der Größe zunimmt.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-117">A virtual hard disk that grows in size each time it is modified.</span></span> <span data-ttu-id="cb3a8-118">Diese Art virtueller Festplatte wird als 3-KB-VHD-Datei gestartet und kann so groß werden, wie die maximale Größe, die beim Erstellen der Datei angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-118">This type of virtual hard disk starts as a 3 KB .vhd file and can grow as large as the maximum size specified when the file was created.</span></span> <span data-ttu-id="cb3a8-119">Die einzige Möglichkeit, die Dateigröße zu reduzieren, besteht darin, die gelöschten Daten zu löschen und dann die virtuelle Festplatte zu komprimieren.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-119">The only way to reduce the file size is to zero out the deleted data and then compact the virtual hard disk.</span></span>

</dd> <dt>

<span data-ttu-id="cb3a8-120"><span id="hyperv.virtualization_glossary_fvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_FVHD"></span>**virtuelle Festplatte mit fester Größe**</span><span class="sxs-lookup"><span data-stu-id="cb3a8-120"><span id="hyperv.virtualization_glossary_fvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_FVHD"></span>**fixed-size virtual hard disk**</span></span>
</dt> <dd>

<span data-ttu-id="cb3a8-121">Eine virtuelle Festplatte mit fester Größe, die festgelegt wird und für die beim Erstellen des Datenträgers der gesamte Speicherplatz zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-121">A virtual hard disk with a fixed size that is determined and for which all space is allocated when the disk is created.</span></span> <span data-ttu-id="cb3a8-122">Die Größe des Datenträgers ändert sich nicht, wenn Daten hinzugefügt oder gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-122">The size of the disk does not change when data is added or deleted.</span></span>

</dd> <dt>

<span data-ttu-id="cb3a8-123"><span id="hyperv.virtualization_glossary_gen1vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN1VM"></span>**Virtueller Computer der Generation 1**</span><span class="sxs-lookup"><span data-stu-id="cb3a8-123"><span id="hyperv.virtualization_glossary_gen1vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN1VM"></span>**Generation 1 virtual machine**</span></span>
</dt> <dd>

<span data-ttu-id="cb3a8-124">Ein virtueller Computer (VM), der die gleiche virtuelle Hardware enthält, die in Hyper-V-Versionen vor Windows 8.1 und Windows Server 2012 R2 vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-124">A virtual machine (VM) that contains the same virtual hardware present in versions of Hyper-V prior to Windows 8.1 and Windows Server 2012 R2</span></span>

</dd> <dt>

<span data-ttu-id="cb3a8-125"><span id="hyperv.virtualization_glossary_gen2vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN2VM"></span>**Virtueller Computer der Generation 2**</span><span class="sxs-lookup"><span data-stu-id="cb3a8-125"><span id="hyperv.virtualization_glossary_gen2vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN2VM"></span>**Generation 2 virtual machine**</span></span>
</dt> <dd>

<span data-ttu-id="cb3a8-126">Ein virtueller Computer (VM), der ein vereinfachtes virtuelles Hardware Modell enthält und UEFI-Firmware anstelle von BIOS verwendet.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-126">A virtual machine (VM) that contains a simplified virtual hardware model and uses UEFI firmware instead of BIOS.</span></span> <span data-ttu-id="cb3a8-127">Auf diesem virtuellen Computer werden die meisten der emulierten Geräte entfernt, was die Komplexität der Verwaltung und die Angriffsfläche für Sicherheitsangriffe reduziert.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-127">In this VM, most of the emulated devices are removed, which reduces management complexity and security attack surface.</span></span>

</dd> <dt>

<span data-ttu-id="cb3a8-128"><span id="hyperv.virtualization_glossary_guestos"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GUESTOS"></span>**Gast Betriebssystem**</span><span class="sxs-lookup"><span data-stu-id="cb3a8-128"><span id="hyperv.virtualization_glossary_guestos"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GUESTOS"></span>**guest operating system**</span></span>
</dt> <dd>

<span data-ttu-id="cb3a8-129">Das auf der virtuellen Maschine ausgeführte Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="cb3a8-129">The operating system running on a virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="cb3a8-130"><span id="hyperv.virtualization_glossary_integration_services"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_INTEGRATION_SERVICES"></span>**Integration Services**</span><span class="sxs-lookup"><span data-stu-id="cb3a8-130"><span id="hyperv.virtualization_glossary_integration_services"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_INTEGRATION_SERVICES"></span>**integration services**</span></span>
</dt> <dd>

<span data-ttu-id="cb3a8-131">Eine Auflistung der Dienste und Software Treiber, die die Leistung maximieren und eine bessere Benutzer Leistung innerhalb eines virtuellen Computers ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-131">A collection of services and software drivers that maximize performance and provide a better user experience within a virtual machine.</span></span> <span data-ttu-id="cb3a8-132">Integration Services sind nur für unterstützte Gast Betriebssysteme verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-132">Integration services are only available for supported guest operating systems.</span></span>

</dd> <dt>

<span data-ttu-id="cb3a8-133"><span id="hyperv.virtualization_glossary_kvp"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_KVP"></span>**Schlüssel-Wert-Paar**</span><span class="sxs-lookup"><span data-stu-id="cb3a8-133"><span id="hyperv.virtualization_glossary_kvp"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_KVP"></span>**key-value pair**</span></span>
</dt> <dd>

<span data-ttu-id="cb3a8-134">Ein Satz von Datenelementen, der einen eindeutigen Bezeichner enthält, der als Schlüssel bezeichnet wird, sowie einen Wert, der die eigentlichen Daten für den Schlüssel ist.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-134">A set of data items that contains a unique identifier, called a key, and a value that is the actual data for the key.</span></span>

</dd> <dt>

<span data-ttu-id="cb3a8-135"><span id="hyperv.virtualization_glossary_physical_computer"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_PHYSICAL_COMPUTER"></span>**physischer Computer**</span><span class="sxs-lookup"><span data-stu-id="cb3a8-135"><span id="hyperv.virtualization_glossary_physical_computer"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_PHYSICAL_COMPUTER"></span>**physical computer**</span></span>
</dt> <dd>

<span data-ttu-id="cb3a8-136">Einen hardwarebasierten Computer im Gegensatz zu einer softwarebasierten virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-136">A hardware-based computer, as opposed to a software-based virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="cb3a8-137"><span id="hyperv.virtualization_glossary_saved_state"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_SAVED_STATE"></span>**gespeicherter Zustand**</span><span class="sxs-lookup"><span data-stu-id="cb3a8-137"><span id="hyperv.virtualization_glossary_saved_state"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_SAVED_STATE"></span>**saved state**</span></span>
</dt> <dd>

<span data-ttu-id="cb3a8-138">Eine Möglichkeit, eine virtuelle Maschine so zu speichern, dass Sie schnell fortgesetzt werden kann, ähnlich wie bei einem Laptop im Ruhezustand.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-138">A manner of storing a virtual machine so that it can be quickly resumed, similar to a hibernated laptop.</span></span> <span data-ttu-id="cb3a8-139">Wenn Sie einen aktiven virtuellen Computer in einem gespeicherten Zustand platzieren, beenden Virtual Server und Hyper-V den virtuellen Computer, schreiben die Daten, die im Arbeitsspeicher vorhanden sind, in temporäre Dateien und beenden den Verbrauch von Systemressourcen.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-139">When you place a running virtual machine in a saved state, Virtual Server and Hyper-V stop the virtual machine, write the data that exists in memory to temporary files, and stop the consumption of system resources.</span></span> <span data-ttu-id="cb3a8-140">Beim Wiederherstellen einer virtuellen Maschine aus einem gespeicherten Zustand wird diese an die gleiche Bedingung zurückgegeben, in der Sie sich beim Speichern des Zustands befand.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-140">Restoring a virtual machine from a saved state returns it to the same condition it was in when its state was saved.</span></span>

</dd> <dt>

<span data-ttu-id="cb3a8-141"><span id="hyperv.virtualization_glossary_vfd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VFD"></span>**virtuelle Diskette**</span><span class="sxs-lookup"><span data-stu-id="cb3a8-141"><span id="hyperv.virtualization_glossary_vfd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VFD"></span>**virtual floppy disk**</span></span>
</dt> <dd>

<span data-ttu-id="cb3a8-142">Eine dateibasierte Version einer physischen Diskette.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-142">A file-based version of a physical floppy disk.</span></span> <span data-ttu-id="cb3a8-143">Eine virtuelle Diskette wird als Datei mit der Dateinamenerweiterung ". VFD" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-143">A virtual floppy disk is stored as a file with a .vfd file name extension.</span></span>

</dd> <dt>

<span data-ttu-id="cb3a8-144"><span id="hyperv.virtualization_glossary_vhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHD"></span>**virtuelle Festplatte**</span><span class="sxs-lookup"><span data-stu-id="cb3a8-144"><span id="hyperv.virtualization_glossary_vhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHD"></span>**virtual hard disk**</span></span>
</dt> <dd>

<span data-ttu-id="cb3a8-145">Das Speichermedium für eine virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-145">The storage medium for a virtual machine.</span></span> <span data-ttu-id="cb3a8-146">Sie kann sich in einer beliebigen Speicher Topologie befinden, auf die das Host Betriebssystem zugreifen kann, einschließlich externer Geräte, Storage Area Networks und Network-Attached Storage.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-146">It can reside on any storage topology that the host operating system can access, including external devices, storage area networks, and network-attached storage.</span></span> <span data-ttu-id="cb3a8-147">Die Dateinamenerweiterung ist ". VHD".</span><span class="sxs-lookup"><span data-stu-id="cb3a8-147">The file name extension is .vhd.</span></span>

</dd> <dt>

<span data-ttu-id="cb3a8-148"><span id="hyperv.virtualization_glossary_vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM"></span>**virtueller Computer**</span><span class="sxs-lookup"><span data-stu-id="cb3a8-148"><span id="hyperv.virtualization_glossary_vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM"></span>**virtual machine**</span></span>
</dt> <dd>

<span data-ttu-id="cb3a8-149">Ein in Software implementierter Computer in einem Computer.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-149">A computer within a computer, implemented in software.</span></span> <span data-ttu-id="cb3a8-150">Eine virtuelle Maschine emuliert ein vollständiges Hardwaresystem vom Prozessor bis zur Netzwerkkarte in einer abgeschlossenen Softwareumgebung und ermöglicht so die parallele Ausführung von normalerweise inkompatiblen Betriebssystemen.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-150">A virtual machine emulates a complete hardware system, from processor to network card, in a self-contained, isolated software environment, enabling the simultaneous operation of otherwise incompatible operating systems.</span></span> <span data-ttu-id="cb3a8-151">Jedes untergeordnete Betriebssystem wird in einem eigenen virtuellen Computer für isolierte Software ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-151">Each child operating system runs in its own isolated software virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="cb3a8-152"><span id="hyperv.virtualization_glossary_vm_config"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM_CONFIG"></span>**Konfiguration der virtuellen Maschine**</span><span class="sxs-lookup"><span data-stu-id="cb3a8-152"><span id="hyperv.virtualization_glossary_vm_config"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM_CONFIG"></span>**virtual machine configuration**</span></span>
</dt> <dd>

<span data-ttu-id="cb3a8-153">Die Konfiguration der Ressourcen, die einem virtuellen Computer zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-153">The configuration of the resources assigned to a virtual machine.</span></span> <span data-ttu-id="cb3a8-154">Beispiele hierfür sind Geräte wie Datenträger und Netzwerkadapter sowie Arbeitsspeicher und Prozessoren.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-154">Examples include devices such as disks and network adapters, as well as memory and processors.</span></span>

</dd> <dt>

<span data-ttu-id="cb3a8-155"><span id="hyperv.virtualization_glossary_vmms"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMMS"></span>**Verwaltungsdienst für virtuelle Computer**</span><span class="sxs-lookup"><span data-stu-id="cb3a8-155"><span id="hyperv.virtualization_glossary_vmms"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMMS"></span>**Virtual Machine Management Service**</span></span>
</dt> <dd>

<span data-ttu-id="cb3a8-156">Der Hyper-V-Dienst, der Verwaltungs Zugriff auf virtuelle Computer bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-156">The Hyper-V service that provides management access to virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="cb3a8-157"><span id="hyperv.virtualization_glossary_vmss"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMSS"></span>**Momentaufnahme des virtuellen Computers**</span><span class="sxs-lookup"><span data-stu-id="cb3a8-157"><span id="hyperv.virtualization_glossary_vmss"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMSS"></span>**virtual machine snapshot**</span></span>
</dt> <dd>

<span data-ttu-id="cb3a8-158">Eine dateibasierte Momentaufnahme des Zustands, der Datenträger Daten und der Konfiguration einer virtuellen Maschine zu einem bestimmten Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-158">A file-based snapshot of the state, disk data, and configuration of a virtual machine at a specific point in time.</span></span>

</dd> <dt>

<span data-ttu-id="cb3a8-159"><span id="hyperv.virtualization_glossary_virtual_network"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_NETWORK"></span>**virtuelles Netzwerk**</span><span class="sxs-lookup"><span data-stu-id="cb3a8-159"><span id="hyperv.virtualization_glossary_virtual_network"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_NETWORK"></span>**virtual network**</span></span>
</dt> <dd>

<span data-ttu-id="cb3a8-160">Eine virtuelle Version eines physischen Netzwerk Schalters.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-160">A virtual version of a physical network switch.</span></span> <span data-ttu-id="cb3a8-161">ein virtuelles Netzwerk kann so konfiguriert werden, dass es für eine oder mehrere virtuelle Maschinen den Zugriff auf lokale oder externe Netzwerkressourcen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-161">A virtual network can be configured to provide access to local or external network resources for one or more virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="cb3a8-162"><span id="hyperv.virtualization_glossary_vnm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VNM"></span>**Virtual Network-Manager**</span><span class="sxs-lookup"><span data-stu-id="cb3a8-162"><span id="hyperv.virtualization_glossary_vnm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VNM"></span>**Virtual Network Manager**</span></span>
</dt> <dd>

<span data-ttu-id="cb3a8-163">Ein Hyper-V-Dienst zum Erstellen und Verwalten virtueller Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-163">A Hyper-V service used to create and manage virtual networks.</span></span>

</dd> <dt>

<span data-ttu-id="cb3a8-164"><span id="hyperv.virtualization_glossary_virtual_switch"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_SWITCH"></span>**virtueller Switch**</span><span class="sxs-lookup"><span data-stu-id="cb3a8-164"><span id="hyperv.virtualization_glossary_virtual_switch"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_SWITCH"></span>**virtual switch**</span></span>
</dt> <dd>

<span data-ttu-id="cb3a8-165">Siehe virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-165">See virtual network.</span></span>

</dd> <dt>

<span data-ttu-id="cb3a8-166"><span id="hyperv.virtualization_glossary_vhdx_resize"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHDX_RESIZE"></span>**Vhdx-Größe ändern**</span><span class="sxs-lookup"><span data-stu-id="cb3a8-166"><span id="hyperv.virtualization_glossary_vhdx_resize"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHDX_RESIZE"></span>**VHDX resize**</span></span>
</dt> <dd>

<span data-ttu-id="cb3a8-167">Der Vorgang, mit dem eine virtuelle Festplatte verkleinert oder erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="cb3a8-167">The operation that shrinks or expands a virtual hard disk.</span></span>

</dd> </dl>

 

 



