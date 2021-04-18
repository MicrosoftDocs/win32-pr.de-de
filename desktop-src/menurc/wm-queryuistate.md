---
title: WM_QUERYUISTATE Meldung (Winuser. h)
description: Eine Anwendung sendet die WM- \_ Abfrage queryuistate, um den Benutzeroberflächen Zustand für ein Fenster abzurufen.
ms.assetid: 3a9e3477-b5d7-4c55-b6d4-8a479451fee8
keywords:
- WM_QUERYUISTATE von Meldungs Menüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- WM_QUERYUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1574fe0dab2a0885c8012bf19eed50facfd6cce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338805"
---
# <a name="wm_queryuistate-message"></a><span data-ttu-id="60065-104">WM \_ queryuistate-Meldung</span><span class="sxs-lookup"><span data-stu-id="60065-104">WM\_QUERYUISTATE message</span></span>

<span data-ttu-id="60065-105">Eine Anwendung sendet die **WM- \_ Abfrage queryuistate** , um den Benutzeroberflächen Zustand für ein Fenster abzurufen.</span><span class="sxs-lookup"><span data-stu-id="60065-105">An application sends the **WM\_QUERYUISTATE** message to retrieve the UI state for a window.</span></span>


```C++
#define WM_QUERYUISTATE                 0x0129
```



## <a name="parameters"></a><span data-ttu-id="60065-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="60065-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60065-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="60065-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="60065-108">Dieser Parameter wird nicht verwendet und muss 0 sein.</span><span class="sxs-lookup"><span data-stu-id="60065-108">This parameter is not used and must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="60065-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="60065-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="60065-110">Dieser Parameter wird nicht verwendet und muss 0 sein.</span><span class="sxs-lookup"><span data-stu-id="60065-110">This parameter is not used and must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60065-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="60065-111">Return value</span></span>

<span data-ttu-id="60065-112">Der Rückgabewert ist **null** , wenn die Fokus Indikatoren und die Tastaturbeschleuniger sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="60065-112">The return value is **NULL** if the focus indicators and the keyboard accelerators are visible.</span></span> <span data-ttu-id="60065-113">Andernfalls kann der Rückgabewert einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="60065-113">Otherwise, the return value can be one or more of the following values.</span></span>



| <span data-ttu-id="60065-114">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="60065-114">Return code/value</span></span>                                                                                                                                       | <span data-ttu-id="60065-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60065-115">Description</span></span>                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="60065-116"><dt>**Uisf \_ Aktiv**</dt> <dt>0x4</dt></span><span class="sxs-lookup"><span data-stu-id="60065-116"><dt>**UISF\_ACTIVE**</dt> <dt>0x4</dt></span></span> </dl>    | <span data-ttu-id="60065-117">Ein Steuerelement sollte in dem Format gezeichnet werden, das für aktive Steuerelemente verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="60065-117">A control should be drawn in the style used for active controls.</span></span><br/> |
| <dl> <span data-ttu-id="60065-118"><dt>**Uisf \_ Hideaccel**</dt> <dt>0x2</dt></span><span class="sxs-lookup"><span data-stu-id="60065-118"><dt>**UISF\_HIDEACCEL**</dt> <dt>0x2</dt></span></span> </dl> | <span data-ttu-id="60065-119">Tastaturbeschleuniger werden ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="60065-119">Keyboard accelerators are hidden.</span></span><br/>                                |
| <dl> <span data-ttu-id="60065-120"><dt>**Uisf \_ Hidefocus**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="60065-120"><dt>**UISF\_HIDEFOCUS**</dt> <dt>0x1</dt></span></span> </dl> | <span data-ttu-id="60065-121">Fokus Indikatoren werden ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="60065-121">Focus indicators are hidden.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="60065-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60065-122">Requirements</span></span>



| <span data-ttu-id="60065-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60065-123">Requirement</span></span> | <span data-ttu-id="60065-124">Wert</span><span class="sxs-lookup"><span data-stu-id="60065-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60065-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="60065-125">Minimum supported client</span></span><br/> | <span data-ttu-id="60065-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60065-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="60065-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="60065-127">Minimum supported server</span></span><br/> | <span data-ttu-id="60065-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60065-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="60065-129">Header</span><span class="sxs-lookup"><span data-stu-id="60065-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="60065-130"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="60065-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60065-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60065-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="60065-132">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="60065-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="60065-133">**WM \_ changeuistate**</span><span class="sxs-lookup"><span data-stu-id="60065-133">**WM\_CHANGEUISTATE**</span></span>](wm-changeuistate.md)
</dt> <dt>

[<span data-ttu-id="60065-134">**WM \_ updateuistate**</span><span class="sxs-lookup"><span data-stu-id="60065-134">**WM\_UPDATEUISTATE**</span></span>](wm-updateuistate.md)
</dt> <dt>

<span data-ttu-id="60065-135">**Licher**</span><span class="sxs-lookup"><span data-stu-id="60065-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="60065-136">Tastaturkürzel</span><span class="sxs-lookup"><span data-stu-id="60065-136">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

 





