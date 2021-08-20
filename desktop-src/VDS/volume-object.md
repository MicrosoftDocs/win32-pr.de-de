---
description: Volume-Objekt
ms.assetid: 92013015-b0f5-4b92-937b-c2637f65810c
title: Volume-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87887dae233a47ef168546bb4d0bab93389ab72e0e0617b64ea0c80fbfab0e83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125390"
---
# <a name="volume-object"></a>Volume-Objekt

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [Virtual Disk Service](virtual-disk-service-portal.md) durch die Windows Storage Verwaltungs-API. [](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

Ein Volumeobjekt modelliert eine logische Speichereinheit, die von einem Softwareanbieter erstellt und dem Dateisystem als Datenträger präsentiert wird. Jedes Volume besteht aus mindestens einem Volumeplex, das wiederum aus Dendungen von einem oder mehreren Datenträgern besteht.

## <a name="volume-types"></a>Volumetypen

VDS unterstützt fünf Volumetypen: einfach, übergreifend, gestreift, gespiegelt und mit Parität gestreift. Einfache, übergreifende und Stripingvolumes sind nicht fehlertolerant. Gespiegelte Volumes und Paritätsvolumes sind fehlertolerant. Im restlichen Teil dieses Abschnitts werden die einzelnen VDS-Volumetypen beschrieben.

-   Ein einfaches Volume ist ein Teil eines physischen Datenträgers, der so funktioniert, als wäre es eine physisch getrennte Einheit. Ein einfaches Volume kann aus einer einzelnen Region auf einem Datenträger oder mehreren Regionen desselben Datenträgers bestehen, die miteinander verknüpft sind.
-   Ein übergreifendes Volume kombiniert Bereiche mit nicht zugewiesenen Speicherplatz von mehreren Datenträgern zu einem logischen Volume, sodass Sie den gesamter Speicherplatz und alle Laufwerkbuchstaben auf einem System mit mehreren Datenträgern effizienter nutzen können.
-   Ein Striping-Volume wird erstellt, indem Bereiche mit freiem Speicherplatz auf mindestens zwei Datenträgern zu einem logischen Volume kombiniert werden. Stripesetvolumes verwenden RAID-0, wodurch Daten über mehrere Datenträger verteilt werden. Stripingvolumes können nicht erweitert oder gespiegelt werden und bieten keine Fehlertoleranz. Wenn einer der Datenträger mit einem Striping-Volume ausfällt, schlägt das gesamte Volume fehl. Beim Erstellen von Stripingvolumes ist es am besten, Datenträger der gleichen Größe, des gleichen Modells und desselben Herstellers zu verwenden.
-   Ein gespiegeltes Volume ist ein fehlertolerantes Volume, das Datenredundanz bietet, indem zwei Kopien oder Plexes des Volumes verwendet werden, um die auf dem Volume gespeicherten Daten zu duplizieren. Alle Daten, die auf das gespiegelte Volume geschrieben werden, werden auf beide Plexes geschrieben, die sich auf separaten physischen Datenträgern befinden. Wenn einer der physischen Datenträger ausfällt, sind die Daten auf dem ausgefallenen Datenträger nicht mehr verfügbar, aber das System wird weiterhin mit dem nicht betroffenen Datenträger betrieben.
-   Ein Striping mit Paritätsvolumen ist ein fehlertolerantes Volume mit Daten- und Paritätsstrips, die zeitweilig auf drei oder mehr physischen Datenträgern verteilt sind. Wenn ein Teil eines physischen Datenträgers ausfällt, können Sie die Daten, die sich im fehlerhaften Teil auf dem fehlerhaften Teil waren, aus den verbleibenden Daten und der Parität neu erstellen. Dieser Volumetyp (auch als RAID-5-Volume bezeichnet) ist eine gute Lösung für Datenredundanz in einer Computerumgebung, in der die meisten Aktivitäten aus dem Lesen von Daten bestehen.

### <a name="volume-creation"></a>Volumeerstellung

Einfache und dynamische Softwareanbieter unterstützen die teilweise gerichtete Volumeerstellung. Ein Aufrufer gibt nur die Attribute an, die von besonderem Interesse sind, und ermöglicht es dem Anbieter, den Rest zu wählen. VDS stellt ein neu erstelltes Volume automatisch mit Ausnahme der Plattformen Windows Server 2003, Enterprise Edition und Windows Server 2003, Datacenter Edition ein.

### <a name="working-with-volumes"></a>Arbeiten mit Volumes

Erstellen Sie immer ein Volume innerhalb desselben Pakets wie die Datenträger, die dazu beitragen. Verwenden Sie [**die IVdsPack::CreateVolume-Methode,**](/windows/desktop/api/Vds/nf-vds-ivdspack-createvolume) um ein neues Volumeobjekt zu erstellen. Sie können die Volumes bestimmen, die in einem bestimmten Paket enthalten sind, indem Sie die [**QueryVolumes-Methode**](/windows/desktop/api/Vds/nf-vds-ivdspack-queryvolumes) aufrufen, die auch von [**IVdsPack verfügbar gemacht wird.**](/windows/desktop/api/Vds/nn-vds-ivdspack) Ein Aufrufer kann einen Zeiger auf ein bestimmtes Volume erhalten, indem er das gewünschte Volumeobjekt aus der -Enumeration auswählt, die von **QueryVolumes zurückgegeben wird.** Mit einem Volumeobjekt können Sie den Status festlegen. Abfrage für Plexes; Erweitern und Verkleinern des Volumes; Plexes hinzufügen, umbrechen und entfernen; und löschen Sie das Volume.

Neben einem Objektbezeichner, einem Namen und einer Seriennummer enthalten Volumeobjekteigenschaften den Volumetyp, die Größe, den Status, die Integrität, den Übergangszustand, Flags und einen empfohlenen Dateisystemtyp.

In der folgenden Tabelle sind verwandte Schnittstellen, Enumerationen und Strukturen aufgeführt.



| Typ                                              | Element                                                                                                                                                                                                               |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schnittstellen, die von diesem Objekt immer verfügbar gemacht werden | [**IVdsVolume**](/windows/desktop/api/Vds/nn-vds-ivdsvolume), [**IVdsVolumeMF**](/windows/desktop/api/Vds/nn-vds-ivdsvolumemf), [**IVdsVolumeMF2**](/windows/desktop/api/Vds/nn-vds-ivdsvolumemf2) \* , [**IVdsVolumeOnline**](/windows/desktop/api/Vds/nn-vds-ivdsvolumeonline) \* und [**IVdsVolumeShrink**](/windows/desktop/api/Vds/nn-vds-ivdsvolumeshrink) \* . |
| Zugeordnete Enumerationen                           | [**VDS \_ \_VOLUMEFLAG,**](/windows/desktop/api/Vds/ne-vds-vds_volume_flag) [**VDS \_ VOLUME \_ STATUS,**](/windows/desktop/api/Vds/ne-vds-vds_volume_status) [**VDS \_ VOLUME \_ TYPE**](/windows/desktop/api/Vds/ne-vds-vds_volume_type)UND [**VDS DISK EXTENT \_ \_ \_ TYPE**](/windows/desktop/api/Vds/ne-vds-vds_disk_extent_type).            |
| Zugeordnete Strukturen                             | [**VDS \_ VOLUME \_ PROP-**](/windows/desktop/api/Vds/ns-vds-vds_volume_prop) und [**VDS-VOLUMEBENACHRICHTIGUNG. \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)                                                                                                        |



 

**\* Windows Server 2003: Diese** Schnittstellen werden erst nach der Windows Vista unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Softwareanbieterobjekte](software-provider-objects.md)
</dt> </dl>

 

 
