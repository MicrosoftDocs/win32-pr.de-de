---
title: EditBox. FontStyle
description: Das FontStyle-Attribut gibt den Schrift Schnitt für das Bearbeitungsfeld-Steuerelement an oder ruft ihn ab.
ms.assetid: bc71359d-2b75-4134-99e8-52b2ca48dcde
keywords:
- EditBox. FontStyle-Fenster Media Player
topic_type:
- apiref
api_name:
- EDITBOX.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4249f6224099c3d2a36a3b26244c9b804be519c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356328"
---
# <a name="editboxfontstyle"></a><span data-ttu-id="d49b3-104">EditBox. FontStyle</span><span class="sxs-lookup"><span data-stu-id="d49b3-104">EDITBOX.fontStyle</span></span>

<span data-ttu-id="d49b3-105">Das **FontStyle** -Attribut gibt den Schrift Schnitt für das Bearbeitungsfeld-Steuerelement an oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="d49b3-105">The **fontStyle** attribute specifies or retrieves the font style for the edit box control.</span></span>

``` syntax
        elementID.fontStyle
```

## <a name="possible-values"></a><span data-ttu-id="d49b3-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="d49b3-106">Possible Values</span></span>

<span data-ttu-id="d49b3-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die einen oder mehrere der folgenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="d49b3-107">This attribute is a read/write **String** containing one or more of the following values.</span></span>



| <span data-ttu-id="d49b3-108">Wert</span><span class="sxs-lookup"><span data-stu-id="d49b3-108">Value</span></span>     | <span data-ttu-id="d49b3-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d49b3-109">Description</span></span>           |
|-----------|-----------------------|
| <span data-ttu-id="d49b3-110">Fett</span><span class="sxs-lookup"><span data-stu-id="d49b3-110">Bold</span></span>      | <span data-ttu-id="d49b3-111">Fett Schriftstil.</span><span class="sxs-lookup"><span data-stu-id="d49b3-111">Bold font style.</span></span>      |
| <span data-ttu-id="d49b3-112">Kursiv</span><span class="sxs-lookup"><span data-stu-id="d49b3-112">Italic</span></span>    | <span data-ttu-id="d49b3-113">Kursiv Schriftstil.</span><span class="sxs-lookup"><span data-stu-id="d49b3-113">Italic font style.</span></span>    |
| <span data-ttu-id="d49b3-114">Underline</span><span class="sxs-lookup"><span data-stu-id="d49b3-114">Underline</span></span> | <span data-ttu-id="d49b3-115">Unterstreichung der Schriftart.</span><span class="sxs-lookup"><span data-stu-id="d49b3-115">Underline font style.</span></span> |
| <span data-ttu-id="d49b3-116">Durchgestrichen</span><span class="sxs-lookup"><span data-stu-id="d49b3-116">Strikeout</span></span> | <span data-ttu-id="d49b3-117">Stil der Strikeout-Schriftart.</span><span class="sxs-lookup"><span data-stu-id="d49b3-117">Strikeout font style.</span></span> |
| <span data-ttu-id="d49b3-118">Normal</span><span class="sxs-lookup"><span data-stu-id="d49b3-118">Normal</span></span>    | <span data-ttu-id="d49b3-119">Normaler Schriftart Stil.</span><span class="sxs-lookup"><span data-stu-id="d49b3-119">Normal font style.</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="d49b3-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d49b3-120">Remarks</span></span>

<span data-ttu-id="d49b3-121">Eine beliebige Kombination der Werte kann mit Leerzeichen getrennt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d49b3-121">Any combination of the values can be used, separated with spaces.</span></span> <span data-ttu-id="d49b3-122">Der normale Stil hat Vorrang vor allen anderen Werten, und alle anderen Werte, die zusammen mit normal angegeben werden, werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d49b3-122">The Normal style has priority over all other values, and any others specified along with Normal will be ignored.</span></span>

<span data-ttu-id="d49b3-123">Zu Renderingzwecken ist normal der Standard Schriftart Stil.</span><span class="sxs-lookup"><span data-stu-id="d49b3-123">For rendering purposes, Normal is the default font style.</span></span> <span data-ttu-id="d49b3-124">Der Standardwert, der von diesem Attribut abgerufen wird, ist "" (leere Zeichenfolge).</span><span class="sxs-lookup"><span data-stu-id="d49b3-124">The default value retrieved from this attribute is "" (empty string).</span></span>

## <a name="requirements"></a><span data-ttu-id="d49b3-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d49b3-125">Requirements</span></span>



| <span data-ttu-id="d49b3-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d49b3-126">Requirement</span></span> | <span data-ttu-id="d49b3-127">Wert</span><span class="sxs-lookup"><span data-stu-id="d49b3-127">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="d49b3-128">Version</span><span class="sxs-lookup"><span data-stu-id="d49b3-128">Version</span></span><br/> | <span data-ttu-id="d49b3-129">Windows Media Player für Windows XP oder höher</span><span class="sxs-lookup"><span data-stu-id="d49b3-129">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d49b3-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d49b3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d49b3-131">**EditBox-Element**</span><span class="sxs-lookup"><span data-stu-id="d49b3-131">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="d49b3-132">**EditBox. fontface**</span><span class="sxs-lookup"><span data-stu-id="d49b3-132">**EDITBOX.fontFace**</span></span>](editbox-fontface.md)
</dt> <dt>

[<span data-ttu-id="d49b3-133">**EditBox. FontSize**</span><span class="sxs-lookup"><span data-stu-id="d49b3-133">**EDITBOX.fontSize**</span></span>](editbox-fontsize.md)
</dt> </dl>

 

 





