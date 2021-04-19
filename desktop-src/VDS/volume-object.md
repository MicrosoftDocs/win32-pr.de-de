---
description: Volume-Objekt
ms.assetid: 92013015-b0f5-4b92-937b-c2637f65810c
title: Volume-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e47092a237e7b0e9441b08c410d95d0836dbdb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366266"
---
# <a name="volume-object"></a>Volume-Objekt

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Ein Volume-Objekt modelliert eine logische Speichereinheit, die von einem Softwareanbieter erstellt und dem Dateisystem als Datenträger angezeigt wird. Jedes Volume umfasst mindestens ein Volume Plex, das wiederum aus Blöcken von einem oder mehreren Datenträgern besteht.

## <a name="volume-types"></a>Volumetypen

VDS unterstützt fünf Volumetypen: einfach, überspannt, Stripeset, gespiegelt und Stripeset mit Parität. Einfache, übergreifende und Stripesetvolumes sind nicht fehlertolerant. gespiegelte und Paritäts Volumes sind fehlertolerant. Im restlichen Teil dieses Abschnitts werden die einzelnen VDS-Volumetypen beschrieben.

-   Ein einfaches Volume ist ein Teil eines physischen Datenträgers, der so funktioniert, als ob es sich um eine physisch separate Einheit handelt. Ein einfaches Volume kann aus einer einzelnen Region auf einem Datenträger oder aus mehreren Regionen desselben Datenträgers bestehen, die miteinander verknüpft sind.
-   Ein übergreifendes Volume kombiniert Bereiche von nicht zugewiesener Speicherplatz von mehreren Datenträgern zu einem logischen Volume, sodass Sie den gesamten Speicherplatz und alle Laufwerk Buchstaben auf einem System mit mehreren Datenträgern effizienter nutzen können.
-   Ein Stripesetvolume wird erstellt, indem Bereiche mit freiem Speicherplatz auf zwei oder mehr Datenträgern in einem logischen Volume kombiniert werden. Stripesetvolumes verwenden RAID-0, das Daten auf mehrere Datenträger verteilt. Stripesetvolumes können nicht erweitert oder gespiegelt werden und bieten keine Fehlertoleranz. Wenn einer der Datenträger, die ein Stripesetvolume enthalten, fehlschlägt, schlägt das gesamte Volume fehl. Beim Erstellen von Stripesetvolumes empfiehlt es sich, Datenträger zu verwenden, die dieselbe Größe, dasselbe Modell und denselben Hersteller haben.
-   Ein gespiegeltes Volume ist ein fehlertolerantes Volume, das Datenredundanz bereitstellt, indem zwei Kopien oder plexe des Volumes zum Duplizieren der auf dem Volume gespeicherten Daten verwendet werden. Alle Daten, die auf das gespiegelte Volume geschrieben werden, werden in beide plexes geschrieben, die sich auf separaten physischen Datenträgern befinden. Wenn einer der physischen Datenträger ausfällt, sind die Daten auf dem fehlerhaften Datenträger nicht mehr verfügbar, das System wird jedoch weiterhin mit dem nicht betroffenen Datenträger betrieben.
-   Ein Stripeset mit Paritäts Volume ist ein fehlertolerantes Volume, bei dem Daten und Parität zeitweise auf drei oder mehr physischen Datenträgern verteilt sind. Wenn ein Teil eines physischen Datenträgers ausfällt, können Sie die Daten, die sich auf dem fehlerhaften Teil befunden haben, aus den verbleibenden Daten und der Parität neu erstellen. Dieser Volumentyp (auch als RAID-5-Volume bezeichnet) ist eine gute Lösung für die Datenredundanz in einer Computerumgebung, in der die meisten Aktivitäten das Lesen von Daten umfassen.

### <a name="volume-creation"></a>Volumeerstellung

Einfache und dynamische Softwareanbieter unterstützen eine teilweise gesteuerte Volumeerstellung. ein Aufrufer gibt nur die Attribute an, die von besonderem Interesse sind, und ermöglicht es dem Anbieter, den Rest auszuwählen. VDS stellt ein neu erstelltes Volume automatisch bereit, außer auf den Plattformen Windows Server 2003, Enterprise Edition und Windows Server 2003, Datacenter Edition.

### <a name="working-with-volumes"></a>Arbeiten mit Volumes

Erstellen Sie immer ein Volume innerhalb desselben Pakets wie die Datenträger, die dazu beitragen. Verwenden Sie die [**ivdspack:: kreatevolume**](/windows/desktop/api/Vds/nf-vds-ivdspack-createvolume) -Methode, um ein neues Volume-Objekt zu erstellen. Sie können die Volumes, die in einem bestimmten Paket enthalten sind, durch Aufrufen der [**queryvolumes**](/windows/desktop/api/Vds/nf-vds-ivdspack-queryvolumes) -Methode ermitteln, die ebenfalls von [**ivdspack**](/windows/desktop/api/Vds/nn-vds-ivdspack)verfügbar gemacht wird. Ein Aufrufer kann einen Zeiger auf ein bestimmtes Volume abrufen, indem er das gewünschte Volumeobjekt aus der von **queryvolumes** zurückgegebenen Enumeration auswählt. Mit einem Volumeobjekt können Sie den Status festlegen. Abfrage von plexes Erweitern und verkleinern Sie das Volume. Hinzufügen, unterbrechen und Entfernen von plexes und löschen Sie das Volume.

Zusätzlich zu einem Objekt Bezeichner, einem Namen und einer Seriennummer enthalten volumeobjekteigenschaften den Volumentyp, die Größe, den Status, die Integrität, den Übergangsstatus, Flags und einen empfohlenen Dateisystemtyp.

In der folgenden Tabelle werden verwandte Schnittstellen, Enumerationen und Strukturen aufgelistet.



| type                                              | Element                                                                                                                                                                                                               |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schnittstellen, die von diesem Objekt immer verfügbar gemacht werden | [**Ivdsvolume**](/windows/desktop/api/Vds/nn-vds-ivdsvolume), [**ivdsvolumemf**](/windows/desktop/api/Vds/nn-vds-ivdsvolumemf), [**IVdsVolumeMF2**](/windows/desktop/api/Vds/nn-vds-ivdsvolumemf2) \* , [**ivdsvolumeonline**](/windows/desktop/api/Vds/nn-vds-ivdsvolumeonline) \* und [**ivdsvolumeshrink**](/windows/desktop/api/Vds/nn-vds-ivdsvolumeshrink) \* . |
| Zugehörige Enumerationen                           | [**VDS \_ \_Volumeflag**](/windows/desktop/api/Vds/ne-vds-vds_volume_flag), [**VDS- \_ \_ Volumestatus**](/windows/desktop/api/Vds/ne-vds-vds_volume_status), [**VDS- \_ \_ Volumentyp**](/windows/desktop/api/Vds/ne-vds-vds_volume_type)und VDS-Datenträger Block- [**\_ \_ \_ Typ**](/windows/desktop/api/Vds/ne-vds-vds_disk_extent_type).            |
| Zugeordnete Strukturen                             | [**VDS \_ \_Volumeprop**](/windows/desktop/api/Vds/ns-vds-vds_volume_prop) -und [**VDS- \_ Volumen \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification).                                                                                                        |



 

**\* Windows Server 2003:** diese Schnittstellen werden bis Windows Vista nicht unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Software Anbieter Objekte](software-provider-objects.md)
</dt> </dl>

 

 
