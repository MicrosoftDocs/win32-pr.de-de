---
description: Subsystem-Objekt
ms.assetid: f605a5de-9256-4b43-8e12-3d78fd6cd9f1
title: Subsystem-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c8314a798ea809b3175377bc5484f19629094db
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "104560736"
---
# <a name="subsystem-object"></a><span data-ttu-id="4ed00-103">Subsystem-Objekt</span><span class="sxs-lookup"><span data-stu-id="4ed00-103">Subsystem Object</span></span>

<span data-ttu-id="4ed00-104">\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]</span><span class="sxs-lookup"><span data-stu-id="4ed00-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="4ed00-105">Ein Subsystem-Objekt modelliert ein Speichersubsystem.</span><span class="sxs-lookup"><span data-stu-id="4ed00-105">A subsystem object models a storage subsystem.</span></span> <span data-ttu-id="4ed00-106">Ein Subsystem ist entweder ein RAID-Gehäuse oder eine PCI-RAID-Karte.</span><span class="sxs-lookup"><span data-stu-id="4ed00-106">A subsystem is either a RAID enclosure or a PCI RAID card.</span></span> <span data-ttu-id="4ed00-107">Ein einzelner Host Computer kann mit einer beliebigen Anzahl von Subsystemen verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="4ed00-107">A single host computer can be connected to any number of subsystems.</span></span> <span data-ttu-id="4ed00-108">Jedes Subsystem wird von genau einem Hardware Anbieter verwaltet.</span><span class="sxs-lookup"><span data-stu-id="4ed00-108">Each subsystem is managed by exactly one hardware provider.</span></span> <span data-ttu-id="4ed00-109">In einer SAN-Konfiguration stellt die Subsystem-Klasse ein SAN-Speicher Gehäuse dar.</span><span class="sxs-lookup"><span data-stu-id="4ed00-109">In a SAN configuration, the subsystem class represents a SAN storage enclosure.</span></span>

<span data-ttu-id="4ed00-110">Ein Subsystem kann eine beliebige Anzahl von Controllern und Laufwerken enthalten und kann eine beliebige Anzahl von LUNs auf dem Computer, auf dem der Hardware Anbieter ausgeführt wird, aufheben (Aufheben der Maskierung).</span><span class="sxs-lookup"><span data-stu-id="4ed00-110">A subsystem can contain any number of controllers and drives, and can surface (unmask) any number of LUNs to the computer on which the hardware provider is running.</span></span> <span data-ttu-id="4ed00-111">Die Maskierung von LUNs auf anderen Computern im Netzwerk kann von einem höheren Subsystem nicht durchführt werden.</span><span class="sxs-lookup"><span data-stu-id="4ed00-111">Higher-end subsystems can unmask LUNs to other computers on the network.</span></span> <span data-ttu-id="4ed00-112">Jedes Laufwerk innerhalb eines Subsystems ist mit einem Bus verbunden und belegt einen Slot im Bus.</span><span class="sxs-lookup"><span data-stu-id="4ed00-112">Each disk drive within a subsystem is connected to a bus and occupies a slot in the bus.</span></span> <span data-ttu-id="4ed00-113">Jeder Controller innerhalb eines Subsystems verfügt über einen oder mehrere Controller Anschlüsse.</span><span class="sxs-lookup"><span data-stu-id="4ed00-113">Each controller within a subsystem has one or more controller ports.</span></span>

<span data-ttu-id="4ed00-114">Die folgende Abbildung zeigt die physischen Geräte, die in einem Subsystem enthalten sind (LUNs werden nicht angezeigt), und die Beziehungen zwischen Ihnen.</span><span class="sxs-lookup"><span data-stu-id="4ed00-114">The illustration that follows shows the physical devices contained in a subsystem (LUNs are not shown) and the relationships among them.</span></span>

![Diagramm, das ein Subsystem anzeigt, das auf der linken Seite mit ' Ports ' beginnt, zu ' Controllers ' wechselt, und dann ein ' Bus ' mit ' Slots ', der zu einzelnen ' Drives ' führt.](images/vdssubsystem.png)

<span data-ttu-id="4ed00-116">VDS-Anwendungen verwenden die [**ivdshwprovider:: querysubsystems**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems) -Methode, um die Subsysteme abzufragen, die zu einem bestimmten Hardware Anbieter gehören.</span><span class="sxs-lookup"><span data-stu-id="4ed00-116">VDS applications use the [**IVdsHwProvider::QuerySubSystems**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems) method to query the subsystems that belong to a specific hardware provider.</span></span> <span data-ttu-id="4ed00-117">Aufrufer können einen Zeiger auf ein bestimmtes Subsystem abrufen, indem Sie das gewünschte Subsystem-Objekt aus der-Enumeration auswählen, das von der **querysubsystems** -Methode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4ed00-117">Callers can get a pointer to a specific subsystem by selecting the desired subsystem object from the enumeration that is returned by the **QuerySubSystems** method.</span></span> <span data-ttu-id="4ed00-118">Mit einem Subsystem-Objekt können Sie den Subsystem-Status festlegen, LUNs erstellen, Laufwerke ersetzen und Controller, Laufwerke und LUNs Abfragen.</span><span class="sxs-lookup"><span data-stu-id="4ed00-118">With a subsystem object, you can set the subsystem status, create LUNs, replace drives, and query for controllers, drives, and LUNs.</span></span>

