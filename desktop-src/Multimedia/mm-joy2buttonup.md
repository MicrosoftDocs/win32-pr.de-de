---
title: MM_JOY2BUTTONUP Meldung (MMSYSTEM. h)
description: Die \_ Meldung mm JOY2BUTTONUP benachrichtigt das Fenster, das den Joystick aufgezeichnet hat JOYSTICKID2, dass eine Schaltfläche freigegeben wurde.
ms.assetid: da024466-7cd3-42ec-90a7-1468eb42841e
keywords:
- MM_JOY2BUTTONUP-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_JOY2BUTTONUP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7a4f2d23739fc72a6898e2b53fc3e1c330687f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346772"
---
# <a name="mm_joy2buttonup-message"></a><span data-ttu-id="24442-104">MM \_ JOY2BUTTONUP Meldung</span><span class="sxs-lookup"><span data-stu-id="24442-104">MM\_JOY2BUTTONUP message</span></span>

<span data-ttu-id="24442-105">Die Meldung **mm \_ JOY2BUTTONUP** benachrichtigt das Fenster, das den Joystick aufgezeichnet hat JOYSTICKID2, dass eine Schaltfläche freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="24442-105">The **MM\_JOY2BUTTONUP** message notifies the window that has captured joystick JOYSTICKID2 that a button has been released.</span></span>


