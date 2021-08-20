---
description: Portalobjekt
ms.assetid: 6655bbae-07d3-416b-9e45-ddcbe3433f40
title: Portalobjekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b7004f648b11b16c8c6279a0a74bae775fa539d8f0a93fc83d7effccea68915
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864520"
---
# <a name="portal-object"></a>Portalobjekt

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [Virtual Disk Service](virtual-disk-service-portal.md) durch die [Windows Storage Verwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Ein Portalobjekt modelliert ein iSCSI-Portal, das in einem iSCSI-Subsystem enthalten ist.

Verwenden Sie die [**IVdsSubSystemIscsi::QueryPortals-Methode,**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals) um die iSCSI-Portale des Subsystems zu bestimmen. Aufrufer können einen Zeiger auf ein bestimmtes Portal abrufen, indem sie das gewünschte Portalobjekt aus der Enumeration auswählen, die von der **QueryPortals-Methode** zurückgegeben wird. Mit einem Portalobjekt können Sie den Portalstatus und die Abfrage nach Portaleigenschaften, zugeordneten Portalgruppen und dem Subsystem festlegen, das das Portal enthält.

Ein Portalobjekt kann höchstens einer Portalgruppe eines angegebenen Ziels zugeordnet werden.

Portale dienen als einer der Endpunkte von MPIO-Pfaden bei iSCSI-Hardwareanbietern, für die Lastenausgleichsrichtlinien erzwungen werden können.

Zu den Portalobjekteigenschaften gehören ein Objektbezeichner, eine IP-Adresse und ein Port sowie der Portalstatus.

In der folgenden Tabelle sind verwandte Schnittstellen, Enumerationen und Strukturen aufgeführt.



| type                                                                                      | Element                                                                                                                 |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Schnittstellen, die von diesem Objekt immer nur in VDS 1.1- und 2.0-iSCSI-Anbietern verfügbar gemacht werden | [**IVdsIscsiPortal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportal).                                                                             |
| Zugeordnete Enumerationen                                                                   | [**VDS \_ STATUS DES \_ ISCSI-PORTALS. \_**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_portal_status)                                                          |
| Zugeordnete Strukturen                                                                     | [**VDS \_ PROP- \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portal_prop) und [**\_ VDS-PORTBENACHRICHTIGUNG \_**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)IM ISCSI-PORTAL . |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hardwareanbieterobjekte](hardware-provider-objects.md)
</dt> <dt>

[**IVdsSubSystemIscsi::QueryPortals**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals)
</dt> </dl>

 

 
