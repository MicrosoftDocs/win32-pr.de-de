---
description: Benachrichtigt eine Anwendung, wenn eine ausgewählte IME Informationen über die Schriftart benötigt, die vom Kompositionsfenster verwendet wird. Die Anwendung empfängt diesen Befehl über die WM- \_ IME- \_ Anforderungs Nachricht mit Parametern, wie unten gezeigt.
ms.assetid: 46bb71ee-8dc9-4ef0-bc4e-59866c122bf7
title: IMR_COMPOSITIONFONT Benachrichtigungs Code (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be2751944e451475fd0bde9a34d8902dcaf30e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358877"
---
# <a name="imr_compositionfont-notification-code"></a><span data-ttu-id="14e10-104">IMR \_ compositionfont-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="14e10-104">IMR\_COMPOSITIONFONT notification code</span></span>

<span data-ttu-id="14e10-105">Benachrichtigt eine Anwendung, wenn eine ausgewählte IME Informationen über die Schriftart benötigt, die vom Kompositionsfenster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="14e10-105">Notifies an application when a selected IME needs information about the font used by the composition window.</span></span> <span data-ttu-id="14e10-106">Die Anwendung empfängt diesen Befehl über die [**WM- \_ IME- \_ Anforderungs**](wm-ime-request.md) Nachricht mit Parametern, wie unten gezeigt.</span><span class="sxs-lookup"><span data-stu-id="14e10-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameters as shown below.</span></span>


```C++
LRESULT IMR_COMPOSITIONFONT
```



## <a name="parameters"></a><span data-ttu-id="14e10-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="14e10-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14e10-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="14e10-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="14e10-109">Legen Sie auf IMR \_ compositionfont fest.</span><span class="sxs-lookup"><span data-stu-id="14e10-109">Set to IMR\_COMPOSITIONFONT.</span></span>

</dd> <dt>

<span data-ttu-id="14e10-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="14e10-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="14e10-111">Zeiger auf einen Puffer, der eine [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="14e10-111">Pointer to a buffer containing a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span> <span data-ttu-id="14e10-112">Die Anwendung füllt die Werte für das aktuelle Kompositionsfenster aus.</span><span class="sxs-lookup"><span data-stu-id="14e10-112">The application fills in the values for the current composition window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14e10-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="14e10-113">Return Value</span></span>

<span data-ttu-id="14e10-114">Gibt einen Wert ungleich 0 (null) zurück, wenn die Anwendung die [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur füllt.</span><span class="sxs-lookup"><span data-stu-id="14e10-114">Returns a nonzero value if the application fills in the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span> <span data-ttu-id="14e10-115">Andernfalls gibt der Befehl 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="14e10-115">Otherwise, the command returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="14e10-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14e10-116">Remarks</span></span>

<span data-ttu-id="14e10-117">Dieser Befehl kann vom IME an ein Fenster gesendet werden, das das ISC \_ showuicompositionwindow-Flag im [**WM \_ IME \_ SetContext**](wm-ime-setcontext.md) -Nachrichten Handler gelöscht hat.</span><span class="sxs-lookup"><span data-stu-id="14e10-117">This command can be sent by the IME to a window that cleared the ISC\_SHOWUICOMPOSITIONWINDOW flag in the [**WM\_IME\_SETCONTEXT**](wm-ime-setcontext.md) message handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="14e10-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14e10-118">Requirements</span></span>



| <span data-ttu-id="14e10-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="14e10-119">Requirement</span></span> | <span data-ttu-id="14e10-120">Wert</span><span class="sxs-lookup"><span data-stu-id="14e10-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14e10-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="14e10-121">Minimum supported client</span></span><br/> | <span data-ttu-id="14e10-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="14e10-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="14e10-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="14e10-123">Minimum supported server</span></span><br/> | <span data-ttu-id="14e10-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="14e10-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="14e10-125">Header</span><span class="sxs-lookup"><span data-stu-id="14e10-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="14e10-126"><dt>Imm. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="14e10-126"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14e10-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14e10-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14e10-128">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="14e10-128">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="14e10-129">Eingabemethoden-Manager-Befehle</span><span class="sxs-lookup"><span data-stu-id="14e10-129">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="14e10-130">**WM- \_ IME- \_ Anforderung**</span><span class="sxs-lookup"><span data-stu-id="14e10-130">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> <dt>

[<span data-ttu-id="14e10-131">**WM \_ IME \_ SetContext**</span><span class="sxs-lookup"><span data-stu-id="14e10-131">**WM\_IME\_SETCONTEXT**</span></span>](wm-ime-setcontext.md)
</dt> </dl>

 

 
