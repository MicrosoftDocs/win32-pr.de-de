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
# <a name="portal-group-object"></a><span data-ttu-id="801fc-103">Portal Gruppen Objekt</span><span class="sxs-lookup"><span data-stu-id="801fc-103">Portal Group Object</span></span>

<span data-ttu-id="801fc-104">\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]</span><span class="sxs-lookup"><span data-stu-id="801fc-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="801fc-105">Ein Portal Gruppen Objekt modelliert eine iSCSI-Portal Gruppe, die in einem iSCSI-Ziel enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="801fc-105">A portal group object models an iSCSI portal group that is contained within an iSCSI target.</span></span>

<span data-ttu-id="801fc-106">Verwenden Sie die [**ivdsiscsitarget:: queryportalgroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups) -Methode, um die Portal Gruppen zu ermitteln, die in einem bestimmten Ziel enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="801fc-106">Use the [**IVdsIscsiTarget::QueryPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups) method to determine the portal groups that are contained by a specific target.</span></span> <span data-ttu-id="801fc-107">Verwenden Sie die [**ivdsiscsiportal:: queryassociatedportalgroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups) -Methode, um die Portal Gruppen zu ermitteln, die einem bestimmten Portal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="801fc-107">Use the [**IVdsIscsiPortal::QueryAssociatedPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups) method to determine the portal groups that are associated with a specified portal.</span></span> <span data-ttu-id="801fc-108">Aufrufer können einen Zeiger auf eine bestimmte Portal Gruppe abrufen, indem Sie das gewünschte Portal Gruppen Objekt aus der-Enumeration auswählen, die von der **queryportalgroups** -Methode oder der **queryassociatedportalgroups** -Methode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="801fc-108">Callers can get a pointer to a specific portal group by selecting the desired portal group object from the enumeration that is returned by the **QueryPortalGroups** method or the **QueryAssociatedPortalGroups** method.</span></span> <span data-ttu-id="801fc-109">Mit einem Portal Gruppen Objekt können Sie Portale hinzufügen oder entfernen und Abfragen für Portal Gruppen Eigenschaften, zugeordnete Portale und das Ziel, das die Portal Gruppe enthält, Abfragen.</span><span class="sxs-lookup"><span data-stu-id="801fc-109">With a portal group object, you can add or remove portals and query for portal group properties, associated portals, and the target that contains the portal group.</span></span>

<span data-ttu-id="801fc-110">Zu den Eigenschaften der Portal Gruppen Objekte gehören ein [Objekt Bezeichner](vds-data-types.md) und das Tag der Portal Gruppe.</span><span class="sxs-lookup"><span data-stu-id="801fc-110">Portal group object properties include an [object identifier](vds-data-types.md) and the portal group tag.</span></span> <span data-ttu-id="801fc-111">Weitere Informationen zu Portal Gruppen Tags finden Sie in der iSCSI-Spezifikation unter <https://go.microsoft.com/fwlink/p/?linkid=158752> .</span><span class="sxs-lookup"><span data-stu-id="801fc-111">For more information about portal group tags, see the iSCSI specification at <https://go.microsoft.com/fwlink/p/?linkid=158752>.</span></span>

<span data-ttu-id="801fc-112">In der folgenden Tabelle werden verwandte Schnittstellen, Enumerationen und Strukturen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="801fc-112">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="801fc-113">type</span><span class="sxs-lookup"><span data-stu-id="801fc-113">Type</span></span>                                                                                      | <span data-ttu-id="801fc-114">Element</span><span class="sxs-lookup"><span data-stu-id="801fc-114">Element</span></span>                                                                                                                                            |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="801fc-115">Schnittstellen, die von diesem Objekt immer nur in VDS 1,1-und 2,0-iSCSI-Anbietern verfügbar gemacht werden</span><span class="sxs-lookup"><span data-stu-id="801fc-115">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 iSCSI providers only</span></span> | <span data-ttu-id="801fc-116">[**Ivdsiscsiportalgroup**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportalgroup).</span><span class="sxs-lookup"><span data-stu-id="801fc-116">[**IVdsIscsiPortalGroup**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportalgroup).</span></span>                                                                                              |
| <span data-ttu-id="801fc-117">Zugehörige Enumerationen</span><span class="sxs-lookup"><span data-stu-id="801fc-117">Associated enumerations</span></span>                                                                   | <span data-ttu-id="801fc-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="801fc-118">None.</span></span>                                                                                                                                              |
| <span data-ttu-id="801fc-119">Zugeordnete Strukturen</span><span class="sxs-lookup"><span data-stu-id="801fc-119">Associated structures</span></span>                                                                     | <span data-ttu-id="801fc-120">[**VDS \_ Gruppen Benachrichtigung für iSCSI- \_ portalgroup- \_ Prop**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portalgroup_prop) und [**VDS- \_ \_ \_ Portal**](/windows/desktop/api/Vds/ns-vds-vds_portal_group_notification).</span><span class="sxs-lookup"><span data-stu-id="801fc-120">[**VDS\_ISCSI\_PORTALGROUP\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portalgroup_prop) and [**VDS\_PORTAL\_GROUP\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_portal_group_notification).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="801fc-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="801fc-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="801fc-122">Hardware Anbieter Objekte</span><span class="sxs-lookup"><span data-stu-id="801fc-122">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="801fc-123">**Ivdsiscsiportal:: queryassociatedportalgroups**</span><span class="sxs-lookup"><span data-stu-id="801fc-123">**IVdsIscsiPortal::QueryAssociatedPortalGroups**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups)
</dt> <dt>

[<span data-ttu-id="801fc-124">**Ivdsiscsitarget:: queryportalgroups**</span><span class="sxs-lookup"><span data-stu-id="801fc-124">**IVdsIscsiTarget::QueryPortalGroups**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups)
</dt> </dl>

 

 
