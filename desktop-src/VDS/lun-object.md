---
description: LUN-Objekt
ms.assetid: ea22bd6d-4a7a-4674-82e9-08460914ff8e
title: LUN-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad74fa65802adb1439360fb2fcdb423c642ef736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355428"
---
# <a name="lun-object"></a>LUN-Objekt

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Ein LUN-Objekt (Logical Unit Number) modelliert eine logische Einheit von adressier barem Speicherplatz, die von einem Hardware Anbieter erstellt und von einem Subsystem bereitgestellt wird. Jede LUN umfasst mindestens einen LUN-Plex, der wiederum aus Blöcken von einem oder mehreren Laufwerken besteht.

## <a name="lun-types"></a>LUN-Typen

VDS unterstützt fünf LUN-Typen: einfach, überspannt, Stripeset, gespiegelt und Stripeset mit Parität. Einfache, übergreifende und stripesetluns sind nicht fehlertolerant. gespiegelte und Paritäts-LUNs sind fehlertolerant. Im restlichen Teil dieses Abschnitts werden die einzelnen VDS-LUN-Typen beschrieben.

-   Eine einfache LUN ist eine nicht fehlertolerante LUN, die sich aus einem einzelnen zusammenhängenden Laufwerks Block von einem einzelnen Laufwerk zusammensetzt. Der zusammenhängende Block kann aus einem einzelnen Bereich von Blöcken oder mehreren Blöcken von Blöcken bestehen, die miteinander verknüpft sind.
-   Eine übergreifende LUN ist eine nicht fehlertolerante LUN, die aus mehreren nicht zusammenhängenden Blöcken von mehreren Laufwerken besteht. Die Daten werden linear in jeden der Blöcke auf dem ersten Laufwerk geschrieben, bis alle ersten Laufwerks Blöcke gefüllt sind, und dann zu jedem der Blöcke auf dem zweiten Laufwerk usw. Übergreifende LUNs bieten eine effiziente Verwendung des Laufwerks Platzes in Subsystemen, die aus verschiedenen Größen bestehen.
-   Eine stripesetlun ist eine nicht fehlertolerante LUN, die aus mehreren, verschachtelten und zusammenhängenden Blöcken von mehreren Laufwerken besteht. Für stripesetluns wird eine RAID-0-Konfiguration verwendet, sodass die Daten zyklisch auf die Blöcke auf den beteiligten Laufwerken verteilt werden. Stripesetluns funktionieren am besten mit Laufwerken derselben Größe, desselben Modells und Ihres Herstellers.
-   Gespiegelte LUNs sind fehlertolerante LUNs, die für die Notfall Wiederherstellung sorgen, indem Sie die Daten in mehreren LUN-plexes duplizieren. Jeder Plex in einer gespiegelten LUN enthält eine Kopie der Daten, die auf dem ursprünglichen Plex gespeichert werden. Alle plexes befinden sich auf einem separaten Laufwerk. Alle Daten, die in eine gespiegelte LUN geschrieben werden, werden gleichzeitig in alle zugehörigen plexes geschrieben. Wenn eines der Mitwirkenden Laufwerke ausfällt, ist der Plex auf diesem Laufwerk nicht mehr verfügbar, aber das System wird weiterhin mit dem nicht betroffenen Plex oder plexes betrieben. Eine gespiegelte LUN kann eine beliebige Anzahl von plexes aufweisen.
-   Ein Stripeset mit Paritäts-LUNs sind fehlertolerante LUNs, die eine Notfall Wiederherstellung ermöglichen, indem Paritäts Daten zeitweise auf drei oder mehr Laufwerke verteilt werden. Wenn eines der Mitwirkenden Laufwerke fehlschlägt, können die verlorenen Daten aus den verbleibenden Daten und der Parität neu erstellt werden.

## <a name="lun-creation"></a>LUN-Erstellung

