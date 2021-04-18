---
description: Wird an alle Fenster der obersten Ebene gesendet, wenn das System mehr als 12,5 Prozent der Systemzeit über ein Intervall von 30 bis 60 Sekunden erkennt. Dies weist darauf hin, dass der Systemspeicher gering ist.
ms.assetid: e8adc655-0252-4a43-8a62-b08e96f5744e
title: WM_COMPACTING Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fb94e77a1c6b27701b26ed4b7e6e01f326aaa40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357906"
---
# <a name="wm_compacting-message"></a><span data-ttu-id="dc9d7-104">Mit der WM \_ komprimierende Nachricht</span><span class="sxs-lookup"><span data-stu-id="dc9d7-104">WM\_COMPACTING message</span></span>

<span data-ttu-id="dc9d7-105">Wird an alle Fenster der obersten Ebene gesendet, wenn das System mehr als 12,5 Prozent der Systemzeit über ein Intervall von 30 bis 60 Sekunden erkennt.</span><span class="sxs-lookup"><span data-stu-id="dc9d7-105">Sent to all top-level windows when the system detects more than 12.5 percent of system time over a 30- to 60-second interval is being spent compacting memory.</span></span> <span data-ttu-id="dc9d7-106">Dies weist darauf hin, dass der Systemspeicher gering ist.</span><span class="sxs-lookup"><span data-stu-id="dc9d7-106">This indicates that system memory is low.</span></span>

<span data-ttu-id="dc9d7-107">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="dc9d7-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> [!Note]  
> <span data-ttu-id="dc9d7-108">Diese Meldung wird nur für die Kompatibilität mit 16-Bit-Windows-basierten Anwendungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="dc9d7-108">This message is provided only for compatibility with 16-bit Windows-based applications.</span></span>

 


```C++
#define WM_COMPACTING                   0x0041
```



## <a name="parameters"></a><span data-ttu-id="dc9d7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc9d7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc9d7-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dc9d7-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc9d7-111">Das Verhältnis der CPU-Zeit (Central Processing Unit), die zurzeit vom System für das System zur CPU-Zeit aufgewendet wird, das zurzeit vom System für andere Vorgänge aufgewendet wird.</span><span class="sxs-lookup"><span data-stu-id="dc9d7-111">The ratio of central processing unit (CPU) time currently spent by the system compacting memory to CPU time currently spent by the system performing other operations.</span></span> <span data-ttu-id="dc9d7-112">Beispielsweise steht 0X8000 für 50 Prozent der CPU-Zeit, die für den Komprimierungs Speicher aufgewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="dc9d7-112">For example, 0x8000 represents 50 percent of CPU time spent compacting memory.</span></span>

</dd> <dt>

<span data-ttu-id="dc9d7-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dc9d7-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc9d7-114">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="dc9d7-114">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc9d7-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dc9d7-115">Return value</span></span>

<span data-ttu-id="dc9d7-116">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="dc9d7-116">Type: **LRESULT**</span></span>

<span data-ttu-id="dc9d7-117">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="dc9d7-117">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc9d7-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dc9d7-118">Remarks</span></span>

<span data-ttu-id="dc9d7-119">Wenn eine Anwendung diese Nachricht empfängt, sollte so viel Arbeitsspeicher wie möglich freigegeben werden. dabei wird die aktuelle Aktivität der Anwendung und die Gesamtzahl der Anwendungen berücksichtigt, die auf dem System ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="dc9d7-119">When an application receives this message, it should free as much memory as possible, taking into account the current level of activity of the application and the total number of applications running on the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc9d7-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc9d7-120">Requirements</span></span>



| <span data-ttu-id="dc9d7-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc9d7-121">Requirement</span></span> | <span data-ttu-id="dc9d7-122">Wert</span><span class="sxs-lookup"><span data-stu-id="dc9d7-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc9d7-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dc9d7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="dc9d7-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dc9d7-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="dc9d7-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dc9d7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="dc9d7-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dc9d7-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dc9d7-127">Header</span><span class="sxs-lookup"><span data-stu-id="dc9d7-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc9d7-128"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="dc9d7-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc9d7-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc9d7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc9d7-130">Übersicht über Windows</span><span class="sxs-lookup"><span data-stu-id="dc9d7-130">Windows Overview</span></span>](windows.md)
</dt> </dl>

 

 
