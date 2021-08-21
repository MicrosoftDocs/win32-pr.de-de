---
description: Portalgruppenobjekt
ms.assetid: e5892e96-b6ad-447a-9627-b44fc6f1b27a
title: Portalgruppenobjekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1021d74a3c8a6a612372db56952be1dabe5380e8e4a49b1b83c5ae2fe54754
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057958"
---
# <a name="portal-group-object"></a>Portalgruppenobjekt

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [Virtual Disk Service](virtual-disk-service-portal.md) durch die Windows Storage Verwaltungs-API. [](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

Ein Portalgruppenobjekt modelliert eine iSCSI-Portalgruppe, die in einem iSCSI-Ziel enthalten ist.

Verwenden Sie [**die IVdsIscsiTarget::QueryPortalGroups-Methode,**](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups) um die Portalgruppen zu bestimmen, die in einem bestimmten Ziel enthalten sind. Verwenden Sie [**die IVdsIscsiPortal::QueryAssociatedPortalGroups-Methode,**](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups) um die Portalgruppen zu bestimmen, die einem angegebenen Portal zugeordnet sind. Aufrufer können einen Zeiger auf eine bestimmte Portalgruppe erhalten, indem sie das gewünschte Portalgruppenobjekt aus der -Enumeration auswählen, die von der **QueryPortalGroups-Methode** oder der **QueryAssociatedPortalGroups-Methode** zurückgegeben wird. Mit einem Portalgruppenobjekt können Sie Portale hinzufügen oder entfernen und Portalgruppeneigenschaften, zugeordnete Portale und das Ziel abfragen, das die Portalgruppe enthält.

Zu den Eigenschaften des Portalgruppenobjekts gehören [ein Objektbezeichner](vds-data-types.md) und das Portalgruppentag. Weitere Informationen zu Portalgruppentags finden Sie in der iSCSI-Spezifikation unter <https://go.microsoft.com/fwlink/p/?linkid=158752> .

In der folgenden Tabelle sind verwandte Schnittstellen, Enumerationen und Strukturen aufgeführt.



| Typ                                                                                      | Element                                                                                                                                            |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Schnittstellen, die von diesem Objekt immer nur in ISCSI-Anbietern der Version 1.1 und 2.0 verfügbar gemacht werden | [**IVdsIscsiPortalGroup**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportalgroup).                                                                                              |
| Zugeordnete Enumerationen                                                                   | Keine.                                                                                                                                              |
| Zugeordnete Strukturen                                                                     | [**VDS \_ ISCSI \_ PORTALGROUP \_ PROP UND**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portalgroup_prop) [**VDS PORTAL GROUP \_ \_ \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_portal_group_notification). |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hardwareanbieterobjekte](hardware-provider-objects.md)
</dt> <dt>

[**IVdsIscsiPortal::QueryAssociatedPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups)
</dt> <dt>

[**IVdsIscsiTarget::QueryPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups)
</dt> </dl>

 

 