```C++
MM_JOY2BUTTONUP 
fwButton = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="24442-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="24442-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24442-107">**Schaltflächen**</span><span class="sxs-lookup"><span data-stu-id="24442-107">**fwButtons**</span></span> 
</dt> <dd>

<span data-ttu-id="24442-108">Gibt die Schaltfläche an, die den Zustand geändert hat, und die gedrückten Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="24442-108">Identifies the button that has changed state and the buttons that are pressed.</span></span> <span data-ttu-id="24442-109">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="24442-109">It can be one of the following:</span></span>



| <span data-ttu-id="24442-110">Wert</span><span class="sxs-lookup"><span data-stu-id="24442-110">Value</span></span>                                                                                                                                                            | <span data-ttu-id="24442-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="24442-111">Meaning</span></span>                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="JOY_BUTTON1CHG"></span><span id="joy_button1chg"></span><dl> <span data-ttu-id="24442-112"><dt>**Freude \_ BUTTON1CHG**</dt></span><span class="sxs-lookup"><span data-stu-id="24442-112"><dt>**JOY\_BUTTON1CHG**</dt></span></span> </dl> | <span data-ttu-id="24442-113">Der erste Joystick Schaltfläche hat den Zustand geändert.</span><span class="sxs-lookup"><span data-stu-id="24442-113">First joystick button has changed state.</span></span><br/>  |
| <span id="JOY_BUTTON2CHG"></span><span id="joy_button2chg"></span><dl> <span data-ttu-id="24442-114"><dt>**Freude \_ BUTTON2CHG**</dt></span><span class="sxs-lookup"><span data-stu-id="24442-114"><dt>**JOY\_BUTTON2CHG**</dt></span></span> </dl> | <span data-ttu-id="24442-115">Die zweite Schaltfläche "Joystick" hat den Zustand geändert.</span><span class="sxs-lookup"><span data-stu-id="24442-115">Second joystick button has changed state.</span></span><br/> |
| <span id="JOY_BUTTON3CHG"></span><span id="joy_button3chg"></span><dl> <span data-ttu-id="24442-116"><dt>**Freude \_ BUTTON3CHG**</dt></span><span class="sxs-lookup"><span data-stu-id="24442-116"><dt>**JOY\_BUTTON3CHG**</dt></span></span> </dl> | <span data-ttu-id="24442-117">Die dritte Schaltfläche "Joystick" hat den Zustand geändert.</span><span class="sxs-lookup"><span data-stu-id="24442-117">Third joystick button has changed state.</span></span><br/>  |
| <span id="JOY_BUTTON4CHG"></span><span id="joy_button4chg"></span><dl> <span data-ttu-id="24442-118"><dt>**Freude \_ BUTTON4CHG**</dt></span><span class="sxs-lookup"><span data-stu-id="24442-118"><dt>**JOY\_BUTTON4CHG**</dt></span></span> </dl> | <span data-ttu-id="24442-119">Der vierte Joystick Schaltfläche hat den Zustand geändert.</span><span class="sxs-lookup"><span data-stu-id="24442-119">Fourth joystick button has changed state.</span></span><br/> |



 

<span data-ttu-id="24442-120">und eine oder mehrere der folgenden Aktionen:</span><span class="sxs-lookup"><span data-stu-id="24442-120">and one or more of the following:</span></span>



| <span data-ttu-id="24442-121">Wert</span><span class="sxs-lookup"><span data-stu-id="24442-121">Value</span></span>                                                                                                                                                   | <span data-ttu-id="24442-122">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="24442-122">Meaning</span></span>                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="JOY_BUTTON1"></span><span id="joy_button1"></span><dl> <span data-ttu-id="24442-123"><dt>**Freude \_ Button1**</dt></span><span class="sxs-lookup"><span data-stu-id="24442-123"><dt>**JOY\_BUTTON1**</dt></span></span> </dl> | <span data-ttu-id="24442-124">Die erste Joystick Schaltfläche wird gedrückt.</span><span class="sxs-lookup"><span data-stu-id="24442-124">First joystick button is pressed.</span></span><br/>  |
| <span id="JOY_BUTTON2"></span><span id="joy_button2"></span><dl> <span data-ttu-id="24442-125"><dt>**Freude \_ Button2**</dt></span><span class="sxs-lookup"><span data-stu-id="24442-125"><dt>**JOY\_BUTTON2**</dt></span></span> </dl> | <span data-ttu-id="24442-126">Die zweite Joystick Schaltfläche wird gedrückt.</span><span class="sxs-lookup"><span data-stu-id="24442-126">Second joystick button is pressed.</span></span><br/> |
| <span id="JOY_BUTTON3"></span><span id="joy_button3"></span><dl> <span data-ttu-id="24442-127"><dt>**Freude \_ BUTTON3**</dt></span><span class="sxs-lookup"><span data-stu-id="24442-127"><dt>**JOY\_BUTTON3**</dt></span></span> </dl> | <span data-ttu-id="24442-128">Die dritte Joystick Schaltfläche wird gedrückt.</span><span class="sxs-lookup"><span data-stu-id="24442-128">Third joystick button is pressed.</span></span><br/>  |
| <span id="JOY_BUTTON4"></span><span id="joy_button4"></span><dl> <span data-ttu-id="24442-129"><dt>**Freude \_ BUTTON4**</dt></span><span class="sxs-lookup"><span data-stu-id="24442-129"><dt>**JOY\_BUTTON4**</dt></span></span> </dl> | <span data-ttu-id="24442-130">Fourth Joystick Schaltfläche wird gedrückt.</span><span class="sxs-lookup"><span data-stu-id="24442-130">Fourth joystick button is pressed.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="24442-131">**XPos**</span><span class="sxs-lookup"><span data-stu-id="24442-131">**xPos**</span></span> 
</dt> <dd>

<span data-ttu-id="24442-132">Die x-Koordinaten des Joysticks in Relation zur oberen linken Ecke des Client Bereichs.</span><span class="sxs-lookup"><span data-stu-id="24442-132">The x-coordinates of the joystick relative to the upper left corner of the client area.</span></span>

</dd> <dt>

<span data-ttu-id="24442-133">**YPos**</span><span class="sxs-lookup"><span data-stu-id="24442-133">**yPos**</span></span> 
</dt> <dd>

<span data-ttu-id="24442-134">Die y-Koordinate des Joysticks in Relation zur oberen linken Ecke des Client Bereichs.</span><span class="sxs-lookup"><span data-stu-id="24442-134">The y-coordinate of the joystick relative to the upper left corner of the client area.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="24442-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="24442-135">Requirements</span></span>



| <span data-ttu-id="24442-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="24442-136">Requirement</span></span> | <span data-ttu-id="24442-137">Wert</span><span class="sxs-lookup"><span data-stu-id="24442-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24442-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="24442-138">Minimum supported client</span></span><br/> | <span data-ttu-id="24442-139">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="24442-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="24442-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="24442-140">Minimum supported server</span></span><br/> | <span data-ttu-id="24442-141">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="24442-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="24442-142">Header</span><span class="sxs-lookup"><span data-stu-id="24442-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="24442-143"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="24442-143"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24442-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24442-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24442-145">Joystick</span><span class="sxs-lookup"><span data-stu-id="24442-145">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="24442-146">Multimedia-Joystick Nachrichten</span><span class="sxs-lookup"><span data-stu-id="24442-146">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 





