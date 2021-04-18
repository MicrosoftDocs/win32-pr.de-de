---
title: MM_JOY2BUTTONDOWN Meldung (MMSYSTEM. h)
description: Die \_ Meldung mm JOY2BUTTONDOWN benachrichtigt das Fenster, das den Joystick JOYSTICKID2 aufgezeichnet hat, dass eine Schaltfläche gedrückt wurde.
ms.assetid: b4cd48ea-91ad-48e9-b0ae-58d8ee124171
keywords:
- MM_JOY2BUTTONDOWN-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_JOY2BUTTONDOWN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f155fcdc21247e01fd5d730f3f7d4daaba705e65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337291"
---
# <a name="mm_joy2buttondown-message"></a><span data-ttu-id="73951-104">MM \_ JOY2BUTTONDOWN Meldung</span><span class="sxs-lookup"><span data-stu-id="73951-104">MM\_JOY2BUTTONDOWN message</span></span>

<span data-ttu-id="73951-105">Die Meldung **mm \_ JOY2BUTTONDOWN** benachrichtigt das Fenster, das den Joystick JOYSTICKID2 aufgezeichnet hat, dass eine Schaltfläche gedrückt wurde.</span><span class="sxs-lookup"><span data-stu-id="73951-105">The **MM\_JOY2BUTTONDOWN** message notifies the window that has captured joystick JOYSTICKID2 that a button has been pressed.</span></span>


```C++
MM_JOY2BUTTONDOWN 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="73951-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="73951-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73951-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*Schaltflächen*</span><span class="sxs-lookup"><span data-stu-id="73951-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span></span>
</dt> <dd>

<span data-ttu-id="73951-108">Gibt die Schaltfläche an, die den Zustand geändert hat, und die gedrückten Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="73951-108">Identifies the button that has changed state and the buttons that are pressed.</span></span> <span data-ttu-id="73951-109">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="73951-109">It can be one of the following:</span></span>



| <span data-ttu-id="73951-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73951-110">Requirement</span></span> | <span data-ttu-id="73951-111">Wert</span><span class="sxs-lookup"><span data-stu-id="73951-111">Value</span></span> |
|-----------------|-------------------------------------------|
| <span data-ttu-id="73951-112">Freude \_ BUTTON1CHG</span><span class="sxs-lookup"><span data-stu-id="73951-112">JOY\_BUTTON1CHG</span></span> | <span data-ttu-id="73951-113">Der erste Joystick Schaltfläche hat den Zustand geändert.</span><span class="sxs-lookup"><span data-stu-id="73951-113">First joystick button has changed state.</span></span>  |
| <span data-ttu-id="73951-114">Freude \_ BUTTON2CHG</span><span class="sxs-lookup"><span data-stu-id="73951-114">JOY\_BUTTON2CHG</span></span> | <span data-ttu-id="73951-115">Die zweite Schaltfläche "Joystick" hat den Zustand geändert.</span><span class="sxs-lookup"><span data-stu-id="73951-115">Second joystick button has changed state.</span></span> |
| <span data-ttu-id="73951-116">Freude \_ BUTTON3CHG</span><span class="sxs-lookup"><span data-stu-id="73951-116">JOY\_BUTTON3CHG</span></span> | <span data-ttu-id="73951-117">Die dritte Schaltfläche "Joystick" hat den Zustand geändert.</span><span class="sxs-lookup"><span data-stu-id="73951-117">Third joystick button has changed state.</span></span>  |
| <span data-ttu-id="73951-118">Freude \_ BUTTON4CHG</span><span class="sxs-lookup"><span data-stu-id="73951-118">JOY\_BUTTON4CHG</span></span> | <span data-ttu-id="73951-119">Der vierte Joystick Schaltfläche hat den Zustand geändert.</span><span class="sxs-lookup"><span data-stu-id="73951-119">Fourth joystick button has changed state.</span></span> |



 

<span data-ttu-id="73951-120">und eine oder mehrere der folgenden Aktionen:</span><span class="sxs-lookup"><span data-stu-id="73951-120">and one or more of the following:</span></span>



| <span data-ttu-id="73951-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73951-121">Requirement</span></span> | <span data-ttu-id="73951-122">Wert</span><span class="sxs-lookup"><span data-stu-id="73951-122">Value</span></span> |
|--------------|------------------------------------|
| <span data-ttu-id="73951-123">Freude \_ Button1</span><span class="sxs-lookup"><span data-stu-id="73951-123">JOY\_BUTTON1</span></span> | <span data-ttu-id="73951-124">Die erste Joystick Schaltfläche wird gedrückt.</span><span class="sxs-lookup"><span data-stu-id="73951-124">First joystick button is pressed.</span></span>  |
| <span data-ttu-id="73951-125">Freude \_ Button2</span><span class="sxs-lookup"><span data-stu-id="73951-125">JOY\_BUTTON2</span></span> | <span data-ttu-id="73951-126">Die zweite Joystick Schaltfläche wird gedrückt.</span><span class="sxs-lookup"><span data-stu-id="73951-126">Second joystick button is pressed.</span></span> |
| <span data-ttu-id="73951-127">Freude \_ BUTTON3</span><span class="sxs-lookup"><span data-stu-id="73951-127">JOY\_BUTTON3</span></span> | <span data-ttu-id="73951-128">Die dritte Joystick Schaltfläche wird gedrückt.</span><span class="sxs-lookup"><span data-stu-id="73951-128">Third joystick button is pressed.</span></span>  |
| <span data-ttu-id="73951-129">Freude \_ BUTTON4</span><span class="sxs-lookup"><span data-stu-id="73951-129">JOY\_BUTTON4</span></span> | <span data-ttu-id="73951-130">Fourth Joystick Schaltfläche wird gedrückt.</span><span class="sxs-lookup"><span data-stu-id="73951-130">Fourth joystick button is pressed.</span></span> |



 

</dd> <dt>

<span data-ttu-id="73951-131"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*XPos*</span><span class="sxs-lookup"><span data-stu-id="73951-131"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="73951-132">Die x-Koordinaten des Joysticks in Relation zur oberen linken Ecke des Client Bereichs.</span><span class="sxs-lookup"><span data-stu-id="73951-132">The x-coordinates of the joystick relative to the upper left corner of the client area.</span></span>

</dd> <dt>

<span data-ttu-id="73951-133"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*YPos*</span><span class="sxs-lookup"><span data-stu-id="73951-133"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="73951-134">Die y-Koordinate des Joysticks in Relation zur oberen linken Ecke des Client Bereichs.</span><span class="sxs-lookup"><span data-stu-id="73951-134">The y-coordinate of the joystick relative to the upper left corner of the client area.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="73951-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73951-135">Requirements</span></span>



| <span data-ttu-id="73951-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73951-136">Requirement</span></span> | <span data-ttu-id="73951-137">Wert</span><span class="sxs-lookup"><span data-stu-id="73951-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73951-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="73951-138">Minimum supported client</span></span><br/> | <span data-ttu-id="73951-139">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73951-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="73951-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="73951-140">Minimum supported server</span></span><br/> | <span data-ttu-id="73951-141">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73951-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="73951-142">Header</span><span class="sxs-lookup"><span data-stu-id="73951-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="73951-143"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="73951-143"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73951-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73951-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73951-145">Joystick</span><span class="sxs-lookup"><span data-stu-id="73951-145">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="73951-146">Multimedia-Joystick Nachrichten</span><span class="sxs-lookup"><span data-stu-id="73951-146">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 





