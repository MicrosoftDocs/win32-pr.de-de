---
title: Ambientattribute. AlphaBlend
description: Das AlphaBlend-Attribut gibt einen Wert an, der eine beliebige Ansicht, unter Ansicht oder ein UI-Widget kombiniert, oder ruft diesen ab.
ms.assetid: a6c47d32-a497-4bfa-8fa3-ef94e267d94b
keywords:
- Ambientattribute. AlphaBlend-Fenster Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.alphaBlend
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8c0f0cb9d885f643b39acfbc5148403a5c8b788
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371479"
---
# <a name="ambientattributesalphablend"></a><span data-ttu-id="1c4ab-104">Ambientattribute. AlphaBlend</span><span class="sxs-lookup"><span data-stu-id="1c4ab-104">AmbientAttributes.alphaBlend</span></span>

<span data-ttu-id="1c4ab-105">Das **AlphaBlend** -Attribut gibt einen Wert an, der eine beliebige **Ansicht**, **unter Ansicht** oder ein UI-Widget kombiniert, oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="1c4ab-105">The **alphaBlend** attribute specifies or retrieves a value for alpha blending any **VIEW**, **SUBVIEW**, or UI widget.</span></span>

``` syntax
        elementID.alphaBlend
```

## <a name="possible-values"></a><span data-ttu-id="1c4ab-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="1c4ab-106">Possible Values</span></span>

<span data-ttu-id="1c4ab-107">Dieses Attribut ist eine Lese-/schreibzahl (**Long**) mit einem Wert zwischen 0 (keine Deckkraft) und 255 (vollständige Deckkraft) und dem Standardwert 255. </span><span class="sxs-lookup"><span data-stu-id="1c4ab-107">This attribute is a read/write **Number** (**long**) with a value ranging from 0 (no opacity) to 255 (full opacity) and a default value of 255.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c4ab-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1c4ab-108">Remarks</span></span>

<span data-ttu-id="1c4ab-109">Dieses Attribut ermöglicht, dass ein Element semitransparent angezeigt wird, abhängig von der Menge der festgelegten Deckkraft.</span><span class="sxs-lookup"><span data-stu-id="1c4ab-109">This attribute allows an element to appear semitransparent, depending on the amount of opacity set.</span></span> <span data-ttu-id="1c4ab-110">Die geringere Deckkraft, desto transparenter wird das Element angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1c4ab-110">The less opacity, the more transparent the element will appear.</span></span> <span data-ttu-id="1c4ab-111">Jedes Element in der Skin kann über einen separaten Deckkraft Wert verfügen, mit Ausnahme der Schaltflächen Elemente in einem **ButtonGroup** -Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="1c4ab-111">Each element in the skin can have a separate opacity value except for button elements in a **BUTTONGROUP** control.</span></span> <span data-ttu-id="1c4ab-112">Wenn **AlphaBlend** in der **Ansicht** festgelegt ist, wird die Deckkraft der gesamten Skin festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1c4ab-112">When **alphaBlend** is set in **VIEW**, the opacity of the entire skin will be set.</span></span> <span data-ttu-id="1c4ab-113">Alpha Blend funktioniert nicht für Fenster Steuerelemente, einschließlich **Wiedergabeliste**, **Effekten**, **ListBox**, **Popup**, **EditBox** und **Video** (wenn **Windows less** auf false festgelegt ist).</span><span class="sxs-lookup"><span data-stu-id="1c4ab-113">Alpha blend will not work for windowed controls, including **PLAYLIST**, **EFFECTS**, **LISTBOX**, **POPUP**, **EDITBOX**, and **VIDEO** (if **windowless** is set to false).</span></span> <span data-ttu-id="1c4ab-114">Wenn **AlphaBlend** auf **Ansicht** festgelegt wird, wird die gesamte Skin transparent.</span><span class="sxs-lookup"><span data-stu-id="1c4ab-114">When **alphaBlend** is set on **VIEW**, the whole skin becomes transparent.</span></span> <span data-ttu-id="1c4ab-115">Die von mehreren Elementen verwendeten **TransparencyColor** -Attribute werden bei **AlphaBlend** nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1c4ab-115">The **transparencyColor** attributes used by several elements are not supported with **alphaBlend**.</span></span>

<span data-ttu-id="1c4ab-116">Wenn Sie **AlphaBlend** mit einem **Text** Element verwenden, für das die **BackgroundColor** nicht angegeben ist, wird eine Hintergrundfarbe von Schwarz verwendet.</span><span class="sxs-lookup"><span data-stu-id="1c4ab-116">When you use **alphaBlend** with a **TEXT** element that does not have the **backgroundColor** specified, a background color of black will be used.</span></span> <span data-ttu-id="1c4ab-117">, Wenn die Vordergrundfarbe ebenfalls schwarz ist (Dies ist der Standardwert für *Text*).**ForegroundColor**), wird der Text möglicherweise nicht lesbar.</span><span class="sxs-lookup"><span data-stu-id="1c4ab-117">If the foreground color is also black (which is the default value for *TEXT*.**foregroundColor**), your text may become unreadable.</span></span> <span data-ttu-id="1c4ab-118">Um dies zu verhindern, geben Sie immer das **BackgroundColor** -Attribut an, oder legen Sie **ForegroundColor** auf eine andere Farbe als schwarz fest.</span><span class="sxs-lookup"><span data-stu-id="1c4ab-118">To prevent this, always specify the **backgroundColor** attribute, or set **foregroundColor** to a color other than black.</span></span>

> [!Note]  
> <span data-ttu-id="1c4ab-119">Dieses Attribut wird in Windows 98 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1c4ab-119">This attribute is not supported in Windows 98.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1c4ab-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1c4ab-120">Requirements</span></span>



| <span data-ttu-id="1c4ab-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1c4ab-121">Requirement</span></span> | <span data-ttu-id="1c4ab-122">Wert</span><span class="sxs-lookup"><span data-stu-id="1c4ab-122">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="1c4ab-123">Version</span><span class="sxs-lookup"><span data-stu-id="1c4ab-123">Version</span></span><br/> | <span data-ttu-id="1c4ab-124">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="1c4ab-124">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1c4ab-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c4ab-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c4ab-126">**Ambient-Attribute**</span><span class="sxs-lookup"><span data-stu-id="1c4ab-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="1c4ab-127">**Ambientattribute. alphablendto**</span><span class="sxs-lookup"><span data-stu-id="1c4ab-127">**AmbientAttributes.alphaBlendTo**</span></span>](ambientattributes-alphablendto.md)
</dt> <dt>

[<span data-ttu-id="1c4ab-128">**Text-Element**</span><span class="sxs-lookup"><span data-stu-id="1c4ab-128">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="1c4ab-129">**Text. BackgroundColor**</span><span class="sxs-lookup"><span data-stu-id="1c4ab-129">**TEXT.backgroundColor**</span></span>](text-backgroundcolor.md)
</dt> <dt>

[<span data-ttu-id="1c4ab-130">**Text. ForegroundColor**</span><span class="sxs-lookup"><span data-stu-id="1c4ab-130">**TEXT.foregroundColor**</span></span>](text-foregroundcolor.md)
</dt> </dl>

 

 





