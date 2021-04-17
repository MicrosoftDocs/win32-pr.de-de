---
description: Portal Gruppen Objekt
ms.assetid: e5892e96-b6ad-447a-9627-b44fc6f1b27a
title: Portal Gruppen Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c915e76debac959a1dc7684d87c9770033b4aa34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530152"
---
# <a name="portal-group-object"></a>Portal Gruppen Objekt

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Ein Portal Gruppen Objekt modelliert eine iSCSI-Portal Gruppe, die in einem iSCSI-Ziel enthalten ist.

Verwenden Sie die [**ivdsiscsitarget:: queryportalgroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups) -Methode, um die Portal Gruppen zu ermitteln, die in einem bestimmten Ziel enthalten sind. Verwenden Sie die [**ivdsiscsiportal:: queryassociatedportalgroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups) -Methode, um die Portal Gruppen zu ermitteln, die einem bestimmten Portal zugeordnet sind. Aufrufer können einen Zeiger auf eine bestimmte Portal Gruppe abrufen, indem Sie das gewünschte Portal Gruppen Objekt aus der-Enumeration auswählen, die von der **queryportalgroups** -Methode oder der **queryassociatedportalgroups** -Methode zurückgegeben wird. Mit einem Portal Gruppen Objekt können Sie Portale hinzufügen oder entfernen und Abfragen für Portal Gruppen Eigenschaften, zugeordnete Portale und das Ziel, das die Portal Gruppe enthält, Abfragen.

Zu den Eigenschaften der Portal Gruppen Objekte gehören ein [Objekt Bezeichner](vds-data-types.md) und das Tag der Portal Gruppe. Weitere Informationen zu Portal Gruppen Tags finden Sie in der iSCSI-Spezifikation unter <https://go.microsoft.com/fwlink/p/?linkid=158752> .

In der folgenden Tabelle werden verwandte Schnittstellen, Enumerationen und Strukturen aufgelistet.



| type                                                                                      | Element                                                                                                                                            |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Schnittstellen, die von diesem Objekt immer nur in VDS 1,1-und 2,0-iSCSI-Anbietern verfügbar gemacht werden | [**Ivdsiscsiportalgroup**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportalgroup).                                                                                              |
| Zugehörige Enumerationen                                                                   | Keine.                                                                                                                                              |
| Zugeordnete Strukturen                                                                     | [**VDS \_ Gruppen Benachrichtigung für iSCSI- \_ portalgroup- \_ Prop**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portalgroup_prop) und [**VDS- \_ \_ \_ Portal**](/windows/desktop/api/Vds/ns-vds-vds_portal_group_notification). |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hardware Anbieter Objekte](hardware-provider-objects.md)
</dt> <dt>

[**Ivdsiscsiportal:: queryassociatedportalgroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups)
</dt> <dt>

[**Ivdsiscsitarget:: queryportalgroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups)
</dt> </dl>

 

 
