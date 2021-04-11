---
description: Wird an ein Symbol gesendet, wenn der Benutzer anfordert, dass das Fenster bis zur vorherigen Größe und Position wieder hergestellt wird.
ms.assetid: 6e14d5fd-6598-4d2e-a463-2b153c9c2aa3
title: WM_QUERYOPEN Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 582fcfce280c0bf98fdf92234b7fab8aaa103a91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042279"
---
# <a name="wm_queryopen-message"></a><span data-ttu-id="179fa-103">WM- \_ Meldung "queryopen"</span><span class="sxs-lookup"><span data-stu-id="179fa-103">WM\_QUERYOPEN message</span></span>

<span data-ttu-id="179fa-104">Wird an ein Symbol gesendet, wenn der Benutzer anfordert, dass das Fenster bis zur vorherigen Größe und Position wieder hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="179fa-104">Sent to an icon when the user requests that the window be restored to its previous size and position.</span></span>

<span data-ttu-id="179fa-105">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="179fa-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_QUERYOPEN                    0x0013
```



## <a name="parameters"></a><span data-ttu-id="179fa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="179fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="179fa-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="179fa-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="179fa-108">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="179fa-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="179fa-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="179fa-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="179fa-110">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="179fa-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="179fa-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="179fa-111">Return value</span></span>

<span data-ttu-id="179fa-112">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="179fa-112">Type: **LRESULT**</span></span>

<span data-ttu-id="179fa-113">Wenn das Symbol geöffnet werden kann, sollte eine Anwendung, die diese Nachricht verarbeitet, **true** zurückgeben. Andernfalls sollte **false** zurückgegeben werden, um zu verhindern, dass das Symbol geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="179fa-113">If the icon can be opened, an application that processes this message should return **TRUE**; otherwise, it should return **FALSE** to prevent the icon from being opened.</span></span>

## <a name="remarks"></a><span data-ttu-id="179fa-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="179fa-114">Remarks</span></span>

<span data-ttu-id="179fa-115">Standardmäßig gibt die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="179fa-115">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns **TRUE**.</span></span>

<span data-ttu-id="179fa-116">Bei der Verarbeitung dieser Nachricht sollte die Anwendung keine Aktionen ausführen, die eine Aktivierung oder eine Fokus Änderung verursachen (z. b. das Erstellen eines Dialog Felds).</span><span class="sxs-lookup"><span data-stu-id="179fa-116">While processing this message, the application should not perform any action that would cause an activation or focus change (for example, creating a dialog box).</span></span>

## <a name="requirements"></a><span data-ttu-id="179fa-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="179fa-117">Requirements</span></span>



| <span data-ttu-id="179fa-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="179fa-118">Requirement</span></span> | <span data-ttu-id="179fa-119">Wert</span><span class="sxs-lookup"><span data-stu-id="179fa-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="179fa-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="179fa-120">Minimum supported client</span></span><br/> | <span data-ttu-id="179fa-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="179fa-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="179fa-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="179fa-122">Minimum supported server</span></span><br/> | <span data-ttu-id="179fa-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="179fa-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="179fa-124">Header</span><span class="sxs-lookup"><span data-stu-id="179fa-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="179fa-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="179fa-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="179fa-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="179fa-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="179fa-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="179fa-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="179fa-128">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="179fa-128">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

<span data-ttu-id="179fa-129">**Licher**</span><span class="sxs-lookup"><span data-stu-id="179fa-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="179fa-130">Windows</span><span class="sxs-lookup"><span data-stu-id="179fa-130">Windows</span></span>](windows.md)
</dt> </dl>

 

 
