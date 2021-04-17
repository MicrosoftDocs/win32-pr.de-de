---
description: Tritt ein, wenn der Benutzer eine Taste loslässt, während das InkEdit-Steuerelement den Fokus besitzt.
ms.assetid: 973d99f2-df09-4315-aaab-72877272100b
title: InkEdit. KeyUp-Ereignis (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 590f5f6b2e81e1996bca973f4994c0eade7ead18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530044"
---
# <a name="inkeditkeyup-event"></a><span data-ttu-id="6edfc-103">InkEdit. KeyUp-Ereignis</span><span class="sxs-lookup"><span data-stu-id="6edfc-103">InkEdit.KeyUp event</span></span>

<span data-ttu-id="6edfc-104">Tritt ein, wenn der Benutzer eine Taste loslässt, während das [InkEdit](inkedit-control-reference.md) -Steuerelement den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="6edfc-104">Occurs when the user releases a key while the [InkEdit](inkedit-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="6edfc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6edfc-105">Syntax</span></span>


```C++
HRESULT KeyUp(
   Long  *pKey,
   short ShiftKey
);
```



## <a name="parameters"></a><span data-ttu-id="6edfc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6edfc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6edfc-107">*pkey*</span><span class="sxs-lookup"><span data-stu-id="6edfc-107">*pKey*</span></span> 
</dt> <dd>

<span data-ttu-id="6edfc-108">Der Code des virtuellen Schlüssels, der vom Benutzer gedrückt wurde.</span><span class="sxs-lookup"><span data-stu-id="6edfc-108">The virtual-key code of the key pressed by the user.</span></span>

</dd> <dt>

<span data-ttu-id="6edfc-109">*ShiftKey*</span><span class="sxs-lookup"><span data-stu-id="6edfc-109">*ShiftKey*</span></span> 
</dt> <dd>

<span data-ttu-id="6edfc-110">Ein Member der [**inkshiftkeymodifierflags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) -Enumeration, der angibt, welche modifiziererschlüssel zum Zeitpunkt des Ereignisses gedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="6edfc-110">A member of the [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) enumeration that indicates which modifier keys are depressed at the time of the event.</span></span>



| <span data-ttu-id="6edfc-111">Wert</span><span class="sxs-lookup"><span data-stu-id="6edfc-111">Value</span></span>                                                                                                                                                                                     | <span data-ttu-id="6edfc-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6edfc-112">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <span data-ttu-id="6edfc-113"><dt>**IKM- \_ Schicht**</dt></span><span class="sxs-lookup"><span data-stu-id="6edfc-113"><dt>**IKM\_Shift**</dt></span></span> </dl>             | <span data-ttu-id="6edfc-114">Gibt an, dass die Umschalttaste als Modifizierer verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="6edfc-114">Specifies that the SHIFT key was used as a modifier.</span></span> <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <span data-ttu-id="6edfc-115"><dt>**IKM \_ Steuer** Element</dt></span><span class="sxs-lookup"><span data-stu-id="6edfc-115"><dt>**IKM\_Control** </dt></span></span> </dl> | <span data-ttu-id="6edfc-116">Gibt an, dass die STRG-Taste als Modifizierer verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="6edfc-116">Specifies that the CTRL key was used as a modifier.</span></span> <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <span data-ttu-id="6edfc-117"><dt>**IKM \_ Alt**</dt></span><span class="sxs-lookup"><span data-stu-id="6edfc-117"><dt>**IKM\_Alt** </dt></span></span> </dl>                 | <span data-ttu-id="6edfc-118">Gibt an, dass die Alt-Taste als Modifizierer verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="6edfc-118">Specifies that the ALT key was used as a modifier.</span></span> <br/>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6edfc-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6edfc-119">Return value</span></span>

<span data-ttu-id="6edfc-120">Wenn dieses Ereignis erfolgreich ist, gibt es " **S \_ OK**" zurück.</span><span class="sxs-lookup"><span data-stu-id="6edfc-120">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6edfc-121">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6edfc-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6edfc-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6edfc-122">Remarks</span></span>

<span data-ttu-id="6edfc-123">Diese Ereignismethode wird in der **\_ iinkeditevents** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="6edfc-123">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="6edfc-124">Die **\_ iinkeditevents** -Schnittstelle implementiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner DISPID \_ ieekeyup.</span><span class="sxs-lookup"><span data-stu-id="6edfc-124">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeKeyUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="6edfc-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6edfc-125">Requirements</span></span>



| <span data-ttu-id="6edfc-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6edfc-126">Requirement</span></span> | <span data-ttu-id="6edfc-127">Wert</span><span class="sxs-lookup"><span data-stu-id="6edfc-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6edfc-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6edfc-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6edfc-129">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6edfc-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6edfc-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6edfc-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6edfc-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6edfc-131">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="6edfc-132">Header</span><span class="sxs-lookup"><span data-stu-id="6edfc-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="6edfc-133"><dt>In "-. h" (auch als "gezeichneten \_ i. c" erforderlich)</dt></span><span class="sxs-lookup"><span data-stu-id="6edfc-133"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6edfc-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6edfc-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="6edfc-135"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6edfc-135"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="6edfc-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6edfc-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6edfc-137">InkEdit</span><span class="sxs-lookup"><span data-stu-id="6edfc-137">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="6edfc-138">**Inkshiftkeymodifierflags-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="6edfc-138">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

<span data-ttu-id="6edfc-139">[**KeyDown-Ereignis, \[ InkEdit-Steuerelement\]**](inkedit-keydown.md)</span><span class="sxs-lookup"><span data-stu-id="6edfc-139">[**KeyDown Event \[InkEdit Control\]**](inkedit-keydown.md)</span></span>
</dt> <dt>

<span data-ttu-id="6edfc-140">[**KeyPress-Ereignis, \[ InkEdit-Steuerelement\]**](inkedit-keypress.md)</span><span class="sxs-lookup"><span data-stu-id="6edfc-140">[**KeyPress Event \[InkEdit Control\]**](inkedit-keypress.md)</span></span>
</dt> </dl>

 

