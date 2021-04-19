---
description: Wird vor der WM Create-Meldung gesendet, \_ Wenn ein Fenster erstmalig erstellt wird.
ms.assetid: 5dd0eda3-83a6-4077-a7a3-e371c9413b0f
title: WM_NCCREATE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8757cbdeba49d54f6e5d842a5b40c7f7ae61cac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362240"
---
# <a name="wm_nccreate-message"></a><span data-ttu-id="5ddc3-103">WM- \_ nccreate-Meldung</span><span class="sxs-lookup"><span data-stu-id="5ddc3-103">WM\_NCCREATE message</span></span>

<span data-ttu-id="5ddc3-104">Wird vor der [**WM \_ Create**](wm-create.md) -Meldung gesendet, wenn ein Fenster erstmalig erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-104">Sent prior to the [**WM\_CREATE**](wm-create.md) message when a window is first created.</span></span>

<span data-ttu-id="5ddc3-105">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCCREATE                     0x0081
```



## <a name="parameters"></a><span data-ttu-id="5ddc3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ddc3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ddc3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5ddc3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ddc3-108">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5ddc3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5ddc3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ddc3-110">Ein Zeiger auf die [**foratestruct**](/windows/win32/api/winuser/ns-winuser-createstructa) -Struktur, die Informationen über das Fenster enthält, das erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-110">A pointer to the [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure that contains information about the window being created.</span></span> <span data-ttu-id="5ddc3-111">Die Member von " **kreatestruct** " sind identisch mit den Parametern der Funktion " [**foratewindowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) ".</span><span class="sxs-lookup"><span data-stu-id="5ddc3-111">The members of **CREATESTRUCT** are identical to the parameters of the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ddc3-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ddc3-112">Return value</span></span>

<span data-ttu-id="5ddc3-113">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="5ddc3-113">Type: **LRESULT**</span></span>

<span data-ttu-id="5ddc3-114">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie " **true** " zurückgeben, um die Erstellung des Fensters fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-114">If an application processes this message, it should return **TRUE** to continue creation of the window.</span></span> <span data-ttu-id="5ddc3-115">Wenn die Anwendung **false** zurückgibt, gibt die Funktion " [**kreatewindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) " oder " [**kreatewindowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) " ein **null** -Handle zurück.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-115">If the application returns **FALSE**, the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function will return a **NULL** handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ddc3-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ddc3-116">Requirements</span></span>



| <span data-ttu-id="5ddc3-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ddc3-117">Requirement</span></span> | <span data-ttu-id="5ddc3-118">Wert</span><span class="sxs-lookup"><span data-stu-id="5ddc3-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ddc3-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5ddc3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5ddc3-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ddc3-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5ddc3-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5ddc3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5ddc3-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ddc3-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5ddc3-123">Header</span><span class="sxs-lookup"><span data-stu-id="5ddc3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ddc3-124"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="5ddc3-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ddc3-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ddc3-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="5ddc3-126">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="5ddc3-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5ddc3-127">**CreateWindow**</span><span class="sxs-lookup"><span data-stu-id="5ddc3-127">**CreateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[<span data-ttu-id="5ddc3-128">**CreateWindowEx**</span><span class="sxs-lookup"><span data-stu-id="5ddc3-128">**CreateWindowEx**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[<span data-ttu-id="5ddc3-129">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="5ddc3-129">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="5ddc3-130">**CREATESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="5ddc3-130">**CREATESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[<span data-ttu-id="5ddc3-131">**WM \_ Erstellen**</span><span class="sxs-lookup"><span data-stu-id="5ddc3-131">**WM\_CREATE**</span></span>](wm-create.md)
</dt> <dt>

<span data-ttu-id="5ddc3-132">**Licher**</span><span class="sxs-lookup"><span data-stu-id="5ddc3-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5ddc3-133">Windows</span><span class="sxs-lookup"><span data-stu-id="5ddc3-133">Windows</span></span>](windows.md)
</dt> </dl>

 

 
