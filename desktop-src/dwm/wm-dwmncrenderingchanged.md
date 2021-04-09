---
title: WM_DWMNCRENDERINGCHANGED Meldung (Winuser. h)
description: Wird gesendet, wenn sich die Renderingleistung des nicht-Client Bereichs geändert hat
ms.assetid: 31beb127-ebec-49a8-8b65-de00941cbd67
keywords:
- WM_DWMNCRENDERINGCHANGED Meldung Desktopfenster-Manager
topic_type:
- apiref
api_name:
- WM_DWMNCRENDERINGCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac32704ea240ccfc4d4de913b940e098ff8f4de4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956550"
---
# <a name="wm_dwmncrenderingchanged-message"></a><span data-ttu-id="57446-104">WM \_ dwmncrenderingchanged-Meldung</span><span class="sxs-lookup"><span data-stu-id="57446-104">WM\_DWMNCRENDERINGCHANGED message</span></span>

<span data-ttu-id="57446-105">Wird gesendet, wenn sich die Renderingleistung des nicht-Client Bereichs geändert hat</span><span class="sxs-lookup"><span data-stu-id="57446-105">Sent when the non-client area rendering policy has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="57446-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="57446-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57446-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="57446-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57446-108">Gibt an, ob das DWM-Rendering für den nicht-Client Bereich des Fensters aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="57446-108">Specifies whether DWM rendering is enabled for the non-client area of the window.</span></span> <span data-ttu-id="57446-109">**True** , wenn aktiviert; andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="57446-109">**TRUE** if enabled; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="57446-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="57446-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57446-111">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="57446-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57446-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="57446-112">Return value</span></span>

<span data-ttu-id="57446-113">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="57446-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="57446-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="57446-114">Remarks</span></span>

<span data-ttu-id="57446-115">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="57446-115">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

<span data-ttu-id="57446-116">Die Funktionen [**DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) und [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) werden verwendet, um die nicht-Client-renderingrichtlinie zu erhalten oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="57446-116">The [**DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) and [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) functions are used to get or set the non-client rendering policy.</span></span>

## <a name="requirements"></a><span data-ttu-id="57446-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="57446-117">Requirements</span></span>



| <span data-ttu-id="57446-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="57446-118">Requirement</span></span> | <span data-ttu-id="57446-119">Wert</span><span class="sxs-lookup"><span data-stu-id="57446-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="57446-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="57446-120">Minimum supported client</span></span><br/> | <span data-ttu-id="57446-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57446-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="57446-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="57446-122">Minimum supported server</span></span><br/> | <span data-ttu-id="57446-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57446-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="57446-124">Header</span><span class="sxs-lookup"><span data-stu-id="57446-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="57446-125"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="57446-125"><dt>Winuser.h</dt></span></span> </dl> |



 

