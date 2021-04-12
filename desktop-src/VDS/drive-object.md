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
# <a name="drive-object"></a>Laufwerks Objekt

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Ein Laufwerks Objekt modelliert ein physisches Laufwerk, das in einem Subsystem enthalten ist. Jedes Laufwerk stellt eine Verbindung mit einem Bus her, belegt einen Slot und enthält eine Reihe von Laufwerks Blöcken. Jedes Laufwerk kann zu einer beliebigen Anzahl von LUNs beitragen. Ein Laufwerk kann auch als Hot Spare festgelegt werden.

Verwenden Sie die [**ivdssubsystem:: querydrives**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives) -Methode, um die Laufwerke zu ermitteln, die in einem bestimmten Subsystem enthalten sind. Aufrufer können einen Zeiger auf ein bestimmtes Laufwerk abrufen, indem Sie das gewünschte Laufwerks Objekt aus der-Enumeration auswählen, das von der **querydrives** -Methode zurückgegeben wird, oder indem Sie die [**ivdssubsystem:: GetDrive**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive) -Methode aufrufen und die gewünschte Busnummer und Slot-Nummer übergeben. Mit einem Laufwerks Objekt können Sie den Laufwerks Status und die Abfrage für Laufwerks Eigenschaften, zugeordnete Laufwerks Blöcke und das Subsystem, das das Laufwerk enthält, festlegen.

Zusätzlich zu einem Objekt Bezeichner, einem Namen und einer Seriennummer enthalten die Eigenschaften des Laufwerks Objekt den Status, den Zustand und die Flags des Laufwerks. die Größe in Bytes. und eine Bus-und Slot-Nummer.

In der folgenden Tabelle werden verwandte Schnittstellen, Enumerationen und Strukturen aufgelistet.



| type                                              | Element                                                                                                                                         |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Schnittstellen, die von diesem Objekt immer verfügbar gemacht werden | [**Ivdsdrive**](/windows/desktop/api/Vds/nn-vds-ivdsdrive)                                                                                                                  |
| Schnittstellen, die von diesem Objekt verfügbar gemacht werden können     | [**Ivdsmaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)                                                                                                      |
| Zugehörige Enumerationen                           | [**VDS \_ \_Laufwerkflag**](/windows/desktop/api/Vds/ne-vds-vds_drive_flag), [**VDS- \_ Laufwerks \_ Status**](/windows/desktop/api/Vds/ne-vds-vds_drive_status)und [**VDS- \_ Laufwerks \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_extent)Block. |
| Zugeordnete Strukturen                             | [**VDS \_ Laufwerk- \_ Prop**](/windows/desktop/api/Vds/ns-vds-vds_drive_prop) -und [**VDS- \_ Laufwerk \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification).                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hardware Anbieter Objekte](hardware-provider-objects.md)
</dt> <dt>

[**Ivdssubsystem:: querydrives**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives)
</dt> <dt>

[**Ivdssubsystem:: GetDrive**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive)
</dt> </dl>

 

 
