---
title: Design. openviewrelative
description: Die openviewrelative-Methode öffnet eine Ansicht in einem neuen Fenster an einer angegebenen Anfangsposition relativ zur oberen linken Ecke der Skin.
ms.assetid: fc31a1ce-e6b9-4084-b244-28fad486f485
keywords:
- Design. openviewrelative Windows-Media Player
topic_type:
- apiref
api_name:
- THEME.openViewRelative
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 80ec93055535640b84c33dde2b61ee59cd5bfdcf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368546"
---
# <a name="themeopenviewrelative"></a><span data-ttu-id="2e830-104">Design. openviewrelative</span><span class="sxs-lookup"><span data-stu-id="2e830-104">THEME.openViewRelative</span></span>

<span data-ttu-id="2e830-105">Die **openviewrelative** -Methode öffnet eine **Ansicht** in einem neuen Fenster an einer angegebenen Anfangsposition relativ zur oberen linken Ecke der Skin.</span><span class="sxs-lookup"><span data-stu-id="2e830-105">The **openViewRelative** method opens a **VIEW** in a new window at a specified initial position relative to the upper-left corner of the skin.</span></span>

``` syntax
        theme.openView(view, left, top)
```

## <a name="parameters"></a><span data-ttu-id="2e830-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e830-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e830-107"><span id="view"></span><span id="VIEW"></span>*Anschauung*</span><span class="sxs-lookup"><span data-stu-id="2e830-107"><span id="view"></span><span id="VIEW"></span>*view*</span></span>
</dt> <dd>

<span data-ttu-id="2e830-108">Eine **Zeichenfolge** , die die **ID** der zu öffnenden **Ansicht** angibt.</span><span class="sxs-lookup"><span data-stu-id="2e830-108">A **String** specifying the **id** of the **VIEW** to open.</span></span>

</dd> <dt>

<span data-ttu-id="2e830-109"><span id="left"></span><span id="LEFT"></span>*linken*</span><span class="sxs-lookup"><span data-stu-id="2e830-109"><span id="left"></span><span id="LEFT"></span>*left*</span></span>
</dt> <dd>

<span data-ttu-id="2e830-110">Eine **Zahl** (**Long**), die den anfänglichen Abstand des linken Rahmens der **Ansicht** vom linken Rand der Skin in Pixel angibt.</span><span class="sxs-lookup"><span data-stu-id="2e830-110">A **Number** (**long**) specifying the initial distance in pixels of the left border of the **VIEW** from the left border of the skin.</span></span> <span data-ttu-id="2e830-111">Ein negativer Wert gibt eine anfängliche Position links vom Skin-Rahmen an.</span><span class="sxs-lookup"><span data-stu-id="2e830-111">A negative value indicates an initial position to the left of the skin border.</span></span>

</dd> <dt>

<span data-ttu-id="2e830-112"><span id="top"></span><span id="TOP"></span>*Nach oben*</span><span class="sxs-lookup"><span data-stu-id="2e830-112"><span id="top"></span><span id="TOP"></span>*top*</span></span>
</dt> <dd>

<span data-ttu-id="2e830-113">Eine **Zahl** (**Long**), die die ursprüngliche Position des oberen Rahmens der **Ansicht** relativ zum oberen Rand der Skin angibt.</span><span class="sxs-lookup"><span data-stu-id="2e830-113">A **Number** (**long**) specifying the initial position of the top border of the **VIEW** relative to the top border of the skin.</span></span> <span data-ttu-id="2e830-114">Ein negativer Wert gibt eine Ausgangsposition oberhalb des Skin-Rahmens an.</span><span class="sxs-lookup"><span data-stu-id="2e830-114">A negative values indicates an initial position above the skin border.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e830-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e830-115">Return Value</span></span>

<span data-ttu-id="2e830-116">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2e830-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e830-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e830-117">Remarks</span></span>

<span data-ttu-id="2e830-118">Die für die **Ansicht** angegebene Position wird verwendet, wenn diese Methode zum ersten Mal aufgerufen wird, nach der der Benutzer die **Ansicht** an eine andere Position ziehen kann.</span><span class="sxs-lookup"><span data-stu-id="2e830-118">The position specified for the **VIEW** is used the first time this method is called, after which the user can drag the **VIEW** to another location.</span></span> <span data-ttu-id="2e830-119">Die neue Position wird gespeichert, und bei nachfolgenden Aufrufen wird die aktuelle Position verwendet.</span><span class="sxs-lookup"><span data-stu-id="2e830-119">The new position is saved, and on subsequent calls, the most recent position is used.</span></span>

## <a name="examples"></a><span data-ttu-id="2e830-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2e830-120">Examples</span></span>


```JScript
<THEME>
  <VIEW>
    <TEXT value="open" 
        onclick="jscript:theme.openViewRelative('newView', 50, 50)"/>
    <TEXT top="30" value="close" 
        onclick="jscript:theme.closeView('newView')"/>
  </VIEW>
  <VIEW id="newView"/>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="2e830-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e830-121">Requirements</span></span>



| <span data-ttu-id="2e830-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e830-122">Requirement</span></span> | <span data-ttu-id="2e830-123">Wert</span><span class="sxs-lookup"><span data-stu-id="2e830-123">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="2e830-124">Version</span><span class="sxs-lookup"><span data-stu-id="2e830-124">Version</span></span><br/> | <span data-ttu-id="2e830-125">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="2e830-125">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2e830-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e830-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e830-127">**Design-Element**</span><span class="sxs-lookup"><span data-stu-id="2e830-127">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="2e830-128">**Design. CloseView**</span><span class="sxs-lookup"><span data-stu-id="2e830-128">**THEME.closeView**</span></span>](theme-closeview.md)
</dt> <dt>

[<span data-ttu-id="2e830-129">**Design. OpenView**</span><span class="sxs-lookup"><span data-stu-id="2e830-129">**THEME.openView**</span></span>](theme-openview.md)
</dt> </dl>

 

 





