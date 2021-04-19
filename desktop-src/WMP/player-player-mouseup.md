---
title: Player. mousetup-Ereignis
description: Das MouseUp-Ereignis tritt auf, wenn der Benutzer eine Maustaste loslässt. | Player. mousetup-Ereignis
ms.assetid: 0f209fc4-2aad-46b1-84ba-2bfbecbe2930
keywords:
- Mouberup-Ereignisfenster Media Player
- Mousup-Ereignis, Windows Media Player, Player-Klasse
- Player-Klasse Windows Media Player, mousup-Ereignis
topic_type:
- apiref
api_name:
- Player.MouseUp
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50883ed8e5ea5696bd3aef1c5170959814de3026
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369469"
---
# <a name="playermouseup-event"></a><span data-ttu-id="b5b1a-107">Player. mousetup-Ereignis</span><span class="sxs-lookup"><span data-stu-id="b5b1a-107">Player.MouseUp event</span></span>

<span data-ttu-id="b5b1a-108">Das **MouseUp** -Ereignis tritt auf, wenn der Benutzer eine Maustaste loslässt.</span><span class="sxs-lookup"><span data-stu-id="b5b1a-108">The **MouseUp** event occurs when the user releases a mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5b1a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5b1a-109">Syntax</span></span>


```JScript
Player.MouseUp(
  nButton,
  nShiftState,
  fX,
  fY
)
```



## <a name="parameters"></a><span data-ttu-id="b5b1a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5b1a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5b1a-111">*nschaltfläche*</span><span class="sxs-lookup"><span data-stu-id="b5b1a-111">*nButton*</span></span> 
</dt> <dd>

<span data-ttu-id="b5b1a-112">**Number** (**int**): gibt ein Bitfeld mit Bits an, die der linken Schaltfläche (Bit 0), der rechten Schaltfläche (Bit 1) und der mittleren Schaltfläche (Bit 2) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b5b1a-112">**Number** (**int**) specifying a bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="b5b1a-113">Diese Bits entsprechen den Werten 1, 2 und 4.</span><span class="sxs-lookup"><span data-stu-id="b5b1a-113">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="b5b1a-114">Es wird nur einer der Bits festgelegt, der die Schaltfläche angibt, die das Ereignis verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="b5b1a-114">Only one of the bits is set, indicating the button that caused the event.</span></span>

</dd> <dt>

<span data-ttu-id="b5b1a-115">*nshiftstate*</span><span class="sxs-lookup"><span data-stu-id="b5b1a-115">*nShiftState*</span></span> 
</dt> <dd>

<span data-ttu-id="b5b1a-116">**Number** (**int**): gibt ein Bitfeld mit den geringsten signifikanten Bits an, die der Umschalttaste (Bit 0), der STRG-Taste (Bit 1) und der Alt-Taste (Bit 2) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b5b1a-116">**Number** (**int**) specifying a bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="b5b1a-117">Diese Bits entsprechen den Werten 1, 2 und 4.</span><span class="sxs-lookup"><span data-stu-id="b5b1a-117">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="b5b1a-118">Das Shift-Argument gibt den Zustand dieser Schlüssel an.</span><span class="sxs-lookup"><span data-stu-id="b5b1a-118">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="b5b1a-119">Einige, alle oder keine der Bits können festgelegt werden. Dies deutet darauf hin, dass einige, alle oder keine der Schlüssel gedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="b5b1a-119">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span>

</dd> <dt>

<span data-ttu-id="b5b1a-120">*Designer*</span><span class="sxs-lookup"><span data-stu-id="b5b1a-120">*fX*</span></span> 
</dt> <dd>

<span data-ttu-id="b5b1a-121">**Number** (**Long**) gibt die x-Koordinate des Mauszeigers relativ zur linken oberen Ecke des Steuer Elements an.</span><span class="sxs-lookup"><span data-stu-id="b5b1a-121">**Number** (**long**) specifying the x coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> <dt>

<span data-ttu-id="b5b1a-122">*herrlichen*</span><span class="sxs-lookup"><span data-stu-id="b5b1a-122">*fY*</span></span> 
</dt> <dd>

<span data-ttu-id="b5b1a-123">**Number** (**Long**) gibt die y-Koordinate des Mauszeigers relativ zur linken oberen Ecke des Steuer Elements an.</span><span class="sxs-lookup"><span data-stu-id="b5b1a-123">**Number** (**long**) specifying the y coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5b1a-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b5b1a-124">Return value</span></span>

<span data-ttu-id="b5b1a-125">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b5b1a-125">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5b1a-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b5b1a-126">Remarks</span></span>

<span data-ttu-id="b5b1a-127">Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich.</span><span class="sxs-lookup"><span data-stu-id="b5b1a-127">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="b5b1a-128">Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="b5b1a-128">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="b5b1a-129">**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b5b1a-129">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5b1a-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5b1a-130">Requirements</span></span>



| <span data-ttu-id="b5b1a-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5b1a-131">Requirement</span></span> | <span data-ttu-id="b5b1a-132">Wert</span><span class="sxs-lookup"><span data-stu-id="b5b1a-132">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b5b1a-133">Version</span><span class="sxs-lookup"><span data-stu-id="b5b1a-133">Version</span></span><br/> | <span data-ttu-id="b5b1a-134">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="b5b1a-134">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="b5b1a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="b5b1a-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="b5b1a-136"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5b1a-136"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5b1a-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5b1a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5b1a-138">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="b5b1a-138">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





