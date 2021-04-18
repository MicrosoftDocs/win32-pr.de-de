---
description: Ein Speicherpool Objekt modelliert einen Speicherpool in einem Speichersubsystem.
ms.assetid: a6104742-3ef9-4570-9728-3e6580953117
title: Speicher Pool Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c44719b825193faa75546ba1a0f7b42155a3e49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366202"
---
# <a name="storage-pool-object"></a><span data-ttu-id="c261f-103">Speicher Pool Objekt</span><span class="sxs-lookup"><span data-stu-id="c261f-103">Storage Pool Object</span></span>

<span data-ttu-id="c261f-104">\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]</span><span class="sxs-lookup"><span data-stu-id="c261f-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="c261f-105">Ein Speicherpool Objekt modelliert einen Speicherpool in einem Speichersubsystem.</span><span class="sxs-lookup"><span data-stu-id="c261f-105">A storage pool object models a storage pool in a storage subsystem.</span></span>

<span data-ttu-id="c261f-106">Ein Speicherpool enthält Laufwerk Blöcke von einem oder mehreren Laufwerken, die vom selben Hardware Anbieter verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="c261f-106">A storage pool contains drive extents from one or more drives that are managed by the same hardware provider.</span></span>

<span data-ttu-id="c261f-107">In der folgenden Tabelle werden verwandte Schnittstellen, Enumerationen und Strukturen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c261f-107">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="c261f-108">type</span><span class="sxs-lookup"><span data-stu-id="c261f-108">Type</span></span>                                              | <span data-ttu-id="c261f-109">Element</span><span class="sxs-lookup"><span data-stu-id="c261f-109">Element</span></span>                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c261f-110">Schnittstellen, die von diesem Objekt immer verfügbar gemacht werden</span><span class="sxs-lookup"><span data-stu-id="c261f-110">Interfaces that are always exposed by this object</span></span> | [<span data-ttu-id="c261f-111">**Ivdsstoragepool**</span><span class="sxs-lookup"><span data-stu-id="c261f-111">**IVdsStoragePool**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsstoragepool)                                                                                                                                                                                                                                                               |
| <span data-ttu-id="c261f-112">Zugehörige Enumerationen</span><span class="sxs-lookup"><span data-stu-id="c261f-112">Associated enumerations</span></span>                           | <span data-ttu-id="c261f-113">[**VDS \_ RAID- \_ Typ**](/windows/desktop/api/Vds/ne-vds-vds_raid_type), [**VDS- \_ Speicher \_ Pool \_ Status**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_status)und [**VDS- \_ Speicher \_ \_ Pooltyp**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_type).</span><span class="sxs-lookup"><span data-stu-id="c261f-113">[**VDS\_RAID\_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_raid_type), [**VDS\_STORAGE\_POOL\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_status), and [**VDS\_STORAGE\_POOL\_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_type).</span></span>                                                                                                                                  |
| <span data-ttu-id="c261f-114">Zugeordnete Strukturen</span><span class="sxs-lookup"><span data-stu-id="c261f-114">Associated structures</span></span>                             | <span data-ttu-id="c261f-115">[**VDS \_ HINTS2**](/windows/desktop/api/Vds/ns-vds-vds_hints2), [**VDS \_ - \_ Pool Attribute**](/windows/desktop/api/Vds/ns-vds-vds_pool_attributes), [**\_ \_ benutzerdefinierte \_ Attribute des VDS-Pools**](/windows/desktop/api/Vds/ns-vds-vds_pool_custom_attributes), Laufwerk Bereich des [**VDS- \_ Speicher \_ \_ \_ Pools**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_drive_extent)und [**VDS- \_ Speicherpool-unter \_ \_ Stützung**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_prop).</span><span class="sxs-lookup"><span data-stu-id="c261f-115">[**VDS\_HINTS2**](/windows/desktop/api/Vds/ns-vds-vds_hints2), [**VDS\_POOL\_ATTRIBUTES**](/windows/desktop/api/Vds/ns-vds-vds_pool_attributes), [**VDS\_POOL\_CUSTOM\_ATTRIBUTES**](/windows/desktop/api/Vds/ns-vds-vds_pool_custom_attributes), [**VDS\_STORAGE\_POOL\_DRIVE\_EXTENT**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_drive_extent), and [**VDS\_STORAGE\_POOL\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_prop).</span></span> |



 

 

 
