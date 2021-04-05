---
description: Übertragung an jedes Fenster nach einem Design Änderungs Ereignis. Beispiele für Design Änderungs Ereignisse sind die Aktivierung eines Designs, die Deaktivierung eines Designs oder ein Übergang von einem Design zu einem anderen.
ms.assetid: 1a4051ac-cc6e-4520-ab66-d0a41a8a4c73
title: WM_THEMECHANGED Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bc15ab64126ff8972b858ef43ddd4d92cd62f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751200"
---
# <a name="wm_themechanged-message"></a><span data-ttu-id="2af93-104">WM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="2af93-104">WM\_THEMECHANGED message</span></span>

<span data-ttu-id="2af93-105">Übertragung an jedes Fenster nach einem Design Änderungs Ereignis.</span><span class="sxs-lookup"><span data-stu-id="2af93-105">Broadcast to every window following a theme change event.</span></span> <span data-ttu-id="2af93-106">Beispiele für Design Änderungs Ereignisse sind die Aktivierung eines Designs, die Deaktivierung eines Designs oder ein Übergang von einem Design zu einem anderen.</span><span class="sxs-lookup"><span data-stu-id="2af93-106">Examples of theme change events are the activation of a theme, the deactivation of a theme, or a transition from one theme to another.</span></span>


```C++
#define WM_THEMECHANGED                 0x031A
```



## <a name="parameters"></a><span data-ttu-id="2af93-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2af93-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2af93-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2af93-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2af93-109">Dieser Parameter ist reserviert.</span><span class="sxs-lookup"><span data-stu-id="2af93-109">This parameter is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="2af93-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2af93-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2af93-111">Dieser Parameter ist reserviert.</span><span class="sxs-lookup"><span data-stu-id="2af93-111">This parameter is reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2af93-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2af93-112">Return value</span></span>

<span data-ttu-id="2af93-113">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="2af93-113">Type: **LRESULT**</span></span>

<span data-ttu-id="2af93-114">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="2af93-114">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2af93-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2af93-115">Remarks</span></span>

<span data-ttu-id="2af93-116">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="2af93-116">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> [!Note]  
> <span data-ttu-id="2af93-117">Diese Meldung wird vom Betriebssystem gepostet.</span><span class="sxs-lookup"><span data-stu-id="2af93-117">This message is posted by the operating system.</span></span> <span data-ttu-id="2af93-118">Anwendungen senden diese Nachricht in der Regel nicht.</span><span class="sxs-lookup"><span data-stu-id="2af93-118">Applications typically do not send this message.</span></span>

 

<span data-ttu-id="2af93-119">Designs sind Spezifikationen für die Darstellung von Steuerelementen, sodass das visuelle Element eines Steuer Elements getrennt von seiner Funktionalität behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="2af93-119">Themes are specifications for the appearance of controls, so that the visual element of a control is treated separately from its functionality.</span></span>

<span data-ttu-id="2af93-120">Um ein vorhandenes Design Handle freizugeben, müssen Sie [**closeermedata**](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata)abrufen.</span><span class="sxs-lookup"><span data-stu-id="2af93-120">To release an existing theme handle, call [**CloseThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata).</span></span> <span data-ttu-id="2af93-121">Verwenden Sie zum Abrufen eines neuen Design Handles [**openfomedata**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata).</span><span class="sxs-lookup"><span data-stu-id="2af93-121">To acquire a new theme handle, use [**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata).</span></span>

<span data-ttu-id="2af93-122">Nach der **WM \_** -Übertragung sind alle vorhandenen Design Handles ungültig.</span><span class="sxs-lookup"><span data-stu-id="2af93-122">Following the **WM\_THEMECHANGED** broadcast, any existing theme handles are invalid.</span></span> <span data-ttu-id="2af93-123">Ein Design fähiges Fenster sollte seine bereits vorhandenen Design Handles freigeben und erneut öffnen, wenn es die **WM \_** -Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="2af93-123">A theme-aware window should release and reopen any of its pre-existing theme handles when it receives the **WM\_THEMECHANGED** message.</span></span> <span data-ttu-id="2af93-124">Wenn die [**openrowmedata**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata) -Funktion **null** zurückgibt, sollte das Fenster ohne Design gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="2af93-124">If the [**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata) function returns **NULL**, the window should paint unthemed.</span></span>

## <a name="requirements"></a><span data-ttu-id="2af93-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2af93-125">Requirements</span></span>



| <span data-ttu-id="2af93-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2af93-126">Requirement</span></span> | <span data-ttu-id="2af93-127">Wert</span><span class="sxs-lookup"><span data-stu-id="2af93-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2af93-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2af93-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2af93-129">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2af93-129">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2af93-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2af93-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2af93-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2af93-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2af93-132">Header</span><span class="sxs-lookup"><span data-stu-id="2af93-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="2af93-133"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="2af93-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2af93-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2af93-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="2af93-135">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="2af93-135">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="2af93-136">**Closethmedata**</span><span class="sxs-lookup"><span data-stu-id="2af93-136">**CloseThemeData**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata)
</dt> <dt>

[<span data-ttu-id="2af93-137">**Isdermeactive**</span><span class="sxs-lookup"><span data-stu-id="2af93-137">**IsThemeActive**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-isthemeactive)
</dt> <dt>

[<span data-ttu-id="2af93-138">**OpenThemeData**</span><span class="sxs-lookup"><span data-stu-id="2af93-138">**OpenThemeData**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata)
</dt> </dl>

 

 
