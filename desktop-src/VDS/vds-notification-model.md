---
description: VDS-Benachrichtigungen
ms.assetid: a0841215-3eb0-4769-b320-4da25b535362
title: VDS-Benachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa99751912f110a77b061d50134135413baf2894
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "104551814"
---
# <a name="vds-notifications"></a>VDS-Benachrichtigungen

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Ein Anbieter kann eine Ereignis Benachrichtigung an VDS senden, und VDS kann die Benachrichtigung wiederum an Anwendungen weiterleiten. Das von VDS verwendete Benachrichtigungs Modell ähnelt dem Verbindungspunkt Modell, das von COM-Objekten verwendet wird.

VDS generiert Dienst Benachrichtigungen für Ereignisse wie z. b. eine Laufwerk Buchstaben Zuweisung oder die Ankunft eines nicht zugeordneten Datenträgers. Wenn VDS einen Datenträger einem Anbieter zuordnet, ist der Anbieter für die Erstellung der zugehörigen Benachrichtigungen verantwortlich. Die folgende Abbildung zeigt die im VDS-Benachrichtigungs Modell verwendeten Schnittstellen und Methoden.

![Diagramm, das die Schnittstelle und Methoden (Empfehlung, OnLoad und OnNotify) zwischen Anwendungen, Virtual Disk Service und V D S-Anbietern anzeigt.](images/vdsnotification.png)

Um Benachrichtigungen zu empfangen, registriert VDS seine [**ivdsadvisesink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink) -Schnittstelle beim Anbieter Objekt, indem er die [**ivdsproviderprivate:: OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload) -Methode aufrufen und einen Zeiger auf die-Schnittstelle übergibt. Wenn ein Benachrichtigungs Ereignis auftritt, z. b. die Ankunft eines neuen Volumes oder Laufwerks, übergibt der Anbieter die entsprechende Benachrichtigungs Struktur als [**ivdsadvisesink:: OnNotify**](/windows/desktop/api/Vds/nf-vds-ivdsadvisesink-onnotify) -Methoden Parameter an VDS.

Der Prozess ähnelt der Anwendung und den VDS. Um Benachrichtigungen zu empfangen, registriert eine Anwendung Ihre [**ivdsadvisesink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink) -Schnittstelle in VDS, indem Sie die [**ivdsservice:: Empfehlung**](/windows/desktop/api/Vds/nf-vds-ivdsservice-advise) -Methode aufrufen und einen Zeiger auf die-Schnittstelle übergibt. Wenn VDS eine Benachrichtigung von einem Anbieter empfängt, übergibt er die entsprechende Benachrichtigungs Struktur an registrierte Anwendungen als [**ivdsadvisesink:: OnNotify**](/windows/desktop/api/Vds/nf-vds-ivdsadvisesink-onnotify) -Methoden Parameter.

> [!Note]  
> Eine Anwendung, die " [**Empfehlung**](/windows/desktop/api/Vds/nf-vds-ivdsservice-advise) " aufruft, muss letztendlich die [**ivdsservice:: unempfehlung**](/windows/desktop/api/Vds/nf-vds-ivdsservice-unadvise) -Methode aufrufen. Im Idealfall sollte Sie **Unrat** anrufen, sobald Sie keine Benachrichtigungen mehr empfangen muss.

 

In der folgenden Tabelle sind die vom Anbieter generierten Benachrichtigungen nach Objekttyp aufgeführt.



