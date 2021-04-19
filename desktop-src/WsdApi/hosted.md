---
description: Definiert die Elemente serviceid, types, pnpxhardwareid und pnpxcompatibleid für die Dienste, die vom Dienst Host definiert werden.
ms.assetid: f901a88f-7e01-4e7f-a0f2-59f2a01b03cd
title: Hosted-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e4d46549898f0a95de362467c759c3d95eb806a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352502"
---
# <a name="hosted-element"></a><span data-ttu-id="55786-103">Hosted-Element</span><span class="sxs-lookup"><span data-stu-id="55786-103">hosted element</span></span>

<span data-ttu-id="55786-104">Definiert die Elemente [**serviceid**](serviceid.md), [**types**](types.md),[**pnpxhardwareid**](pnpxhardwareid.md)und [**pnpxcompatibleid**](pnpxcompatibleid.md) für die Dienste, die vom Dienst Host definiert werden.</span><span class="sxs-lookup"><span data-stu-id="55786-104">Defines the [**ServiceID**](serviceid.md), [**Types**](types.md),[**PnPXHardwareId**](pnpxhardwareid.md), and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements for the services defined by the service host.</span></span>

## <a name="usage"></a><span data-ttu-id="55786-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="55786-105">Usage</span></span>

``` syntax
<hosted>
  child elements
</hosted>
```

## <a name="attributes"></a><span data-ttu-id="55786-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="55786-106">Attributes</span></span>

<span data-ttu-id="55786-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="55786-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="55786-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="55786-108">Child elements</span></span>



| <span data-ttu-id="55786-109">Element</span><span class="sxs-lookup"><span data-stu-id="55786-109">Element</span></span>                                                 | <span data-ttu-id="55786-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55786-110">Description</span></span>                                                                      |
|---------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="55786-111">**Pnpxcompatibleid**</span><span class="sxs-lookup"><span data-stu-id="55786-111">**PnPXCompatibleId**</span></span>](pnpxcompatibleid.md)<br/> | <span data-ttu-id="55786-112">Gibt den mit PnP-X kompatiblen Bezeichner des Dienstanbieter an.</span><span class="sxs-lookup"><span data-stu-id="55786-112">Specifies the PnP-X Compatible Identifier of the service.</span></span><br/> <br/> |
| [<span data-ttu-id="55786-113">**Pnpxhardwareid**</span><span class="sxs-lookup"><span data-stu-id="55786-113">**PnPXHardwareId**</span></span>](pnpxhardwareid.md)<br/>     | <span data-ttu-id="55786-114">Gibt den PnP-X-Hardware Bezeichner des Dienstanbieter an.</span><span class="sxs-lookup"><span data-stu-id="55786-114">Specifies the PnP-X Hardware Identifier of the service.</span></span><br/> <br/>   |
| [<span data-ttu-id="55786-115">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="55786-115">**ServiceID**</span></span>](serviceid.md)<br/>               | <span data-ttu-id="55786-116">Definiert einen Dienst Bezeichner für den Dienst Host.</span><span class="sxs-lookup"><span data-stu-id="55786-116">Defines a service identifier for the service host.</span></span><br/> <br/>        |
| [<span data-ttu-id="55786-117">**Typen**</span><span class="sxs-lookup"><span data-stu-id="55786-117">**Types**</span></span>](types.md)<br/>                       | <span data-ttu-id="55786-118">Definiert eine Liste der qualifizierten XSD-Namen.</span><span class="sxs-lookup"><span data-stu-id="55786-118">Defines a list of XSD qualified names.</span></span><br/> <br/>                    |



### <a name="child-element-sequence"></a><span data-ttu-id="55786-119">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="55786-119">Child element sequence</span></span>

``` syntax
(
  ServiceID, 
  Types, 
  PnPXHardwareId?, 
  PnPXCompatibleId?
)
```

## <a name="parent-elements"></a><span data-ttu-id="55786-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="55786-120">Parent elements</span></span>



| <span data-ttu-id="55786-121">Element</span><span class="sxs-lookup"><span data-stu-id="55786-121">Element</span></span>                                         | <span data-ttu-id="55786-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55786-122">Description</span></span>                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="55786-123">**hostmetadata**</span><span class="sxs-lookup"><span data-stu-id="55786-123">**hostMetadata**</span></span>](hostmetadata.md)<br/> | <span data-ttu-id="55786-124">Die hostingmetadaten für das Gerät, das implementiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="55786-124">The hosting metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="55786-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55786-125">Remarks</span></span>

<span data-ttu-id="55786-126">Jeder von einem Dienst Host bereitgestellte Dienst sollte über eigene **gehostete** Element Informationen verfügen, um sicherzustellen, dass der Dienst in Antworten auf Metadatenanforderungen ordnungsgemäß veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="55786-126">Each service provided by a service host should have its own **hosted** element information to ensure that the service is published properly in responses to metadata requests.</span></span>

<span data-ttu-id="55786-127">Die [**pnpxhardwareid**](pnpxhardwareid.md) -und [**pnpxcompatibleid-**](pnpxcompatibleid.md) Elemente sind optional, aber wenn Sie verwendet werden, müssen Sie miteinander verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="55786-127">The [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements are optional, but when used, they must be used together.</span></span> <span data-ttu-id="55786-128">Wenn eine solche vorhanden ist, muss auch die andere vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="55786-128">If one is present, the other must be present as well.</span></span>

<span data-ttu-id="55786-129">Wenn ein [**pnpxenvicecategory**](pnpxdevicecategory.md) -Element vorhanden ist, muss mindestens ein **gehosteter** -Element sowohl [**pnpxhardwareid**](pnpxhardwareid.md) -als auch [**pnpxcompatibleid-**](pnpxcompatibleid.md) Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="55786-129">If a [**PnPXDeviceCategory**](pnpxdevicecategory.md) element is present, then at least one **hosted** element must contain both [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements.</span></span> <span data-ttu-id="55786-130">Ebenso muss, wenn **pnpxhardwareid** -und **pnpxcompatibleid-** Elemente in einem **gehosteten** Element vorhanden sind, mindestens ein **pnpxenvicecategory** -Element im [**thismodelmetadata**](thismodelmetadata.md) -Element vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="55786-130">Similarly, if **PnPXHardwareId** and **PnPXCompatibleId** elements are present in a **hosted** element, at least one **PnPXDeviceCategory** element must be present inside the [**thisModelMetadata**](thismodelmetadata.md) element.</span></span>

## <a name="element-information"></a><span data-ttu-id="55786-131">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="55786-131">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="55786-132">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="55786-132">Minimum supported system</span></span><br/> | <span data-ttu-id="55786-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="55786-133">Windows Vista</span></span> |
| <span data-ttu-id="55786-134">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="55786-134">Can be empty</span></span>                        | <span data-ttu-id="55786-135">Nein</span><span class="sxs-lookup"><span data-stu-id="55786-135">No</span></span>            |



 

 




