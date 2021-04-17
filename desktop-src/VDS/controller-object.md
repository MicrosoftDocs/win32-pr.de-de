---
description: Controller Objekt
ms.assetid: ae2c4d47-15a6-4b9d-9165-4ee04a6ff3a8
title: Controller Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7db9468c1ca4c8f07c5498724333bdad9fc53bf
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "104568072"
---
# <a name="controller-object"></a><span data-ttu-id="517eb-103">Controller Objekt</span><span class="sxs-lookup"><span data-stu-id="517eb-103">Controller Object</span></span>

<span data-ttu-id="517eb-104">\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]</span><span class="sxs-lookup"><span data-stu-id="517eb-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="517eb-105">Ein Controller Objekt modelliert einen Controller in einem Subsystem.</span><span class="sxs-lookup"><span data-stu-id="517eb-105">A controller object models a controller in a subsystem.</span></span> <span data-ttu-id="517eb-106">Controller sind in Subsystemen enthalten, und jeder Controller verfügt über einen oder mehrere Controllerports, über die der Host Computer in LUNs schreiben und aus diesen lesen kann.</span><span class="sxs-lookup"><span data-stu-id="517eb-106">Controllers are contained by subsystems, and each controller has one or more controller ports through which the host computer can write to and read from LUNs.</span></span> <span data-ttu-id="517eb-107">Ein einzelner Controller kann gleichzeitig für eine LUN auf aktiv festgelegt und für andere Benutzer inaktiv sein.</span><span class="sxs-lookup"><span data-stu-id="517eb-107">A single controller can be simultaneously set to active for one LUN and inactive for others.</span></span> <span data-ttu-id="517eb-108">Ein Controller, der für eine angegebene LUN aktiv ist, ist für die Behandlung von Eingaben und Ausgaben von der LUN verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="517eb-108">A controller that is active for a specified LUN carries the responsibility for handling input to and output from the LUN.</span></span> <span data-ttu-id="517eb-109">Diese Idee wird in der folgenden Abbildung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="517eb-109">The following figure illustrates this idea.</span></span>

![Diagramm, das einen "controller" mit einer aktiven LUN auf der linken Seite und zwei aktive LUNs auf der rechten Seite anzeigt.](images/vdscontroller.png)

<span data-ttu-id="517eb-111">**VDS 1,0:** Alle Controller eines Subsystems sind entweder auf "aktiv" oder "inaktiv" festgelegt, und zwar in Bezug auf die einzelnen LUNs, die das Subsystem hat.</span><span class="sxs-lookup"><span data-stu-id="517eb-111">**VDS 1.0:** Each of a subsystem's controllers is set to either active or inactive in relation to each of the LUNs the subsystem surfaces.</span></span>

<span data-ttu-id="517eb-112">VDS-Anwendungen verwenden die [**ivdssubsystem:: querycontrollers**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querycontrollers) -Methode, um die Controller zu ermitteln, die in einem bestimmten Subsystem enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="517eb-112">VDS applications use the [**IVdsSubSystem::QueryControllers**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querycontrollers) method to determine the controllers that are contained by a specific subsystem.</span></span> <span data-ttu-id="517eb-113">Aufrufer können einen Zeiger auf einen bestimmten Controller abrufen, indem Sie das gewünschte Controller Objekt aus der-Enumeration auswählen, die von der **querycontrollers** -Methode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="517eb-113">Callers can get a pointer to a specific controller by selecting the desired controller object from the enumeration that is returned by the **QueryControllers** method.</span></span> <span data-ttu-id="517eb-114">Mit einem Controller Objekt kann ein Aufrufer den Controller Status festlegen, die zugehörigen LUNs Abfragen, seine Controller Anschlüsse Abfragen und den Cache leeren und für ungültig erklären.</span><span class="sxs-lookup"><span data-stu-id="517eb-114">With a controller object, a caller can set the controller status, query for its associated LUNs, query for its controller ports, and flush and invalidate the cache.</span></span>

<span data-ttu-id="517eb-115">Zusätzlich zu einem Objekt Bezeichner, einem Namen und einer Seriennummer enthalten die Eigenschaften des Controller Objekts den Controller Status und-Zustand sowie die Anzahl der Ports.</span><span class="sxs-lookup"><span data-stu-id="517eb-115">In addition to an object identifier, a name, and a serial number, controller object properties include the controller status and health, and a count of the ports.</span></span>

<span data-ttu-id="517eb-116">In der folgenden Tabelle werden verwandte Schnittstellen, Enumerationen und Strukturen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="517eb-116">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="517eb-117">type</span><span class="sxs-lookup"><span data-stu-id="517eb-117">Type</span></span>                                                                                              | <span data-ttu-id="517eb-118">Element</span><span class="sxs-lookup"><span data-stu-id="517eb-118">Element</span></span>                                                                                                                        |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="517eb-119">Schnittstellen, die von diesem Objekt immer verfügbar gemacht werden</span><span class="sxs-lookup"><span data-stu-id="517eb-119">Interfaces that are always exposed by this object</span></span>                                                 | [<span data-ttu-id="517eb-120">**Ivdscontroller**</span><span class="sxs-lookup"><span data-stu-id="517eb-120">**IVdsController**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdscontroller)                                                                                       |
| <span data-ttu-id="517eb-121">Schnittstellen, die von diesem Objekt immer in VDS 1,1 und 2,0 Fibre Channel Anbietern verfügbar gemacht werden</span><span class="sxs-lookup"><span data-stu-id="517eb-121">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 Fibre Channel providers only</span></span> | [<span data-ttu-id="517eb-122">**Ivdscontrollercontrollerport**</span><span class="sxs-lookup"><span data-stu-id="517eb-122">**IVdsControllerControllerPort**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdscontrollercontrollerport)                                                           |
| <span data-ttu-id="517eb-123">Schnittstellen, die von diesem Objekt verfügbar gemacht werden können</span><span class="sxs-lookup"><span data-stu-id="517eb-123">Interfaces that may be exposed by this object</span></span>                                                     | [<span data-ttu-id="517eb-124">**Ivdsmaintenance**</span><span class="sxs-lookup"><span data-stu-id="517eb-124">**IVdsMaintenance**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)                                                                                     |
| <span data-ttu-id="517eb-125">Zugehörige Enumerationen</span><span class="sxs-lookup"><span data-stu-id="517eb-125">Associated enumerations</span></span>                                                                           | <span data-ttu-id="517eb-126">[**VDS \_ Controller \_ Status**](/windows/desktop/api/Vds/ne-vds-vds_controller_status).</span><span class="sxs-lookup"><span data-stu-id="517eb-126">[**VDS\_CONTROLLER\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_controller_status).</span></span>                                                                      |
| <span data-ttu-id="517eb-127">Zugeordnete Strukturen</span><span class="sxs-lookup"><span data-stu-id="517eb-127">Associated structures</span></span>                                                                             | <span data-ttu-id="517eb-128">[**VDS \_ Controller- \_ Prop**](/windows/desktop/api/Vds/ns-vds-vds_controller_prop) -und [**VDS- \_ Controller \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification).</span><span class="sxs-lookup"><span data-stu-id="517eb-128">[**VDS\_CONTROLLER\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_controller_prop) and [**VDS\_CONTROLLER\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="517eb-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="517eb-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="517eb-130">Hardware Anbieter Objekte</span><span class="sxs-lookup"><span data-stu-id="517eb-130">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="517eb-131">**Ivdssubsystem:: querycontrollers**</span><span class="sxs-lookup"><span data-stu-id="517eb-131">**IVdsSubSystem::QueryControllers**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querycontrollers)
</dt> </dl>

 

 
