---
description: Definiert die Hersteller- und Modellmetadaten für das zu implementierte Gerät. Dieses Element wird nur für Geräteimplementierungen (Hosts) verwendet.
ms.assetid: 2ebd3092-39aa-469c-a8c9-23f373ba0e66
title: thisModelMetadata-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 872bcdfcf3f93bfc8fe307684c31cdebb2000b05
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995337"
---
# <a name="thismodelmetadata-element"></a><span data-ttu-id="d1eac-104">thisModelMetadata-Element</span><span class="sxs-lookup"><span data-stu-id="d1eac-104">thisModelMetadata element</span></span>

<span data-ttu-id="d1eac-105">Definiert die Hersteller- und Modellmetadaten für das zu implementierte Gerät.</span><span class="sxs-lookup"><span data-stu-id="d1eac-105">Defines the manufacturer and model metadata for the device to be implemented.</span></span> <span data-ttu-id="d1eac-106">Dieses Element wird nur für Geräteimplementierungen (Hosts) verwendet.</span><span class="sxs-lookup"><span data-stu-id="d1eac-106">This element is used for device implementations (hosts) only.</span></span>

## <a name="usage"></a><span data-ttu-id="d1eac-107">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="d1eac-107">Usage</span></span>

``` syntax
<thisModelMetadata>
  child elements
</thisModelMetadata>
```

## <a name="attributes"></a><span data-ttu-id="d1eac-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d1eac-108">Attributes</span></span>

<span data-ttu-id="d1eac-109">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="d1eac-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="d1eac-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d1eac-110">Child elements</span></span>



| <span data-ttu-id="d1eac-111">Element</span><span class="sxs-lookup"><span data-stu-id="d1eac-111">Element</span></span>                                                     | <span data-ttu-id="d1eac-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d1eac-112">Description</span></span>                                                                                                                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1eac-113">**Hersteller**</span><span class="sxs-lookup"><span data-stu-id="d1eac-113">**manufacturer**</span></span>](manufacturer.md)<br/>             | <span data-ttu-id="d1eac-114">Name des Herstellers.</span><span class="sxs-lookup"><span data-stu-id="d1eac-114">Name of the manufacturer.</span></span> <span data-ttu-id="d1eac-115">Mindestens eine von [**manufacturer oder**](manufacturer.md) [**manufacturerLS**](manufacturerls.md) muss in den Metadaten vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="d1eac-115">At least one of [**manufacturer**](manufacturer.md) or [**manufacturerLS**](manufacturerls.md) must be present in the metadata.</span></span><br/> <br/> |
| [<span data-ttu-id="d1eac-116">**manufacturerLS**</span><span class="sxs-lookup"><span data-stu-id="d1eac-116">**manufacturerLS**</span></span>](manufacturerls.md)<br/>         | <span data-ttu-id="d1eac-117">Lokalisierte Version des Herstellernamens.</span><span class="sxs-lookup"><span data-stu-id="d1eac-117">Localized version of the manufacturer name.</span></span><br/> <br/>                                                                                                                 |
| [<span data-ttu-id="d1eac-118">**manufacturerURL**</span><span class="sxs-lookup"><span data-stu-id="d1eac-118">**manufacturerURL**</span></span>](manufacturerurl.md)<br/>       | <span data-ttu-id="d1eac-119">URL-Adresse des Herstellers.</span><span class="sxs-lookup"><span data-stu-id="d1eac-119">Manufacturer URL address.</span></span><br/> <br/>                                                                                                                                   |
| [<span data-ttu-id="d1eac-120">**modelName**</span><span class="sxs-lookup"><span data-stu-id="d1eac-120">**modelName**</span></span>](modelname.md)<br/>                   | <span data-ttu-id="d1eac-121">Der Name des Geräts.</span><span class="sxs-lookup"><span data-stu-id="d1eac-121">Name of the device.</span></span> <span data-ttu-id="d1eac-122">In den Metadaten [**muss mindestens modelName**](modelname.md) oder [**modelNameLS**](modelnamels.md) vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="d1eac-122">At least one of [**modelName**](modelname.md) or [**modelNameLS**](modelnamels.md) must be present in the metadata.</span></span><br/> <br/>                   |
| [<span data-ttu-id="d1eac-123">**modelNameLS**</span><span class="sxs-lookup"><span data-stu-id="d1eac-123">**modelNameLS**</span></span>](modelnamels.md)<br/>               | <span data-ttu-id="d1eac-124">Lokalisierte Version des Gerätenamens.</span><span class="sxs-lookup"><span data-stu-id="d1eac-124">Localized version of the device name.</span></span><br/> <br/>                                                                                                                       |
| [<span data-ttu-id="d1eac-125">**modelNumber**</span><span class="sxs-lookup"><span data-stu-id="d1eac-125">**modelNumber**</span></span>](modelnumber.md)<br/>               | <span data-ttu-id="d1eac-126">Modellnummer des Geräts.</span><span class="sxs-lookup"><span data-stu-id="d1eac-126">Model number of the device.</span></span><br/> <br/>                                                                                                                                 |
| [<span data-ttu-id="d1eac-127">**modelURL**</span><span class="sxs-lookup"><span data-stu-id="d1eac-127">**modelURL**</span></span>](modelurl.md)<br/>                     | <span data-ttu-id="d1eac-128">URL-Adresse für das Gerätemodell.</span><span class="sxs-lookup"><span data-stu-id="d1eac-128">URL address for the device model.</span></span><br/> <br/>                                                                                                                           |
| [<span data-ttu-id="d1eac-129">**PnPXDeviceCategory**</span><span class="sxs-lookup"><span data-stu-id="d1eac-129">**PnPXDeviceCategory**</span></span>](pnpxdevicecategory.md)<br/> | <span data-ttu-id="d1eac-130">PnP-X-Kategorie, zu der das Gerät gehört.</span><span class="sxs-lookup"><span data-stu-id="d1eac-130">PnP-X category to which the device belongs.</span></span> <br/> <br/>                                                                                                                |
| [<span data-ttu-id="d1eac-131">**presentationURL**</span><span class="sxs-lookup"><span data-stu-id="d1eac-131">**presentationURL**</span></span>](presentationurl.md)<br/>       | <span data-ttu-id="d1eac-132">URL-Adresse der Präsentationsdaten des Gerätemodells.</span><span class="sxs-lookup"><span data-stu-id="d1eac-132">URL address of the device model's presentation data.</span></span><br/> <br/>                                                                                                        |



