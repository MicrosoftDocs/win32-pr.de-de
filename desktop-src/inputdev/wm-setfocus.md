---
title: WM_SETFOCUS Meldung (Winuser. h)
description: Wird an ein Fenster gesendet, nachdem es den Tastaturfokus erhalten hat.
ms.assetid: 77180e4c-95a6-41a4-93d9-033381ae7543
keywords:
- Tastatur-und Maus Eingaben für WM_SETFOCUS Nachricht
topic_type:
- apiref
api_name:
- WM_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b304d7f7739ce551c1efc6a1d33a934c48dc8b4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478759"
---
# <a name="wm_setfocus-message"></a><span data-ttu-id="c54e8-104">WM- \_ SetFocus-Nachricht</span><span class="sxs-lookup"><span data-stu-id="c54e8-104">WM\_SETFOCUS message</span></span>

<span data-ttu-id="c54e8-105">Wird an ein Fenster gesendet, nachdem es den Tastaturfokus erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="c54e8-105">Sent to a window after it has gained the keyboard focus.</span></span>


```C++
#define WM_SETFOCUS                     0x0007
```



## <a name="parameters"></a><span data-ttu-id="c54e8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c54e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c54e8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c54e8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c54e8-108">Ein Handle für das Fenster, das den Tastaturfokus verloren hat.</span><span class="sxs-lookup"><span data-stu-id="c54e8-108">A handle to the window that has lost the keyboard focus.</span></span> <span data-ttu-id="c54e8-109">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="c54e8-109">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c54e8-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c54e8-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c54e8-111">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c54e8-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c54e8-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c54e8-112">Return value</span></span>

<span data-ttu-id="c54e8-113">Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="c54e8-113">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="c54e8-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c54e8-114">Remarks</span></span>

<span data-ttu-id="c54e8-115">Zum Anzeigen einer Einfügemarke sollte eine Anwendung die entsprechenden Caretzeichen aufrufen, wenn Sie die **WM \_ SetFocus** -Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="c54e8-115">To display a caret, an application should call the appropriate caret functions when it receives the **WM\_SETFOCUS** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c54e8-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c54e8-116">Requirements</span></span>



| <span data-ttu-id="c54e8-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c54e8-117">Requirement</span></span> | <span data-ttu-id="c54e8-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c54e8-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c54e8-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c54e8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c54e8-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c54e8-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c54e8-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c54e8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c54e8-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c54e8-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c54e8-123">Header</span><span class="sxs-lookup"><span data-stu-id="c54e8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c54e8-124"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="c54e8-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c54e8-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c54e8-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="c54e8-126">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="c54e8-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c54e8-127">**SetFocus**</span><span class="sxs-lookup"><span data-stu-id="c54e8-127">**SetFocus**</span></span>](/windows/win32/api/winuser/nf-winuser-setfocus)
</dt> <dt>

[<span data-ttu-id="c54e8-128">**WM- \_ killfokus**</span><span class="sxs-lookup"><span data-stu-id="c54e8-128">**WM\_KILLFOCUS**</span></span>](wm-killfocus.md)
</dt> <dt>

<span data-ttu-id="c54e8-129">**Licher**</span><span class="sxs-lookup"><span data-stu-id="c54e8-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c54e8-130">Tastatureingabe</span><span class="sxs-lookup"><span data-stu-id="c54e8-130">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

