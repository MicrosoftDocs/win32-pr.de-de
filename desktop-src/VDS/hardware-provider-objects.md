---
description: Hardware Anbieter Objekte
ms.assetid: d1724219-1487-485b-9c52-5003069fe9e2
title: Hardware Anbieter Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1aaebf61e97487b48a6b8bf0dbd91cc6aa3e0bd
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "106353239"
---
# <a name="hardware-provider-objects"></a><span data-ttu-id="20ecd-103">Hardware Anbieter Objekte</span><span class="sxs-lookup"><span data-stu-id="20ecd-103">Hardware Provider Objects</span></span>

<span data-ttu-id="20ecd-104">\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]</span><span class="sxs-lookup"><span data-stu-id="20ecd-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="20ecd-105">Das VDS-Objektmodell enthält eine Reihe von Objekten, mit denen Hardware Anbieter Entitäten abgefragt und konfiguriert werden können.</span><span class="sxs-lookup"><span data-stu-id="20ecd-105">The VDS object model includes a set of objects to query and configure hardware provider entities.</span></span> <span data-ttu-id="20ecd-106">(Beachten Sie, dass VDS zwar einen Softwareanbieter enthält, aber einen Hardware Anbieter und die zugeordnete Hardware separat kaufen müssen, um die Hardware Anbieter Objekte nutzen zu können.) Diese Hardware Anbieter Objekte stellen physische Geräte (z. b. Subsysteme, Laufwerke und Controller) und virtuelle Geräte (z. b. LUNs und LUN-plexes) dar.</span><span class="sxs-lookup"><span data-stu-id="20ecd-106">(Note that while VDS includes a software provider, you must purchase a hardware provider and the associated hardware separately to take advantage of the hardware provider objects.) These hardware provider objects represent physical devices (such as subsystems, drives, and controllers) and virtual devices (such as LUNs and LUN plexes).</span></span>

<span data-ttu-id="20ecd-107">Ein Hardware Anbieter sollte ein COM-Objekt für jedes physische oder virtuelle Gerät erstellen.</span><span class="sxs-lookup"><span data-stu-id="20ecd-107">A hardware provider should create one COM object for each physical or virtual device.</span></span>

<span data-ttu-id="20ecd-108">Die folgende Abbildung zeigt die Beziehung zwischen dem Anbieter Objekt und dem Satz von Hardware Anbieter Objekten sowie die Beziehung zwischen den verschiedenen Hardware Anbieter Objekten selbst.</span><span class="sxs-lookup"><span data-stu-id="20ecd-108">The illustration that follows shows the relationship between the provider object and the set of hardware provider objects, as well as the relationship between the various hardware provider objects themselves.</span></span>

![<span data-ttu-id="20ecd-109">Diagramm, das die Beziehung zwischen "Provider" und "Subsystem", "controller", "LUN", "LUN Plex", "Drive" und "Spindel" anzeigt.</span><span class="sxs-lookup"><span data-stu-id="20ecd-109">Diagram that shows the relationship between the 'Provider' and 'Subsystem', 'Controller', 'LUN', 'LUN plex', 'Drive', and 'Spindle'.</span></span> ](images/vdshwobjects.png)

<span data-ttu-id="20ecd-110">Ein Anbieter Objekt kann eine beliebige Anzahl von Subsystemen enthalten.</span><span class="sxs-lookup"><span data-stu-id="20ecd-110">A provider object can contain any number of subsystems.</span></span> <span data-ttu-id="20ecd-111">Alle Hardware Anbieter können mehrere Instanzen desselben subsystemmodells verwalten.</span><span class="sxs-lookup"><span data-stu-id="20ecd-111">All hardware providers are capable of managing multiple instances of the same subsystem model.</span></span> <span data-ttu-id="20ecd-112">Viele Hardware Anbieter können auch mehrere Instanzen von unterschiedlichen subsystemmodellen verwalten.</span><span class="sxs-lookup"><span data-stu-id="20ecd-112">Many hardware providers are also capable of managing multiple instances of different subsystem models.</span></span> <span data-ttu-id="20ecd-113">Ein einzelner Computer kann eine beliebige Anzahl von Hardwareanbietern hosten.</span><span class="sxs-lookup"><span data-stu-id="20ecd-113">A single computer can host any number of hardware providers.</span></span>

<span data-ttu-id="20ecd-114">Ein Subsystem-Objekt kann eine beliebige Anzahl von Controllern und Laufwerken enthalten und kann beliebig viele LUNs enthalten.</span><span class="sxs-lookup"><span data-stu-id="20ecd-114">A subsystem object can contain any number of controllers and drives, and can surface any number of LUNs.</span></span> <span data-ttu-id="20ecd-115">Ein LUN-Objekt besteht aus mindestens einem LUN-Plex, und jeder LUN-Plex ist abhängig vom Plex-Typ einem oder mehreren Laufwerken zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="20ecd-115">A LUN object comprises of at least one LUN plex, and each LUN plex maps to one or more drives, depending on the plex type.</span></span> <span data-ttu-id="20ecd-116">Controller Objekte können Dateneingaben/-Ausgaben für eine beliebige Anzahl von LUN-Objekten verwalten.</span><span class="sxs-lookup"><span data-stu-id="20ecd-116">Controller objects can manage data input/output for any number of LUN objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="20ecd-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="20ecd-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20ecd-118">VDS-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="20ecd-118">VDS Object Model</span></span>](vds-object-model.md)
</dt> </dl>

 

 