VDS unterstützt vier Modelle, mit denen Anwendungen LUNs erstellen können: explizit gerichtet, teilweise gesteuert, automatisiert und Hersteller spezifisch. Alle Hardware Anbieter müssen explizit und teilweise gesteuerte LUN-Erstellung unterstützen, und es wird dringend empfohlen, die automatisierte LUN-Erstellung zu unterstützen. (Die herstellerspezifische LUN-Erstellung erfolgt außerhalb des Umfangs dieses Handbuchs.)

Mithilfe der explizit gerichteten LUN-Erstellung kann der Aufrufer alle Attribute der LUN angeben. Die teilweise gesteuerte LUN-Erstellung ermöglicht dem Aufrufer, nur die Attribute anzugeben, die von besonderem Interesse sind, und dem Anbieter dann die Auswahl der restlichen Attribute zu ermöglichen. Die Automatisierung der automatischen LUN umfasst das Aktivieren des Aufrufers, um einfach den LUN-Typ und die Größe zusammen mit einem Satz von "automagalen hinweisen" (vordefinierte Einstellungen für LUN-Attribute) anzugeben, und ermöglicht dem Anbieter dann die automatische Erstellung der LUN.

## <a name="lun-masking"></a>LUN-Masking

VDS unterstützt die LUN-Maskierung für Subsysteme, die diese Funktion anbieten. Alle LUNs werden auf dem Computer angezeigt, auf dem der Anbieter ausgeführt wird. Die LUN-Maskierung ermöglicht einem Aufrufer das Aufheben der Maskierung ausgewählter LUNs auf anderen Computern im Netzwerk. Wenn Sie eine LUN auf einem Computer aufheben, hat der Computer Zugriff auf die LUN. Computer, für die eine LUN maskiert ist, nicht.

Eine nicht maskierte LUN macht sowohl [**ivdslun**](/windows/desktop/api/Vds/nn-vds-ivdslun) -als auch [**ivdsdisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) -Schnittstellen für den lokalen Host verfügbar. Sie können **ivdsdisk** zum Hinzufügen einer LUN zu einem Softwareanbieter Paket, zum Erstellen und Entfernen von Volumes, zum Zuweisen von Laufwerk Buchstaben usw. verwenden. Weitere Informationen zu den auf einem Datenträger ausgeführten Vorgängen finden Sie unter Datenträger [Objekt](disk-object.md).

Nachdem eine LUN für einen Zielcomputer nicht maskiert oder von einem Zielcomputer maskiert wurde, ändert sich die Sichtbarkeit der LUN auf dem Computer möglicherweise erst, wenn eine busüberprüfung durchgeführt wird. Die VDS-Anwendung auf dem Zielcomputer initiiert die erneute busüberprüfung durch Aufrufen von [**ivdsservice:: REENUMERATE**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate). Die Initiierung des busneuscans ist die Verantwortung der VDS-Anwendung, nicht des Hardware Anbieters.

## <a name="lun-multipathing"></a>LUN Multipfad

Hardware Anbieter, die Multipfad-e/a (MPIO) unterstützen, können Richtlinien für den Lastenausgleich für Pfade zwischen einer LUN und dem lokalen Host festlegen. LUNs, die diese Funktion unterstützen, machen die [**ivdslunmpio**](/windows/desktop/api/Vds/nn-vds-ivdslunmpio) -Schnittstelle für den lokalen Host verfügbar.

## <a name="working-with-luns"></a>Arbeiten mit LUNs

Verwenden Sie die [**ivdssubsystem:: deatelun-**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-createlun) Methode, um ein neues LUN-Objekt zu erstellen. Sie können die LUNs Abfragen, die von einem bestimmten Subsystem angezeigt werden, indem Sie die [**queryluns**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-queryluns) -Methode aufrufen, die auch von [**ivdssubsystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem)verfügbar gemacht wird. Ein Aufrufer kann einen Zeiger auf eine bestimmte LUN abrufen, indem er das gewünschte LUN-Objekt aus der von **queryluns** zurückgegebenen Enumeration auswählt. Mit einem LUN-Objekt können Sie den LUN-Status festlegen. Abfragen für alle aktiven Controller, plexes und automagandeutungen Erweitern und Verkleinern der LUN Hinzufügen und Entfernen von plexes Masken festlegen; Anwenden von hinweisen und löschen Sie die LUN.

