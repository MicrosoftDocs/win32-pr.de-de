---
title: Ambientattribute. clippingimage
description: Das clippingimage-Attribut gibt den Bereich an, an den das Steuerelement abgeschnitten wird, oder ruft ihn ab.
ms.assetid: e4b51d31-f9c7-4398-983d-95867a2cab45
keywords:
- Ambientattribute. clippingimage-Fenster Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.clippingImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e05e05ca9c7c3efdf842ffd4297da6f9fee035d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365585"
---
# <a name="ambientattributesclippingimage"></a><span data-ttu-id="f8fbd-104">Ambientattribute. clippingimage</span><span class="sxs-lookup"><span data-stu-id="f8fbd-104">AmbientAttributes.clippingImage</span></span>

<span data-ttu-id="f8fbd-105">Das **clippingimage** -Attribut gibt den Bereich an, an den das Steuerelement abgeschnitten wird, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="f8fbd-105">The **clippingImage** attribute specifies or retrieves the region to clip the control to.</span></span>

``` syntax
        elementID.clippingImage
```

## <a name="possible-values"></a><span data-ttu-id="f8fbd-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="f8fbd-106">Possible Values</span></span>

<span data-ttu-id="f8fbd-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die den Namen der Bilddatei angibt</span><span class="sxs-lookup"><span data-stu-id="f8fbd-107">This attribute is a read/write **String** indicating the image file name.</span></span> <span data-ttu-id="f8fbd-108">Er besitzt keinen Standardwert.</span><span class="sxs-lookup"><span data-stu-id="f8fbd-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8fbd-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8fbd-109">Remarks</span></span>

<span data-ttu-id="f8fbd-110">Das **clippingimage** -Attribut unterstützt PNG-, JPG-, BMP-und GIF-Dateien (ohne animierte GIFs).</span><span class="sxs-lookup"><span data-stu-id="f8fbd-110">The **clippingImage** attribute supports PNG, JPG, BMP, and GIF files (not including animated GIFs).</span></span> <span data-ttu-id="f8fbd-111">Da es sich bei den JPGs um Verlust Verluste handelt, werden Sie daher nicht für das Abschneiden von Images empfohlen.</span><span class="sxs-lookup"><span data-stu-id="f8fbd-111">Because JPGs are lossy and therefore subject to unexpected color change, they are not recommended for clipping images.</span></span>

<span data-ttu-id="f8fbd-112">Dieses Attribut ist nützlich, wenn Sie nur einen Teil des Steuerelement Bilds anzeigen möchten, nicht den gesamten rechteckigen Bereich.</span><span class="sxs-lookup"><span data-stu-id="f8fbd-112">This attribute is useful when you want to display only a part of the control image and not the entire rectangular area.</span></span> <span data-ttu-id="f8fbd-113">Das **clippingcolor** -Attribut gibt die Bereiche des clippingbilds an, die transparenten, nicht klickbaren Teilen des Steuer Elements entsprechen.</span><span class="sxs-lookup"><span data-stu-id="f8fbd-113">The **clippingColor** attribute indicates the regions of the clipping image that correspond to transparent, non-clickable portions of the control.</span></span> <span data-ttu-id="f8fbd-114">Das Steuerelement kann daher eine beliebige Form aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f8fbd-114">The control can therefore be of any shape.</span></span> <span data-ttu-id="f8fbd-115">Um optimale Ergebnisse zu erzielen, sollte das clippingbild die gleiche Größe wie das Steuerelement Bild aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f8fbd-115">For best results, the clipping image should be the same size as the control image.</span></span>

<span data-ttu-id="f8fbd-116">Das **clippingimage** -Attribut wird von den Elementen " **Wiedergabeliste**", " **View**" und " **subview** " nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f8fbd-116">The **clippingImage** attribute is not supported by the **PLAYLIST**, **VIEW**, and **SUBVIEW** elements.</span></span> <span data-ttu-id="f8fbd-117">Ein clippingbild funktioniert nicht mit dem **Video** Element, wenn es sich um ein *Video* handelt. **Windows less** ist auf false festgelegt, ebenso wie das **Effects** -Element bei *Effekten*. " **Fenster** " ist auf "true" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f8fbd-117">A clipping image will not work with the **VIDEO** element if *VIDEO*.**windowless** is set to false, nor with the **EFFECTS** element if *EFFECTS*.**windowed** is set to true.</span></span>

<span data-ttu-id="f8fbd-118">Da die Verwendung von Clipping-Images zu Leistungseinbußen führt, sollten Sie nicht verwendet werden, wenn die Effizienz ein Problem ist.</span><span class="sxs-lookup"><span data-stu-id="f8fbd-118">Because the use of clipping images imposes a performance penalty, they should not be used when efficiency is an issue.</span></span>

## <a name="examples"></a><span data-ttu-id="f8fbd-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f8fbd-119">Examples</span></span>

<span data-ttu-id="f8fbd-120">Ein Beispiel zur Veranschaulichung der Verwendung dieses Attributs finden Sie unter [ButtonElement. mappingColor](buttonelement-mappingcolor.md) -Attribut.</span><span class="sxs-lookup"><span data-stu-id="f8fbd-120">See the [BUTTONELEMENT.mappingColor](buttonelement-mappingcolor.md) attribute for a sample illustrating the use of this attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8fbd-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8fbd-121">Requirements</span></span>



| <span data-ttu-id="f8fbd-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f8fbd-122">Requirement</span></span> | <span data-ttu-id="f8fbd-123">Wert</span><span class="sxs-lookup"><span data-stu-id="f8fbd-123">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="f8fbd-124">Version</span><span class="sxs-lookup"><span data-stu-id="f8fbd-124">Version</span></span><br/> | <span data-ttu-id="f8fbd-125">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="f8fbd-125">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f8fbd-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8fbd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8fbd-127">**Ambient-Attribute**</span><span class="sxs-lookup"><span data-stu-id="f8fbd-127">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="f8fbd-128">**Ambientattribute. clippingcolor**</span><span class="sxs-lookup"><span data-stu-id="f8fbd-128">**AmbientAttributes.clippingColor**</span></span>](ambientattributes-clippingcolor.md)
</dt> </dl>

 

 





