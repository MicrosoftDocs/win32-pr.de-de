---
description: Wird einmal an ein Fenster gesendet, nachdem es in die modale Verschiebungs-oder Anpassungs Schleife gelangt ist.
ms.assetid: fe09db71-2c79-47f2-b575-516e960915d4
title: WM_ENTERSIZEMOVE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfaf27c888311991b88278a9d4e69482efd06111
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368876"
---
# <a name="wm_entersizemove-message"></a><span data-ttu-id="5b5b0-103">WM- \_ entersizemove-Meldung</span><span class="sxs-lookup"><span data-stu-id="5b5b0-103">WM\_ENTERSIZEMOVE message</span></span>

<span data-ttu-id="5b5b0-104">Wird einmal an ein Fenster gesendet, nachdem es in die modale Verschiebungs-oder Anpassungs Schleife gelangt ist.</span><span class="sxs-lookup"><span data-stu-id="5b5b0-104">Sent one time to a window after it enters the moving or sizing modal loop.</span></span> <span data-ttu-id="5b5b0-105">Das Fenster wechselt in die modale Verschiebungs-oder Anpassungs Schleife, wenn der Benutzer auf die Titelleiste des Fensters oder den Größen Anpassungsrahmen klickt, oder wenn das Fenster die " [**WM \_ syscommand**](../menurc/wm-syscommand.md) "-Meldung an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion übergibt und der *wParam* -Parameter der Nachricht den Wert **SC \_ Move** oder **SC \_ size** angibt.</span><span class="sxs-lookup"><span data-stu-id="5b5b0-105">The window enters the moving or sizing modal loop when the user clicks the window's title bar or sizing border, or when the window passes the [**WM\_SYSCOMMAND**](../menurc/wm-syscommand.md) message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function and the *wParam* parameter of the message specifies the **SC\_MOVE** or **SC\_SIZE** value.</span></span> <span data-ttu-id="5b5b0-106">Der Vorgang ist fertiggestellt, wenn [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5b5b0-106">The operation is complete when [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) returns.</span></span>

<span data-ttu-id="5b5b0-107">Das System sendet die WM-Nachricht " **\_ entersizemove** " unabhängig davon, ob das Ziehen von vollständigen Fenstern aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="5b5b0-107">The system sends the **WM\_ENTERSIZEMOVE** message regardless of whether the dragging of full windows is enabled.</span></span>

<span data-ttu-id="5b5b0-108">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="5b5b0-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_ENTERSIZEMOVE                0x0231
```



## <a name="parameters"></a><span data-ttu-id="5b5b0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b5b0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b5b0-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5b5b0-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b5b0-111">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="5b5b0-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5b5b0-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5b5b0-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b5b0-113">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="5b5b0-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b5b0-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5b5b0-114">Return value</span></span>

<span data-ttu-id="5b5b0-115">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="5b5b0-115">Type: **LRESULT**</span></span>

<span data-ttu-id="5b5b0-116">Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="5b5b0-116">An application should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b5b0-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5b5b0-117">Requirements</span></span>



| <span data-ttu-id="5b5b0-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5b5b0-118">Requirement</span></span> | <span data-ttu-id="5b5b0-119">Wert</span><span class="sxs-lookup"><span data-stu-id="5b5b0-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b5b0-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5b5b0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5b5b0-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5b5b0-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5b5b0-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5b5b0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5b5b0-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5b5b0-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5b5b0-124">Header</span><span class="sxs-lookup"><span data-stu-id="5b5b0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b5b0-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="5b5b0-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b5b0-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b5b0-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="5b5b0-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="5b5b0-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5b5b0-128">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="5b5b0-128">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="5b5b0-129">**WM- \_ exitsizemove**</span><span class="sxs-lookup"><span data-stu-id="5b5b0-129">**WM\_EXITSIZEMOVE**</span></span>](wm-exitsizemove.md)
</dt> <dt>

[<span data-ttu-id="5b5b0-130">**WM ( \_ syscommand)**</span><span class="sxs-lookup"><span data-stu-id="5b5b0-130">**WM\_SYSCOMMAND**</span></span>](../menurc/wm-syscommand.md)
</dt> <dt>

<span data-ttu-id="5b5b0-131">**Licher**</span><span class="sxs-lookup"><span data-stu-id="5b5b0-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5b5b0-132">Windows</span><span class="sxs-lookup"><span data-stu-id="5b5b0-132">Windows</span></span>](windows.md)
</dt> </dl>

 

 
