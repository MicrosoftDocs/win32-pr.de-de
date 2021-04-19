---
title: Player. Click-Ereignis
description: Das Click-Ereignis tritt auf, wenn der Benutzer auf eine Maustaste klickt.
ms.assetid: c2d5fab9-9b53-4d0c-a001-8cbf4430e713
keywords:
- Klicken Sie auf Ereignisfenster Media Player
- Klicken Sie auf Ereignis Windows Media Player, Player-Klasse
- Windows Media Player Player-Klasse, Click-Ereignis
topic_type:
- apiref
api_name:
- Player.Click
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8389460d59018b221749719d32edbaa89943808
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370707"
---
# <a name="playerclick-event"></a><span data-ttu-id="f4e68-106">Player. Click-Ereignis</span><span class="sxs-lookup"><span data-stu-id="f4e68-106">Player.Click event</span></span>

<span data-ttu-id="f4e68-107">Das **Click** -Ereignis tritt auf, wenn der Benutzer auf eine Maustaste klickt.</span><span class="sxs-lookup"><span data-stu-id="f4e68-107">The **Click** event occurs when the user clicks a mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4e68-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4e68-108">Syntax</span></span>


```JScript
Player.Click(
  nButton,
  nShiftState,
  fX,
  fY
)
```



## <a name="parameters"></a><span data-ttu-id="f4e68-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4e68-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4e68-110">*nschaltfläche*</span><span class="sxs-lookup"><span data-stu-id="f4e68-110">*nButton*</span></span> 
</dt> <dd>

<span data-ttu-id="f4e68-111">**Number** (**int**): gibt ein Bitfeld mit Bits an, die der linken Schaltfläche (Bit 0), der rechten Schaltfläche (Bit 1) und der mittleren Schaltfläche (Bit 2) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="f4e68-111">**Number** (**int**) specifying a bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="f4e68-112">Diese Bits entsprechen den Werten 1, 2 und 4.</span><span class="sxs-lookup"><span data-stu-id="f4e68-112">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="f4e68-113">Es wird nur einer der Bits festgelegt, der die Schaltfläche angibt, die das Ereignis verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="f4e68-113">Only one of the bits is set, indicating the button that caused the event.</span></span>

</dd> <dt>

<span data-ttu-id="f4e68-114">*nshiftstate*</span><span class="sxs-lookup"><span data-stu-id="f4e68-114">*nShiftState*</span></span> 
</dt> <dd>

<span data-ttu-id="f4e68-115">**Number** (**int**): gibt ein Bitfeld mit den geringsten signifikanten Bits an, die der Umschalttaste (Bit 0), der STRG-Taste (Bit 1) und der Alt-Taste (Bit 2) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="f4e68-115">**Number** (**int**) specifying a bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="f4e68-116">Diese Bits entsprechen den Werten 1, 2 und 4.</span><span class="sxs-lookup"><span data-stu-id="f4e68-116">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="f4e68-117">Das Shift-Argument gibt den Zustand dieser Schlüssel an.</span><span class="sxs-lookup"><span data-stu-id="f4e68-117">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="f4e68-118">Einige, alle oder keine der Bits können festgelegt werden. Dies deutet darauf hin, dass einige, alle oder keine der Schlüssel gedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="f4e68-118">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span>

</dd> <dt>

<span data-ttu-id="f4e68-119">*Designer*</span><span class="sxs-lookup"><span data-stu-id="f4e68-119">*fX*</span></span> 
</dt> <dd>

<span data-ttu-id="f4e68-120">**Number** (**Long**) gibt die x-Koordinate des Mauszeigers relativ zur linken oberen Ecke des Steuer Elements an.</span><span class="sxs-lookup"><span data-stu-id="f4e68-120">**Number** (**long**) specifying the x coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> <dt>

<span data-ttu-id="f4e68-121">*herrlichen*</span><span class="sxs-lookup"><span data-stu-id="f4e68-121">*fY*</span></span> 
</dt> <dd>

<span data-ttu-id="f4e68-122">**Number** (**Long**) gibt die y-Koordinate des Mauszeigers relativ zur linken oberen Ecke des Steuer Elements an.</span><span class="sxs-lookup"><span data-stu-id="f4e68-122">**Number** (**long**) specifying the y coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4e68-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f4e68-123">Return value</span></span>

<span data-ttu-id="f4e68-124">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f4e68-124">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4e68-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4e68-125">Remarks</span></span>

<span data-ttu-id="f4e68-126">Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich.</span><span class="sxs-lookup"><span data-stu-id="f4e68-126">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="f4e68-127">Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="f4e68-127">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="f4e68-128">**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f4e68-128">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4e68-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4e68-129">Requirements</span></span>



| <span data-ttu-id="f4e68-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f4e68-130">Requirement</span></span> | <span data-ttu-id="f4e68-131">Wert</span><span class="sxs-lookup"><span data-stu-id="f4e68-131">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f4e68-132">Version</span><span class="sxs-lookup"><span data-stu-id="f4e68-132">Version</span></span><br/> | <span data-ttu-id="f4e68-133">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="f4e68-133">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="f4e68-134">DLL</span><span class="sxs-lookup"><span data-stu-id="f4e68-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="f4e68-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4e68-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4e68-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4e68-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4e68-137">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="f4e68-137">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





