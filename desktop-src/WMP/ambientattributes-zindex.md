---
title: Ambientattribute. ZIndex
description: Das ZIndex-Attribut gibt die Reihenfolge an, in der das Steuerelement gerendert wird.
ms.assetid: b05c9efc-5d1d-4cba-89f4-b4200ce99e09
keywords:
- Fenster Media Player "ambientattribute. ZIndex"
topic_type:
- apiref
api_name:
- AmbientAttributes.zIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52480cc387c0a9e5e45c4b8e8fd2dae4199dbd16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372671"
---
# <a name="ambientattributeszindex"></a><span data-ttu-id="e27e5-104">Ambientattribute. ZIndex</span><span class="sxs-lookup"><span data-stu-id="e27e5-104">AmbientAttributes.zIndex</span></span>

<span data-ttu-id="e27e5-105">Das **ZIndex** -Attribut gibt die Reihenfolge an, in der das Steuerelement gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="e27e5-105">The **zIndex** attribute specifies or retrieves the order in which the control is rendered.</span></span>

``` syntax
        elementID.zIndex
```

## <a name="possible-values"></a><span data-ttu-id="e27e5-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="e27e5-106">Possible Values</span></span>

<span data-ttu-id="e27e5-107">Dieses Attribut ist eine Lese-/schreibzahl (**Long**) mit einem Standardwert von 0 (null). </span><span class="sxs-lookup"><span data-stu-id="e27e5-107">This attribute is a read/write **Number** (**long**) with a default value of zero.</span></span> <span data-ttu-id="e27e5-108">Der Bereich entspricht dem Wert einer langen ganzen Zahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="e27e5-108">The range is that of a signed long integer.</span></span>

## <a name="remarks"></a><span data-ttu-id="e27e5-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e27e5-109">Remarks</span></span>

<span data-ttu-id="e27e5-110">Die Hintergrund Bitmap einer **Sicht** oder **unter Ansicht** hat einen Fixed z-Index von 0 (null).</span><span class="sxs-lookup"><span data-stu-id="e27e5-110">The background bitmap of a **VIEW** or **SUBVIEW** has a fixed z index of zero.</span></span> <span data-ttu-id="e27e5-111">Wenn Sie möchten, dass ein Steuerelement hinter dem Hintergrund steht, muss der **ZIndex** auf eine negative Zahl festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e27e5-111">If you want a control to be behind the background, the **zIndex** must be set to a negative number.</span></span>

<span data-ttu-id="e27e5-112">Der z-Index einer **Sicht** oder **unter Ansicht** ist ein absoluter Index, während der z-Index eines Steuer Elements relativ zum z-Index der **Sicht** oder **unter Ansicht** ist, in der es enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="e27e5-112">The z index of a **VIEW** or **SUBVIEW** is an absolute index, while the z index of a control is relative to the z index of the **VIEW** or **SUBVIEW** that contains it.</span></span>

<span data-ttu-id="e27e5-113">Das **ZIndex** -Attribut wird vom **Browser** -und **Wiedergabe** Listenelement nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e27e5-113">The **zIndex** attribute is not supported by the **BROWSER** and **PLAYLIST** elements.</span></span> <span data-ttu-id="e27e5-114">Es funktioniert nicht mit dem **Video** -Element, wenn es sich um *Video* handelt. **Windows less** ist auf false festgelegt, ebenso wie das **Effects** -Element bei **Effekten**. " **Fenster** " ist auf "true" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e27e5-114">It will not work with the **VIDEO** element if *VIDEO*.**windowless** is set to false, nor with the **EFFECTS** element if **EFFECTS**.**windowed** is set to true.</span></span>

<span data-ttu-id="e27e5-115">**ButtonElement** -Elemente verwenden den **ZIndex** Ihrer **ButtonGroup**.</span><span class="sxs-lookup"><span data-stu-id="e27e5-115">**BUTTONELEMENT** elements use the **zIndex** of their **BUTTONGROUP**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e27e5-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e27e5-116">Requirements</span></span>



| <span data-ttu-id="e27e5-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e27e5-117">Requirement</span></span> | <span data-ttu-id="e27e5-118">Wert</span><span class="sxs-lookup"><span data-stu-id="e27e5-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="e27e5-119">Version</span><span class="sxs-lookup"><span data-stu-id="e27e5-119">Version</span></span><br/> | <span data-ttu-id="e27e5-120">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="e27e5-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e27e5-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e27e5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e27e5-122">**Ambient-Attribute**</span><span class="sxs-lookup"><span data-stu-id="e27e5-122">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





