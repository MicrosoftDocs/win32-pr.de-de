---
description: Controller Port Objekt
ms.assetid: 5f94bcdc-93ab-4522-88bd-009a049b5dc9
title: Controller Port Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7547581358bd79212b1093384ce1589e331f6ee0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343276"
---
# <a name="controller-port-object"></a><span data-ttu-id="a1d03-103">Controller Port Objekt</span><span class="sxs-lookup"><span data-stu-id="a1d03-103">Controller Port Object</span></span>

<span data-ttu-id="a1d03-104">\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]</span><span class="sxs-lookup"><span data-stu-id="a1d03-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="a1d03-105">Ein Controller Port Objekt modelliert einen Controller Anschluss in einem Subsystem.</span><span class="sxs-lookup"><span data-stu-id="a1d03-105">A controller port object models a controller port in a subsystem.</span></span> <span data-ttu-id="a1d03-106">Host Computer können mithilfe von Controller Anschlüssen in LUNs schreiben und daraus lesen.</span><span class="sxs-lookup"><span data-stu-id="a1d03-106">Host computers can write to and read from LUNs through controller ports.</span></span> <span data-ttu-id="a1d03-107">Controller Anschlüsse sind in Controllern in einem Subsystem enthalten.</span><span class="sxs-lookup"><span data-stu-id="a1d03-107">Controller ports are contained by controllers in a subsystem.</span></span> <span data-ttu-id="a1d03-108">In VDS 1,1 und VDS 2.0 ist jede Controller-Ports eines Subsystems entweder auf "aktiv" oder "inaktiv" festgelegt, und zwar in Bezug auf die einzelnen LUNs des Subsystems.</span><span class="sxs-lookup"><span data-stu-id="a1d03-108">In VDS 1.1 and VDS2.0, each of a subsystem's controller ports is set to either active or inactive in relation to each of the LUNs the subsystem surfaces.</span></span> <span data-ttu-id="a1d03-109">Ein einzelner Controllerport kann dann gleichzeitig für eine LUN auf aktiv festgelegt und für andere Benutzer inaktiv sein.</span><span class="sxs-lookup"><span data-stu-id="a1d03-109">A single controller port, then, can be simultaneously set to active for one LUN and inactive for others.</span></span> <span data-ttu-id="a1d03-110">Ein Controllerport, der für eine bestimmte LUN aktiv ist, ist für die Behandlung von Eingaben und Ausgaben von der LUN verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="a1d03-110">A controller port that is active for a given LUN carries responsibility for handling input to and output from the LUN.</span></span>

<span data-ttu-id="a1d03-111">Aktive Controllerports dienen als einer der Endpunkte von MPIO-Pfaden in Fibre Channel Hardwareanbietern, auf denen Richtlinien für den Lastenausgleich festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="a1d03-111">Active controller ports serve as one of the endpoints of MPIO paths in Fibre Channel hardware providers, upon which load balancing policies can be imposed.</span></span>

<span data-ttu-id="a1d03-112">Verwenden Sie die [**ivdscontrollercontrollerport:: querycontrollerports**](/windows/desktop/api/Vds/nf-vds-ivdscontrollercontrollerport-querycontrollerports) -Methode, um die Controller Anschlüsse zu ermitteln, die in einem bestimmten Controller enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="a1d03-112">Use the [**IVdsControllerControllerPort::QueryControllerPorts**](/windows/desktop/api/Vds/nf-vds-ivdscontrollercontrollerport-querycontrollerports) method to determine the controller ports that are contained by a specific controller.</span></span> <span data-ttu-id="a1d03-113">Aufrufer können einen Zeiger auf einen bestimmten Controllerport abrufen, indem Sie das gewünschte Controller Port Objekt aus der-Enumeration auswählen, die von der **querycontrollerports** -Methode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a1d03-113">Callers can get a pointer to a specific controller port by selecting the desired controller port object from the enumeration that is returned by the **QueryControllerPorts** method.</span></span> <span data-ttu-id="a1d03-114">Bei einem Controller Objekt kann ein Aufrufer den Status des Controller Ports festlegen und die zugehörigen LUNs Abfragen.</span><span class="sxs-lookup"><span data-stu-id="a1d03-114">With a controller object, a caller can set the controller port status and query for its associated LUNs.</span></span>

<span data-ttu-id="a1d03-115">Zu den Controller Objekteigenschaften gehören ein Objekt Bezeichner, ein Name, eine Seriennummer und der Status des Controller Ports.</span><span class="sxs-lookup"><span data-stu-id="a1d03-115">Controller object properties include an object identifier, a name, a serial number, and the controller port status.</span></span>

<span data-ttu-id="a1d03-116">In der folgenden Tabelle werden verwandte Schnittstellen, Enumerationen und Strukturen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a1d03-116">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="a1d03-117">type</span><span class="sxs-lookup"><span data-stu-id="a1d03-117">Type</span></span>                                                                                              | <span data-ttu-id="a1d03-118">Element</span><span class="sxs-lookup"><span data-stu-id="a1d03-118">Element</span></span>                                                                                               |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1d03-119">Schnittstellen, die von diesem Objekt immer in VDS 1,1 und 2,0 Fibre Channel Anbietern verfügbar gemacht werden</span><span class="sxs-lookup"><span data-stu-id="a1d03-119">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 Fibre Channel providers only</span></span> | [<span data-ttu-id="a1d03-120">**Ivdscontrollerport**</span><span class="sxs-lookup"><span data-stu-id="a1d03-120">**IVdsControllerPort**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdscontrollerport)                                                      |
| <span data-ttu-id="a1d03-121">Zugehörige Enumerationen</span><span class="sxs-lookup"><span data-stu-id="a1d03-121">Associated enumerations</span></span>                                                                           | [<span data-ttu-id="a1d03-122">**VDS- \_ Port \_ Status**</span><span class="sxs-lookup"><span data-stu-id="a1d03-122">**VDS\_PORT\_STATUS**</span></span>](/windows/desktop/api/Vds/ne-vds-vds_port_status)                                                          |
| <span data-ttu-id="a1d03-123">Zugeordnete Strukturen</span><span class="sxs-lookup"><span data-stu-id="a1d03-123">Associated structures</span></span>                                                                             | <span data-ttu-id="a1d03-124">[**VDS \_ Port \_**](/windows/desktop/api/Vds/ns-vds-vds_port_prop) -und [ **VDS- \_ Port \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)</span><span class="sxs-lookup"><span data-stu-id="a1d03-124">[**VDS\_PORT\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_port_prop) and [**VDS\_PORT\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a1d03-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a1d03-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1d03-126">Hardware Anbieter Objekte</span><span class="sxs-lookup"><span data-stu-id="a1d03-126">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="a1d03-127">**Ivdscontrollercontrollerport:: querycontrollerports**</span><span class="sxs-lookup"><span data-stu-id="a1d03-127">**IVdsControllerControllerPort::QueryControllerPorts**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdscontrollercontrollerport-querycontrollerports)
</dt> </dl>

 

 
