---
description: Definiert die Elemente ServiceID, Types, PnPXHardwareId und PnPXCompatibleId für die vom Diensthost definierten Dienste.
ms.assetid: f901a88f-7e01-4e7f-a0f2-59f2a01b03cd
title: Gehostetes Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3d281b5e058f8716c12c655ebcdb9a17bdfa4fb
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994887"
---
# <a name="hosted-element"></a><span data-ttu-id="120e5-103">Gehostetes Element</span><span class="sxs-lookup"><span data-stu-id="120e5-103">hosted element</span></span>

<span data-ttu-id="120e5-104">Definiert die Elemente [**ServiceID,**](serviceid.md) [**Types,**](types.md)[**PnPXHardwareId**](pnpxhardwareid.md)und [**PnPXCompatibleId**](pnpxcompatibleid.md) für die vom Diensthost definierten Dienste.</span><span class="sxs-lookup"><span data-stu-id="120e5-104">Defines the [**ServiceID**](serviceid.md), [**Types**](types.md),[**PnPXHardwareId**](pnpxhardwareid.md), and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements for the services defined by the service host.</span></span>

## <a name="usage"></a><span data-ttu-id="120e5-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="120e5-105">Usage</span></span>

``` syntax
<hosted>
  child elements
</hosted>
```

## <a name="attributes"></a><span data-ttu-id="120e5-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="120e5-106">Attributes</span></span>

<span data-ttu-id="120e5-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="120e5-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="120e5-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="120e5-108">Child elements</span></span>



| <span data-ttu-id="120e5-109">Element</span><span class="sxs-lookup"><span data-stu-id="120e5-109">Element</span></span>                                                 | <span data-ttu-id="120e5-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="120e5-110">Description</span></span>                                                                      |
|---------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="120e5-111">**PnPXCompatibleId**</span><span class="sxs-lookup"><span data-stu-id="120e5-111">**PnPXCompatibleId**</span></span>](pnpxcompatibleid.md)<br/> | <span data-ttu-id="120e5-112">Gibt den PnP-X-kompatiblen Bezeichner des Diensts an.</span><span class="sxs-lookup"><span data-stu-id="120e5-112">Specifies the PnP-X Compatible Identifier of the service.</span></span><br/> <br/> |
| [<span data-ttu-id="120e5-113">**PnPXHardwareId**</span><span class="sxs-lookup"><span data-stu-id="120e5-113">**PnPXHardwareId**</span></span>](pnpxhardwareid.md)<br/>     | <span data-ttu-id="120e5-114">Gibt den PnP-X-Hardwarebezeichner des Diensts an.</span><span class="sxs-lookup"><span data-stu-id="120e5-114">Specifies the PnP-X Hardware Identifier of the service.</span></span><br/> <br/>   |
| [<span data-ttu-id="120e5-115">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="120e5-115">**ServiceID**</span></span>](serviceid.md)<br/>               | <span data-ttu-id="120e5-116">Definiert einen Dienstbezeichner für den Diensthost.</span><span class="sxs-lookup"><span data-stu-id="120e5-116">Defines a service identifier for the service host.</span></span><br/> <br/>        |
| [<span data-ttu-id="120e5-117">**Typen**</span><span class="sxs-lookup"><span data-stu-id="120e5-117">**Types**</span></span>](types.md)<br/>                       | <span data-ttu-id="120e5-118">Definiert eine Liste der qualifizierten XSD-Namen.</span><span class="sxs-lookup"><span data-stu-id="120e5-118">Defines a list of XSD qualified names.</span></span><br/> <br/>                    |



### <a name="child-element-sequence"></a><span data-ttu-id="120e5-119">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="120e5-119">Child element sequence</span></span>

``` syntax
(
  ServiceID, 
  Types, 
  PnPXHardwareId?, 
  PnPXCompatibleId?
)
```

## <a name="parent-elements"></a><span data-ttu-id="120e5-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="120e5-120">Parent elements</span></span>



| <span data-ttu-id="120e5-121">Element</span><span class="sxs-lookup"><span data-stu-id="120e5-121">Element</span></span>                                         | <span data-ttu-id="120e5-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="120e5-122">Description</span></span>                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="120e5-123">**hostMetadata**</span><span class="sxs-lookup"><span data-stu-id="120e5-123">**hostMetadata**</span></span>](hostmetadata.md)<br/> | <span data-ttu-id="120e5-124">Die Hostingmetadaten für das zu implementierende Gerät.</span><span class="sxs-lookup"><span data-stu-id="120e5-124">The hosting metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="120e5-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="120e5-125">Remarks</span></span>

<span data-ttu-id="120e5-126">Jeder von einem Diensthost bereitgestellte Dienst sollte über eigene Informationen zu **gehosteten** Elementen verfügen, um sicherzustellen, dass der Dienst ordnungsgemäß als Antwort auf Metadatenanforderungen veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="120e5-126">Each service provided by a service host should have its own **hosted** element information to ensure that the service is published properly in responses to metadata requests.</span></span>

<span data-ttu-id="120e5-127">Die [**Elemente PnPXHardwareId**](pnpxhardwareid.md) und [**PnPXCompatibleId**](pnpxcompatibleid.md) sind optional, müssen jedoch zusammen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="120e5-127">The [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements are optional, but when used, they must be used together.</span></span> <span data-ttu-id="120e5-128">Wenn eine vorhanden ist, muss auch die andere vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="120e5-128">If one is present, the other must be present as well.</span></span>

<span data-ttu-id="120e5-129">Wenn ein [**PnPXDeviceCategory-Element**](pnpxdevicecategory.md) vorhanden ist, muss mindestens ein **gehostetes** Element sowohl [**PnPXHardwareId-**](pnpxhardwareid.md) als auch [**PnPXCompatibleId-Elemente**](pnpxcompatibleid.md) enthalten.</span><span class="sxs-lookup"><span data-stu-id="120e5-129">If a [**PnPXDeviceCategory**](pnpxdevicecategory.md) element is present, then at least one **hosted** element must contain both [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements.</span></span> <span data-ttu-id="120e5-130">Wenn **PnPXHardwareId-** und **PnPXCompatibleId-Elemente** in einem **gehosteten** Element vorhanden sind, muss mindestens ein **PnPXDeviceCategory-Element** innerhalb des [**thisModelMetadata-Elements**](thismodelmetadata.md) vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="120e5-130">Similarly, if **PnPXHardwareId** and **PnPXCompatibleId** elements are present in a **hosted** element, at least one **PnPXDeviceCategory** element must be present inside the [**thisModelMetadata**](thismodelmetadata.md) element.</span></span>

## <a name="element-information"></a><span data-ttu-id="120e5-131">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="120e5-131">Element information</span></span>



| <span data-ttu-id="120e5-132">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="120e5-132">Label</span></span> | <span data-ttu-id="120e5-133">Wert</span><span class="sxs-lookup"><span data-stu-id="120e5-133">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="120e5-134">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="120e5-134">Minimum supported system</span></span><br/> | <span data-ttu-id="120e5-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="120e5-135">Windows Vista</span></span> |
| <span data-ttu-id="120e5-136">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="120e5-136">Can be empty</span></span>                        | <span data-ttu-id="120e5-137">Nein</span><span class="sxs-lookup"><span data-stu-id="120e5-137">No</span></span>            |



 

 




