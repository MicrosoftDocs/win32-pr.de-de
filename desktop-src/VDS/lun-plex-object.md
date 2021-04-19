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
# <a name="lun-plex-object"></a><span data-ttu-id="86142-103">LUN-Plex-Objekt</span><span class="sxs-lookup"><span data-stu-id="86142-103">LUN Plex Object</span></span>

<span data-ttu-id="86142-104">\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]</span><span class="sxs-lookup"><span data-stu-id="86142-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="86142-105">Ein LUN-Plex-Objekt modelliert einen LUN-Plex, der in einer LUN enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="86142-105">A LUN plex object models a LUN plex that is contained by a LUN.</span></span> <span data-ttu-id="86142-106">Nur eine gespiegelte LUN kann über mehrere plexes verfügen. alle anderen LUN-Typen haben einen Plex.</span><span class="sxs-lookup"><span data-stu-id="86142-106">Only a mirrored LUN can have multiple plexes; all other LUN types have one plex.</span></span> <span data-ttu-id="86142-107">Jeder Plex enthält eine Kopie der Daten auf der LUN.</span><span class="sxs-lookup"><span data-stu-id="86142-107">Each plex contains a copy of the data on the LUN.</span></span> <span data-ttu-id="86142-108">Neue plexe können einer LUN hinzugefügt werden, und mit Ausnahme des ursprünglichen Plex können vorhandene plexe entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="86142-108">New plexes can be added to a LUN, and, with the exception of the original plex, existing plexes can be removed.</span></span> <span data-ttu-id="86142-109">VDS unterstützt vier LUN-Plex-Typen: einfach, überspannt, Stripeset und Stripeset mit Parität.</span><span class="sxs-lookup"><span data-stu-id="86142-109">VDS supports four LUN plex types: simple, spanned, striped, and striped with parity.</span></span> <span data-ttu-id="86142-110">Eine Beschreibung dieser LUN-Typen finden Sie unter dem [LUN-Objekt](lun-object.md).</span><span class="sxs-lookup"><span data-stu-id="86142-110">For a description of each of these LUN types, see the [LUN Object](lun-object.md).</span></span>

<span data-ttu-id="86142-111">Verwenden Sie die [**ivdslun:: addplex**](/windows/desktop/api/Vds/nf-vds-ivdslun-addplex) -Methode, um einem LUN einen Plex und die [**ivdslun:: removeplex**](/windows/desktop/api/Vds/nf-vds-ivdslun-removeplex) -Methode hinzuzufügen, um den Plex zu löschen.</span><span class="sxs-lookup"><span data-stu-id="86142-111">Use the [**IVdsLun::AddPlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-addplex) method to add a plex to a LUN and the [**IVdsLun::RemovePlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-removeplex) method to delete the plex.</span></span> <span data-ttu-id="86142-112">Sie können LUN-plexes Abfragen, indem Sie die [**ivdslun:: queryplexes**](/windows/desktop/api/Vds/nf-vds-ivdslun-queryplexes) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="86142-112">You can query for LUN plexes by invoking the [**IVdsLun::QueryPlexes**](/windows/desktop/api/Vds/nf-vds-ivdslun-queryplexes) method.</span></span> <span data-ttu-id="86142-113">Sie können einen Zeiger auf einen bestimmten LUN-Plex abrufen, indem Sie das gewünschte Plex-Objekt aus der-Enumeration auswählen, die von der **queryplexes** -Methode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="86142-113">You can get a pointer to a specific LUN plex by selecting the desired plex object from the enumeration that is returned by the **QueryPlexes** method.</span></span> <span data-ttu-id="86142-114">Mit einem Plex-Objekt können Sie die Laufwerks Blöcke und automagandeutungen Abfragen und neue Hinweise anwenden.</span><span class="sxs-lookup"><span data-stu-id="86142-114">With a plex object, you can query for the drive extents and automagic hints, and apply new hints.</span></span>

<span data-ttu-id="86142-115">Zusätzlich zu einem Objekt Bezeichner, einem Namen und einer Seriennummer enthalten die LUN-Plex-Objekteigenschaften den Plex-Typ, die Größe, den Status, die Integrität, den Übergangsstatus und die Flags. eine Liste der Maskierungen und die Stripesetgröße; und eine Einstellung für die Neuerstellungs Priorität.</span><span class="sxs-lookup"><span data-stu-id="86142-115">In addition to an object identifier, a name, and a serial number, LUN plex object properties include the plex type, size, status, health, transition state, and flags; an unmasking list and stripe size; and a rebuild priority setting.</span></span>

<span data-ttu-id="86142-116">In der folgenden Tabelle werden verwandte Schnittstellen, Enumerationen und Strukturen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="86142-116">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="86142-117">type</span><span class="sxs-lookup"><span data-stu-id="86142-117">Type</span></span>                                              | <span data-ttu-id="86142-118">Element</span><span class="sxs-lookup"><span data-stu-id="86142-118">Element</span></span>                                                                                                                                                          |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86142-119">Schnittstellen, die von diesem Objekt immer verfügbar gemacht werden</span><span class="sxs-lookup"><span data-stu-id="86142-119">Interfaces that are always exposed by this object</span></span> | <span data-ttu-id="86142-120">[**Ivdslunplex**](/windows/desktop/api/Vds/nn-vds-ivdslunplex).</span><span class="sxs-lookup"><span data-stu-id="86142-120">[**IVdsLunPlex**](/windows/desktop/api/Vds/nn-vds-ivdslunplex).</span></span>                                                                                                                              |
| <span data-ttu-id="86142-121">Zugehörige Enumerationen</span><span class="sxs-lookup"><span data-stu-id="86142-121">Associated enumerations</span></span>                           | <span data-ttu-id="86142-122">[**VDS \_ LUN \_ Plex- \_ Flag**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_flag), [**VDS- \_ LUN-Plex- \_ \_ Status**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_status)und [**VDS- \_ LUN-Plex- \_ \_ Typ**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_type).</span><span class="sxs-lookup"><span data-stu-id="86142-122">[**VDS\_LUN\_PLEX\_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_flag), [**VDS\_LUN\_PLEX\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_status), and [**VDS\_LUN\_PLEX\_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_type).</span></span> |
| <span data-ttu-id="86142-123">Zugeordnete Strukturen</span><span class="sxs-lookup"><span data-stu-id="86142-123">Associated structures</span></span>                             | <span data-ttu-id="86142-124">[**VDS \_ LUN \_ Plex- \_ Prop**](/windows/desktop/api/Vds/ns-vds-vds_lun_plex_prop).</span><span class="sxs-lookup"><span data-stu-id="86142-124">[**VDS\_LUN\_PLEX\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_lun_plex_prop).</span></span>                                                                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="86142-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="86142-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86142-126">Hardware Anbieter Objekte</span><span class="sxs-lookup"><span data-stu-id="86142-126">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="86142-127">LUN-Objekt</span><span class="sxs-lookup"><span data-stu-id="86142-127">LUN Object</span></span>](lun-object.md)
</dt> </dl>

 

 
