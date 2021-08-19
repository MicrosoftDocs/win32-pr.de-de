---
description: Volume Plex-Objekt
ms.assetid: 9e770bfc-2bcb-45f0-a7fc-ba526349839e
title: Volume Plex-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c140cbf50e1939be7f62499aa90a299e07c157cd22b1a2e039e5e7bb2053b497
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603027"
---
# <a name="volume-plex-object"></a>Volume Plex-Objekt

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [Virtual Disk Service](virtual-disk-service-portal.md) durch die Windows Storage Verwaltungs-API. [](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

Ein Volumeplexobjekt modelliert einen Volumeplex, der in einem Volume enthalten ist. Nur ein gespiegeltes Volume kann mehrere Plexe haben. alle anderen Volumetypen verfügen über einen Plex. Jeder Plex enthält eine Kopie der Daten auf dem Volume. VDS unterstützt vier Volumeplex-Typen: einfach, übergreifend, gestreift und mit Parität gestreift. Eine Beschreibung der einzelnen Volumetypen finden Sie im [Volumeobjekt](volume-object.md).

Es gibt zwei Möglichkeiten, ein Volume mit mehreren Plexes zu erstellen. Sie können die [**IVdsPack::CreateVolume-Methode**](/windows/desktop/api/Vds/nf-vds-ivdspack-createvolume) verwenden, um das gespiegelte Volume direkt zu erstellen, oder die [**IVdsVolume::AddPlex-Methode**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-addplex) verwenden, um einem anderen Volume ein Volume hinzuzufügen. Die Volumes (und die zugrunde liegenden Datenträger) müssen sich im gleichen Paket enthalten. Die folgende Abbildung zeigt ein Beispiel für das Hinzufügen eines Volumes (B) als Plex zu einem anderen Volume (A) und des resultierenden multiplexierten Volumes (A). Die Daten auf Volume A bleiben intakt, während die Daten auf Volume B zu einer gespiegelten Kopie der Daten auf Volume A werden.

![Diagramm, das zwei einzelne Plexe zeigt, eine mit einfachem Volume A und eine mit einfachem Volume B, gleich mehreren Plexes mit gespiegelter Lautstärke A.](images/vdsplex.png)

Sie können Volumeplexes abfragen, indem Sie die [**IVdsVolume::QueryPlexes-Methode**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-queryplexes) aufrufen. Sie können einen Zeiger auf einen bestimmten Volumeplex erhalten, indem Sie das gewünschte Plex-Objekt aus der -Enumeration auswählen, die von **QueryPlexes zurückgegeben wird.** Mit Ausnahme des letzten Plexes können vorhandene Plexes beschädigt oder entfernt werden. Verwenden Sie [**IVdsVolume::BreakPlex,**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-breakplex) um einen Plex von einem Volume zu trennen und das unterbrochene Plex-Objekt in ein Volumeobjekt zu konvertieren. Verwenden Sie [**IVdsVolume::RemovePlex,**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-removeplex) um die Plex-Datei vollständig zu löschen. Sie können versuchen, einen fehlertoleranten Plex zu reparieren, indem Sie die [**IVdsVolumePlex::Repair-Methode**](/windows/desktop/api/Vds/nf-vds-ivdsvolumeplex-repair) aufrufen, die fehlerhafte Member auf gute Datenträger verschiebt.

Neben einem Objektbezeichner und einem Plextyp enthalten volumeplex-Objekteigenschaften den Status, die Integrität und den Übergangszustand des Plex. Dieses Objekt verfügt über keine Flags.

In der folgenden Tabelle sind verwandte Schnittstellen, Enumerationen und Strukturen aufgeführt.



| Typ                                              | Element                                                                                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schnittstellen, die von diesem Objekt immer verfügbar gemacht werden | [**IVdsVolumePlex**](/windows/desktop/api/Vds/nn-vds-ivdsvolumeplex).                                                                                                                                          |
| Zugeordnete Enumerationen                           | [**VDS \_ VOLUME \_ PLEX \_ STATUS**](/windows/desktop/api/Vds/ne-vds-vds_volume_plex_status), [**VDS \_ VOLUME \_ PLEX \_ TYPE**](/windows/desktop/api/Vds/ne-vds-vds_volume_plex_type)UND [**VDS DISK EXTENT \_ \_ \_ TYPE**](/windows/desktop/api/Vds/ne-vds-vds_disk_extent_type). |
| Zugeordnete Strukturen                             | [**VDS \_ VOLUME \_ PLEX \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_volume_plex_prop).                                                                                                                           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Softwareanbieterobjekte](software-provider-objects.md)
</dt> <dt>

[Volume-Objekt](volume-object.md)
</dt> </dl>

 

 
