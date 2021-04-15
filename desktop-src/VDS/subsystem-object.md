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
# <a name="subsystem-object"></a>Subsystem-Objekt

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Ein Subsystem-Objekt modelliert ein Speichersubsystem. Ein Subsystem ist entweder ein RAID-Gehäuse oder eine PCI-RAID-Karte. Ein einzelner Host Computer kann mit einer beliebigen Anzahl von Subsystemen verbunden werden. Jedes Subsystem wird von genau einem Hardware Anbieter verwaltet. In einer SAN-Konfiguration stellt die Subsystem-Klasse ein SAN-Speicher Gehäuse dar.

Ein Subsystem kann eine beliebige Anzahl von Controllern und Laufwerken enthalten und kann eine beliebige Anzahl von LUNs auf dem Computer, auf dem der Hardware Anbieter ausgeführt wird, aufheben (Aufheben der Maskierung). Die Maskierung von LUNs auf anderen Computern im Netzwerk kann von einem höheren Subsystem nicht durchführt werden. Jedes Laufwerk innerhalb eines Subsystems ist mit einem Bus verbunden und belegt einen Slot im Bus. Jeder Controller innerhalb eines Subsystems verfügt über einen oder mehrere Controller Anschlüsse.

Die folgende Abbildung zeigt die physischen Geräte, die in einem Subsystem enthalten sind (LUNs werden nicht angezeigt), und die Beziehungen zwischen Ihnen.

![Diagramm, das ein Subsystem anzeigt, das auf der linken Seite mit ' Ports ' beginnt, zu ' Controllers ' wechselt, und dann ein ' Bus ' mit ' Slots ', der zu einzelnen ' Drives ' führt.](images/vdssubsystem.png)

VDS-Anwendungen verwenden die [**ivdshwprovider:: querysubsystems**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems) -Methode, um die Subsysteme abzufragen, die zu einem bestimmten Hardware Anbieter gehören. Aufrufer können einen Zeiger auf ein bestimmtes Subsystem abrufen, indem Sie das gewünschte Subsystem-Objekt aus der-Enumeration auswählen, das von der **querysubsystems** -Methode zurückgegeben wird. Mit einem Subsystem-Objekt können Sie den Subsystem-Status festlegen, LUNs erstellen, Laufwerke ersetzen und Controller, Laufwerke und LUNs Abfragen.

Zusätzlich zu einem Objekt Bezeichner, einem Namen und einer Seriennummer enthalten subsystemobjekteigenschaften den Subsystem Status, den Zustand und die Flags. die Anzahl der Controller, Slots und Busse; und eine Einstellung für die Neuerstellungs Priorität.

In der folgenden Tabelle werden verwandte Schnittstellen, Enumerationen und Strukturen aufgelistet.



| type                                                                                      | Element                                                                                                                          |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| Schnittstellen, die von diesem Objekt immer verfügbar gemacht werden                                         | [**Ivdssubsystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem).                                                                                          |
| Schnittstellen, die von diesem Objekt immer nur in VDS 1,1-und 2,0-iSCSI-Anbietern verfügbar gemacht werden | [**Ivdssubsystemiscsi**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemiscsi) und [**ivdssubsystematimporttarget**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemimporttarget).             |
| Schnittstellen, die von diesem Objekt verfügbar gemacht werden können                                             | [**Ivdssubsystemnaming**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemnaming) und [**ivdsmaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance).                               |
| Zugehörige Enumerationen                                                                   | [**VDS \_ \_ \_ Subsystemflag**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_flag) und [**Status des VDS- \_ \_ Subsystems \_**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_status).             |
| Zugeordnete Strukturen                                                                     | [**VDS \_ Sub- \_ System- \_ Prop**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_prop) -und [**VDS- \_ unter \_ System \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification). |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hardware Anbieter Objekte](hardware-provider-objects.md)
</dt> <dt>

[**Ivdshwprovider:: querysubsystems**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems)
</dt> </dl>

 

 