| Object     | Benachrichtigung                              | Wert | Verknüpfung mit Ereignis Beschreibung                                             |
|------------|-------------------------------------------|-------|-----------------------------------------------------------------------|
| Pack       | **VDS \_ NF \_ Pack \_ eintreffen**                 | 1     | [**VDS- \_ Paket \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification)              |
| Pack       | **VDS \_ NF \_ Pack wird \_ abgefährt**                 | 2     | [**VDS- \_ Paket \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification)              |
| Pack       | **VDS \_ NF \_ Pack \_ ändern**                 | 3     | [**VDS- \_ Paket \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification)              |
| Lautstärke     | **VDS- \_ NF- \_ Volume \_ ankommt**               | 4     | [**VDS- \_ Volumen \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Lautstärke     | **VDS-Laufwerk mit \_ NF- \_ Volume \_**               | 5     | [**VDS- \_ Volumen \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Lautstärke     | **VDS- \_ NF- \_ Volume \_ ändern**               | 6     | [**VDS- \_ Volumen \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Lautstärke     | **\_ \_ \_ \_ Fortschritt der VDS-NF-Volumen Erstellung** | 7     | [**VDS- \_ Volumen \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Datenträger       | **VDS-NF-Datenträger \_ \_ \_ Ankunft**                 | 8     | [**VDS-Datenträger \_ \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)              |
| Datenträger       | **VDS-NF-Datenträger \_ \_ \_**                 | 9     | [**VDS-Datenträger \_ \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)              |
| Datenträger       | **VDS \_ NF \_ Disk \_ Modify**                 | 10    | [**VDS-Datenträger \_ \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)              |
| Partition  | **VDS- \_ NF- \_ Partition \_ eintreffen**            | 11    | [**VDS- \_ Partitions \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_partition_notification)    |
| Partition  | **VDS \_ NF- \_ Partition wird \_ abgefährt**            | 12    | [**VDS- \_ Partitions \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_partition_notification)    |
| Partition  | **Änderung der VDS- \_ NF- \_ Partition \_**            | 13    | [**VDS- \_ Partitions \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_partition_notification)    |
| Subsystem  | **VDS \_ NF- \_ unter \_ System \_ Ankunft**          | 101   | [**VDS- \_ unter \_ System \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification) |
| Subsystem  | **VDS \_ NF \_ - \_ Subsystem wird \_ abgefährt**          | 102   | [**VDS- \_ unter \_ System \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification) |
| Subsystem  | **Änderung des VDS \_ NF- \_ \_ Subsystems \_**          | 151   | [**VDS- \_ unter \_ System \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification) |
| Controller | **VDS- \_ NF- \_ Controller \_ eintreffen**           | 103   | [**VDS- \_ Controller \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Controller | **VDS- \_ NF- \_ Controller wird von \_**           | 104   | [**VDS- \_ Controller \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Controller | **Ändern des VDS- \_ NF- \_ Controllers \_**           | 350   | [**VDS- \_ Controller \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Controller | **VDS- \_ NF- \_ Controller \_ entfernt**          | 351   | [**VDS- \_ Controller \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Port       | **Änderung des VDS- \_ NF- \_ Ports \_**                 | 352   | [**VDS- \_ Port \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)              |
| Port       | **VDS- \_ NF- \_ Port \_ entfernt**                | 353   | [**VDS- \_ Port \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)              |
| Laufwerk      | **VDS \_ NF- \_ Laufwerk \_ eintreffen**                | 105   | [**VDS- \_ Laufwerk \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| Laufwerk      | **VDS \_ NF- \_ Laufwerk wird \_ abgefährt**                | 106   | [**VDS- \_ Laufwerk \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| Laufwerk      | **VDS \_ NF- \_ Laufwerk \_ ändern**                | 107   | [**VDS- \_ Laufwerk \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| Laufwerk      | **VDS- \_ Laufwerk "NF" \_ \_ entfernt**               | 354   | [**VDS- \_ Laufwerk \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| LUN        | **VDS \_ NF- \_ LUN \_ eintreffen**                  | 108   | [**VDS- \_ LUN- \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                |
| LUN        | **VDS \_ NF- \_ LUN wird entfernt \_**                  | 109   | [**VDS- \_ LUN- \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                |
| LUN        | **VDS \_ NF- \_ LUN \_ ändern**                  | 110   | [**VDS- \_ LUN- \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                |



 

Die verbleibenden Benachrichtigungen werden von VDS generiert. In der folgenden Tabelle werden Dienst basierte Benachrichtigungs Konstanten nach Kategorie aufgelistet.



| Category     | Benachrichtigung                                | Wert | Verknüpfung mit Ereignis Beschreibung                                                 |
|--------------|---------------------------------------------|-------|---------------------------------------------------------------------------|
| Datenträger         | **VDS-NF-Datenträger \_ \_ \_ Ankunft**                   | 8     | [**VDS-Datenträger \_ \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)                  |
| Datenträger         | **VDS-NF-Datenträger \_ \_ \_**                   | 9     | [**VDS-Datenträger \_ \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)                  |
| Datenträger         | **VDS \_ NF \_ Disk \_ Modify**                   | 10    | [**VDS-Datenträger \_ \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)                  |
| Laufwerkbuchstabe | **VDS \_ NF \_ Laufwerk \_ Buchstabe \_ frei**            | 201   | [**VDS- \_ Laufwerk \_ Buchstaben \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_drive_letter_notification) |
| Laufwerkbuchstabe | **VDS \_ NF \_ Laufwerk \_ Buchstabe \_ zuweisen**          | 202   | [**VDS- \_ Laufwerk \_ Buchstaben \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_drive_letter_notification) |
| Dateisystem  | **Ändern des VDS- \_ NF- \_ Datei \_ Systems \_**           | 203   | [**VDS- \_ Datei \_ System \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_file_system_notification)   |
| Dateisystem  | **Status des VDS- \_ NF- \_ Datei \_ System \_ Formats \_** | 204   | [**VDS- \_ Datei \_ System \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_file_system_notification)   |
| Lautstärke       | **Änderung der VDS \_ NF-Einstellungspunkte \_ \_ \_**          | 205   | [**VDS \_ - \_ einstellungspunktbenachrichtigung \_**](/windows/desktop/api/Vds/ns-vds-vds_mount_point_notification)   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[VDS-Objektmodell](vds-object-model.md)
</dt> <dt>

[**Ivdsadvisesink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink)
</dt> <dt>

[**Ivdsadvisesink:: OnNotify**](/windows/desktop/api/Vds/nf-vds-ivdsadvisesink-onnotify)
</dt> <dt>

[**Ivdsproviderprivate:: OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload)
</dt> <dt>

[**Ivdsservice:: Empfehlung**](/windows/desktop/api/Vds/nf-vds-ivdsservice-advise)
</dt> </dl>

 

 
