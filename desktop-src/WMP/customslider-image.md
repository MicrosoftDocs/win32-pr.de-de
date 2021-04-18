---
title: Customslider. Image
description: Das Image-Attribut gibt den Namen der Datei an oder Ruft den Namen der Datei ab, die den verschiedenen Zuständen des benutzerdefinierten Schiebereglers entspricht.
ms.assetid: 7db4f924-76af-4451-831c-1ed8ab1315ee
keywords:
- Windows-Media Player "customslider. Image"
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f425ce138b2a11d2be834f39603ecc295c52c706
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352005"
---
# <a name="customsliderimage"></a><span data-ttu-id="b6158-104">Customslider. Image</span><span class="sxs-lookup"><span data-stu-id="b6158-104">CUSTOMSLIDER.image</span></span>

<span data-ttu-id="b6158-105">Das **Image** -Attribut gibt den Namen der Datei an oder Ruft den Namen der Datei ab, die den verschiedenen Zuständen des benutzerdefinierten Schiebereglers entspricht.</span><span class="sxs-lookup"><span data-stu-id="b6158-105">The **image** attribute specifies or retrieves the name of the file containing the images corresponding to the various states of the custom slider.</span></span>

``` syntax
        elementID.image
```

## <a name="possible-values"></a><span data-ttu-id="b6158-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="b6158-106">Possible Values</span></span>

<span data-ttu-id="b6158-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die den Namen einer Bilddatei enthält.</span><span class="sxs-lookup"><span data-stu-id="b6158-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6158-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b6158-108">Remarks</span></span>

<span data-ttu-id="b6158-109">Das **Image** -Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b6158-109">The **image** attribute is required.</span></span> <span data-ttu-id="b6158-110">Es gibt eine Bilddatei an, die aus mindestens einem untergeordneten Bild besteht, das entweder horizontal oder vertikal angeordnet ist und die verschiedenen Zustände des benutzerdefinierten Schiebereglers darstellt.</span><span class="sxs-lookup"><span data-stu-id="b6158-110">It specifies an image file that consists of one or more sub-images, arranged either horizontally or vertically, representing the various states of the custom slider.</span></span> <span data-ttu-id="b6158-111">Jedes untergeordnete Image muss die gleichen Dimensionen wie das **positionImage** aufweisen, oder der benutzerdefinierte Schieberegler funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="b6158-111">Each sub-image must have the same dimensions as the **positionImage** or the custom slider will not work correctly.</span></span> <span data-ttu-id="b6158-112">Die Höhe oder Breite des gesamten Bilds muss daher ein gleich Vielfaches der Höhe oder Breite des **positionbilds** sein.</span><span class="sxs-lookup"><span data-stu-id="b6158-112">The height or width of the overall image must therefore be an even multiple of the height or width of the **positionImage**.</span></span>

<span data-ttu-id="b6158-113">Die unterstützten Bild Dateitypen sind BMP, JPG, PNG und GIF (keine animierten GIFs).</span><span class="sxs-lookup"><span data-stu-id="b6158-113">The supported image file types are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="examples"></a><span data-ttu-id="b6158-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b6158-114">Examples</span></span>

<span data-ttu-id="b6158-115">Im folgenden finden Sie ein Beispiel für ein benutzerdefiniertes Schieberegler-Image.</span><span class="sxs-lookup"><span data-stu-id="b6158-115">The following is an example of a custom slider image.</span></span> <span data-ttu-id="b6158-116">Das entsprechende **positionImage** wird im Beispiel Abschnitt der **positionImage** -Eigenschaft angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b6158-116">The corresponding **positionImage** is shown in the example section of the **positionImage** property.</span></span>

![Beispiel eines customslider-Bilds](images/dial.png)

<span data-ttu-id="b6158-118">Das **positionImage** -Attribut enthält auch ein Codebeispiel, das veranschaulicht, wie die Attribute des **customslider** -Elements verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b6158-118">The **positionImage** attribute also contains a code sample illustrating how the attributes of the **CUSTOMSLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6158-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6158-119">Requirements</span></span>



| <span data-ttu-id="b6158-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6158-120">Requirement</span></span> | <span data-ttu-id="b6158-121">Wert</span><span class="sxs-lookup"><span data-stu-id="b6158-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="b6158-122">Version</span><span class="sxs-lookup"><span data-stu-id="b6158-122">Version</span></span><br/> | <span data-ttu-id="b6158-123">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="b6158-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b6158-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6158-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6158-125">**Customslider-Element**</span><span class="sxs-lookup"><span data-stu-id="b6158-125">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> <dt>

[<span data-ttu-id="b6158-126">**Customslider. positionImage**</span><span class="sxs-lookup"><span data-stu-id="b6158-126">**CUSTOMSLIDER.positionImage**</span></span>](customslider-positionimage.md)
</dt> </dl>

 

 





