---
title: WM_GETHOTKEY Meldung (Winuser. h)
description: Wird gesendet, um den einem Fenster zugeordneten Hot-Schlüssel zu bestimmen.
ms.assetid: 6f527758-e713-47a8-a571-3bf3270f0b33
keywords:
- Tastatur-und Maus Eingaben für WM_GETHOTKEY Nachricht
topic_type:
- apiref
api_name:
- WM_GETHOTKEY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f045ceefaf33c8d8edba0cb69e062ad589cfd833
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476158"
---
# <a name="wm_gethotkey-message"></a><span data-ttu-id="3e5ad-104">WM- \_ GetHotKey-Nachricht</span><span class="sxs-lookup"><span data-stu-id="3e5ad-104">WM\_GETHOTKEY message</span></span>

<span data-ttu-id="3e5ad-105">Wird gesendet, um den einem Fenster zugeordneten Hot-Schlüssel zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="3e5ad-105">Sent to determine the hot key associated with a window.</span></span>


```C++
#define WM_GETHOTKEY                    0x0033
```



## <a name="parameters"></a><span data-ttu-id="3e5ad-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e5ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e5ad-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3e5ad-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3e5ad-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="3e5ad-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3e5ad-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3e5ad-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3e5ad-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="3e5ad-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e5ad-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3e5ad-111">Return value</span></span>

<span data-ttu-id="3e5ad-112">Der Rückgabewert ist der Code und die modifiziererer des virtuellen Schlüssels für die Hot-Taste, oder **null** , wenn dem Fenster keine heiße Taste zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3e5ad-112">The return value is the virtual-key code and modifiers for the hot key, or **NULL** if no hot key is associated with the window.</span></span> <span data-ttu-id="3e5ad-113">Der Code für den virtuellen Schlüssel befindet sich im unteren Byte des Rückgabewerts, und die Modifizierer sind im hohen Byte.</span><span class="sxs-lookup"><span data-stu-id="3e5ad-113">The virtual-key code is in the low byte of the return value and the modifiers are in the high byte.</span></span> <span data-ttu-id="3e5ad-114">Die modifiziererer können eine Kombination der folgenden Flags aus "kommctrl. h" sein.</span><span class="sxs-lookup"><span data-stu-id="3e5ad-114">The modifiers can be a combination of the following flags from CommCtrl.h.</span></span>



| <span data-ttu-id="3e5ad-115">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="3e5ad-115">Return code/value</span></span>                                                                                                                                         | <span data-ttu-id="3e5ad-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e5ad-116">Description</span></span>             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <dl> <span data-ttu-id="3e5ad-117"><dt>**Hotkeyf \_ ALT**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="3e5ad-117"><dt>**HOTKEYF\_ALT**</dt> <dt>0x04</dt></span></span> </dl>     | <span data-ttu-id="3e5ad-118">ALT-TASTE</span><span class="sxs-lookup"><span data-stu-id="3e5ad-118">ALT key</span></span><br/>      |
| <dl> <span data-ttu-id="3e5ad-119"><dt>**Hotkeyf \_ Steuer**</dt> Element <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="3e5ad-119"><dt>**HOTKEYF\_CONTROL**</dt> <dt>0x02</dt></span></span> </dl> | <span data-ttu-id="3e5ad-120">STRG-Taste</span><span class="sxs-lookup"><span data-stu-id="3e5ad-120">CTRL key</span></span><br/>     |
| <dl> <span data-ttu-id="3e5ad-121"><dt>**Hotkeyf \_ EXT**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="3e5ad-121"><dt>**HOTKEYF\_EXT**</dt> <dt>0x08</dt></span></span> </dl>     | <span data-ttu-id="3e5ad-122">Erweiterter Schlüssel</span><span class="sxs-lookup"><span data-stu-id="3e5ad-122">Extended key</span></span><br/> |
| <dl> <span data-ttu-id="3e5ad-123"><dt>**Hotkeyf \_ UMSCHALT**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="3e5ad-123"><dt>**HOTKEYF\_SHIFT**</dt> <dt>0x01</dt></span></span> </dl>   | <span data-ttu-id="3e5ad-124">Umschalttaste</span><span class="sxs-lookup"><span data-stu-id="3e5ad-124">SHIFT key</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="3e5ad-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e5ad-125">Remarks</span></span>

<span data-ttu-id="3e5ad-126">Diese Hotkeys sind nicht mit den von der [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) -Funktion festgelegten Hotkeys verknüpft.</span><span class="sxs-lookup"><span data-stu-id="3e5ad-126">These hot keys are unrelated to the hot keys set by the [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e5ad-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e5ad-127">Requirements</span></span>



| <span data-ttu-id="3e5ad-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3e5ad-128">Requirement</span></span> | <span data-ttu-id="3e5ad-129">Wert</span><span class="sxs-lookup"><span data-stu-id="3e5ad-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e5ad-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3e5ad-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3e5ad-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3e5ad-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3e5ad-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3e5ad-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3e5ad-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3e5ad-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3e5ad-134">Header</span><span class="sxs-lookup"><span data-stu-id="3e5ad-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e5ad-135"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="3e5ad-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e5ad-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e5ad-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="3e5ad-137">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="3e5ad-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3e5ad-138">**RegisterHotKey**</span><span class="sxs-lookup"><span data-stu-id="3e5ad-138">**RegisterHotKey**</span></span>](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[<span data-ttu-id="3e5ad-139">**WM- \_ Objekt Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="3e5ad-139">**WM\_SETHOTKEY**</span></span>](wm-sethotkey.md)
</dt> <dt>

<span data-ttu-id="3e5ad-140">**Licher**</span><span class="sxs-lookup"><span data-stu-id="3e5ad-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3e5ad-141">Tastatureingabe</span><span class="sxs-lookup"><span data-stu-id="3e5ad-141">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

