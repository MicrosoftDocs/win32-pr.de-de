---
description: Wird an ein Fenster gesendet, wenn der nicht-Client Bereich geändert werden muss, um einen aktiven oder inaktiven Zustand anzugeben.
ms.assetid: d25732b9-b9ab-4754-a4cf-002d32e3945e
title: WM_NCACTIVATE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a23cc5e0495d6679efea805eab80290b209906d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368755"
---
# <a name="wm_ncactivate-message"></a><span data-ttu-id="98475-103">WM- \_ ncaktivierungs Meldung</span><span class="sxs-lookup"><span data-stu-id="98475-103">WM\_NCACTIVATE message</span></span>

<span data-ttu-id="98475-104">Wird an ein Fenster gesendet, wenn der nicht-Client Bereich geändert werden muss, um einen aktiven oder inaktiven Zustand anzugeben.</span><span class="sxs-lookup"><span data-stu-id="98475-104">Sent to a window when its nonclient area needs to be changed to indicate an active or inactive state.</span></span>

<span data-ttu-id="98475-105">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="98475-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCACTIVATE                   0x0086
```



## <a name="parameters"></a><span data-ttu-id="98475-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="98475-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98475-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="98475-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="98475-108">Gibt an, wann eine Titelleiste oder ein Symbol geändert werden muss, um einen aktiven oder inaktiven Zustand anzugeben.</span><span class="sxs-lookup"><span data-stu-id="98475-108">Indicates when a title bar or icon needs to be changed to indicate an active or inactive state.</span></span> <span data-ttu-id="98475-109">Wenn eine aktive Titelleiste oder ein Symbol gezeichnet werden soll, ist der *wParam* -Parameter **true**.</span><span class="sxs-lookup"><span data-stu-id="98475-109">If an active title bar or icon is to be drawn, the *wParam* parameter is **TRUE**.</span></span> <span data-ttu-id="98475-110">Wenn eine inaktive Titelleiste oder ein Symbol gezeichnet werden soll, ist *wParam* auf **false** gesetzt.</span><span class="sxs-lookup"><span data-stu-id="98475-110">If an inactive title bar or icon is to be drawn, *wParam* is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="98475-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="98475-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="98475-112">Wenn ein [visueller Stil](../controls/themes-overview.md) für dieses Fenster aktiv ist, wird dieser Parameter nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="98475-112">When a [visual style](../controls/themes-overview.md) is active for this window, this parameter is not used.</span></span>

<span data-ttu-id="98475-113">Wenn ein visueller Stil für dieses Fenster nicht aktiv ist, ist dieser Parameter ein Handle für einen optionalen Update Bereich für den nicht-Client Bereich des Fensters.</span><span class="sxs-lookup"><span data-stu-id="98475-113">When a visual style is not active for this window, this parameter is a handle to an optional update region for the nonclient area of the window.</span></span> <span data-ttu-id="98475-114">Wenn dieser Parameter auf-1 festgelegt ist, zeichnet [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) den nicht-Client Bereich nicht neu, um die Statusänderung widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="98475-114">If this parameter is set to -1, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) does not repaint the nonclient area to reflect the state change.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98475-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="98475-115">Return value</span></span>

<span data-ttu-id="98475-116">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="98475-116">Type: **LRESULT**</span></span>

<span data-ttu-id="98475-117">Wenn der *wParam* -Parameter den Wert **false** hat, sollte eine Anwendung **true** zurückgeben, um anzugeben, dass das System die Standard Verarbeitung fortsetzen soll, oder es sollte **false** zurückgeben, um die Änderung zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="98475-117">When the *wParam* parameter is **FALSE**, an application should return **TRUE** to indicate that the system should proceed with the default processing, or it should return **FALSE** to prevent the change.</span></span> <span data-ttu-id="98475-118">Wenn *wParam* den Wert **true** hat, wird der Rückgabewert ignoriert.</span><span class="sxs-lookup"><span data-stu-id="98475-118">When *wParam* is **TRUE**, the return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="98475-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98475-119">Remarks</span></span>

<span data-ttu-id="98475-120">Das Verarbeiten von Nachrichten, die sich auf den nicht-Client Bereich eines Standard Fensters beziehen, wird nicht empfohlen, da die Anwendung alle erforderlichen Teile des nicht-Client Bereichs für das Fenster zeichnen muss.</span><span class="sxs-lookup"><span data-stu-id="98475-120">Processing messages related to the nonclient area of a standard window is not recommended, because the application must be able to draw all the required parts of the nonclient area for the window.</span></span> <span data-ttu-id="98475-121">Wenn eine Anwendung diese Nachricht verarbeitet, muss Sie " **true** " zurückgeben, um das System zum Abschluss der Änderung des aktiven Fensters zu leiten.</span><span class="sxs-lookup"><span data-stu-id="98475-121">If an application does process this message, it must return **TRUE** to direct the system to complete the change of active window.</span></span> <span data-ttu-id="98475-122">Wenn das Fenster beim Empfang dieser Nachricht minimiert wird, sollte die Anwendung die Nachricht an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="98475-122">If the window is minimized when this message is received, the application should pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span>

<span data-ttu-id="98475-123">Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion zeichnet die Titelleiste oder den Symbol Titel in den aktiven Farben, wenn der *wParam* -Parameter **true** ist, und in den inaktiven Farben, wenn *wParam* den Wert **false** hat.</span><span class="sxs-lookup"><span data-stu-id="98475-123">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function draws the title bar or icon title in its active colors when the *wParam* parameter is **TRUE** and in its inactive colors when *wParam* is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="98475-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98475-124">Requirements</span></span>



| <span data-ttu-id="98475-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="98475-125">Requirement</span></span> | <span data-ttu-id="98475-126">Wert</span><span class="sxs-lookup"><span data-stu-id="98475-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98475-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="98475-127">Minimum supported client</span></span><br/> | <span data-ttu-id="98475-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="98475-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="98475-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="98475-129">Minimum supported server</span></span><br/> | <span data-ttu-id="98475-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="98475-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="98475-131">Header</span><span class="sxs-lookup"><span data-stu-id="98475-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="98475-132"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="98475-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98475-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98475-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="98475-134">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="98475-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="98475-135">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="98475-135">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

<span data-ttu-id="98475-136">**Licher**</span><span class="sxs-lookup"><span data-stu-id="98475-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="98475-137">Windows</span><span class="sxs-lookup"><span data-stu-id="98475-137">Windows</span></span>](windows.md)
</dt> </dl>

 

 