<span data-ttu-id="4ed00-119">Zusätzlich zu einem Objekt Bezeichner, einem Namen und einer Seriennummer enthalten subsystemobjekteigenschaften den Subsystem Status, den Zustand und die Flags. die Anzahl der Controller, Slots und Busse; und eine Einstellung für die Neuerstellungs Priorität.</span><span class="sxs-lookup"><span data-stu-id="4ed00-119">In addition to an object identifier, a name, and a serial number, subsystem object properties include the subsystem status, health, and flags; a count of the controllers, slots, and buses; and a rebuild priority setting.</span></span>

<span data-ttu-id="4ed00-120">In der folgenden Tabelle werden verwandte Schnittstellen, Enumerationen und Strukturen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="4ed00-120">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="4ed00-121">type</span><span class="sxs-lookup"><span data-stu-id="4ed00-121">Type</span></span>                                                                                      | <span data-ttu-id="4ed00-122">Element</span><span class="sxs-lookup"><span data-stu-id="4ed00-122">Element</span></span>                                                                                                                          |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ed00-123">Schnittstellen, die von diesem Objekt immer verfügbar gemacht werden</span><span class="sxs-lookup"><span data-stu-id="4ed00-123">Interfaces that are always exposed by this object</span></span>                                         | <span data-ttu-id="4ed00-124">[**Ivdssubsystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem).</span><span class="sxs-lookup"><span data-stu-id="4ed00-124">[**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem).</span></span>                                                                                          |
| <span data-ttu-id="4ed00-125">Schnittstellen, die von diesem Objekt immer nur in VDS 1,1-und 2,0-iSCSI-Anbietern verfügbar gemacht werden</span><span class="sxs-lookup"><span data-stu-id="4ed00-125">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 iSCSI providers only</span></span> | <span data-ttu-id="4ed00-126">[**Ivdssubsystemiscsi**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemiscsi) und [**ivdssubsystematimporttarget**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemimporttarget).</span><span class="sxs-lookup"><span data-stu-id="4ed00-126">[**IVdsSubSystemIscsi**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemiscsi) and [**IVdsSubSystemImportTarget**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemimporttarget).</span></span>             |
| <span data-ttu-id="4ed00-127">Schnittstellen, die von diesem Objekt verfügbar gemacht werden können</span><span class="sxs-lookup"><span data-stu-id="4ed00-127">Interfaces that may be exposed by this object</span></span>                                             | <span data-ttu-id="4ed00-128">[**Ivdssubsystemnaming**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemnaming) und [**ivdsmaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance).</span><span class="sxs-lookup"><span data-stu-id="4ed00-128">[**IVdsSubSystemNaming**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemnaming) and [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance).</span></span>                               |
| <span data-ttu-id="4ed00-129">Zugehörige Enumerationen</span><span class="sxs-lookup"><span data-stu-id="4ed00-129">Associated enumerations</span></span>                                                                   | <span data-ttu-id="4ed00-130">[**VDS \_ \_ \_ Subsystemflag**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_flag) und [**Status des VDS- \_ \_ Subsystems \_**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_status).</span><span class="sxs-lookup"><span data-stu-id="4ed00-130">[**VDS\_SUB\_SYSTEM\_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_flag) and [**VDS\_SUB\_SYSTEM\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_status).</span></span>             |
| <span data-ttu-id="4ed00-131">Zugeordnete Strukturen</span><span class="sxs-lookup"><span data-stu-id="4ed00-131">Associated structures</span></span>                                                                     | <span data-ttu-id="4ed00-132">[**VDS \_ Sub- \_ System- \_ Prop**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_prop) -und [**VDS- \_ unter \_ System \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification).</span><span class="sxs-lookup"><span data-stu-id="4ed00-132">[**VDS\_SUB\_SYSTEM\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_prop) and [**VDS\_SUB\_SYSTEM\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="4ed00-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4ed00-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ed00-134">Hardware Anbieter Objekte</span><span class="sxs-lookup"><span data-stu-id="4ed00-134">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="4ed00-135">**Ivdshwprovider:: querysubsystems**</span><span class="sxs-lookup"><span data-stu-id="4ed00-135">**IVdsHwProvider::QuerySubSystems**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems)
</dt> </dl>

 

 
