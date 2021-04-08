---
title: WM_SIZECLIPBOARD Meldung (Winuser. h)
description: Wird von einem Fenster der Zwischenablage Anzeige an den Besitzer der Zwischenablage gesendet, wenn die Zwischenablage Daten im CF \_ -Besitzer Anzeige Format enthält und der Client Bereich der Zwischenablage-Viewer die Größe geändert hat.
ms.assetid: 95991d03-8677-4dde-b72a-082dec4834b3
keywords:
- WM_SIZECLIPBOARD Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_SIZECLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 235de630b20757a571b1917a975d1425bee06cde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741864"
---
# <a name="wm_sizeclipboard-message"></a><span data-ttu-id="bfad2-104">WM- \_ sizeclipboard-Meldung</span><span class="sxs-lookup"><span data-stu-id="bfad2-104">WM\_SIZECLIPBOARD message</span></span>

<span data-ttu-id="bfad2-105">Wird von einem Fenster der Zwischenablage Anzeige an den Besitzer der Zwischenablage gesendet, wenn die Zwischenablage Daten im CF-Besitzer [**\_ Anzeige**](standard-clipboard-formats.md) Format enthält und der Client Bereich der Zwischenablage-Viewer die Größe geändert hat.</span><span class="sxs-lookup"><span data-stu-id="bfad2-105">Sent to the clipboard owner by a clipboard viewer window when the clipboard contains data in the [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) format and the clipboard viewer's client area has changed size.</span></span>


```C++
#define WM_SIZECLIPBOARD                0x030B
```



## <a name="parameters"></a><span data-ttu-id="bfad2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bfad2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfad2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bfad2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bfad2-108">Ein Handle für das Fenster der Zwischenablage Anzeige.</span><span class="sxs-lookup"><span data-stu-id="bfad2-108">A handle to the clipboard viewer window.</span></span>

</dd> <dt>

<span data-ttu-id="bfad2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bfad2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bfad2-110">Ein Handle für ein globales Speicher Objekt, das eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="bfad2-110">A handle to a global memory object that contains a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="bfad2-111">Die-Struktur gibt die neuen Dimensionen des Client Bereichs der Zwischenablage Anzeige an.</span><span class="sxs-lookup"><span data-stu-id="bfad2-111">The structure specifies the new dimensions of the clipboard viewer's client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfad2-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bfad2-112">Return value</span></span>

<span data-ttu-id="bfad2-113">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="bfad2-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfad2-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bfad2-114">Remarks</span></span>

<span data-ttu-id="bfad2-115">Wenn das Fenster der Zwischenablage Anzeige zerstört oder seine Größe geändert wird, wird eine **WM- \_ sizeclipboard** -Meldung mit einem NULL-Rechteck (0, 0, 0, 0) als neue Größe gesendet.</span><span class="sxs-lookup"><span data-stu-id="bfad2-115">When the clipboard viewer window is about to be destroyed or resized, a **WM\_SIZECLIPBOARD** message is sent with a null rectangle (0, 0, 0, 0) as the new size.</span></span> <span data-ttu-id="bfad2-116">Dadurch wird es dem Besitzer der Zwischenablage ermöglicht, seine Anzeige Ressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="bfad2-116">This permits the clipboard owner to free its display resources.</span></span>

<span data-ttu-id="bfad2-117">Der Besitzer der Zwischenablage muss die [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) -Funktion verwenden, um das Speicher Objekt zu sperren, das [**Rect**](/previous-versions//dd162897(v=vs.85))enthält.</span><span class="sxs-lookup"><span data-stu-id="bfad2-117">The clipboard owner must use the [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) function to lock the memory object that contains [**RECT**](/previous-versions//dd162897(v=vs.85)).</span></span> <span data-ttu-id="bfad2-118">Vor der Rückgabe muss der Besitzer der Zwischenablage das Objekt mithilfe der [**globalunlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) -Funktion entsperren.</span><span class="sxs-lookup"><span data-stu-id="bfad2-118">Before returning, the clipboard owner must unlock the object by using the [**GlobalUnlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfad2-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bfad2-119">Requirements</span></span>



| <span data-ttu-id="bfad2-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bfad2-120">Requirement</span></span> | <span data-ttu-id="bfad2-121">Wert</span><span class="sxs-lookup"><span data-stu-id="bfad2-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfad2-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bfad2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bfad2-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bfad2-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="bfad2-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bfad2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bfad2-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bfad2-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bfad2-126">Header</span><span class="sxs-lookup"><span data-stu-id="bfad2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfad2-127"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="bfad2-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfad2-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bfad2-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="bfad2-129">**Licher**</span><span class="sxs-lookup"><span data-stu-id="bfad2-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bfad2-130">Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="bfad2-130">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

