---
title: Image-Element (WMP-SDK)
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Image-Element (WMP-SDK)
ms.assetid: 06804c26-e847-43a7-bb75-60da600c7d4f
keywords:
- Bild Element Windows-Media Player
topic_type:
- apiref
api_name:
- Image Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c10b62365453f395c1aaf373e355c21260900f8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360959"
---
# <a name="image-element-wmp-sdk"></a><span data-ttu-id="dba5e-105">Image-Element (WMP-SDK)</span><span class="sxs-lookup"><span data-stu-id="dba5e-105">Image Element (WMP SDK)</span></span>

> [!Note]  
> <span data-ttu-id="dba5e-106">In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores</span><span class="sxs-lookup"><span data-stu-id="dba5e-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="dba5e-107">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dba5e-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="dba5e-108">Das **Image** -Element gibt die Bilder an, die von Windows Media Player dem Benutzer angezeigt werden, um den Online Store darzustellen.</span><span class="sxs-lookup"><span data-stu-id="dba5e-108">The **Image** element specifies the images that Windows Media Player displays to the user to represent the online store.</span></span>

``` syntax
<Image
    EulaURL = "URL"
    MenuURL = "URL"
    ServiceLargeURL = "URL"
    ServiceSmallURL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="dba5e-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="dba5e-109">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="dba5e-110"><span id="EulaURL__required_for_type_1_stores__ignored_for_type_2_"></span><span id="eulaurl__required_for_type_1_stores__ignored_for_type_2_"></span><span id="EULAURL__REQUIRED_FOR_TYPE_1_STORES__IGNORED_FOR_TYPE_2_"></span>**Eulaurl** (erforderlich für den Speicher vom Typ 1, wird für Typ 2 ignoriert)</span><span class="sxs-lookup"><span data-stu-id="dba5e-110"><span id="EulaURL__required_for_type_1_stores__ignored_for_type_2_"></span><span id="eulaurl__required_for_type_1_stores__ignored_for_type_2_"></span><span id="EULAURL__REQUIRED_FOR_TYPE_1_STORES__IGNORED_FOR_TYPE_2_"></span>**EulaURL** (required for type 1 stores, ignored for type 2)</span></span>
</dt> <dd>

<span data-ttu-id="dba5e-111">Die URL für das Logo, das von Windows Media Player im Dialogfeld Endbenutzer-Lizenzvertrag (EULA) angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="dba5e-111">URL for the logo that Windows Media Player displays in the end user license agreement (EULA) dialog box.</span></span> <span data-ttu-id="dba5e-112">Dabei muss es sich um ein PNG-Bild handeln, das 80 x 80 Pixel ist.</span><span class="sxs-lookup"><span data-stu-id="dba5e-112">This must be a PNG image that is 80 x 80 pixels.</span></span>

</dd> <dt>

<span data-ttu-id="dba5e-113"><span id="MenuURL__optional_"></span><span id="menuurl__optional_"></span><span id="MENUURL__OPTIONAL_"></span>**Menuurl** (optional)</span><span class="sxs-lookup"><span data-stu-id="dba5e-113"><span id="MenuURL__optional_"></span><span id="menuurl__optional_"></span><span id="MENUURL__OPTIONAL_"></span>**MenuURL** (optional)</span></span>
</dt> <dd>

<span data-ttu-id="dba5e-114">Die URL für das Bild, das von Windows Media Player im Menü Dienste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="dba5e-114">URL for the image that Windows Media Player displays on the services menu.</span></span> <span data-ttu-id="dba5e-115">Dieses Bild muss 15 x 15 Pixel betragen.</span><span class="sxs-lookup"><span data-stu-id="dba5e-115">This image must be 15 x 15 pixels.</span></span>

</dd> <dt>

<span data-ttu-id="dba5e-116"><span id="ServiceLargeURL__optional_"></span><span id="servicelargeurl__optional_"></span><span id="SERVICELARGEURL__OPTIONAL_"></span>**Servicelargeurl** (optional)</span><span class="sxs-lookup"><span data-stu-id="dba5e-116"><span id="ServiceLargeURL__optional_"></span><span id="servicelargeurl__optional_"></span><span id="SERVICELARGEURL__OPTIONAL_"></span>**ServiceLargeURL** (optional)</span></span>
</dt> <dd>

<span data-ttu-id="dba5e-117">Bei einem Online Store vom Typ 1 ist dies die URL für das Image, das in Windows Media Player auf der Registerkarte " **Online Stores** " angezeigt wird. Für Windows Media Player 11 muss dieses Bild 45 Pixel breit und 13 Pixel hoch sein.</span><span class="sxs-lookup"><span data-stu-id="dba5e-117">For a type 1 online store, this is the URL for the image that Windows Media Player displays on the **Online Stores** tab. For Windows Media Player 11, this image must be 45 pixels wide by 13 pixels high.</span></span> <span data-ttu-id="dba5e-118">Bei Windows Media Player 12 muss dieses Bild 45 Pixel breit und 30 Pixel hoch sein.</span><span class="sxs-lookup"><span data-stu-id="dba5e-118">For Windows Media Player 12, this image must be 45 pixels wide by 30 pixels high.</span></span> <span data-ttu-id="dba5e-119">Um sowohl die Versionen 11 als auch 12 von Windows Media Player zu unterstützen, müssen Sie zwei separate ServiceInfo.xml Dokumente bereitstellen, von denen jedes auf das Bild der passenden Größe für servicelargeurl zeigt.</span><span class="sxs-lookup"><span data-stu-id="dba5e-119">To support both versions 11 and 12 of Windows Media Player, you must provide two separate ServiceInfo.xml documents, each of which points to the appropriately sized image for ServiceLargeURL.</span></span>

<span data-ttu-id="dba5e-120">Bei einem Online Store vom Typ 2 ist dies die URL für das Image, das in Windows Media Player neben der Registerkarte **Online Stores** oder neben den Schaltflächen für den Aufgabenbereich angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="dba5e-120">For a type 2 online store, this is the URL for the image that Windows Media Player displays beside the **Online Stores** tab or beside the task pane buttons.</span></span> <span data-ttu-id="dba5e-121">Dieses Bild muss 30 x 30 Pixel betragen.</span><span class="sxs-lookup"><span data-stu-id="dba5e-121">This image must be 30 x 30 pixels.</span></span>

</dd> <dt>

<span data-ttu-id="dba5e-122"><span id="ServiceSmallURL__optional_"></span><span id="servicesmallurl__optional_"></span><span id="SERVICESMALLURL__OPTIONAL_"></span>**Servicesmallurl** (optional)</span><span class="sxs-lookup"><span data-stu-id="dba5e-122"><span id="ServiceSmallURL__optional_"></span><span id="servicesmallurl__optional_"></span><span id="SERVICESMALLURL__OPTIONAL_"></span>**ServiceSmallURL** (optional)</span></span>
</dt> <dd>

<span data-ttu-id="dba5e-123">Die URL für das Logo, das zusammen mit der im **Description** -Element angegebenen Marketing Beschreibung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="dba5e-123">URL for the logo that is displayed along with the marketing description specified in the **Description** element.</span></span> <span data-ttu-id="dba5e-124">Wenn Sie nicht bereitgestellt wird, ist sie leer.</span><span class="sxs-lookup"><span data-stu-id="dba5e-124">If it is not supplied, it will be blank.</span></span> <span data-ttu-id="dba5e-125">(Alle Typen, optional) Dabei muss es sich um ein PNG-Bild handeln, das 45 Pixel breit und 13 Pixel hoch ist.</span><span class="sxs-lookup"><span data-stu-id="dba5e-125">(All types, optional) This must be a PNG image that is 45 pixels wide and 13 pixels high.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="dba5e-126">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="dba5e-126">Parent/Child Elements</span></span>



| <span data-ttu-id="dba5e-127">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="dba5e-127">Hierarchy</span></span>       | <span data-ttu-id="dba5e-128">Element</span><span class="sxs-lookup"><span data-stu-id="dba5e-128">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="dba5e-129">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dba5e-129">Parent elements</span></span> | <span data-ttu-id="dba5e-130">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="dba5e-130">**ServiceInfo**</span></span> |
| <span data-ttu-id="dba5e-131">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dba5e-131">Child elements</span></span>  | <span data-ttu-id="dba5e-132">Keine</span><span class="sxs-lookup"><span data-stu-id="dba5e-132">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="dba5e-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dba5e-133">Remarks</span></span>

<span data-ttu-id="dba5e-134">Die unterstützten Bildformate sind GIF, JPG, BMP und PNG (das empfohlene Format).</span><span class="sxs-lookup"><span data-stu-id="dba5e-134">The supported image formats are .gif, .jpg, .bmp, and .png (which is the recommended format).</span></span> <span data-ttu-id="dba5e-135">Die Verwendung von Webtransparenz wird unterstützt und empfohlen.</span><span class="sxs-lookup"><span data-stu-id="dba5e-135">Using Web transparency is both supported and recommended.</span></span> <span data-ttu-id="dba5e-136">Animierte GIF-Dateien werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dba5e-136">Animated GIF files are not supported.</span></span>

<span data-ttu-id="dba5e-137">Wenn Sie keinen Wert für **menuurl** angeben, zeigt Windows Media Player im Menü für den Online Shop keine Grafik an.</span><span class="sxs-lookup"><span data-stu-id="dba5e-137">If you do not supply a value for **MenuURL**, Windows Media Player displays no graphic on the menu for your online store.</span></span>

<span data-ttu-id="dba5e-138">Sie können ein animiertes Bild für servicelargeurl bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="dba5e-138">You can provide an animated image for ServiceLargeURL.</span></span> <span data-ttu-id="dba5e-139">In Windows Media Player 10 oder 11 ist das Bild animiert.</span><span class="sxs-lookup"><span data-stu-id="dba5e-139">In Windows Media Player 10 or 11, the image is animated.</span></span> <span data-ttu-id="dba5e-140">In Windows Media Player 12 wird nur der erste Frame des Bilds angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dba5e-140">In Windows Media Player 12, only the first frame of the image is displayed.</span></span> <span data-ttu-id="dba5e-141">Zum Bereitstellen eines animierten Bilds erstellen Sie eine einzelne Bilddatei, die aufeinander folgende Rahmen der Animation enthält.</span><span class="sxs-lookup"><span data-stu-id="dba5e-141">To provide an animated image, create a single image file that contains successive frames of your animation.</span></span> <span data-ttu-id="dba5e-142">Beispielsweise können Sie für ein Bild, das 30 Pixel breit und 30 Pixel hoch ist, 20 aufeinander folgende Bilder nebeneinander in einem Bild bereitstellen, das 600 Pixel breit und 30 Pixel hoch ist.</span><span class="sxs-lookup"><span data-stu-id="dba5e-142">For example, for an image that is 30 pixels wide and 30 pixels high, you could supply 20 successive images side by side in an image that is 600 pixels wide and 30 pixels high.</span></span> <span data-ttu-id="dba5e-143">Ein solches Bild wird von Windows Media Player automatisch animiert, indem die 20 einzelnen Bilder nacheinander angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="dba5e-143">Windows Media Player would automatically animate such an image by showing the 20 individual images one after another.</span></span> <span data-ttu-id="dba5e-144">Diese Animation tritt nur einmal auf, wenn der Online Shop geöffnet wird. der Vorgang wird nicht wiederholt.</span><span class="sxs-lookup"><span data-stu-id="dba5e-144">This animation occurs only once when the online store opens; it does not repeat.</span></span>

## <a name="requirements"></a><span data-ttu-id="dba5e-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dba5e-145">Requirements</span></span>



| <span data-ttu-id="dba5e-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dba5e-146">Requirement</span></span> | <span data-ttu-id="dba5e-147">Wert</span><span class="sxs-lookup"><span data-stu-id="dba5e-147">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="dba5e-148">Version</span><span class="sxs-lookup"><span data-stu-id="dba5e-148">Version</span></span><br/> | <span data-ttu-id="dba5e-149">Windows Media Player 10 oder höher</span><span class="sxs-lookup"><span data-stu-id="dba5e-149">Windows Media Player 10 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dba5e-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dba5e-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dba5e-151">**Beispiel eines serviceInfo-Dokuments für einen Online Store vom Typ 1**</span><span class="sxs-lookup"><span data-stu-id="dba5e-151">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="dba5e-152">**Beispiel eines serviceInfo-Dokuments für einen Typ 2-Online Store**</span><span class="sxs-lookup"><span data-stu-id="dba5e-152">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="dba5e-153">**Servicinfo-Dokument**</span><span class="sxs-lookup"><span data-stu-id="dba5e-153">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





