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
# <a name="portal-object"></a><span data-ttu-id="49bb1-103">Portal Objekt</span><span class="sxs-lookup"><span data-stu-id="49bb1-103">Portal Object</span></span>

<span data-ttu-id="49bb1-104">\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]</span><span class="sxs-lookup"><span data-stu-id="49bb1-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="49bb1-105">Ein Portal Objekt modelliert ein iSCSI-Portal, das in einem iSCSI-Subsystem enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="49bb1-105">A portal object models an iSCSI portal that is contained within an iSCSI subsystem.</span></span>

<span data-ttu-id="49bb1-106">Verwenden Sie die [**ivdssubsystemiscsi:: queryportals**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals) -Methode, um die iSCSI-Portale des Subsystems zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="49bb1-106">Use the [**IVdsSubSystemIscsi::QueryPortals**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals) method to determine the iSCSI portals of the subsystem.</span></span> <span data-ttu-id="49bb1-107">Aufrufer können einen Zeiger auf ein bestimmtes Portal abrufen, indem Sie das gewünschte Portal Objekt aus der-Enumeration auswählen, die von der **queryportals** -Methode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="49bb1-107">Callers can get a pointer to a specific portal by selecting the desired portal object from the enumeration that is returned by the **QueryPortals** method.</span></span> <span data-ttu-id="49bb1-108">Mit einem Portal Objekt können Sie den Portal Status und die Abfrage für Portal Eigenschaften, zugehörige Portal Gruppen und das Subsystem festlegen, das das Portal enthält.</span><span class="sxs-lookup"><span data-stu-id="49bb1-108">With a portal object, you can set the portal status and query for portal properties, associated portal groups, and the subsystem that contains the portal.</span></span>

<span data-ttu-id="49bb1-109">Ein Portal Objekt kann nur höchstens einer Portal Gruppe eines angegebenen Ziels zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="49bb1-109">A portal object can only be associated with at most one portal group of a specified target.</span></span>

<span data-ttu-id="49bb1-110">Portale dienen als einer der Endpunkte von MPIO-Pfaden in iSCSI-Hardwareanbietern, auf denen Richtlinien für den Lastenausgleich festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="49bb1-110">Portals serve as one of the endpoints of MPIO paths in iSCSI hardware providers, upon which load balancing policies can be imposed.</span></span>

<span data-ttu-id="49bb1-111">Zu den Portal Objekteigenschaften gehören ein Objekt Bezeichner, eine IP-Adresse und ein Port sowie der Status des Portals.</span><span class="sxs-lookup"><span data-stu-id="49bb1-111">Portal object properties include an object identifier, an IP address and port, and the portal status.</span></span>

<span data-ttu-id="49bb1-112">In der folgenden Tabelle werden verwandte Schnittstellen, Enumerationen und Strukturen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="49bb1-112">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="49bb1-113">type</span><span class="sxs-lookup"><span data-stu-id="49bb1-113">Type</span></span>                                                                                      | <span data-ttu-id="49bb1-114">Element</span><span class="sxs-lookup"><span data-stu-id="49bb1-114">Element</span></span>                                                                                                                 |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49bb1-115">Schnittstellen, die von diesem Objekt immer nur in VDS 1,1-und 2,0-iSCSI-Anbietern verfügbar gemacht werden</span><span class="sxs-lookup"><span data-stu-id="49bb1-115">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 iSCSI providers only</span></span> | <span data-ttu-id="49bb1-116">[**Ivdsiscsiportal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportal).</span><span class="sxs-lookup"><span data-stu-id="49bb1-116">[**IVdsIscsiPortal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportal).</span></span>                                                                             |
| <span data-ttu-id="49bb1-117">Zugehörige Enumerationen</span><span class="sxs-lookup"><span data-stu-id="49bb1-117">Associated enumerations</span></span>                                                                   | <span data-ttu-id="49bb1-118">[**VDS \_ \_ \_ Status des iSCSI-Portals**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_portal_status).</span><span class="sxs-lookup"><span data-stu-id="49bb1-118">[**VDS\_ISCSI\_PORTAL\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_portal_status).</span></span>                                                          |
| <span data-ttu-id="49bb1-119">Zugeordnete Strukturen</span><span class="sxs-lookup"><span data-stu-id="49bb1-119">Associated structures</span></span>                                                                     | <span data-ttu-id="49bb1-120">[**VDS \_ Unter \_ \_ Stützung für das iSCSI-Portal**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portal_prop) und [**VDS- \_ Port \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_port_notification).</span><span class="sxs-lookup"><span data-stu-id="49bb1-120">[**VDS\_ISCSI\_PORTAL\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portal_prop) and [**VDS\_PORT\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_port_notification).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="49bb1-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="49bb1-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49bb1-122">Hardware Anbieter Objekte</span><span class="sxs-lookup"><span data-stu-id="49bb1-122">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="49bb1-123">**Ivdssubsystemiscsi:: queryportals**</span><span class="sxs-lookup"><span data-stu-id="49bb1-123">**IVdsSubSystemIscsi::QueryPortals**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals)
</dt> </dl>

 

 
