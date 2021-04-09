---
description: Definiert die Hersteller-und Modell Metadaten für das zu implementierende Gerät. Dieses Element wird nur für Geräte Implementierungen (Hosts) verwendet.
ms.assetid: 2ebd3092-39aa-469c-a8c9-23f373ba0e66
title: thismodelmetadata-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c1a35d6449d4e8bba0ecf79e7dc87b00dee894b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867600"
---
# <a name="thismodelmetadata-element"></a><span data-ttu-id="b52be-104">thismodelmetadata-Element</span><span class="sxs-lookup"><span data-stu-id="b52be-104">thisModelMetadata element</span></span>

<span data-ttu-id="b52be-105">Definiert die Hersteller-und Modell Metadaten für das zu implementierende Gerät.</span><span class="sxs-lookup"><span data-stu-id="b52be-105">Defines the manufacturer and model metadata for the device to be implemented.</span></span> <span data-ttu-id="b52be-106">Dieses Element wird nur für Geräte Implementierungen (Hosts) verwendet.</span><span class="sxs-lookup"><span data-stu-id="b52be-106">This element is used for device implementations (hosts) only.</span></span>

## <a name="usage"></a><span data-ttu-id="b52be-107">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="b52be-107">Usage</span></span>

``` syntax
<thisModelMetadata>
  child elements
</thisModelMetadata>
```

## <a name="attributes"></a><span data-ttu-id="b52be-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b52be-108">Attributes</span></span>

<span data-ttu-id="b52be-109">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="b52be-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b52be-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b52be-110">Child elements</span></span>



| <span data-ttu-id="b52be-111">Element</span><span class="sxs-lookup"><span data-stu-id="b52be-111">Element</span></span>                                                     | <span data-ttu-id="b52be-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b52be-112">Description</span></span>                                                                                                                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b52be-113">**Bauers**</span><span class="sxs-lookup"><span data-stu-id="b52be-113">**manufacturer**</span></span>](manufacturer.md)<br/>             | <span data-ttu-id="b52be-114">Der Name des Herstellers.</span><span class="sxs-lookup"><span data-stu-id="b52be-114">Name of the manufacturer.</span></span> <span data-ttu-id="b52be-115">In den Metadaten muss mindestens einer der [**Hersteller**](manufacturer.md) oder [**manufacturerls**](manufacturerls.md) vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="b52be-115">At least one of [**manufacturer**](manufacturer.md) or [**manufacturerLS**](manufacturerls.md) must be present in the metadata.</span></span><br/> <br/> |
| [<span data-ttu-id="b52be-116">**manufacturerls**</span><span class="sxs-lookup"><span data-stu-id="b52be-116">**manufacturerLS**</span></span>](manufacturerls.md)<br/>         | <span data-ttu-id="b52be-117">Lokalisierte Version des Hersteller namens.</span><span class="sxs-lookup"><span data-stu-id="b52be-117">Localized version of the manufacturer name.</span></span><br/> <br/>                                                                                                                 |
| [<span data-ttu-id="b52be-118">**ManufacturerUrl**</span><span class="sxs-lookup"><span data-stu-id="b52be-118">**manufacturerURL**</span></span>](manufacturerurl.md)<br/>       | <span data-ttu-id="b52be-119">Die URL-Adresse des Herstellers.</span><span class="sxs-lookup"><span data-stu-id="b52be-119">Manufacturer URL address.</span></span><br/> <br/>                                                                                                                                   |
| [<span data-ttu-id="b52be-120">**modelName**</span><span class="sxs-lookup"><span data-stu-id="b52be-120">**modelName**</span></span>](modelname.md)<br/>                   | <span data-ttu-id="b52be-121">Der Name des Geräts.</span><span class="sxs-lookup"><span data-stu-id="b52be-121">Name of the device.</span></span> <span data-ttu-id="b52be-122">In den Metadaten muss mindestens eine von [**modelname**](modelname.md) oder [**modelnamels**](modelnamels.md) vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="b52be-122">At least one of [**modelName**](modelname.md) or [**modelNameLS**](modelnamels.md) must be present in the metadata.</span></span><br/> <br/>                   |
| [<span data-ttu-id="b52be-123">**modelnamels**</span><span class="sxs-lookup"><span data-stu-id="b52be-123">**modelNameLS**</span></span>](modelnamels.md)<br/>               | <span data-ttu-id="b52be-124">Lokalisierte Version des Geräte namens.</span><span class="sxs-lookup"><span data-stu-id="b52be-124">Localized version of the device name.</span></span><br/> <br/>                                                                                                                       |
| [<span data-ttu-id="b52be-125">**modelnumber**</span><span class="sxs-lookup"><span data-stu-id="b52be-125">**modelNumber**</span></span>](modelnumber.md)<br/>               | <span data-ttu-id="b52be-126">Modellnummer des Geräts.</span><span class="sxs-lookup"><span data-stu-id="b52be-126">Model number of the device.</span></span><br/> <br/>                                                                                                                                 |
| [<span data-ttu-id="b52be-127">**modelurl**</span><span class="sxs-lookup"><span data-stu-id="b52be-127">**modelURL**</span></span>](modelurl.md)<br/>                     | <span data-ttu-id="b52be-128">Die URL-Adresse für das Gerätemodell.</span><span class="sxs-lookup"><span data-stu-id="b52be-128">URL address for the device model.</span></span><br/> <br/>                                                                                                                           |
| [<span data-ttu-id="b52be-129">**Pnpxde vicecategory**</span><span class="sxs-lookup"><span data-stu-id="b52be-129">**PnPXDeviceCategory**</span></span>](pnpxdevicecategory.md)<br/> | <span data-ttu-id="b52be-130">PnP-X-Kategorie, zu der das Gerät gehört.</span><span class="sxs-lookup"><span data-stu-id="b52be-130">PnP-X category to which the device belongs.</span></span> <br/> <br/>                                                                                                                |
| [<span data-ttu-id="b52be-131">**presentationurl**</span><span class="sxs-lookup"><span data-stu-id="b52be-131">**presentationURL**</span></span>](presentationurl.md)<br/>       | <span data-ttu-id="b52be-132">Die URL-Adresse der Präsentationsdaten des Geräte Modells.</span><span class="sxs-lookup"><span data-stu-id="b52be-132">URL address of the device model's presentation data.</span></span><br/> <br/>                                                                                                        |



