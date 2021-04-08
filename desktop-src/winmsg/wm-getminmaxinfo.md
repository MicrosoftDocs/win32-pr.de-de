---
description: Wird an ein Fenster gesendet, wenn die Größe oder Position des Fensters geändert wird. Eine Anwendung kann diese Nachricht verwenden, um die standardmäßige maximierte Größe und Position des Fensters zu überschreiben, bzw. die standardmäßige oder maximale nach Verfolgungs Größe.
ms.assetid: af2295e0-2d0b-4ac0-b689-16138022f4b7
title: WM_GETMINMAXINFO Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29cbca97d38f7fca90c93ef7bf0606ea49306da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866759"
---
# <a name="wm_getminmaxinfo-message"></a><span data-ttu-id="d0a25-104">WM \_ getminmaxinfo-Meldung</span><span class="sxs-lookup"><span data-stu-id="d0a25-104">WM\_GETMINMAXINFO message</span></span>

<span data-ttu-id="d0a25-105">Wird an ein Fenster gesendet, wenn die Größe oder Position des Fensters geändert wird.</span><span class="sxs-lookup"><span data-stu-id="d0a25-105">Sent to a window when the size or position of the window is about to change.</span></span> <span data-ttu-id="d0a25-106">Eine Anwendung kann diese Nachricht verwenden, um die standardmäßige maximierte Größe und Position des Fensters zu überschreiben, bzw. die standardmäßige oder maximale nach Verfolgungs Größe.</span><span class="sxs-lookup"><span data-stu-id="d0a25-106">An application can use this message to override the window's default maximized size and position, or its default minimum or maximum tracking size.</span></span>

<span data-ttu-id="d0a25-107">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="d0a25-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_GETMINMAXINFO                0x0024
```



## <a name="parameters"></a><span data-ttu-id="d0a25-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0a25-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0a25-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d0a25-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0a25-110">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d0a25-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d0a25-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d0a25-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0a25-112">Ein Zeiger auf eine [**minmaxinfo**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) -Struktur, die die standardmäßige maximierte Position und die Standardabmessungen sowie die Standard-und maximale nach Verfolgungs Größe enthält.</span><span class="sxs-lookup"><span data-stu-id="d0a25-112">A pointer to a [**MINMAXINFO**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) structure that contains the default maximized position and dimensions, and the default minimum and maximum tracking sizes.</span></span> <span data-ttu-id="d0a25-113">Eine Anwendung kann die Standardwerte überschreiben, indem die Elemente dieser Struktur festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d0a25-113">An application can override the defaults by setting the members of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0a25-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d0a25-114">Return value</span></span>

<span data-ttu-id="d0a25-115">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="d0a25-115">Type: **LRESULT**</span></span>

<span data-ttu-id="d0a25-116">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d0a25-116">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0a25-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d0a25-117">Remarks</span></span>

<span data-ttu-id="d0a25-118">Die maximale nach Verfolgungs Größe ist die größte Fenstergröße, die erstellt werden kann, indem die Rahmen verwendet werden, um das Fenster zu verkleinern.</span><span class="sxs-lookup"><span data-stu-id="d0a25-118">The maximum tracking size is the largest window size that can be produced by using the borders to size the window.</span></span> <span data-ttu-id="d0a25-119">Die Mindestgröße für die Nachverfolgung ist die kleinste Fenstergröße, die mithilfe der Rahmengröße des Fensters erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="d0a25-119">The minimum tracking size is the smallest window size that can be produced by using the borders to size the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0a25-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d0a25-120">Requirements</span></span>



| <span data-ttu-id="d0a25-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d0a25-121">Requirement</span></span> | <span data-ttu-id="d0a25-122">Wert</span><span class="sxs-lookup"><span data-stu-id="d0a25-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0a25-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d0a25-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d0a25-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d0a25-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d0a25-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d0a25-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d0a25-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d0a25-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d0a25-127">Header</span><span class="sxs-lookup"><span data-stu-id="d0a25-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0a25-128"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="d0a25-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0a25-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0a25-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="d0a25-130">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="d0a25-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d0a25-131">**Fenster**</span><span class="sxs-lookup"><span data-stu-id="d0a25-131">**MoveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[<span data-ttu-id="d0a25-132">**SetWindowPos**</span><span class="sxs-lookup"><span data-stu-id="d0a25-132">**SetWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[<span data-ttu-id="d0a25-133">**MINMAXINFO**</span><span class="sxs-lookup"><span data-stu-id="d0a25-133">**MINMAXINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-minmaxinfo)
</dt> <dt>

<span data-ttu-id="d0a25-134">**Licher**</span><span class="sxs-lookup"><span data-stu-id="d0a25-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d0a25-135">Windows</span><span class="sxs-lookup"><span data-stu-id="d0a25-135">Windows</span></span>](windows.md)
</dt> </dl>

 

 
