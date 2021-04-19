---
title: ButtonGroup. mappingImage
description: Das mappingImage-Attribut gibt den Namen des Bilds an, das die Schaltflächen Zuordnung der ButtonGroup darstellt, oder ruft ihn ab.
ms.assetid: bfea52d1-0e7f-4f77-a212-d34e356a4d85
keywords:
- ButtonGroup. mappingImage-Fenster Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.mappingImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26e4afc44a00d5ce9b15ee01d4a0dc1aff52c555
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367694"
---
# <a name="buttongroupmappingimage"></a><span data-ttu-id="50aef-104">ButtonGroup. mappingImage</span><span class="sxs-lookup"><span data-stu-id="50aef-104">BUTTONGROUP.mappingImage</span></span>

<span data-ttu-id="50aef-105">Das **mappingImage** -Attribut gibt den Namen des Bilds an, das die Schaltflächen Zuordnung der **ButtonGroup** darstellt, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="50aef-105">The **mappingImage** attribute specifies or retrieves the name of the image representing the button map of the **BUTTONGROUP**.</span></span>

``` syntax
        elementID.mappingImage
```

## <a name="possible-values"></a><span data-ttu-id="50aef-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="50aef-106">Possible Values</span></span>

<span data-ttu-id="50aef-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="50aef-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="50aef-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50aef-108">Remarks</span></span>

<span data-ttu-id="50aef-109">Dies ist ein obligatorisches Attribut, das angegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="50aef-109">This is a mandatory attribute that must be specified.</span></span>

<span data-ttu-id="50aef-110">Das Zuordnungsbild sollte die gleichen Dimensionen wie das Haupt **Bild** sein.</span><span class="sxs-lookup"><span data-stu-id="50aef-110">The mapping image should be the same dimensions as the main **image**.</span></span> <span data-ttu-id="50aef-111">Dabei handelt es sich um eine Karte der durch Klicken aktivierbaren Bereiche des Haupt Bilds.</span><span class="sxs-lookup"><span data-stu-id="50aef-111">It is a map of the clickable areas of the main image.</span></span> <span data-ttu-id="50aef-112">Erstellen Sie die Zuordnung, indem Sie jeden klickbaren Bereich mit einer anderen Farbe ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="50aef-112">Construct the map by filling each clickable area with a different color.</span></span>

<span data-ttu-id="50aef-113">Wenn Sie die einzelnen **ButtonElement-Elemente** definieren, legen Sie Ihre Farbe mithilfe des **mappingColor** -Attributs aus der Zuordnung fest.</span><span class="sxs-lookup"><span data-stu-id="50aef-113">When defining each **BUTTONELEMENT**, designate its color from the map using the **mappingColor** attribute.</span></span> <span data-ttu-id="50aef-114">Wenn Sie z. b. im Hauptbild eine Schaltflächen Grafik mit der Schaltfläche "mit Vorzeichen" haben, können Sie eine Karte mit dem Bereich der roten Farbe erstellen.</span><span class="sxs-lookup"><span data-stu-id="50aef-114">For example, if you have a stop-sign-shaped button graphic in the main image, you can create a map with the area of the sign colored red.</span></span> <span data-ttu-id="50aef-115">Das **ButtonElement** -Attribut muss dann als rot angegeben werden, damit das Bild für das Abbrechen des signierten Zeichens geklickt werden kann.</span><span class="sxs-lookup"><span data-stu-id="50aef-115">The **BUTTONELEMENT** attribute must then be specified as red to make the stop-sign image clickable.</span></span>

<span data-ttu-id="50aef-116">Die unterstützten Bildformate sind BMP, JPG, PNG und GIF (keine animierten GIFs).</span><span class="sxs-lookup"><span data-stu-id="50aef-116">The supported image formats are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span> <span data-ttu-id="50aef-117">Da es sich bei den JPGs um Verlust Verluste handelt, werden Sie daher nicht für die Zuordnung von Bildern empfohlen.</span><span class="sxs-lookup"><span data-stu-id="50aef-117">Because JPGs are lossy and therefore subject to unexpected color change, they are not recommended for mapping images.</span></span>

## <a name="examples"></a><span data-ttu-id="50aef-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="50aef-118">Examples</span></span>

<span data-ttu-id="50aef-119">Die folgende Abbildung ist ein Beispiel für ein **mappingImage** und das sichtbare Bild, dem es entspricht.</span><span class="sxs-lookup"><span data-stu-id="50aef-119">The following illustration is an example of a **mappingImage** and the visible image it corresponds to.</span></span> <span data-ttu-id="50aef-120">Diese Images sind Teil der Skin im kleinen Ordner, der im SDK enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="50aef-120">These images are part of the skin in the Tiny folder included with the SDK.</span></span>

![Bild der Beispiel Zuordnung](images/absam01m.png)![Beispiel Hintergrundbild](images/absam01f.png)

<span data-ttu-id="50aef-123">Siehe *ButtonElement*. [mappingColor](buttonelement-mappingcolor.md) -Attribut für ein Codebeispiel zur Veranschaulichung der Verwendung dieses Attributs.</span><span class="sxs-lookup"><span data-stu-id="50aef-123">See the *BUTTONELEMENT*.[mappingColor](buttonelement-mappingcolor.md) attribute for a code sample illustrating the use of this attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="50aef-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50aef-124">Requirements</span></span>



| <span data-ttu-id="50aef-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50aef-125">Requirement</span></span> | <span data-ttu-id="50aef-126">Wert</span><span class="sxs-lookup"><span data-stu-id="50aef-126">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="50aef-127">Version</span><span class="sxs-lookup"><span data-stu-id="50aef-127">Version</span></span><br/> | <span data-ttu-id="50aef-128">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="50aef-128">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="50aef-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50aef-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50aef-130">**ButtonElement. mappingColor**</span><span class="sxs-lookup"><span data-stu-id="50aef-130">**BUTTONELEMENT.mappingColor**</span></span>](buttonelement-mappingcolor.md)
</dt> <dt>

[<span data-ttu-id="50aef-131">**ButtonGroup-Element**</span><span class="sxs-lookup"><span data-stu-id="50aef-131">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="50aef-132">**ButtonGroup. Image**</span><span class="sxs-lookup"><span data-stu-id="50aef-132">**BUTTONGROUP.image**</span></span>](buttongroup-image.md)
</dt> <dt>

[<span data-ttu-id="50aef-133">**ButtonGroup. TransparencyColor**</span><span class="sxs-lookup"><span data-stu-id="50aef-133">**BUTTONGROUP.transparencyColor**</span></span>](buttongroup-transparencycolor.md)
</dt> </dl>

 

 





