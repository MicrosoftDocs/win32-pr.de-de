---
title: DM_POINTERHITTEST Meldung
description: Wird an ein Fenster gesendet, wenn eine Zeiger Eingabe zuerst erkannt wird, um das wahrscheinlichste Eingabe Ziel für die direkte Bearbeitung zu ermitteln.
ms.assetid: E4CE60F0-0C2A-440A-8F64-B070867A1572
keywords:
- Eingabe Meldungen und Benachrichtigungen der DM_POINTERHITTEST Nachricht
topic_type:
- apiref
api_name:
- DM_POINTERHITTEST
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 23efab4606f758acfffdd02fa4c53a729f1f4a99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104864"
---
# <a name="dm_pointerhittest-message"></a><span data-ttu-id="fa68c-104">DM_POINTERHITTEST Meldung</span><span class="sxs-lookup"><span data-stu-id="fa68c-104">DM_POINTERHITTEST message</span></span>

<span data-ttu-id="fa68c-105">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="fa68c-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fa68c-106">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="fa68c-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fa68c-107">Wird an ein Fenster gesendet, wenn eine Zeiger Eingabe zuerst erkannt wird, um das wahrscheinlichste Eingabe Ziel für die [direkte Bearbeitung](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal)zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="fa68c-107">Sent to a window, when pointer input is first detected, in order to determine the most probable input target for [Direct Manipulation](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal).</span></span>

> <span data-ttu-id="fa68c-108">\[! Wichtig\]</span><span class="sxs-lookup"><span data-stu-id="fa68c-108">\[!Important\]</span></span>  
> <span data-ttu-id="fa68c-109">Desktop-Apps sollten dpi-fähig sein.</span><span class="sxs-lookup"><span data-stu-id="fa68c-109">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="fa68c-110">Wenn Ihre APP nicht dpi-fähig ist, können Bildschirm Koordinaten, die in Zeiger Nachrichten und zugehörigen Strukturen enthalten sind, aufgrund der dpi-Virtualisierung ungenau erscheinen.</span><span class="sxs-lookup"><span data-stu-id="fa68c-110">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="fa68c-111">Die dpi-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht mit dpi-Werten kompatibel sind und standardmäßig aktiv sind (Benutzer können Sie deaktivieren).</span><span class="sxs-lookup"><span data-stu-id="fa68c-111">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="fa68c-112">Weitere Informationen finden Sie unter [Schreiben von High-dpi-Win32-Anwendungen](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fa68c-112">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define DM_POINTERHITTEST       0x0250
```



## <a name="parameters"></a><span data-ttu-id="fa68c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa68c-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa68c-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fa68c-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa68c-115">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="fa68c-115">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="fa68c-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fa68c-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa68c-117">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="fa68c-117">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa68c-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fa68c-118">Return value</span></span>

<span data-ttu-id="fa68c-119">NULL</span><span class="sxs-lookup"><span data-stu-id="fa68c-119">NULL</span></span>

## <a name="requirements"></a><span data-ttu-id="fa68c-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa68c-120">Requirements</span></span>



| <span data-ttu-id="fa68c-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fa68c-121">Requirement</span></span> | <span data-ttu-id="fa68c-122">Wert</span><span class="sxs-lookup"><span data-stu-id="fa68c-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa68c-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fa68c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="fa68c-124">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fa68c-124">Windows 10 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fa68c-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fa68c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="fa68c-126">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fa68c-126">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fa68c-127">Header</span><span class="sxs-lookup"><span data-stu-id="fa68c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa68c-128"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="fa68c-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa68c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa68c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa68c-130">Meldungen</span><span class="sxs-lookup"><span data-stu-id="fa68c-130">Messages</span></span>](messages.md)
</dt> </dl>

 

