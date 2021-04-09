---
title: WM_DESTROYCLIPBOARD Meldung (Winuser. h)
description: Wird an den Besitzer der Zwischenablage gesendet, wenn ein Aufrufe der EmptyClipboard-Funktion die Zwischenablage leert. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: 9f75b7fb-e9ae-4876-ba99-7db931b9c2ff
keywords:
- WM_DESTROYCLIPBOARD Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_DESTROYCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c3e4b6c2e2d378d0f78cee1824b1e4ce17a433a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957197"
---
# <a name="wm_destroyclipboard-message"></a><span data-ttu-id="1e826-105">WM \_ destroyclipboard-Nachricht</span><span class="sxs-lookup"><span data-stu-id="1e826-105">WM\_DESTROYCLIPBOARD message</span></span>

<span data-ttu-id="1e826-106">Wird an den Besitzer der Zwischenablage gesendet, wenn ein Aufrufe der [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) -Funktion die Zwischenablage leert.</span><span class="sxs-lookup"><span data-stu-id="1e826-106">Sent to the clipboard owner when a call to the [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) function empties the clipboard.</span></span>

<span data-ttu-id="1e826-107">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="1e826-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_DESTROYCLIPBOARD             0x0307
```



## <a name="parameters"></a><span data-ttu-id="1e826-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e826-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e826-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1e826-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e826-110">Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="1e826-110">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1e826-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1e826-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e826-112">Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="1e826-112">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e826-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1e826-113">Return value</span></span>

<span data-ttu-id="1e826-114">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="1e826-114">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e826-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e826-115">Requirements</span></span>



| <span data-ttu-id="1e826-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e826-116">Requirement</span></span> | <span data-ttu-id="1e826-117">Wert</span><span class="sxs-lookup"><span data-stu-id="1e826-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e826-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1e826-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1e826-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e826-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1e826-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1e826-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1e826-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e826-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1e826-122">Header</span><span class="sxs-lookup"><span data-stu-id="1e826-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e826-123"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="1e826-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e826-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e826-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="1e826-125">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="1e826-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1e826-126">**EmptyClipboard**</span><span class="sxs-lookup"><span data-stu-id="1e826-126">**EmptyClipboard**</span></span>](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard)
</dt> <dt>

<span data-ttu-id="1e826-127">**Licher**</span><span class="sxs-lookup"><span data-stu-id="1e826-127">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1e826-128">Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="1e826-128">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

