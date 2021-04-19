---
title: Player. mousermove-Ereignis
description: Das MouseMove-Ereignis tritt auf, wenn der Mauszeiger verschoben wird. | Player. mousermove-Ereignis
ms.assetid: 026928a3-25a6-4e67-837a-df71c05e49ee
keywords:
- Media Player "mousmove-Ereignisfenster"
- Mousmove-Ereignis, Windows Media Player, Player-Klasse
- Player-Klasse, Windows Media Player, mousmove-Ereignis
topic_type:
- apiref
api_name:
- Player.MouseMove
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a536609ba5e3095fed9826b071084491a81b385f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358010"
---
# <a name="playermousemove-event"></a><span data-ttu-id="0b1cc-107">Player. mousermove-Ereignis</span><span class="sxs-lookup"><span data-stu-id="0b1cc-107">Player.MouseMove event</span></span>

<span data-ttu-id="0b1cc-108">Das **MouseMove** -Ereignis tritt auf, wenn der Mauszeiger verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="0b1cc-108">The **MouseMove** event occurs when the mouse pointer is moved.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b1cc-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b1cc-109">Syntax</span></span>


```JScript
Player.MouseMove(
  nButton,
  nShiftState,
  fX,
  fY
)
```



## <a name="parameters"></a><span data-ttu-id="0b1cc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b1cc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b1cc-111">*nschaltfläche*</span><span class="sxs-lookup"><span data-stu-id="0b1cc-111">*nButton*</span></span> 
</dt> <dd>

<span data-ttu-id="0b1cc-112">**Number** (**int**): gibt ein Bitfeld mit Bits an, die der linken Schaltfläche (Bit 0), der rechten Schaltfläche (Bit 1) und der mittleren Schaltfläche (Bit 2) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0b1cc-112">**Number** (**int**) specifying a bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="0b1cc-113">Diese Bits entsprechen den Werten 1, 2 und 4.</span><span class="sxs-lookup"><span data-stu-id="0b1cc-113">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="0b1cc-114">Einige, alle oder keine der Bits können festgelegt werden. Dies deutet darauf hin, dass einige, alle oder keine der Schaltflächen gedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="0b1cc-114">Some, all, or none of the bits can be set, indicating that some, all, or none of the buttons are pressed.</span></span>

</dd> <dt>

<span data-ttu-id="0b1cc-115">*nshiftstate*</span><span class="sxs-lookup"><span data-stu-id="0b1cc-115">*nShiftState*</span></span> 
</dt> <dd>

<span data-ttu-id="0b1cc-116">**Number** (**int**): gibt ein Bitfeld mit den geringsten signifikanten Bits an, die der Umschalttaste (Bit 0), der STRG-Taste (Bit 1) und der Alt-Taste (Bit 2) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0b1cc-116">**Number** (**int**) specifying a bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="0b1cc-117">Diese Bits entsprechen den Werten 1, 2 und 4.</span><span class="sxs-lookup"><span data-stu-id="0b1cc-117">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="0b1cc-118">Das Shift-Argument gibt den Zustand dieser Schlüssel an.</span><span class="sxs-lookup"><span data-stu-id="0b1cc-118">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="0b1cc-119">Einige, alle oder keine der Bits können festgelegt werden. Dies deutet darauf hin, dass einige, alle oder keine der Schlüssel gedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="0b1cc-119">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span>

</dd> <dt>

<span data-ttu-id="0b1cc-120">*Designer*</span><span class="sxs-lookup"><span data-stu-id="0b1cc-120">*fX*</span></span> 
</dt> <dd>

<span data-ttu-id="0b1cc-121">**Number** (**Long**) gibt die x-Koordinate des Mauszeigers relativ zur linken oberen Ecke des Steuer Elements an.</span><span class="sxs-lookup"><span data-stu-id="0b1cc-121">**Number** (**long**) specifying the x coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> <dt>

<span data-ttu-id="0b1cc-122">*herrlichen*</span><span class="sxs-lookup"><span data-stu-id="0b1cc-122">*fY*</span></span> 
</dt> <dd>

<span data-ttu-id="0b1cc-123">**Number** (**Long**) gibt die y-Koordinate des Mauszeigers relativ zur linken oberen Ecke des Steuer Elements an.</span><span class="sxs-lookup"><span data-stu-id="0b1cc-123">**Number** (**long**) specifying the y coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b1cc-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0b1cc-124">Return value</span></span>

<span data-ttu-id="0b1cc-125">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0b1cc-125">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b1cc-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b1cc-126">Remarks</span></span>

<span data-ttu-id="0b1cc-127">Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich.</span><span class="sxs-lookup"><span data-stu-id="0b1cc-127">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="0b1cc-128">Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="0b1cc-128">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="0b1cc-129">**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0b1cc-129">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b1cc-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b1cc-130">Requirements</span></span>



| <span data-ttu-id="0b1cc-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b1cc-131">Requirement</span></span> | <span data-ttu-id="0b1cc-132">Wert</span><span class="sxs-lookup"><span data-stu-id="0b1cc-132">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0b1cc-133">Version</span><span class="sxs-lookup"><span data-stu-id="0b1cc-133">Version</span></span><br/> | <span data-ttu-id="0b1cc-134">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="0b1cc-134">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="0b1cc-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0b1cc-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="0b1cc-136"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b1cc-136"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b1cc-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b1cc-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b1cc-138">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="0b1cc-138">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





