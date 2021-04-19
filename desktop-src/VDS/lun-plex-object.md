---
description: LUN-Plex-Objekt
ms.assetid: db6eabaa-1b84-4613-ab2a-8d5904305e08
title: LUN-Plex-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1b51657ccbfc0f1bd3d73e54128cac3f0b507c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353976"
---
# <a name="lun-plex-object"></a>LUN-Plex-Objekt

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Ein LUN-Plex-Objekt modelliert einen LUN-Plex, der in einer LUN enthalten ist. Nur eine gespiegelte LUN kann über mehrere plexes verfügen. alle anderen LUN-Typen haben einen Plex. Jeder Plex enthält eine Kopie der Daten auf der LUN. Neue plexe können einer LUN hinzugefügt werden, und mit Ausnahme des ursprünglichen Plex können vorhandene plexe entfernt werden. VDS unterstützt vier LUN-Plex-Typen: einfach, überspannt, Stripeset und Stripeset mit Parität. Eine Beschreibung dieser LUN-Typen finden Sie unter dem [LUN-Objekt](lun-object.md).

Verwenden Sie die [**ivdslun:: addplex**](/windows/desktop/api/Vds/nf-vds-ivdslun-addplex) -Methode, um einem LUN einen Plex und die [**ivdslun:: removeplex**](/windows/desktop/api/Vds/nf-vds-ivdslun-removeplex) -Methode hinzuzufügen, um den Plex zu löschen. Sie können LUN-plexes Abfragen, indem Sie die [**ivdslun:: queryplexes**](/windows/desktop/api/Vds/nf-vds-ivdslun-queryplexes) -Methode aufrufen. Sie können einen Zeiger auf einen bestimmten LUN-Plex abrufen, indem Sie das gewünschte Plex-Objekt aus der-Enumeration auswählen, die von der **queryplexes** -Methode zurückgegeben wird. Mit einem Plex-Objekt können Sie die Laufwerks Blöcke und automagandeutungen Abfragen und neue Hinweise anwenden.

Zusätzlich zu einem Objekt Bezeichner, einem Namen und einer Seriennummer enthalten die LUN-Plex-Objekteigenschaften den Plex-Typ, die Größe, den Status, die Integrität, den Übergangsstatus und die Flags. eine Liste der Maskierungen und die Stripesetgröße; und eine Einstellung für die Neuerstellungs Priorität.

In der folgenden Tabelle werden verwandte Schnittstellen, Enumerationen und Strukturen aufgelistet.



| type                                              | Element                                                                                                                                                          |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schnittstellen, die von diesem Objekt immer verfügbar gemacht werden | [**Ivdslunplex**](/windows/desktop/api/Vds/nn-vds-ivdslunplex).                                                                                                                              |
| Zugehörige Enumerationen                           | [**VDS \_ LUN \_ Plex- \_ Flag**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_flag), [**VDS- \_ LUN-Plex- \_ \_ Status**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_status)und [**VDS- \_ LUN-Plex- \_ \_ Typ**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_type). |
| Zugeordnete Strukturen                             | [**VDS \_ LUN \_ Plex- \_ Prop**](/windows/desktop/api/Vds/ns-vds-vds_lun_plex_prop).                                                                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hardware Anbieter Objekte](hardware-provider-objects.md)
</dt> <dt>

[LUN-Objekt](lun-object.md)
</dt> </dl>

 

 
