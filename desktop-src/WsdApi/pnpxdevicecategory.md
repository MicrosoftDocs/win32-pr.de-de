---
description: Gibt die PnP-X-Kategorie an, zu der das Gerät gehört. Es können mehrere Kategorien angegeben werden.
ms.assetid: 1ca46000-4700-4326-8f49-1b9a22d45bfa
title: PnPXDeviceCategory-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a08084d780c26d2f7fab902156939fd14a3e60c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996587"
---
# <a name="pnpxdevicecategory-element"></a><span data-ttu-id="f0e09-104">PnPXDeviceCategory-Element</span><span class="sxs-lookup"><span data-stu-id="f0e09-104">PnPXDeviceCategory element</span></span>

<span data-ttu-id="f0e09-105">Gibt die PnP-X-Kategorie an, zu der das Gerät gehört.</span><span class="sxs-lookup"><span data-stu-id="f0e09-105">Specifies the PnP-X category to which the device belongs.</span></span> <span data-ttu-id="f0e09-106">Es können mehrere Kategorien angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f0e09-106">More than one category can be specified.</span></span>

## <a name="usage"></a><span data-ttu-id="f0e09-107">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="f0e09-107">Usage</span></span>

``` syntax
<PnPXDeviceCategory/>
```

## <a name="attributes"></a><span data-ttu-id="f0e09-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f0e09-108">Attributes</span></span>

<span data-ttu-id="f0e09-109">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="f0e09-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f0e09-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f0e09-110">Child elements</span></span>

<span data-ttu-id="f0e09-111">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="f0e09-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="f0e09-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f0e09-112">Parent elements</span></span>



| <span data-ttu-id="f0e09-113">Element</span><span class="sxs-lookup"><span data-stu-id="f0e09-113">Element</span></span>                                                   | <span data-ttu-id="f0e09-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f0e09-114">Description</span></span>                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f0e09-115">**thisModelMetadata**</span><span class="sxs-lookup"><span data-stu-id="f0e09-115">**thisModelMetadata**</span></span>](thismodelmetadata.md)<br/> | <span data-ttu-id="f0e09-116">Definiert die Hersteller- und Modellmetadaten für das zu implementierende Gerät.</span><span class="sxs-lookup"><span data-stu-id="f0e09-116">Defines the manufacturer and model metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="f0e09-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f0e09-117">Remarks</span></span>

<span data-ttu-id="f0e09-118">Geräte können auch eine Geräteunterkategorie für eine beschreibendere Gerätekategorie angeben.</span><span class="sxs-lookup"><span data-stu-id="f0e09-118">Devices can also specify a device subcategory for a more descriptive device category.</span></span> <span data-ttu-id="f0e09-119">Beispielsweise identifiziert "Phones.WindowsMobile Cameras.DigitalZooCamera MediaDevices.MusicPlayer" ein Gerät, bei dem es sich um ein Microsoft Windows Mobile-Gerät mit einer Kamera und einem Musikplayer handelt.</span><span class="sxs-lookup"><span data-stu-id="f0e09-119">For example, "Phones.WindowsMobile Cameras.DigitalStillCamera MediaDevices.MusicPlayer" identifies a device that is a Microsoft Windows Mobile  device with a camera and music player.</span></span> <span data-ttu-id="f0e09-120">Die primäre Gerätekategorie für dieses Gerät wäre "Phones".</span><span class="sxs-lookup"><span data-stu-id="f0e09-120">The primary device category for this device would be "Phones".</span></span>

<span data-ttu-id="f0e09-121">Um mehr als eine Gerätekategorie anzugeben, trennen Sie die Kategorien durch ein Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="f0e09-121">To specify more than one device category, separate the categories with a space.</span></span> <span data-ttu-id="f0e09-122">Beispielsweise identifiziert "Druckerspeicher" ein Gerät mit der primären Kategorie "Drucker" und der sekundären Kategorie "Speicher".</span><span class="sxs-lookup"><span data-stu-id="f0e09-122">For example, "Printers Storage" identifies a device with a primary category of "Printers" and a secondary category of "Storage".</span></span>

<span data-ttu-id="f0e09-123">Wenn ein **PnPXDeviceCategory-Element** vorhanden ist, sollte mindestens ein [**gehostetes**](hosted.md) Element sowohl [**PnPXHardwareId-**](pnpxhardwareid.md) als auch [**PnPXCompatibleId-Elemente**](pnpxcompatibleid.md) enthalten.</span><span class="sxs-lookup"><span data-stu-id="f0e09-123">If a **PnPXDeviceCategory** element is present, then at least one [**hosted**](hosted.md) element should contain both [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements.</span></span> <span data-ttu-id="f0e09-124">Wenn **PnPXHardwareId-** und **PnPXCompatibleId-Elemente** in einem **gehosteten** Element vorhanden sind, sollte mindestens ein **PnPXDeviceCategory-Element** innerhalb des [**thisModelMetadata-Elements**](thismodelmetadata.md) vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="f0e09-124">Similarly, if **PnPXHardwareId** and **PnPXCompatibleId** elements are present in a **hosted** element, at least one **PnPXDeviceCategory** element should be present inside the [**thisModelMetadata**](thismodelmetadata.md) element.</span></span>

## <a name="element-information"></a><span data-ttu-id="f0e09-125">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="f0e09-125">Element information</span></span>



| <span data-ttu-id="f0e09-126">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="f0e09-126">Label</span></span> | <span data-ttu-id="f0e09-127">Wert</span><span class="sxs-lookup"><span data-stu-id="f0e09-127">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="f0e09-128">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="f0e09-128">Minimum supported system</span></span><br/> | <span data-ttu-id="f0e09-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f0e09-129">Windows Vista</span></span> |
| <span data-ttu-id="f0e09-130">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="f0e09-130">Can be empty</span></span>                        | <span data-ttu-id="f0e09-131">Ja</span><span class="sxs-lookup"><span data-stu-id="f0e09-131">Yes</span></span>           |



 

 




