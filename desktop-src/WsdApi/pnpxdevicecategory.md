---
description: Gibt die PnP-X-Kategorie an, zu der das Gerät gehört. Es können mehr als eine Kategorie angegeben werden.
ms.assetid: 1ca46000-4700-4326-8f49-1b9a22d45bfa
title: Pnpxdebug-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 731dd78fbe366fc9c7923686d3d9ac90b772c23d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363495"
---
# <a name="pnpxdevicecategory-element"></a><span data-ttu-id="4c08e-104">Pnpxdebug-Element</span><span class="sxs-lookup"><span data-stu-id="4c08e-104">PnPXDeviceCategory element</span></span>

<span data-ttu-id="4c08e-105">Gibt die PnP-X-Kategorie an, zu der das Gerät gehört.</span><span class="sxs-lookup"><span data-stu-id="4c08e-105">Specifies the PnP-X category to which the device belongs.</span></span> <span data-ttu-id="4c08e-106">Es können mehr als eine Kategorie angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4c08e-106">More than one category can be specified.</span></span>

## <a name="usage"></a><span data-ttu-id="4c08e-107">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="4c08e-107">Usage</span></span>

``` syntax
<PnPXDeviceCategory/>
```

## <a name="attributes"></a><span data-ttu-id="4c08e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4c08e-108">Attributes</span></span>

<span data-ttu-id="4c08e-109">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="4c08e-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="4c08e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4c08e-110">Child elements</span></span>

<span data-ttu-id="4c08e-111">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="4c08e-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="4c08e-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4c08e-112">Parent elements</span></span>



| <span data-ttu-id="4c08e-113">Element</span><span class="sxs-lookup"><span data-stu-id="4c08e-113">Element</span></span>                                                   | <span data-ttu-id="4c08e-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4c08e-114">Description</span></span>                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4c08e-115">**thismodelmetadata**</span><span class="sxs-lookup"><span data-stu-id="4c08e-115">**thisModelMetadata**</span></span>](thismodelmetadata.md)<br/> | <span data-ttu-id="4c08e-116">Definiert die Hersteller-und Modell Metadaten für das zu implementierende Gerät.</span><span class="sxs-lookup"><span data-stu-id="4c08e-116">Defines the manufacturer and model metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="4c08e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4c08e-117">Remarks</span></span>

<span data-ttu-id="4c08e-118">Geräte können auch eine Geräte Unterkategorie für eine beschreibende Gerätekategorie angeben.</span><span class="sxs-lookup"><span data-stu-id="4c08e-118">Devices can also specify a device subcategory for a more descriptive device category.</span></span> <span data-ttu-id="4c08e-119">Beispielsweise identifiziert "Phones. WindowsMobile Kameras. digitalstillcamera mediadevices. Musicplayer" ein Gerät, das ein Microsoft Windows Mobile-Gerät mit einer Kamera und einem Musikplayer ist.</span><span class="sxs-lookup"><span data-stu-id="4c08e-119">For example, "Phones.WindowsMobile Cameras.DigitalStillCamera MediaDevices.MusicPlayer" identifies a device that is a Microsoft Windows Mobile  device with a camera and music player.</span></span> <span data-ttu-id="4c08e-120">Die primäre Gerätekategorie für dieses Gerät wäre "Smartphones".</span><span class="sxs-lookup"><span data-stu-id="4c08e-120">The primary device category for this device would be "Phones".</span></span>

<span data-ttu-id="4c08e-121">Wenn Sie mehr als eine Gerätekategorie angeben möchten, trennen Sie die Kategorien durch ein Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="4c08e-121">To specify more than one device category, separate the categories with a space.</span></span> <span data-ttu-id="4c08e-122">Beispielsweise identifiziert "Drucker Speicher" ein Gerät mit der primär Kategorie "Drucker" und der sekundären Kategorie "Speicher".</span><span class="sxs-lookup"><span data-stu-id="4c08e-122">For example, "Printers Storage" identifies a device with a primary category of "Printers" and a secondary category of "Storage".</span></span>

<span data-ttu-id="4c08e-123">Wenn ein **pnpxenvicecategory** -Element vorhanden ist, sollte mindestens ein [**gehosteter**](hosted.md) -Element sowohl [**pnpxhardwareid**](pnpxhardwareid.md) -als auch [**pnpxcompatibleid-**](pnpxcompatibleid.md) Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="4c08e-123">If a **PnPXDeviceCategory** element is present, then at least one [**hosted**](hosted.md) element should contain both [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements.</span></span> <span data-ttu-id="4c08e-124">Ebenso muss, wenn **pnpxhardwareid** -und **pnpxcompatibleid-** Elemente in einem **gehosteten** Element vorhanden sind, mindestens ein **pnpxenvicecategory** -Element im [**thismodelmetadata**](thismodelmetadata.md) -Element vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="4c08e-124">Similarly, if **PnPXHardwareId** and **PnPXCompatibleId** elements are present in a **hosted** element, at least one **PnPXDeviceCategory** element should be present inside the [**thisModelMetadata**](thismodelmetadata.md) element.</span></span>

## <a name="element-information"></a><span data-ttu-id="4c08e-125">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="4c08e-125">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="4c08e-126">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="4c08e-126">Minimum supported system</span></span><br/> | <span data-ttu-id="4c08e-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4c08e-127">Windows Vista</span></span> |
| <span data-ttu-id="4c08e-128">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="4c08e-128">Can be empty</span></span>                        | <span data-ttu-id="4c08e-129">Ja</span><span class="sxs-lookup"><span data-stu-id="4c08e-129">Yes</span></span>           |



 

 




