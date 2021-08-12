---
description: Subsystemobjekt
ms.assetid: f605a5de-9256-4b43-8e12-3d78fd6cd9f1
title: Subsystemobjekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4af9837da90497b07d133362c0a61549a63665f2c75d4c97b2d07369e4589fa7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603149"
---
# <a name="subsystem-object"></a>Subsystemobjekt

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [Virtual Disk Service](virtual-disk-service-portal.md) durch die Windows Storage Verwaltungs-API. [](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

Ein Subsystemobjekt modelliert ein Speichersubsystem. Ein Subsystem ist entweder ein RAID-Gehäuse oder eine PCI-RAID-Karte. Ein einzelner Hostcomputer kann mit einer beliebigen Anzahl von Subsystemen verbunden werden. Jedes Subsystem wird von genau einem Hardwareanbieter verwaltet. In einer SAN-Konfiguration stellt die Subsystemklasse ein SAN-Speichergehäuse dar.

Ein Subsystem kann eine beliebige Anzahl von Controllern und Laufwerken enthalten und eine beliebige Anzahl von LUNs auf dem Computer, auf dem der Hardwareanbieter ausgeführt wird, verfügbar machen (die Entmaskung wird entmaskiert). Bei Subsystemen mit höheren Enden können LUNs für andere Computer im Netzwerk entmaskiert werden. Jedes Laufwerk in einem Subsystem ist mit einem Bus verbunden und belegt einen Slot im Bus. Jeder Controller innerhalb eines Subsystems verfügt über mindestens einen Controllerport.

Die folgende Abbildung zeigt die physischen Geräte, die in einem Subsystem enthalten sind (LUNs werden nicht angezeigt) und die Beziehungen zwischen ihnen.

![Diagramm, das ein Subsystem zeigt, das mit "Ports" auf der linken Seite beginnt, zu "Controllern" und dann zu einem "Bus" mit "Slots" führt, der zu einzelnen Laufwerken führt.](images/vdssubsystem.png)

VDS-Anwendungen verwenden die [**IVdsHwProvider::QuerySubSystems-Methode**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems) zum Abfragen der Subsysteme, die zu einem bestimmten Hardwareanbieter gehören. Aufrufer können einen Zeiger auf ein bestimmtes Subsystem erhalten, indem sie das gewünschte Subsystemobjekt aus der -Enumeration auswählen, die von der **QuerySubSystems-Methode zurückgegeben** wird. Mit einem Subsystemobjekt können Sie den Subsystemstatus festlegen, LUNs erstellen, Laufwerke ersetzen und Controller, Laufwerke und LUNs abfragen.

Neben einem Objektbezeichner, einem Namen und einer Seriennummer enthalten Subsystemobjekteigenschaften den Subsystemstatus, die Integrität und flags. anzahl der Controller, Slots und Buslinien; und eine Neustellungsprioritätseinstellung.

In der folgenden Tabelle sind verwandte Schnittstellen, Enumerationen und Strukturen aufgeführt.



| type                                                                                      | Element                                                                                                                          |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| Schnittstellen, die von diesem Objekt immer verfügbar gemacht werden                                         | [**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem).                                                                                          |
| Schnittstellen, die von diesem Objekt immer nur in ISCSI-Anbietern der Version 1.1 und 2.0 verfügbar gemacht werden | [**IVdsSubSystemIscsi**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemiscsi) und [**IVdsSubSystemImportTarget**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemimporttarget).             |
| Schnittstellen, die von diesem Objekt verfügbar gemacht werden können                                             | [**IVdsSubSystemNaming**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemnaming) und [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance).                               |
| Zugeordnete Enumerationen                                                                   | [**VDS \_ \_ \_ SUBSYSTEMFLAG**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_flag) und [**VDS \_ SUB SYSTEM \_ \_ STATUS**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_status).             |
| Zugeordnete Strukturen                                                                     | [**VDS \_ SUBSYSTEM \_ \_ PROP UND**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_prop) [**VDS SUB SYSTEM \_ \_ \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification). |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hardwareanbieterobjekte](hardware-provider-objects.md)
</dt> <dt>

[**IVdsHwProvider::QuerySubSystems**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems)
</dt> </dl>

 

 