Neben einem Objekt Bezeichner, einem Namen und einer Seriennummer enthalten die LUN-Objekteigenschaften den LUN-Typ, die Größe, den Status, die Integrität, den Übergangsstatus und die Flags. eine Liste der Maskierungen; und eine Einstellung für die Neuerstellungs Priorität.

In der folgenden Tabelle werden verwandte Schnittstellen, Enumerationen und Strukturen aufgelistet.



| type                                                                                              | Element                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schnittstellen, die von diesem Objekt immer verfügbar gemacht werden                                                 | [**Ivdslun**](/windows/desktop/api/Vds/nn-vds-ivdslun)                                                                                                                                                                                                                                                                                          |
| Schnittstellen, die von diesem Objekt immer in VDS 1,1 und 2,0 Fibre Channel Anbietern verfügbar gemacht werden | [**Ivdsluncontrollerports**](/windows/desktop/api/Vds/nn-vds-ivdsluncontrollerports)                                                                                                                                                                                                                                                            |
| Schnittstellen, die von diesem Objekt immer nur in VDS 1,1-und 2,0-iSCSI-Anbietern verfügbar gemacht werden         | [**Ivdsluniscsi**](/windows/desktop/api/Vds/nn-vds-ivdsluniscsi)                                                                                                                                                                                                                                                                                |
| Schnittstellen, die von diesem Objekt verfügbar gemacht werden können\*                                                   | [**Ivdsmaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance), [**ivdslunmpio**](/windows/desktop/api/Vds/nn-vds-ivdslunmpio), [**ivdslunnaming**](/windows/desktop/api/Vds/nn-vds-ivdslunnaming)und [**ivdslunnumber**](/windows/desktop/api/Vds/nn-vds-ivdslunnumber)**Windows Server 2008, Windows Vista und Windows Server 2003:** die [**ivdslunnumber**](/windows/desktop/api/Vds/nn-vds-ivdslunnumber) -Schnittstelle wird nicht unterstützt.<br/> |
| Zugehörige Enumerationen                                                                           | [**VDS \_ LUN- \_ Flag**](/windows/desktop/api/Vds/ne-vds-vds_lun_flag) und [**VDS- \_ LUN- \_ Status**](/windows/desktop/api/Vds/ne-vds-vds_lun_status)und [**VDS- \_ LUN- \_ Typ**](/windows/desktop/api/Vds/ne-vds-vds_lun_type)                                                                                                                                                                                   |
| Zugeordnete Strukturen                                                                             | [**VDS \_ LUN- \_ Informationen**](/windows/desktop/api/VdsLun/ns-vdslun-vds_lun_information), [**VDS- \_ LUN-unter \_ Stützung**](/windows/desktop/api/Vds/ns-vds-vds_lun_prop)und [**VDS- \_ LUN- \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                                                                                                                                                            |



 

\* Weitere Informationen finden Sie unter [Disk Object](disk-object.md) for additional Interface ([**ivdsdisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)), das verfügbar gemacht wird, wenn die LUN als ein Datenträger auf dem lokalen Host Computer nicht maskiert ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hardware Anbieter Objekte](hardware-provider-objects.md)
</dt> <dt>

[Pack-Objekt](pack-object.md)
</dt> <dt>

[Disk-Objekt](disk-object.md)
</dt> <dt>

[**Ivdslun**](/windows/desktop/api/Vds/nn-vds-ivdslun)
</dt> <dt>

[**Ivdsdisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)
</dt> <dt>

[Hinzufügen eines Laufwerk Buchstabens zu einer LUN](adding-a-drive-letter-to-a-lun.md)
</dt> </dl>

 

