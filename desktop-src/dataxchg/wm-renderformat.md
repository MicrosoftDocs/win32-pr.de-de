---
title: WM_RENDERFORMAT Meldung (Winuser. h)
description: Wird an den Besitzer der Zwischenablage gesendet, wenn er das Rendern eines bestimmten Zwischenablage Formats verzögert hat und eine Anwendung Daten in diesem Format angefordert hat.
ms.assetid: 81638109-4c5e-4b4c-b2db-4208b6ee83cc
keywords:
- WM_RENDERFORMAT Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_RENDERFORMAT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9d0e8539dc666c7a791a24c9ba7ac772c3c2c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340708"
---
# <a name="wm_renderformat-message"></a><span data-ttu-id="c6429-104">WM- \_ Renderformat-Meldung</span><span class="sxs-lookup"><span data-stu-id="c6429-104">WM\_RENDERFORMAT message</span></span>

<span data-ttu-id="c6429-105">Wird an den Besitzer der Zwischenablage gesendet, wenn er das Rendern eines bestimmten Zwischenablage Formats verzögert hat und eine Anwendung Daten in diesem Format angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="c6429-105">Sent to the clipboard owner if it has delayed rendering a specific clipboard format and if an application has requested data in that format.</span></span> <span data-ttu-id="c6429-106">Der Besitzer der Zwischenablage muss die Daten im angegebenen Format Renderingdaten in der Zwischenablage platzieren, indem er die [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) -Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="c6429-106">The clipboard owner must render data in the specified format and place it on the clipboard by calling the [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) function.</span></span>


```C++
#define WM_RENDERFORMAT                 0x0305
```



## <a name="parameters"></a><span data-ttu-id="c6429-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6429-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6429-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c6429-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6429-109">Das zu rendernde [Zwischenablage Format](standard-clipboard-formats.md) .</span><span class="sxs-lookup"><span data-stu-id="c6429-109">The [clipboard format](standard-clipboard-formats.md) to be rendered.</span></span>

</dd> <dt>

<span data-ttu-id="c6429-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c6429-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6429-111">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c6429-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6429-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c6429-112">Return value</span></span>

<span data-ttu-id="c6429-113">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c6429-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6429-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6429-114">Remarks</span></span>

<span data-ttu-id="c6429-115">Bei der Reaktion auf eine **WM- \_ Renderformat** -Nachricht darf der Besitzer der Zwischenablage die Zwischenablage vor dem Aufrufen von [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)nicht öffnen.</span><span class="sxs-lookup"><span data-stu-id="c6429-115">When responding to a **WM\_RENDERFORMAT** message, the clipboard owner must not open the clipboard before calling [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata).</span></span> <span data-ttu-id="c6429-116">Das Öffnen der Zwischenablage ist nicht erforderlich, bevor Daten als Antwort auf **WM \_ Renderformat** platziert werden, und jeder Versuch, die Zwischenablage zu öffnen, schlägt fehl, da die Zwischenablage derzeit von der Anwendung geöffnet wird, die das zu rendernde Format angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="c6429-116">Opening the clipboard is not necessary before placing data in response to **WM\_RENDERFORMAT**, and any attempt to open the clipboard will fail because the clipboard is currently being held open by the application that requested the format to be rendered.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6429-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6429-117">Requirements</span></span>



| <span data-ttu-id="c6429-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6429-118">Requirement</span></span> | <span data-ttu-id="c6429-119">Wert</span><span class="sxs-lookup"><span data-stu-id="c6429-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6429-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c6429-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c6429-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6429-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c6429-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c6429-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c6429-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6429-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c6429-124">Header</span><span class="sxs-lookup"><span data-stu-id="c6429-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6429-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="c6429-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6429-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6429-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="c6429-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="c6429-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c6429-128">**SetClipboardData**</span><span class="sxs-lookup"><span data-stu-id="c6429-128">**SetClipboardData**</span></span>](/windows/win32/api/winuser/nf-winuser-setclipboarddata)
</dt> <dt>

[<span data-ttu-id="c6429-129">**WM- \_ renderallformats**</span><span class="sxs-lookup"><span data-stu-id="c6429-129">**WM\_RENDERALLFORMATS**</span></span>](wm-renderallformats.md)
</dt> <dt>

<span data-ttu-id="c6429-130">**Licher**</span><span class="sxs-lookup"><span data-stu-id="c6429-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c6429-131">Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="c6429-131">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

 





