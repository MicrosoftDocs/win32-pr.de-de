---
description: Wird gesendet, wenn eine Anwendung den aktivierten Zustand eines Fensters ändert.
ms.assetid: df2cf953-121f-43bb-a06c-d10e445bfb5e
title: WM_ENABLE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82bc83b84cbbf8e0c0145ef7d2730179cab54a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348134"
---
# <a name="wm_enable-message"></a><span data-ttu-id="443ba-103">WM- \_ Aktivierungs Nachricht</span><span class="sxs-lookup"><span data-stu-id="443ba-103">WM\_ENABLE message</span></span>

<span data-ttu-id="443ba-104">Wird gesendet, wenn eine Anwendung den aktivierten Zustand eines Fensters ändert.</span><span class="sxs-lookup"><span data-stu-id="443ba-104">Sent when an application changes the enabled state of a window.</span></span> <span data-ttu-id="443ba-105">Er wird an das Fenster gesendet, dessen aktivierter Zustand geändert wird.</span><span class="sxs-lookup"><span data-stu-id="443ba-105">It is sent to the window whose enabled state is changing.</span></span> <span data-ttu-id="443ba-106">Diese Nachricht wird gesendet, bevor die [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) -Funktion zurückgegeben wird, aber nachdem der aktivierte Zustand (das [**\_ Deaktivierte WS**](window-styles.md) -Stilbit) des Fensters geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="443ba-106">This message is sent before the [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) function returns, but after the enabled state ([**WS\_DISABLED**](window-styles.md) style bit) of the window has changed.</span></span>

<span data-ttu-id="443ba-107">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="443ba-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_ENABLE                       0x000A
```



## <a name="parameters"></a><span data-ttu-id="443ba-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="443ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="443ba-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="443ba-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="443ba-110">Gibt an, ob das Fenster aktiviert oder deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="443ba-110">Indicates whether the window has been enabled or disabled.</span></span> <span data-ttu-id="443ba-111">Dieser Parameter ist **true** , wenn das Fenster aktiviert wurde, oder **false** , wenn das Fenster deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="443ba-111">This parameter is **TRUE** if the window has been enabled or **FALSE** if the window has been disabled.</span></span>

</dd> <dt>

<span data-ttu-id="443ba-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="443ba-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="443ba-113">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="443ba-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="443ba-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="443ba-114">Return value</span></span>

<span data-ttu-id="443ba-115">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="443ba-115">Type: **LRESULT**</span></span>

<span data-ttu-id="443ba-116">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="443ba-116">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="443ba-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="443ba-117">Requirements</span></span>



| <span data-ttu-id="443ba-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="443ba-118">Requirement</span></span> | <span data-ttu-id="443ba-119">Wert</span><span class="sxs-lookup"><span data-stu-id="443ba-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="443ba-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="443ba-120">Minimum supported client</span></span><br/> | <span data-ttu-id="443ba-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="443ba-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="443ba-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="443ba-122">Minimum supported server</span></span><br/> | <span data-ttu-id="443ba-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="443ba-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="443ba-124">Header</span><span class="sxs-lookup"><span data-stu-id="443ba-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="443ba-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="443ba-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="443ba-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="443ba-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="443ba-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="443ba-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="443ba-128">**EnableWindow**</span><span class="sxs-lookup"><span data-stu-id="443ba-128">**EnableWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-enablewindow)
</dt> <dt>

<span data-ttu-id="443ba-129">**Licher**</span><span class="sxs-lookup"><span data-stu-id="443ba-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="443ba-130">Windows</span><span class="sxs-lookup"><span data-stu-id="443ba-130">Windows</span></span>](windows.md)
</dt> </dl>

 

 
