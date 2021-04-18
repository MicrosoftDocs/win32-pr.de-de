---
title: WM_POINTERACTIVATE Meldung
description: Wird an ein inaktives Fenster gesendet, wenn ein primärer Zeiger eine WM_POINTERDOWN über das Fenster generiert.
ms.assetid: 4eec37da-227c-4be1-bf0b-99704caa1322
keywords:
- Eingabe Meldungen und Benachrichtigungen der WM_POINTERACTIVATE Nachricht
topic_type:
- apiref
api_name:
- WM_POINTERACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: b9bda11b5cb7a27f7744df6e20890a125a66bd88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344486"
---
# <a name="wm_pointeractivate-message"></a><span data-ttu-id="c7d3d-104">WM_POINTERACTIVATE Meldung</span><span class="sxs-lookup"><span data-stu-id="c7d3d-104">WM_POINTERACTIVATE message</span></span>

<span data-ttu-id="c7d3d-105">Wird an ein inaktives Fenster gesendet, wenn ein primärer Zeiger eine [**WM_POINTERDOWN**](wm-pointerdown.md) über das Fenster generiert.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-105">Sent to an inactive window when a primary pointer generates a [**WM_POINTERDOWN**](wm-pointerdown.md) over the window.</span></span> <span data-ttu-id="c7d3d-106">Solange die Nachricht nicht behandelt wird, wird die übergeordnete Fenster Kette nach oben verschoben, bis Sie das Fenster der obersten Ebene erreicht.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-106">As long as the message remains unhandled, it travels up the parent window chain until it is reaches the top-level window.</span></span> <span data-ttu-id="c7d3d-107">Anwendungen können auf diese Meldung reagieren, um anzugeben, ob Sie aktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-107">Applications can respond to this message to specify whether they wish to be activated.</span></span>

<span data-ttu-id="c7d3d-108">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_POINTERACTIVATE             0x024B
```



## <a name="parameters"></a><span data-ttu-id="c7d3d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7d3d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7d3d-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c7d3d-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7d3d-111">Enthält den Zeiger Bezeichner und zusätzliche Informationen.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-111">Contains the pointer identifier and additional information.</span></span> <span data-ttu-id="c7d3d-112">Verwenden Sie die folgenden Makros, um diese Informationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-112">Use the following macros to retrieve this information.</span></span>

<span data-ttu-id="c7d3d-113">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): Zeiger Bezeichner</span><span class="sxs-lookup"><span data-stu-id="c7d3d-113">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): pointer identifier</span></span>

<span data-ttu-id="c7d3d-114">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): Treffer Test Wert, der von der Verarbeitung der [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) Nachricht zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-114">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): hit-test value returned from processing the [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="c7d3d-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c7d3d-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7d3d-116">Enthält das Handle für das Fenster auf oberster Ebene des Fensters, das aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-116">Contains the handle to the top-level window of the window being activated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7d3d-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c7d3d-117">Return value</span></span>

<span data-ttu-id="c7d3d-118">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie einen der im Abschnitt "Hinweise" beschriebenen Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-118">If an application processes this message, it should return one of the values described in the Remarks section.</span></span>

<span data-ttu-id="c7d3d-119">Wenn die Anwendung diese Nachricht nicht verarbeitet, sollte Sie [**defwindowproc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-119">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="c7d3d-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7d3d-120">Remarks</span></span>

<span data-ttu-id="c7d3d-121">Eine Anwendung kann diese Nachricht verarbeiten und einen der folgenden Werte zurückgeben, um zu bestimmen, wie das System die Aktivierung und die Aktivierungs Eingabe verarbeitet:</span><span class="sxs-lookup"><span data-stu-id="c7d3d-121">An application can handle this message and return one of the following values to determine how the system processes the activation and the activating input:</span></span>

-   <span data-ttu-id="c7d3d-122">PA_ACTIVATE</span><span class="sxs-lookup"><span data-stu-id="c7d3d-122">PA_ACTIVATE</span></span>
-   <span data-ttu-id="c7d3d-123">PA_NOACTIVATE</span><span class="sxs-lookup"><span data-stu-id="c7d3d-123">PA_NOACTIVATE</span></span>

<span data-ttu-id="c7d3d-124">Beachten Sie Folgendes: Wenn der Benutzer mit dem System mit mehreren gleichzeitigen Zeigern interagiert, ist die Aktivierungs Chance, die die **WM_POINTERACTIVATE** Nachricht darstellt, für Anwendungen nur für die ersten dieser Zeiger verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-124">It is important to note that, when the user is interacting with the system with multiple simultaneous pointers, the activation opportunity that the **WM_POINTERACTIVATE** message represents is available to applications only for the first of those pointers.</span></span> <span data-ttu-id="c7d3d-125">Anwendungen sollten daher beachten, dass Sie möglicherweise weiterhin Eingaben von Zeigern empfangen, wenn Sie inaktiv sind.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-125">Applications should, therefore, be aware that they may still receive input from pointers while they are inactive.</span></span>

<span data-ttu-id="c7d3d-126">Wenn die Anwendung diese Nachricht nicht verarbeitet, übergibt [**defwindowproc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) die Nachricht an das übergeordnete Fenster.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-126">If the application does not handle this message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) passes the message to the parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7d3d-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7d3d-127">Requirements</span></span>



| <span data-ttu-id="c7d3d-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7d3d-128">Requirement</span></span> | <span data-ttu-id="c7d3d-129">Wert</span><span class="sxs-lookup"><span data-stu-id="c7d3d-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7d3d-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c7d3d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c7d3d-131">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7d3d-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="c7d3d-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c7d3d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c7d3d-133">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7d3d-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c7d3d-134">Header</span><span class="sxs-lookup"><span data-stu-id="c7d3d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7d3d-135"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="c7d3d-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7d3d-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7d3d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7d3d-137">Meldungen</span><span class="sxs-lookup"><span data-stu-id="c7d3d-137">Messages</span></span>](messages.md)
</dt> </dl>

 

