---
description: Laufwerksobjekt
ms.assetid: c1c17a97-cf4b-45b7-bc32-4bad94c3ddb2
title: Laufwerksobjekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d04ec68fab408c4ed6412990296c0ebb265b8c3e4c4c9b05645b1f4bd1e625fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603420"
---
# <a name="drive-object"></a>Laufwerksobjekt

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [Virtual Disk Service](virtual-disk-service-portal.md) durch die Windows Storage Verwaltungs-API. [](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

Ein Laufwerkobjekt modelliert ein physisches Laufwerk, das in einem Subsystem enthalten ist. Jedes Laufwerk stellt eine Verbindung mit einem Bus, belegt einen Slot und enthält eine Reihe von Laufwerksdeuten. Jedes Laufwerk kann zu einer beliebigen Anzahl von LUNs beitragen. Ein Laufwerk kann auch als Hotspare festgelegt werden.

Verwenden Sie [**die IVdsSubSystem::QueryDrives-Methode,**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives) um die Laufwerke zu bestimmen, die in einem bestimmten Subsystem enthalten sind. Aufrufer können einen Zeiger auf ein bestimmtes Laufwerk erhalten, indem sie das gewünschte Laufwerksobjekt aus der -Enumeration auswählen, die von der **QueryDrives-Methode** zurückgegeben wird, oder indem sie die [**IVdsSubSystem::GetDrive-Methode**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive) aufrufen und den gewünschten Bus und die Slotnummer übergeben. Mit einem Laufwerkobjekt können Sie den Laufwerksstatus festlegen und Laufwerkseigenschaften, zugeordnete Laufwerksausdungen und das Subsystem abfragen, das das Laufwerk enthält.

Neben einem Objektbezeichner, einem Namen und einer Seriennummer enthalten laufwerksobjekteigenschaften den Laufwerksstatus, die Integrität und flags. die Größe in Bytes; und eine Bus- und Slotnummer.

In der folgenden Tabelle sind verwandte Schnittstellen, Enumerationen und Strukturen aufgeführt.



| type                                              | Element                                                                                                                                         |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Schnittstellen, die von diesem Objekt immer verfügbar gemacht werden | [**IVdsDrive**](/windows/desktop/api/Vds/nn-vds-ivdsdrive)                                                                                                                  |
| Schnittstellen, die von diesem Objekt verfügbar gemacht werden können     | [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)                                                                                                      |
| Zugeordnete Enumerationen                           | [**VDS \_ \_LAUFWERKSFLAG,**](/windows/desktop/api/Vds/ne-vds-vds_drive_flag) [**\_ \_ VDS-LAUFWERKSTATUS**](/windows/desktop/api/Vds/ne-vds-vds_drive_status)UND [**\_ VDS-LAUFWERKS-EXTENT \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_extent). |
| Zugeordnete Strukturen                             | [**VDS \_ \_LAUFWERKSPROP-**](/windows/desktop/api/Vds/ns-vds-vds_drive_prop) [**UND \_ VDS-LAUFWERKBENACHRICHTIGUNG. \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hardwareanbieterobjekte](hardware-provider-objects.md)
</dt> <dt>

[**IVdsSubSystem::QueryDrives**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives)
</dt> <dt>

[**IVdsSubSystem::GetDrive**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive)
</dt> </dl>

 

 
