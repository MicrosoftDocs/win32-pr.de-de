---
title: MM_JOY2ZMOVE Meldung (MMSYSTEM. h)
description: Die mm \_ JOY2ZMOVE-Meldung benachrichtigt das Fenster, das den Joystick aufgezeichnet hat JOYSTICKID2, dass sich die Position des Joysticks auf der z-Achse geändert hat.
ms.assetid: f09a1a11-8c97-4a03-a388-8bf9ab89a3db
keywords:
- MM_JOY2ZMOVE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_JOY2ZMOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d899a4a1c93304075cb166ba805367ceed6ddd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342491"
---
# <a name="mm_joy2zmove-message"></a><span data-ttu-id="643e0-104">MM \_ JOY2ZMOVE Meldung</span><span class="sxs-lookup"><span data-stu-id="643e0-104">MM\_JOY2ZMOVE message</span></span>

<span data-ttu-id="643e0-105">Die **mm \_ JOY2ZMOVE** -Meldung benachrichtigt das Fenster, das den Joystick aufgezeichnet hat JOYSTICKID2, dass sich die Position des Joysticks auf der z-Achse geändert hat.</span><span class="sxs-lookup"><span data-stu-id="643e0-105">The **MM\_JOY2ZMOVE** message notifies the window that has captured joystick JOYSTICKID2 that the joystick position on the z-axis has changed.</span></span>


```C++
MM_JOY2ZMOVE 
fwButtons = wParam; 
zPos = LOWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="643e0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="643e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="643e0-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*Schaltflächen*</span><span class="sxs-lookup"><span data-stu-id="643e0-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span></span>
</dt> <dd>

<span data-ttu-id="643e0-108">Gibt die Schaltflächen an, die gedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="643e0-108">Identifies the buttons that are pressed.</span></span> <span data-ttu-id="643e0-109">Es kann sich um einen oder mehrere der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="643e0-109">It can be one or more of the following values.</span></span>



| <span data-ttu-id="643e0-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="643e0-110">Requirement</span></span> | <span data-ttu-id="643e0-111">Wert</span><span class="sxs-lookup"><span data-stu-id="643e0-111">Value</span></span> |
|--------------|------------------------------------|
| <span data-ttu-id="643e0-112">Freude \_ Button1</span><span class="sxs-lookup"><span data-stu-id="643e0-112">JOY\_BUTTON1</span></span> | <span data-ttu-id="643e0-113">Die erste Joystick Schaltfläche wird gedrückt.</span><span class="sxs-lookup"><span data-stu-id="643e0-113">First joystick button is pressed.</span></span>  |
| <span data-ttu-id="643e0-114">Freude \_ Button2</span><span class="sxs-lookup"><span data-stu-id="643e0-114">JOY\_BUTTON2</span></span> | <span data-ttu-id="643e0-115">Die zweite Joystick Schaltfläche wird gedrückt.</span><span class="sxs-lookup"><span data-stu-id="643e0-115">Second joystick button is pressed.</span></span> |
| <span data-ttu-id="643e0-116">Freude \_ BUTTON3</span><span class="sxs-lookup"><span data-stu-id="643e0-116">JOY\_BUTTON3</span></span> | <span data-ttu-id="643e0-117">Die dritte Joystick Schaltfläche wird gedrückt.</span><span class="sxs-lookup"><span data-stu-id="643e0-117">Third joystick button is pressed.</span></span>  |
| <span data-ttu-id="643e0-118">Freude \_ BUTTON4</span><span class="sxs-lookup"><span data-stu-id="643e0-118">JOY\_BUTTON4</span></span> | <span data-ttu-id="643e0-119">Fourth Joystick Schaltfläche wird gedrückt.</span><span class="sxs-lookup"><span data-stu-id="643e0-119">Fourth joystick button is pressed.</span></span> |



 

</dd> <dt>

<span data-ttu-id="643e0-120"><span id="zPos"></span><span id="zpos"></span><span id="ZPOS"></span>*ZPOS*</span><span class="sxs-lookup"><span data-stu-id="643e0-120"><span id="zPos"></span><span id="zpos"></span><span id="ZPOS"></span>*zPos*</span></span>
</dt> <dd>

<span data-ttu-id="643e0-121">Die z-Koordinate des Joysticks.</span><span class="sxs-lookup"><span data-stu-id="643e0-121">The z-coordinate of the joystick.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="643e0-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="643e0-122">Requirements</span></span>



| <span data-ttu-id="643e0-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="643e0-123">Requirement</span></span> | <span data-ttu-id="643e0-124">Wert</span><span class="sxs-lookup"><span data-stu-id="643e0-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="643e0-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="643e0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="643e0-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="643e0-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="643e0-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="643e0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="643e0-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="643e0-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="643e0-129">Header</span><span class="sxs-lookup"><span data-stu-id="643e0-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="643e0-130"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="643e0-130"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="643e0-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="643e0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="643e0-132">Joystick</span><span class="sxs-lookup"><span data-stu-id="643e0-132">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="643e0-133">Multimedia-Joystick Nachrichten</span><span class="sxs-lookup"><span data-stu-id="643e0-133">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 





