---
title: MM_JOY2MOVE Meldung (MMSYSTEM. h)
description: Die \_ Meldung mm JOY2MOVE benachrichtigt das Fenster, das den Joystick aufgezeichnet hat JOYSTICKID2, dass sich die Position des Joysticks geändert hat.
ms.assetid: 8dc1c092-3947-43d5-8504-a4e4e121fbcb
keywords:
- MM_JOY2MOVE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_JOY2MOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8921f0ae76d05c429d6750944a26662c1276af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103035"
---
# <a name="mm_joy2move-message"></a><span data-ttu-id="dd86c-104">MM \_ JOY2MOVE Meldung</span><span class="sxs-lookup"><span data-stu-id="dd86c-104">MM\_JOY2MOVE message</span></span>

<span data-ttu-id="dd86c-105">Die Meldung **mm \_ JOY2MOVE** benachrichtigt das Fenster, das den Joystick aufgezeichnet hat JOYSTICKID2, dass sich die Position des Joysticks geändert hat.</span><span class="sxs-lookup"><span data-stu-id="dd86c-105">The **MM\_JOY2MOVE** message notifies the window that has captured joystick JOYSTICKID2 that the joystick position has changed.</span></span>


```C++
MM_JOY2MOVE 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="dd86c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd86c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd86c-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*Schaltflächen*</span><span class="sxs-lookup"><span data-stu-id="dd86c-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span></span>
</dt> <dd>

<span data-ttu-id="dd86c-108">Gibt die Schaltflächen an, die gedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="dd86c-108">Identifies the buttons that are pressed.</span></span> <span data-ttu-id="dd86c-109">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="dd86c-109">It can be one or more of the following values:</span></span>



| <span data-ttu-id="dd86c-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dd86c-110">Requirement</span></span> | <span data-ttu-id="dd86c-111">Wert</span><span class="sxs-lookup"><span data-stu-id="dd86c-111">Value</span></span> |
|--------------|------------------------------------|
| <span data-ttu-id="dd86c-112">Freude \_ Button1</span><span class="sxs-lookup"><span data-stu-id="dd86c-112">JOY\_BUTTON1</span></span> | <span data-ttu-id="dd86c-113">Die erste Joystick Schaltfläche wird gedrückt.</span><span class="sxs-lookup"><span data-stu-id="dd86c-113">First joystick button is pressed.</span></span>  |
| <span data-ttu-id="dd86c-114">Freude \_ Button2</span><span class="sxs-lookup"><span data-stu-id="dd86c-114">JOY\_BUTTON2</span></span> | <span data-ttu-id="dd86c-115">Die zweite Joystick Schaltfläche wird gedrückt.</span><span class="sxs-lookup"><span data-stu-id="dd86c-115">Second joystick button is pressed.</span></span> |
| <span data-ttu-id="dd86c-116">Freude \_ BUTTON3</span><span class="sxs-lookup"><span data-stu-id="dd86c-116">JOY\_BUTTON3</span></span> | <span data-ttu-id="dd86c-117">Die dritte Joystick Schaltfläche wird gedrückt.</span><span class="sxs-lookup"><span data-stu-id="dd86c-117">Third joystick button is pressed.</span></span>  |
| <span data-ttu-id="dd86c-118">Freude \_ BUTTON4</span><span class="sxs-lookup"><span data-stu-id="dd86c-118">JOY\_BUTTON4</span></span> | <span data-ttu-id="dd86c-119">Fourth Joystick Schaltfläche wird gedrückt.</span><span class="sxs-lookup"><span data-stu-id="dd86c-119">Fourth joystick button is pressed.</span></span> |



 

</dd> <dt>

<span data-ttu-id="dd86c-120"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*XPos*</span><span class="sxs-lookup"><span data-stu-id="dd86c-120"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="dd86c-121">Die x-Koordinaten des Joysticks in Relation zur oberen linken Ecke des Client Bereichs.</span><span class="sxs-lookup"><span data-stu-id="dd86c-121">The x-coordinates of the joystick relative to the upper left corner of the client area.</span></span>

</dd> <dt>

<span data-ttu-id="dd86c-122"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*YPos*</span><span class="sxs-lookup"><span data-stu-id="dd86c-122"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="dd86c-123">Die y-Koordinate des Joysticks in Relation zur oberen linken Ecke des Client Bereichs.</span><span class="sxs-lookup"><span data-stu-id="dd86c-123">The y-coordinate of the joystick relative to the upper left corner of the client area.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd86c-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd86c-124">Requirements</span></span>



| <span data-ttu-id="dd86c-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dd86c-125">Requirement</span></span> | <span data-ttu-id="dd86c-126">Wert</span><span class="sxs-lookup"><span data-stu-id="dd86c-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd86c-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dd86c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="dd86c-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dd86c-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="dd86c-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dd86c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="dd86c-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dd86c-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="dd86c-131">Header</span><span class="sxs-lookup"><span data-stu-id="dd86c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd86c-132"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dd86c-132"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd86c-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd86c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd86c-134">Joystick</span><span class="sxs-lookup"><span data-stu-id="dd86c-134">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="dd86c-135">Multimedia-Joystick Nachrichten</span><span class="sxs-lookup"><span data-stu-id="dd86c-135">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 





