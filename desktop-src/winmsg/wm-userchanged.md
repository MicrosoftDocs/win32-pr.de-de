---
description: Wird an alle Fenster gesendet, nachdem sich der Benutzer angemeldet hat. Wenn sich der Benutzer anmeldet oder anmeldet, aktualisiert das System die benutzerspezifischen Einstellungen. Das System sendet diese Nachricht sofort nach dem Aktualisieren der Einstellungen.
title: WM_USERCHANGED Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowmessages\wm_userchanged.htm
api_name:
- WM_USERCHANGED
api_type:
- HeaderDef
api_location:
- Winuser.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 14458bdafa0bbf4421c67db8102491db4e1fe6b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960656"
---
# <a name="wm_userchanged-message"></a><span data-ttu-id="d3c0e-105">WM \_ userchanged-Meldung</span><span class="sxs-lookup"><span data-stu-id="d3c0e-105">WM\_USERCHANGED message</span></span>

<span data-ttu-id="d3c0e-106">Wird an alle Fenster gesendet, nachdem sich der Benutzer angemeldet hat.</span><span class="sxs-lookup"><span data-stu-id="d3c0e-106">Sent to all windows after the user has logged on or off.</span></span> <span data-ttu-id="d3c0e-107">Wenn sich der Benutzer anmeldet oder anmeldet, aktualisiert das System die benutzerspezifischen Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="d3c0e-107">When the user logs on or off, the system updates the user-specific settings.</span></span> <span data-ttu-id="d3c0e-108">Das System sendet diese Nachricht sofort nach dem Aktualisieren der Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="d3c0e-108">The system sends this message immediately after updating the settings.</span></span>

<span data-ttu-id="d3c0e-109">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="d3c0e-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> [!Note]  
> <span data-ttu-id="d3c0e-110">Diese Meldung wird ab Windows Vista nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d3c0e-110">This message is not supported as of Windows Vista.</span></span>

 


```C++
#define WM_USERCHANGED                  0x0054
```



## <a name="parameters"></a><span data-ttu-id="d3c0e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3c0e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3c0e-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d3c0e-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3c0e-113">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d3c0e-113">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d3c0e-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d3c0e-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3c0e-115">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d3c0e-115">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3c0e-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d3c0e-116">Return value</span></span>

<span data-ttu-id="d3c0e-117">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="d3c0e-117">Type: **LRESULT**</span></span>

<span data-ttu-id="d3c0e-118">Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="d3c0e-118">An application should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3c0e-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3c0e-119">Requirements</span></span>



| <span data-ttu-id="d3c0e-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d3c0e-120">Requirement</span></span> | <span data-ttu-id="d3c0e-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d3c0e-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3c0e-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d3c0e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d3c0e-123">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3c0e-123">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d3c0e-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d3c0e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d3c0e-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d3c0e-125">None supported</span></span><br/>                                                                                |
| <span data-ttu-id="d3c0e-126">Header</span><span class="sxs-lookup"><span data-stu-id="d3c0e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3c0e-127"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="d3c0e-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3c0e-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3c0e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3c0e-129">Übersicht über Windows</span><span class="sxs-lookup"><span data-stu-id="d3c0e-129">Windows Overview</span></span>](windows.md)
</dt> </dl>

 

 
