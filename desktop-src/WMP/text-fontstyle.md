---
title: Text. FontStyle
description: Das FontStyle-Attribut gibt den Schrift Schnitt für das Text Steuerelement an oder ruft ihn ab.
ms.assetid: 1bb99305-dccc-489d-9a02-7cb306f0d47d
keywords:
- Text. FontStyle-Fenster Media Player
topic_type:
- apiref
api_name:
- TEXT.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab6ddfb3ff31cba50027c010ed10c2129d45134
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369959"
---
# <a name="textfontstyle"></a><span data-ttu-id="36b0c-104">Text. FontStyle</span><span class="sxs-lookup"><span data-stu-id="36b0c-104">TEXT.fontStyle</span></span>

<span data-ttu-id="36b0c-105">Das **FontStyle** -Attribut gibt den Schrift Schnitt für das Text Steuerelement an oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="36b0c-105">The **fontStyle** attribute specifies or retrieves the font style for the Text control.</span></span>

``` syntax
        elementID.fontStyle
```

## <a name="possible-values"></a><span data-ttu-id="36b0c-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="36b0c-106">Possible Values</span></span>

<span data-ttu-id="36b0c-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die einen oder mehrere der folgenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="36b0c-107">This attribute is a read/write **String** containing one or more of the following values.</span></span>



| <span data-ttu-id="36b0c-108">Wert</span><span class="sxs-lookup"><span data-stu-id="36b0c-108">Value</span></span>     | <span data-ttu-id="36b0c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36b0c-109">Description</span></span>                 |
|-----------|-----------------------------|
| <span data-ttu-id="36b0c-110">Fett</span><span class="sxs-lookup"><span data-stu-id="36b0c-110">Bold</span></span>      | <span data-ttu-id="36b0c-111">Fett Schriftstil.</span><span class="sxs-lookup"><span data-stu-id="36b0c-111">Bold font style.</span></span>            |
| <span data-ttu-id="36b0c-112">Kursiv</span><span class="sxs-lookup"><span data-stu-id="36b0c-112">Italic</span></span>    | <span data-ttu-id="36b0c-113">Kursiv Schriftstil.</span><span class="sxs-lookup"><span data-stu-id="36b0c-113">Italic font style.</span></span>          |
| <span data-ttu-id="36b0c-114">Underline</span><span class="sxs-lookup"><span data-stu-id="36b0c-114">Underline</span></span> | <span data-ttu-id="36b0c-115">Unterstreichung der Schriftart.</span><span class="sxs-lookup"><span data-stu-id="36b0c-115">Underline font style.</span></span>       |
| <span data-ttu-id="36b0c-116">Durchgestrichen</span><span class="sxs-lookup"><span data-stu-id="36b0c-116">Strikeout</span></span> | <span data-ttu-id="36b0c-117">Stil der Strikeout-Schriftart.</span><span class="sxs-lookup"><span data-stu-id="36b0c-117">Strikeout font style.</span></span>       |
| <span data-ttu-id="36b0c-118">Normal</span><span class="sxs-lookup"><span data-stu-id="36b0c-118">Normal</span></span>    | <span data-ttu-id="36b0c-119">Standard.</span><span class="sxs-lookup"><span data-stu-id="36b0c-119">Default.</span></span> <span data-ttu-id="36b0c-120">Normaler Schriftart Stil.</span><span class="sxs-lookup"><span data-stu-id="36b0c-120">Normal font style.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="36b0c-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="36b0c-121">Remarks</span></span>

<span data-ttu-id="36b0c-122">Eine beliebige Kombination der Werte kann mit Leerzeichen getrennt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="36b0c-122">Any combination of the values can be used, separated with spaces.</span></span> <span data-ttu-id="36b0c-123">Der normale Stil hat Vorrang vor allen anderen Werten, und alle anderen Werte, die zusammen mit normal angegeben werden, werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="36b0c-123">The Normal style has priority over all other values, and any others specified along with Normal will be ignored.</span></span>

<span data-ttu-id="36b0c-124">Im [value](text-value.md) -Attribut finden Sie ein Beispiel, das veranschaulicht, wie die Attribute des **Text** -Elements verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="36b0c-124">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="36b0c-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="36b0c-125">Requirements</span></span>



| <span data-ttu-id="36b0c-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="36b0c-126">Requirement</span></span> | <span data-ttu-id="36b0c-127">Wert</span><span class="sxs-lookup"><span data-stu-id="36b0c-127">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="36b0c-128">Version</span><span class="sxs-lookup"><span data-stu-id="36b0c-128">Version</span></span><br/> | <span data-ttu-id="36b0c-129">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="36b0c-129">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="36b0c-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36b0c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36b0c-131">**Text-Element**</span><span class="sxs-lookup"><span data-stu-id="36b0c-131">**TEXT Element**</span></span>](text-element.md)
</dt> </dl>

 

 





