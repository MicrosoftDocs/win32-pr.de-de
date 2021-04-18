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
# <a name="storage-pool-object"></a>Speicher Pool Objekt

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Ein Speicherpool Objekt modelliert einen Speicherpool in einem Speichersubsystem.

Ein Speicherpool enthält Laufwerk Blöcke von einem oder mehreren Laufwerken, die vom selben Hardware Anbieter verwaltet werden.

In der folgenden Tabelle werden verwandte Schnittstellen, Enumerationen und Strukturen aufgelistet.



| type                                              | Element                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schnittstellen, die von diesem Objekt immer verfügbar gemacht werden | [**Ivdsstoragepool**](/windows/desktop/api/Vds/nn-vds-ivdsstoragepool)                                                                                                                                                                                                                                                               |
| Zugehörige Enumerationen                           | [**VDS \_ RAID- \_ Typ**](/windows/desktop/api/Vds/ne-vds-vds_raid_type), [**VDS- \_ Speicher \_ Pool \_ Status**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_status)und [**VDS- \_ Speicher \_ \_ Pooltyp**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_type).                                                                                                                                  |
| Zugeordnete Strukturen                             | [**VDS \_ HINTS2**](/windows/desktop/api/Vds/ns-vds-vds_hints2), [**VDS \_ - \_ Pool Attribute**](/windows/desktop/api/Vds/ns-vds-vds_pool_attributes), [**\_ \_ benutzerdefinierte \_ Attribute des VDS-Pools**](/windows/desktop/api/Vds/ns-vds-vds_pool_custom_attributes), Laufwerk Bereich des [**VDS- \_ Speicher \_ \_ \_ Pools**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_drive_extent)und [**VDS- \_ Speicherpool-unter \_ \_ Stützung**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_prop). |



 

 

 
