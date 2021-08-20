---
description: LUN-Objekt
ms.assetid: ea22bd6d-4a7a-4674-82e9-08460914ff8e
title: LUN-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d315e33b8d253e346b42b01f86a85379aadace73e517a169cc653214a9c674d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118347491"
---
# <a name="lun-object"></a>LUN-Objekt

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [Virtual Disk Service](virtual-disk-service-portal.md) durch die Windows Storage Verwaltungs-API. [](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

Ein LUN-Objekt (logische Einheitennummer) modelliert eine logische Einheit von adressierbarem Speicherplatz, die von einem Hardwareanbieter erstellt und von einem Subsystem zur Verfügung steht. Jede LUN besteht aus mindestens einem LUN-Plex, der wiederum aus Ausdrungen von einem oder mehreren Laufwerken besteht.

## <a name="lun-types"></a>LUN-Typen

VDS unterstützt fünf LUN-Typen: einfach, spanned, striped, mirrored und striped mit Parität. Einfache, übergreifende und Striping-LUNs sind nicht fehlertolerant. Gespiegelte und Paritäts-LUNs sind fehlertolerant. Im restlichen Teil dieses Abschnitts werden die einzelnen VDS-LUN-Typen beschrieben.

-   Bei einer einfachen LUN handelt es sich um eine nicht fehlertolerante LUN, die aus einem einzelnen zusammenhängenden Laufwerksdeut von einem einzelnen Laufwerk besteht. Der zusammenhängende Block kann aus einem einzelnen Bereich von Blöcken oder mehreren Bereichen von Blöcken bestehen, die miteinander verknüpft sind.
-   Eine übergreifende LUN ist eine nicht fehlertolerante LUN, die aus mehreren unzusammenhängenden Ausdrungen von mehreren Laufwerken besteht. Die Daten werden linear in jeden Derdungseinheiten auf dem ersten Laufwerk geschrieben, bis alle ersten Laufwerkseinheiten gefüllt sind, und dann in jeden der Aufdungseinheiten auf dem zweiten Laufwerk und so weiter. Übergreifende LUNs ermöglichen eine effiziente Nutzung des Laufwerkspeicherplatzes in Subsystemen, die Laufwerke verschiedener Größen umfassen.
-   Eine Striping-LUN ist eine nicht fehlertolerante LUN, die aus mehreren, überlappten, zusammenhängenden Ausdrundungen von mehreren Laufwerken besteht. Striping-LUNs verwenden eine RAID-0-Konfiguration, damit Daten zyklisch über die Dweiten auf den beitragenden Laufwerken "gestreift" werden. Striping-LUNs funktionieren am besten mit Laufwerken der gleichen Größe, desselben Modells und desselben Herstellers.
-   Gespiegelte LUNs sind fehlertolerante LUNs, die eine Notfallwiederherstellung ermöglichen, indem die Daten auf mehrere LUN-Plexe dupliziert werden. Jeder Plex in einer gespiegelten LUN enthält eine Kopie der Daten, die auf dem ursprünglichen Plex gespeichert sind. Jede der Plexes befindet sich auf einem separaten Laufwerk. Alle Daten, die in eine gespiegelte LUN geschrieben werden, werden gleichzeitig auf die einzelnen Plexes geschrieben. Wenn eines der beitragenden Laufwerke ausfällt, ist der Plex auf diesem Laufwerk nicht mehr verfügbar, aber das System arbeitet weiterhin mit den nicht betroffenen Plexen oder Plexes. Eine gespiegelte LUN kann eine beliebige Anzahl von Plexes haben.
-   Striping mit Paritäts-LUNs sind fehlertolerante LUNs, die für die Notfallwiederherstellung sorgen, indem Paritätsdaten zeitweilig auf drei oder mehr Laufwerken entfernt werden. Wenn eines der beitragenden Laufwerke ausfällt, können die verloren gegangenen Daten aus den verbleibenden Daten und der Parität neu erstellt werden.

## <a name="lun-creation"></a>LUN-Erstellung

VDS unterstützt vier Modelle, mit denen Anwendungen LUNs erstellen können: explizit gerichtet, teilweise gerichtet, automagisch und herstellerspezifisch. Alle Hardwareanbieter müssen die explizite und teilweise gerichtete LUN-Erstellung unterstützen. Es wird dringend empfohlen, die automatische LUN-Erstellung zu unterstützen. (Die herstellerspezifische LUN-Erstellung wird in diesem Leitfaden nicht bereitgestellt.)

Durch die explizite LuN-Erstellung kann der Aufrufer alle Attribute der LUN angeben. Die teilweise gerichtete LUN-Erstellung ermöglicht es dem Aufrufer, nur die Attribute anzugeben, die von besonderem Interesse sind, und dem Anbieter dann die Auswahl des Rests zu ermöglichen. Bei der automatischen LUN-Erstellung kann der Aufrufer einfach den LUN-Typ und die Größe zusammen mit einem Satz von "automatischen Hinweisen" (vordefinierte Einstellungen für LUN-Attribute) angeben und dem Anbieter dann ermöglichen, die LUN automatisch zu erstellen.

## <a name="lun-masking"></a>LUN-Masking

VDS unterstützt die LUN-Entmaskung für Subsysteme, die diese Funktion bieten. Alle LUNs werden auf dem Computer, auf dem der Anbieter ausgeführt wird, zur Oberfläche. Durch die Entmaskung der LUN kann ein Aufrufer ausgewählte LUNs für andere Computer im Netzwerk "entmasken". Wenn Sie eine LUN für einen Computer entmasken, hat der Computer Zugriff auf die LUN. Computer, für die eine LUN maskiert ist, tun dies nicht.

Eine nicht maskierte LUN macht sowohl die [**IVdsLun-**](/windows/desktop/api/Vds/nn-vds-ivdslun) als auch [**die IVdsDisk-Schnittstelle**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) für den lokalen Host verfügbar. Mit **IVdsDisk** können Sie einem Softwareanbieterpaket eine LUN hinzufügen, Volumes erstellen und entfernen, Laufwerkbuchstaben zuweisen und so weiter. Weitere Informationen zu den Vorgängen, die auf einem Datenträger ausgeführt werden, finden Sie unter [Disk Object](disk-object.md).

Nachdem eine LUN für einen Zielcomputer maskiert oder von einem Zielcomputer maskiert wurde, ändert sich die Sichtbarkeit der LUN auf diesem Computer möglicherweise erst, wenn ein bus-Rescan durchgeführt wird. Die VDS-Anwendung auf dem Zielcomputer initiiert den erneuten Scan des Bus durch Aufrufen von [**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate). Das Initiieren des erneuten Einscannens des Bus liegt in der Verantwortung der VDS-Anwendung, nicht des Hardwareanbieters.

## <a name="lun-multipathing"></a>LUN-Multipfad

Hardwareanbieter, die Multipfad-E/A (MPIO) unterstützen, können Lastenausgleichsrichtlinien für Pfade zwischen einer LUN und dem lokalen Host festlegen. LUNs, die diese Funktion unterstützen, machen die [**IVdsLunMpio-Schnittstelle**](/windows/desktop/api/Vds/nn-vds-ivdslunmpio) für den lokalen Host verfügbar.

## <a name="working-with-luns"></a>Arbeiten mit LUNs

Verwenden Sie [**die IVdsSubSystem::CreateLun-Methode,**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-createlun) um ein neues LUN-Objekt zu erstellen. Sie können die LUNs abfragen, die von einem bestimmten Subsystem angezeigt werden, indem Sie die [**QueryLuns-Methode**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-queryluns) aufrufen, die auch von [**IVdsSubSystem verfügbar gemacht wird.**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem) Ein Aufrufer kann einen Zeiger auf eine bestimmte LUN erhalten, indem er das gewünschte LUN-Objekt aus der -Enumeration auswählt, die von **QueryLuns zurückgegeben wird.** Mit einem LUN-Objekt können Sie den LUN-Status festlegen. Abfrage für alle aktiven Controller, Plexes und automagic-Hinweise; Erweitern und Verkleinern der LUN; Plexes hinzufügen und entfernen; Masken festlegen; Hinweise anwenden; und löschen Sie die LUN.

Neben einem Objektbezeichner, einem Namen und einer Seriennummer enthalten lun-Objekteigenschaften den LUN-Typ, die Größe, den Status, die Integrität, den Übergangszustand und flags. eine Freimaurungsliste; und eine Neustellungsprioritätseinstellung.

In der folgenden Tabelle sind verwandte Schnittstellen, Enumerationen und Strukturen aufgeführt.



| Typ                                                                                              | Element                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schnittstellen, die von diesem Objekt immer verfügbar gemacht werden                                                 | [**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun)                                                                                                                                                                                                                                                                                          |
| Schnittstellen, die von diesem Objekt immer in VDS 1.1 und 2.0 verfügbar gemacht werden, Fibre Channel anbieter | [**IVdsLunControllerPorts**](/windows/desktop/api/Vds/nn-vds-ivdsluncontrollerports)                                                                                                                                                                                                                                                            |
| Schnittstellen, die von diesem Objekt immer nur in ISCSI-Anbietern der Version 1.1 und 2.0 verfügbar gemacht werden         | [**IVdsLunIscsi**](/windows/desktop/api/Vds/nn-vds-ivdsluniscsi)                                                                                                                                                                                                                                                                                |
| Schnittstellen, die von diesem Objekt verfügbar gemacht werden können\*                                                   | [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance), [**IVdsLunMpio**](/windows/desktop/api/Vds/nn-vds-ivdslunmpio), [**IVdsLunNaming**](/windows/desktop/api/Vds/nn-vds-ivdslunnaming)und IVdsLunNumber **Windows Server 2008, Windows Vista und Windows Server 2003:** Die [**IVdsLunNumber-Schnittstelle**](/windows/desktop/api/Vds/nn-vds-ivdslunnumber)wird nicht unterstützt. [](/windows/desktop/api/Vds/nn-vds-ivdslunnumber)<br/> |
| Zugeordnete Enumerationen                                                                           | [**VDS \_ \_LUN-FLAG**](/windows/desktop/api/Vds/ne-vds-vds_lun_flag) und [**\_ VDS-LUN-STATUS \_**](/windows/desktop/api/Vds/ne-vds-vds_lun_status)und [**VDS-LUN-TYP \_ \_**](/windows/desktop/api/Vds/ne-vds-vds_lun_type)                                                                                                                                                                                   |
| Zugeordnete Strukturen                                                                             | [**VDS \_ \_LUN-INFORMATIONEN,**](/windows/desktop/api/VdsLun/ns-vdslun-vds_lun_information) [**VDS \_ LUN \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_lun_prop)UND [**\_ VDS-LUN-BENACHRICHTIGUNG \_**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                                                                                                                                                            |



 

\*Weitere Schnittstellen [**(IVdsDisk),**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)die verfügbar gemacht werden, wenn die LUN als Datenträger auf dem lokalen Hostcomputer entmaskiert wird, finden Sie unter [Datenträgerobjekt.](disk-object.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hardwareanbieterobjekte](hardware-provider-objects.md)
</dt> <dt>

[Pack-Objekt](pack-object.md)
</dt> <dt>

[Datenträgerobjekt](disk-object.md)
</dt> <dt>

[**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun)
</dt> <dt>

[**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)
</dt> <dt>

[Hinzufügen eines Laufwerkbuchstabens zu einer LUN](adding-a-drive-letter-to-a-lun.md)
</dt> </dl>

 

