---
description: VDS-Benachrichtigungen
ms.assetid: a0841215-3eb0-4769-b320-4da25b535362
title: VDS-Benachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 931731cc9c2b4aa73f7599c1fcbfad2f885bc74978ab15ba4e1efbf9d2a7522c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603112"
---
# <a name="vds-notifications"></a>VDS-Benachrichtigungen

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [Virtual Disk Service](virtual-disk-service-portal.md) durch die [Windows Storage Verwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Ein Anbieter kann eine Ereignisbenachrichtigung an VDS senden, und VDS kann die Benachrichtigung wiederum an Anwendungen weiterleiten. Das von VDS verwendete Benachrichtigungsmodell ähnelt dem Verbindungspunktmodell, das von COM-Objekten verwendet wird.

VDS generiert Dienstbenachrichtigungen für Ereignisse wie eine Laufwerkbuchstabenzuweisung oder den Eingang eines nicht zugeordneten Datenträgers. Sobald VDS einem Anbieter einen Datenträger zuordnet, ist der Anbieter für das Generieren der zugeordneten Benachrichtigungen verantwortlich. Die folgende Abbildung zeigt die Schnittstellen und Methoden, die im VDS-Benachrichtigungsmodell verwendet werden.

![Diagramm, das die Schnittstelle und die Methoden (Advise, OnLoad und OnNotify) zwischen Anwendungen, Virtual Disk Service und V D S-Anbietern zeigt.](images/vdsnotification.png)

Zum Empfangen von Benachrichtigungen registriert VDS seine [**IVdsAdviseSink-Schnittstelle**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink) beim Anbieterobjekt, indem die [**IVdsProviderPrivate::OnLoad-Methode**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload) aufgerufen und ein Zeiger an die Schnittstelle übergeben wird. Wenn ein Benachrichtigungsereignis auftritt, z. B. das Eintreffen eines neuen Volumes oder Laufwerks, übergibt der Anbieter die entsprechende Benachrichtigungsstruktur als [**IVdsAdviseSink::OnNotify-Methodenparameter**](/windows/desktop/api/Vds/nf-vds-ivdsadvisesink-onnotify) an VDS.

Der Prozess ist zwischen einer Anwendung und VDS ähnlich. Um Benachrichtigungen zu empfangen, registriert eine Anwendung ihre [**IVdsAdviseSink-Schnittstelle**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink) bei VDS, indem sie die [**IVdsService::Advise-Methode aufruft**](/windows/desktop/api/Vds/nf-vds-ivdsservice-advise) und einen Zeiger an die Schnittstelle übergibt. Wenn VDS eine Benachrichtigung von einem Anbieter empfängt, übergibt es die entsprechende Benachrichtigungsstruktur als [**IVdsAdviseSink::OnNotify-Methodenparameter**](/windows/desktop/api/Vds/nf-vds-ivdsadvisesink-onnotify) an registrierte Anwendungen.

> [!Note]  
> Eine Anwendung, die [**Advise aufruft,**](/windows/desktop/api/Vds/nf-vds-ivdsservice-advise) muss schließlich die [**IVdsService::Unadvise-Methode**](/windows/desktop/api/Vds/nf-vds-ivdsservice-unadvise) aufrufen. Im Idealfall sollte **unadvise** aufgerufen werden, sobald keine Benachrichtigungen mehr empfangen werden müssen.

 

In der folgenden Tabelle werden die vom Anbieter generierten Benachrichtigungen nach Objekttyp aufgelistet.



| Object     | Benachrichtigung                              | Wert | Link zur Ereignisbeschreibung                                             |
|------------|-------------------------------------------|-------|-----------------------------------------------------------------------|
| Pack       | **VDS \_ NF \_ PACK \_ ARRIVE**                 | 1     | [**VDS \_ \_ PACK-BENACHRICHTIGUNG**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification)              |
| Pack       | **VDS \_ NF \_ \_ PACK(EN)**                 | 2     | [**VDS \_ \_ PACK-BENACHRICHTIGUNG**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification)              |
| Pack       | **VDS \_ NF \_ PACK \_ MODIFY**                 | 3     | [**VDS \_ \_ PACK-BENACHRICHTIGUNG**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification)              |
| Volume     | **VDS \_ NF \_ VOLUME \_ ARRIVE**               | 4     | [**\_VDS-VOLUMEBENACHRICHTIGUNG \_**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Volume     | **VDS \_ NF VOLUME AUS DEM \_ \_ VOLUME**               | 5     | [**\_VDS-VOLUMEBENACHRICHTIGUNG \_**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Volume     | **VDS \_ NF \_ VOLUME \_ MODIFY**               | 6     | [**\_VDS-VOLUMEBENACHRICHTIGUNG \_**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Volume     | **VDS \_ NF \_ VOLUME \_ REBUILDING \_ PROGRESS** | 7     | [**\_VDS-VOLUMEBENACHRICHTIGUNG \_**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Datenträger       | **VDS \_ NF \_ DISK \_ ARRIVE**                 | 8     | [**VDS \_ DISK \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)              |
| Datenträger       | **VDS \_ NF \_ DISK \_ AUSWEICHEN**                 | 9     | [**VDS \_ DISK \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)              |
| Datenträger       | **VDS \_ NF \_ DISK \_ MODIFY**                 | 10    | [**VDS \_ DISK \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)              |
| Partition  | **VDS \_ NF \_ PARTITION \_ ARRIVE**            | 11    | [**\_VDS-PARTITIONSBENACHRICHTIGUNG \_**](/windows/desktop/api/Vds/ns-vds-vds_partition_notification)    |
| Partition  | **VDS \_ \_ NF-PARTITIONSABWANDERER \_**            | 12    | [**\_VDS-PARTITIONSBENACHRICHTIGUNG \_**](/windows/desktop/api/Vds/ns-vds-vds_partition_notification)    |
| Partition  | **VDS \_ NF \_ PARTITION \_ MODIFY**            | 13    | [**\_VDS-PARTITIONSBENACHRICHTIGUNG \_**](/windows/desktop/api/Vds/ns-vds-vds_partition_notification)    |
| Subsystem  | **VDS \_ NF \_ SUB \_ SYSTEM \_ ARRIVE**          | 101   | [**\_ \_ VDS-UNTERSYSTEMBENACHRICHTIGUNG \_**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification) |
| Subsystem  | **VDS \_ NF SUB SYSTEM AUS DEM \_ \_ \_ SYSTEM**          | 102   | [**\_ \_ VDS-UNTERSYSTEMBENACHRICHTIGUNG \_**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification) |
| Subsystem  | **VDS \_ NF \_ SUB \_ SYSTEM \_ MODIFY**          | 151   | [**\_ \_ VDS-UNTERSYSTEMBENACHRICHTIGUNG \_**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification) |
| Controller | **VDS \_ NF \_ CONTROLLER \_ ARRIVE**           | 103   | [**\_VDS-CONTROLLERBENACHRICHTIGUNG \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Controller | **VDS \_ NF \_ CONTROLLER \_ CONTROLLERS**           | 104   | [**\_VDS-CONTROLLERBENACHRICHTIGUNG \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Controller | **VDS \_ NF \_ CONTROLLER \_ MODIFY**           | 350   | [**\_VDS-CONTROLLERBENACHRICHTIGUNG \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Controller | **VDS \_ NF \_ CONTROLLER \_ ENTFERNT**          | 351   | [**\_VDS-CONTROLLERBENACHRICHTIGUNG \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Port       | **VDS \_ NF \_ PORT \_ MODIFY**                 | 352   | [**\_VDS-PORTBENACHRICHTIGUNG \_**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)              |
| Port       | **VDS \_ \_ NF-PORT \_ ENTFERNT**                | 353   | [**\_VDS-PORTBENACHRICHTIGUNG \_**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)              |
| Laufwerk      | **VDS \_ NF \_ DRIVE \_ ARRIVE**                | 105   | [**\_VDS-LAUFWERKBENACHRICHTIGUNG \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| Laufwerk      | **VDS \_ NF DRIVE AUS DEM \_ \_ LAUFWERK**                | 106   | [**\_VDS-LAUFWERKBENACHRICHTIGUNG \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| Laufwerk      | **VDS \_ NF \_ DRIVE \_ MODIFY**                | 107   | [**\_VDS-LAUFWERKBENACHRICHTIGUNG \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| Laufwerk      | **VDS \_ \_ NF-LAUFWERK \_ ENTFERNT**               | 354   | [**\_VDS-LAUFWERKBENACHRICHTIGUNG \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| LUN        | **VDS \_ NF \_ LUN \_ ARRIVE**                  | 108   | [**\_ \_ VDS-LUN-BENACHRICHTIGUNG**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                |
| LUN        | **VDS \_ NF \_ \_ LUNS**                  | 109   | [**\_ \_ VDS-LUN-BENACHRICHTIGUNG**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                |
| LUN        | **VDS \_ NF \_ LUN \_ MODIFY**                  | 110   | [**\_ \_ VDS-LUN-BENACHRICHTIGUNG**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                |



 

VDS generiert die verbleibenden Benachrichtigungen. In der folgenden Tabelle sind dienstbasierte Benachrichtigungskonstanten nach Kategorie aufgeführt.



| Category     | Benachrichtigung                                | Wert | Link zur Ereignisbeschreibung                                                 |
|--------------|---------------------------------------------|-------|---------------------------------------------------------------------------|
| Datenträger         | **VDS \_ NF \_ DISK \_ ARRIVE**                   | 8     | [**VDS \_ DISK \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)                  |
| Datenträger         | **VDS \_ NF \_ DISK \_ AUSWEICHEN**                   | 9     | [**VDS \_ DISK \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)                  |
| Datenträger         | **VDS \_ NF \_ DISK \_ MODIFY**                   | 10    | [**VDS \_ DISK \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)                  |
| Laufwerkbuchstabe | **VDS \_ NF \_ DRIVE \_ LETTER \_ FREE**            | 201   | [**\_ \_ VDS-LAUFWERKBUCHSTABENBENACHRICHTIGUNG \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_letter_notification) |
| Laufwerkbuchstabe | **VDS \_ \_ NF-LAUFWERKBUCHSTABE \_ \_ ZUWEISEN**          | 202   | [**\_ \_ VDS-LAUFWERKBUCHSTABENBENACHRICHTIGUNG \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_letter_notification) |
| Dateisystem  | **VDS \_ NF \_ FILE \_ SYSTEM \_ MODIFY**           | 203   | [**\_ \_ VDS-DATEISYSTEMBENACHRICHTIGUNG \_**](/windows/desktop/api/Vds/ns-vds-vds_file_system_notification)   |
| Dateisystem  | **STATUS DES VDS \_ \_ \_ NF-DATEISYSTEMFORMATS \_ \_** | 204   | [**\_ \_ VDS-DATEISYSTEMBENACHRICHTIGUNG \_**](/windows/desktop/api/Vds/ns-vds-vds_file_system_notification)   |
| Volume       | **ÄNDERUNG DER \_ VDS-NF-BEREITSTELLUNGSPUNKTE \_ \_ \_**          | 205   | [**\_ \_ VDS-BEREITSTELLUNGSPUNKTBENACHRICHTIGUNG \_**](/windows/desktop/api/Vds/ns-vds-vds_mount_point_notification)   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[VDS-Objektmodell](vds-object-model.md)
</dt> <dt>

[**IVdsAdviseSink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink)
</dt> <dt>

[**IVdsAdviseSink::OnNotify**](/windows/desktop/api/Vds/nf-vds-ivdsadvisesink-onnotify)
</dt> <dt>

[**IVdsProviderPrivate::OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload)
</dt> <dt>

[**IVdsService::Advise**](/windows/desktop/api/Vds/nf-vds-ivdsservice-advise)
</dt> </dl>

 

 
