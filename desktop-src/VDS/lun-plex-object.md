---
description: LUN-Plex-Objekt
ms.assetid: db6eabaa-1b84-4613-ab2a-8d5904305e08
title: LUN-Plex-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df52b60bcbd23269d766435749b40b8c636361390359182a38a695ab6252a27f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999441"
---
# <a name="lun-plex-object"></a>LUN-Plex-Objekt

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [Virtual Disk Service](virtual-disk-service-portal.md) durch die [Windows Storage Verwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Ein LUN-Plexobjekt modelliert ein LUN-Plex, das in einer LUN enthalten ist. Nur eine gespiegelte LUN kann mehrere Plexes aufweisen. alle anderen LUN-Typen verfügen über einen Plex. Jedes Plex enthält eine Kopie der Daten auf der LUN. Einer LUN können neue Plexes hinzugefügt werden, und mit Ausnahme des ursprünglichen Plexs können vorhandene Plexes entfernt werden. VDS unterstützt vier LUN-Plex-Typen: einfach, übergreifend, gestreift und gestreift mit Parität. Eine Beschreibung der einzelnen LUN-Typen finden Sie im [LUN-Objekt](lun-object.md).

Verwenden Sie die [**IVdsLun::AddPlex-Methode,**](/windows/desktop/api/Vds/nf-vds-ivdslun-addplex) um einer LUN ein Plex hinzuzufügen, und die [**IVdsLun::RemovePlex-Methode,**](/windows/desktop/api/Vds/nf-vds-ivdslun-removeplex) um das Plex zu löschen. Sie können LUN-Plexes abfragen, indem Sie die [**IVdsLun::QueryPlexes-Methode**](/windows/desktop/api/Vds/nf-vds-ivdslun-queryplexes) aufrufen. Sie können einen Zeiger auf ein bestimmtes LUN-Plex abrufen, indem Sie das gewünschte Plex-Objekt aus der Enumeration auswählen, die von der **QueryPlexes-Methode** zurückgegeben wird. Mit einem Plex-Objekt können Sie Laufwerks-Erweiterungen und Automagic-Hinweise abfragen und neue Hinweise anwenden.

Neben einem Objektbezeichner, einem Namen und einer Seriennummer enthalten lun-plex-Objekteigenschaften den Plextyp, die Größe, den Status, die Integrität, den Übergangszustand und flags. eine Nichtmaskungsliste und Stripegröße; und eine Einstellung für die Neuerstellungspriorität.

In der folgenden Tabelle sind verwandte Schnittstellen, Enumerationen und Strukturen aufgeführt.



| type                                              | Element                                                                                                                                                          |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schnittstellen, die immer von diesem Objekt verfügbar gemacht werden | [**IVdsLunPlex**](/windows/desktop/api/Vds/nn-vds-ivdslunplex).                                                                                                                              |
| Zugeordnete Enumerationen                           | [**VDS \_ LUN \_ PLEX \_ FLAG**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_flag), [**VDS \_ LUN \_ PLEX \_ STATUS**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_status)und [**VDS \_ LUN \_ PLEX \_ TYPE**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_type). |
| Zugeordnete Strukturen                             | [**VDS \_ LUN \_ PLEX \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_lun_plex_prop).                                                                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hardwareanbieterobjekte](hardware-provider-objects.md)
</dt> <dt>

[LUN-Objekt](lun-object.md)
</dt> </dl>

 

 
