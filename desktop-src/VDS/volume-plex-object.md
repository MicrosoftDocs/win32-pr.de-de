---
description: Volume Plex-Objekt
ms.assetid: 9e770bfc-2bcb-45f0-a7fc-ba526349839e
title: Volume Plex-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54a858bc6ce98761bb687e8dca473b1b68879da8
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "104350889"
---
# <a name="volume-plex-object"></a>Volume Plex-Objekt

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Ein Volume-Plex-Objekt modelliert ein Volume Plex, das in einem Volume enthalten ist. Nur ein gespiegeltes Volume kann über mehrere plexes verfügen. alle anderen Volumetypen haben einen Plex. Jeder Plex enthält eine Kopie der Daten auf dem Volume. VDS unterstützt vier volumeplex-Typen: einfach, überspannt, Stripeset und Stripeset mit Parität. Eine Beschreibung der einzelnen Volumetypen finden Sie im Volume- [Objekt](volume-object.md).

Es gibt zwei Möglichkeiten, ein Volume mit mehreren plexes zu erstellen. Sie können die [**ivdspack:: kreatevolume**](/windows/desktop/api/Vds/nf-vds-ivdspack-createvolume) -Methode verwenden, um das gespiegelte Volume direkt zu erstellen. Sie können auch die [**ivdsvolume:: addplex**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-addplex) -Methode verwenden, um einem anderen Volume ein Volume hinzuzufügen. Die Volumes (und die zugrunde liegenden Datenträger) müssen sich im gleichen Paket befinden. Die folgende Abbildung zeigt ein Beispiel für das Hinzufügen eines Volumes (B) als Plex zu einem anderen Volume (a) und das resultierende Multiplex Volume (a). Die Daten auf Volume a bleiben intakt, während die Daten auf Volume B zu einer gespiegelten Kopie der Daten auf Volume a werden.

![Diagramm, das zwei einzelne plexe anzeigt, eine mit einfachem Volume a und eine mit einfachem Volume B, die mehreren plexes mit gespiegeltem Volume a entspricht.](images/vdsplex.png)

Sie können Volumeplexes Abfragen, indem Sie die [**ivdsvolume:: queryplexes**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-queryplexes) -Methode aufrufen. Sie können einen Zeiger auf einen bestimmten volumeplex abrufen, indem Sie das gewünschte Plex-Objekt aus der von **queryplexes** zurückgegebenen Enumeration auswählen. Mit Ausnahme des letzten Plex können vorhandene plexe beschädigt oder entfernt werden. Verwenden Sie [**ivdsvolume:: breakplex**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-breakplex) , um einen Plex von einem Volume aufzuteilen und das unterbrochene Plex-Objekt in ein Volumeobjekt zu konvertieren. Verwenden Sie [**ivdsvolume:: removeplex**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-removeplex) , um den Plex vollständig zu löschen. Sie können versuchen, einen fehlertoleranten Plex zu reparieren, indem Sie die [**ivdsvolumeplex:: Repair**](/windows/desktop/api/Vds/nf-vds-ivdsvolumeplex-repair) -Methode aufrufen, die ungültige Member zu guten Datenträgern verschiebt.

Zusätzlich zu einem Objekt Bezeichner und einem Plex-Typ enthalten die Eigenschaften des volumeplex-Objekts den Status, den Zustand und den Übergangsstatus des Plex. Dieses Objekt hat keine Flags.

In der folgenden Tabelle werden verwandte Schnittstellen, Enumerationen und Strukturen aufgelistet.



| type                                              | Element                                                                                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schnittstellen, die von diesem Objekt immer verfügbar gemacht werden | [**Ivdsvolumeplex**](/windows/desktop/api/Vds/nn-vds-ivdsvolumeplex).                                                                                                                                          |
| Zugehörige Enumerationen                           | [**VDS \_ \_ \_ Status des volumeplex**](/windows/desktop/api/Vds/ne-vds-vds_volume_plex_status), VDS-Laufwerks- [**\_ \_ Plex- \_ Typ**](/windows/desktop/api/Vds/ne-vds-vds_volume_plex_type)und VDS-Datenträger [**\_ \_ \_ Typen**](/windows/desktop/api/Vds/ne-vds-vds_disk_extent_type). |
| Zugeordnete Strukturen                             | [**VDS \_ Volume \_ Plex- \_ Prop**](/windows/desktop/api/Vds/ns-vds-vds_volume_plex_prop).                                                                                                                           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Software Anbieter Objekte](software-provider-objects.md)
</dt> <dt>

[Volume-Objekt](volume-object.md)
</dt> </dl>

 

 