### <a name="child-element-sequence"></a><span data-ttu-id="d1eac-133">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="d1eac-133">Child element sequence</span></span>

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

## <a name="parent-elements"></a><span data-ttu-id="d1eac-134">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d1eac-134">Parent elements</span></span>



| <span data-ttu-id="d1eac-135">Element</span><span class="sxs-lookup"><span data-stu-id="d1eac-135">Element</span></span>                                     | <span data-ttu-id="d1eac-136">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d1eac-136">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1eac-137">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="d1eac-137">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="d1eac-138">Das Stammelement einer WSDAPI-Codegenerator-XML-Skriptdatei.</span><span class="sxs-lookup"><span data-stu-id="d1eac-138">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="d1eac-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d1eac-139">Remarks</span></span>

<span data-ttu-id="d1eac-140">Die Herstellermetadaten entsprechen dem Abschnitt mit den Herstellermetadaten, der im Geräteprofil beschrieben ist (details finden Sie im Geräteprofil).</span><span class="sxs-lookup"><span data-stu-id="d1eac-140">The manufacturer metadata matches the manufacturer metadata section described in the device profile (consult the device profile for details).</span></span> <span data-ttu-id="d1eac-141">Der Herstellername oder mindestens eine lokalisierte Version des Herstellernamens muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d1eac-141">The manufacturer name or at least one localized version of the manufacturer name must be provided.</span></span> <span data-ttu-id="d1eac-142">Der Modellname oder mindestens eine lokalisierte Version des Modellnamens muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d1eac-142">The model name or at least one localized version of the model name must be provided.</span></span>

<span data-ttu-id="d1eac-143">Das [**thisModelMetadataDefinition-Element**](thismodelmetadatadefinition.md) wird anschließend verwendet, um eine C-Konstante zu generieren, die diese Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="d1eac-143">The [**thisModelMetadataDefinition**](thismodelmetadatadefinition.md) element is subsequently used to generate a C constant containing this information.</span></span>

<span data-ttu-id="d1eac-144">Wenn ein [**PnPXDeviceCategory-Element**](pnpxdevicecategory.md) vorhanden ist, muss mindestens ein [**gehostetes**](hosted.md) Element sowohl [**PnPXHardwareId-**](pnpxhardwareid.md) als auch [**PnPXCompatibleId-Elemente**](pnpxcompatibleid.md) enthalten.</span><span class="sxs-lookup"><span data-stu-id="d1eac-144">If a [**PnPXDeviceCategory**](pnpxdevicecategory.md) element is present, then at least one [**hosted**](hosted.md) element must contain both [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements.</span></span> <span data-ttu-id="d1eac-145">Wenn **PnPXHardwareId-** und **PnPXCompatibleId-Elemente** in einem **gehosteten** Element vorhanden sind, muss ein **PnPXDeviceCategory-Element** innerhalb des **thisModelMetadata-Elements** vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="d1eac-145">Similarly, if **PnPXHardwareId** and **PnPXCompatibleId** elements are present in a **hosted** element, a **PnPXDeviceCategory** element must be present inside the **thisModelMetadata** element.</span></span>

## <a name="element-information"></a><span data-ttu-id="d1eac-146">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="d1eac-146">Element information</span></span>



| <span data-ttu-id="d1eac-147">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="d1eac-147">Label</span></span> | <span data-ttu-id="d1eac-148">Wert</span><span class="sxs-lookup"><span data-stu-id="d1eac-148">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="d1eac-149">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="d1eac-149">Minimum supported system</span></span><br/> | <span data-ttu-id="d1eac-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1eac-150">Windows Vista</span></span> |
| <span data-ttu-id="d1eac-151">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="d1eac-151">Can be empty</span></span>                        | <span data-ttu-id="d1eac-152">Nein</span><span class="sxs-lookup"><span data-stu-id="d1eac-152">No</span></span>            |



 

 




