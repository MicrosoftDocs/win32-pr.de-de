---
title: ListBox. FontStyle
description: Das FontStyle-Attribut gibt den Schrift Schnitt für das Listenfeld-Steuerelement an oder ruft ihn ab.
ms.assetid: c42b80b6-0dea-4080-a06e-931fdc02fa55
keywords:
- ListBox. FontStyle-Fenster Media Player
topic_type:
- apiref
api_name:
- LISTBOX.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0903ac77f1fa4307dfcabad6311eb556617d8153
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364947"
---
# <a name="listboxfontstyle"></a><span data-ttu-id="7a079-104">ListBox. FontStyle</span><span class="sxs-lookup"><span data-stu-id="7a079-104">LISTBOX.fontStyle</span></span>

<span data-ttu-id="7a079-105">Das **FontStyle** -Attribut gibt den Schrift Schnitt für das Listenfeld-Steuerelement an oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="7a079-105">The **fontStyle** attribute specifies or retrieves the font style for the list box control.</span></span>

``` syntax
        elementID.fontStyle
```

## <a name="possible-values"></a><span data-ttu-id="7a079-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="7a079-106">Possible Values</span></span>

<span data-ttu-id="7a079-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die einen oder mehrere der folgenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="7a079-107">This attribute is a read/write **String** containing one or more of the following values.</span></span>



| <span data-ttu-id="7a079-108">Wert</span><span class="sxs-lookup"><span data-stu-id="7a079-108">Value</span></span>     | <span data-ttu-id="7a079-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7a079-109">Description</span></span>           |
|-----------|-----------------------|
| <span data-ttu-id="7a079-110">Fett</span><span class="sxs-lookup"><span data-stu-id="7a079-110">Bold</span></span>      | <span data-ttu-id="7a079-111">Fett Schriftstil.</span><span class="sxs-lookup"><span data-stu-id="7a079-111">Bold font style.</span></span>      |
| <span data-ttu-id="7a079-112">Kursiv</span><span class="sxs-lookup"><span data-stu-id="7a079-112">Italic</span></span>    | <span data-ttu-id="7a079-113">Kursiv Schriftstil.</span><span class="sxs-lookup"><span data-stu-id="7a079-113">Italic font style.</span></span>    |
| <span data-ttu-id="7a079-114">Underline</span><span class="sxs-lookup"><span data-stu-id="7a079-114">Underline</span></span> | <span data-ttu-id="7a079-115">Unterstreichung der Schriftart.</span><span class="sxs-lookup"><span data-stu-id="7a079-115">Underline font style.</span></span> |
| <span data-ttu-id="7a079-116">Durchgestrichen</span><span class="sxs-lookup"><span data-stu-id="7a079-116">Strikeout</span></span> | <span data-ttu-id="7a079-117">Stil der Strikeout-Schriftart.</span><span class="sxs-lookup"><span data-stu-id="7a079-117">Strikeout font style.</span></span> |
| <span data-ttu-id="7a079-118">Normal</span><span class="sxs-lookup"><span data-stu-id="7a079-118">Normal</span></span>    | <span data-ttu-id="7a079-119">Normaler Schriftart Stil.</span><span class="sxs-lookup"><span data-stu-id="7a079-119">Normal font style.</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="7a079-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a079-120">Remarks</span></span>

<span data-ttu-id="7a079-121">Eine beliebige Kombination der Werte kann mit Leerzeichen getrennt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7a079-121">Any combination of the values can be used, separated with spaces.</span></span> <span data-ttu-id="7a079-122">Der normale Stil hat Vorrang vor allen anderen Werten, und alle anderen Werte, die zusammen mit normal angegeben werden, werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="7a079-122">The Normal style has priority over all other values, and any others specified along with Normal will be ignored.</span></span>

<span data-ttu-id="7a079-123">Zu Renderingzwecken ist normal der Standard Schriftart Stil.</span><span class="sxs-lookup"><span data-stu-id="7a079-123">For rendering purposes, Normal is the default font style.</span></span> <span data-ttu-id="7a079-124">Der Standardwert, der von diesem Attribut abgerufen wird, ist "" (leere Zeichenfolge).</span><span class="sxs-lookup"><span data-stu-id="7a079-124">The default value retrieved from this attribute is "" (empty string).</span></span>

## <a name="requirements"></a><span data-ttu-id="7a079-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a079-125">Requirements</span></span>



| <span data-ttu-id="7a079-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a079-126">Requirement</span></span> | <span data-ttu-id="7a079-127">Wert</span><span class="sxs-lookup"><span data-stu-id="7a079-127">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="7a079-128">Version</span><span class="sxs-lookup"><span data-stu-id="7a079-128">Version</span></span><br/> | <span data-ttu-id="7a079-129">Windows Media Player für Windows XP oder höher</span><span class="sxs-lookup"><span data-stu-id="7a079-129">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7a079-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a079-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a079-131">**ListBox-Element**</span><span class="sxs-lookup"><span data-stu-id="7a079-131">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> <dt>

[<span data-ttu-id="7a079-132">**ListBox. FontSize**</span><span class="sxs-lookup"><span data-stu-id="7a079-132">**LISTBOX.fontSize**</span></span>](listbox-fontsize.md)
</dt> </dl>

 

 





