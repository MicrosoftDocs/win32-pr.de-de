---
description: Portal Objekt
ms.assetid: 6655bbae-07d3-416b-9e45-ddcbe3433f40
title: Portal Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01328d8dccfe7a29c0686cde9b531df63d56e63e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369857"
---
# <a name="portal-object"></a>Portal Objekt

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Ein Portal Objekt modelliert ein iSCSI-Portal, das in einem iSCSI-Subsystem enthalten ist.

Verwenden Sie die [**ivdssubsystemiscsi:: queryportals**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals) -Methode, um die iSCSI-Portale des Subsystems zu ermitteln. Aufrufer können einen Zeiger auf ein bestimmtes Portal abrufen, indem Sie das gewünschte Portal Objekt aus der-Enumeration auswählen, die von der **queryportals** -Methode zurückgegeben wird. Mit einem Portal Objekt können Sie den Portal Status und die Abfrage für Portal Eigenschaften, zugehörige Portal Gruppen und das Subsystem festlegen, das das Portal enthält.

Ein Portal Objekt kann nur höchstens einer Portal Gruppe eines angegebenen Ziels zugeordnet werden.

Portale dienen als einer der Endpunkte von MPIO-Pfaden in iSCSI-Hardwareanbietern, auf denen Richtlinien für den Lastenausgleich festgelegt werden können.

Zu den Portal Objekteigenschaften gehören ein Objekt Bezeichner, eine IP-Adresse und ein Port sowie der Status des Portals.

In der folgenden Tabelle werden verwandte Schnittstellen, Enumerationen und Strukturen aufgelistet.



| type                                                                                      | Element                                                                                                                 |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Schnittstellen, die von diesem Objekt immer nur in VDS 1,1-und 2,0-iSCSI-Anbietern verfügbar gemacht werden | [**Ivdsiscsiportal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportal).                                                                             |
| Zugehörige Enumerationen                                                                   | [**VDS \_ \_ \_ Status des iSCSI-Portals**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_portal_status).                                                          |
| Zugeordnete Strukturen                                                                     | [**VDS \_ Unter \_ \_ Stützung für das iSCSI-Portal**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portal_prop) und [**VDS- \_ Port \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_port_notification). |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hardware Anbieter Objekte](hardware-provider-objects.md)
</dt> <dt>

[**Ivdssubsystemiscsi:: queryportals**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals)
</dt> </dl>

 

 
