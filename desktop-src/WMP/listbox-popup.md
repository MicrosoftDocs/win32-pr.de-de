---
title: ListBox. popUp
description: Das Popup Attribut gibt einen Wert an, der angibt, ob das Element ein popUp-oder Listenfeld-Steuerelement darstellt.
ms.assetid: b0ade23a-6164-4dd4-b599-43ea1fcd44e4
keywords:
- ListBox. popUp-Fenster Media Player
topic_type:
- apiref
api_name:
- LISTBOX.popUp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43d197adbdf2ec27ea6ef7bf04c5c71d15ae923d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372365"
---
# <a name="listboxpopup"></a><span data-ttu-id="809b0-104">ListBox. popUp</span><span class="sxs-lookup"><span data-stu-id="809b0-104">LISTBOX.popUp</span></span>

<span data-ttu-id="809b0-105">Das **Popup** Attribut gibt einen Wert an, der angibt, ob das Element ein popUp-oder Listenfeld-Steuerelement darstellt.</span><span class="sxs-lookup"><span data-stu-id="809b0-105">The **popUp** attribute specifies a value indicating whether the element represents a popup or list box control.</span></span>

``` syntax
<ELEMENT popUp="value">
```

## <a name="possible-values"></a><span data-ttu-id="809b0-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="809b0-106">Possible Values</span></span>

<span data-ttu-id="809b0-107">Dieses Attribut ist ein **boolescher** Wert, der nur zur Entwurfszeit angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="809b0-107">This attribute is a **Boolean** specified at design time only.</span></span>



| <span data-ttu-id="809b0-108">Wert</span><span class="sxs-lookup"><span data-stu-id="809b0-108">Value</span></span> | <span data-ttu-id="809b0-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="809b0-109">Description</span></span>                                |
|-------|--------------------------------------------|
| <span data-ttu-id="809b0-110">true</span><span class="sxs-lookup"><span data-stu-id="809b0-110">true</span></span>  | <span data-ttu-id="809b0-111">Das-Element stellt ein Popup-Steuerelement dar.</span><span class="sxs-lookup"><span data-stu-id="809b0-111">The element represents a popup control.</span></span>    |
| <span data-ttu-id="809b0-112">false</span><span class="sxs-lookup"><span data-stu-id="809b0-112">false</span></span> | <span data-ttu-id="809b0-113">Das-Element stellt ein Listenfeld-Steuerelement dar.</span><span class="sxs-lookup"><span data-stu-id="809b0-113">The element represents a list box control.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="809b0-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="809b0-114">Remarks</span></span>

<span data-ttu-id="809b0-115">Das **Popup** -Element stellt ein Listenfeld-Steuerelement dar, das nur bei Bedarf angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="809b0-115">The **POPUP** element represents a list box control that is displayed only when needed.</span></span> <span data-ttu-id="809b0-116">Sie ist mit dem **ListBox** -Element identisch, außer dem Standardwert dieses Attributs, das das Anzeigeverhalten ändert.</span><span class="sxs-lookup"><span data-stu-id="809b0-116">It is identical to the **LISTBOX** element except for the default value of this attribute, which changes the display behavior.</span></span> <span data-ttu-id="809b0-117">Der Standardwert für **ListBox** -Elemente ist false.</span><span class="sxs-lookup"><span data-stu-id="809b0-117">For **LISTBOX** elements, the default value is false.</span></span> <span data-ttu-id="809b0-118">Für **Popup** Elemente ist der Standardwert true.</span><span class="sxs-lookup"><span data-stu-id="809b0-118">For **POPUP** elements, the default value is true.</span></span> <span data-ttu-id="809b0-119">Anstatt dieses Attribut anzugeben, sollte das **ListBox** -oder **Popup** Element entsprechend dem gewünschten Verhalten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="809b0-119">Instead of specifying this attribute, the **LISTBOX** or **POPUP** element should be used to according to the desired behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="809b0-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="809b0-120">Requirements</span></span>



| <span data-ttu-id="809b0-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="809b0-121">Requirement</span></span> | <span data-ttu-id="809b0-122">Wert</span><span class="sxs-lookup"><span data-stu-id="809b0-122">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="809b0-123">Version</span><span class="sxs-lookup"><span data-stu-id="809b0-123">Version</span></span><br/> | <span data-ttu-id="809b0-124">Windows Media Player für Windows XP oder höher</span><span class="sxs-lookup"><span data-stu-id="809b0-124">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="809b0-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="809b0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="809b0-126">**ListBox-Element**</span><span class="sxs-lookup"><span data-stu-id="809b0-126">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> <dt>

[<span data-ttu-id="809b0-127">**Popup-Element**</span><span class="sxs-lookup"><span data-stu-id="809b0-127">**POPUP Element**</span></span>](popup-element.md)
</dt> </dl>

 

 





