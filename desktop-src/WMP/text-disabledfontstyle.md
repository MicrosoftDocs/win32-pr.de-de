---
title: Text. disabledfontstyle
description: Das disabledfontstyle-Attribut gibt den Schriftart Stil an, der für das Text Steuerelement verwendet wird, wenn er deaktiviert ist, oder ruft ihn ab.
ms.assetid: d0593fe0-f80d-44a3-b989-e85887465d8a
keywords:
- Text. disabledfontstyle-Fenster Media Player
topic_type:
- apiref
api_name:
- TEXT.disabledFontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 563ab039a5eae00324f3a810c7d32f08729629b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372576"
---
# <a name="textdisabledfontstyle"></a><span data-ttu-id="631bf-104">Text. disabledfontstyle</span><span class="sxs-lookup"><span data-stu-id="631bf-104">TEXT.disabledFontStyle</span></span>

<span data-ttu-id="631bf-105">Das **disabledfontstyle** -Attribut gibt den Schriftart Stil an, der für das Text Steuerelement verwendet wird, wenn er deaktiviert ist, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="631bf-105">The **disabledFontStyle** attribute specifies or retrieves the font style used for the Text control when it is disabled.</span></span>

``` syntax
        elementID.disabledFontStyle
```

## <a name="possible-values"></a><span data-ttu-id="631bf-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="631bf-106">Possible Values</span></span>

<span data-ttu-id="631bf-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die einen oder mehrere der folgenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="631bf-107">This attribute is a read/write **String** containing one or more of the following values.</span></span>



| <span data-ttu-id="631bf-108">Wert</span><span class="sxs-lookup"><span data-stu-id="631bf-108">Value</span></span>     | <span data-ttu-id="631bf-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="631bf-109">Description</span></span>           |
|-----------|-----------------------|
| <span data-ttu-id="631bf-110">Fett</span><span class="sxs-lookup"><span data-stu-id="631bf-110">Bold</span></span>      | <span data-ttu-id="631bf-111">Fett Schriftstil.</span><span class="sxs-lookup"><span data-stu-id="631bf-111">Bold font style.</span></span>      |
| <span data-ttu-id="631bf-112">Kursiv</span><span class="sxs-lookup"><span data-stu-id="631bf-112">Italic</span></span>    | <span data-ttu-id="631bf-113">Kursiv Schriftstil.</span><span class="sxs-lookup"><span data-stu-id="631bf-113">Italic font style.</span></span>    |
| <span data-ttu-id="631bf-114">Underline</span><span class="sxs-lookup"><span data-stu-id="631bf-114">Underline</span></span> | <span data-ttu-id="631bf-115">Unterstreichung der Schriftart.</span><span class="sxs-lookup"><span data-stu-id="631bf-115">Underline font style.</span></span> |
| <span data-ttu-id="631bf-116">Durchgestrichen</span><span class="sxs-lookup"><span data-stu-id="631bf-116">Strikeout</span></span> | <span data-ttu-id="631bf-117">Stil der Strikeout-Schriftart.</span><span class="sxs-lookup"><span data-stu-id="631bf-117">Strikeout font style.</span></span> |
| <span data-ttu-id="631bf-118">Normal</span><span class="sxs-lookup"><span data-stu-id="631bf-118">Normal</span></span>    | <span data-ttu-id="631bf-119">Normaler Schriftart Stil.</span><span class="sxs-lookup"><span data-stu-id="631bf-119">Normal font style.</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="631bf-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="631bf-120">Remarks</span></span>

<span data-ttu-id="631bf-121">Eine beliebige Kombination der Werte kann mit Leerzeichen getrennt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="631bf-121">Any combination of the values can be used, separated with spaces.</span></span> <span data-ttu-id="631bf-122">Der normale Stil hat Vorrang vor allen anderen Werten, und alle anderen Werte, die zusammen mit normal angegeben werden, werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="631bf-122">The Normal style has priority over all other values, and any others specified along with Normal will be ignored.</span></span>

<span data-ttu-id="631bf-123">Wenn **disabledfontstyle** nicht angegeben wird, wird **FontStyle** verwendet.</span><span class="sxs-lookup"><span data-stu-id="631bf-123">If **disabledFontStyle** is not specified, **fontStyle** is used.</span></span>

<span data-ttu-id="631bf-124">Im [value](text-value.md) -Attribut finden Sie ein Beispiel, das veranschaulicht, wie die Attribute des **Text** -Elements verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="631bf-124">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="631bf-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="631bf-125">Requirements</span></span>



| <span data-ttu-id="631bf-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="631bf-126">Requirement</span></span> | <span data-ttu-id="631bf-127">Wert</span><span class="sxs-lookup"><span data-stu-id="631bf-127">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="631bf-128">Version</span><span class="sxs-lookup"><span data-stu-id="631bf-128">Version</span></span><br/> | <span data-ttu-id="631bf-129">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="631bf-129">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="631bf-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="631bf-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="631bf-131">**Text-Element**</span><span class="sxs-lookup"><span data-stu-id="631bf-131">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="631bf-132">**Text. FontStyle**</span><span class="sxs-lookup"><span data-stu-id="631bf-132">**TEXT.fontStyle**</span></span>](text-fontstyle.md)
</dt> </dl>

 

 





