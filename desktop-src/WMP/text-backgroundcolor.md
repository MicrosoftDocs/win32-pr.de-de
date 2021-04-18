---
title: Text. BackgroundColor
description: Das BackgroundColor-Attribut gibt die Hintergrundfarbe für das Text Steuerelement an oder ruft diese ab.
ms.assetid: 0c16318f-bf57-4c5f-85c1-46641124d431
keywords:
- Text. BackgroundColor-Fenster Media Player
topic_type:
- apiref
api_name:
- TEXT.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff833fad0b5ad60b49479c57dc51cbe82f48dbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358274"
---
# <a name="textbackgroundcolor"></a><span data-ttu-id="381e8-104">Text. BackgroundColor</span><span class="sxs-lookup"><span data-stu-id="381e8-104">TEXT.backgroundColor</span></span>

<span data-ttu-id="381e8-105">Das **BackgroundColor** -Attribut gibt die Hintergrundfarbe für das Text Steuerelement an oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="381e8-105">The **backgroundColor** attribute specifies or retrieves the background color for the Text control.</span></span>

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a><span data-ttu-id="381e8-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="381e8-106">Possible Values</span></span>

<span data-ttu-id="381e8-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die einen beliebigen Microsoft Internet Explorer-Farbwert oder den Wert "None" enthält.</span><span class="sxs-lookup"><span data-stu-id="381e8-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value or the value "none".</span></span> <span data-ttu-id="381e8-108">Der Standardwert ist "None". Dies bedeutet, dass der Hintergrund transparent ist.</span><span class="sxs-lookup"><span data-stu-id="381e8-108">It has a default value of "none", which means the background is transparent.</span></span>

## <a name="remarks"></a><span data-ttu-id="381e8-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="381e8-109">Remarks</span></span>

<span data-ttu-id="381e8-110">Die Hintergrundfarbe wird für die Höhe und Breite des Steuer Elements festgelegt.</span><span class="sxs-lookup"><span data-stu-id="381e8-110">The background color is set for the height and width of the control.</span></span> <span data-ttu-id="381e8-111">Wenn Height und Width nicht festgelegt sind, wird die Hintergrundfarbe auf die Höhe und Breite des Texts festgelegt.</span><span class="sxs-lookup"><span data-stu-id="381e8-111">If height and width are not set, the background color is set to the height and width of the text.</span></span>

<span data-ttu-id="381e8-112">Wenn Sie **AlphaBlend** oder **alphablendto** mit einem **Text** Element verwenden, für das keine **BackgroundColor** angegeben ist, wird eine Hintergrundfarbe von Schwarz verwendet.</span><span class="sxs-lookup"><span data-stu-id="381e8-112">When you use **alphaBlend** or **alphaBlendTo** with a **TEXT** element that does not have the **backgroundColor** specified, a background color of black will be used.</span></span> <span data-ttu-id="381e8-113">Wenn die Vordergrundfarbe ebenfalls schwarz ist (Dies ist der Standardwert für das **ForegroundColor** -Attribut), wird der Text möglicherweise nicht lesbar.</span><span class="sxs-lookup"><span data-stu-id="381e8-113">If the foreground color is also black (which is the default value for the **foregroundColor** attribute), your text may become unreadable.</span></span> <span data-ttu-id="381e8-114">Um dies zu verhindern, geben Sie immer das **BackgroundColor** -Attribut an, oder legen Sie **ForegroundColor** auf eine andere Farbe als schwarz fest.</span><span class="sxs-lookup"><span data-stu-id="381e8-114">To prevent this, always specify the **backgroundColor** attribute, or set **foregroundColor** to a color other than black.</span></span>

<span data-ttu-id="381e8-115">Im [value](text-value.md) -Attribut finden Sie ein Beispiel, das veranschaulicht, wie die Attribute des **Text** -Elements verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="381e8-115">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="381e8-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="381e8-116">Requirements</span></span>



| <span data-ttu-id="381e8-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="381e8-117">Requirement</span></span> | <span data-ttu-id="381e8-118">Wert</span><span class="sxs-lookup"><span data-stu-id="381e8-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="381e8-119">Version</span><span class="sxs-lookup"><span data-stu-id="381e8-119">Version</span></span><br/> | <span data-ttu-id="381e8-120">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="381e8-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="381e8-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="381e8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="381e8-122">**Ambientattribute. AlphaBlend**</span><span class="sxs-lookup"><span data-stu-id="381e8-122">**AmbientAttributes.alphaBlend**</span></span>](ambientattributes-alphablend.md)
</dt> <dt>

[<span data-ttu-id="381e8-123">**Ambientattribute. alphablendto**</span><span class="sxs-lookup"><span data-stu-id="381e8-123">**AmbientAttributes.alphaBlendTo**</span></span>](ambientattributes-alphablendto.md)
</dt> <dt>

[<span data-ttu-id="381e8-124">**Farb Verweis**</span><span class="sxs-lookup"><span data-stu-id="381e8-124">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="381e8-125">**Text-Element**</span><span class="sxs-lookup"><span data-stu-id="381e8-125">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="381e8-126">**Text. ForegroundColor**</span><span class="sxs-lookup"><span data-stu-id="381e8-126">**TEXT.foregroundColor**</span></span>](text-foregroundcolor.md)
</dt> </dl>

 

 