### <a name="child-element-sequence"></a><span data-ttu-id="b52be-133">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="b52be-133">Child element sequence</span></span>

``` syntax
(
  manufacturer?, 
  manufacturerLS*, 
  manufacturerURL?, 
  modelName?, 
  modelNameLS*, 
  modelNumber, 
  modelURL?, 
  PnPXDeviceCategory?, 
  presentationURL?
)
```

## <a name="parent-elements"></a><span data-ttu-id="b52be-134">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b52be-134">Parent elements</span></span>



| <span data-ttu-id="b52be-135">Element</span><span class="sxs-lookup"><span data-stu-id="b52be-135">Element</span></span>                                     | <span data-ttu-id="b52be-136">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b52be-136">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="b52be-137">**wsdcodegen**</span><span class="sxs-lookup"><span data-stu-id="b52be-137">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="b52be-138">Das Stamm Element einer XML-Skriptdatei des WSDAPI-Code-Generators.</span><span class="sxs-lookup"><span data-stu-id="b52be-138">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="b52be-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b52be-139">Remarks</span></span>

<span data-ttu-id="b52be-140">Die Hersteller Metadaten stimmen mit dem im Geräte Profil beschriebenen Abschnitt der Hersteller Metadaten überein (Weitere Informationen finden Sie im Geräte Profil).</span><span class="sxs-lookup"><span data-stu-id="b52be-140">The manufacturer metadata matches the manufacturer metadata section described in the device profile (consult the device profile for details).</span></span> <span data-ttu-id="b52be-141">Der Herstellername oder mindestens eine lokalisierte Version des Hersteller namens muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b52be-141">The manufacturer name or at least one localized version of the manufacturer name must be provided.</span></span> <span data-ttu-id="b52be-142">Der Modellname oder mindestens eine lokalisierte Version des Modell namens muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b52be-142">The model name or at least one localized version of the model name must be provided.</span></span>

<span data-ttu-id="b52be-143">Anschließend wird das [**thisModelMetadataDefinition**](thismodelmetadatadefinition.md) -Element verwendet, um eine C-Konstante zu generieren, die diese Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="b52be-143">The [**thisModelMetadataDefinition**](thismodelmetadatadefinition.md) element is subsequently used to generate a C constant containing this information.</span></span>

<span data-ttu-id="b52be-144">Wenn ein [**pnpxenvicecategory**](pnpxdevicecategory.md) -Element vorhanden ist, muss mindestens ein [**gehosteter**](hosted.md) -Element sowohl [**pnpxhardwareid**](pnpxhardwareid.md) -als auch [**pnpxcompatibleid-**](pnpxcompatibleid.md) Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="b52be-144">If a [**PnPXDeviceCategory**](pnpxdevicecategory.md) element is present, then at least one [**hosted**](hosted.md) element must contain both [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements.</span></span> <span data-ttu-id="b52be-145">Ebenso muss, wenn **pnpxhardwareid** -und **pnpxcompatibleid-** Elemente in einem **gehosteten** Element vorhanden sind, ein **pnpxenvicecategory** -Element im **thismodelmetadata** -Element vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="b52be-145">Similarly, if **PnPXHardwareId** and **PnPXCompatibleId** elements are present in a **hosted** element, a **PnPXDeviceCategory** element must be present inside the **thisModelMetadata** element.</span></span>

## <a name="element-information"></a><span data-ttu-id="b52be-146">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="b52be-146">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="b52be-147">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="b52be-147">Minimum supported system</span></span><br/> | <span data-ttu-id="b52be-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b52be-148">Windows Vista</span></span> |
| <span data-ttu-id="b52be-149">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="b52be-149">Can be empty</span></span>                        | <span data-ttu-id="b52be-150">Nein</span><span class="sxs-lookup"><span data-stu-id="b52be-150">No</span></span>            |



 

 




