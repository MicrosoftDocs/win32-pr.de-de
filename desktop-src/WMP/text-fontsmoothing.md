---
title: Text. fontermoothing
description: Mit dem Attribut "FontSmoothing" wird ein Wert angegeben oder abgerufen, der angibt, ob die Schriftart Glättung aktiviert ist.
ms.assetid: bd6f0468-285e-44b3-a5e8-361744c5ce4a
keywords:
- Text. FON-moothing-Fenster Media Player
topic_type:
- apiref
api_name:
- TEXT.fontSmoothing
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcdf285572b4edda0f514cb3519b6953f9e94677
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373623"
---
# <a name="textfontsmoothing"></a><span data-ttu-id="c03ae-104">Text. fontermoothing</span><span class="sxs-lookup"><span data-stu-id="c03ae-104">TEXT.fontSmoothing</span></span>

<span data-ttu-id="c03ae-105">Mit dem Attribut " **FontSmoothing** " wird ein Wert angegeben oder abgerufen, der angibt, ob die Schriftart Glättung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c03ae-105">The **fontSmoothing** attribute specifies or retrieves a value indicating whether font smoothing is enabled.</span></span>

``` syntax
        elementID.fontSmoothing
```

## <a name="possible-values"></a><span data-ttu-id="c03ae-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="c03ae-106">Possible Values</span></span>

<span data-ttu-id="c03ae-107">Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="c03ae-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="c03ae-108">Wert</span><span class="sxs-lookup"><span data-stu-id="c03ae-108">Value</span></span> | <span data-ttu-id="c03ae-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c03ae-109">Description</span></span>                          |
|-------|--------------------------------------|
| <span data-ttu-id="c03ae-110">true</span><span class="sxs-lookup"><span data-stu-id="c03ae-110">true</span></span>  | <span data-ttu-id="c03ae-111">Die Schriftart Glättung ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c03ae-111">Font smoothing is enabled.</span></span>           |
| <span data-ttu-id="c03ae-112">false</span><span class="sxs-lookup"><span data-stu-id="c03ae-112">false</span></span> | <span data-ttu-id="c03ae-113">Standard.</span><span class="sxs-lookup"><span data-stu-id="c03ae-113">Default.</span></span> <span data-ttu-id="c03ae-114">Die Schriftart Glättung ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c03ae-114">Font smoothing is disabled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c03ae-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c03ae-115">Remarks</span></span>

<span data-ttu-id="c03ae-116">Die Schriftart Glättung verwendet das Antialiasing-Feature des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="c03ae-116">Font smoothing uses the anti-aliasing feature of the operating system.</span></span> <span data-ttu-id="c03ae-117">Wenn die Schriftart Glättung aktiviert ist und das Betriebssystem Antialiasing unterstützt, versucht Windows Media Player, den Text zu glätten.</span><span class="sxs-lookup"><span data-stu-id="c03ae-117">If font smoothing is enabled and the operating system supports anti-aliasing, Windows Media Player attempts to smooth the text.</span></span> <span data-ttu-id="c03ae-118">Nicht alle Schriftarten unterstützen Antialiasing.</span><span class="sxs-lookup"><span data-stu-id="c03ae-118">Not all fonts support anti-aliasing.</span></span> <span data-ttu-id="c03ae-119">Windows Media Player 10 verwendet die Windows XP ClearType Anti-Aliasing-Methode.</span><span class="sxs-lookup"><span data-stu-id="c03ae-119">Windows Media Player 10 uses the Windows XP ClearType anti-aliasing method.</span></span>

-   <span data-ttu-id="c03ae-120">**Warnung** Die Schriftart Glättung über eine transparente Farbe kann bewirken, dass die transparente Farbe in die Zeichen hinein mischt.</span><span class="sxs-lookup"><span data-stu-id="c03ae-120">**Warning** Font smoothing over a transparent color may cause the transparent color to blend into the characters.</span></span> <span data-ttu-id="c03ae-121">Es wird nicht empfohlen, dass Sie " **fonensmoothing** " verwenden, wenn der Text über eine Transparenz angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c03ae-121">It is not recommended that you use **fontSmoothing** if the text will display over a transparency.</span></span>

<span data-ttu-id="c03ae-122">Im [value](text-value.md) -Attribut finden Sie ein Beispiel, das veranschaulicht, wie die Attribute des **Text** -Elements verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c03ae-122">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="c03ae-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c03ae-123">Requirements</span></span>



| <span data-ttu-id="c03ae-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c03ae-124">Requirement</span></span> | <span data-ttu-id="c03ae-125">Wert</span><span class="sxs-lookup"><span data-stu-id="c03ae-125">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c03ae-126">Version</span><span class="sxs-lookup"><span data-stu-id="c03ae-126">Version</span></span><br/> | <span data-ttu-id="c03ae-127">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="c03ae-127">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c03ae-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c03ae-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c03ae-129">**Text-Element**</span><span class="sxs-lookup"><span data-stu-id="c03ae-129">**TEXT Element**</span></span>](text-element.md)
</dt> </dl>

 

 





