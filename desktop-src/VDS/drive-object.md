---
description: Laufwerks Objekt
ms.assetid: c1c17a97-cf4b-45b7-bc32-4bad94c3ddb2
title: Laufwerks Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df8501c79f9381dba80a1fe0276014dccdf7a34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216177"
---
# <a name="drive-object"></a><span data-ttu-id="15d55-103">Laufwerks Objekt</span><span class="sxs-lookup"><span data-stu-id="15d55-103">Drive Object</span></span>

<span data-ttu-id="15d55-104">\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]</span><span class="sxs-lookup"><span data-stu-id="15d55-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="15d55-105">Ein Laufwerks Objekt modelliert ein physisches Laufwerk, das in einem Subsystem enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="15d55-105">A drive object models a physical disk drive that is contained within a subsystem.</span></span> <span data-ttu-id="15d55-106">Jedes Laufwerk stellt eine Verbindung mit einem Bus her, belegt einen Slot und enthält eine Reihe von Laufwerks Blöcken.</span><span class="sxs-lookup"><span data-stu-id="15d55-106">Each drive connects to a bus, occupies a slot, and contains a set of drive extents.</span></span> <span data-ttu-id="15d55-107">Jedes Laufwerk kann zu einer beliebigen Anzahl von LUNs beitragen.</span><span class="sxs-lookup"><span data-stu-id="15d55-107">Each drive can contribute extents to any number of LUNs.</span></span> <span data-ttu-id="15d55-108">Ein Laufwerk kann auch als Hot Spare festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="15d55-108">A drive can also be designated as a hot spare.</span></span>

<span data-ttu-id="15d55-109">Verwenden Sie die [**ivdssubsystem:: querydrives**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives) -Methode, um die Laufwerke zu ermitteln, die in einem bestimmten Subsystem enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="15d55-109">Use the [**IVdsSubSystem::QueryDrives**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives) method to determine the drives that are contained by a specific subsystem.</span></span> <span data-ttu-id="15d55-110">Aufrufer können einen Zeiger auf ein bestimmtes Laufwerk abrufen, indem Sie das gewünschte Laufwerks Objekt aus der-Enumeration auswählen, das von der **querydrives** -Methode zurückgegeben wird, oder indem Sie die [**ivdssubsystem:: GetDrive**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive) -Methode aufrufen und die gewünschte Busnummer und Slot-Nummer übergeben.</span><span class="sxs-lookup"><span data-stu-id="15d55-110">Callers can get a pointer to a specific drive by selecting the desired drive object from the enumeration that is returned by the **QueryDrives** method, or by invoking the [**IVdsSubSystem::GetDrive**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive) method and passing in the desired bus and slot number.</span></span> <span data-ttu-id="15d55-111">Mit einem Laufwerks Objekt können Sie den Laufwerks Status und die Abfrage für Laufwerks Eigenschaften, zugeordnete Laufwerks Blöcke und das Subsystem, das das Laufwerk enthält, festlegen.</span><span class="sxs-lookup"><span data-stu-id="15d55-111">With a drive object, you can set the drive status and query for drive properties, associated drive extents, and the subsystem containing the drive.</span></span>

<span data-ttu-id="15d55-112">Zusätzlich zu einem Objekt Bezeichner, einem Namen und einer Seriennummer enthalten die Eigenschaften des Laufwerks Objekt den Status, den Zustand und die Flags des Laufwerks. die Größe in Bytes. und eine Bus-und Slot-Nummer.</span><span class="sxs-lookup"><span data-stu-id="15d55-112">In addition to an object identifier, a name, and a serial number, drive object properties include the drive status, health, and flags; the size in bytes; and a bus and slot number.</span></span>

<span data-ttu-id="15d55-113">In der folgenden Tabelle werden verwandte Schnittstellen, Enumerationen und Strukturen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="15d55-113">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="15d55-114">type</span><span class="sxs-lookup"><span data-stu-id="15d55-114">Type</span></span>                                              | <span data-ttu-id="15d55-115">Element</span><span class="sxs-lookup"><span data-stu-id="15d55-115">Element</span></span>                                                                                                                                         |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15d55-116">Schnittstellen, die von diesem Objekt immer verfügbar gemacht werden</span><span class="sxs-lookup"><span data-stu-id="15d55-116">Interfaces that are always exposed by this object</span></span> | [<span data-ttu-id="15d55-117">**Ivdsdrive**</span><span class="sxs-lookup"><span data-stu-id="15d55-117">**IVdsDrive**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsdrive)                                                                                                                  |
| <span data-ttu-id="15d55-118">Schnittstellen, die von diesem Objekt verfügbar gemacht werden können</span><span class="sxs-lookup"><span data-stu-id="15d55-118">Interfaces that may be exposed by this object</span></span>     | [<span data-ttu-id="15d55-119">**Ivdsmaintenance**</span><span class="sxs-lookup"><span data-stu-id="15d55-119">**IVdsMaintenance**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)                                                                                                      |
| <span data-ttu-id="15d55-120">Zugehörige Enumerationen</span><span class="sxs-lookup"><span data-stu-id="15d55-120">Associated enumerations</span></span>                           | <span data-ttu-id="15d55-121">[**VDS \_ \_Laufwerkflag**](/windows/desktop/api/Vds/ne-vds-vds_drive_flag), [**VDS- \_ Laufwerks \_ Status**](/windows/desktop/api/Vds/ne-vds-vds_drive_status)und [**VDS- \_ Laufwerks \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_extent)Block.</span><span class="sxs-lookup"><span data-stu-id="15d55-121">[**VDS\_DRIVE\_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_drive_flag), [**VDS\_DRIVE\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_drive_status), and [**VDS\_DRIVE\_EXTENT**](/windows/desktop/api/Vds/ns-vds-vds_drive_extent).</span></span> |
| <span data-ttu-id="15d55-122">Zugeordnete Strukturen</span><span class="sxs-lookup"><span data-stu-id="15d55-122">Associated structures</span></span>                             | <span data-ttu-id="15d55-123">[**VDS \_ Laufwerk- \_ Prop**](/windows/desktop/api/Vds/ns-vds-vds_drive_prop) -und [**VDS- \_ Laufwerk \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification).</span><span class="sxs-lookup"><span data-stu-id="15d55-123">[**VDS\_DRIVE\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_drive_prop) and [**VDS\_DRIVE\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification).</span></span>                                      |



 

## <a name="related-topics"></a><span data-ttu-id="15d55-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="15d55-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15d55-125">Hardware Anbieter Objekte</span><span class="sxs-lookup"><span data-stu-id="15d55-125">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="15d55-126">**Ivdssubsystem:: querydrives**</span><span class="sxs-lookup"><span data-stu-id="15d55-126">**IVdsSubSystem::QueryDrives**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives)
</dt> <dt>

[<span data-ttu-id="15d55-127">**Ivdssubsystem:: GetDrive**</span><span class="sxs-lookup"><span data-stu-id="15d55-127">**IVdsSubSystem::GetDrive**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive)
</dt> </dl>

 

 
