---
description: Wird einmal an ein Fenster gesendet, nachdem es die modale Verschiebungs-oder Anpassungs Schleife verlassen hat.
ms.assetid: 3466bfb5-c38d-49d8-a4ab-bf23d09c454c
title: WM_EXITSIZEMOVE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22eda44827345ef491814aab69bf0b802b924e5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347482"
---
# <a name="wm_exitsizemove-message"></a><span data-ttu-id="5ea1b-103">WM- \_ exitsizemove-Meldung</span><span class="sxs-lookup"><span data-stu-id="5ea1b-103">WM\_EXITSIZEMOVE message</span></span>

<span data-ttu-id="5ea1b-104">Wird einmal an ein Fenster gesendet, nachdem es die modale Verschiebungs-oder Anpassungs Schleife verlassen hat.</span><span class="sxs-lookup"><span data-stu-id="5ea1b-104">Sent one time to a window, after it has exited the moving or sizing modal loop.</span></span> <span data-ttu-id="5ea1b-105">Das Fenster wechselt in die modale Verschiebungs-oder Anpassungs Schleife, wenn der Benutzer auf die Titelleiste des Fensters oder den Größen Anpassungsrahmen klickt, oder wenn das Fenster die " [**WM \_ syscommand**](../menurc/wm-syscommand.md) "-Meldung an die Funktion " [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) " übergibt und der *wParam* -Parameter der Meldung den Wert **SC \_ MOV** E oder **SC \_ size** angibt.</span><span class="sxs-lookup"><span data-stu-id="5ea1b-105">The window enters the moving or sizing modal loop when the user clicks the window's title bar or sizing border, or when the window passes the [**WM\_SYSCOMMAND**](../menurc/wm-syscommand.md) message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function and the *wParam* parameter of the message specifies the **SC\_MOV** E or **SC\_SIZE** value.</span></span> <span data-ttu-id="5ea1b-106">Der Vorgang ist fertiggestellt, wenn [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5ea1b-106">The operation is complete when [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) returns.</span></span>

<span data-ttu-id="5ea1b-107">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="5ea1b-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_EXITSIZEMOVE                 0x0232
```



## <a name="parameters"></a><span data-ttu-id="5ea1b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ea1b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ea1b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5ea1b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ea1b-110">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="5ea1b-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5ea1b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5ea1b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ea1b-112">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="5ea1b-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ea1b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ea1b-113">Return value</span></span>

<span data-ttu-id="5ea1b-114">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="5ea1b-114">Type: **LRESULT**</span></span>

<span data-ttu-id="5ea1b-115">Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="5ea1b-115">An application should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ea1b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ea1b-116">Requirements</span></span>



| <span data-ttu-id="5ea1b-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ea1b-117">Requirement</span></span> | <span data-ttu-id="5ea1b-118">Wert</span><span class="sxs-lookup"><span data-stu-id="5ea1b-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea1b-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5ea1b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5ea1b-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ea1b-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5ea1b-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5ea1b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5ea1b-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ea1b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5ea1b-123">Header</span><span class="sxs-lookup"><span data-stu-id="5ea1b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ea1b-124"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="5ea1b-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ea1b-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ea1b-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="5ea1b-126">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="5ea1b-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5ea1b-127">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="5ea1b-127">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="5ea1b-128">**WM \_ Enterprise**</span><span class="sxs-lookup"><span data-stu-id="5ea1b-128">**WM\_ENTERSIZEMOVE**</span></span>](wm-entersizemove.md)
</dt> <dt>

<span data-ttu-id="5ea1b-129">**Licher**</span><span class="sxs-lookup"><span data-stu-id="5ea1b-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5ea1b-130">Windows</span><span class="sxs-lookup"><span data-stu-id="5ea1b-130">Windows</span></span>](windows.md)
</dt> </dl>

 

 
