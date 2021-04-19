---
title: Text. ToolTip
description: Das ToolTip-Attribut gibt den QuickInfo-Text für das Text Steuerelement an oder ruft ihn ab.
ms.assetid: 3e275607-e7ff-4424-8310-c628ede22629
keywords:
- Text. QuickInfo-Fenster Media Player
topic_type:
- apiref
api_name:
- TEXT.toolTip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b064f2abefd07ec65a82069196b1012561699b62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372357"
---
# <a name="texttooltip"></a><span data-ttu-id="f1cb1-104">Text. ToolTip</span><span class="sxs-lookup"><span data-stu-id="f1cb1-104">TEXT.toolTip</span></span>

<span data-ttu-id="f1cb1-105">Das **ToolTip** -Attribut gibt den QuickInfo-Text für das Text Steuerelement an oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="f1cb1-105">The **toolTip** attribute specifies or retrieves the ToolTip text for the text control.</span></span>

``` syntax
        elementID.toolTip
```

## <a name="possible-values"></a><span data-ttu-id="f1cb1-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="f1cb1-106">Possible Values</span></span>

<span data-ttu-id="f1cb1-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge** mit einer maximalen Länge von 1024 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="f1cb1-107">This attribute is a read/write **String** with a maximum length of 1024 characters.</span></span> <span data-ttu-id="f1cb1-108">Er besitzt keinen Standardwert.</span><span class="sxs-lookup"><span data-stu-id="f1cb1-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1cb1-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f1cb1-109">Remarks</span></span>

<span data-ttu-id="f1cb1-110">Wenn dieses Attribut nicht angegeben wird und der Text im **value** -Attribut im Text Steuerelement abgeschnitten wird, oder wenn **WordWrap** auf true festgelegt ist, wird in der QuickInfo der vollständige Text des **value** -Attributs angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f1cb1-110">If this attribute is not specified, and the text in the **value** attribute is truncated in the Text control, or **wordWrap** is set to true, the ToolTip will display the full text of the **value** attribute.</span></span>

<span data-ttu-id="f1cb1-111">Wenn dieses Attribut auf "" (leere Zeichenfolge) festgelegt ist, wird keine QuickInfo angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f1cb1-111">When this attribute is set to "" (empty string), no ToolTip is displayed.</span></span>

<span data-ttu-id="f1cb1-112">Im [value](text-value.md) -Attribut finden Sie ein Beispiel, das veranschaulicht, wie die Attribute des **Text** -Elements verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1cb1-112">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1cb1-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1cb1-113">Requirements</span></span>



| <span data-ttu-id="f1cb1-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f1cb1-114">Requirement</span></span> | <span data-ttu-id="f1cb1-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f1cb1-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="f1cb1-116">Version</span><span class="sxs-lookup"><span data-stu-id="f1cb1-116">Version</span></span><br/> | <span data-ttu-id="f1cb1-117">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="f1cb1-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f1cb1-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1cb1-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1cb1-119">**Text-Element**</span><span class="sxs-lookup"><span data-stu-id="f1cb1-119">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="f1cb1-120">**Text. Value**</span><span class="sxs-lookup"><span data-stu-id="f1cb1-120">**TEXT.value**</span></span>](text-value.md)
</dt> <dt>

[<span data-ttu-id="f1cb1-121">**Text. WordWrap**</span><span class="sxs-lookup"><span data-stu-id="f1cb1-121">**TEXT.wordWrap**</span></span>](text-wordwrap.md)
</dt> </dl>

 

 





