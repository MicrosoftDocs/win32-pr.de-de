---
description: Software Anbieter Objekte
ms.assetid: 0d415238-7558-4d90-a122-e65ae7760344
title: Software Anbieter Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c16f81cd975c892760d1851720e65584453e7745
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "103869335"
---
# <a name="software-provider-objects"></a><span data-ttu-id="49c96-103">Software Anbieter Objekte</span><span class="sxs-lookup"><span data-stu-id="49c96-103">Software Provider Objects</span></span>

<span data-ttu-id="49c96-104">\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]</span><span class="sxs-lookup"><span data-stu-id="49c96-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="49c96-105">Software Anbieter Objekte modellieren physische Geräte, z. b. IDE-Datenträger und CD-ROMs, sowie virtuelle Elemente wie Pakete, Volumes und Volumeplexes.</span><span class="sxs-lookup"><span data-stu-id="49c96-105">Software provider objects model physical devices, such as IDE disks and CD-ROMs, and virtual elements like packs, volumes, and volume plexes.</span></span> <span data-ttu-id="49c96-106">Die folgende Abbildung zeigt die Beziehung zwischen dem Anbieter Objekt und dem Satz von Softwareanbieter Objekten sowie die Beziehung zwischen den verschiedenen Softwareanbieter Objekten selbst.</span><span class="sxs-lookup"><span data-stu-id="49c96-106">The following illustration shows the relationship between the provider object and the set of software provider objects, as well as the relationship between the various software provider objects themselves.</span></span>

![Diagramm, das die Beziehung zwischen einem Anbieter-und Softwareanbieter Objekt, wie z. b. "Pack" und "Volume", anzeigt.](images/vdsswobjects.png)

<span data-ttu-id="49c96-108">Ein Anbieter Objekt kann NULL oder mehr Pakete enthalten.</span><span class="sxs-lookup"><span data-stu-id="49c96-108">A provider object can contain zero or more packs.</span></span> <span data-ttu-id="49c96-109">Ein Pack-Objekt kann NULL oder mehr Datenträger und Volumes enthalten.</span><span class="sxs-lookup"><span data-stu-id="49c96-109">A pack object can contain zero or more disks and volumes.</span></span> <span data-ttu-id="49c96-110">Ein Volume besteht aus mindestens einem Volume Plex, und jeder volumeplex kann je nach Plex-Typ einem oder mehreren Datenträgern zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="49c96-110">A volume comprises of at least one volume plex and each volume plex can map to one or more disks, depending on the plex type.</span></span> <span data-ttu-id="49c96-111">VDS verwaltet nicht zugewiesene Datenträger direkt ohne Paket Container.</span><span class="sxs-lookup"><span data-stu-id="49c96-111">VDS manages unallocated disks directly, without a pack container.</span></span> <span data-ttu-id="49c96-112">In den restlichen Themen dieses Abschnitts werden die Plex-Objekte Pack, Disk, Volume und Volume beschrieben.</span><span class="sxs-lookup"><span data-stu-id="49c96-112">The remaining topics of this section describe the pack, disk, volume, and volume plex objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="49c96-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="49c96-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49c96-114">VDS-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="49c96-114">VDS Object Model</span></span>](vds-object-model.md)
</dt> </dl>

 

 
