---
title: Text. ForegroundColor
description: Das ForegroundColor-Attribut gibt die Textfarbe für das Text Steuerelement an oder ruft diese ab.
ms.assetid: 1ddbad93-fbff-4be6-9797-6594b5f09a1e
keywords:
- Text. ForegroundColor-Fenster Media Player
topic_type:
- apiref
api_name:
- TEXT.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e452a18a085337e8cbf0ec88567d6a57a0a498a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356371"
---
# <a name="textforegroundcolor"></a><span data-ttu-id="d1076-104">Text. ForegroundColor</span><span class="sxs-lookup"><span data-stu-id="d1076-104">TEXT.foregroundColor</span></span>

<span data-ttu-id="d1076-105">Das **ForegroundColor** -Attribut gibt die Textfarbe für das Text Steuerelement an oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="d1076-105">The **foregroundColor** attribute specifies or retrieves the text color for the Text control.</span></span>

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a><span data-ttu-id="d1076-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="d1076-106">Possible Values</span></span>

<span data-ttu-id="d1076-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge** mit einem beliebigen Microsoft Internet Explorer-Farbwert.</span><span class="sxs-lookup"><span data-stu-id="d1076-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value.</span></span> <span data-ttu-id="d1076-108">Der Standardwert ist "schwarz".</span><span class="sxs-lookup"><span data-stu-id="d1076-108">The default value is "black".</span></span>

<span data-ttu-id="d1076-109">Im [value](text-value.md) -Attribut finden Sie ein Beispiel, das veranschaulicht, wie die Attribute des **Text** -Elements verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d1076-109">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

<span data-ttu-id="d1076-110">Wenn Sie **AlphaBlend** oder **alphablendto** mit einem **Text** Element verwenden, für das keine **BackgroundColor** angegeben ist, wird eine Hintergrundfarbe von Schwarz verwendet.</span><span class="sxs-lookup"><span data-stu-id="d1076-110">When you use **alphaBlend** or **alphaBlendTo** with a **TEXT** element that does not have the **backgroundColor** specified, a background color of black will be used.</span></span> <span data-ttu-id="d1076-111">Wenn die Vordergrundfarbe ebenfalls schwarz ist (Dies ist der Standardwert für das **ForegroundColor** -Attribut), wird der Text möglicherweise nicht lesbar.</span><span class="sxs-lookup"><span data-stu-id="d1076-111">If the foreground color is also black (which is the default value for the **foregroundColor** attribute), your text may become unreadable.</span></span> <span data-ttu-id="d1076-112">Um dies zu verhindern, geben Sie immer das **BackgroundColor** -Attribut an, oder legen Sie **ForegroundColor** auf eine andere Farbe als schwarz fest.</span><span class="sxs-lookup"><span data-stu-id="d1076-112">To prevent this, always specify the **backgroundColor** attribute, or set **foregroundColor** to a color other than black.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1076-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1076-113">Requirements</span></span>



| <span data-ttu-id="d1076-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1076-114">Requirement</span></span> | <span data-ttu-id="d1076-115">Wert</span><span class="sxs-lookup"><span data-stu-id="d1076-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="d1076-116">Version</span><span class="sxs-lookup"><span data-stu-id="d1076-116">Version</span></span><br/> | <span data-ttu-id="d1076-117">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="d1076-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d1076-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1076-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1076-119">**Ambientattribute. AlphaBlend**</span><span class="sxs-lookup"><span data-stu-id="d1076-119">**AmbientAttributes.alphaBlend**</span></span>](ambientattributes-alphablend.md)
</dt> <dt>

[<span data-ttu-id="d1076-120">**Ambientattribute. alphablendto**</span><span class="sxs-lookup"><span data-stu-id="d1076-120">**AmbientAttributes.alphaBlendTo**</span></span>](ambientattributes-alphablendto.md)
</dt> <dt>

[<span data-ttu-id="d1076-121">**Farb Verweis**</span><span class="sxs-lookup"><span data-stu-id="d1076-121">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="d1076-122">**Text-Element**</span><span class="sxs-lookup"><span data-stu-id="d1076-122">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="d1076-123">**Text. BackgroundColor**</span><span class="sxs-lookup"><span data-stu-id="d1076-123">**TEXT.backgroundColor**</span></span>](text-backgroundcolor.md)
</dt> </dl>

 

 





